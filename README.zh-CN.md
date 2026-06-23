# AgentPal

AgentPal 是面向 Agent Runtime 的 Pal Workspace，也是 Pal Pack 标准实践。

AgentPal，让每个 Agent 都有自己的 Pal。

AgentPal v0.1.0-rc.1 是一个 Markdown / JSON / 协议工作区，可用于 Codex、Claude Code，以及其他能够读取结构化工作区文件的 CLI Agent。它不是 Agent Runtime，不是多 Agent Runtime，不是执行层，不是桌面 App，不是 Web App，也不是安装器。

## 当前 Release Candidate

- 版本：`v0.1.0-rc.1`
- 当前 active path：`Simple Pal Mode only`
- 默认 Main Pal / Leader / Conductor：`Mira`
- 官方 8 个 Pal：`Mira`、`Atlas`、`Vega`、`Rhea`、`Quinn`、`Morgan`、`Harper`、`Nova`
- 显式调用专业 Pal：`/pal Name`

## 当前已经可用

- AgentPal 作为 AgentPal Workspace 和 Pal Pack 标准实践已经可用。
- 它为 Runtime 提供 Pal 层：身份、知识、技能、上下文、记忆边界、输出契约、协作、审查、总结和学习规则。
- Mira 是普通消息的默认入口 Pal。
- Mira 可以通过 Fast Route 在同一条回复中把实质任务交给 owner Pal。
- 当前路径支持 Task Package、Context Slicing 和 Asset Loading Budget。
- 通过 contacts / registry 支持 `/pal Name` 调用当前已注册 Pal。
- 当前可以在 Codex、Claude Code 和通用 CLI Agent 路径中体验 AgentPal。

## v0.1 当前未启用

- AgentPal 不是 Agent Runtime，也不是执行引擎。
- AgentPal 在 `v0.1.0-rc.1` 中不是多 Agent Runtime，不是 Subagent Mode，也不是 parallel child workflow 系统。
- Deep Conductor 目前只是 future design。
- external Agent orchestration 目前只是 future design。
- AgentPal 不是桌面 App、Web App、托管服务、市场、守护进程、扫描器、校验器或自动安装器。
- 当前版本中的 PalBench 是 small-sample validation，不是统计显著 benchmark。

## Quick Start

### Codex

1. 在 Codex 中打开 AgentPal Workspace。
2. 复制 [`INIT_PROMPT.md`](INIT_PROMPT.md) 的内容。
3. 让 Codex 以 Mira 为默认入口完成初始化。
4. 普通任务先找 Mira，或用 `/pal Name` 显式调用专业 Pal。
5. 当前路径只使用 `Simple Pal Mode only`。

详见：[`docs/04-runtime-guides/01-use-with-codex.md`](docs/04-runtime-guides/01-use-with-codex.md)

### Claude Code

1. 先进入真实用户项目目录：

   ```text
   cd <your-project>
   claude
   ```

2. 粘贴 [`prompts/claude-code/install-agentpal-current-project.md`](prompts/claude-code/install-agentpal-current-project.md) 的一段式接入提示词。
3. 任务上下文应始终以当前项目目录为准，不要把 AgentPal 工作区误当成用户项目。
4. `.claude/settings.local.json` 是本机配置，不应提交。
5. 这条路径是轻量项目接入，不是 Claude Code 深度插件，也不是自动安装器。

详见：[`docs/04-runtime-guides/02-use-with-claude-code.md`](docs/04-runtime-guides/02-use-with-claude-code.md)

### 通用 CLI Agent

1. 先进入真实用户项目目录：

   ```text
   cd <your-project>
   <your-cli-agent>
   ```

2. 粘贴 [`prompts/cli-agent/install-agentpal-current-project.md`](prompts/cli-agent/install-agentpal-current-project.md) 的通用接入提示词。
3. 只要 CLI Agent 能读取目录、遵循 Markdown / JSON 指令、维护上下文，就可以按通用路径接入。
4. 这是一份 generic compatibility guide，不承诺所有 CLI Agent 都已经验证。

详见：[`docs/04-runtime-guides/03-use-with-generic-cli-agent.md`](docs/04-runtime-guides/03-use-with-generic-cli-agent.md)

## 官方 Pals

| Pal | 角色 | 直接调用 |
| --- | --- | --- |
| Mira | Main Pal / Leader / Conductor | `/pal Mira` |
| Atlas | 开发 | `/pal Atlas` |
| Vega | 调研 | `/pal Vega` |
| Rhea | 系统 | `/pal Rhea` |
| Quinn | 质量 | `/pal Quinn` |
| Morgan | 文档 | `/pal Morgan` |
| Harper | 写作 | `/pal Harper` |
| Nova | 产品 | `/pal Nova` |

Mira 是默认入口。专业 Pal 默认不监听。

## Simple Pal Mode 如何工作

在 `v0.1.0-rc.1` 中，普通消息先到 Mira。Mira 逐案判断任务归属；如果某个已注册专业 Pal 应该主责，Mira 会做简短交接并停止，由 owner Pal 在同一条回复中立刻接手，并使用自己的 Pal 资产与输出契约完成回答。

`/pal Name` 不是启动一个独立 Agent 进程，而是让当前 Runtime 进入该 Pal 的工作方式。

## Fast Route / Task Package / Context Slicing

- Fast Route 是 `v0.1.0-rc.1` 当前有效的 clear-task handoff 模式。
- Task Package 用来把目标、上下文、约束、证据要求和验收条件压缩给当前 Runtime。
- Context Slicing 表示只加载当前任务真正需要的文件切片。
- Asset Loading Budget 用来限制默认加载的 Pal 资产范围。
- Deep Conductor 只作为 future design 被记录，不是当前 active path。

## PalBench Small-Sample Validation

当前仓库中的 PalBench 资料是 release candidate 的 small-sample validation，只能作为谨慎证据使用；它不是统计显著 benchmark，也不用于宣称模型优劣。

## 仓库结构

| 路径 | 作用 |
| --- | --- |
| `pals/` | 官方与用户扩展的 Pal Pack |
| `contacts/` | Pal 联系册与别名 |
| `registry/` | Pal 索引与发现记录 |
| `orchestration/` | 运行规则与协议文档 |
| `prompts/` | 复制即用的接入与维护提示词 |
| `docs/` | 用户文档 |
| `projects/` | 外部项目绑定模板 |
| `templates/` | 可复用模板 |

## 文档入口

- 文档首页：[`docs/README.md`](docs/README.md)
- 概览：[`docs/00-overview/`](docs/00-overview/)
- Pal Pack 标准：[`docs/03-pal-pack-standard/`](docs/03-pal-pack-standard/)
- Runtime 指南：[`docs/04-runtime-guides/`](docs/04-runtime-guides/)
- 创建 Pal：[`docs/07-authoring-pals/`](docs/07-authoring-pals/)
- 调度方法论：[`docs/05-orchestration-methodology/`](docs/05-orchestration-methodology/)
- 验证与证据：[`docs/06-validation-and-evidence/`](docs/06-validation-and-evidence/)
- Release Candidate 文档：[`docs/08-release-candidate/`](docs/08-release-candidate/)
- 当前状态：[`docs/00-overview/01-current-status.md`](docs/00-overview/01-current-status.md)
- 当前能力：[`docs/00-overview/02-current-capabilities.md`](docs/00-overview/02-current-capabilities.md)
- AgentPal 当前不是什么：[`docs/00-overview/04-what-agentpal-is-not.md`](docs/00-overview/04-what-agentpal-is-not.md)
- RC 摘要：[`docs/00-overview/05-release-candidate-summary.md`](docs/00-overview/05-release-candidate-summary.md)
- 项目优先接入：[`docs/04-runtime-guides/04-project-first-connection.md`](docs/04-runtime-guides/04-project-first-connection.md)

## 贡献

贡献时请保持 `v0.1.0-rc.1` 的发布边界：AgentPal 是 Agent Runtime 的 Pal Workspace 和 Pal Pack 标准实践，当前 active path 只有 `Simple Pal Mode only`。不要把 future design 写成当前运行能力。

详见：[`CONTRIBUTING.md`](CONTRIBUTING.md)。

## License

MIT。见 [`LICENSE`](LICENSE)。
