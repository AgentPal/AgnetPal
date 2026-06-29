# AgentPal

**AgentPal 是一个用于搭建多 AI 团队的轻量框架。**

AgentPal 可以安装或挂载到 Codex、Claude Code、OpenCode 等 Agent Runtime 下使用，让现有 Agent 获得一套由多个专业 Pal 组成的 AI 团队组织层。

AgentPal 不替代 Codex、Claude Code、OpenClaw、Hermes、workbuddy 等 Agent 系统。
它关注的是另一个问题：

> 如何用更轻、更容易维护、更低成本的方式，组织一个可协作的 AI 团队。

一句话理解：

> **AgentPal = 给现有 Agent 增加一个 Pal 团队组织层。**

---

## 安装

AgentPal 当前是一个本地工作区，不是 npm / pip 包，不是 CLI installer，也不是后台服务。

你可以用两种方式安装：

### 方式 A：下载 release package

1. 从 GitHub Release 下载 `agentpal-v0.5.0-rc.1.zip`。
2. 解压到本地目录，例如 `<path-to-AgentPal>`。
3. 把这个目录作为 AgentPal 工作区保留。
4. 在能够读取本地 Markdown / JSON 文件的 Agent Runtime 中打开它。

### 方式 B：clone 仓库

```bash
git clone https://github.com/AgentPal/AgentPal.git
cd AgentPal
```

然后把 clone 下来的目录作为 AgentPal 工作区打开。

当前推荐路径是 Codex。打开 AgentPal 目录后，复制 [`prompts/codex/initialize-agentpal-workspace.md`](prompts/codex/initialize-agentpal-workspace.md) 的内容到 fresh Codex 对话中，确认 Mira 欢迎你并列出当前 Pal。

---

## Pal 是什么？

AgentPal 使用 **Pal** 作为 AI 团队的基本组织单位。

在 AgentPal 中：

```text
Skill 是能力包。
Pal 是会使用 Skill 的工作伙伴。

Agent 是执行运行层。
Pal 是会使用 Agent 的工作伙伴。
```

也就是说，Pal 不是 Skill，也不是完整 Agent Runtime。

Pal 位于 Skill 和 Agent 之间：

```text
Skill  -> 能力包
Pal    -> 会使用 Skill 和 Agent 的工作伙伴
Agent  -> 执行运行层
```

一个 Pal 可以拥有自己的身份、职责、知识、记忆、Skill、流程和协作边界。
它知道自己负责什么，也知道什么时候应该使用某个 Skill，什么时候应该把任务交给 Codex、Claude Code、OpenCode 或其他 Agent Runtime 执行。

---

## Skill、Pal、Agent 的关系

### Skill 是能力包

Skill 通常是一组可复用的能力、提示词、流程或工具使用说明。

例如：

- 写作风格 Skill
- 代码审查 Skill
- Office 文档处理 Skill
- 搜索与调研 Skill
- 某个工具或插件的使用 Skill

Skill 的价值是让 AI 更会做某一类事情。

但 Skill 通常比较轻，它一般不承担长期角色，也不负责记忆、协作、项目理解和团队分工。

> **Skill 让 AI 拥有某种能力。**

### Agent 是执行运行层

Agent 是真正执行任务的运行层。

例如 Codex、Claude Code、OpenCode、OpenHands，或者 OpenClaw、Hermes、workbuddy 等系统中创建出来的 Agent。

Agent 可以读写文件、调用工具、运行命令、规划步骤、完成任务。

> **Agent 负责执行。**

### Pal 是工作伙伴

Pal 是会使用 Skill 和 Agent 的工作伙伴。

一个 Pal 可以：

- 拥有明确身份和职责
- 记住用户、项目和历史工作
- 使用自己的知识和流程
- 引用和组合多个 Skill
- 判断应该调用哪个 Agent Runtime
- 与其他 Pal 协作
- 把任务拆给合适的 Agent 或子 Agent
- 汇总执行结果并反馈给用户

> **Pal 负责理解角色、组织协作、使用 Skill，并指挥 Agent 执行。**

---

## Pal 与 Skill 的区别

| 对比项 | Skill | Pal |
| --- | --- | --- |
| 核心定位 | 能力包 | 会使用能力包的工作伙伴 |
| 是否有身份 | 通常没有 | 有 |
| 是否有长期职责 | 通常没有 | 有 |
| 是否有记忆 | 通常没有 | 有 |
| 是否有知识体系 | 有限 | 有 |
| 是否能组合多个 Skill | 有限 | 可以 |
| 是否能与其他角色协作 | 通常不能 | 可以 |
| 是否能判断使用哪个 Agent | 通常不能 | 可以 |
| 更像什么 | 工具能力 | 团队成员 |

简单说：

> **Skill 是能力。Pal 是会使用能力的人。**

---

## Pal 与 Agent 的区别

| 对比项 | Agent | Pal |
| --- | --- | --- |
| 核心定位 | 执行运行层 | 会使用 Agent 的工作伙伴 |
| 是否负责真实执行 | 是 | 通常交给 Agent 执行 |
| 是否读写文件 / 调用工具 | 是 | 通过 Agent 或 Skill 完成 |
| 是否有稳定角色身份 | 不一定 | 有 |
| 是否有独立记忆和知识 | 取决于系统 | 有 |
| 是否适合轻量创建多个角色 | 成本较高 | 更轻 |
| 是否适合组织 AI 团队 | 可以，但通常更重 | 天然适合 |
| 更像什么 | 执行者 / 运行时 | 团队成员 / 任务负责人 |

AgentPal 不想重新造一个 Agent Runtime。

它的目标是：

> **让现有 Agent 拥有团队、角色、记忆、流程和协作能力。**

---

## 多 Pal 与多 Agent 的区别

多 Pal 和多 Agent 的目标其实是一致的：

> 都希望用多个 AI 角色协作，完成比单个 AI 更复杂的任务。

区别在于实现方式。

这里比较的不是 AgentPal 和 OpenClaw、Hermes、workbuddy 这些系统本身。
而是比较：

```text
AgentPal 创建的多 Pal 团队
vs
OpenClaw / Hermes / workbuddy 等系统中创建出来的多 Agent 团队
```

| 对比项 | 多 Agent | 多 Pal |
| --- | --- | --- |
| 目标 | 多角色协作完成任务 | 多角色协作完成任务 |
| 基本单位 | Agent | Pal |
| 执行方式 | 多个 Agent 分别运行 | Pal 组织任务，按需调用 Agent |
| 使用复杂度 | 通常较高 | 更轻 |
| 运行成本 | 可能较高 | 可控 |
| 上下文管理 | 多 Agent 间较复杂 | Pal 共享组织层上下文 |
| 是否每个角色都要运行成 Agent | 通常是 | 不需要 |
| 适合普通用户搭建团队 | 有门槛 | 更友好 |
| 适合复杂任务 | 适合 | 也适合，可按需调用多 Agent |

AgentPal 的思路是：

> **不是所有 AI 角色都必须变成一个独立运行的 Agent。**

很多时候，一个 Pal 只需要拥有清晰的身份、知识、记忆和流程，就能很好地承担某个团队角色。
只有当任务真的需要独立上下文、并行执行、隔离环境或专业工具链时，Pal 才需要调用子 Agent 或外部 Agent。

所以：

```text
多 Agent = 多个执行智能体
多 Pal   = 多个会协作、会使用 Agent 的工作伙伴
```

AgentPal 可以使用多 Agent，但不强制所有角色都变成 Agent。

---

## AgentPal 内置 Pal

AgentPal 内置了一组常用 Pal，帮助用户开箱即用地搭建 AI 团队。

当前 v0.5 内置 Pal 以 [`workspace/organization/contacts/pals.json`](workspace/organization/contacts/pals.json) 为准。

| Pal | 角色 | 主要用途 |
| --- | --- | --- |
| Mira | 主秘书 / 总协调 | 理解用户需求，协调 Pal、Agent、Skill 与项目上下文 |
| PalSmith | Pal 创建与治理专家 | 创建、优化、体检、升级 Pal 和 Pal 团队 |
| Faye | FDE / 方案设计专家 | 梳理业务场景、用户流程、数据、接口、风险和交付路径 |
| Atlas | 开发专家 | 负责代码实现、架构分析、工程任务拆分与技术执行 |
| Nova | 产品与体验专家 | 负责产品设计、用户流程、交互体验与功能取舍 |
| Quinn | 测试与质量专家 | 负责测试设计、验收标准、回归检查和质量评审 |
| Vega | 调研专家 | 负责资料调研、外部信息整理和知识分析 |
| Morgan | 文档与文件工作流专家 | 负责文档结构、文件工作流、Office/PDF 任务包 |
| Harper | 写作与内容专家 | 负责写作、文案、叙事、语气、编辑和声明安全 |
| Rhea | 系统与 Runtime 安全专家 | 负责 Runtime 边界、权限、no-code 安全和发布安全 |

---

## 用 PalSmith 和 Faye 搭建自己的 AI 团队

AgentPal 内置的 PalSmith 和 Faye，可以帮助用户从“使用内置 Pal”，进一步走向“创建自己的专业 AI 团队”。

### PalSmith

PalSmith 负责创建和治理 Pal。

它可以帮助你：

- 创建一个新 Pal
- 设计 Pal 的身份、职责、知识、记忆和 Skill
- 检查 Pal 是否职责过宽、过弱或重复
- 升级已有 Pal
- 设计一个完整 Pal 团队

### Faye

Faye 负责 FDE 式方案设计。

她可以帮助你把真实业务需求整理成：

- 业务场景定义
- 用户流程
- 数据清单
- 系统接口清单
- 风险点
- 验收标准
- 交付步骤
- 需要哪些 Pal 协作
- 哪些部分需要开发
- 哪些部分可以由现有 Agent / Skill 完成

PalSmith 更擅长搭建 AI 团队。
Faye 更擅长把真实业务变成可落地方案。

---

## 开源协议

AgentPal 使用 MIT License 开源。
