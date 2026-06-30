# Authorize User Custom Pal Discovery

Copy this prompt into AgentPal when you want PalSmith to plan an explicit authorization flow for a user custom Pal.

```text
/pal PalSmith 我想让这个用户自定义 Pal 可以被工作区发现。

Pal 路径：
<paste-user-custom-pal-path>

请先不要修改 contacts、official/pals、Marketplace、运行时代码或任何注册表文件。

请先判断：
1. 这个 Pal 当前是否是 user custom Pal，是否仍是 official: false；
2. 当前默认 discovery / delegation / contacts / Marketplace 状态是什么；
3. 我需要选择哪些授权范围；
4. 需要哪些调用者、任务范围、数据访问、记忆访问、有效期和撤销规则；
5. 是否需要 Quinn / QA 复核。

请最多先问我 3 个关键问题。

如果我要求“让所有 Pal 都能自动用它”，请不要默认全量授权；请改为建议最小安全范围，例如 workspace_discoverable + 指定调用者 + 指定任务范围。

如果我要求“上架 Marketplace”，请区分：
- Marketplace draft metadata；
- public listing request；
- 真实 Marketplace 后端不存在；
- 不能直接公开上架。

如果我要求“把它加入公司联系人，让大家都能用”，请区分：
- workspace discovery；
- workspace invocation；
- contacts registration；
- organization-level policy；
- delegation authorization；
- 不能直接修改 `workspace/organization/contacts`。

在我明确确认前，不要写任何文件。
```

Boundary:

- This prompt does not make the Pal official.
- This prompt does not add the Pal to central contacts.
- This prompt does not enable default delegation.
- This prompt does not publish to a Marketplace.
- This prompt does not build a runtime, CLI, scanner, daemon, connector, backend service, or Marketplace backend.
