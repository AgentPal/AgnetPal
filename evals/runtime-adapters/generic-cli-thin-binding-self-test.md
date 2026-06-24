# Generic CLI Thin Binding Self-Test

## Status

Current for AgentPal `v0.1.0-rc.1`.

## Purpose

Verify that generic CLI project binding uses the shared core gates without Claude-specific files.

## Pass Conditions

- `AGENTS.md` contains one thin AgentPal protected block.
- `.agentpal/project.json` points to core gates.
- `.agentpal/AGENTPAL.md` is a thin pointer.
- No `.claude/settings.local.json` is created for generic CLI binding.
- No full protocols, Pal assets, docs, examples, evals, or release files are copied into `.agentpal/`.

## Fail Conditions

- Generic CLI binding creates Claude-specific settings.
- Generic CLI binding embeds a full copy of AgentPal rules.
- Generic CLI binding stores a copied Pal list as source of truth.
