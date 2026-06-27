# Plan -> Execute -> Verify Package

```yaml
schema: agentpal.plan-execute-verify-package.v0.3
workflow_id:
created_at:
user_goal:
owner_pal_candidate:
planner_stage:
  goal:
  scope:
  allowed_files:
  forbidden_files:
  constraints:
  acceptance_criteria:
  runtime_candidates:
  evidence_required:
execute_stage:
  executor_type: runtime
  executor_candidate:
  steps:
    - "<bounded execution step>"
  do_not_do:
    - "do not modify unrelated files"
    - "do not create runtime code unless explicitly in scope"
  required_report:
    - affected_paths
    - commands_run
    - outputs
    - failures
    - not_run
verify_stage:
  verifier_candidate:
  can_read:
    - execution_report
    - affected_paths
    - command_outputs
  decision_values:
    - pass
    - fail
    - partial
    - not-run
    - blocked
boundary:
  runtime_is_execution_layer_only: true
  completion_report_is_not_evidence: true
  no_automatic_loop: true
```
