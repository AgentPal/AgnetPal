# Runtimes

Use this project-level template to record host Runtime availability, permissions, and limitations for one bound project.

Runtime records are evidence notes only. They are not automatic scans, installers, validators, or execution engines.

## Records

| profile_id | organization_profile_ref | runtime_name | source | confidence | last_updated | confirmed_by | status | project_available | project_limitations | verification_notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Required Field Notes

- `profile_type`: `runtime`.
- `project_scope`: describe the bound project, shell, workspace, or host session where the Runtime facts apply.
- `privacy_boundary`: record only project-approved Runtime facts.
- `credential_policy`: do not store credentials, tokens, passwords, API keys, cookies, or secrets.
- `known_limitations`: record project-specific file, command, tool, sandbox, or approval limits.
- `not_run` / `not_confirmed`: record permissions or tools that were not verified.
- `usage_memory`: record project-specific successes, failures, recommendations, and `not-run` notes.
- `project_override_policy`: project records may supplement organization Runtime notes without modifying central Pal contacts or global Runtime facts.
- `unknown_fields`: keep unconfirmed read, write, command, network, tool, or external directory access as `unknown`.
