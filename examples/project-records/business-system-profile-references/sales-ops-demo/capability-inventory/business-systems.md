# Sales Ops Demo Business Systems

This project-level example references a Generic CRM organization profile example without modifying organization facts.

| Field | Value |
| --- | --- |
| project_id | `sales-ops-demo` |
| project_type | `example` |
| organization_profile_ref | `examples/capability-inventory/business-system-profiles/generic-crm-public-governance-profile.example.json` |
| real organization profile location | `workspace/organization/capability-inventory/business-systems/` |
| project reference path | `examples/project-records/business-system-profile-references/sales-ops-demo/capability-inventory/business-systems.md` |
| system | Generic CRM public governance example |
| project scope | contact follow-up planning; deal review notes; customer service handoff notes |
| project available | unknown |
| source | example only |
| confidence | example_only |

## Unknown

- account access
- contact read access
- deal write access
- export permission
- API access

## Not-Run Checks

- CRM login check: not-run
- contact visibility check: not-run
- write permission check: not-run
- export permission check: not-run

## Missing Evidence

- user confirmation: missing
- host Runtime evidence: missing
- admin permission evidence: missing

## Forbidden

- no CRM connector
- no customer data export
- no CRM token
- no external project `.agentpal/business-systems/`
- no external project `.agentpal/capability-inventory/`
- no central roster modification
- no keyword routing

## Project Override Policy

This file records project-scope notes only. It must not update `workspace/organization/contacts/pals.json`, silently change organization-level CRM capability facts, or claim global CRM account, write, export, API, or customer-data access.

