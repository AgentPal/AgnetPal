<!-- Future design only. Not active in AgentPal v0.1 runtime. / 未来设计，仅作规划参考，不属于 AgentPal v0.1 当前运行行为。 -->

# AI Routing Judgement Regression

## Purpose

Verify that AgentPal chooses Mira direct answer, Codex generic, Simple Pal Mode, or same-response Pal consultation through AI judgement, not fixed keywords.

## Global Pass Criteria

- No response may say a phrase "hits" a route rule.
- No task/domain wording may require a fixed Pal set.
- Subagent Mode is not active in AgentPal v0.1.0-rc.1 task handling.
- Simple explanation and low-token requests must stay lightweight.
- Explicit `/pal Name` and explicit Codex generic requests remain deterministic.

## Case 1: Multi-Perspective Complex Task

Inputs:

```text
这个项目下一版值不值得继续做？如果值得，怎么开发，怎么验收？
```

```text
帮我从产品、工程和发布质量三个角度看一下这个项目下一步怎么走。
```

```text
我不想只听技术建议，你帮我判断继续做有没有价值、工程上怎么推进、发布前怎么把关。
```

Expected:

- Mira identifies that several independent perspectives may be useful.
- Mira uses Simple Pal Mode: one owner, bounded consultant/reviewer sections, or a Task Package.
- The answer must not claim Subagent Mode or parallel child workflows were started.
- The answer does not claim Nova, Atlas, or Quinn are required by wording alone.

## Case 2: Explicit Single Pal

Input:

```text
/pal Atlas 帮我看下一步怎么开发。
```

Expected:

- Direct Pal command is honored if Atlas exists.
- Atlas may answer in Simple Pal Mode.
- No automatic Nova / Quinn consultation unless the active AI explains why it is materially needed; no Subagent spawn in v0.1.0-rc.1.

## Case 3: Simple Explanation

Input:

```text
开发计划和验收计划有什么区别？
```

Expected:

- Mira or Codex generic can answer directly.
- Subagent Mode is not used merely because "开发" and "验收" appear.
- If Subagent Mode is used, this case fails.

## Case 4: Save Token

Input:

```text
简单说一下这个项目下一步，不要多 Pal，不要开 subagent，省 token。
```

Expected:

- Respect the user constraint.
- Do not start Subagent Mode.
- Mira may answer briefly or suggest a single Pal only if useful.

## Case 5: Codex Generic

Input:

```text
不要使用任何 Pal 的知识和流程，只用 Codex 通用能力回答：这个项目继续开发应该注意什么？
```

Expected:

- Response starts with `Codex generic answer:`.
- No Mira / Atlas / Nova / Quinn prefix.
- No Subagent Mode.

## Case 6: Ambiguous Request

Input:

```text
这个项目我有点迷茫，你觉得下一步怎么搞？
```

Expected:

- Mira may ask a clarifying question or give a lightweight judgement.
- No fixed Pal route.
- If multiple perspectives are useful, Mira should keep them inside Simple Pal Mode or prepare a Task Package. Do not suggest active Subagent Mode for v0.1.0-rc.1.

## Fail Signs

- Mentions keyword matching as the reason for routing.
- Says a semantic phrase requires a fixed Pal set.
- Starts subagents for a short definition question.
- Ignores "不要多 Pal" or "不要开 subagent".
- Uses a Pal prefix for explicit Codex generic requests.

