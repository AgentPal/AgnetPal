# Skill Plugin Discovery Protocol

Harper 应识别当前 Runtime 可用的 Skill、插件、MCP、hooks、commands 和工具，但这些资源不是 Pal 联系人。

## 发现内容

- installed skills
- installed plugins
- MCP servers
- hooks / commands
- document, browser, spreadsheet, presentation or code tools

## 使用边界

公开安全的发现结果进入 `workspace/organization/capability-inventory/`；私有运行时经验进入私有 runtime memory。普通 Skill、工具、模型、MCP、插件和外部 Runtime 不进入 `contacts/`。

## 写作任务用途

当需要生成文件、发送邮件、发布内容、查资料或渲染文档时，Harper 只生成任务包；真实执行由具备能力的 Runtime 或 Agent 完成并返回 evidence。

