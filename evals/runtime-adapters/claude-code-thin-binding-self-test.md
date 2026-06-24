# Claude Code Thin Binding Self-Test

## Status

Current for AgentPal `v0.1.0-rc.1`.

## Purpose

Verify that Claude Code project binding remains thin while still granting access to the AgentPal workspace.

## Pass Conditions

- `CLAUDE.md` contains one thin AgentPal protected block.
- `AGENTS.md` contains one thin AgentPal protected block.
- `.claude/settings.local.json` contains `permissions.additionalDirectories` with the AgentPal workspace root.
- `.gitignore` excludes `.claude/settings.local.json`.
- `.agentpal/project.json` points to core gates.
- `.agentpal/AGENTPAL.md` is a thin pointer.
- No full protocols or Pal assets are copied into `.agentpal/`.

## Fail Conditions

- Claude Code binding has no AgentPal workspace access path.
- `CLAUDE.md` embeds a full copy of AgentPal rules.
- `.agentpal/` contains copied full Pal Packs.
