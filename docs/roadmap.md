# Hippo Roadmap

This roadmap is structured for extension: each milestone is a self-contained
section with status, theme, scope, and acceptance signals. Add new milestones
by appending a new section with the same shape; promote items from `Future`
into a milestone when they're funded.

Status legend:
- ✅ **Shipped** — closed and frozen
- 🟢 **Current** — actively being built
- 🟡 **Planned** — committed, sequenced after the current milestone
- 🔵 **Exploratory** — interesting, not yet committed
- ⚪ **Future** — captured so it isn't lost; not promised

---

## Alpha ✅

**Status.** Shipped — feature-complete per the
[`docs/plans/alpha/`](plans/alpha/) plan. CLI, MCP stdio server, hybrid
search, Dream-Mode hygiene, cross-project promotion, and launchd/systemd
installers are all implemented and covered by unit + integration tests.
Several post-shipment enhancements landed under the Alpha umbrella before
Beta begins — see *Alpha post-shipment enhancements* below.

**Theme.** Local-first, single-binary memory system. Strict scoping,
hybrid search, Dream-Mode hygiene, MCP-native. Everything else is deferred.

**In scope.**

- Cobra CLI: `setup`, `project init`, `mcp serve`, `memory ...`, `search`,
  `ask`, `dream ...`, `embedding rebuild`.
- MCP stdio server with the full tool surface: `hippo_memory_add`,
  `hippo_memory_add_structured`, `hippo_memory_get`, `hippo_memory_update`,
  `hippo_memory_archive`, `hippo_memory_reinforce`, `hippo_memory_relate`,
  `hippo_memory_promote`, `hippo_search`, `hippo_memory_timeline`,
  `hippo_ask`, `hippo_project_ensure`, `hippo_preference_set` /
  `_get` / `_list` / `_delete`, `hippo_judge`, `hippo_audit`. (Hard
  delete is intentionally CLI-only — see
  [ADR-0015](adr/0015-hard-delete-cli-only.md).)
- Pure-Go data layer: `modernc.org/sqlite` + `sqlc` + `golang-migrate`.
- Embeddings via OpenAI-compatible HTTP, stored as BLOB, ranked by in-Go
  cosine. Default model: `text-embedding-3-large`.
- Topic-key upsert, relationship annotations, store-layer `<private>`
  redaction, audit log on every mutation.
- Cross-project memory elevation: explicit `hippo_memory_promote` plus
  Dream-suggested promotions reviewed via `hippo_judge` /
  `hippo dream review`. See
  [ADR-0028](adr/0028-cross-project-memory-elevation.md).
- Dream Mode deterministic phases (decay/dedup/stale/low-quality/missing-
  metadata), optional LLM phases (summary/relation/contradiction).
- macOS `launchd` and Linux `systemd` installers for scheduled Dream.
- TDD-sliced build (21 slices), strict `AccessContext` enforcement,
  exhaustive by-ID leakage regression suite.

**Out of scope (deferred to later milestones).**

- Sessions, prompt capture, topic-key suggestion tool.
- HTTP API (only CLI + MCP in Alpha; future HTTP should be exposed as
  another `hippo` command from the same binary unless a later ADR splits
  deployment artifacts).
- Multi-device / cloud sync.
- Windows scheduled-Dream installer.
- Vector index via `vtab` module (BLOB + cosine is sufficient at personal
  scale).
- Importing memories from other systems.
- Web UI / TUI / dashboard.
- Auto-capture of raw agent tool calls — see ADR-0024 (this is a stated
  non-goal, not a deferral).

**Acceptance signals.**

- `go build ./...` produces a CGO-free binary on macOS, Linux, Windows.
- `go test ./...` and `go test -tags=integration ./...` are green.
- A working agent integration end-to-end: register a project, save a
  memory from one cwd, find it from a worktree, *don't* find it from an
  unrelated repo.
- Dream runs scheduled by `launchd`/`systemd` produce audit and
  review-suggestion rows without ever hard-deleting.

**Plan.** [`docs/plans/alpha/`](plans/alpha/).

---

## Alpha post-shipment enhancements ✅

**Status.** Shipped on top of Alpha. These were small, load-bearing
additions to the Alpha surface rather than new milestones; each is
preserved as its own ADR so future readers don't have to git-archaeology
the change.

- **Workspace split.** `apps/hippo` is reduced to a thin binary
  wrapper; the entire product implementation moved to
  `packages/core` (`@hippo/core`). One `hippo` binary still ships.
  See [ADR-0033](adr/0033-single-binary-core-workspace.md).
- **Project groups.** New `project_groups`, `project_group_members`,
  and `project_group_pair_descriptions` tables, `ProjectService`
  group APIs, `hippo project group {create,add,remove,list,show,relate}`
  CLI, and `hippo_project_group_*` MCP tools. Groups link related
  projects so reads (search, ask, timeline, memory `get` /
  `list` / `timeline`) can span the group via
  `AccessContext.ReadableProjectIDs`; writes stay project-scoped, and
  audit-logged group mutations require `AllowGlobalWrite`. See
  [ADR-0034](adr/0034-project-groups.md).
- **Ambient agent guidance.** `hippo init` registers the project and
  installs a repo-local Hippo memory skill at
  `.agents/skills/hippo-memory/SKILL.md` and
  `.claude/skills/hippo-memory/SKILL.md`, plus an idempotent
  `<!-- BEGIN HIPPO MEMORY -->`…`<!-- END HIPPO MEMORY -->` block in
  `AGENTS.md` and `CLAUDE.md`. The MCP server emits compact
  Instructions for ambient discovery and exposes the canonical policy
  as the `hippo_memory_policy` prompt and `hippo://memory-policy`
  resource. Each Hippo memory MCP tool now ships an enriched
  when-to-use description. See
  [ADR-0035](adr/0035-ambient-agent-guidance.md).
- **Agent-initiated promotion suggestions.** New MCP tool
  `hippo_memory_suggest_promotion` lets an agent surface a project
  memory as a candidate for elevation to user scope. Hippo writes a
  pending `review_suggestions(kind='promotion')` row sourced from the
  agent; the existing `hippo_judge` / `hippo dream review` workflow
  owns acceptance. Suggestions deduplicate by suppressing repeats
  while a prior suggestion is pending/accepted, and by re-emitting
  when the source memory's revision or reinforcement counts change.
  See [ADR-0036](adr/0036-agent-promotion-suggestions.md).
- **Promotion scoring carries reinforcement and group context.** The
  Dream promotion phase now factors `revision_count`,
  `reinforcement_count`, and the source memory's `ProjectGroups`
  into the score and payload; agent-sourced suggestions include the
  same context for human/LLM review.

---

## Beta ✅

**Status.** Shipped — feature-complete per the
[`docs/plans/beta/`](plans/beta/) plan. Debug TUI, onboarding TUIs,
sessions, prompts, topic-key suggestion, learnings, and the Beta
acceptance signals are all implemented and covered by unit +
integration tests.

**Theme.** TUI-first debug + agent ergonomics on top of the Alpha core.
The user can finally see and curate their data; agents capture sessions
and prompts; Dream synthesizes learnings from reinforced clusters.

**In scope.**

- **Debug TUI** entered via `hippo ui`. Multi-tab master-detail
  (Memories | Sessions | Learnings | Review) with inline-chip filters,
  `/` hybrid search, and archive-only CRUD (hard delete stays CLI-only
  per [ADR-0015](adr/0015-hard-delete-cli-only.md)). Promotion-review
  surface for Dream- and agent-suggested promotions. See
  [ADR-0037](adr/0037-tui-in-process-service-link.md) and
  [ADR-0038](adr/0038-tui-access-scope.md).
- **Setup TUI** wrapping `hippo setup` and **Project-init TUI** wrapping
  `hippo init`. Both wrap (not replace) the existing flag-based forms;
  `--no-tui` and non-TTY callers keep the current path. See
  [ADR-0042](adr/0042-onboarding-tui-wrap-pattern.md).
- **Sessions.** `hippo_session_start` / `_end` / `_summary` / `_get` /
  `_list`. Explicit + stateless: callers carry `session_id`; Hippo
  stores rows but holds no per-actor state. Schema adds `sessions` and
  a nullable `memories.session_id` FK. New Dream LLM phase summarizes
  closed-but-unsummarized sessions. See
  [ADR-0039](adr/0039-sessions-explicit-stateless.md).
- **Prompt capture.** Separate entity from memories with dual linkage
  (explicit `memory_prompts` M:M for direct causal; session
  co-membership for context). Schema adds `prompts`, `memory_prompts`,
  `prompt_embeddings`. Prompts are immutable post-record, searchable
  but rank-deprioritized in `hippo_search` and `hippo_ask`. See
  [ADR-0040](adr/0040-prompts-separate-entity.md).
- **Topic-key suggestion tool.** Standalone `hippo_topic_key_suggest`
  MCP tool + CLI mirror + Debug TUI integration in the new-memory form.
  Never inline auto-suggest. See
  [ADR-0041](adr/0041-topic-key-suggestion-tool.md).
- **Learnings (memory → pattern promotion).** First-class entity parallel
  to memories, Dream-promoted from reinforced clusters with LLM
  synthesis. Hard-partitioned in `hippo_search` (Learnings block before
  Memories block); learnings-first citation budget in `hippo_ask`.
  Editable post-synthesis via `hippo_learning_update`; `human_edited_at`
  marker blocks subsequent Dream rewrites. See
  [ADR-0027](adr/0027-learnings-as-first-class-entity.md) (Accepted).

**Out of scope (deferred to 1.0 or later milestones).**

- **HTTP API.** No consumer in Beta after WebUI deferral. Revisit when
  a real consumer (the WebUI, or an external script / extension)
  drives the API shape.
- **WebUI.** Deferred. When/if built, it will be a **local-only** Go
  `net/http` + HTMX + `html/template` server bound to `127.0.0.1`,
  single binary, no JavaScript toolchain.
- **Windows scheduled Dream.** Task Scheduler installer is deferred —
  current users are on macOS / Linux.
- **Hard delete in the TUI** stays CLI-only per
  [ADR-0015](adr/0015-hard-delete-cli-only.md). The TUI's destructive
  primitive is *archive* (reversible via Unarchive).
- **Bulk write operations in the TUI.** Single-row writes only in v1;
  bulk earns its slice when usage shows the need.
- **Multi-device / cloud sync.** Stays in 1.0.
- **Vector index via `vtab` module.** BLOB + Go cosine is still
  sufficient at personal scale.
- **Auto-capture of raw agent tool calls.** Stated non-goal per
  [ADR-0024](adr/0024-curated-memories-only.md).

**Acceptance signals.**

- `go build ./...` produces a CGO-free binary on macOS, Linux, Windows.
- `go test ./...` and `go test -tags=integration ./...` are green —
  including new `session/`, `prompt/`, `learning/` packages and the
  three TUI trees (`tui/{widgets,setup,init,debug}/`).
- **Onboarding TUI E2E** (`teatest`): fresh `hippo setup` completes
  via TUI; re-run loads existing config as defaults; `--no-tui`
  falls back to the flag-based form unchanged. `hippo init` writes
  the project record and installs the agent-scaffolding files per
  [ADR-0035](adr/0035-ambient-agent-guidance.md).
- **Debug TUI E2E** (`teatest`): launch `hippo ui` over a seeded DB
  spanning multiple projects; default view shows everything readable
  with the CWD project pinned; filter chips, `/` hybrid search, CRUD
  verbs, and the Review tab all round-trip through services.
- **Sessions E2E**: `_start` → memory adds → `_end` → `_summary`;
  Dream summary phase populates closed-but-unsummarized sessions.
  Closed-session writes are rejected.
- **Prompts E2E**: `_record` a prompt, link memories via
  `prompt_ids`, browse via memory-detail panels, filter chip, and
  `:prompts` palette. Search returns prompts with the `(prompt)`
  indicator and rank-deprioritized score.
- **Topic-key suggestion E2E**: tool returns top-5 with `exists`
  flags scoped to the target catalog; LLM-unavailable returns the
  envelope error pattern. TUI `tab` flow integrates suggestion into
  the new-memory form.
- **Learnings E2E**: Dream cluster-synthesis produces a `learning`
  with linked `learning_sources`; manual edit sets `human_edited_at`;
  subsequent Dream run does not rewrite the edited learning;
  `hippo_search` hard-partitions; `hippo_ask` cites learnings first.
- **Audit fidelity**: every TUI write produces an audit row with
  `actor: tui`.
- **Alpha acceptance signals continue to pass** (no regression).

**Plan.** [`docs/plans/beta/`](plans/beta/).

---

## Beta post-shipment enhancements ✅

**Status.** Shipped on top of Beta. This bucket is reserved for small,
load-bearing additions that land before the next milestone and should be
remembered with Beta rather than promoted into their own milestone.

No post-shipment enhancements have landed yet.

---

## 1.0 🔵

**Theme.** Production-ready, multi-device.

**Candidate scope.**

- **Append-only chunk sync.** Content-hashed, compressed chunks with a
  small append-only manifest. Merge-conflict-safe by construction.
  Suitable for git-backed sync between machines.
- **Vector index module.** A `modernc.org/sqlite/vtab`-backed vector
  module if BLOB + Go cosine starts hitting latency walls on real
  corpora.
- **Stable schema, semver guarantees.**
- **Backup / restore commands.**

---

## Future ⚪

Captured so the ideas aren't lost. No commitment, no sequencing.

- Local WebUI (HTMX-rendered, `127.0.0.1`-bound, single binary) for users
  who'd rather click than navigate a TUI. Beta lands the TUI;
  the WebUI may follow once a real consumer (the user themselves, or an
  external integration) makes the API shape concrete.
- Multi-user / multi-tenant deployments.
- Importer for memories from external systems.
- Plugin/extension surface for custom Dream phases.
- Multimodal memories (images, audio transcripts).
- Encrypted-at-rest store option.
- Per-memory expiration / TTL policies beyond Dream's confidence decay.

---

## How to extend this file

When adding a milestone:

1. Append a new top-level `## <Name> <emoji>` section after the last
   committed milestone.
2. Fill in **Theme**, **In scope** (or **Candidate scope**), **Out of
   scope**, **Acceptance signals**.
3. Cross-link the corresponding plan directory once one exists
   (`docs/plans/<name>/`).
4. Move items out of `Future` into the new milestone's scope when they're
   funded.

When promoting a milestone from 🟡 Planned to 🟢 Current, update the status
emoji and add the plan link. When closing a milestone, change to ✅ Shipped
and freeze the section.
