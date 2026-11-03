# linear-project-init

一个从 Codex 调用 Linear MCP 的可复用项目初始化 Skill。**每次只需提供项目名称**，其余规则内置。

## 安装

将整个 `linear-project-init` 文件夹复制到 `~/.agents/skills/linear-project-init/`，确保其中存在 `SKILL.md`，然后重启 Codex 会话。

```bash
mkdir -p ~/.agents/skills
cp -R linear-project-init ~/.agents/skills/
```

确保 Codex 已配置并授权 Linear MCP；Skill 不会替你自动安装或授权 MCP。

## 调用

```text
使用 $linear-project-init 初始化项目：XXX
```

**无需重复**“使用 Linear MCP、复用 Team/Project、默认生命周期、先审批、最后验证”等规则；它们都写在 `SKILL.md` 和 `references/` 中。

## 内置流程

1. Discover：只读检查 MCP、Team、Project 及已有对象。
2. Plan：按默认模板提出最小初始化计划，区分复用与新建。
3. Approve：向用户展示写入计划，明确批准前不写入。
4. Execute：批准后调用 MCP，重复运行不应重复创建对象。
5. Verify：重新读取并报告真实 ID/URL、成功项和限制。

默认六个里程碑；只创建 Product Definition 的五项初始任务。不会自动开始 Product Brief，也不会凭空创建需求。

## 文件

- `SKILL.md`：执行规范和默认规则
- `references/project-template.md`：项目和里程碑模板
- `references/naming-conventions.md`：命名与去重规则
- `references/approval-policy.md`：审批和变更控制

内部步骤默认连续推进；仅关键未决事项、最终成果和未授权的 Linear 批次需要确认。阶段映射、版本审批及恢复规则见 `references/operating-contract.md`。

本仓库可用符号链接安装：`ln -s "<仓库绝对路径>/linear_workflow/linear-project-init" ~/.agents/skills/linear-project-init`。目标已存在时先检查，不要覆盖。新会话加载技能；链接方式会直接使用仓库修订。
