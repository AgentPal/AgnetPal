# Business System Profile Review Flow

## Purpose

Project usage memory can suggest organization-level review, but cannot update organization truth by itself.

This no-code review flow defines how a project-scoped Business System observation becomes a review packet for possible organization-level profile updates.

The review packet can recommend an update. It is not the update.

## Inputs

- project usage memory
- project capability record
- organization profile ref
- user confirmation
- host Runtime evidence
- missing / not-run / unknown fields

## Required Review Packet Fields

| Field | Meaning |
| --- | --- |
| `review_id` | Stable public-safe review id. |
| `source_project_id` | Project that produced the usage memory or capability observation. |
| `source_project_record_path` | Central project record path or public-safe example path. |
| `organization_profile_ref` | Organization Business System profile or public-safe example being reviewed. |
| `business_system_id` | Business System id from the profile or example. |
| `proposed_change` | Narrow change being proposed for human review. |
| `evidence_summary` | Evidence available now, separated from assumptions. |
| `user_confirmation` | Explicit user confirmation status and source. |
| `host_runtime_evidence` | Current host Runtime evidence, or `not-run` when absent. |
| `unknown_fields` | Fields that remain unknown. |
| `not_run_checks` | Checks that did not run. |
| `missing_evidence` | Evidence required but absent. |
| `risk_notes` | Privacy, permission, external-write, and scope risks. |
| `recommended_status` | Suggested review result. |
| `decision` | Final decision when reviewed. |
| `decision_by` | User, maintainer, Pal, or Runtime evidence source that made the decision. |
| `decision_date` | Decision date or `unknown`. |
| `writeback_plan` | Manual writeback steps if approved. |

## Allowed Outcomes

- `approved_for_manual_update`
- `rejected`
- `blocked_missing_evidence`
- `needs_user_confirmation`
- `needs_runtime_evidence`
- `needs_more_review`

## Forbidden Outcomes

- `auto_update_organization_profile`
- `auto_modify_central_roster`
- `auto_create_connector`
- `store_credentials`
- `keyword_route`
- `write_to_external_project_agentpal`

## Review Rules

- A review packet can suggest a profile update, but it must not modify the profile by itself.
- Organization profile updates require explicit user confirmation.
- Host Runtime evidence must be current, scoped, and reviewable.
- Project usage memory must remain project-scoped until review completes.
- If evidence is absent, keep `unknown`, `not-run`, or `missing`; do not convert them into availability.
- The central Pal roster must not be modified by a Business System profile review.
- No review flow may create a connector, API client, scanner, validator, daemon, background sync job, automatic execution path, or keyword route.
- Review materials must not be written into an external project `.agentpal/` directory by default, including `.agentpal/reviews/`.

## Manual Writeback Boundary

When a review is `approved_for_manual_update`, the writeback plan may propose a manual edit to an organization Business System profile under:

```text
workspace/organization/capability-inventory/
```

That manual edit still needs:

- explicit user approval for the organization-level change
- current evidence or a user-confirmed source
- a privacy and credential check
- preservation of no-keyword-routing policy
- no central roster modification

If any of these are missing, the decision should remain `blocked_missing_evidence`, `needs_user_confirmation`, `needs_runtime_evidence`, or `needs_more_review`.

