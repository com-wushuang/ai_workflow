# mvp-planning-workflow

A bounded Codex Skill for MVP Planning with installed PM Skills, Linear MCP and Git Markdown.

## Install (macOS / Linux)
Unzip, then copy the **mvp-planning-workflow** folder into `~/.agents/skills/`. Restart Codex.

## Invoke
`使用 $mvp-planning-workflow 开始 BTC Trading OS 的 MVP Planning`

The skill first performs read-only discovery, then waits for approval before interviews. It stops after MVP Scope delivery and permitted Linear synchronization. It **never** starts PRD automatically.

## Preconditions
Linear MCP connected; relevant PM Skills installed (if not, the skill reports limitations); repository available; approved Product Brief present.

## Output
`docs/product/MVP-Scope.md` (plus decision/assumption notes as needed), and user-approved Linear updates.
