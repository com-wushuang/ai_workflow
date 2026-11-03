# Linear MCP synchronization policy

1. Read the existing Project, MVP Planning milestone, related Issues, and linked resources first. Match by identifiers and titles; do not create duplicates.
2. Git Markdown is canonical. Prefer linking a committed, accessible GitHub/Git URL to `docs/product/MVP-Scope.md`; do not invent a URL before a remote path is verified. If no remote URL is available, record a local path in an issue comment only with user approval, and flag that it is not a clickable remote document.
3. Proposed write plan must show exact target IDs, fields, new issue names if any, status changes, and the intended link/comment. Reuse existing exact-batch approval; otherwise wait for explicit user approval.
4. Update only existing MVP Planning tasks or create minimal process tasks specifically approved by the user. Do not auto-generate PRD or development Issues. Never advance the next milestone.
5. Use only MCP capabilities actually available in this session. If unsupported, explain the limitation and offer manual instructions.
6. Read back all modified objects and report verified outcomes, failed operations, and remaining manual actions.

Authorization and recovery follow `operating-contract.md`: reuse existing approval for the exact batch, do not request approval per API call, and resume partial writes from verified state.
