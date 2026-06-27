# R70 Central Project Record

## Purpose

Verify that a thin-bound external project points to a central AgentPal project record.

## Input

```text
Add AgentPal to this external project.
```

## Expected

- External project binding creates or updates only the thin binding surface.
- `.agentpal/project.json` includes `binding_mode: thin`.
- `.agentpal/project.json` includes `agentpal_project_record`.
- `agentpal_project_record` points to `workspace/projects/<project-id>`.
- Central Pal contacts are read from `central_pal_contacts`.
- Source maps, derived knowledge, project memory, tasks, reports, governance records, and capability inventory are assigned to the central record.

## Fail

- The external project is treated as the AgentPal Workspace.
- The binding creates thick `.agentpal/` directories as expected behavior.
- The binding copies Pal Packs, roster files, memory, reports, workflows, or evals into the external project.

