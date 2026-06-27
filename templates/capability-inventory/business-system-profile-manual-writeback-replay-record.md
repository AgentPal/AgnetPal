# Business System Profile Manual Writeback Replay Record

replay_id:

source_evidence_pack_id:

organization_profile_ref:

business_system_id:

manual_writeback_status:

manual_writeback_actor:

manual_writeback_date:

changed_fields_summary:

previous_profile_snapshot_summary:

updated_profile_snapshot_summary:

evidence_used:

user_confirmation_summary:

host_runtime_evidence_summary:

second_verification_status:

second_verification_evidence:

not_run_checks:

missing_evidence:

rollback_record:

risk_notes:

final_decision:

recorded_by:

recorded_at:

forbidden_actions:

- Do not modify central Pal roster.
- Do not write to external project .agentpal/.
- Do not store credentials.
- Do not create connector.
- Do not keyword-route.
- Do not convert not-run into pass.
- Do not hide missing evidence.
- Do not use replay record as an execution engine.

## Status Options

- `manual_writeback_completed`
- `manual_writeback_rejected`
- `manual_writeback_reverted`
- `second_verification_passed`
- `second_verification_failed`
- `second_verification_not_run`
- `second_verification_blocked_missing_evidence`

## Boundary

This replay record audits a manual writeback after it happened. It does not execute writeback, does not automatically rollback, does not update central Pal contacts, does not create a connector or API client, does not store credentials, does not route by keywords, and does not write replay / rollback / verification records into an external project `.agentpal/` directory by default.

If second verification did not run, keep `second_verification_status: second_verification_not_run`.
