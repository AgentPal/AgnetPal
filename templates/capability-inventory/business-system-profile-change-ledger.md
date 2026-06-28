# Business System Profile Change Ledger

ledger_id:

business_system_id:

organization_profile_ref:

ledger_owner:

entries:

last_reviewed_by:

last_reviewed_at:

next_review_date:

status:

## Entry template

entry_id:

decision_ref:

evidence_pack_ref:

replay_record_ref:

audit_trail_ref:

changed_fields:

old_value_summary:

new_value_summary:

change_reason:

manual_update_scope:

second_verification_status:

second_verification_ref:

rollback_ref:

supersedes_entry:

unknowns_retained:

not_run_checks_retained:

missing_evidence_retained:

risk_notes:

recorded_by:

recorded_at:

forbidden_actions:

- Do not modify central Pal roster.
- Do not write to external project .agentpal/.
- Do not store credentials.
- Do not create connector.
- Do not keyword-route.
- Do not auto-call external APIs.
- Do not convert not-run into pass.
- Do not hide missing evidence.
- Do not use this ledger as a writeback engine.

## Status Options

- `active`
- `archived`
- `needs_review`
- `blocked_missing_evidence`
- `superseded`

## Boundary

This change ledger records manual, human-governed changes to an organization Business System Profile. It does not execute writeback, does not automatically update organization profiles, does not automatically rollback, does not automatically close missing evidence, does not update central Pal contacts, does not call external APIs, does not create a connector or API client, does not store credentials, does not route by keywords, and does not write change ledger records into an external project `.agentpal/` directory by default.

`old_value_summary` and `new_value_summary` are public-safe summaries only. If second verification did not run, keep it as `not-run`. If evidence is missing, keep it as `missing`. `next_review_date` is a human reminder, not an automatic task.
