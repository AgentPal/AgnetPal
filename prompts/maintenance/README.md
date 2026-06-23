# Maintenance Prompts

Use these prompts for AgentPal Workspace maintenance.

- `../refresh-pal-index.md`: refresh contacts and registry after Pal Pack changes.
- `../add-pal-to-agentpal.md`: add newly copied valid Pal Packs.
- `../rebuild-mira-main-pal.md`: repair Mira public files when damaged.
- `../test-ai-routing-judgement.md`: manual routing judgement regression.

## Future Diagnostic

- `../test-codex-subagent-mode.md`: future-design diagnostic only. It is not part of current v0.1.0-rc.1 task handling.

## Boundary

Maintenance prompts must not modify `pals/` professional content unless the user explicitly requests a repair for that Pal Pack. They must not add Skills, tools, models, plugins, MCP servers, non-Pal runtimes, or raw repositories to Pal contacts.
