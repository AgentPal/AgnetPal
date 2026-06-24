# Deliverable-Aware Task Judgement Example

## Status

Current for AgentPal `v0.1.0-rc.1`.

This example shows a staged Task Package in Simple Pal Mode. It does not activate Deep Conductor, Subagent Mode, parallel child workflows, external Agent calls, or automatic multi-Pal execution.

## User Request

```text
帮我调研 26 年 Agent 发展趋势，撰写详细的分析报告，并将报告内容制作成精美的 HTML 页面。
```

## Expected Mira Shape

```text
Mira：这是一个复合交付任务，不只是单一研究任务。

我会保持 Conductor 角色，先按交付物和阶段组织：
1. 研究与内容阶段：形成趋势调研、证据表、分析报告结构和结论；研究能力是这个阶段的候选需求。
2. 实现与交付物落地阶段：把已确认的报告内容做成可查看的 HTML 页面；开发实现能力是这个阶段的候选需求。
3. 验收阶段：检查内容事实边界、页面可打开性、视觉完成度、链接和交付证据。

这些是基于当前目标的候选分工，不是固定路由。当前 v0.1 仍是 Simple Pal Mode，我会把它整理成分阶段 Task Package，让当前 Runtime 按证据要求执行。
```

## Task Judgement Packet

```yaml
schema: agentpal.task-judgement.v0.1
task_goal: research 2026 Agent trends, write an analysis report, and deliver it as an HTML page
domain_focus: Agent development trends
deliverables:
  content_deliverables:
    - deliverable: detailed analysis report
      acceptance_note: contains evidence, structure, conclusions, and uncertainty notes
  final_deliverables:
    - deliverable: polished HTML page
      acceptance_note: can be opened and inspected as a rendered page
complexity: complex
risk_level: medium
work_stages:
  - stage_id: research-content
    stage_goal: collect current evidence and shape the report
    capability_needs:
      - current-source research
      - evidence table
      - uncertainty handling
    pal_candidates:
      - pal_id: vega-research
        candidate_role: content_stage_owner
        why_candidate: the stage requires research planning, source quality judgement, and evidence synthesis
        not_a_fixed_route: true
    runtime_candidates:
      - runtime_id: current-runtime
        why_candidate: may browse, read sources, or inspect files when authorized
        not_a_fixed_route: true
    skill_candidates: []
    verification_needs:
      - sources and dates must be visible
  - stage_id: implementation-deliverable
    stage_goal: convert approved report content into a polished HTML artifact
    capability_needs:
      - file implementation
      - page structure
      - visual layout judgement
      - browser or file-open verification
    pal_candidates:
      - pal_id: atlas-developer
        candidate_role: implementation_stage_owner
        why_candidate: the stage requires implementation-oriented task packaging and evidence review
        not_a_fixed_route: true
    runtime_candidates:
      - runtime_id: current-runtime
        why_candidate: may create and verify files when authorized
        not_a_fixed_route: true
    skill_candidates: []
    verification_needs:
      - generated HTML path exists
      - page can be opened or inspected
      - no private paths or secrets are embedded
  - stage_id: verification
    stage_goal: check content, rendering, and completion evidence
    capability_needs:
      - evidence review
      - acceptance criteria
      - risk check
    pal_candidates:
      - pal_id: quinn-quality
        candidate_role: verifier
        why_candidate: the stage benefits from quality and evidence review
        not_a_fixed_route: true
    runtime_candidates: []
    skill_candidates: []
    verification_needs:
      - pass/fail with evidence gaps
overall_conductor:
  default: Mira
  current_conductor: Mira
  note: Mira keeps overall coordination because the request has multiple deliverables and stages
recommended_mode:
  candidate: staged_task_package
  note: active v0.1 written package, not Deep Conductor execution
decision_basis:
  - user_goal
  - deliverables
  - capability_needs
  - available_pals
  - available_runtime
  - context
  - risk
hardcoded_routing_policy:
  fixed_keyword_routes_allowed: false
  task_domain_fixed_routes_allowed: false
  candidates_are_not_routes: true
```

## Context Access List Sketch

```yaml
schema: agentpal.context-access-list.v0.1
workflow_id: agent-trend-html-report-example
stage_id: implementation-deliverable
stage_goal: create the HTML artifact from accepted report content
recipient_type: pal
recipient_candidate:
  id: atlas-developer
  why_candidate: implementation-stage judgement is needed before runtime file edits
  not_a_fixed_route: true
task: prepare implementation Task Package for the HTML deliverable
can_read_summaries:
  - summary_id: accepted-research-report-content
    reason: implementation should use approved content, not raw full research traces
can_receive_outputs_from:
  - step_id: research-content
    output_type: accepted report content and evidence summary
cannot_read:
  - full_agentpal_workspace
  - all_pals
  - unrelated_pal_memory
  - private_user_memory
  - credentials_or_secrets
need_output: implementation Task Package with file path, layout requirements, acceptance criteria, and evidence required
verification_required: true
```

## Staged Task Package

```text
Task Package
- Goal: deliver a sourced Agent trend analysis report as a polished HTML page.
- Domain focus: Agent development trends.
- Content deliverables: research report, evidence summary, uncertainty notes.
- Final deliverables: HTML page.
- Work stages:
  1. Research / content stage: collect and synthesize evidence.
  2. Implementation stage: produce the HTML artifact from accepted content.
  3. Verification stage: check sources, rendering, links, file path, and public-safe boundary.
- Candidate notes: candidates are selected by AI judgement from current contacts / registry and runtime availability. They are not fixed routes.
- v0.1 boundary: staged Task Package only; no automatic Deep Conductor or Subagent execution.
```
