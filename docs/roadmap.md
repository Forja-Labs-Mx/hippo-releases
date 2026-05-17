# Hippo Roadmap

This roadmap is structured for extension: each milestone is a self-contained
section with status, theme, scope, and acceptance signals. Add new milestones
by appending a new section with the same shape; promote items from `Future`
into a milestone when they're funded.

Status legend:
- ✅ **Shipped** — closed and frozen
- 🟢 **Current** — active focus
- 🟡 **Planned** — committed, sequenced after the current milestone
- ⏸️ **Parked** — deliberately out of the active plan; no timeline
- 🔵 **Exploratory** — interesting, not yet committed
- ⚪ **Future** — captured so it isn't lost; not promised

---

## Alpha 🟢

**Status.** Current. The original Alpha implementation is feature-complete
per the [`docs/plans/alpha/`](plans/alpha/) plan, and the product remains in
Alpha while real use teaches us whether Hippo works, where it works, and where
it doesn't. There is no deadline for moving to Beta. CLI, MCP stdio server,
hybrid search, Dream-Mode hygiene, cross-project promotion, launchd/systemd
installers, and the completed work previously grouped under Beta are now all
part of Alpha. See *Alpha post-shipment enhancements* below.

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

- HTTP API (current Alpha surfaces are CLI, MCP, and TUI; future HTTP
  should be exposed as another `hippo` command from the same binary unless
  a later ADR splits deployment artifacts).
- Multi-device / cloud sync.
- Windows scheduled-Dream installer.
- Vector index via `vtab` module (BLOB + cosine is sufficient at personal
  scale).
- Importing memories from other systems.
- Web UI / dashboard.
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
- **Debug TUI.** `hippo ui` provides a multi-tab master-detail surface
  (Memories | Sessions | Learnings | Review) with inline-chip filters,
  `/` hybrid search, archive-only destructive CRUD, and promotion-review
  flows for Dream- and agent-suggested promotions. See
  [ADR-0037](adr/0037-tui-in-process-service-link.md) and
  [ADR-0038](adr/0038-tui-access-scope.md).
- **Onboarding TUIs.** `hippo setup` and `hippo init` can run through
  TUIs that wrap, rather than replace, the existing flag-based forms.
  `--no-tui` and non-TTY callers keep the scripted path. See
  [ADR-0042](adr/0042-onboarding-tui-wrap-pattern.md) and
  [ADR-0043](adr/0043-onboarding-tui-shape.md).
- **Sessions.** `hippo_session_start` / `_end` / `_summary` / `_get` /
  `_list` group memories into explicit caller-owned work episodes.
  Callers carry `session_id`; Hippo stores rows but holds no per-actor
  state. See [ADR-0039](adr/0039-sessions-explicit-stateless.md).
- **Prompt capture.** Prompts are separate immutable entities with dual
  linkage: direct causal links through `memory_prompts` and contextual
  linkage through session co-membership. See
  [ADR-0040](adr/0040-prompts-separate-entity.md).
- **Topic-key suggestion.** `hippo_topic_key_suggest` helps agents and
  users reuse an existing memory taxonomy without silently auto-selecting
  a topic key. See
  [ADR-0041](adr/0041-topic-key-suggestion-tool.md).
- **Learnings.** Dream can promote reinforced memory clusters into
  first-class learnings, partitioned ahead of memories in search and
  citation budgets. Human-edited learnings are protected from later Dream
  rewrites. See
  [ADR-0027](adr/0027-learnings-as-first-class-entity.md).

---

## Beta ⏸️

**Status.** Parked. Beta is deliberately out of the active roadmap while
Hippo stays in Alpha discovery. There is no timeline, deadline, or implied
release train for moving from Alpha to Beta.

**Theme.** To be redefined after sustained Alpha use. A future Beta should
be justified by observed usage and pain, not by the existence of a prior plan.

**Current commitment.** None. Completed work previously grouped under Beta has
been folded into Alpha. The previous [`docs/plans/beta/`](plans/beta/)
documents remain as historical planning material and implementation reference,
but they are not the active roadmap, a release gate, or a commitment that a
future Beta must ship that exact scope.

**Questions before reviving Beta.**

- Does Hippo reliably help real agents and humans remember useful context
  across sessions?
- Which workflows produce durable memories, and which produce noise?
- Which surfaces are actually needed for curation: CLI, MCP, TUI, WebUI,
  or something smaller?
- Which features are essential enough to stabilize before any beta promise?

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
  who'd rather click than navigate a CLI or TUI. A prior Beta draft put TUI
  first, but no Beta scope is currently committed; the WebUI may follow once
  a real consumer (the user themselves, or an external integration) makes the
  API shape concrete.
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
emoji and add the plan link. When parking a milestone, mark it ⏸️ Parked and
remove any implied scope or deadline. When closing a milestone, change to
✅ Shipped and freeze the section.
