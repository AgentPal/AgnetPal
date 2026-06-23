# Routing Reward Memory Example

This is a synthetic public-safe example.

```yaml
schema: agentpal.routing-decision-record.v0.1
record_id: route-example-001
created_at: 2026-01-01
task_summary: release checklist review for a public markdown/json workspace
task_type: release-check
selected:
  pal: selected-quality-owner
  topology: single_owner_with_task_package
  agent_runtime: markdown-json-capable-runtime
  model: unknown
  reasoning_strength: high
  skill_plugin_mcp: []
context_usage:
  index_known_count: 20
  content_read_count: 8
verification_plan: check JSON, no runtime files, no internal path leakage
outcome:
  verification_result: pass
  false_completion_caught: false
  user_accepted: true
  rework_count: 1
next_time_recommendation:
  recommendation: use a release-check owner and explicit evidence table again
  non_binding: true
```

This memory is not a rule. It is evidence for future AI Judgement.

Lesson: routing memory is corrected by results. A stronger model profile would not automatically be selected next time if this bounded quality-check path stayed cheaper, more verifiable, and accepted.
