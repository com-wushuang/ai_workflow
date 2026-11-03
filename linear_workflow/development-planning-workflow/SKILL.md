---
name: development-planning-workflow
description: Run only the Development Planning lifecycle stage for a named Linear project using installed PM Skills, Linear MCP and Git Markdown; require explicit review gates and stop before the next stage.
---


# Development Planning Workflow

## Scope and invocation
Invoke with `使用 $development-planning-workflow 开始 <项目名称> 的Development Planning`. Own ONLY this stage. Never start Validation & Release or any other lifecycle stage.

## Entry gate

- Read the approved PRD, UX and UI deliverables; check their explicit approval records, versions and linked Linear objects. If missing, pause and request a decision.

- Identify the correct Linear project without creating another one; locate matching milestone and existing issues where possible.

- Inventory existing stage artifacts and resume from confirmed work; do not restart or overwrite without approval.

## Execution phases

### Phase 1: Technical discovery
Read approved product and design artifacts, repo architecture, conventions and existing code; map dependencies and constraints. Do not change code.
At phase end, show findings and request confirmation before advancing.

### Phase 2: Architecture and tradeoffs
Develop architecture options, data/API contracts, integration points, security, performance and operational concerns. Present tradeoffs for user decisions.
At phase end, show findings and request confirmation before advancing.

### Phase 3: Work breakdown
Map approved requirements into epics/tasks with acceptance criteria, dependencies, estimates as ranges, and implementation order. Do not create issues yet.
At phase end, show findings and request confirmation before advancing.

### Phase 4: Verification and rollout plan
Define test strategy, quality gates, migration, observability, rollback and release dependencies.
At phase end, show findings and request confirmation before advancing.

### Phase 5: Review and approval
Check requirement traceability, feasibility, missing design decisions, risks and sequencing; request explicit approval.
At phase end, show findings and request confirmation before advancing.

### Phase 6: Linear sync and stop
Show proposed epics/issues, links and statuses; request separate authorization; create/update supported objects, verify and STOP. No coding.
At phase end, show findings and request confirmation before advancing.

## Deliverables

- `docs/engineering/Technical-Plan.md` (Draft until explicitly approved)

- `docs/engineering/Implementation-Backlog.md` (Draft until explicitly approved)

- `docs/engineering/Test-Strategy.md` (Draft until explicitly approved)

## Mandatory reference material

- `references/technical-plan-template.md`

- `references/backlog-template.md`

- `references/test-strategy-template.md`

- `references/review-gate.md`

- `references/linear-sync.md`



## Shared operating rules
- User makes all product and approval decisions. Clearly distinguish confirmed facts, assumptions, and AI proposals.
- Ask no more than TWO substantive questions per interview turn. At the end of each phase, recap and request explicit approval to advance within this stage.
- Discover installed PM Skills and read their actual SKILL.md before using them. Use only skills relevant to this stage; never invoke a cross-stage orchestrator. If unavailable, use this skill's own reference templates.
- Discover actual Linear MCP capabilities, read the named project and its milestones/issues first, and reuse existing objects. Never invent tool names or pretend unsupported operations succeeded.
- Before EVERY Linear write, present an exact write plan and obtain separate explicit authorization; after writing, read back and verify. A document approval is not automatically authorization to write to Linear.
- Git Markdown is the canonical source for text deliverables. Check existing files and resume; don't overwrite approved content without permission. Do not git commit, push, merge or delete without explicit authorization.
- If entry approvals are missing, stop and ask. File presence, a completed issue or an advanced milestone alone do not prove approval.
- On completion, report artifact paths, approval status, unresolved risks and verified Linear changes, then STOP. Never start the next lifecycle stage or ask its interview questions.
- A natural-language recommendation for the next stage is informational, not permission to execute it.

