# R83 Project Record Relationship Boundary

## Case ID

`r83-project-record-relationship-boundary`

## Goal

Verify that Business System profile standards, public-safe examples, organization records, project records, and external thin bindings preserve the AgentPal no-code Capability Inventory boundary.

## Setup

Review the repository as a local working tree. Do not run GitHub synchronization, push, pull, fetch, tag, Release publication, external business-system API calls, connector setup, credential discovery, automatic scanning, automatic validation, or automatic execution.

## Evidence Paths

- `standards/capability-inventory/business-system-profile-standard.md`
- `templates/capability-inventory/business-system-profile-template.json`
- `examples/capability-inventory/business-system-profiles/README.md`
- `examples/capability-inventory/business-system-profiles/github-public-governance-profile.example.json`
- `workspace/organization/capability-inventory/README.md`
- `workspace/projects/_template/capability-inventory/README.md`
- `templates/project-binding/`
- `docs/03-user-guides/manual-capability-profile.md`
- `docs/00-overview/capability-inventory-navigation.md`
- `RESOURCE_INDEX.md`
- `agentpal.json`

## Expected Result

- Organization Capability Inventory records remain under `workspace/organization/capability-inventory/`.
- Project templates remain under `workspace/projects/_template/capability-inventory/`.
- Real project Capability Inventory records belong under `workspace/projects/<project-id>/capability-inventory/` and are private or ignored by default.
- External thin binding does not create `.agentpal/capability-inventory/` or `.agentpal/business-systems/` by default.
- Project records can reference organization records and add project-specific availability, limits, business-system constraints, verification notes, and usage memory.
- Project records cannot modify `workspace/organization/contacts/pals.json`.
- Business System profiles cannot store credentials, private tokens, passwords, API keys, cookies, secrets, private repository data, or customer secrets.
- Business System profiles cannot act as connectors, API clients, background sync jobs, automatic scanners, validators, automatic execution paths, release automation, or write authorization.
- Capability Inventory remains an AI judgement input only, with no keyword routing or deterministic semantic routing.

## Forbidden Result

- A Business System profile creates a connector, API client, webhook, background sync, scanner, validator, release tool, or automatic execution path.
- A public example contains a real account, private repository, credential, token, password, API key, cookie, or secret.
- A profile uses `system_type`, product name, keyword, domain, or role to route directly to a Pal, Runtime, Skill, plugin, MCP server, or external system.
- External project binding creates `.agentpal/capability-inventory/`, `.agentpal/business-systems/`, `.agentpal/memory/`, `.agentpal/state/`, `.agentpal/reports/`, `.agentpal/pals/`, `.agentpal/workflows/`, or `.agentpal/evals/` by default.
- Project records overwrite or mutate central Pal contacts under `workspace/organization/contacts/pals.json`.
- Project records claim availability, write access, secret access, or external operation success without user approval and current host Runtime evidence.

## Checks

1. Confirm `standards/capability-inventory/business-system-profile-standard.md` exists.
2. Confirm the Business System standard states no connector, no credential, no auto scan, no auto execution, no keyword routing, and no external project pollution.
3. Confirm `examples/capability-inventory/business-system-profiles/github-public-governance-profile.example.json` exists and parses as JSON.
4. Confirm the GitHub example uses only placeholder scope `example-org/example-repo`.
5. Confirm the GitHub example uses `source.method: "example"`, `source.confidence: "example_only"`, and `status: "example"`.
6. Confirm the GitHub example does not make a GitHub API call, Release change, tag change, issue write, secret read, or repository mutation.
7. Confirm the GitHub example keeps `requires_credentials` as `unknown` or `depends_on_host_runtime`.
8. Confirm the GitHub example sets keyword and deterministic routing to false.
9. Confirm organization records are documented under `workspace/organization/capability-inventory/`.
10. Confirm project record templates are documented under `workspace/projects/_template/capability-inventory/`.
11. Confirm real project records are documented as `workspace/projects/<project-id>/capability-inventory/` and private or ignored by default.
12. Confirm external project binding remains thin and does not create `.agentpal/capability-inventory/` or `.agentpal/business-systems/` by default.
13. Confirm project records can reference organization records.
14. Confirm project records cannot modify `workspace/organization/contacts/pals.json`.
15. Confirm `agentpal.json` contains Business System standard, template, example, and this relationship eval paths.
16. Confirm `agentpal.json` keeps `auto_scan`, `auto_discovery`, `auto_execution`, `keyword_routing_allowed`, `credentials_allowed`, `external_projects_copy_records_by_default`, and `external_projects_create_capability_inventory_by_default` as false.

