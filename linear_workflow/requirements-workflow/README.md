# requirements-workflow

Codex Skill for Requirements / PRD stage, designed for PM Skills + Linear MCP + Git Markdown.

## Install
Copy this entire directory to `~/.agents/skills/requirements-workflow/` and restart Codex.

## Invoke
`使用 $requirements-workflow 开始 BTC Trading OS 的需求定义`

## Output
- `docs/product/PRD.md`
- `docs/product/User-Stories.md`
- Optional decision log and open questions
- Approved Linear updates only after review

## Important
Requires an explicitly approved MVP Scope. Stops after Requirements; does not start UX or coding. Tool access and workflow rules are not a hard security sandbox: keep MCP write approval enabled where available.

内部步骤默认连续推进；仅关键未决事项、最终成果和未授权的 Linear 批次需要确认。阶段映射、版本审批及恢复规则见 `references/operating-contract.md`。

本仓库可用符号链接安装：`ln -s "<仓库绝对路径>/linear_workflow/requirements-workflow" ~/.agents/skills/requirements-workflow`。目标已存在时先检查，不要覆盖。新会话加载技能；链接方式会直接使用仓库修订。
