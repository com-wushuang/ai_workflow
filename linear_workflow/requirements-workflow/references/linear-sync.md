# Linear Sync Policy

## Read first
Resolve the exact existing project and Requirements milestone; inspect issues, documents and prior updates. Prefer reuse, never duplicate by name alone; compare identifiers and scope.

## Before write
Present a change table: object, identifier, current value, proposed value, rationale. Ask explicit permission. No write on silence or ambiguous consent.

## On approval
- Update only Requirements-stage issues or milestone supported by the connected MCP.
- Attach or reference canonical Git PRD and User Stories (repository URL and commit when available).
- Optionally create a requirements document in Linear only if supported and approved; Git remains canonical.
- Do not create development issues, UX issues, or transition the next milestone.
- Read back changes and report confirmed vs failed/unsupported operations.

If no repository remote URL exists, record relative paths and explain that Linear cannot link to a remote document until it is published. Do not push Git automatically.

Authorization and recovery follow `operating-contract.md`: reuse existing approval for the exact batch, do not request approval per API call, and resume partial writes from verified state.
