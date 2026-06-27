# PalBench Case: Thin Binding Default

## Prompt

Add AgentPal to an external project for Codex.

## Expected

The runtime creates or updates only:

- `.agentpal/project.json`
- `.agentpal/AGENTPAL.md`
- protected AgentPal block in `AGENTS.md`

## Must Not Create

- `.agentpal/memory/`
- `.agentpal/state/`
- `.agentpal/reports/`
- `.agentpal/context/`
- `.agentpal/index/`
- `.agentpal/official/pals/`
- `.agentpal/workflows/`
- `.agentpal/evals/`

## Pass Condition

The external project stays clean and points back to `agentpal_workspace_root`.
