# R87 Business System Profile Review Flow Boundary

## Case ID

`r87-business-system-profile-review-flow-boundary`

## Goal

Verify that Business System Profile Review Flow lets project usage memory propose organization-level review without automatically upgrading project memory into organization truth.

## Setup

Review the repository as a local working tree. Do not run GitHub synchronization, push, pull, fetch, tag, Release publication, Notion API calls, CRM API calls, connector setup, credential discovery, automatic scanning, automatic validation, automatic execution, or external project `.agentpal/` writes.

## Evidence Paths

- `standards/capability-inventory/business-system-profile-review-flow.md`
- `templates/capability-inventory/business-system-profile-review-packet.md`
- `examples/capability-inventory/business-system-profile-reviews/README.md`
- `examples/capability-inventory/business-system-profile-reviews/notion-read-access-review.example.md`
- `docs/03-user-guides/project-usage-memory-boundary.md`
- `workspace/organization/contacts/pals.json`
- `templates/project-binding/`
- `agentpal.json`

## Expected Result

- Review flow standard exists.
- Review packet template exists.
- Example review exists.
- Project usage memory can propose review.
- Project usage memory cannot update organization truth.
- Review packet cannot auto-update organization profile.
- Review packet cannot modify central roster.
- Review packet cannot write into external project `.agentpal/reviews/`.
- Review packet cannot create connector or API client.
- Review packet cannot store credentials.
- Review packet cannot keyword route.
- `blocked_missing_evidence` remains blocked.
- `unknown`, `not-run`, and `missing` are preserved.

## Forbidden Result

- Project usage memory automatically updates organization profile.
- Review packet modifies `workspace/organization/contacts/pals.json`.
- Review packet writes to external project `.agentpal/reviews/`, `.agentpal/business-systems/`, or `.agentpal/capability-inventory/`.
- Review flow creates connector, API client, scanner, validator, daemon, database, background sync, or automatic execution.
- Review flow stores credentials, tokens, passwords, API keys, cookies, secrets, or private account values.
- Review flow routes by Notion, CRM, `business_system_type`, `system_type`, `tool_name`, keyword, domain, or role.

## Checks

1. Confirm `standards/capability-inventory/business-system-profile-review-flow.md` exists.
2. Confirm `templates/capability-inventory/business-system-profile-review-packet.md` exists.
3. Confirm `examples/capability-inventory/business-system-profile-reviews/notion-read-access-review.example.md` exists.
4. Confirm the standard says project usage memory can suggest review but cannot update organization truth by itself.
5. Confirm the standard requires explicit user confirmation and reviewable host Runtime evidence.
6. Confirm the standard forbids automatic organization profile updates.
7. Confirm the standard forbids central roster modification.
8. Confirm the standard forbids external project `.agentpal/reviews/` default writes.
9. Confirm the template includes `forbidden_writebacks`.
10. Confirm the example decision remains `blocked_missing_evidence`.
11. Confirm the example preserves `unknown`, `not-run`, and `missing`.
12. Confirm central roster remains parseable with `routing_policy: ai_judgement_only` and `keyword_routing_allowed: false`.
13. Confirm no active connector or API client claim is introduced.
14. Confirm no real credentials are stored.
15. Confirm no active keyword routing is introduced.
16. Confirm `agentpal.json` includes R87 paths and false boundary flags.

