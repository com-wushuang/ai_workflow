---
name: ux-design-workflow
description: Run only the UX Design lifecycle stage for a named Linear project using installed PM Skills, Linear MCP and Git Markdown; require explicit review gates and stop before the next stage.
---


# UX Design Workflow

## Scope and invocation
Invoke with `使用 $ux-design-workflow 开始 <项目名称> 的UX Design`. Own ONLY this stage. Never start UI Design or any other lifecycle stage.

## Entry gate

- Read the approved PRD and User Stories; check their explicit approval records, versions and linked Linear objects. If missing, pause and request a decision.

- Identify the correct Linear project without creating another one; locate matching milestone and existing issues where possible.

- Inventory existing stage artifacts and resume from confirmed work; do not restart or overwrite without approval.

## Execution phases

### Phase 1: Context and traceability
Read approved PRD, User Stories and MVP Scope. Map priority user stories to personas, tasks, entry points and success outcomes. Check missing decisions.
At phase end, show findings and request confirmation before advancing.

### Phase 2: User journeys and information architecture
Interview for user goals, contexts, navigation, content hierarchy, empty/error/permission states and accessibility needs. Produce journeys and IA.
At phase end, show findings and request confirmation before advancing.

### Phase 3: Task flows and low-fidelity wireframes
Create step-by-step flows and screen inventory, with text wireframe specifications or diagrams. Do not claim a Markdown spec is a finished visual wireframe; link actual Figma/other design files if created with available tools.
At phase end, show findings and request confirmation before advancing.

### Phase 4: Usability validation plan
Define realistic tasks, expected outcomes, high-risk interactions, accessibility and usability checks. Flag untested assumptions.
At phase end, show findings and request confirmation before advancing.

### Phase 5: Review and approval
Use review gate; assess story coverage, consistency, discoverability, error handling and scope. Revise until explicit approval.
At phase end, show findings and request confirmation before advancing.

### Phase 6: Linear sync and stop
Show proposed Linear writes; after authorization sync status and artifact links, verify and STOP.
At phase end, show findings and request confirmation before advancing.

## Deliverables

- `docs/design/UX-Spec.md` (Draft until explicitly approved)

- `docs/design/User-Flows.md` (Draft until explicitly approved)

- `docs/design/Wireframes.md` (Draft until explicitly approved)

## Mandatory reference material

- `references/ux-spec-template.md`

- `references/user-flows-template.md`

- `references/wireframes-template.md`

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

