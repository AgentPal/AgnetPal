# Routing Decision Record Template

```yaml
schema: agentpal.routing-decision-record.v0.3
record_id:
created_at:
task_summary:
task_type:
topology_candidate:
owner_pal_candidate:
verifier_pal_candidate:
runtime_candidate:
model_or_reasoning_candidate:
skill_plugin_mcp_candidates:
context_index_known_count:
context_content_read_count:
decision_basis:
  - "<case-specific reason>"
privacy_review:
  public_safe: true
  sensitive_context_excluded: true
not_a_fixed_route: true
```

Use this record as a judgement trace, not as a route table.
