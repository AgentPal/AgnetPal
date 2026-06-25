# PalSmith / Pal 资产治理 Pal

PalSmith 是 AgentPal 的系统级 Pal，用于创建、管理、导入、导出、体检、升级和发布 Pal Pack。

PalSmith 默认只读。它先生成计划、风险说明和确认问题；真实写入、复制、打包、下载、删除或发布由当前 Runtime 在用户确认后执行并返回 evidence。

## Direct Call

```text
/pal PalSmith
```

## Common Requests

- `/pal PalSmith 创建一个小红书运营 Pal`
- `/pal PalSmith 创建一个跨境电商运营团队`
- `/pal PalSmith 体检所有 Pal`
- `/pal PalSmith 从 GitHub 导入这个 Pal Pack`
- `/pal PalSmith 从本地目录导入 Pal`
- `/pal PalSmith 导出 Research Pal，不含记忆`
- `/pal PalSmith 导出 Atlas，含记忆完整包`

## Key Boundaries

- GitHub 导入先进入 staging，不默认信任。
- 导出 Pal 必须先选择导出类型。
- 含 memory / state / reports 的导出必须强确认。
- 普通 Skill、Knowledge、Tool、模型、插件、MCP、外部 Agent 不进入 Pal 通讯录。
- 用户私人记忆不得进入公开 Pal Pack。

## Main Assets

- `core/` defines Pal creation, import/export, health check, versioning, permission, reporting, and risk protocols.
- `governance/` defines permission, privacy, staging, import/export, version, and audit policies.
- `templates/` provides plans, reports, change proposals, and user confirmation questions.
- `scanners/` provides checklists for structure, privacy, schema, import/export risk, memory size, and collaboration permissions.
- `workflows/` provides end-to-end procedures.
- `evals/` provides smoke and regression checks for PalSmith behavior.
