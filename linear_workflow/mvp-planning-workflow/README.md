# mvp-planning-workflow

A bounded Codex Skill for MVP Planning with installed PM Skills, Linear MCP and Git Markdown.

## Install (macOS / Linux)
Unzip, then copy the **mvp-planning-workflow** folder into `~/.agents/skills/`. Restart Codex.

## Invoke
`使用 $mvp-planning-workflow 开始 BTC Trading OS 的 MVP Planning`

The skill first performs read-only discovery, then continues interviews under the workflow invocation. It stops after MVP Scope delivery and permitted Linear synchronization. It **never** starts PRD automatically.

## Preconditions
Linear MCP connected; PM Skills optional (bundled templates are the fallback); repository available; approved Product Brief present.

## Output
`docs/product/MVP-Scope.md` (plus decision/assumption notes as needed), and user-approved Linear updates.

内部步骤默认连续推进；仅关键未决事项、最终成果和未授权的 Linear 批次需要确认。阶段映射、版本审批及恢复规则见 `references/operating-contract.md`。

本仓库可用符号链接安装：`ln -s "<仓库绝对路径>/linear_workflow/mvp-planning-workflow" ~/.agents/skills/mvp-planning-workflow`。目标已存在时先检查，不要覆盖。新会话加载技能；链接方式会直接使用仓库修订。
