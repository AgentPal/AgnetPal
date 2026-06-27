# Business System Profile Manual Writeback Replay Record

## Purpose

A replay record audits a manual writeback after it has happened.

It is not a writeback engine.

The replay record is a no-code audit artifact. It records what changed, which evidence was used, who performed or confirmed the manual writeback, how rollback would work, and how second verification was recorded. It must not execute writeback, rollback, API calls, connector setup, credential discovery, external project writes, or central roster changes.

## Inputs

- manual update evidence pack
- previous profile snapshot summary
- updated profile snapshot summary
- manual writeback actor
- user confirmation
- host Runtime evidence
- second verification result
- rollback note

## Required Fields

| Field | Meaning |
| --- | --- |
| `replay_id` | Stable public-safe replay record id. |
| `source_evidence_pack_id` | Manual update evidence pack that authorized preparation for manual writeback. |
| `organization_profile_ref` | Organization Business System Profile that was manually updated or considered. |
| `business_system_id` | Business System id from the profile. |
| `manual_writeback_status` | Manual writeback result. |
| `manual_writeback_actor` | User, maintainer, or host Runtime summary for the manual action. |
| `manual_writeback_date` | Date of manual writeback or `unknown`. |
| `changed_fields_summary` | Narrow summary of changed fields. |
| `previous_profile_snapshot_summary` | Public-safe summary of state before manual writeback. |
| `updated_profile_snapshot_summary` | Public-safe summary of state after manual writeback. |
| `evidence_used` | Evidence relied on during manual writeback. |
| `user_confirmation_summary` | User confirmation status, scope, and source. |
| `host_runtime_evidence_summary` | Host Runtime evidence summary, or `not-run` when absent. |
| `second_verification_status` | Honest second verification status. |
| `second_verification_evidence` | Evidence used for second verification, or `missing` / `not-run`. |
| `not_run_checks` | Checks that did not run and must not be reported as pass. |
| `missing_evidence` | Required evidence that is still absent. |
| `rollback_record` | Rollback target, steps, owner, status, and verification summary. |
| `risk_notes` | Privacy, permission, credential, routing, external-write, and scope risks. |
| `final_decision` | Final audit decision for this replay record. |
| `recorded_by` | Person, Pal, or host Runtime summary that recorded the audit. |
| `recorded_at` | Record date or `unknown`. |

## Allowed Statuses

- `manual_writeback_completed`
- `manual_writeback_rejected`
- `manual_writeback_reverted`
- `second_verification_passed`
- `second_verification_failed`
- `second_verification_not_run`
- `second_verification_blocked_missing_evidence`

## Forbidden Behavior

- `auto_writeback_organization_profile`
- `auto_rollback`
- `auto_modify_central_roster`
- `auto_create_connector`
- `store_credentials`
- `keyword_route`
- `write_to_external_project_agentpal`
- `hide_missing_evidence`
- `convert_not_run_to_pass`

## Replay Record Boundary

Replay Record only audits. It does not execute.

It may say that a manual writeback was completed if that fact is supported by evidence, but it must not perform the writeback itself and must not imply that recording the replay changed the organization profile.

## Rollback Record Boundary

Rollback Record only explains. It is not an automatic rollback program.

It can record:

- previous snapshot summary
- rollback target
- rollback steps
- rollback owner
- rollback verification
- rollback status

It must not automatically modify files, automatically call Git, Notion, CRM, GitHub, Feishu, or any other API, modify external project `.agentpal/`, or modify central roster.

## Second Verification Boundary

Second verification must be recorded honestly.

Allowed second verification statuses:

- `second_verification_passed`
- `second_verification_failed`
- `second_verification_not_run`
- `second_verification_blocked_missing_evidence`

`not-run` is not pass. Missing evidence is not complete.

Do not say `verified`, `complete`, or `passed` when the required evidence is absent, indirect, stale, or not inspected.

## Organization Profile Boundary

Replay records may reference organization-level Business System Profiles under:

```text
workspace/organization/capability-inventory/business-systems/
```

The replay record must not update:

```text
workspace/organization/contacts/pals.json
workspace/organization/contacts/PAL_CONTACTS.md
external-project/.agentpal/
```

## Credential Boundary

Replay records must not store real credentials, private tokens, passwords, API keys, cookies, integration secrets, private workspace ids, customer exports, or session values.

If host Runtime evidence depended on authentication, record only a public-safe evidence summary without credential values.

## External Project Boundary

External user projects remain thin-bound. Do not write replay records, rollback records, or verification records into external project `.agentpal/replay/`, `.agentpal/rollback/`, `.agentpal/verification/`, `.agentpal/evidence/`, `.agentpal/reviews/`, `.agentpal/business-systems/`, `.agentpal/capability-inventory/`, `.agentpal/memory/`, `.agentpal/reports/`, or `.agentpal/state/` by default.

## Routing Boundary

Business System Profiles, Review Packets, Evidence Packs, and Replay Records are AI judgement inputs only. They must not become:

- `keyword_map`
- `domain_map`
- `role_map`
- deterministic task-to-Pal routing
- deterministic task-to-runtime routing
- deterministic system-type-to-tool routing

Explicit `/pal Name` or `@Name` remains user intent, not keyword routing.
