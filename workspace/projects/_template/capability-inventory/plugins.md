# Plugins

Use this project-level template to record plugin availability, permissions, and limitations for one bound project.

Plugin records are AI judgement inputs only. They are not automatic plugin discovery results, installers, validators, or fixed routes.

## Records

| profile_id | organization_profile_ref | plugin_name | source | confidence | last_updated | confirmed_by | status | project_available | project_limitations | verification_notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Required Field Notes

- `profile_type`: `plugin`.
- `project_scope`: describe where this plugin is available or relevant in the bound project.
- `privacy_boundary`: record only public-safe or user-approved project facts.
- `credential_policy`: do not store credentials, tokens, passwords, API keys, cookies, or secrets.
- `known_limitations`: record project-specific permission, account, runtime, input, or output limits.
- `not_run` / `not_confirmed`: record plugin operations not verified in this project.
- `usage_memory`: record project-specific successes, failures, recommendations, and `not-run` notes.
- `project_override_policy`: project records may supplement organization plugin notes without modifying central Pal contacts or global plugin facts.
- `unknown_fields`: keep unconfirmed availability, permissions, or write access as `unknown`.
