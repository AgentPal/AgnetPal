# Project Workgroup

AgentPal can be bound to an external user project through a `.agentpal/` folder and a protected AgentPal block in the external project root `AGENTS.md`.

## Current Boundary

Project means external user project by default, not the AgentPal Workspace itself.

In an external project-bound session:

- `active_project_root` is the external user project.
- `agentpal_workspace_root` is only a Pal source and routing reference.
- "project", "this project", and "current project" mean the external project.
- The external project's `.agentpal/` folder is a binding layer, not the full Pal asset store.

## Pal Discovery

For Pal discovery, direct Pal calls, owner routing, and selected Pal asset loading, the runtime may read bounded contacts, registry, and selected Pal files from `agentpal_workspace_root`.

This does not make the AgentPal Workspace a second current project.

## Remove Workgroup

Removing an AgentPal workgroup should remove only the AgentPal binding files and protected block. It must not delete user project source, `.git`, package files, user-authored `AGENTS.md` content, or the AgentPal Workspace.

## Related

- [Collaboration overview](00-collaboration-overview.md)
- [Repository map](../00-overview/02-repository-map.md)
- [Public/private boundary](../03-pal-pack-standard/11-public-private-boundary.md)
