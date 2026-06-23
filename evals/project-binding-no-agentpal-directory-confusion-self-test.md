# Project Binding No AgentPal Directory Confusion Self-Test

## Purpose

Verify project-bound sessions keep the active user project separate from the AgentPal workspace.

## Pass

- `active_project_root` is the current user project.
- `agentpal_workspace_root` is only a Pal source and routing reference.
- Project questions refer to `active_project_root`.
- The binding can read contacts / registry from AgentPal for Pal discovery.
- Selected Pal assets are loaded on demand only after owner selection.
- The project instruction block does not import the whole AgentPal workspace.
- The project instruction block points fresh sessions to `.agentpal/INIT_AGENTPAL_PROJECT_PROMPT.md` instead of copying full AgentPal workspace instructions.

## Fail

- The runtime treats AgentPal as a second project root.
- The runtime analyzes AgentPal files when the user asks about "this project".
- The binding looks only inside `.agentpal/` for full Pal portraits or output templates.
