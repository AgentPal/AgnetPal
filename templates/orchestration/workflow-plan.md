# Workflow Plan Template

This template describes a planned workflow. In AgentPal v0.1.0-rc.1, only Fast Route, Single Owner, and Task Package are active. Other topologies are future design unless the user manually asks for a written plan.

```yaml
schema: agentpal.workflow-plan.v0.1
workflow_id:
created_at:
task_goal:
topology:
  selected:
  status: active-v0.1 | future-design-only | manual-plan-only
  reason:
owner:
  pal_id:
  output_contract:
steps:
  - step_id:
    recipient_type: pal | runtime | skill | plugin | mcp | verifier | secretary-summary
    recipient_id:
    task:
    input_summary:
    context_access_list:
    output_expected:
    verification_required: false
isolation:
  independent_judgement: false
  drafts_hidden_until_summary: true
verification:
  evidence_required:
  failure_conditions:
routing_memory:
  write_candidate: false
  privacy_review_required: true
do_not_do:
```
