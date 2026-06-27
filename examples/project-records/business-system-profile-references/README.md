# Business System Profile Reference Project Examples

These examples show how central project records can reference organization-level Business System profiles without becoming real private project records.

They are public-safe examples only. They are not stored under `workspace/projects/<project-id>/`, and they do not create any external project `.agentpal/` directories.

## Examples

| Example | Referenced profile | Project scope |
| --- | --- | --- |
| `content-ops-demo/` | `examples/capability-inventory/business-system-profiles/notion-public-governance-profile.example.json` | content planning, editorial notes, document reference |
| `sales-ops-demo/` | `examples/capability-inventory/business-system-profiles/generic-crm-public-governance-profile.example.json` | contact follow-up planning, deal review notes, customer service handoff notes |

## Boundary

Project records may reference organization Business System profiles and add project-scope limitations, not-run checks, missing evidence, and usage memory.

Project records must not:

- update `workspace/organization/contacts/pals.json`
- convert project usage memory into organization truth
- copy central Pal rosters into an external project
- write `.agentpal/business-systems/` or `.agentpal/capability-inventory/` into an external project by default
- claim connectors, API clients, credentials, automatic scans, automatic writes, or keyword routing

