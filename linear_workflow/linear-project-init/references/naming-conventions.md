# Naming and Deduplication Conventions

- **Team:** reuse an existing team. Never create a team by default.
- **Project:** `<Product Name>`; add `— MVP v1` only when the user explicitly wants release-scoped projects.
- **Milestone:** `NN · Phase Name` (e.g. `01 · Product Definition`).
- **Issue:** `PD · Verb + outcome` for Product Definition; use `MVP`, `REQ`, `UX`, `DEV`, `VAL` for later stages if needed.
- **Document:** `Product Brief` (use version and approval status inside the document, not in the title unless required).
- **Git document:** `docs/product/Product-Brief.md`.

## Matching before creating
1. Prefer exact Linear IDs or URLs already returned by the MCP.
2. Within the selected team, compare project names case-insensitively and normalize extra whitespace.
3. If multiple similar projects exist, ask which one to use; do not guess.
4. Within the chosen project, check milestones by normalized name and issues by normalized title **and project membership**.
5. Reuse matches instead of creating duplicates. If an existing item differs materially from the template, present a proposed update and request approval.
6. Never use a generated placeholder URL or ID as a substitute for a returned value.

## Idempotency
Running the Skill twice should yield the same project structure without duplicated objects. After partial failure, inspect current state and resume only missing approved operations.
