# Business System Profile Manual Update Evidence Pack

evidence_pack_id:

source_review_id:

organization_profile_ref:

business_system_id:

current_profile_snapshot_summary:

approved_change_summary:

evidence_summary:

user_confirmation_summary:

host_runtime_evidence_summary:

manual_writeback_target:

manual_writeback_steps:

rollback_note:

second_verification_checklist:

second_verification_status:

not_run_checks:

missing_evidence:

risk_notes:

decision:

decision_by:

decision_date:

forbidden_writebacks:

- Do not modify central Pal roster.
- Do not write to external project .agentpal/.
- Do not store credentials.
- Do not create connector.
- Do not keyword-route.
- Do not convert not-run into pass.
- Do not hide missing evidence.

## Decision Options

- `ready_for_manual_writeback`
- `blocked_missing_evidence`
- `blocked_missing_user_confirmation`
- `manual_writeback_completed`
- `manual_writeback_rejected`
- `second_verification_passed`
- `second_verification_failed`
- `second_verification_not_run`

## Boundary

This evidence pack follows an approved Business System Profile review packet. It can prepare a manual organization profile writeback, but it must not perform automatic writeback, update central Pal contacts, create a connector or API client, store credentials, route by keywords, or write evidence records into an external project `.agentpal/` directory by default.

Second verification must be recorded after manual writeback. If it did not run, keep `second_verification_status: second_verification_not_run`.
