# Business System Profile Change Ledger

## Purpose

A change ledger records manual, human-governed changes to an organization Business System Profile.

It is not a writeback engine.

The ledger records changes that have already happened through manual writeback or that have been explicitly approved for manual update by a human governance decision. It does not create, execute, approve, reject, rollback, verify, or close any change by itself.

The ledger is a no-code governance artifact. It records field-level old/new summaries, source decision records, evidence references, replay records, audit trail indexes, second verification status, rollback references, superseded entries, retained unknowns, retained not-run checks, retained missing evidence, and the next manual review date. It must not automatically change organization truth, modify central contacts, create connectors, store credentials, call external APIs, write into an external project `.agentpal/`, or route by keywords.

## Inputs

- governance decision record
- manual update evidence pack
- manual writeback replay record
- audit trail index
- second verification result
- rollback reference
- current organization profile snapshot summary

## Required Fields

| Field | Meaning |
| --- | --- |
| `ledger_id` | Stable public-safe id for the change ledger. |
| `business_system_id` | Business System id from the organization profile. |
| `organization_profile_ref` | Organization Business System Profile or public-safe example being tracked. |
| `ledger_owner` | Human, maintainer, Pal, or governance reviewer responsible for maintaining the ledger. |
| `entries` | Field-level change entries. |
| `last_reviewed_by` | Human, maintainer, Pal, or reviewer that last reviewed the ledger. |
| `last_reviewed_at` | Last review date or `unknown`. |
| `next_review_date` | Human reminder date for the next review; not an automatic task. |
| `status` | Ledger status. |

## Entry Fields

| Field | Meaning |
| --- | --- |
| `entry_id` | Stable public-safe id for one field-level change entry. |
| `decision_ref` | Governance decision record that approved, blocked, or explained the change. |
| `evidence_pack_ref` | Manual update evidence pack used for the change. |
| `replay_record_ref` | Manual writeback replay record for the completed change, if it happened. |
| `audit_trail_ref` | Audit trail index connecting related review, evidence, replay, rollback, and verification records. |
| `changed_fields` | Fields changed or proposed for manual update. |
| `old_value_summary` | Public-safe summary of previous value; use `unknown` when not evidenced. |
| `new_value_summary` | Public-safe summary of new value; do not store secrets or private identifiers. |
| `change_reason` | Evidence-based reason for the change. |
| `manual_update_scope` | Exact field/path scope allowed or recorded for the manual update. |
| `second_verification_status` | Verification status such as `second_verification_not_run`, `needs_second_verification`, `passed`, `failed`, or `blocked`. |
| `second_verification_ref` | Reference to second verification evidence, or `missing`. |
| `rollback_ref` | Rollback note or replay record rollback reference. |
| `supersedes_entry` | Prior ledger entry superseded by this entry, or `none`. |
| `unknowns_retained` | Facts that remain unknown and must not be invented. |
| `not_run_checks_retained` | Checks that did not run and must not be reported as pass. |
| `missing_evidence_retained` | Evidence still missing after the change record. |
| `risk_notes` | Privacy, permission, credential, routing, external-write, and scope risks. |
| `recorded_by` | Person, Pal, or host Runtime summary that recorded the entry. |
| `recorded_at` | Entry creation date or `unknown`. |

## Allowed Statuses

- `active`
- `archived`
- `needs_review`
- `blocked_missing_evidence`
- `superseded`

## Forbidden Behavior

- `auto_update_organization_profile`
- `auto_modify_central_roster`
- `auto_call_external_api`
- `auto_close_missing_evidence`
- `convert_not_run_to_pass`
- `store_credentials`
- `keyword_route`
- `write_to_external_project_agentpal`

## Change Boundary

Change Ledgers record manual changes. They do not execute changes.

If a field was updated manually, the ledger can record the already-completed update with references to the decision, evidence, replay record, audit trail, second verification result, and rollback note.

If a field was only approved for future manual update, the ledger must say so and must not imply that the organization profile has already changed.

The ledger itself does not automatically change organization truth. Organization Business System Profile truth changes only through explicit human-governed manual updates with reviewable evidence.

## Field Summary Boundary

`old_value_summary` and `new_value_summary` are summaries only. They must not contain real credentials, private tokens, passwords, API keys, cookies, integration secrets, private workspace ids, private customer exports, session values, or sensitive identifiers.

Do not convert:

- `unknown` to available without decision and evidence
- `not-run` to pass
- missing evidence to complete
- user confirmation missing to approved
- indirect project usage memory to organization truth

## Evidence Boundary

Unknowns, missing evidence, and not-run checks must remain visible in each entry until reviewable evidence exists.

If second verification did not run, record `second_verification_not_run` or `needs_second_verification`. Do not report second verification as passed without current host Runtime evidence.

If evidence remains missing, keep it in `missing_evidence_retained`. Do not hide it because a ledger entry exists.

## Organization Profile Boundary

Change Ledgers may reference organization-level Business System Profiles under:

```text
workspace/organization/capability-inventory/business-systems/
```

They must not update:

```text
workspace/organization/contacts/pals.json
workspace/organization/contacts/PAL_CONTACTS.md
external-project/.agentpal/
```

Business System Profile change ledgers cannot change Pal roster, Pal replacement, Pal activation, or routing policy.

## Next Review Boundary

`next_review_date` is a human reminder and governance planning note. It is not a scheduled automation, background task, daemon, calendar item, monitor, scanner, validator, connector, or auto-review trigger.

## External Project Boundary

External user projects remain thin-bound. Do not write change ledgers into external project `.agentpal/change-ledger/`, `.agentpal/governance-decisions/`, `.agentpal/audit-trail/`, `.agentpal/replay/`, `.agentpal/rollback/`, `.agentpal/verification/`, `.agentpal/evidence/`, `.agentpal/reviews/`, `.agentpal/business-systems/`, `.agentpal/capability-inventory/`, `.agentpal/memory/`, `.agentpal/reports/`, or `.agentpal/state/` by default.

Organization-level change ledgers belong in the AgentPal Workspace when explicitly maintained, not in the external project binding directory.

## Routing Boundary

Business System Profiles, Review Packets, Evidence Packs, Replay Records, Audit Trail Indexes, Governance Decision Records, and Change Ledgers are AI judgement inputs only. They must not become:

- `keyword_map`
- `domain_map`
- `role_map`
- deterministic task-to-Pal routing
- deterministic task-to-runtime routing
- deterministic system-type-to-tool routing

Explicit `/pal Name` or `@Name` remains user intent, not keyword routing.
