---
name: mvp-planning-workflow
description: Run a bounded, human-approved MVP Planning workflow using an approved Product Brief, installed PM Skills, Git Markdown, and Linear MCP. Invoke only when the user explicitly requests MVP planning for a project.
---

# MVP Planning Workflow

## Operating contract
Read `references/operating-contract.md` on entry for authorization, canonical sources, durable approval state, lifecycle mapping and recovery.

## Purpose and boundary
Own **only MVP Planning**. Convert an approved Product Brief into an explicitly reviewed MVP scope. Never begin PRD, UX/UI, development, or another lifecycle stage. A mention of the next stage is informational, never authorization. Do not invoke a general lifecycle orchestrator or an auto-chain that may advance stages.

## Non-negotiable rules
1. Read-only discovery first. Identify the repository, the Product Brief and its approval status, decision/assumption logs, and the existing Linear project/MVP milestone/issues. Reuse existing objects; never create duplicates.
2. Confirm the Product Brief was approved by the user. If not, stop and request approval or remediation. Do not silently treat a generated draft as approved.
3. Discover installed PM Skills and inspect their actual instructions before selecting relevant prioritization, opportunity, experiment, or scope skills. Do not invent skill names or assume an installation. Invoke one bounded task at a time, not an end-to-end auto-orchestrator.
4. Interview in rounds of **at most two questions**. Clearly distinguish user decisions, source facts, unverified assumptions, and AI proposals. Do not fabricate evidence, metrics, user research, or scope decisions.
5. Continue between internal phases. Pause for material decisions and final MVP Scope approval; do not enter another lifecycle stage automatically.
6. Git Markdown is the canonical source for content and version history. Linear tracks project progress, issue status and links. Inspect actual MCP tool capabilities; never claim unsupported Document or Milestone operations succeeded.
7. Before creating/updating Linear objects, show a concrete change plan (object, existing/new, intended fields and links) and obtain explicit user approval. Do not close a milestone without explicit approval.
8. After delivery and permitted synchronization, report paths, links, decisions, remaining risks and **STOP**. Never start Requirements/PRD interviews.
9. If user says stop/pause, stop new questions and writes; summarize current state read-only. No background activity.

## Input
- Explicit project name or unambiguous current project.
- Approved `docs/product/Product-Brief.md` (or discover equivalent and confirm canonical path).
- Existing Linear Project and MVP Planning milestone, if any.

## Workflow

### 0. Discover and validate (read-only)
- Locate repo and approved Product Brief; read related logs.
- Read Linear project/milestones/issues; check for an existing MVP Scope.
- Inventory relevant installed PM Skills, choosing only those useful to the current subtask.
- Report sources, missing inputs, and a proposed plan. Continue interviews under the invocation; ask only essential missing questions.

### 1. MVP objective and testable assumptions
- Clarify the smallest meaningful user outcome and which Product Brief assumptions the MVP must test.
- Specify observable success/failure signals without inventing thresholds.
- Write confirmed decisions and outstanding assumptions to working notes.
- **Checkpoint G1:** record outcome, hypotheses and unresolved decisions.

### 2. Candidate scope and prioritization
- Elicit candidate capabilities and dependencies; compare value, learning, effort, risk and sequencing.
- Separate **Must-have**, **Later**, and **Out of scope**. Show alternatives and tradeoffs; the user chooses.
- **Decision G2:** obtain user choices for unresolved material scope tradeoffs.

### 3. Validation and delivery boundaries
- Define MVP success criteria, test approach, nonfunctional constraints, release assumptions, and key risks.
- Do not turn this into detailed PRD/user stories or implementation tasks.
- **Checkpoint G3:** record validation boundaries; pause only for material unresolved choices.

### 4. Draft and review
- Generate `docs/product/MVP-Scope.md` using `references/mvp-scope-template.md`, status **Draft**.
- Review with `references/review-gate.md`: traceability to approved Brief, minimality, clear exclusions, testability, assumptions, risks and consistency.
- Present review findings; revise with user decisions. **Gate G4:** user must explicitly approve the final scope before status becomes Approved.

### 5. Git and Linear synchronization
- Maintain working notes and decision/assumption records in Git; preserve existing content and avoid overwriting user edits.
- Present exact proposed Linear changes and reuse existing batch approval or request it if missing; follow `references/linear-sync.md`.
- Only perform approved writes; read back to verify. If link publication is impossible, report a manual follow-up rather than inventing a URL.
- Summarize delivery and **STOP**.

## State handling and recovery
On resume, inspect the current artifact, recorded approvals and Linear state. Identify the last confirmed gate and resume there; do not replay interviews or reapply writes blindly. User approval must be explicit in the conversation or a clearly recorded approval entry, never inferred from silence or task completion.

## References
- `references/mvp-scope-template.md`
- `references/review-gate.md`
- `references/linear-sync.md`
