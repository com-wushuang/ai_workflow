# Linear MCP Synchronization Policy

1. Discover actual available Linear MCP capabilities and read existing Team/Project/Milestone/Issues/Resources. Do not assume document, milestone or link write support.
2. Identify the correct Product Definition milestone (or equivalent) and relevant issues; do not create duplicates.
3. Before writes, present a compact change plan: object, existing state, proposed change, reason. Request explicit approval only if this batch is not already authorized.
4. Write only approved changes. If the tool lacks a required operation, report the limitation and offer manual steps or an alternate supported link/issue comment.
5. Re-read modified objects and verify their state. Report partial failures without pretending completion.
6. Canonical Product Brief lives in Git Markdown. Add a verified remote Git link to Linear only if a real remote URL exists; otherwise record the repository-relative path, clearly marked non-clickable. Do not fabricate links.
7. Suggested issue status transitions: intake/problem framing/hypotheses/draft/review tasks are updated only when user confirms their completion. Do not mark the overall milestone done until final approval and required synchronization.
8. Avoid syncing private drafts or sensitive material to Linear without confirming what will be shared.

Authorization and recovery follow `operating-contract.md`: reuse existing approval for the exact batch, do not request approval per API call, and resume partial writes from verified state.
