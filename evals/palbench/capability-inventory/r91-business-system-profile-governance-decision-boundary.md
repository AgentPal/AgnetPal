# R91 Business System Profile Governance Decision Boundary

## Case ID

`r91-business-system-profile-governance-decision-boundary`

## Goal

Verify that a Business System Profile Governance Decision Record can record a human governance decision after review, evidence pack, replay record, and audit trail review without becoming an approval engine, execution system, automatic organization profile updater, central roster mutation, external project `.agentpal/` writer, connector, credential store, missing-evidence closer, not-run-to-pass converter, or keyword route.

## Setup

Review the repository as a local working tree. Do not run GitHub synchronization, push, pull, fetch, tag, Release publication, Notion API calls, CRM API calls, connector setup, credential discovery, automatic scanning, automatic validation, automatic execution, automatic rollback, automatic API calls, or external project `.agentpal/` writes.

## Evidence Paths

- `standards/capability-inventory/business-system-profile-governance-decision-record.md`
- `templates/capability-inventory/business-system-profile-governance-decision-record.md`
- `examples/capability-inventory/business-system-profile-reviews/notion-read-access-governance-decision.example.md`
- `examples/capability-inventory/business-system-profile-reviews/notion-read-access-audit-trail-index.example.md`
- `examples/capability-inventory/business-system-profile-reviews/notion-read-access-review.example.md`
- `examples/capability-inventory/business-system-profile-reviews/notion-read-access-manual-update-evidence.example.md`
- `examples/capability-inventory/business-system-profile-reviews/notion-read-access-manual-writeback-replay.example.md`
- `workspace/organization/contacts/pals.json`
- `templates/project-binding/`
- `agentpal.json`

## Expected Result

- Governance decision standard exists.
- Governance decision template exists.
- Governance decision example exists.
- Decision record references audit trail, review, evidence, and replay records.
- Decision record cannot auto-update organization profile.
- Decision record cannot auto-modify central roster.
- Decision record cannot auto-close missing evidence.
- Decision record cannot convert not-run to pass.
- Decision record cannot create connector or API client.
- Decision record cannot store credentials.
- Decision record cannot keyword route.
- Decision record cannot write into external project `.agentpal/governance-decisions/`.
- `needs_second_verification` keeps manual update blocked.
- needs_second_verification keeps manual update blocked.
- Unknown / not-run / missing are preserved.

## Forbidden Result

- Automatic organization profile update.
- Central roster modification.
- External project `.agentpal/governance-decisions/`.
- Connector or API client creation.
- Credential storage.
- Keyword routing.
- Not-run converted to pass.
- Missing evidence hidden.
- Manual update allowed while second verification missing.

## Checks

1. Confirm `standards/capability-inventory/business-system-profile-governance-decision-record.md` exists.
2. Confirm `templates/capability-inventory/business-system-profile-governance-decision-record.md` exists.
3. Confirm `examples/capability-inventory/business-system-profile-reviews/notion-read-access-governance-decision.example.md` exists.
4. Confirm the standard says governance decision records capture a human governance decision.
5. Confirm the standard says it is not an approval engine and not an execution system.
6. Confirm the standard references audit trail, review, evidence, replay, second verification, user confirmation, and host Runtime evidence.
7. Confirm the standard forbids automatic organization profile updates.
8. Confirm the standard forbids central roster modification.
9. Confirm the standard forbids automatic missing-evidence closure.
10. Confirm the standard forbids converting not-run to pass.
11. Confirm the standard forbids connector and API client creation.
12. Confirm the standard forbids credential storage.
13. Confirm the standard forbids keyword routing.
14. Confirm the standard forbids external project `.agentpal/governance-decisions/` default writes.
15. Confirm the template includes `forbidden_actions`.
16. Confirm the template says the record is not an execution engine.
17. Confirm the example references `notion-read-access-audit-trail-index.example.md`.
18. Confirm the example references `notion-read-access-review.example.md`.
19. Confirm the example references `notion-read-access-manual-update-evidence.example.md`.
20. Confirm the example references `notion-read-access-manual-writeback-replay.example.md`.
21. Confirm the example uses `decision: needs_second_verification`.
22. Confirm the example keeps `manual_update_allowed: false` while second verification evidence is missing.
23. Confirm the example preserves unknowns.
24. Confirm the example preserves not-run checks.
25. Confirm the example preserves missing evidence.
26. Confirm central roster remains parseable with `routing_policy: ai_judgement_only` and `keyword_routing_allowed: false`.
27. Confirm no active connector or API client claim is introduced.
28. Confirm no real credentials are stored.
29. Confirm no active keyword routing is introduced.
30. Confirm `agentpal.json` includes R91 paths and false boundary flags.
