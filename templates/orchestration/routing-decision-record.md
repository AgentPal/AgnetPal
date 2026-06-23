# Routing Decision Record Template

This records why a route was selected and whether it later worked. It is not a route rule.

```yaml
schema: agentpal.routing-decision-record.v0.1
record_id:
created_at:
task_summary:
task_type:
decision_context:
  active_project:
  user_constraints:
  risk_level:
selected:
  pal:
  topology:
  agent_runtime:
  model:
  reasoning_strength:
  skill_plugin_mcp: []
why_selected:
alternatives_considered:
  - candidate:
    reason_not_selected:
context_usage:
  index_known_count:
  content_read_count:
  content_read_files: []
verification_plan:
privacy_review:
outcome:
  verification_result:
  false_completion_caught:
  user_accepted:
  rework_count:
  failure_reason:
next_time_recommendation:
  recommendation:
  non_binding: true
```
