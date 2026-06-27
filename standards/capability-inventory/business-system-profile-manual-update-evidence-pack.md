# Business System Profile Manual Update Evidence Pack

## Purpose

An approved Business System Profile review packet can lead to a manual evidence pack, but not automatic writeback.

The evidence pack is a no-code audit artifact for a proposed organization-level Business System Profile update. It records the approved change, evidence, user confirmation, host Runtime evidence, rollback note, manual writeback instructions, and second verification requirements before any organization profile is edited.

## Inputs

- approved review packet
- current organization profile
- project usage memory
- user confirmation
- host Runtime evidence
- risk notes

## Required Fields

| Field | Meaning |
| --- | --- |
| `evidence_pack_id` | Stable public-safe evidence pack id. |
| `source_review_id` | Approved review packet that this evidence pack follows. |
| `organization_profile_ref` | Organization Business System Profile being considered for manual update. |
| `business_system_id` | Business System id from the profile. |
| `current_profile_snapshot_summary` | Short summary of the profile state before manual update. |
| `approved_change_summary` | Narrow change approved for possible manual writeback. |
| `evidence_summary` | Evidence available now, separated from assumptions. |
| `user_confirmation_summary` | User confirmation status, source, and scope. |
| `host_runtime_evidence_summary` | Current host Runtime evidence, or `not-run` when absent. |
| `manual_writeback_target` | Organization profile path under `workspace/organization/capability-inventory/business-systems/`. |
| `manual_writeback_steps` | Human-readable steps for the host Runtime or maintainer after explicit approval. |
| `rollback_note` | How to restore the previous profile state if the manual update is rejected or fails. |
| `second_verification_checklist` | Checks required after manual writeback. |
| `second_verification_status` | Current second verification result. |
| `not_run_checks` | Checks that did not run and must not be reported as pass. |
| `missing_evidence` | Evidence required but absent. |
| `risk_notes` | Privacy, permission, credential, external-write, and scope risks. |
| `decision` | Current evidence pack decision. |
| `decision_by` | User, maintainer, Pal, or Runtime evidence source that made the decision. |
| `decision_date` | Decision date or `unknown`. |

## Allowed Outcomes

- `ready_for_manual_writeback`
- `blocked_missing_evidence`
- `blocked_missing_user_confirmation`
- `manual_writeback_completed`
- `manual_writeback_rejected`
- `second_verification_passed`
- `second_verification_failed`
- `second_verification_not_run`

## Forbidden Outcomes

- `auto_writeback_organization_profile`
- `auto_modify_central_roster`
- `auto_create_connector`
- `store_credentials`
- `keyword_route`
- `write_to_external_project_agentpal`
- `hide_missing_evidence`
- `convert_not_run_to_pass`

## Relationship To Review Flow

The evidence pack follows an approved review packet. It does not replace approval and does not create approval by itself.

A review packet with `approved_for_manual_update` means the proposed change may be prepared for manual writeback. It does not mean the organization profile has already changed.

If the source review is not approved, the evidence pack decision must be `blocked_missing_evidence`, `blocked_missing_user_confirmation`, or another blocked state.

## Manual Writeback Boundary

Manual writeback can target only an organization-level Business System Profile under:

```text
workspace/organization/capability-inventory/business-systems/
```

Manual writeback must not update:

```text
workspace/organization/contacts/pals.json
workspace/organization/contacts/PAL_CONTACTS.md
external-project/.agentpal/
```

The evidence pack must not create a connector, API client, scanner, validator, daemon, background sync job, automatic execution path, or keyword route.

## Credential Boundary

The evidence pack must not store real credentials, private tokens, passwords, API keys, cookies, integration secrets, private workspace ids, customer data exports, or session values.

If host Runtime evidence depends on authentication, record only a public-safe summary such as `runtime_reported_access_without_secret_value`. Do not paste the secret.

## Relationship To Rollback

The evidence pack must include a rollback note before manual update.

The rollback note should describe how to restore the previous profile snapshot summary or revert the specific manual profile edit. Missing rollback information blocks writeback.

## Relationship To Second Verification

The evidence pack must record second verification status.

Second verification runs after manual writeback. It checks that the intended profile changed, forbidden files did not change, no credential leaked, no connector appeared, no keyword route appeared, and not-run / missing states were preserved honestly.

`not-run` is not pass. Missing evidence is not completion.

If second verification was not executed, use:

```text
second_verification_status: second_verification_not_run
```

Do not convert `second_verification_not_run` into `second_verification_passed`.

## External Project Boundary

External user projects remain thin-bound. Do not write evidence packs into external project `.agentpal/evidence/`, `.agentpal/reviews/`, `.agentpal/business-systems/`, `.agentpal/capability-inventory/`, `.agentpal/memory/`, `.agentpal/reports/`, or `.agentpal/state/` by default.

Project-specific evidence belongs under the central project record. Organization-level evidence packs belong in the AgentPal Workspace when explicitly maintained, not in the external project binding directory.

## Routing Boundary

Business System Profiles, review packets, and evidence packs are AI judgement inputs only. They must not become:

- `keyword_map`
- `domain_map`
- `role_map`
- deterministic task-to-Pal routing
- deterministic task-to-runtime routing
- deterministic system-type-to-tool routing

Explicit `/pal Name` or `@Name` remains user intent, not keyword routing.
