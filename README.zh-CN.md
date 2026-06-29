# AgentPal

AgentPal 是面向 Agent Runtime 的 no-code AI 团队组织层。

它不替代 Codex、Claude Code、OpenCode、OpenHands、OpenClaw、Hermes、workbuddy、Gemini CLI、DeepSeek-TUI 或其他执行环境。AgentPal 做的是另一件事：给这些 Runtime 增加一套可读、可维护、可协作的 Pal 工作区，包括身份、职责、知识、Skill、工作流、记忆边界、任务包、验收习惯和协作规则。

一句话理解：

> AgentPal = 给现有 Agent 增加一个 Pal 团队组织层。

## AgentPal 是什么

AgentPal v0.5 是一个 Markdown / JSON / protocol workspace，适合能读取本地文件并遵循结构化指令的 Agent Runtime。

AgentPal 是：

- no-code Pal 组织层
- Pal Pack 与 AI 团队工作区
- 用角色化 Pal 组织 AI 工作伙伴的方法
- 把外部用户项目薄绑定到中央 AgentPal 工作区的方式
- public-safe 的文档、模板、示例、标准和验证记录集合

AgentPal 不是：

- Agent Runtime
- 多 Agent Runtime
- App Runtime
- 桌面 App 或 Web App
- installer、CLI、daemon、scanner、connector layer 或 marketplace
- 外部系统执行器
- 替代真实读写文件、运行命令、调用工具或发布 Release 的宿主 Runtime

## Pal / Skill / Agent

AgentPal 明确区分三层：

```text
Skill  -> 能力包
Pal    -> 会使用 Skill 和 Agent 的工作伙伴
Agent  -> 执行运行层
```

这三句话是 AgentPal 的定位钉子：

- Skill 是能力包，Pal 是会使用 Skill 的工作伙伴。
- Agent 是执行运行层，Pal 是会使用 Agent 的工作伙伴。
- 多 Pal 与多 Agent 目标一致，但 AgentPal 用更轻的组织层降低复杂度和成本。

Skill 通常让 AI 更会做某一类事情。Pal 拥有稳定岗位：身份、职责、知识、工作流、记忆规则、输出契约、协作边界和验收习惯。Agent Runtime 负责真实执行。

## 多 Pal 与多 Agent

多 Agent 系统通常会创建多个真实执行的 Agent。它很强，但也容易带来配置、上下文、成本、权限和结果合并的复杂度。

AgentPal 选择更轻的起点：

- Pal 负责组织工作、上下文、职责和验收。
- 宿主 Runtime 在需要真实文件、命令、工具或发布动作时执行任务。
- 如果当前 Runtime 已证明支持子 Agent 或外部 Agent，并且用户明确授权，Pal Team 可以为它们准备任务包和验收规则。

不是每个 AI 角色都必须变成一个独立运行的 Agent。很多角色更适合先成为稳定的 Pal：负责理解目标、塑形任务、选择上下文和验证结果。

## 当前已验证能力边界

v0.5 的公开声明必须保守。

| Runtime / mode | 状态 | 公开口径 |
| --- | --- | --- |
| Codex | verified | 已有 Codex-first AgentPal 工作区初始化和 Pal 协作证据。 |
| Codex child/background thread 与 subagent 使用 | limited / evidence-backed | 仅在当前 Codex 宿主有证据且用户授权时可写。 |
| Claude Code | limited | 只有 minimal handoff evidence；不声明 full host acceptance。 |
| Generic CLI Agent | compatibility path | 有 prompt-based 路径，但不声明广泛宿主验收。 |
| DeepSeek / DeepSeek-TUI | experimental / version-help only | 不能写成完整支持。 |
| Plan Mode | current UI evidence unavailable | 不能写成已真实 UI 验证。 |
| Goal Mode | limited | 有 active-goal 证据，但有 UI capture limitation。 |
| OpenCode / Gemini | unavailable in current evidence | 不能写成当前已支持。 |
| GitHub、Notion、Lark、Cloudflare 等外部系统 | not generally validated | AgentPal 可准备任务包，但不声明直接写回集成。 |

Host capability 必须来自 visible evidence、manual profile 或 runtime-reported profile。AgentPal 不会自动扫描用户系统。

## 内置官方 Pal

当前 official Pal 一共 10 个。事实来源是 [`workspace/organization/contacts/pals.json`](workspace/organization/contacts/pals.json)。

| Pal | 角色 | 适合处理 | 直接调用 |
| --- | --- | --- | --- |
| Mira | Main Pal / Leader / Conductor | 初始接待、路由、项目上下文、交接、总结 | `/pal Mira` |
| Atlas | Developer / Implementation Lead | 工程计划、代码任务包、实现评审 | `/pal Atlas` |
| Nova | Product / Strategy Lead | 产品定义、PRD、用户流程、优先级、路线图 | `/pal Nova` |
| Faye | AI Delivery Pal | 业务场景、用户流程、数据/接口清单、风险、Delivery Pack、`FAYE_BUILD_REQUEST` | `/pal Faye` |
| Vega | Research / Intelligence Lead | 调研计划、资料综合、证据矩阵、不确定性分析 | `/pal Vega` |
| Quinn | Quality / Verification Lead | 验收标准、回归检查、证据审查、发布门禁 | `/pal Quinn` |
| Morgan | Document / File Workflow Lead | 文档结构、文件工作流、Office/PDF 任务包 | `/pal Morgan` |
| Harper | Writing / Content Craft Lead | 写作、文案、叙事、语气、编辑、声明安全 | `/pal Harper` |
| Rhea | System / Runtime Safety Lead | Runtime 边界、权限、no-code 安全、发布安全 | `/pal Rhea` |
| PalSmith | Pal Asset Governor | 创建、体检、升级和治理 Pal 与 Pal Team | `/pal PalSmith` |

Mira 是默认入口 Pal。专业 Pal 默认不监听；Mira 会在适合时交给它们，用户也可以直接用 `/pal Name` 调用。

## 安装与 Codex 初始化

AgentPal 当前不是 npm / pip / CLI 安装包，而是一个本地工作区。

1. clone 或下载本仓库。
2. 把 AgentPal 目录保留为独立本地工作区。
3. 在 Codex 中把 AgentPal 目录作为项目打开。
4. 打开 [`prompts/codex/initialize-agentpal-workspace.md`](prompts/codex/initialize-agentpal-workspace.md)。
5. 把整篇 prompt 复制到 fresh Codex 对话中。
6. 确认 Mira 欢迎你，并列出当前 10 个 Pal。
7. 普通消息交给 Mira，或用 `/pal Name` 直接调用专业 Pal。

快速入口：

- [`START_HERE.md`](START_HERE.md)
- [`prompts/codex/README.md`](prompts/codex/README.md)
- [`docs/04-runtime-guides/01-use-with-codex.md`](docs/04-runtime-guides/01-use-with-codex.md)

## 绑定到外部项目

日常工作通常发生在你的真实项目里，而不是 AgentPal 工作区里。

AgentPal 使用 thin binding：

- 外部项目仍然是当前项目。
- AgentPal 工作区只是 Pal 来源和组织层。
- `.agentpal/` 只保存少量绑定文件。
- 不把 Pal Packs、docs、evals、release files、memory、reports 或 AgentPal 内部资产复制进外部项目。

当前项目绑定入口：

- Claude Code：[`prompts/claude-code/install-agentpal-current-project.md`](prompts/claude-code/install-agentpal-current-project.md)
- Generic CLI Agent：[`prompts/generic-cli-agent/install-agentpal-current-project.md`](prompts/generic-cli-agent/install-agentpal-current-project.md)

Codex-first 是当前已验证的发布主路径。其他宿主路径必须保留当前证据限制。

## 用 PalSmith 和 Faye 搭建自己的 AI 团队

AgentPal 内置 PalSmith 和 Faye，帮助用户从“使用内置 Pal”走向“搭建自己的 AI 团队”。

Faye 更适合把真实业务需求整理成落地方案：

- 业务场景
- 用户流程
- 数据清单
- 接口清单
- 风险与缺失信息
- 验收交接
- `FAYE_BUILD_REQUEST`

PalSmith 更适合设计和治理 Pal Team：

- 新 Pal 或团队蓝图
- Pal 职责与边界
- Pal Pack 结构
- knowledge / skill / workflow / runbook 分类
- 体检与治理建议

入口：

- [`docs/PalSmith.md`](docs/PalSmith.md)
- [`docs/03-user-guides/palsmith-v0.5-pal-creation-and-upgrade.md`](docs/03-user-guides/palsmith-v0.5-pal-creation-and-upgrade.md)
- [`docs/07-authoring-pals/README.md`](docs/07-authoring-pals/README.md)
- [`docs/03-pal-pack-standard/README.md`](docs/03-pal-pack-standard/README.md)

## 项目结构

| 路径 | 用途 |
| --- | --- |
| `AGENTS.md` | AgentPal mode 的 Runtime 指令 |
| `PAL.md` | 工作区身份 |
| `SKILL.md` | Skill-aware Runtime 入口 |
| `agentpal.json` | 结构化工作区元数据 |
| `prompts/` | 可复制的 Runtime prompts |
| `official/pals/` | 官方 Pal Packs |
| `workspace/organization/contacts/` | 中央 Pal 名册和 contact cards |
| `workspace/projects/` | 外部项目的中央记录 |
| `docs/` | 用户文档、概念、Runtime 指南、创建指南 |
| `standards/` | no-code 标准与协议 |
| `templates/` | public-safe 模板 |
| `examples/` | public-safe 示例 |
| `evals/` 和 `release/` | 验证与发布证据归档 |

## 文档入口

建议从这里开始：

- [`docs/README.md`](docs/README.md)
- [`docs/00-overview/00-what-is-agentpal.md`](docs/00-overview/00-what-is-agentpal.md)
- [`docs/01-concepts/07-why-pal.md`](docs/01-concepts/07-why-pal.md)
- [`docs/04-runtime-guides/00-runtime-compatibility.md`](docs/04-runtime-guides/00-runtime-compatibility.md)
- [`RESOURCE_INDEX.md`](RESOURCE_INDEX.md)

验证与发布记录仍然可查，但不是用户第一入口。

## 当前限制

- AgentPal 不自己执行任务。
- AgentPal 不包含 scanner、daemon、connector system、marketplace、installer 或 app runtime。
- AgentPal v0.5 不声明完整的非 Codex 宿主验收。
- AgentPal 不声明可直接写入 GitHub、Notion、Lark、Cloudflare、CRM 或客户系统；除非当前宿主 Runtime 对具体动作有明确授权和执行证据。
- 客户数据和私有项目事实不能进入 public examples、Pal Packs 或 global knowledge。
- Deep Conductor 是 no-code collaboration 和 mode-decision protocol，不是自动后台执行器。

## License

MIT。见 [`LICENSE`](LICENSE)。
