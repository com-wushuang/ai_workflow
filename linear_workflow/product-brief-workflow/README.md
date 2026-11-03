# product-brief-workflow

A Codex Skill for a human-approved Product Brief workflow with installed PM Skills, Linear MCP and Git Markdown.

## Install
Unzip the package and copy the `product-brief-workflow` directory to `~/.agents/skills/` (or your project-specific `.agents/skills/`). Start a new Codex session.

## Invoke
`使用 $product-brief-workflow 开始 BTC Trading OS 的产品定义`

Run Codex from the product's Git repository. Ensure Linear MCP is configured and the relevant PM Skills are installed. The skill discovers capabilities rather than assuming particular commands. It will ask for any missing project/repository details and for approval before Linear writes.

## Canonical artifacts
- `docs/product/Product-Brief.md`
- `docs/product/decision-log.md` (as needed)
- `docs/product/assumption-log.md` (as needed)

Git Markdown is the source of truth. Linear tracks work and links to approved deliverables.
