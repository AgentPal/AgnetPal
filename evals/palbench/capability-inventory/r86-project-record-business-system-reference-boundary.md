# R86 Project Record Business System Reference Boundary

## Case ID

`r86-project-record-business-system-reference-boundary`

## Goal

Verify that public-safe central project record examples can reference organization-level Business System profiles without becoming real private project records, polluting external `.agentpal/`, changing the central roster, or turning project usage memory into organization truth.

## Setup

Review the repository as a local working tree. Do not run GitHub synchronization, push, pull, fetch, tag, Release publication, Notion API calls, CRM API calls, connector setup, credential discovery, automatic scanning, automatic validation, or automatic execution.

## Evidence Paths

- `examples/project-records/business-system-profile-references/README.md`
- `examples/project-records/business-system-profile-references/content-ops-demo/`
- `examples/project-records/business-system-profile-references/sales-ops-demo/`
- `docs/03-user-guides/project-usage-memory-boundary.md`
- `examples/capability-inventory/business-system-profiles/notion-public-governance-profile.example.json`
- `examples/capability-inventory/business-system-profiles/generic-crm-public-governance-profile.example.json`
- `workspace/organization/contacts/pals.json`
- `workspace/projects/_template/capability-inventory/`
- `templates/project-binding/`

## Expected Result

- `content-ops-demo` exists.
- `sales-ops-demo` exists.
- Both examples are under `examples/project-records/`, not `workspace/projects/<real-project-id>/`.
- Both examples include `PROJECT.md`, `project.json`, `capability-inventory/business-systems.md`, and `memory/project-usage-memory.md`.
- Both `project.json` files parse.
- Both examples reference organization or Business System profiles.
- Both keep project usage memory project-scoped.
- Neither modifies `workspace/organization/contacts/pals.json`.
- Neither writes to external project `.agentpal/business-systems/`.
- Neither writes to external project `.agentpal/capability-inventory/`.
- No connector or API client claim is introduced.
- No credentials are stored.
- No keyword routing is introduced.
- `unknown`, `not-run`, and `missing` evidence states are retained.

## Forbidden Result

- Example stored as a real private project record under `workspace/projects/<project-id>/`.
- Central roster changed.
- Project usage memory becomes organization truth.
- External project `.agentpal/` pollution.
- Connector or API client claim.
- Credential storage.
- Keyword routing based on Notion, CRM, `business_system_type`, `system_type`, or `tool_name`.
- Converting `unknown` into available, `not-run` into pass, or `missing` evidence into completion.

## Checks

1. Confirm `examples/project-records/business-system-profile-references/content-ops-demo/` exists.
2. Confirm `examples/project-records/business-system-profile-references/sales-ops-demo/` exists.
3. Confirm neither example is under `workspace/projects/`.
4. Confirm both examples include `PROJECT.md`, `project.json`, `capability-inventory/business-systems.md`, and `memory/project-usage-memory.md`.
5. Confirm both `project.json` files parse.
6. Confirm the content demo references `notion-public-governance-profile.example.json`.
7. Confirm the sales demo references `generic-crm-public-governance-profile.example.json`.
8. Confirm project usage memory says it is not organization truth.
9. Confirm central roster remains parseable with `routing_policy: ai_judgement_only` and `keyword_routing_allowed: false`.
10. Confirm thin binding templates do not create external `.agentpal/business-systems/` or `.agentpal/capability-inventory/` by default.
11. Confirm no active connector or API client claim is introduced.
12. Confirm no real credentials, tokens, passwords, API keys, cookies, or secrets are stored.
13. Confirm no active keyword routing is introduced.
14. Confirm `unknown`, `not-run`, and `missing` remain visible in both examples.
15. Confirm `agentpal.json` includes R86 example, guide, eval, and false boundary flags.

