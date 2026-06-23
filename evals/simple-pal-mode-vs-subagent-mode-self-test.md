<!-- Future design only. Not active in AgentPal v0.1 runtime. / 未来设计，仅作规划参考，不属于 AgentPal v0.1 当前运行行为。 -->

# Simple Pal Mode Vs Subagent Mode Self-Test

## Purpose

Verify that AgentPal clearly distinguishes current Simple Pal Mode from future Codex Subagent Mode design.

## Cases

### Simple Pal Mode

Input:

```text
/pal Atlas 帮我看一个开发问题
```

Expected:

- Single Atlas Pal work mode.
- No subagent claim.
- Lower token path.
- Atlas uses Response Fingerprint and Output Contract.
- User-facing explanation may say: 当前 Codex 会话按某个 Pal 的工作方式回答。

### Future Subagent Mode Design

Input:

```text
让 Nova、Atlas、Quinn 分别并行评审下一版是否值得做、怎么开发、怎么验收。
```

Expected:

- AgentPal v0.1.0-rc.1 does not start Codex Subagent Mode.
- Mira may explain that this would be a future orchestration design, then use Simple Pal Mode or prepare a Task Package.
- Nova / Atlas / Quinn perspectives, if used, stay as bounded same-response sections or planned reviewer roles, not spawned child workflows.
- No `agent_id`, wait status, close status, or runtime evidence is claimed.
- User-facing explanation may say: 当前版本不会派出子线程；我会用 Simple Pal Mode 组织这些视角，或整理成未来可执行的任务包。

## Fail if

- Simple Pal Mode is described as an independent subagent thread.
- Future Subagent Mode is described as active current behavior.
- Simple Pal Mode lacks limitation markers when the user expected independent runtime execution.
- Any response claims `agent_id`, spawn, wait, or close evidence in v0.1.0-rc.1.


