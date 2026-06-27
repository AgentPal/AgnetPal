# MCP

Use this project-level template to record MCP server availability, tools, resources, and limitations for one bound project.

MCP records are AI judgement inputs only. They are not automatic MCP discovery results, installers, validators, or fixed routes.

## Records

| profile_id | organization_profile_ref | mcp_server | source | confidence | last_updated | confirmed_by | status | project_available | project_limitations | verification_notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |

## Required Field Notes

- `profile_type`: `mcp`.
- `project_scope`: describe where this MCP server is available or relevant in the bound project.
- `privacy_boundary`: record only public-safe or user-approved project facts.
- `credential_policy`: do not store credentials, tokens, passwords, API keys, cookies, or secrets.
- `known_limitations`: record project-specific tool, resource, permission, runtime, input, or output limits.
- `not_run` / `not_confirmed`: record tools or resources not verified in this project.
- `usage_memory`: record project-specific successes, failures, recommendations, and `not-run` notes.
- `project_override_policy`: project records may supplement organization MCP notes without modifying central Pal contacts or global MCP facts.
- `unknown_fields`: keep unconfirmed availability, permissions, tools, resources, or write access as `unknown`.
