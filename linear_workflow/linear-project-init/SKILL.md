---
name: linear-project-init
description: Initialize or reconcile a product lifecycle project in Linear using the configured Linear MCP. Use when the user asks to initialize, bootstrap, or standardize a Linear product project from Codex. Read existing state, propose a plan, require explicit approval before writes, execute idempotently, and verify results. Does not conduct Product Brief interviews or invent product requirements.
---

# Linear Project Initialization

## Purpose
Initialize a lightweight product lifecycle structure in Linear from Codex. Linear is the project/task system of record; product documents and code may live in Git and be linked from Linear.

## References
Read these files before proposing a plan:
- `references/project-template.md` — default project structure and initial issues
- `references/naming-conventions.md` — naming and deduplication rules
- `references/approval-policy.md` — approval and safety gates

## Invocation contract (minimal user input)
The normal invocation is **only**: `使用 $linear-project-init 初始化项目：<项目名称>`.
The project name is the only required input. Treat all rules in this Skill and its references as **defaults**, not questions the user must repeat. Never ask the user to restate the MCP requirement, reuse policy, lifecycle template, approval gate, or verification requirement. Do not require the user to copy a long prompt.

Optional inputs, only if voluntarily supplied: existing Linear team, project summary, Git repository URL, non-default template. Discover the team automatically. If exactly one suitable team is accessible, use it in the proposed plan; if multiple plausible teams exist and selection matters, ask one targeted question. Do not invent product requirements from the name. Missing optional inputs should not block planning; leave descriptions blank or TBD.

## Defaults (automatic)
- Always use the configured Linear MCP; inspect available tools and stop with setup guidance if unavailable.
- Reuse existing Team, Project, milestones and issues whenever matching; never create a Team by default.
- Apply `references/project-template.md` unless the user requests a different template.
- Apply `references/naming-conventions.md` automatically.
- Show a complete, concrete write plan and wait for **explicit approval** before any Linear write, as specified in `references/approval-policy.md`.
- After approved writes, re-read Linear and report verified results with actual returned links.
- Do not conduct Product Brief interviews or create detailed future-stage requirements during initialization.


## Execution workflow

### Phase 1 — Discover (read-only)
1. Inspect available Linear MCP tools and verify access. Do not assume a tool exists because it is mentioned in this Skill.
2. List accessible teams and search existing projects by exact name and plausible variants.
3. For any matching project, inspect existing milestones, issues, and documents when the MCP exposes those operations.
4. Identify which operations are supported, unsupported, or require a manual fallback.
5. If Linear MCP is unavailable, stop and give the user the connection error and next diagnostic step; never pretend a remote action succeeded.

### Phase 2 — Plan (read-only)
1. Use `references/project-template.md` to propose a minimal lifecycle structure.
2. Separate objects into **reuse**, **create**, **update**, **skip**, and **manual** categories.
3. Keep future phases as milestones only; create detailed issues for Product Definition only. Never fabricate MVP features or implementation tasks.
4. Present a compact, explicit write plan with target team/project, each object and action, expected relationships, and any limitations.
5. Ask for explicit approval of this plan. Stop before any write.

### Phase 3 — Execute (write, only after approval)
1. Re-check target object existence immediately before creating it; use stable IDs where possible.
2. Create/reuse the project in the approved team.
3. Create/reuse milestones if supported. If unsupported, do not create fake milestone issues unless separately approved; provide a manual fallback.
4. Create/reuse Product Definition issues and associate them with the project and milestone when supported.
5. Create or link a Product Brief document only when explicitly included in the approved plan and the corresponding MCP write tool exists. Otherwise record a manual step.
6. Avoid overwriting user-authored content. Ask again before any destructive change or materially different write not covered by approval.
7. Record returned object IDs and URLs; do not invent them.

### Phase 4 — Verify and report
1. Re-read the project and created objects via Linear MCP.
2. Compare actual state with the approved plan. Mark each item **verified**, **unverified**, **failed**, or **manual**.
3. Report project link, milestone/issue links where returned, any incomplete steps, and safe next actions.
4. If partially failed, do not blindly retry the entire plan; resume from verified existing state.
5. Do not start Product Brief automatically. Offer it as the next separate workflow.

## Interaction rules
- Never make Linear writes during discovery or planning.
- Approval is specific to the displayed plan, not a blanket permission for future changes.
- Ask no more than two clarification questions per turn when feasible.
- Distinguish observed Linear data, user-provided facts, assumptions, and recommendations.
- Respect existing team workflows and issue statuses; do not create or change workflow states without explicit approval.
- Never claim a Linear object exists without confirming it through tool output.
- For unsupported MCP operations, explain the limitation and provide an actionable manual alternative.

## Completion criteria
The project exists in the intended team; all supported, approved objects have been created or reused; relationships are verified where possible; all exceptions are reported; and the user receives actual links/identifiers and a clear next step.
