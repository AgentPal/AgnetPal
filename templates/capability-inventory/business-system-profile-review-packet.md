# Business System Profile Review Packet

review_id:

source_project_id:

source_project_record_path:

organization_profile_ref:

business_system_id:

review_reason:

proposed_change:

evidence_summary:

user_confirmation:

host_runtime_evidence:

unknown_fields:

not_run_checks:

missing_evidence:

risk_notes:

recommended_status:

decision:

decision_by:

decision_date:

writeback_plan:

forbidden_writebacks:

- Do not modify central Pal roster.
- Do not write to external project `.agentpal/`.
- Do not store credentials.
- Do not create connector.
- Do not keyword-route.

## Status Options

- `approved_for_manual_update`
- `rejected`
- `blocked_missing_evidence`
- `needs_user_confirmation`
- `needs_runtime_evidence`
- `needs_more_review`

## Boundary

This packet is a no-code review artifact. It can recommend an organization Business System profile update, but it must not automatically update organization truth, modify `workspace/organization/contacts/pals.json`, create external system connectors, store credentials, or write review records into an external project `.agentpal/` directory by default.

