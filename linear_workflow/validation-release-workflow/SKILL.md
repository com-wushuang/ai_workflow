---
name: validation-release-workflow
description: Run only the Validation & Release lifecycle stage for a named Linear project using installed PM Skills, Linear MCP and Git Markdown; require explicit review gates and stop before the next stage.
---


# Validation & Release Workflow

## Scope and invocation
Invoke with `使用 $validation-release-workflow 开始 <项目名称> 的Validation & Release`. Own ONLY this stage. Never start none or any other lifecycle stage.

## Entry gate

- Read the approved PRD, MVP scope, technical plan, implemented build and test evidence; check their explicit approval records, versions and linked Linear objects. If missing, pause and request a decision.

- Identify the correct Linear project without creating another one; locate matching milestone and existing issues where possible.

- Inventory existing stage artifacts and resume from confirmed work; do not restart or overwrite without approval.

## Execution phases

### Phase 1: Release candidate inventory
Read approved acceptance criteria, MVP success metrics, build/commit references, available tests and Linear issues. If no build/evidence exists, report blocked and stop.
At phase end, show findings and request confirmation before advancing.

### Phase 2: Validation matrix
Map requirements and user journeys to test evidence, defects, risk levels and pass/fail/unknown statuses. Never invent test results.
At phase end, show findings and request confirmation before advancing.

### Phase 3: User acceptance and MVP evaluation
Prepare UAT scenarios and measurement plan; collect actual evidence when available. Distinguish proposed metrics from observed data.
At phase end, show findings and request confirmation before advancing.

### Phase 4: Release readiness
Review security/privacy, performance, operations, deployment, rollback, support and known issues. Recommend go/no-go with explicit uncertainties.
At phase end, show findings and request confirmation before advancing.

### Phase 5: Human go/no-go
Present release decision packet. User alone authorizes release; approval to prepare does not authorize deploy or publish.
At phase end, show findings and request confirmation before advancing.

### Phase 6: Linear sync and stop
With separate approval, sync release evidence and task statuses. Verify and STOP. Never deploy or publish unless separately and explicitly requested with appropriate tools.
At phase end, show findings and request confirmation before advancing.

## Deliverables

- `docs/release/Validation-Report.md` (Draft until explicitly approved)

- `docs/release/Release-Readiness.md` (Draft until explicitly approved)

- `docs/release/Release-Decision.md` (Draft until explicitly approved)

## Mandatory reference material

- `references/validation-report-template.md`

- `references/release-readiness-template.md`

- `references/release-decision-template.md`

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

