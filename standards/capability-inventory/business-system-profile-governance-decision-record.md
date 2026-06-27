# Business System Profile Governance Decision Record

## Purpose

A governance decision record captures a human governance decision after review, evidence pack, replay record, and audit trail review.

It is not an approval engine and not an execution system.

The record is a no-code governance artifact. It records who approved, rejected, blocked, or superseded a proposed organization Business System Profile state change, which evidence was considered, which unknowns remain, which checks did not run, which evidence is still missing, and what manual follow-up may be considered. It must not execute writeback, automatically approve or reject reviews, automatically close missing evidence, modify central contacts, create connectors, store credentials, write into external project `.agentpal/`, or route by keywords.

## Inputs

- audit trail index
- review packet
- manual update evidence pack
- manual writeback replay record
- second verification result
- user confirmation
- host Runtime evidence
- risk notes
- open unknowns
- missing evidence

## Required Fields

| Field | Meaning |
| --- | --- |
| `decision_id` | Stable public-safe decision record id. |
| `business_system_id` | Business System id from the organization profile. |
| `organization_profile_ref` | Organization Business System Profile or public-safe example being governed. |
| `source_audit_trail_ref` | Audit trail index used for this decision. |
| `source_review_refs` | Review packet refs considered. |
| `source_evidence_pack_refs` | Manual update evidence pack refs considered. |
| `source_replay_record_refs` | Manual writeback replay record refs considered. |
| `decision` | Human governance decision status. |
| `decision_reason` | Short evidence-based reason for the decision. |
| `decision_by` | Human, maintainer, or governance reviewer responsible for the decision. |
| `decision_date` | Decision date or `unknown`. |
| `evidence_considered` | Evidence records, summaries, and host Runtime evidence considered. |
| `unknowns_retained` | Facts that remain unknown and must not be invented. |
| `not_run_checks_retained` | Checks that did not run and must not be reported as pass. |
| `missing_evidence_retained` | Required evidence that remains missing. |
| `second_verification_requirement` | Whether second verification is required, completed, blocked, failed, or not-run. |
| `manual_update_allowed` | Whether a bounded manual organization profile update is allowed by this decision. |
| `manual_update_scope` | Exact fields or paths allowed for a manual update, if any. |
| `writeback_target` | Organization-level target for an approved manual update, or `none`. |
| `rollback_requirement` | Rollback note or requirement that must exist before or after manual update. |
| `follow_up_actions` | Suggested human actions only; not automatic execution. |
| `risk_notes` | Privacy, permission, credential, routing, external-write, and scope risks. |
| `recorded_by` | Person, Pal, or host Runtime summary that recorded the decision. |
| `recorded_at` | Record creation date or `unknown`. |

## Allowed Decisions

- `approved_for_manual_profile_update`
- `rejected`
- `blocked_missing_evidence`
- `needs_user_confirmation`
- `needs_host_runtime_evidence`
- `needs_second_verification`
- `superseded_by_later_decision`

## Forbidden Behavior

- `auto_update_organization_profile`
- `auto_modify_central_roster`
- `auto_close_missing_evidence`
- `convert_not_run_to_pass`
- `auto_create_connector`
- `store_credentials`
- `keyword_route`
- `write_to_external_project_agentpal`

## Decision Boundary

Governance Decision Records record human governance decisions. They do not execute.

They may allow a bounded manual organization profile update, but they do not perform that update. If `manual_update_allowed` is true, `manual_update_scope` must be narrow and explicit, `writeback_target` must be an organization-level target, and required rollback or second verification notes must remain visible.

If `manual_update_allowed` is false, the decision record must not be treated as permission to write profile fields, modify central contacts, call external systems, or close missing evidence.

## Evidence Boundary

Unknown, missing, and not-run states must be retained.

Do not convert:

- `unknown` to available
- `not-run` to pass
- missing evidence to complete
- user confirmation missing to approved
- indirect evidence to organization truth

If second verification is required and has not run, use `needs_second_verification` or another blocked status. Do not approve manual profile updates while second verification evidence is missing unless the decision explicitly records a narrow exception and the unresolved risk.

## Organization Profile Boundary

Governance Decision Records may reference organization-level Business System Profiles under:

```text
workspace/organization/capability-inventory/business-systems/
```

They must not update:

```text
workspace/organization/contacts/pals.json
workspace/organization/contacts/PAL_CONTACTS.md
external-project/.agentpal/
```

Business System Profile governance cannot change Pal roster, Pal replacement, Pal activation, or routing policy.

## Credential Boundary

Governance Decision Records must not store real credentials, private tokens, passwords, API keys, cookies, integration secrets, private workspace ids, customer exports, or session values.

If the decision depends on authenticated host Runtime evidence, record only a public-safe summary or path reference. Do not paste credential values.

## External Project Boundary

External user projects remain thin-bound. Do not write governance decision records into external project `.agentpal/governance-decisions/`, `.agentpal/audit-trail/`, `.agentpal/replay/`, `.agentpal/rollback/`, `.agentpal/verification/`, `.agentpal/evidence/`, `.agentpal/reviews/`, `.agentpal/business-systems/`, `.agentpal/capability-inventory/`, `.agentpal/memory/`, `.agentpal/reports/`, or `.agentpal/state/` by default.

Organization-level governance decisions belong in the AgentPal Workspace when explicitly maintained, not in the external project binding directory.

## Routing Boundary

Business System Profiles, Review Packets, Evidence Packs, Replay Records, Audit Trail Indexes, and Governance Decision Records are AI judgement inputs only. They must not become:

- `keyword_map`
- `domain_map`
- `role_map`
- deterministic task-to-Pal routing
- deterministic task-to-runtime routing
- deterministic system-type-to-tool routing

Explicit `/pal Name` or `@Name` remains user intent, not keyword routing.
