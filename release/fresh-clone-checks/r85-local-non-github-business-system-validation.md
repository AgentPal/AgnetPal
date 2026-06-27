# R85 Local Non-GitHub Business System Validation

Date: 2026-06-28

Scope: local-only validation for non-GitHub Business System examples, a manual Notion walkthrough, non-verifiable field guidance, R85 PalBench coverage, metadata updates, and no-code boundary preservation.

No GitHub synchronization, push, pull, fetch, tag, Release action, Notion API call, CRM API call, connector setup, credential discovery, automatic scan, automatic validation, or automatic execution was performed.

## Directory And File Evidence

| Check | Result |
| --- | --- |
| Working directory | `J:\开发\AgentPal` |
| Git top level | `J:\开发\AgentPal` |
| Notion example exists | true |
| Notion example path | `examples/capability-inventory/business-system-profiles/notion-public-governance-profile.example.json` |
| CRM example exists | true |
| CRM example path | `examples/capability-inventory/business-system-profiles/generic-crm-public-governance-profile.example.json` |
| Manual Notion walkthrough exists | true |
| Manual Notion walkthrough path | `examples/capability-inventory/business-system-profiles/manual-notion-profile-walkthrough.md` |
| Non-verifiable fields note exists | true |
| Non-verifiable fields note path | `examples/capability-inventory/business-system-profiles/non-verifiable-business-system-fields.md` |
| R85 eval exists | true |
| R85 eval path | `evals/palbench/capability-inventory/r85-non-github-business-system-boundary.md` |
| Thin binding templates exist | true |
| Central project template exists | true |
| Official Pal directory exists | true |

## Notion Example Summary

`notion-public-governance-profile.example.json` is a public-safe example with placeholder workspace and database names only.

It keeps the following as unknown or unverified:

- availability;
- workspace access;
- database access;
- page read access;
- page write access;
- API access;
- integration status;
- export permission;
- admin permission;
- billing or plan capability;
- user role;
- workspace ID.

It uses empty `allowed_operations`, requires explicit user approval for external writes, and states that Business System Profile remains AI judgement input only with no keyword or deterministic routing.

## CRM Example Summary

`generic-crm-public-governance-profile.example.json` is a public-safe generic CRM example with placeholder CRM names only and no customer data.

It keeps the following as unknown or unverified:

- account access;
- contact read access;
- deal write access;
- ticket write access;
- pipeline access;
- export permission;
- API access;
- admin permission;
- billing or plan capability;
- user role;
- business workflow ownership.

It uses empty `allowed_operations`, requires explicit user approval for external writes, and does not infer customer-data access from `system_type: crm`.

## Walkthrough Summary

`manual-notion-profile-walkthrough.md` covers:

- user-confirmed possible Notion use for project docs or content planning;
- organization profile draft location under `workspace/organization/capability-inventory/business-systems/`;
- project record reference location under `workspace/projects/<project-id>/capability-inventory/business-systems.md`;
- unknown fields for access, permissions, API, workspace ID, role, export, and billing;
- not-run checks for workspace, database, page, write, API, integration, export, admin, and billing checks;
- missing evidence such as user confirmation, host Runtime evidence, screenshot, export, admin setting, or task report;
- correct next step: ask the user for confirmation or run a user-approved host Runtime check;
- forbidden behavior: no Notion connection, no token storage, no connector, no external `.agentpal/business-systems/`, and no keyword routing.

## Non-Verifiable Fields Summary

`non-verifiable-business-system-fields.md` explains that access, write permission, admin permission, API availability, export permission, billing or plan capability, user role, workspace / tenant / account identifiers, integration status, workflow ownership, output destinations, and customer-data handling permission usually cannot be verified by AgentPal itself.

It requires evidence from user confirmation, current host Runtime evidence, business system UI confirmation, screenshot, exported report, documented admin setting, system log, audit record, or a task report.

It includes the required boundary:

```text
Not verified != false
Not run != pass
Unknown != available
Missing evidence != acceptable completion
```

## R85 Eval Summary

`evals/palbench/capability-inventory/r85-non-github-business-system-boundary.md` checks:

- Notion example exists and parses;
- CRM example exists and parses;
- manual Notion walkthrough exists;
- non-verifiable fields note exists;
- no real credentials;
- no active connector / API client claim;
- no active automatic scanner or validator claim;
- no active keyword routing;
- unknown fields remain unknown;
- not-run checks remain not-run;
- missing evidence is not hidden;
- no default external `.agentpal/business-systems/` or `.agentpal/capability-inventory/`;
- central roster is not modified by a project capability record;
- `agentpal.json` keeps the R85 paths and false auto / credential / external-copy flags.

## Metadata And Index Checks

| Check | Result |
| --- | --- |
| `agentpal.json` includes Notion example path | pass |
| `agentpal.json` includes CRM example path | pass |
| `agentpal.json` includes manual Notion walkthrough path | pass |
| `agentpal.json` includes non-verifiable fields path | pass |
| `agentpal.json` includes R85 eval path | pass |
| `auto_scan` | false |
| `auto_discovery` | false |
| `auto_execution` | false |
| `keyword_routing_allowed` | false |
| `credentials_allowed` | false |
| `external_projects_copy_records_by_default` | false |
| `external_projects_create_capability_inventory_by_default` | false |
| `external_projects_create_business_systems_by_default` | false |
| `RESOURCE_INDEX.md` six Capability Inventory categories retained | pass |
| `RESOURCE_INDEX.md` lists R85 Notion, CRM, walkthrough, non-verifiable fields, and eval | pass |

## JSON And Roster Checks

| Check | Result |
| --- | --- |
| Visible JSON files parsed | 80 |
| JSON parse failures | 0 |
| Notion example parse | pass |
| CRM example parse | pass |
| Official Pal dirs | 9 |
| Central registered Pals | 9 |
| Central active Pals | 9 |
| `routing_policy` | `ai_judgement_only` |
| `keyword_routing_allowed` | false |
| Exact JSON route keys `keyword_map`, `domain_map`, `role_map` | 0 |

## Search Classification

| Check | Result | Classification |
| --- | --- | --- |
| `.agentpal/(memory|state|reports|context|index|pals|workflows|evals|capability-inventory|business-systems)` | 0 active bugs | hits are forbidden lists, boundary language, archive records, release evidence, examples that say not to write there, or regression expectations |
| active keyword routing bug | 0 active bugs | exact JSON route-key search returned 0; text hits are forbidden, boundary, or eval contexts |
| Notion / CRM / Feishu route bug | 0 active bugs | hits are negative boundary text or `business_system_type_is_not_a_route` fields |
| active scanner / validator / automatic scan claim | 0 active bugs | hits are no-code boundary, known limitation, failure example, release evidence, or R85 negative contexts |
| active connector / API client claim | 0 active bugs | hits are negative boundaries, forbidden failure example, templates, examples, or release-safety text |
| credential / token / password / API key / cookie / secret leak | 0 real leaks found | hits are policy, exclusions, templates, examples, or release-safety text; R85 examples contain no real credential values |

## Thin Binding Check

| Check | Result |
| --- | --- |
| `templates/project-binding/` exists | true |
| `workspace/projects/_template/` exists | true |
| Forbidden default child dirs in project-binding templates | none found |
| External project `.agentpal/capability-inventory/` default | absent |
| External project `.agentpal/business-systems/` default | absent |

## Clean Copy Check

Local clean-copy path:

```text
C:\Users\Administrator\AppData\Local\Temp\agentpal-r85-clean-copy-20260628031126
```

| Check | Result |
| --- | --- |
| Git-visible files | 2804 |
| Copied files | 2804 |
| Required R85 / binding paths missing | 0 |
| Clean-copy JSON files parsed | 53 |
| Clean-copy JSON parse failures | 0 |
| Clean-copy official Pal dirs | 9 |
| Clean-copy registered Pals | 9 |
| Clean-copy active Pals | 9 |
| Clean-copy `routing_policy` | `ai_judgement_only` |
| Clean-copy `keyword_routing_allowed` | false |
| Clean-copy exact JSON route-key hits | 0 |
| Clean-copy forbidden project-binding child dirs | 0 |
| Clean-copy `auto_scan` | false |
| Clean-copy `auto_discovery` | false |
| Clean-copy `auto_execution` | false |
| Clean-copy `credentials_allowed` | false |

Clean-copy gates passed: required paths missing 0, JSON failures 0, official Pal dirs 9, registered Pals 9, active Pals 9, keyword routing false, JSON route-key hits 0, forbidden project-binding child dirs 0, automatic / credential flags false, and copied files matched Git-visible files.

## Boundary Summary

R85 did not add a CLI, app, scanner, validator, daemon, database, automatic sync, automatic execution engine, keyword router, deterministic semantic router, connector, API client, Notion integration, CRM integration, Feishu integration, GitHub Release tool, or runtime capability probe.

R85 kept external project binding thin: project-local `.agentpal/` remains an entrypoint surface only, while project memory, reports, source maps, governance records, and capability inventory belong in central AgentPal Workspace records.
