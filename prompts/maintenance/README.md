# Maintenance Prompts

Use these prompts for AgentPal Workspace maintenance.

- `../refresh-pal-index.md`: refresh central Pal roster records after Pal Pack changes.
- `../add-pal-to-agentpal.md`: add newly copied valid Pal Packs.
- `../rebuild-mira-main-pal.md`: repair Mira public files when damaged.
- `../test-ai-routing-judgement.md`: manual routing judgement regression.

Run Pal registration and index refresh prompts from the AgentPal Workspace:

- Codex: open AgentPal as its own Codex project, then paste the prompt into the AgentPal project conversation.
- Claude Code: `cd <path-to-AgentPal>`, run `claude`, then paste the prompt.
- Generic CLI Agent: `cd <path-to-AgentPal>`, start the CLI agent, then paste the prompt.

Do not rely on an external project session restart to register a newly copied Pal Pack. Restarting can reload the current index, but registration is the maintenance action that updates `workspace/organization/contacts/`.

## Future Diagnostic

- `../test-codex-subagent-mode.md`: diagnostic only. It is not evidence that AgentPal can automatically execute subagents or external Agents in current task handling.

## Boundary

Maintenance prompts must not modify `official/pals/` professional content unless the user explicitly requests a repair for that Pal Pack. They must not add Skills, tools, models, plugins, MCP servers, non-Pal runtimes, or raw repositories to Pal contacts.

Maintenance prompts must not run `git push`, `git pull`, `git fetch`, create tags, create GitHub Releases, call GitHub publication APIs, add scanners, add daemons, add installers, add connectors, create runtime services, or claim host capability availability without explicit current-session evidence and authorization.
