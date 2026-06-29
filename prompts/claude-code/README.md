# Claude Code Prompts

Use these prompts when Claude Code is already running inside the target user project.

## Current Prompts

- `install-agentpal-current-project.md`: project-first AgentPal binding for Claude Code.
- `remove-agentpal-current-project.md`: project-local AgentPal binding removal.
- `verify-agentpal-current-project.md`: project-local verification prompt.

## AgentPal Workspace Path

The install prompt is copy-paste ready. Do not edit it before pasting.

When Claude Code runs the prompt, it asks for the local AgentPal Workspace path unless you already provided a clear path in the current conversation. Enter the path to your AgentPal directory, for example:

```text
<path-to-AgentPal>
```

Claude Code may also need `.claude/settings.local.json` to include the AgentPal Workspace path under `permissions.additionalDirectories`. That file is local machine configuration and should not be committed.

## Boundary

The Claude Code prompt connects an external user project to AgentPal through a thin binding. It does not make AgentPal the project, copy Pal Packs or Pal assets into the project, activate automatic Subagent Mode, create a runtime service, add scanners, add connectors, add installers, or publish remotely.

AgentPal v0.5 Deep Conductor is a no-code collaboration and mode-decision protocol. Claude Code may follow bounded task packages when evidence and permission exist, but AgentPal must not claim automatic external-Agent execution or host capability availability without current-session evidence or a manual capability profile.

R157 Agent-use protocol adds Decision Cards, Host Capability Snapshots, Skill /
Plugin Invocation Records, and Claude Code Handoff Acceptance Cards. A
successful `claude --bare -p` minimal call proves only minimal callability, not
full AgentPal host acceptance.
