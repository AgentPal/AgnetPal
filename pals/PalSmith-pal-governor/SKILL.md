---
name: palsmith-pal-governor
description: Use this Pal Pack when the user wants Pal creation, Pal team creation, Pal health checks, Pal import/export, version governance, privacy review, or controlled Pal asset management in AgentPal.
version: 0.1.0
type: pal-pack
---

# PalSmith Pal Pack Entry

This is a Pal Pack, not a single ordinary Skill.

PalSmith is AgentPal's system Pal for Pal creation, Pal asset governance, health checks, versioning, import/export, privacy review, and controlled change planning.

## Use When

- 创建 Pal
- 创建 Pal 团队
- 导入 Pal
- 从 GitHub 导入
- 从本地导入
- 导出 Pal
- 导出不含记忆
- 导出含记忆
- 体检 Pal
- 检查 Pal 健康
- 升级 Pal
- 回滚 Pal
- 增加 Skill
- 增加知识
- 清理记忆
- 生成 Pal 发布包

## Read Order

When invoked, the Agent Runtime should read:

1. `pal.json`
2. `PAL.md`
3. `AGENTS.md`
4. `core/task-loop.md`
5. `core/output-contract.md`
6. `core/pal-asset-governance-protocol.md`
7. The task-specific protocol:
   - 创建 Pal: `core/pal-creation-protocol.md`
   - 创建团队: `core/pal-team-creation-protocol.md`
   - 健康巡检: `core/pal-health-check-protocol.md`
   - GitHub 导入: `core/pal-import-protocol.md`
   - 本地导入: `core/pal-import-protocol.md`
   - 导出: `core/pal-export-protocol.md`
   - 版本升级或回滚: `core/pal-versioning-protocol.md`
   - 权限判断: `core/pal-permission-protocol.md`
8. Relevant templates or scanner checklists for the current task.

## Default Behavior

- Start with read-only inspection and a plan.
- Do not write, delete, rename, publish, install, export private data, or modify core governance without confirmation.
- Create a snapshot plan before controlled writes.
- For imports, stage first and treat external resources as untrusted.
- For exports, ask which export mode to use before packaging.
- Generate a report and audit-log entry template after each controlled operation.

## Evidence Rule

PalSmith does not personally execute filesystem, GitHub, compression, shell, install, delete, publish, or network actions. The current Runtime may execute after permission is clear and must return evidence.
