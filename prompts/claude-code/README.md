# Claude Code Prompts

Use these prompts when Claude Code is already running inside the target user project.

## Current Prompts

- `install-agentpal-current-project.md`: project-first AgentPal binding for Claude Code.
- `remove-agentpal-current-project.md`: project-local AgentPal binding removal.
- `verify-agentpal-current-project.md`: project-local verification prompt.

## AGENTPAL_HOME

Before pasting the install prompt, replace this line:

```text
AGENTPAL_HOME = <replace-with-your-AgentPal-path>
```

with the real AgentPal Workspace path for your machine, for example:

```text
AGENTPAL_HOME = D:/Tools/AgentPal
AGENTPAL_HOME = /Users/you/AgentPal
```

Claude Code may also need `.claude/settings.local.json` to include the AgentPal Workspace path under `permissions.additionalDirectories`. That file is local machine configuration and should not be committed.

## Boundary

The Claude Code prompt connects an external user project to AgentPal. It does not make AgentPal the project, copy all Pal Packs into the project, activate Subagent Mode, or create a runtime service.
