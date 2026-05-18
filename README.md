# Hippo

A self-hosted, single-binary AI memory system for coding agents and humans.

> **Status:** Alpha. The Alpha milestone described in
> [`docs/plans/alpha/`](docs/plans/alpha/) is feature-complete, but Hippo
> remains in Alpha while real use shows what works, what doesn't, and what
> should stabilize before any Beta commitment. Completed work that was
> previously grouped under Beta is now folded into Alpha. Follow-up
> enhancements have been layered on while the milestone settles: project
> groups for grouped read visibility ([ADR-0034](docs/adr/0034-project-groups.md)),
> ambient agent guidance via `hippo init` and the MCP policy surface
> ([ADR-0035](docs/adr/0035-ambient-agent-guidance.md)), and an
> agent-initiated promotion suggestion flow
> ([ADR-0036](docs/adr/0036-agent-promotion-suggestions.md)). See
> [`docs/roadmap.md`](docs/roadmap.md) for the current Alpha discovery
> posture; Beta is parked with no timeline.

## What it is

Hippo gives any local AI agent — Claude Code, Codex, Cursor, your own — a
persistent place to remember things across sessions. It runs as one Go binary
with one SQLite file. No cloud, no server, no Docker, no API keys for the
core data plane.

## What it does

- **Durable memory CRUD.** Add, read, update, archive, reinforce, relate,
  promote across scopes.
- **Strict scoping.** Project memories stay in the project that wrote them.
  User and global memories are visible everywhere. The boundary is enforced
  on every read, every search, every by-ID lookup.
- **Project groups.** Opt-in groups link related projects so reads (search,
  ask, timeline) can see across the group while writes stay project-scoped
  — see [ADR-0034](docs/adr/0034-project-groups.md).
- **Hybrid search.** FTS5 keyword recall plus semantic re-ranking against
  locally stored embedding vectors.
- **Progressive retrieval.** A cheap broad search, a cheap chronological
  neighborhood read, and an explicit full-body fetch — agents pay for what
  they need.
- **Topic-key upsert.** Saving the same evolving topic doesn't accumulate
  duplicates; it bumps a revision counter.
- **Dream Mode.** Scheduled hygiene: confidence decay, stale detection,
  duplicate suggestions, low-quality and missing-metadata flags, optional
  LLM contradiction and promotion surfacing — all auditable, never
  destructive.
- **Cross-project promotion.** Explicit `memory promote` plus Dream-suggested
  promotions reviewed via `hippo dream review` /
  [`hippo_dream` mode `judge`](docs/adr/0028-cross-project-memory-elevation.md).
- **Defense-in-depth privacy.** `<private>...</private>` spans are redacted
  at the store layer before anything is persisted or indexed.
- **MCP-native.** Tools speak the [Model Context
  Protocol](https://modelcontextprotocol.io) over stdio so any compatible
  agent can wire Hippo up directly.
- **Ambient agent guidance.** `hippo init` installs a repo-local Hippo
  memory skill and idempotent `AGENTS.md` / `CLAUDE.md` blocks; the MCP
  server ships compact instructions plus a `hippo_memory_policy` prompt
  and `hippo://memory-policy` resource — see
  [ADR-0035](docs/adr/0035-ambient-agent-guidance.md).

## Install

Hippo ships for macOS and Linux as a single CGO-free binary. The release
pipeline publishes public GitHub Release archives to
`Forja-Labs-Mx/hippo-releases`, Homebrew cask metadata to
`Forja-Labs-Mx/homebrew-tap`, and Linux package files for each release PR merged
to `main`.

With Homebrew:

```sh
brew tap Forja-Labs-Mx/tap
brew install --cask hippo
brew upgrade --cask hippo
brew uninstall --cask hippo
```

From a GitHub Release archive:

```sh
curl -LO https://github.com/Forja-Labs-Mx/hippo-releases/releases/download/vX.Y.Z/hippo_vX.Y.Z_darwin_arm64.tar.gz
tar -xzf hippo_vX.Y.Z_darwin_arm64.tar.gz
install -m 0755 hippo ~/.local/bin/hippo
hippo --version
```

With a local Linux package file:

```sh
sudo apt install ./hippo_VERSION_linux_amd64.deb
sudo dnf install ./hippo_VERSION_linux_amd64.rpm
sudo apk add --allow-untrusted ./hippo_VERSION_linux_amd64.apk
```

To build from source, clone the repo and check out a release tag:

```sh
git checkout vX.Y.Z
CGO_ENABLED=0 go build -trimpath -o hippo ./apps/hippo
```

Or, using the monorepo's Turborepo wiring:

```sh
aube install --ignore-scripts
aube run --no-install turbo -- run build --filter=@hippo/app
# binary lands at apps/hippo/dist/hippo
```

User-local config and state live under `~/.hippo/`:

- `~/.hippo/config.yaml` — YAML config (embedding provider, model, …).
- `~/.hippo/hippo.db` — SQLite database (memories, embeddings, audit,
  scheduled Dream run history).
- `~/.hippo/logs/` — log files from scheduled Dream runs.

## Quickstart

Hippo's main path is agent-first: set it up once globally, then opt projects
in one at a time. After that, your agent should use Hippo through MCP without
you running memory commands by hand.

```sh
hippo setup                                # global config, provider presets, agent MCP install, Dream scheduler
cd /path/to/project
hippo init                                 # project registration and repo-local agent guidance
```

During setup, Hippo installs MCP entries for any combination of Codex, Claude,
Cursor, and OpenCode, and writes provider presets for OpenAI, Anthropic, or
Ollama as the text provider and OpenAI or Ollama as the embedding provider.
Setup can also opt into native notifications for background scheduled Dream
failures; notifications are failure-only and do not fire for manual
`hippo dream run` commands. For scripted installs, pass flags directly:

```sh
hippo setup --agent codex --agent claude --text-provider openai --embedding-provider openai
hippo setup --agent codex --text-provider ollama --embedding-provider ollama --notify-on-failure
```

The agent MCP entry runs `hippo mcp serve`; users normally do not run that
command directly. MCP serving is always pinned to one workspace root so
agent-supplied `path` values cannot pivot into unrelated repositories. By
default the server pins to its own current working directory at startup, which
is the project the agent was launched from. For non-default deployments you can
override that pin with `--workspace-root <dir>` or
`HIPPO_WORKSPACE_ROOT=<dir>`. `hippo setup` writes a plain `hippo mcp serve`
entry into managed agent configs (no baked-in path), so the same global config
keeps working as you switch between worktrees and sibling projects. The CLI
commands below remain available for manual curation, debugging, and advanced
workflows. Every command supports `--output text|json` and `--config <path>`.

## CLI surface

| Command | Purpose |
|---|---|
| `hippo setup` | Initialize global config + database, optionally install agent MCP entries, configure provider presets, and install the Dream scheduler. |
| `hippo init` | Register the current project and install repo-local agent guidance. |
| `hippo project init` / `status` | Link the current worktree to a Hippo project; show the active project and its groups. |
| `hippo project group create` / `add` / `remove` / `list` / `show` / `relate` | Manage project groups and the unordered descriptions that explain how grouped projects relate. |
| `hippo memory add` / `get` / `list` / `update` / `archive` / `delete` / `promote` | Curate memories. `delete` is a hard, audit-logged removal; everything else is soft. |
| `hippo search <query>` | Hybrid (FTS5 + cosine) search, optionally `--scope` filtered. |
| `hippo ask <question>` | RAG-style answer drawn from visible memories. |
| `hippo embedding rebuild` | Re-enqueue embedding jobs for live memories. |
| `hippo dream run` | Deterministic Dream phases (decay, stale, duplicate, low-quality, missing-metadata). |
| `hippo dream review` | Resolve a pending suggestion (`accept` / `accept_with_rewrite` / `dismiss`). |
| `hippo dream install` / `uninstall` / `status` | Manage the recurring launchd/systemd job and inspect scheduled-run health. |
| `hippo mcp serve` | Serve the default entity-router MCP surface over stdio MCP, rejecting paths outside the workspace root (defaults to cwd; override with `--workspace-root <dir>`). |
| `hippo mcp serve --surface legacy` | Serve the pre-router MCP tool surface for local eval/debug compatibility, rejecting paths outside the workspace root (defaults to cwd; override with `--workspace-root <dir>`). |
| `hippo mcp eval-toolset` | Compare model tool-use efficiency across legacy and entity MCP surfaces using the configured text provider. |

Run any command with `--help` for full flag documentation.

## MCP tools

`hippo mcp serve` exposes the compact entity-router surface by default:

- `hippo_memory(mode: "add" | "get" | "update" | "archive" |
  "reinforce" | "relate" | "promote" | "suggest_promotion" |
  "suggest_topic_key" | "timeline")`
- `hippo_session(mode: "start" | "end" | "summary" | "get" | "list")`
- `hippo_prompt(mode: "record" | "get" | "list" | "archive")`
- `hippo_learning(mode: "get" | "list" | "update" | "archive" |
  "unarchive" | "reinforce")`
- `hippo_project(mode: "ensure" | "group_create" | "group_add" |
  "group_remove" | "group_list" | "group_show" | "group_relate")`
- `hippo_preference(mode: "set" | "get" | "list" | "delete")`
- **Retrieval / governance** — `hippo_search`, `hippo_ask`, `hippo_audit`,
  plus conditional `hippo_dream(mode: "judge")`
- **Agent guidance** — server instructions plus `hippo_memory_policy` prompt and
  `hippo://memory-policy` resource.

The pre-router per-verb tool catalog is available with
`hippo mcp serve --surface legacy` for local comparison and short-term debug
compatibility during alpha.

MCP does not create project rows by default. Run `hippo project init` or
`hippo init` from a repository before using MCP tools there. The
`--allow-project-provisioning` serve flag is an explicit compatibility escape
hatch for trusted local workflows; leave it off for normal agent use.

Hard delete is intentionally CLI-only — see
[ADR-0015](docs/adr/0015-hard-delete-cli-only.md).

## Where to learn more

- [`docs/plans/alpha/`](docs/plans/alpha/) — the Alpha plan, sectioned by
  topic. Start with [`abstract.md`](docs/plans/alpha/abstract.md) for the
  whole picture, or jump to a specific area.
- [`docs/adr/`](docs/adr/) — architecture decision records. Every load-bearing
  technical choice is captured here with its context and consequences.
- [`docs/roadmap.md`](docs/roadmap.md) — current Alpha posture, parked Beta,
  and unscheduled 1.0 / Future candidates.

## Development

This repository is organized as an aube/Turborepo monorepo. `apps/hippo` is a
thin binary wrapper (`main.go` only) and `packages/core` (`@hippo/core`) owns
the entire product implementation: the Cobra command tree (`packages/core/cli`,
including `mcp serve`), the MCP server, the feature packages, and shared
infrastructure — see [ADR-0033](docs/adr/0033-single-binary-core-workspace.md).
The workspace uses `aube-lock.yaml` as the package lockfile and
`packageManager: "npm@11.12.1"` only as Turborepo compatibility metadata until
Turbo supports aube directly; aube is the package manager used for installs,
scripts, CI, Docker builds, and hooks. The local `.npmrc` disables aube's
package-manager strictness for that explicit compatibility exception.

```sh
aube install --ignore-scripts
aube run --no-install build           # turbo: builds apps/hippo
aube run --no-install test            # turbo: unit tests across the monorepo
aube run --no-install integration-tests
aube run --no-install lint
aube run --no-install fmt:check
aube run --no-install check           # format:check + lint + check-types + test
```

For Go-specific workflows, the `Makefile` exposes the underlying targets:

```sh
make test               # go test -short ./... (root + packages/core + apps/hippo)
make test-integration   # go test -tags=integration ./...
make lint               # golangci-lint
make vulncheck          # govulncheck
```

To build only the binary app:

```sh
aube run --no-install turbo -- run build --filter=@hippo/app
```

Release automation is documented in [`docs/release.md`](docs/release.md).

## License

See [LICENSE](LICENSE).
