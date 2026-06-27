# Routing Decision Record Template

```yaml
schema: agentpal.routing-decision-record.v0.3
record_id:
created_at:
task_summary:
project_id:
task_type:
topology_candidate:
pal_candidates:
  - pal:
    role_candidate:
    reason:
owner_pal_selected:
  pal:
  reason:
verifier_candidates:
  - pal:
    reason:
runtime_candidates:
  - runtime:
    reason:
    current_evidence_required: true
runtime_selected:
  runtime:
  evidence:
model_or_reasoning_candidate:
runtime_skill_candidates:
  - name:
    type:
    reason:
runtime_skills_used:
  - name:
    used:
    evidence:
pal_owned_skills_used:
  - pal:
    skill_or_method:
    purpose:
context_budget:
  context_read_count:
  profile_read_count:
  memory_used:
decision_basis:
  - "<case-specific reason>"
privacy_review:
  public_safe: true
  sensitive_context_excluded: true
not_a_fixed_route: true
```

Use this record as a judgement trace, not as a route table.

`runtime_skill_candidates` and `runtime_skills_used` refer to host Runtime capabilities. `pal_owned_skills_used` refers to Pal methods and output contracts. Keep them separate.

`not_a_fixed_route: true` must remain present. Any next-time lesson is evidence for future AI Judgement, not a rule.
