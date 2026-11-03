# Approval and Change-Control Policy

## Read-only operations
Listing teams, projects, issues, milestones, documents and inspecting MCP capabilities require no additional approval within this workflow.

## Mandatory approval gate
Before the first write, show:
- Target Linear team and project (existing or new)
- Objects to reuse/create/update, with names and relationships
- Any document creation or linking
- Unsupported operations and manual fallbacks
- Explicit statement: **No Linear changes have been made yet**

Ask: `是否批准按以上计划初始化 Linear 项目？` Reuse explicit existing approval of this exact batch; otherwise wait for an unambiguous yes. Ambiguous replies mean no approval.

## Scope of approval
Approval covers only the shown changes. Obtain fresh approval for:
- Switching target team/project
- Deleting, archiving, or moving objects
- Overwriting existing descriptions or user-authored content
- Changing issue workflow statuses, permissions, assignees, deadlines, or priorities not in the plan
- Creating substitute objects because an MCP capability is unavailable

## Execution reporting
Report per object: planned action, actual action, returned ID/URL if available, and verification status. On tool error, stop affected operations, explain the partial state, and request direction if recovery changes the approved plan.

## Product decisions
Do not mark Product Brief `Approved` unless the user explicitly approves the content. Approval of project initialization is **not** approval of the product definition.
