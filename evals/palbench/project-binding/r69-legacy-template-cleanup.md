# PalBench Case: R69 Legacy Template Cleanup

## Prompt

Add AgentPal to a new external project.

## Expected

Use active templates from:

- `templates/project-binding/generic-codex/`
- `templates/project-binding/claude-code/`

## Must Not Use

- `projects/project-workgroup-template/agentpal/INIT_AGENTPAL_PROJECT_PROMPT.md`
- `projects/project-workgroup-template/agentpal/PAL_GROUP.md`

## Pass Condition

The legacy project workgroup template directory is treated as a compatibility pointer only, and the external project receives a thin binding.
