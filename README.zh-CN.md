# AgentPal

AgentPal 是给编程 Agent 使用的 Pal 层。

它不是 Agent 层，不是多 Agent 运行时，也不是执行层。AgentPal 给现有运行时提供一套结构化的 Pal 工作区：身份、知识、技能、上下文、记忆、输出契约、协作规则、审查习惯、总结方式和学习存储规则。

AgentPal v0.1.0-rc.1 是 Markdown / JSON / 协议工作区。它没有桌面 UI、Web UI、守护进程、扫描器、安装器、服务，也没有必须安装的运行时依赖。

## 当前运行方式

AgentPal v0.1.0-rc.1 只使用 Simple Pal Mode。

在 Simple Pal Mode 下：

- Mira 是默认 Main Pal、Leader Pal 和 Conductor。普通消息先从 Mira 开始。
- Mira 对实质任务逐案判断。
- 如果某个已注册 Pal 可以主责这个任务，Mira 只做简短交接，然后停止作答。
- owner Pal 在同一条回复中立即接手回答。
- owner Pal 使用自己的 `PAL.md`、`SKILL.md`、`pal.json`、相关资产、Output Contract，并在缺少资产时诚实说明 fallback。
- AgentPal 不在普通回答中展示运行模式元数据。

因为 Pal 层是普通文件和协议，AgentPal 可以配合 Codex、Claude Code、CodeWhale、Gemini CLI、DeepSeek-TUI 或其它能够读取 Markdown / JSON 的 Agent 运行时使用。

## 调度方法论

AgentPal 不对标大模型，也不声称超过 GPT、Claude 或其它模型。AgentPal 学习的是调度方法论：通过透明的 Pal 层，帮助用户更好地使用现有 Agent Runtime、模型、推理强度、Skill、插件、上下文、验收和记忆。

AgentPal 不和基础模型竞争。它研究的是怎样把已有 Agent Runtime 用得更好。

受 Fugu 等调度方法启发，AgentPal 区分两层：

- Fast Route：清晰任务交给一个合适的 Pal / Runtime / Skill。
- Deep Conductor：未来用于复杂任务的调度设计，包含 workflow topology、Context Access List、隔离、验收和 routing memory。

v0.1 先提供基础：Mira 作为默认 Main Pal / Leader Pal / Conductor、官方 Pal Pack、Simple Pal Mode、AI Judgement 路由、Context Slicing、Task Package，以及 Claude Code / 通用 CLI Agent 一段式项目接入。未来设计会继续发展 Capability Inventory、Context Access List、Routing Reward Memory、Workflow Topology、Deep Conductor 和 PalBench 评估。

参考：`docs/research/agentpal-orchestration-methodology.md`、`docs/research/fugu-inspired-agentpal-methodology.md`、`docs/research/palbench-design.md`。

R33 新增了小样本 PalBench smoke 验证：`docs/research/palbench-r33-small-sample-report.md`。它展示了任务包清晰度、验收意识、文件级上下文风险控制和用户路由负担方面的初步证据。它不是统计显著 benchmark，也不比较底层大模型能力。

## Mira 单一入口

多数情况下，用户只需要先找 Mira。不需要反复自己判断应该叫 Atlas、Nova、Quinn、Codex、Claude Code、某个 Skill、某个插件，还是未来的 Deep Conductor。

Mira 会接收目标，检查 contacts / registry，判断任务归属，需要时组织受限上下文，然后交给 owner Pal。显式 `/pal 名称` 仍然可用。

## 上下文切片与 Token 策略

AgentPal 的上下文优势来自“按需读取正确切片”，不是把所有内容都塞进上下文。

普通任务中：

- Mira 读取用户目标、任务状态、当前规则和 contacts / registry 摘要。
- Mira 不会为了路由而读取所有 Pal 的专业知识。
- owner Pal 读取自己的最小必需文件和 1-3 个相关资产。
- 项目文件、memory、examples、evals、reports、imports 和 future design 文档只在任务需要时读取。
- `RESOURCE_INDEX.md` 和各 Pal 的 `index.md` 是导航索引，不是默认全量上下文入口。

AgentPal v0.1.0-rc.1 还没有真实 token 计量，但定义了上下文预算、文件读取层级和资产使用报告，方便审计。

初始化默认使用短流程。它只读取根规则、工作区元数据、contacts / registry JSON、Mira 最小资产和 Runtime Response Gate。深度初始化只用于诊断、发布检查、registry 修复、初始化失败或用户明确要求。

通过目录列表、registry 或索引知道文件名，只算 `index_known_*`，不代表读取了正文。真正打开读取过内容的文件才记录为 `content_read_*`。

Mira 有自己的秘书输出契约：`pals/Mira-main/core/output-contract.md`。它允许 Mira 做接待、澄清、摘要、交接、Task Package 压缩和资产报告，但禁止 Mira 代替其它 owner Pal 输出专业正文。

## Pal 是什么

Pal 不是独立运行进程。Pal 是面向任务的工作包，包含：

- 身份和职责
- 知识和技能
- 上下文和记忆边界
- 输出契约
- 审查和总结习惯
- 学习和 Skill 存储规则

真正读取文件、写入文件、运行命令、调用工具、发布、删除等动作仍由当前运行时完成。AgentPal 负责帮助运行时判断谁来回答、使用哪些资产、怎样诚实汇报。

## 内置 Pal

内置 Pal 包括：

- Mira：Main Pal、Leader Pal、Conductor 和秘书式协调者
- Atlas：开发视角
- Vega：研究和证据视角
- Rhea：本机系统和环境视角
- Quinn：质量、风险、证据和验收视角
- Morgan：文档和文件工作流视角
- Harper：写作和沟通视角
- Nova：产品和决策视角

能力说明只是非绑定示例，不是路由表。owner 选择由 AI 根据当前请求、上下文、约束、风险、期望输出和可用 Pal 资产逐案判断。

## 快速开始

1. 在你的 Agent 运行时中打开这个工作区。
2. 运行或粘贴 `INIT_PROMPT.md`。
3. 像普通对话一样先找 Mira。
4. 用 `/pal Name` 直接点名某个 Pal。
5. 需要新增 Pal 时，把 Pal Pack 放到 `pals/` 下，并刷新 contacts / registry。

## 在 Claude Code 中使用

真实项目里推荐采用“当前项目优先”的方式：

```text
cd <your-project>
claude
```

然后粘贴 `prompts/claude-code/install-agentpal-current-project.md`，并填写你的 AgentPal 路径：

```text
Please connect AgentPal to the current project.
AGENTPAL_HOME = <path-to-AgentPal>
```

这个一段式接入提示词会创建或更新 `.agentpal/`、`CLAUDE.md`、`AGENTS.md` 和 `.claude/settings.local.json`。它会合并 `permissions.additionalDirectories`，让 Claude Code 可以访问 AgentPal 工作区路径。

`.claude/settings.local.json` 是本机配置，不应提交。接入提示词会在需要时把它加入 `.gitignore`。

默认不要求用户记住 `claude --add-dir <path-to-AgentPal>`。如果当前 Claude Code 会话没有立即读取到新增目录，可以重启 Claude Code，或临时使用 `/add-dir <path-to-AgentPal>`。

## 在通用 CLI Agent 中使用

对 CodeWhale、Gemini CLI 或其它能读取 Markdown/JSON 的 Agent Runtime：

```text
cd <your-project>
<your-cli-agent>
```

然后粘贴 `prompts/cli-agent/install-agentpal-current-project.md` 并提供 AgentPal 路径。通用提示词会创建 `.agentpal/` 并更新 `AGENTS.md`，不依赖 Claude Code 设置。

## 外部项目工作组

AgentPal 可以作为工作组引用加入外部项目。在外部项目绑定会话中：

- 外部项目是当前项目
- AgentPal 只是 Pal 来源和路由参考
- “这个项目”指外部项目，不指 AgentPal 工作区

项目内接入优先使用 Claude Code 或通用 CLI 的一段式提示词。`prompts/join-external-project-workgroup.md` 仍可用于在 AgentPal 工作区会话中由 AgentPal 主动绑定外部项目。

## Skill 存储

如果用户明确要求把方法保存成 Skill，或类似操作超过 3 次，owner Pal 会把正式 Skill 存到自己的目录：

```text
pals/<Owner-Pal-Directory>/skills/<skill-id>/SKILL.md
```

除非用户明确要求创建全局运行时 Skill，否则不要把 AgentPal Pal-owned Skill 存入全局 runtime skill 目录。

## 未来运行时编排

子工作流、外部 Runtime 运行时、MCP 托管 Agent、远程 Agent 服务等未来设计，单独记录在 `docs/99-reference/future-agent-orchestration.md`。这些内容不属于 AgentPal v0.1.0-rc.1 当前运行行为。
