# Business System Profile Standard

## Purpose

Business System Profiles record governance facts for external business systems that may matter during AI judgement. They describe what is known, unknown, allowed, forbidden, and evidence-backed about systems such as GitHub, Feishu, Notion, Jira, Linear, CRM, OA, ERP, WordPress, databases, or customer-specific tools.

They are no-code Capability Inventory records. They are not connectors, API clients, credential stores, permission grants, background sync jobs, automatic scanners, automatic validators, automatic execution paths, or keyword routes.

## What Belongs Here

- Public-safe system identity, such as name, system type, vendor, or product family.
- The intended governance scope, such as organization-wide notes or one project record.
- Confirmed access method, or `unknown` when access is not confirmed.
- Required permissions, allowed operations, forbidden operations, and approval gates.
- Output destinations and external write boundaries.
- Source, confidence, verification method, last checked value, and not-run notes.
- Privacy boundaries, retention limits, customer-data exclusions, and credential policy.
- Relationship to organization records, project records, and thin external bindings.

## What Does Not Belong Here

- Real credentials, private tokens, passwords, API keys, cookies, private keys, session values, or secrets.
- Private repository names, customer account identifiers, private URLs, or confidential system paths unless explicitly public-safe.
- Executable connector code, API client code, webhooks, background workers, daemons, sync jobs, or validators.
- Automatic scans of the user's machine, browser, accounts, cloud systems, repositories, or business tools.
- Claims that a system is available, writable, or authorized without current user confirmation or host Runtime evidence.
- Keyword maps, domain maps, role maps, deterministic routing tables, or semantic shortcuts from system type to Pal, Runtime, Skill, plugin, MCP server, or external tool.

## Required Fields

| Field | Required Meaning |
| --- | --- |
| `schema` | Profile schema or example schema identifier. |
| `profile_type` | Must be `business-system`. |
| `id` | Stable public-safe profile id. |
| `name` | Human-readable system or example name. |
| `system_type` | Broad category; never a routing key. |
| `description` | Public-safe purpose and boundary note. |
| `status` | `available`, `limited`, `unavailable`, `not-run`, `not-confirmed`, `unknown`, or `example`. |
| `source` | Method, confirmation basis, last checked value, and confidence. |
| `access` | Access method, approval requirement, credential policy, and whether credentials are required or unknown. |
| `required_permissions` | Permissions needed, or `unknown` / empty when unconfirmed. |
| `allowed_operations` | Conservative operations allowed by confirmed evidence. |
| `forbidden_operations` | Operations that must not happen from this profile. |
| `external_writes` | Approval and Runtime-evidence requirements before any external write. |
| `routing_boundary` | AI judgement input only; keyword and deterministic routing disabled. |
| `verification` | What was verified, what was not run, and what evidence is needed. |
| `unknown_fields` | Unconfirmed fields that must remain `unknown` until evidence exists. |

## Unknown Fields

Unknown or unconfirmed facts must stay as `unknown`, `not-run`, `not-confirmed`, `depends_on_host_runtime`, or empty arrays. Do not infer access from a product name. Do not infer write access from read access. Do not infer private repository, tenant, workspace, organization, or account visibility from public examples.

## Credential Policy

Business System Profiles must not store real credentials, private tokens, passwords, API keys, cookies, private keys, refresh tokens, session identifiers, webhook secrets, or customer secrets.

If a system requires credentials, the profile may say `requires_credentials: "depends_on_host_runtime"` or `requires_credentials: "unknown"`. The profile must not contain the credential value. The host Runtime or user approval process remains responsible for real authentication evidence.

## Operation Boundaries

Allowed operations should be conservative and evidence-backed. When evidence is missing, prefer read-only, public-safe descriptions or `unknown`.

Forbidden operations must explicitly cover unapproved writes, deletes, releases, tag changes, secret access, permission changes, customer data extraction, and private account inspection when those actions are not currently authorized by the user and evidenced by the host Runtime.

## External Writes

External writes require all of the following:

- explicit user authorization for the specific action;
- current host Runtime evidence that the action is available and scoped correctly;
- a Pal-layer owner judgement or task package when AgentPal mode is active;
- a report of what was executed and what evidence was returned.

A Business System Profile may inform the judgement, but it must not trigger a write, release, sync, issue edit, database update, ticket change, or notification by itself.

## Verification

Verification records should separate:

- `verified`: facts supported by current evidence;
- `not_run`: checks not performed;
- `missing`: evidence that is required but absent;
- `last_checked`: date or `unknown`;
- `evidence_paths`: local public-safe files or task reports when available.

Do not smooth missing evidence into a pass. Use `not-run`, `not-confirmed`, or `unknown`.

## Relationship To Organization And Project Records

Organization-level Business System records belong under:

```text
workspace/organization/capability-inventory/
```

Project-level Business System records belong under the central project record:

```text
workspace/projects/<project-id>/capability-inventory/
```

Project records may reference organization records and add project-specific availability, limitations, customer constraints, verification notes, and usage memory. Project records must not modify the central Pal roster, central contact files, or global organization facts.

## Relationship To Thin Binding

External project bindings stay thin. Installing AgentPal into another directory should create or update binding entrypoints such as:

```text
<project>/.agentpal/project.json
<project>/.agentpal/AGENTPAL.md
<project>/AGENTS.md or <project>/CLAUDE.md protected AgentPal block
```

It should not create default external-project copies of:

```text
<project>/.agentpal/capability-inventory/
<project>/.agentpal/business-systems/
<project>/.agentpal/memory/
<project>/.agentpal/state/
<project>/.agentpal/reports/
<project>/.agentpal/pals/
<project>/.agentpal/workflows/
<project>/.agentpal/evals/
```

Capability records stay in the central AgentPal Workspace unless a user explicitly approves a public-safe example or central project record update.

## Relationship To AI Judgement Routing

Business System Profiles are AI judgement inputs only. They may help a Pal decide risk, approval needs, fallback method, evidence requirements, or whether a host Runtime should be asked to perform a task.

They must not become keyword routing, deterministic domain routing, automatic Runtime selection, automatic plugin selection, or automatic external system invocation. A `system_type` such as `github`, `crm`, or `jira` is not a route.

## Examples

- Template: `templates/capability-inventory/business-system-profile-template.json`
- Public-safe examples: `examples/capability-inventory/business-system-profiles/`
- Manual guide: `docs/03-user-guides/manual-capability-profile.md`
- Relationship regression: `evals/palbench/capability-inventory/r83-project-record-relationship-boundary.md`

Example records must be synthetic or public-safe, use placeholders such as `example-org/example-repo`, and mark their source confidence as example-only.

