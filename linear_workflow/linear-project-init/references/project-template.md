# Default Product Lifecycle Project Template

This is a **proposed template**, not a claim about pre-existing Linear objects. Adapt it to the user's actual workspace and approved preferences.

## Project
- Name: `<Product Name>` (or user-approved release-specific name)
- Team: user-selected existing Linear team
- Description: one-sentence user-provided purpose; if unknown, leave blank or label TBD
- Optional link: Git repository URL, only if supplied or verified

## Milestones (in order)
1. `01 · Product Definition` — deliverable: approved Product Brief
2. `02 · MVP Planning` — deliverable: approved MVP Scope
3. `03 · Requirements` — deliverable: approved PRD
4. `04 · UX/UI Design` — deliverable: reviewed designs and specifications
5. `05 · Development` — deliverable: implemented and tested MVP
6. `06 · Validation & Release` — deliverable: validation and release record

Milestones are phases, not a claim that work must proceed in a rigid waterfall. If the MCP cannot create milestones, flag them as manual; do not silently substitute labels or issues.

## Initial issues (Product Definition only)
- `PD · Capture product idea and context` — Done when known facts, unknowns and constraints are recorded.
- `PD · Define target user and problem` — Done when the user has reviewed the problem statement and assumptions are labeled.
- `PD · Identify hypotheses and evidence` — Done when key assumptions, evidence and validation questions are recorded.
- `PD · Draft Product Brief` — Done when a complete draft exists and unresolved items are marked.
- `PD · Review and approve Product Brief` — Done only after explicit user approval; draft completion is not approval.

Default all new issues to the team's ordinary backlog/to-do state; do not set deadlines, assignees, priorities, estimates, or cycles without instructions.

## Documents
- `Product Brief` — optional Linear Project Document, if the MCP supports it and the user approved creating it.
- Canonical Markdown location, if the user wants Git-managed docs: `docs/product/Product-Brief.md`.
- Decide with the user whether Linear Document or Git Markdown is the canonical source to prevent conflicting versions. Linking is preferable to maintaining two editable masters.

## Future work
Do not pre-populate detailed MVP, PRD, UX, or development issues during initialization. Add them when their upstream stage is reviewed.
