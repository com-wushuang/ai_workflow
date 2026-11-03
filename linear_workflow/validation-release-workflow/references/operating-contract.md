# Workflow operating contract

Read this contract on entry. It applies within this skill only; explicit user instructions and existing authorization take precedence. Helper skills do not expand the assigned stage or introduce redundant approvals.

## Decisions and authorization
- Invoking the workflow authorizes discovery, analysis, interviews and reversible local draft edits within this stage. Continue between internal phases without asking permission to proceed.
- Ask at most two focused questions per round when material information is missing. Use labeled proposals for routine choices; never invent evidence, metrics or user decisions.
- Pause for material scope/architecture/visual-direction choices that cannot be inferred, unresolved blockers, and final artifact approval. Present a concrete draft before requesting final approval. Silence and tool success are not approval.
- Preserve authorization already given in this conversation. Show one exact Linear batch plan (target IDs/names, operations, fields, links and status transitions); ask only for changes not already authorized. One approval covers all calls in that batch, including safe retries after checking remote state. Re-approval is needed only for material deviations, destructive changes or a changed target.
- Document approval alone does not authorize Linear writes. Never deploy, publish, commit, push, merge or delete unless the user has authorized that action. Stop at the end of this lifecycle stage; do not invoke the next workflow automatically.

## Sources and capabilities
- Git Markdown is canonical for product/engineering text; Linear tracks progress and links. Existing Linear-authoritative projects require an explicit migration decision before creating a competing master; read-only analysis may continue.
- Inspect actual Linear tools and reuse existing objects. Never invent APIs, IDs, URLs or remote success. Read back changed objects and report verified/failed/unverified/manual separately. Resume partial batches from observed state.
- If Linear is unavailable, continue supported local work and record sync as Pending; never call the remote stage complete. Initialization itself requires Linear access.
- Discover only relevant installed PM helper skills and read them before use. They are optional; use the bundled templates if unavailable. Never use a cross-stage orchestrator.

## Durable state and approvals
Maintain `docs/workflow-state.md` in the product repository, one section per stage. Do not create product state inside the skill package. Record:

| Field | Required content |
|---|---|
| stage | Canonical lifecycle stage name |
| status | Draft / Needs Decision / Approved / Needs Reapproval |
| artifacts | Paths and current artifact versions |
| source_versions | Upstream paths and exact versions used |
| approved_versions | Exact versions approved, or Pending |
| approval_reference | Actual explicit user approval, date and conversation reference or faithfully recorded quotation; never invent an identity or message ID |
| exceptions | Conditions, unresolved blockers and approved waivers |
| sync_status | Pending / Verified / Partial / Manual, object IDs and outcomes |
| next_action | Next unfinished action within this stage |

Every deliverable must identify its version and approval status, using existing metadata or a short header. Record approvals against versions, not filenames alone. Before changing approved content, preserve the approved revision (Git history or a local versioned snapshot); obtain a scope decision if the requested change is ambiguous. A substantive change increments the version, marks it Needs Reapproval and identifies affected downstream artifacts. Mark affected downstream stages Needs Reapproval; do not erase earlier approvals or invalidate unrelated work for formatting-only edits. Conditional approval must list its conditions; blocking conditions prevent downstream entry unless explicitly waived for a specified scope.

On resume, read artifacts, this state record and relevant Linear state. Use explicit approval in the conversation if it has not yet been recorded; save it once rather than asking again. Reconcile discrepancies, resume the first unfinished action, and avoid repeating completed interviews or writes. If the user pauses, stop and save the resume point.

## Lifecycle mapping and handoff
| Stage | Linear milestone | Owner / completion evidence |
|---|---|---|
| Product Brief | 01 · Product Definition | product-brief-workflow / approved Brief |
| MVP Planning | 02 · MVP Planning | mvp-planning-workflow / approved Scope |
| Requirements | 03 · Requirements | requirements-workflow / approved PRD and stories |
| UX Design | 04 · UX/UI Design | ux-design-workflow / approved UX artifacts; does not complete shared milestone |
| UI Design | 04 · UX/UI Design | ui-design-workflow / approved agreed UI delivery mode; complete shared milestone only when UX and UI are both approved |
| Development Planning | 05 · Development | development-planning-workflow / approved plan, backlog, test strategy and implementation handoff; does not complete Development |
| Implementation | 05 · Development | separately authorized coding task / build, commit or source revision, test commands/results, defects and deviations |
| Validation & Release | 06 · Validation & Release | validation-release-workflow / evidence-based validation and human go/no-go; actual release remains Pending until deployment evidence exists or a no-release decision is recorded |

For existing custom milestones, record actual IDs and the mapping; never rename/restructure automatically. Implementation is intentionally outside these eight skills. Its handoff must name the coding task/owner (or Pending), inputs, acceptance criteria, required test evidence and return path. Missing owner does not block drafting a plan; missing implementation evidence blocks validation of a release candidate.

## Completion report
Report artifact paths/versions, approval status, unresolved risks, verified Linear changes and sync gaps, then stop. Distinguish local delivery, remote synchronization and actual deployment; none implies the others.
