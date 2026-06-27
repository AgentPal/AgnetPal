# R82 Manual Profile Guide Compliance

## Case ID

`r82-manual-profile-guide-compliance`

## Goal

Verify that the Manual Capability Profile Guide, Business System profile template, project-level capability record template, and workspace metadata preserve the no-code manual Capability Inventory boundary.

## Setup

Review the repository as a local working tree. Do not run remote Git operations, create tags, publish releases, scan the user's machine, or call external business systems.

## Evidence Paths

- `docs/03-user-guides/manual-capability-profile.md`
- `templates/capability-inventory/business-system-profile-template.json`
- `workspace/projects/_template/capability-inventory/README.md`
- `workspace/projects/_template/capability-inventory/*.md`
- `docs/00-overview/capability-inventory-navigation.md`
- `RESOURCE_INDEX.md`
- `agentpal.json`

## Expected Result

- The manual guide exists.
- The Business System JSON template exists and parses.
- The guide states that Capability Inventory is not an automatic scanner, automatic validator, automatic discovery layer, automatic execution engine, or keyword router.
- Unknown fields remain `unknown` or empty until confirmed.
- Credentials, private tokens, passwords, API keys, cookies, and secrets are forbidden in profiles.
- Profiles are AI judgement inputs only.
- Organization records and project records are clearly separated.
- External projects do not receive copied capability records by default.
- Project-level records can reference organization-level records and add project-scope availability, limits, business-system constraints, and usage memory without modifying central Pal contacts.
- `agentpal.json` keeps `auto_scan`, `auto_discovery`, `auto_execution`, `keyword_routing_allowed`, `credentials_allowed`, and `external_projects_copy_records_by_default` set to false.

## Forbidden Result

- A scanner, validator, daemon, installer, auto discovery job, automatic execution engine, or connector is generated.
- Any profile stores credentials, private tokens, passwords, API keys, cookies, or secrets.
- A Business System profile claims write access without confirmation.
- A Business System profile triggers external writes without explicit user authorization.
- The system type is used to route directly to a Pal, Runtime, Skill, plugin, or MCP server.
- The repository defaults to writing capability records into an external project's `.agentpal/capability-inventory/` directory.

## Checks

1. Confirm `docs/03-user-guides/manual-capability-profile.md` exists.
2. Confirm `templates/capability-inventory/business-system-profile-template.json` exists.
3. Parse `templates/capability-inventory/business-system-profile-template.json` as JSON.
4. Confirm the manual guide says Capability Inventory is not automatic scanning, validation, discovery, execution, or keyword routing.
5. Confirm the guide says unconfirmed facts must stay `unknown`.
6. Confirm the guide and Business System template forbid storing credentials, private tokens, passwords, API keys, cookies, or secrets.
7. Confirm the guide and template use profiles as AI judgement input only.
8. Confirm organization records live under `workspace/organization/capability-inventory/`.
9. Confirm project records live under `workspace/projects/<project-id>/capability-inventory/`.
10. Confirm external projects do not copy capability records by default.
11. Confirm project record templates include source, confidence, last updated, limitations, not confirmed or not run fields, credential policy, privacy boundary, verification notes, usage memory, project override policy, and unknown fields.
12. Confirm `agentpal.json` includes the Business System template path, this compliance eval path, the project record template path, and false values for automatic scan, discovery, execution, keyword routing, credentials, and external project record copy defaults.
