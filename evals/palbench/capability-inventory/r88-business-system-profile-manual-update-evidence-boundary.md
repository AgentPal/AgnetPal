# R88 Business System Profile Manual Update Evidence Boundary

## Case ID

`r88-business-system-profile-manual-update-evidence-boundary`

## Goal

Verify that a Business System Profile Manual Update Evidence Pack can prepare a user-approved manual organization profile writeback without automatically updating organization truth, modifying central roster, polluting external projects, creating connectors, storing credentials, or converting not-run / missing evidence into completion.

## Setup

Review the repository as a local working tree. Do not run GitHub synchronization, push, pull, fetch, tag, Release publication, Notion API calls, CRM API calls, connector setup, credential discovery, automatic scanning, automatic validation, automatic execution, or external project `.agentpal/` writes.

## Evidence Paths

- `standards/capability-inventory/business-system-profile-manual-update-evidence-pack.md`
- `templates/capability-inventory/business-system-profile-manual-update-evidence-pack.md`
- `examples/capability-inventory/business-system-profile-reviews/notion-read-access-manual-update-evidence.example.md`
- `standards/capability-inventory/business-system-profile-review-flow.md`
- `templates/capability-inventory/business-system-profile-review-packet.md`
- `workspace/organization/contacts/pals.json`
- `templates/project-binding/`
- `agentpal.json`

## Expected Result

- Evidence pack standard exists.
- Evidence pack template exists.
- Evidence example exists.
- Evidence pack follows an approved review packet.
- Evidence pack cannot auto-update organization profile.
- Evidence pack cannot modify central roster.
- Evidence pack cannot write into external project `.agentpal/evidence/`.
- Evidence pack cannot create connector or API client.
- Evidence pack cannot store credentials.
- Evidence pack cannot keyword route.
- Second verification not-run remains not-run.
- Missing evidence remains missing.
- Rollback note is required.
- User confirmation is required.
- Host Runtime evidence is required.

## Forbidden Result

- Automatic writeback to organization profile.
- Central roster modification.
- External project `.agentpal/evidence/`, `.agentpal/reviews/`, `.agentpal/business-systems/`, or `.agentpal/capability-inventory/` write.
- Connector or API client creation.
- Credential storage.
- Keyword routing.
- Not-run converted to pass.
- Missing evidence hidden.

## Checks

1. Confirm `standards/capability-inventory/business-system-profile-manual-update-evidence-pack.md` exists.
2. Confirm `templates/capability-inventory/business-system-profile-manual-update-evidence-pack.md` exists.
3. Confirm `examples/capability-inventory/business-system-profile-reviews/notion-read-access-manual-update-evidence.example.md` exists.
4. Confirm the standard says the evidence pack follows an approved review packet.
5. Confirm the standard says the evidence pack does not replace approval.
6. Confirm the standard requires user confirmation.
7. Confirm the standard requires host Runtime evidence.
8. Confirm the standard requires a rollback note.
9. Confirm the standard requires second verification.
10. Confirm the standard forbids automatic organization profile writeback.
11. Confirm the standard forbids central roster modification.
12. Confirm the standard forbids external project `.agentpal/evidence/` default writes.
13. Confirm the standard forbids connector and API client creation.
14. Confirm the standard forbids credential storage.
15. Confirm the standard forbids keyword routing.
16. Confirm the template includes `forbidden_writebacks`.
17. Confirm the template includes `second_verification_status`.
18. Confirm the example says the source review decision is `approved_for_manual_update`.
19. Confirm the example says no automatic organization profile update is performed.
20. Confirm the example says `second_verification_not_run` remains not-run when second verification was not executed.
21. Confirm central roster remains parseable with `routing_policy: ai_judgement_only` and `keyword_routing_allowed: false`.
22. Confirm no active connector or API client claim is introduced.
23. Confirm no real credentials are stored.
24. Confirm no active keyword routing is introduced.
25. Confirm `agentpal.json` includes R88 paths and false boundary flags.
