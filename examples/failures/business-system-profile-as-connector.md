# Failure Example: Treating Business System Profile as a Connector

This is a forbidden failure example. Do not copy this pattern into a real Capability Inventory profile, project record, connector, Runtime Task Package, or external project binding.

The token-like value below is a fake forbidden example value:

```text
ghp_DO_NOT_USE_EXAMPLE_TOKEN
```

It is not a real credential and must never be used.

## Bad Pattern

```text
profile_type: business-system
system_type: github
api_token: ghp_DO_NOT_USE_EXAMPLE_TOKEN
connector_enabled: true
auto_scan: true
auto_connect: true
auto_route: github -> Atlas
default_external_project_path: <project>/.agentpal/business-systems/github.md
central_roster_update:
  add_route: system_type=github -> Atlas
external_write_permission: granted
release_permission: granted
```

The bad pattern treats a governance profile as if it were executable infrastructure.

## Why This Is Wrong

It violates the Business System Profile boundary:

- no connector: a profile must not create or imply an API client, webhook, sync job, or integration program;
- no credential storage: a profile must not store tokens, passwords, API keys, cookies, private keys, session values, or secrets;
- no auto scan: AgentPal must not claim it automatically scanned GitHub or the user's machine;
- no auto execution: a profile must not write issues, comments, branches, tags, releases, secrets, settings, or permissions;
- no keyword routing: `system_type=github` must not route to Atlas, Mira, Quinn, a Runtime, a Skill, a plugin, an MCP server, or an external tool;
- thin binding: external projects must not receive `.agentpal/business-systems/` or `.agentpal/capability-inventory/` by default;
- central roster boundary: project capability records must not modify `workspace/organization/contacts/pals.json`.

## Correct Behavior

Create a governance profile only:

```text
profile_type: business-system
system_type: source-control-and-collaboration
status: not-confirmed
credential_policy: do not store credentials
access.requires_credentials: depends_on_host_runtime
routing_boundary.use_as_ai_judgement_input_only: true
routing_boundary.keyword_routing_allowed: false
external_writes.allowed_without_explicit_user_approval: false
verification.github_api_access_check: not-run
verification.required_runtime_evidence: missing
```

Wait for explicit user approval and current host Runtime evidence before any real external operation.

## Forbidden Outputs

Do not output:

- a real token, password, API key, cookie, private key, session value, or secret;
- a connector implementation;
- an API client implementation;
- a background sync job;
- an automatic scanner or validator;
- a deterministic route such as `github -> Atlas`;
- an external project `.agentpal/business-systems/` default directory;
- a central roster mutation from a project capability record;
- a claim that GitHub was scanned, connected, written to, released, tagged, or modified without current host Runtime evidence.

