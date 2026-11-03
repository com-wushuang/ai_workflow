---
name: product-brief-workflow
description: Facilitate a product definition workflow using installed PM Skills, a Git-tracked Product Brief, and Linear MCP for project tracking. Trigger when asked to start, continue, or review a Product Brief for a named Linear project.
---

# Product Brief Workflow

## Operating contract
Read `references/operating-contract.md` on entry for authorization, canonical sources, durable approval state, lifecycle mapping and recovery.

## Invocation
User only needs to name a product or Linear project, e.g. `Use $product-brief-workflow to start product definition for BTC Trading OS`.

## Operating contract
- Run from the product's Git repository. If none is open, ask for the repository path before creating files; do not invent a repo.
- Read `references/brief-template.md`, `references/review-gate.md`, and `references/linear-sync.md` when needed.
- First discover available Linear MCP tools and installed PM Skills. Do not assume specific tools or skill names exist; read their instructions before invoking. Prefer relevant PM Skills for problem statements, hypotheses, and value proposition, but adapt to what is installed.
- Read the named Linear Project, its Product Definition milestone (or equivalent), relevant issues and linked resources. If project is ambiguous, ask which one. Do not create a duplicate project or milestone.
- Treat Linear as the tracker and Git Markdown as the source of truth for Product Brief content. If a document is mirrored into Linear, clearly label it a mirror and keep canonical Git path/link.
- Preserve existing user-approved decisions and content; reconcile changes rather than overwrite. Distinguish confirmed facts, user decisions, assumptions, open questions, and AI proposals.
- Ask at most TWO focused questions per conversational turn. Never invent user interviews, research, evidence, or metrics.
- Pause only at material decision gates and final artifact approval; internal analysis and drafting continue under the existing request.
- Before Linear writes, show the batch plan and obtain authorization only if it is not already covered by existing approval. Never claim a write succeeded without checking tool results. For Git file edits, show the planned path and intended edits first; only mark Approved on explicit approval.
- Do not start PRD, UX/UI, development or detailed implementation as part of this skill.

## Workflow
### 0. Discover and resume
1. Check Git repository and existing `docs/product/Product-Brief.md` (including status and decisions), and existing decision/assumption logs.
2. Discover Linear MCP and relevant PM Skills; report unavailable dependencies and proceed only with supported steps. If Linear is unavailable, allow a local draft but do not claim Linear sync.
3. Read Linear project and existing Product Definition work. Detect completed steps to resume, not restart.
4. Present a concise current-state summary and next action. Ask only essential missing information.

### 1. Idea intake
Collect product idea, origin, target user hypotheses, problem, intended outcomes, constraints, unknowns. Capture as notes, not a premature PRD. Record framing; ask only about material unresolved decisions.

### 2. Problem framing
Use an available problem-definition PM Skill if appropriate. Separate problem from proposed solution; record user, situation, pain, evidence, alternatives, and uncertainty. Record the problem statement and unresolved decisions.

### 3. Hypotheses and value
Use relevant installed PM Skills where available. Record value proposition, assumptions, evidence strength, candidate success metrics and how they might be validated. Never present untested assumptions as facts. Obtain a decision only if high-level direction remains unresolved.

### 4. Draft
Use `references/brief-template.md`. Write or update `docs/product/Product-Brief.md` with status `Draft`; maintain `docs/product/decision-log.md` and `docs/product/assumption-log.md` when needed. Preserve existing content. Include unresolved questions and source/evidence labels. Do not manufacture certainty.

### 5. Review
Apply `references/review-gate.md` to evaluate clarity, traceability, consistency, scope, measurability and risks. Present concrete issues and revise with user input. Only user may approve. If approved, change status to `Approved`, record approver and date as supplied or reliably available, and note any remaining caveats. Do not claim approval before the user explicitly says so.

### 6. Linear synchronization
Follow `references/linear-sync.md`: propose changes, reuse batch approval or obtain it if missing, execute supported MCP calls, re-read to verify, report actual links and any gaps. Associate the canonical Git document link when a remote URL is known; never invent a GitHub URL. Do not close milestones based solely on an AI-generated draft.

## Interaction and checkpoints
At meaningful checkpoints: state current stage, findings, unresolved decisions and proposed artifact changes. Internal phase transitions require no approval. Keep the dialogue concise. Continue from saved files and Linear on subsequent sessions.

## Definition of done
- User explicitly approved the Product Brief.
- Git Markdown has an accurate Approved status and review record.
- Decision and assumption logs are current (or explicitly unnecessary).
- Linear updates were approved, attempted only via supported tools, and verified; any missing sync is reported as incomplete.
- Final message lists actual artifact paths and verified Linear links, not fabricated URLs.

## Workflow Boundary — Mandatory

This skill owns only the Product Brief stage.

After Product Brief approval and Linear synchronization:

1. Report the final deliverables and their locations.
2. Report Linear issues and milestone status.
3. Mark this workflow as completed.
4. STOP execution.

Do NOT:
- Start MVP Planning.
- Ask MVP-related interview questions.
- Invoke another lifecycle workflow.
- Create MVP documents or issues.
- Advance the project to another stage automatically.

Mentioning the next stage is informational only.

The next lifecycle stage requires a new,
explicit user instruction invoking its workflow.