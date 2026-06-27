# Skills

Use this project-level template to record Skill availability, limits, and usage experience for one bound project.

Skill records are AI judgement inputs only. They are not automatic Skill discovery results, installers, validators, or fixed routes.

## Records

| profile_id | organization_profile_ref | skill_name | source | confidence | last_updated | confirmed_by | status | project_available | project_limitations | verification_notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Required Field Notes

- `profile_type`: `skill`.
- `project_scope`: describe where this Skill is available or relevant in the bound project.
- `privacy_boundary`: record only public-safe or user-approved project facts.
- `credential_policy`: do not store credentials, tokens, passwords, API keys, cookies, or secrets.
- `known_limitations`: record project-specific input, runtime, permission, output, or quality limits.
- `not_run` / `not_confirmed`: record Skill operations not verified in this project.
- `usage_memory`: record project-specific successes, failures, recommendations, and `not-run` notes.
- `project_override_policy`: project records may supplement organization Skill notes without modifying central Pal contacts or global Skill facts.
- `unknown_fields`: keep unconfirmed availability, permissions, or external effects as `unknown`.
