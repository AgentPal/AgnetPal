# Context Budget Plan

Use this template before a conductor-shaped task or any task where context bloat, cost, or verification tradeoffs matter.

```yaml
schema: agentpal.context_budget_plan.v0.1
task_id: example-task-id
user_goal: ""
budget_intent:
  priority: "" # speed | cost | verification | balanced
  reason: ""
index_only_sources:
  - path: ""
    reason: ""
full_text_sources:
  - path: ""
    reason: ""
summarize_first_sources:
  - path: ""
    reason: ""
memory_sources:
  - source: ""
    reason: ""
    freshness_or_risk_note: ""
capability_profiles_to_read:
  - path: ""
    profile_type: "" # Runtime | Model | Reasoning | Skill | Plugin | MCP | Pal
    reason: ""
runtime_skill_candidates_to_check:
  - name: ""
    reason: ""
model_or_reasoning_suggestion:
  model_candidate: ""
  reasoning_candidate: ""
  reason: ""
verification_must_not_skip:
  - ""
counts_to_report:
  context_read_count: 0
  profile_read_count: 0
  memory_used: false
not_run_reporting_rule: "Any skipped evidence check must be reported as not-run with reason."
```
