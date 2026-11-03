# Linear MCP synchronization policy
1. Read current project, relevant milestone and issues; reuse existing objects.
2. Present proposed writes as a table: object | identifier | operation | changed fields | reason | canonical Git link.
3. Wait for explicit user authorization of this exact write plan.
4. Call only available Linear MCP tools; if milestone/document APIs are absent, report the limitation and use a link or manual action.
5. Read back each changed object, compare intended vs actual, and report partial failures.
6. Never treat stage approval as permission to start another stage, nor as permission for deployment.
