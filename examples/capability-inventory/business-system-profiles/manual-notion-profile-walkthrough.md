# Manual Notion Business System Profile Walkthrough

This walkthrough shows how to record a non-code Business System profile when the user only confirms that Notion may be used for project documentation or content planning.

It is a public-safe example. It does not connect to Notion, store credentials, inspect a workspace, verify access, create a connector, create an API client, scan accounts, write pages, or route tasks by keyword.

## User-Confirmed Facts

Example user statement:

```text
We may use Notion to store project docs or content plans.
```

Confirmed facts:

- system family: Notion
- possible use: project documentation or content planning
- confirmation source: user statement

Not confirmed:

- workspace access
- database access
- page access
- write permission
- API access
- integration status
- workspace ID
- user role
- admin permission
- export permission
- billing plan capability
- token or integration secret

## Organization Profile Draft

Save public-safe organization-level notes under:

```text
workspace/organization/capability-inventory/business-systems/
```

Suggested draft file name:

```text
workspace/organization/capability-inventory/business-systems/notion-public-governance-profile.md
```

The draft should record only confirmed facts and conservative boundaries:

```text
profile_type: business-system
system_name: Notion
system_type: workspace-docs
status: not-confirmed
source.method: user_confirmed
availability: unknown
workspace_access: unknown
database_access: unknown
write_access: unknown
api_access: unknown
permission_check: not-run
verification_evidence: missing
credential_policy: do not store credentials, tokens, cookies, or secrets
routing_boundary: AI judgement input only; no keyword routing
```

Do not mark Notion as available, writable, connected, scanned, or verified unless current evidence proves it.

## Project Record Reference

For a bound external project, save project-specific references only in the central AgentPal project record:

```text
workspace/projects/<project-id>/capability-inventory/business-systems.md
```

Example project note:

```text
## Notion

organization_profile_ref: workspace/organization/capability-inventory/business-systems/notion-public-governance-profile.md
project_scope: possible project documentation or content planning
project_available: unknown
project_write_access: unknown
project_api_access: unknown
verification_notes: not-run
missing_evidence:
- user confirmation of workspace access
- screenshot, export, admin setting, or host Runtime evidence
- explicit approval for any external write
```

The external user project should remain thin-bound. Do not create:

```text
<project>/.agentpal/business-systems/
<project>/.agentpal/capability-inventory/
```

## Unknown Fields

Keep these as `unknown` until confirmed:

- availability
- workspace access
- database access
- page read access
- page write access
- API access
- integration status
- workspace ID
- user role
- admin permission
- export permission
- billing or plan capability
- business workflow ownership

Unknown does not mean false. Unknown also does not mean available.

## Not-Run Checks

Mark these as `not-run` unless the current host Runtime actually provides evidence:

- Notion workspace access check
- Notion database access check
- Notion page read check
- Notion page write check
- Notion API availability check
- integration permission check
- export permission check
- admin role check
- billing or plan capability check

Not-run does not mean pass.

## Missing Evidence

Evidence is missing until the user or host Runtime provides it.

Acceptable evidence may include:

- user confirmation of workspace access
- host Runtime evidence from a user-approved action
- screenshot or UI confirmation provided by the user
- exported report
- documented admin setting
- task report showing the exact approved check and result

Missing evidence is not acceptable completion for an access, write, or API claim.

## Correct Next Step

Ask the user for the smallest needed confirmation, or ask the host Runtime to perform a user-approved check and report evidence.

Example:

```text
Please confirm whether this AgentPal organization should record Notion as a possible documentation system only, or whether you want the host Runtime to verify workspace access in a separate approved task.
```

If no evidence is provided, keep access, permission, and API fields as `unknown`, checks as `not-run`, and evidence as `missing`.

## Forbidden Behavior

Do not:

- connect to Notion from this profile
- store a Notion token, integration secret, password, API key, cookie, session value, or private secret
- claim workspace, database, page, write, export, admin, or API access without evidence
- create a connector, API client, scanner, validator, background sync job, or automatic execution path
- default to writing business-system records into an external project's `.agentpal/` directory
- create external project `.agentpal/business-systems/` or `.agentpal/capability-inventory/` by default
- route to a Pal, Runtime, Skill, plugin, MCP server, or external tool based on `notion`, `workspace-docs`, or `system_type`
- modify `workspace/organization/contacts/pals.json` from a project capability record

Business System Profile remains AI judgement input only.
