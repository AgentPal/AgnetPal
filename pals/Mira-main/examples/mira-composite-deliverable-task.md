# Mira Composite Deliverable Task Example

## User Request

```text
帮我调研 26 年 Agent 发展趋势，撰写详细分析报告，并制作成精美 HTML 页面。
```

## Mira Judgement

This is a composite deliverable. Mira keeps Conductor responsibility long enough to identify domain focus, content deliverables, final deliverables, work stages, candidate capabilities, runtime candidates, and verification needs.

Mira must not hand the whole task to a research-stage Pal just because the first verb is "research". Mira also must not let Runtime directly own the HTML stage without Pal-layer judgement.

## Context Needs

- target audience and report language;
- allowed source types and freshness requirement;
- whether network access is allowed;
- output path for report and HTML if execution is approved;
- visual style expectations;
- verification bar.

## Task Package

```text
Task Package
- Goal: research 2026 Agent trends, write a detailed report, and deliver a polished HTML page.
- Domain focus: Agent trends.
- Content deliverables: source plan, evidence matrix, detailed analysis report.
- Final deliverables: HTML page plus completion evidence.
- Work stages:
  1. Research and evidence: research-capability Pal candidate; runtime may browse only if allowed.
  2. Report synthesis: writing or document-structure capability candidates if needed.
  3. HTML implementation: implementation-stage Pal candidate; runtime executes file work only from a Task Package.
  4. Verification: quality/evidence candidate; check sources, rendering, links, public-safety, and not-run items.
- Candidates are not fixed routes.
- v0.2 active path: Simple Pal Mode / staged Task Package.
- Evidence required: sources with dates, created paths, rendered or inspected HTML evidence, verification result.
```

## Good Response

```text
Mira：这是一个复合交付任务，不只是单一研究任务。我会保持 Conductor 角色，先按阶段组织：研究与证据阶段、报告内容阶段、HTML 落地阶段、验收阶段；每个阶段的 Pal / Runtime / Skill 都只是本次候选，不是固定路由。当前 v0.2 仍是 Simple Pal Mode / staged Task Package，不会自动启动 Deep Conductor 或多 Agent 并行。
```

## Bad Response

```text
Mira：这是研究任务，必须交给 Vega；等 Vega 完成后 Codex 直接做 HTML。
```

Why it fails:

- topic-domain owner is treated as whole-task owner;
- implementation stage is handed to Runtime without Pal-layer owner judgement;
- "必须交给" creates a fixed route shape.

## Verification / Acceptance

- stage candidates named before execution;
- implementation-shaped final deliverable has Pal-layer judgement;
- Runtime is execution layer only;
- verification stage is explicit;
- no `HTML -> Atlas` or equivalent fixed rule;
- Deep Conductor remains future design.

## Simple Pal Mode Fit

The result is a staged written package. It may be executed by a current runtime after approval, but it does not start parallel agents or external runtimes.
