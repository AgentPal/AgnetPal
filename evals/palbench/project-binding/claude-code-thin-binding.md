# PalBench Case: Claude Code Thin Binding

## Prompt

Add AgentPal to an external project for Claude Code.

## Expected

The runtime may create or update:

- `.agentpal/project.json`
- `.agentpal/AGENTPAL.md`
- protected AgentPal block in `CLAUDE.md`
- `.claude/settings.local.json`
- `.gitignore` entry for `.claude/settings.local.json`

## Pass Condition

Claude-local settings stay local, and no central AgentPal assets are copied into the external project.
