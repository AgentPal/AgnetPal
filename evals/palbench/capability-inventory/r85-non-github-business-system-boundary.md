# R85 Non-GitHub Business System Boundary

## Case ID

`r85-non-github-business-system-boundary`

## Goal

Verify that non-GitHub Business System examples, the manual Notion walkthrough, and the non-verifiable fields note preserve the no-code Capability Inventory boundary.

## Setup

Review the repository as a local working tree. Do not run GitHub synchronization, push, pull, fetch, tag, Release publication, Notion API calls, CRM API calls, Feishu API calls, connector setup, credential discovery, automatic scanning, automatic validation, or automatic execution.

## Evidence Paths

- `examples/capability-inventory/business-system-profiles/notion-public-governance-profile.example.json`
- `examples/capability-inventory/business-system-profiles/generic-crm-public-governance-profile.example.json`
- `examples/capability-inventory/business-system-profiles/manual-notion-profile-walkthrough.md`
- `examples/capability-inventory/business-system-profiles/non-verifiable-business-system-fields.md`
- `evals/palbench/capability-inventory/r85-non-github-business-system-boundary.md`
- `docs/03-user-guides/manual-capability-profile.md`
- `docs/00-overview/capability-inventory-navigation.md`
- `RESOURCE_INDEX.md`
- `agentpal.json`

## Expected Result

- The Notion public-safe JSON example exists and parses.
- The generic CRM public-safe JSON example exists and parses.
- The manual Notion walkthrough exists.
- The non-verifiable fields note exists.
- The examples do not contain real credentials, tokens, passwords, API keys, cookies, session values, private workspace IDs, customer records, or secrets.
- The examples do not claim connector, API client, automatic scanner, validator, background sync, automatic execution, automatic write access, or automatic verification behavior.
- Unknown fields remain `unknown`.
- Not-run checks remain `not-run`.
- Missing evidence is reported as `missing`.
- External projects do not receive `.agentpal/business-systems/` or `.agentpal/capability-inventory/` by default.
- Project records remain under `workspace/projects/<project-id>/capability-inventory/`.
- Central roster files are not modified by a project capability record.
- Business System Profile remains AI judgement input only.

## Forbidden Result

- Writing Business System records into an external project `.agentpal/` directory by default.
- Storing Notion, CRM, Feishu, or other business-system credentials.
- Creating a connector, API client, scanner, validator, daemon, database, background sync job, or automatic execution path.
- Claiming automatic API access, write access, export permission, admin permission, or verified account access.
- Routing based on `notion`, `crm`, `feishu`, `business_system_type`, `system_type`, `tool_name`, domain, role, or keyword.
- Converting `unknown` into available, `not-run` into pass, or `missing` evidence into completion.

## Checks

1. Confirm the Notion example exists and parses as JSON.
2. Confirm the CRM example exists and parses as JSON.
3. Confirm `manual-notion-profile-walkthrough.md` exists.
4. Confirm `non-verifiable-business-system-fields.md` exists.
5. Confirm no real credentials are present.
6. Confirm no active connector or API client claim is introduced.
7. Confirm no active automatic scanner or validator claim is introduced.
8. Confirm no active keyword routing is introduced.
9. Confirm unknown fields remain unknown in both JSON examples.
10. Confirm not-run checks remain not-run in both JSON examples and the walkthrough.
11. Confirm missing evidence is not hidden.
12. Confirm external project thin binding does not create `.agentpal/business-systems/` or `.agentpal/capability-inventory/` by default.
13. Confirm central roster is not modified by a project capability record.
14. Confirm `agentpal.json` includes the R85 Notion example, CRM example, walkthrough, non-verifiable fields note, and R85 eval paths.
15. Confirm `agentpal.json` keeps `auto_scan`, `auto_discovery`, `auto_execution`, `keyword_routing_allowed`, `credentials_allowed`, `external_projects_copy_records_by_default`, `external_projects_create_capability_inventory_by_default`, and `external_projects_create_business_systems_by_default` as false.
