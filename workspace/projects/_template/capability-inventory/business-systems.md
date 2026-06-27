# Business Systems

Use this project-level template to record external business systems that are available, limited, or relevant for one bound project.

Business System records are governance inputs only. They are not connectors, API clients, credential stores, automatic write paths, or keyword routes.

## Records

| profile_id | organization_profile_ref | system_name | system_type | source | confidence | last_updated | confirmed_by | status | project_available | project_limitations | verification_notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Required Field Notes

- `profile_type`: `business-system`.
- `project_scope`: describe the bound project, workflow, customer, or business process where this system matters.
- `privacy_boundary`: record only public-safe or user-approved operational facts.
- `credential_policy`: do not store credentials, tokens, passwords, API keys, cookies, or secrets.
- `allowed_operations`: list only confirmed operations.
- `forbidden_operations`: include unapproved external writes and any access not confirmed for this project.
- `usage_memory`: record successes, failures, recommendations, and `not-run` notes from project tasks.
- `project_override_policy`: project records may supplement organization records with project-specific constraints; they must not modify central Pal contacts or global capability facts.
- `unknown_fields`: keep access, permissions, write access, API access, and output destinations as `unknown` or empty until confirmed.
