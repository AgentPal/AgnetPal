<!-- Future design only. Not active in AgentPal v0.1 runtime. / 未来设计，仅作规划参考，不属于 AgentPal v0.1 当前运行行为。 -->

# Subagent Parallel Case-By-Case Self-Test

This self-test is a non-binding example. It must not be used as a keyword routing rule.

## Input

```text
这个项目下一版值不值得继续做？如果值得，怎么开发，怎么验收？
```

## Expected Judgement

Mira decides case-by-case whether bounded Simple Pal Mode perspectives or a Task Package are useful.

Subagent Mode is future design only in AgentPal v0.1.0-rc.1 and is not keyword-triggered or invoked.

If a future design document discusses Subagent Mode, the selected Pal set must be justified by the current task and available assets. No fixed Pal set is required by the wording alone.

## Expected Current Route

- select owner Pal case-by-case
- select consultant Pal(s) or reviewer Pal(s) case-by-case only when useful
- keep the work in Simple Pal Mode or produce a Task Package
- do not spawn, wait, or close child workflows
- do not record `agent_id` evidence

## Expected Role Boundaries

- each selected Pal stays inside its own Output Contract
- each selected Pal reads required identity and output assets
- Mira preserves each Pal's conclusion, agreements, conflicts, missing evidence, final recommendation, and next action

## Fail If

- Mira answers all professional content herself.
- A fixed Pal set is required because of a keyword phrase.
- Any Pal omits required assets or output contract.
- The answer claims Subagent Mode started in v0.1.0-rc.1.
- Mira merges Pal conclusions into one unlabeled paragraph.
- Any `agent_id` / wait / close evidence is invented.



