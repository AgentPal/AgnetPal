# Notion Read Access Governance Decision Example

This is a public-safe example. It does not modify an organization profile, create a Notion connector, store credentials, call Notion APIs, update the central Pal roster, write into an external project `.agentpal/governance-decisions/`, or route by keywords.

## Decision Record

decision_id: `governance-decision-content-ops-demo-notion-read-access-001`

business_system_id: `notion-public-governance`

business_system: Notion public governance profile

organization_profile_ref: `examples/capability-inventory/business-system-profiles/notion-public-governance-profile.example.json`

source_audit_trail_ref: `examples/capability-inventory/business-system-profile-reviews/notion-read-access-audit-trail-index.example.md`

source_review_refs:

- `examples/capability-inventory/business-system-profile-reviews/notion-read-access-review.example.md`

source_evidence_pack_refs:

- `examples/capability-inventory/business-system-profile-reviews/notion-read-access-manual-update-evidence.example.md`

source_replay_record_refs:

- `examples/capability-inventory/business-system-profile-reviews/notion-read-access-manual-writeback-replay.example.md`

decision: `needs_second_verification`

decision_reason: Read access may be user-confirmed in the public-safe premise, but second verification evidence is still missing.

decision_by: `example-governance-reviewer`

decision_date: `2026-06-28`

recorded_by: `example-maintainer`

recorded_at: `2026-06-28`

## Evidence Considered

- review packet: `notion-read-access-review.example.md`
- manual update evidence pack: `notion-read-access-manual-update-evidence.example.md`
- replay record: `notion-read-access-manual-writeback-replay.example.md`
- audit trail index: `notion-read-access-audit-trail-index.example.md`

## Unknowns Retained

- write access
- API access
- workspace admin role

## Not-run Checks Retained

- second verification
- real Notion UI inspection
- real Notion API inspection
- rollback execution
- rollback verification

## Missing Evidence Retained

- second verification evidence
- current host Runtime evidence for a real workspace
- user-approved proof of current real Notion read access
- proof that write access remains unavailable or unknown in a real workspace
- proof that API access remains unavailable or unknown in a real workspace

## Second Verification Requirement

second_verification_requirement: `required_not_run`

second_verification_status: `second_verification_not_run`

second_verification_evidence: `missing`

The decision remains `needs_second_verification` until a user-approved host Runtime check provides reviewable evidence.

## Manual Update Allowance

manual_update_allowed: false

manual_update_scope: none until second verification is completed

writeback_target: none

rollback_requirement: keep rollback note from `notion-read-access-manual-writeback-replay.example.md`; no automatic rollback

## Follow-up Actions

These are suggestions only:

1. Ask the user whether to run second verification through the host Runtime.
2. If the user approves, request host Runtime evidence without collecting tokens or secrets.
3. Keep `second_verification_not_run` until the check actually runs.
4. Keep missing evidence open until reviewable evidence exists.
5. Reopen governance review after second verification evidence is available.

## Forbidden Actions

- no automatic profile update
- no central roster change
- no external project `.agentpal/governance-decisions/`
- no Notion connector
- no Notion API client
- no token / secret / password / cookie / API key
- no real workspace id
- no real page id
- no real database id
- no keyword routing

## Boundary

This governance decision record records a human governance decision. It does not execute writeback, call Notion, create a connector, store credentials, update central contacts, write into an external project, close missing evidence, convert not-run into pass, or modify organization truth.
