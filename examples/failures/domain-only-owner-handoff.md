# Domain-Only Owner Handoff Failure

## Status

Regression example for AgentPal `v0.1.0-rc.1`.

## User Request

```text
帮我调研 26 年 Agent 发展趋势，撰写详细的分析报告，并将报告内容制作成精美的 HTML 页面。
```

## Incorrect Behavior

```text
Mira：这个任务属于研究型主任务，我把 owner handoff 给 Vega。接下来由 Vega 负责趋势调研、报告结构和结论，我这边的当前 Codex 执行层再把结果落成 HTML 页面。
```

## Why This Fails

- It judges only the topic domain.
- It misses the final deliverable.
- It treats a content-stage owner as the whole-task owner.
- It lets the Runtime appear to take over the implementation stage without Pal-layer judgement.
- It does not identify research, content, implementation, and verification stages.
- It does not produce a staged Task Package.

## Correct Behavior

The current Main Pal or owner Pal should perform deliverable-aware Task Judgement:

- identify the domain focus
- identify content deliverables and final deliverables
- identify work stages
- identify capability needs
- name Pal / Runtime / Skill candidates, not fixed routes
- include verification needs
- keep v0.1 as Simple Pal Mode only

For this request, Mira should keep Conductor responsibility and organize a staged Task Package. A research-capable Pal may be a candidate for the research / content stage. A development-capable Pal may be a candidate for the implementation stage. A quality-capable Pal may be a verification candidate. These are candidates produced by AI judgement, not keyword routes.

## Boundary

This example must not be converted into a rule that any artifact type always belongs to a specific Pal. It exists to prevent domain-only routing and Runtime-bypasses-Pal-layer regressions.
