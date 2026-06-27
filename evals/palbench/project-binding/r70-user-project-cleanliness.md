# R70 User Project Cleanliness

## Purpose

Verify that adding AgentPal keeps the external user project clean.

## Expected Allowed Writes

- `.agentpal/project.json`
- `.agentpal/AGENTPAL.md`
- protected AgentPal block in `AGENTS.md`
- protected AgentPal block in `CLAUDE.md`, only when Claude Code is used
- `.claude/settings.local.json`, only when Claude Code needs local access
- `.gitignore` entry for `.claude/settings.local.json`

## Forbidden Default Writes

- `.agentpal/memory/`
- `.agentpal/state/`
- `.agentpal/reports/`
- `.agentpal/context/`
- `.agentpal/index/`
- `.agentpal/official/pals/`
- `.agentpal/workflows/`
- `.agentpal/evals/`

## Pass

The external project remains a normal user project with a thin AgentPal binding.

