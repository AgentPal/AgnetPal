# Owner + Verifier Task Package

Use this template when one Pal owns the work and another Pal candidate independently checks evidence.

```yaml
schema: agentpal.owner-verifier-package.v0.3
workflow_id:
created_at:
user_goal:
workflow_boundary:
  no_code_staged_workflow: true
  no_automatic_background_agents: true
  no_automatic_parallel_runtimes: true
  runtime_is_execution_layer_only: true
  candidates_not_fixed_routes: true

owner_task:
  owner_pal_candidate:
  owner_fit_reason:
  task_summary:
  expected_deliverables:
    - <deliverable>
  acceptance_criteria:
    - <criterion>
  constraints:
    - <constraint>
  allowed_files:
    - <path-or-pattern>
  forbidden_files:
    - <path-or-pattern>
  owner_needed_output:
    - plan
    - task_package
    - completion_claim
    - evidence_inventory
  evidence_required_for_verification:
    - <evidence-source>

verifier_task:
  verifier_pal_candidate:
  verifier_fit_reason:
  verification_mode: review | release_gate | acceptance_check | evidence_audit
  verifier_must_not_rely_only_on_owner_claim: true
  allowed_verdicts:
    - pass
    - fail
    - blocked
  verifier_needed_output:
    - verdict
    - checked_evidence
    - missing_evidence
    - risks
    - required_repairs
    - confidence

context_packet:
  template: templates/orchestration/verifier-context-packet.md
  packet_id:
  evidence_to_check:
    - <evidence-source>
  cannot_read:
    - private_user_memory
    - unrelated_pal_assets
    - secrets
    - full_chat_history_by_default

verification_result:
  template: templates/orchestration/verification-result-record.md
  verification_id:
  expected_verdict_format: pass | fail | blocked

synthesis:
  summarizer_candidate: Mira | owner_pal_candidate
  must_preserve_verifier_verdict: true
  required_summary:
    - owner_claim
    - verifier_verdict
    - checked_evidence
    - missing_evidence
    - risks
    - recommended_next_step

repair_package:
  create_if_verdict:
    - fail
    - blocked
  required_fields:
    - repair_goal
    - missing_or_failed_criteria
    - evidence_needed
    - owner_candidate_for_repair
    - return_to_verifier_candidate
```
