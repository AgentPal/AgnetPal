# Core Gate Update Propagation Self-Test

## Status

Current for AgentPal `v0.1.0-rc.1`.

## Purpose

Verify that Codex, Claude Code, and generic CLI adapters inherit core gate updates by pointing to the same AgentPal workspace files.

## Pass Conditions

- `prompts/codex/initialize-agentpal-workspace.md` points to `core/agentpal-core-gate.md`.
- `prompts/claude-code/install-agentpal-current-project.md` points project bindings to `core/agentpal-core-gate.md`.
- `prompts/generic-cli-agent/install-agentpal-current-project.md` points project bindings to `core/agentpal-core-gate.md`.
- `templates/project-binding/prompts/install-thin-binding.md` points to core gates.
- `templates/project-binding/root-agents-agentpal-block-template.md` points to core gates.
- No adapter needs to duplicate the full Deliverable-aware Task Judgement rule to inherit changes.

## Fail Conditions

- First Pal Gate exists only in a Codex prompt.
- Claude Code or Generic CLI prompts keep an independent long copy of the rule body.
- Updating `core/deliverable-aware-task-judgement-gate.md` would require manually rewriting every adapter prompt.
