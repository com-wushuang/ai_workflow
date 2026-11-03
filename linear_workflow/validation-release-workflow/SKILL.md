---
name: validation-release-workflow
description: Run only the Validation & Release lifecycle stage for a named Linear project using installed PM Skills, Linear MCP and Git Markdown; require explicit review gates and stop before the next stage.
---


# Validation & Release Workflow

## Operating contract
Read `references/operating-contract.md` on entry for authorization, canonical sources, durable approval state, lifecycle mapping and recovery.

## Scope and invocation
Invoke with `使用 $validation-release-workflow 开始 <项目名称> 的Validation & Release`. Own ONLY this stage. Do not start another lifecycle stage or deploy automatically.

## Entry gate

- Read the approved PRD, MVP scope, technical plan, implemented build and test evidence; check their explicit approval records, versions and linked Linear objects. If approved source decisions are missing, pause for the missing decision. If build or execution evidence is missing, report the specific blocker and stop without a redundant approval request.

- Identify the correct Linear project without creating another one; locate matching milestone and existing issues where possible.

- Inventory existing stage artifacts and resume from confirmed work; do not restart or overwrite without approval.

## Execution phases

### Phase 1: Release candidate inventory
Read `docs/engineering/Implementation-Handoff.md`, `docs/engineering/Implementation-Evidence.md` (or verified equivalents), approved acceptance criteria, MVP success metrics, build/commit references, available tests and Linear issues. If no build/evidence exists, report blocked and stop.
When entry evidence is present, summarize material findings and continue; otherwise preserve the blocked state. Pause under the operating contract as needed.

### Phase 2: Validation matrix
Map requirements and user journeys to test evidence, defects, risk levels and pass/fail/unknown statuses. Never invent test results.
When entry evidence is present, summarize material findings and continue; otherwise preserve the blocked state. Pause under the operating contract as needed.

### Phase 3: User acceptance and MVP evaluation
Prepare UAT scenarios and measurement plan; collect actual evidence when available. Distinguish proposed metrics from observed data.
When entry evidence is present, summarize material findings and continue; otherwise preserve the blocked state. Pause under the operating contract as needed.

### Phase 4: Release readiness
Review security/privacy, performance, operations, deployment, rollback, support and known issues. Recommend go/no-go with explicit uncertainties.
When entry evidence is present, summarize material findings and continue; otherwise preserve the blocked state. Pause under the operating contract as needed.

### Phase 5: Human go/no-go
Present release decision packet. User alone authorizes release; approval to prepare does not authorize deploy or publish.
When entry evidence is present, summarize material findings and continue; otherwise preserve the blocked state. Pause under the operating contract as needed.

### Phase 6: Linear sync and stop
With batch authorization (reuse existing approval), sync release evidence and task statuses. Verify and STOP. Never deploy or publish unless separately and explicitly requested with appropriate tools.
When entry evidence is present, summarize material findings and continue; otherwise preserve the blocked state. Pause under the operating contract as needed.

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
- Ask at most two substantive questions per round; internal phase transitions do not require approval.
- Discover installed PM Skills and read their actual SKILL.md before using them. Use only skills relevant to this stage; never invoke a cross-stage orchestrator. If unavailable, use this skill's own reference templates.
- Discover actual Linear MCP capabilities, read the named project and its milestones/issues first, and reuse existing objects. Never invent tool names or pretend unsupported operations succeeded.
- Follow the operating contract for batch write authorization and read-back verification; do not ask again for an authorized batch.
- Git Markdown is the canonical source for text deliverables. Check existing files and resume; don't overwrite approved content without permission. Do not git commit, push, merge or delete without explicit authorization.
- If entry approvals are missing, stop and ask. File presence, a completed issue or an advanced milestone alone do not prove approval.
- On completion, report artifact paths, approval status, unresolved risks and verified Linear changes, then STOP. Never start the next lifecycle stage or ask its interview questions.
- A natural-language recommendation for the next stage is informational, not permission to execute it.

