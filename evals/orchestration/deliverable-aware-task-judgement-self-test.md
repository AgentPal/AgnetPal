# Deliverable-Aware Task Judgement Self-Test

## Status

Current for AgentPal `v0.1.0-rc.1`.

This self-test checks whether the first Pal, current Main Pal, or owner Pal handles composite deliverable tasks without keyword routing.

## Case A: Default Mira Entry

Input:

```text
帮我调研 26 年 Agent 发展趋势，撰写详细分析报告，并制作成精美 HTML 页面。
```

Expected:

- Output starts with `Mira：`.
- Mira identifies a composite deliverable task.
- Mira keeps Conductor responsibility.
- Mira does not only hand off to a research-stage Pal.
- Mira identifies the final deliverable.
- Mira identifies research, content, implementation, and verification stages.
- Mira names selected or provisional stage owner Pals before asking clarification questions.
- Mira outputs Pal stage owners plus Runtime / Skill executor candidates, not fixed routes.
- The output does not contain `HTML 必须 Atlas`.
- The output does not contain keyword routing or task/domain -> fixed Pal rules.
- Runtime does not bypass the Pal layer for the implementation stage.
- The HTML/page/frontend implementation stage is not owned by current Codex Runtime alone.
- If Atlas is registered and no better registered owner is justified, Atlas is named as the implementation-stage owner.
- v0.1 output is a staged Task Package or staged judgement, not active Deep Conductor.
- A quality / evidence review candidate may be included when useful, but not as a fixed route.

## Case B: Direct Atlas Call

Input:

```text
/pal Atlas 帮我调研 26 年 Agent 发展趋势，撰写详细分析报告，并制作成精美 HTML 页面。
```

Expected:

- Output starts with `Atlas：`.
- Atlas does not only do the HTML stage.
- Atlas does not directly reject the research stage.
- Atlas performs deliverable-aware Task Judgement.
- Atlas explains which stages it can responsibly own.
- Atlas names selected or provisional stage owner Pals before asking clarification questions.
- Atlas identifies the research/content stage as needing research capability candidates.
- Atlas may suggest Mira as upper-level Conductor or produce a staged Task Package.
- The output does not contain `HTML 必须 Atlas`.
- The output does not contain fixed keyword routing.
- The output keeps v0.1 as Simple Pal Mode only.

## Case C: Direct Vega Call

Input:

```text
/pal Vega 帮我调研 26 年 Agent 发展趋势，写报告，并做成 HTML 页面。
```

Expected:

- Output starts with `Vega：`.
- Vega does not treat the whole task as only research.
- Vega states that it is suited to the research/content stage.
- Vega identifies the final HTML page as requiring an implementation stage.
- Vega names selected or provisional stage owner Pals before asking clarification questions.
- If Atlas is registered and no better registered owner is justified, Vega names Atlas as the implementation-stage owner.
- Vega outputs a staged Task Package or implementation-stage candidate notes.
- The output does not contain fixed keyword routing.
- The output does not let the Runtime directly take over implementation without Pal-layer judgement.
- The output keeps v0.1 as Simple Pal Mode only.

## Fail Conditions

- Any response says or implies a specific artifact type always belongs to a specific Pal.
- Any response uses a task/domain -> fixed Pal table.
- Any first Pal asks only clarification questions before naming stage owner Pals.
- Any response says a Runtime will simply handle the remaining stage after one content Pal finishes.
- Any response names current Codex Runtime or another Runtime as the sole owner of a page / HTML / code implementation stage.
- Any response says a later Pal or Runtime will decide all stage owners.
- Any response claims Deep Conductor, Subagent Mode, external Agent calls, or multi-runtime orchestration are active in v0.1.

## Notes

Pal capability descriptions are allowed as orientation. They fail this test only if they are turned into fixed routes.
