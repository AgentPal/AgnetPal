# Business System Profile Governance Decision Record

decision_id:

business_system_id:

organization_profile_ref:

source_audit_trail_ref:

source_review_refs:

source_evidence_pack_refs:

source_replay_record_refs:

decision:

decision_reason:

decision_by:

decision_date:

evidence_considered:

unknowns_retained:

not_run_checks_retained:

missing_evidence_retained:

second_verification_requirement:

manual_update_allowed:

manual_update_scope:

writeback_target:

rollback_requirement:

follow_up_actions:

risk_notes:

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
- Do not use this record as an execution engine.

## Decision Options

- `approved_for_manual_profile_update`
- `rejected`
- `blocked_missing_evidence`
- `needs_user_confirmation`
- `needs_host_runtime_evidence`
- `needs_second_verification`
- `superseded_by_later_decision`

## Boundary

This governance decision record records a human governance decision after review, evidence pack, replay record, and audit trail review. It does not execute actions, does not automatically update organization profiles, does not automatically close missing evidence, does not update central Pal contacts, does not create a connector or API client, does not store credentials, does not route by keywords, and does not write governance decision records into an external project `.agentpal/` directory by default.

If `manual_update_allowed` is true, keep `manual_update_scope` narrow and explicit. If second verification did not run, keep it as `not-run`. If evidence is missing, keep it as `missing`.
