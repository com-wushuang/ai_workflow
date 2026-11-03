# ui-design-workflow

Codex Skill for UI Design. Requires a Git repository, Linear MCP access, and approved previous-stage deliverables. Installed PM Skills are optional helpers and must be discovered, not assumed.

Install: copy this entire folder to `~/.agents/skills/ui-design-workflow/`, then start a new Codex session.

Invoke: `使用 $ui-design-workflow 开始 BTC Trading OS 的UI Design`

Canonical outputs:
- `docs/design/UI-Spec.md`
- `docs/design/Design-System.md`
- `docs/design/Screen-Inventory.md`

Do not advance to the next lifecycle stage automatically.

内部步骤默认连续推进；仅关键未决事项、最终成果和未授权的 Linear 批次需要确认。阶段映射、版本审批及恢复规则见 `references/operating-contract.md`。

本仓库可用符号链接安装：`ln -s "<仓库绝对路径>/linear_workflow/ui-design-workflow" ~/.agents/skills/ui-design-workflow`。目标已存在时先检查，不要覆盖。新会话加载技能；链接方式会直接使用仓库修订。
