# Manual GitHub Business System Profile Walkthrough

This walkthrough shows how a user-confirmed fact set can become an organization-level Business System Profile and a project-level capability record reference.

It is an example only. It does not call the GitHub API, create a connector, store credentials, scan an account, create a Release, write a tag, or route work by keyword.

## User-Confirmed Facts

Public-safe example facts:

- The user says this project may use GitHub for source hosting.
- The user confirms no GitHub token should be stored in AgentPal.
- The user confirms the example repository name can be shown as `example-org/example-repo`.
- The user has not confirmed write access.
- The user has not confirmed issue access.
- The user has not confirmed release permission.
- The user has not confirmed private repository access.
- The user has not asked AgentPal to call GitHub in this walkthrough.

## Organization Profile Draft

The organization-level profile belongs in the central AgentPal Workspace:

```text
workspace/organization/capability-inventory/business-systems/
```

Suggested public-safe organization profile shape:

```text
profile_type: business-system
profile_id: github-public-governance-example
name: GitHub Public Governance Example
system_type: source-control-and-collaboration
status: not-confirmed
source.method: user_confirmed
source.confidence: low
example_scope.repository: example-org/example-repo
access.requires_credentials: depends_on_host_runtime
credential_policy: Do not store GitHub tokens, passwords, API keys, cookies, private keys, session values, or secrets in this profile.
allowed_operations:
  - use public-safe repository facts as AI judgement input
forbidden_operations:
  - do not write issues, comments, labels, branches, commits, tags, releases, settings, or secrets without explicit user approval and current host Runtime evidence
  - do not read private repositories from this profile
routing_boundary:
  use_as_ai_judgement_input_only: true
  keyword_routing_allowed: false
```

This profile records governance boundaries only. It does not prove GitHub access exists and does not authorize any operation.

## Project Record Reference

The project-level record belongs in the central project record, not in the external project `.agentpal/` directory:

```text
workspace/projects/<project-id>/capability-inventory/business-systems.md
```

Project record reference:

```text
profile_id: project-github-governance
profile_type: business-system
organization_profile_ref: workspace/organization/capability-inventory/business-systems/github-public-governance-example
project_scope: example project using placeholder repository example-org/example-repo
project_available: unknown
project_limitations:
  - write access has not been confirmed
  - issue access has not been confirmed
  - release permission has not been confirmed
  - private repository access has not been confirmed
verification_notes:
  - no GitHub API call was made
  - no connector was configured
  - no token was stored
usage_memory:
  - not-run: no task has used this Business System profile for a real GitHub operation
project_override_policy:
  - this project record may narrow or annotate the organization profile
  - it must not modify central Pal contacts
```

Project records can add project-specific availability, limits, usage memory, and verification notes. They cannot replace the organization profile and cannot edit `workspace/organization/contacts/pals.json`.

## What Remains Unknown

- `write_access: unknown`
- `issue_access: unknown`
- `release_permission: unknown`
- `private_repository_access: unknown`
- `installed_github_app_or_cli_auth: unknown`
- `rate_limits: unknown`
- `output_destinations: unknown`

Unknown means the fact is not confirmed. Do not infer access from the word GitHub or from the repository placeholder.

## What Is Not-Run

- `github_api_access_check: not-run`
- `issue_permission_check: not-run`
- `release_permission_check: not-run`
- `tag_write_check: not-run`
- `secret_access_check: not-run`
- `connector_setup_check: not-run`

Not-run means the check did not execute. It is neither pass nor fail.

## What Is Missing

To use GitHub for a real task, the following evidence is missing:

- explicit user approval for the specific operation;
- current host Runtime evidence for repository visibility;
- current host Runtime evidence for the requested permission;
- a task-specific approval boundary for any external write;
- verification output after the host Runtime performs the approved action.

Missing means required evidence is absent. Report it honestly instead of smoothing it into a pass.

## Thin Binding Reminder

The external project keeps only thin binding files such as:

```text
<project>/.agentpal/project.json
<project>/.agentpal/AGENTPAL.md
<project>/AGENTS.md protected AgentPal block
<project>/CLAUDE.md protected AgentPal block
<project>/.claude/settings.local.json
```

Do not create these by default:

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

## What Must Not Happen

- Do not store a GitHub token in a profile.
- Do not automatically connect to GitHub.
- Do not create a connector or API client.
- Do not create `.agentpal/business-systems/` in the external project by default.
- Do not route to a Pal because `system_type` mentions GitHub.
- Do not edit central Pal contacts from a project capability record.
- Do not claim a scan, write, Release, tag, issue edit, or repository mutation happened without current host Runtime evidence.

