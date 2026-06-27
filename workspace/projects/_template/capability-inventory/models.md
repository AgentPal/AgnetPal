# Models

Use this project-level template to record model availability, limits, or usage experience for one bound project.

Model records are AI judgement inputs only. They are not automatic model discovery results, benchmark certificates, or deterministic routes.

## Records

| profile_id | organization_profile_ref | model_name | source | confidence | last_updated | confirmed_by | status | project_available | project_limitations | verification_notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Required Field Notes

- `profile_type`: `model`.
- `project_scope`: describe where this model is available or relevant in the bound project.
- `privacy_boundary`: do not record private prompts, customer data, or unrelated project memory unless explicitly approved.
- `credential_policy`: do not store credentials, tokens, passwords, API keys, cookies, or secrets.
- `known_limitations`: record project-specific context, quality, cost, availability, or policy limits.
- `not_run` / `not_confirmed`: record controls, access, or behavior that were not verified.
- `usage_memory`: record project-specific successes, failures, recommendations, and `not-run` notes.
- `project_override_policy`: project records may supplement organization model notes without changing central Pal contacts, model standards, or global facts.
- `unknown_fields`: keep unconfirmed access, cost, limits, or routing suitability as `unknown`.
