# Owner + Verifier Task Package

```yaml
schema: agentpal.owner-verifier-package.v0.3
workflow_id:
created_at:
user_goal:
owner_pal_candidate:
verifier_pal_candidate:
runtime_candidates:
owner_stage:
  goal:
  scope:
  constraints:
  allowed_files:
  forbidden_files:
  needed_output:
  acceptance_criteria:
  evidence_required:
verification_context:
  can_read:
    - original_goal_summary
    - owner_final_report
    - evidence_outputs
  cannot_read:
    - private_user_memory
    - unrelated_pal_assets
    - secrets
verifier_stage:
  needed_output: "decision, evidence map, gaps, risk, next action"
  allowed_decisions:
    - pass
    - fail
    - partial
    - not-run
    - blocked
summary_stage:
  summarizer_candidate: Mira
  routing_memory_candidate: true
boundary:
  no_automatic_parallel_execution: true
  verifier_not_final_business_approver: true
  candidates_not_fixed_routes: true
```
