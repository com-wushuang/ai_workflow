# Linear MCP synchronization policy
1. Read current project, relevant milestone and issues; reuse existing objects.
2. Present proposed writes as a table: object | identifier | operation | changed fields | reason | canonical Git link.
3. Reuse existing explicit authorization of this exact batch; otherwise wait for user authorization.
4. Call only available Linear MCP tools; if milestone/document APIs are absent, report the limitation and use a link or manual action.
5. Read back each changed object, compare intended vs actual, and report partial failures.
6. Never treat stage approval as permission to start another stage, nor as permission for deployment.

Authorization and recovery follow `operating-contract.md`: reuse existing approval for the exact batch, do not request approval per API call, and resume partial writes from verified state.
