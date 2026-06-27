# R84 Business System Manual Walkthrough Boundary

## Case ID

`r84-business-system-manual-walkthrough-boundary`

## Goal

Verify that the Business System manual walkthrough, project record reference, unknown / not-run / missing examples, and failure example preserve the no-code Capability Inventory boundary.

## Setup

Review the repository as a local working tree. Do not run GitHub synchronization, push, pull, fetch, tag, Release publication, external business-system API calls, connector setup, credential discovery, automatic scanning, automatic validation, or automatic execution.

## Evidence Paths

- `examples/capability-inventory/business-system-profiles/manual-github-profile-walkthrough.md`
- `examples/capability-inventory/business-system-profiles/github-project-record-reference.example.md`
- `examples/capability-inventory/business-system-profiles/unknown-not-run-missing-examples.md`
- `examples/failures/business-system-profile-as-connector.md`
- `evals/palbench/capability-inventory/r84-business-system-manual-walkthrough-boundary.md`
- `docs/03-user-guides/manual-capability-profile.md`
- `docs/00-overview/capability-inventory-navigation.md`
- `RESOURCE_INDEX.md`
- `agentpal.json`

## Expected Result

- The walkthrough exists and shows the path from user-confirmed facts to organization profile draft to project record reference.
- The walkthrough explains what remains `unknown`, what is `not-run`, and what evidence is `missing`.
- The project record reference stores project-specific notes under `workspace/projects/<project-id>/capability-inventory/`, not external project `.agentpal/`.
- The unknown / not-run / missing examples explain all three terms and include the required boundary text.
- The failure example exists and is clearly marked forbidden.
- The failure example fake token appears only as a forbidden fake value.
- Business System Profile remains an AI judgement input only.
- External projects do not receive `.agentpal/business-systems/` or `.agentpal/capability-inventory/` by default.
- Project capability records do not modify the central roster.

## Forbidden Result

- Any example stores a real credential, token, password, API key, cookie, private key, session value, or secret.
- Any example creates or claims an active connector, API client, scanner, validator, background sync job, Release tool, or automatic execution path.
- Any example uses `system_type=github`, `github`, a domain, a role, or a keyword to route directly to a Pal, Runtime, Skill, plugin, MCP server, or external tool.
- Any example defaults to writing capability records into an external project's `.agentpal/business-systems/` or `.agentpal/capability-inventory/` directory.
- Any project capability record modifies `workspace/organization/contacts/pals.json`.
- `unknown` becomes available, `not-run` becomes pass, or missing evidence is hidden.

## Checks

1. Confirm `manual-github-profile-walkthrough.md` exists.
2. Confirm `github-project-record-reference.example.md` exists.
3. Confirm `unknown-not-run-missing-examples.md` exists.
4. Confirm `examples/failures/business-system-profile-as-connector.md` exists.
5. Confirm the failure example is clearly marked forbidden.
6. Confirm no real credentials are present.
7. Confirm the only GitHub token-like prefix hit is the fake forbidden value in the forbidden failure example.
8. Confirm no active connector or API client claim is introduced.
9. Confirm no active automatic scanner or validator claim is introduced.
10. Confirm no active keyword routing is introduced.
11. Confirm external project thin binding does not create `.agentpal/business-systems/` or `.agentpal/capability-inventory/` by default.
12. Confirm central roster is not modified by a project capability record.
13. Confirm `agentpal.json` includes the R84 walkthrough, unknown / not-run / missing examples, failure example, and R84 eval paths.
14. Confirm `agentpal.json` keeps `auto_scan`, `auto_discovery`, `auto_execution`, `keyword_routing_allowed`, `credentials_allowed`, `external_projects_copy_records_by_default`, `external_projects_create_capability_inventory_by_default`, and `external_projects_create_business_systems_by_default` as false.
