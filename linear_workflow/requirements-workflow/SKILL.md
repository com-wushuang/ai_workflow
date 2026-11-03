---
name: requirements-workflow
description: Convert an approved MVP Scope into a reviewed PRD, user stories and testable acceptance criteria using available PM Skills, Git Markdown and Linear MCP. Use only when the user explicitly requests the requirements stage for a named project.
---

# Requirements Workflow

## Operating contract
Read `references/operating-contract.md` on entry for authorization, canonical sources, durable approval state, lifecycle mapping and recovery.

## Mission and boundary
Own ONLY the Requirements / PRD stage. Never start UX, UI, engineering design, coding, testing or another lifecycle workflow. A recommendation about next steps is not authorization to execute them. On completion, report and STOP.

## Invocation
User supplies a project name, e.g. `使用 $requirements-workflow 开始 BTC Trading OS 的需求定义`.
All stable rules are in this skill; do not ask the user to repeat them.

## Dependencies and discovery
- Work in the current Git repository. Check repository root and existing documents before creating anything.
- Discover actual installed PM Skills and inspect their instructions. Prefer relevant PRD, user-story and acceptance-criteria skills when available. Do not fabricate skill names or assume an orchestration command exists. If missing, use this workflow's templates and say so.
- Discover the Linear MCP tools actually exposed in the current Codex session. Read project, milestone, issues and documents where supported. Never claim unsupported tools exist.
- If the project is ambiguous, ask the user to choose; do not create a new project automatically.

## Entry gate
1. Read `docs/product/Product-Brief.md` and `docs/product/MVP-Scope.md` if present; find equivalent canonical files or Linear links otherwise.
2. Verify that MVP Scope is explicitly approved and identify its version and source. A file's existence or a Linear milestone transition is not approval.
3. If approval is missing or scope conflicts with the Brief, stop and request a decision. Do not silently repair the approved scope.
4. Inventory any existing PRD, user stories, acceptance criteria, decision log, and Linear tasks. Resume from confirmed work; never overwrite without approval.

## Workflow (one phase at a time)
### Phase 1 — Scope traceability
Map each approved MVP capability to its user, problem, intended outcome and source section. Flag missing rationale or ambiguous scope. Ask at most two high-impact questions per round. Continue unless a material decision is unresolved.

### Phase 2 — Requirements discovery
For each in-scope capability, elicit actors, triggers, main flow, alternate/error flows, data and permissions, business rules, integrations and dependencies. Distinguish facts, decisions, assumptions and proposals. Avoid inventing behavior. Pause only for material unresolved decisions.

### Phase 3 — Stories and acceptance criteria
Create testable user stories and scenario-based acceptance criteria (Given/When/Then where useful). Include negative cases, edge cases, and relevant nonfunctional requirements. Assign stable requirement IDs and map them to MVP capabilities. Pause only for material unresolved decisions.

### Phase 4 — PRD drafting
Write `docs/product/PRD.md` and `docs/product/User-Stories.md` using reference templates. Maintain `docs/product/requirements-decision-log.md` and `docs/product/requirements-open-questions.md` as needed. Mark status Draft. Preserve links to Brief and MVP Scope and a requirement-to-scope traceability table. Do not mark approved without explicit user authorization.

### Phase 5 — Review gate
Use `references/review-gate.md`. Inspect scope fidelity, completeness, ambiguity, feasibility questions, testability, contradictions, privacy/security and unresolved decisions. Present findings, ask for corrections, revise. Approval must be an explicit user decision; otherwise leave Draft/Needs Revision.

### Phase 6 — Controlled Linear synchronization
Read `references/linear-sync.md`. Show a concrete write plan (objects, fields, links and status changes). Reuse existing authorization for this batch, or request it if missing. Then call only supported Linear MCP operations; verify by reading back. If Document writes are unsupported, link the canonical Git files or report the limitation. Do not create implementation issues by default; user must separately approve issue decomposition.

### Phase 7 — Stop
Report PRD and stories paths, approval state, open questions, Linear links, and any verification failures. STOP. Do not invoke another skill or start UX/engineering. Never interpret approval of PRD as permission for the next stage.

## Cross-cutting rules
- User owns product decisions. AI suggestions must be labeled as suggestions.
- No more than TWO substantive interview questions per round.
- Internal phases continue without permission requests; summarize material findings.
- Git writes to the working documents are allowed for drafting; never commit, push, merge, delete, or rewrite approved artifacts without explicit approval.
- Linear is a tracker, not the source of truth for PRD text; canonical Markdown in Git is authoritative.
- Authorize Linear changes once per concrete batch under the operating contract.
- Do not treat tool execution success as proof of final state: read back and verify.
- Do not call cross-stage PM Skills orchestration commands even if available.
- If the user asks to pause, stop without progressing; summarize state and resume point.

## Required reference files
Read `references/prd-template.md`, `references/user-stories-template.md`, `references/review-gate.md`, and `references/linear-sync.md` at the relevant phases.
