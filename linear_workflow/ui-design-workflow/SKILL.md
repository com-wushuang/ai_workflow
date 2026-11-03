---
name: ui-design-workflow
description: Run only the UI Design lifecycle stage for a named Linear project using installed PM Skills, Linear MCP and Git Markdown; require explicit review gates and stop before the next stage.
---


# UI Design Workflow

## Operating contract
Read `references/operating-contract.md` on entry for authorization, canonical sources, durable approval state, lifecycle mapping and recovery.

## Scope and invocation
Invoke with `使用 $ui-design-workflow 开始 <项目名称> 的UI Design`. Own ONLY this stage. Never start Development Planning or any other lifecycle stage.

## Entry gate

- Read the approved UX specification and flows, approved PRD; check their explicit approval records, versions and linked Linear objects. If missing, pause and request a decision.

- Identify the correct Linear project without creating another one; locate matching milestone and existing issues where possible.

- Inventory existing stage artifacts and resume from confirmed work; do not restart or overwrite without approval.

## Execution phases

### Phase 1: Input and visual artifact discovery
Read approved UX deliverables, PRD, any existing Figma/design system assets. Verify source files are accessible; identify missing visuals.
Summarize material findings and continue; pause only under the operating contract.

### Phase 2: Visual direction and delivery mode
Read existing brand, visual priorities, platform and accessibility constraints. Record delivery mode: Visual Required (default), or Spec Only only on explicit user choice. Tool unavailability does not silently change the mode. Present material unresolved alternatives for selection.
Summarize material findings and continue; pause only under the operating contract.

### Phase 3: Design system
Define tokens, typography, spacing, colors, components, variants, states and responsive rules; validate contrast and accessibility where feasible.
Summarize material findings and continue; pause only under the operating contract.

### Phase 4: High-fidelity screens
Specify or create actual high-fidelity designs only using an available authorized design tool; otherwise create implementation-ready screen specs and clearly label visuals as pending. In Visual Required mode, missing visuals block stage completion; local specs may still be delivered. In explicitly selected Spec Only mode, approve specifications only and record that visual design was not delivered.
Summarize material findings and continue; pause only under the operating contract.

### Phase 5: Design QA and approval
Review against UX flows, consistency, responsive layouts, component states and accessibility. Obtain explicit approval.
Summarize material findings and continue; pause only under the operating contract.

### Phase 6: Linear sync and stop
Show write plan, reuse existing authorization or request it if missing, update only supported objects, verify and STOP.
Summarize material findings and continue; pause only under the operating contract.

## Deliverables

- `docs/design/UI-Spec.md` (Draft until explicitly approved)

- `docs/design/Design-System.md` (Draft until explicitly approved)

- `docs/design/Screen-Inventory.md` (Draft until explicitly approved)

## Mandatory reference material

- `references/ui-spec-template.md`

- `references/design-system-template.md`

- `references/screen-inventory-template.md`

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

