# Notion Read Access Manual Writeback Replay Example

## Example Scope

- replay_id: `replay-content-ops-notion-read-access-example`
- source_evidence_pack: `notion-read-access-manual-update-evidence.example.md`
- source_evidence_pack_id: `evidence-content-ops-notion-read-access-example`
- manual_writeback_status: `manual_writeback_completed`
- organization_profile_ref: `examples/capability-inventory/business-system-profiles/notion-public-governance-profile.example.json`
- business_system_id: `notion-public-governance-example`
- example_only: true

## Replay Premise

This public-safe example assumes a manual writeback has already happened in an approved example scenario.

The replay record does not perform the writeback. It only records what the manual writeback claimed to change and what verification still says.

## Changed Field Summary

```text
read_access: unknown -> user_confirmed
```

No other access field changes are implied.

## Previous Profile Snapshot Summary

- read access: `unknown`
- write access: `unknown`
- API access: `unknown`
- integration status: `unknown`
- real workspace id: none
- real page id: none
- real database id: none
- token: none
- connector: none

## Updated Profile Snapshot Summary

- read access: `user_confirmed` by example user confirmation
- write access: `unknown`
- API access: `unknown`
- integration status: `unknown`
- export permission: `unknown`
- admin permission: `unknown`
- real workspace id: none
- real page id: none
- real database id: none
- token: none
- connector: none

## Evidence Used

- source evidence pack: `notion-read-access-manual-update-evidence.example.md`
- user confirmation: example placeholder, not a real user confirmation
- host Runtime evidence: example placeholder, not a real Runtime result
- credential evidence: none stored
- connector evidence: none created

## Second Verification Result

```text
second_verification_status: second_verification_not_run
```

This safer example keeps second verification as not-run. It does not claim pass because no real manual writeback or real host Runtime verification was executed.

## Not-Run Checks

- second verification: not-run
- Notion workspace access check: not-run
- Notion page read check: not-run
- Notion database visibility check: not-run
- central roster diff check in a real repository: not-run for this example
- external project `.agentpal/replay/` check in a real project: not-run for this example

## Missing Evidence

- real user confirmation
- real host Runtime evidence
- actual organization profile diff
- actual second verification report
- screenshot or UI confirmation
- exported report or documented admin setting

## Rollback Record

rollback_status: `rollback_not_run`

rollback_target:

```text
workspace/organization/capability-inventory/business-systems/
```

rollback_steps:

1. Re-open the previous profile snapshot summary.
2. Restore `read_access` from `user_confirmed` to `unknown` if the manual writeback is rejected, over-scoped, or unsupported by evidence.
3. Confirm write access, API access, integration status, export permission, and admin permission remain `unknown`.
4. Confirm no central Pal roster file changed.
5. Confirm no external project `.agentpal/replay/`, `.agentpal/rollback/`, or `.agentpal/verification/` directory was created.
6. Record rollback verification honestly as pass, failed, blocked, or not-run.

rollback_verification: `not-run`

This rollback record is explanatory only. It does not automatically modify files or call Git, Notion, CRM, GitHub, Feishu, or any other API.

## Final Decision

```text
final_decision: replay_recorded_with_second_verification_not_run
recorded_by: example
recorded_at: unknown
```

The replay is recorded as an example audit artifact. It does not certify real Notion read access and does not update any organization profile.

## Forbidden

- no automatic writeback
- no automatic rollback
- no Notion connector
- no Notion API client
- no token
- no password
- no API key
- no cookie
- no integration secret
- no private workspace id, page id, or database id
- no central roster change
- no external project `.agentpal/replay/`
- no external project `.agentpal/rollback/`
- no external project `.agentpal/verification/`
- no external project `.agentpal/evidence/`
- no keyword routing
- no hidden missing evidence
- no not-run to pass conversion
