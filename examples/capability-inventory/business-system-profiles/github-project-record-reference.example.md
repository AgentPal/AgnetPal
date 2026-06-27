# GitHub Project Record Reference Example

This example shows a project-level reference to an organization Business System Profile.

It is a public-safe Markdown example. It is not a GitHub connector, API client, credential, scan result, release action, or automatic route.

## Save Location

Save real project-level records under the central AgentPal Workspace:

```text
workspace/projects/<project-id>/capability-inventory/business-systems.md
```

Do not save them under:

```text
<project>/.agentpal/business-systems/
<project>/.agentpal/capability-inventory/
```

## Example Record

```text
profile_id: project-github-governance
profile_type: business-system
organization_profile_ref: workspace/organization/capability-inventory/business-systems/github-public-governance-example
project_scope: placeholder project using example-org/example-repo
source: user_confirmed
confidence: low
last_updated: unknown
confirmed_by: example user
status: not-confirmed
project_available: unknown
project_limitations:
  - repository visibility has not been verified by a host Runtime
  - issue access is unknown
  - write access is unknown
  - release permission is unknown
privacy_boundary:
  - use only public-safe placeholder repository names
  - do not store private repository names or customer data
credential_policy:
  - do not store tokens, passwords, API keys, cookies, private keys, session values, or secrets
verification_notes:
  - github_api_access_check: not-run
  - release_permission_check: not-run
  - required_runtime_evidence: missing
usage_memory:
  - not-run: no real GitHub task has used this profile yet
project_override_policy:
  - project record can narrow or annotate the organization profile
  - project record must not modify workspace/organization/contacts/pals.json
unknown_fields:
  - write_access
  - issue_access
  - release_permission
  - private_repository_access
  - installed_github_app_or_cli_auth
```

## Interpretation

- `unknown` fields are unconfirmed and must not be treated as available.
- `not-run` checks have not executed and must not be reported as pass.
- `missing` evidence must be reported before a real external write can happen.
- `organization_profile_ref` is a reference, not a copy of credentials or permissions.
- `system_type` is not a route to a Pal, Runtime, Skill, plugin, MCP server, or external tool.

