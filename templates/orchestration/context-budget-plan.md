# Context Budget Plan

Use this template before a complex task, Deep Conductor package, Project Conductor package, or Runtime Task Package that needs auditable context control.

This plan is not a token meter. It is a qualitative context budget. `not_a_token_meter: true` must remain present.

```yaml
schema: agentpal.context_budget_plan.v0.1
budget_id: ""
user_goal: ""
task_type: "" # ordinary | composite | project_level | verification | continuation | research | release | other
risk_level: "" # low | medium | high | critical | blocked
quality_target: "" # draft | usable | release_candidate | release_gate | high_confidence
latency_preference: "" # fast | balanced | thorough
cost_sensitivity: "" # low | medium | high
initial_read_tier: 1
max_read_tier: 4
index_known_paths:
  count: 0
  paths: []
  note: "Index-known paths are not content-read files."
memory_to_use:
  pal_project_memory_snapshot: []
  routing_memory_summary: []
  runtime_skill_usage_memory: []
  verification_memory: []
  privacy_notes: []
profiles_to_read:
  runtime_profiles: []
  model_profiles: []
  reasoning_profiles: []
  skill_profiles: []
  plugin_profiles: []
  mcp_profiles: []
  pal_profiles: []
summary_sources:
  - source: ""
    reason: ""
full_content_required:
  - path: ""
    reason: ""
forbidden_context:
  - ""
runtime_skill_candidates:
  - name: ""
    type: ""
    reason: ""
    availability_check_required: true
verification_context:
  required_evidence: []
  verifier_candidates: []
  not_run_reporting_required: true
tier_escalation_rules:
  - from_tier: 1
    to_tier: 2
    reason: ""
  - from_tier: 2
    to_tier: 3
    reason: ""
  - from_tier: 3
    to_tier: 4
    reason: ""
stop_conditions:
  - ""
ask_user_conditions:
  - ""
expected_context_usage_report:
  required: true
  template: templates/orchestration/context-usage-report.md
not_a_token_meter: true
```

## Rules

- `full_content_required` must include a reason for each file.
- `forbidden_context` supports privacy and relevance.
- Higher tiers cost more context; use low-to-high unless risk justifies jumping.
- Verification context must not be removed merely to reduce cost.
- Runtime Skill candidates are checked by the host Runtime, not by AgentPal.
- This template must not claim exact token or cost numbers.
