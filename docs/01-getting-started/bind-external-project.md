# Bind An External Project

Use thin binding when you want an external project to use AgentPal.

The external project stays the current project. The AgentPal workspace is only a Pal source and routing reference.

## What To Add

The normal project-side binding surface is small:

- `.agentpal/project.json`
- `.agentpal/AGENTPAL.md`
- protected AgentPal block in `AGENTS.md`
- for Claude Code, protected AgentPal block in `CLAUDE.md`
- for Claude Code, local `.claude/settings.local.json` plus a `.gitignore` entry when needed

Use the current templates:

- `templates/project-binding/generic-codex/`
- `templates/project-binding/claude-code/`

## Roots To Keep Separate

- `active_project_root`: the external user project
- `agentpal_workspace_root`: the central AgentPal workspace
- `agentpal_project_record`: the central record under `workspace/projects/<project-id>/`

When the user says "this project" in a bound project, answer about `active_project_root`, not about the AgentPal workspace.

## What Not To Copy

Do not copy these into the external project's `.agentpal/` folder by default:

- Pal Packs
- central contacts
- docs
- evals
- release files
- memory
- reports
- source maps
- derived knowledge
- governance records
- capability inventory
- Org Packs, FDE Packs, or Delivery Packs

Those records belong in the AgentPal workspace, usually under `workspace/projects/<project-id>/`, after an explicit task and privacy check.

## Why Thin Binding Exists

Thin binding prevents the user project from becoming a clone of AgentPal. It keeps the project easy to remove, keeps private project facts out of public Pal assets, and lets Mira and specialist Pals read central contacts without polluting the user's repository.

## Current Limits

- External project writeback is not generally validated.
- Host capability must be reported from visible evidence, a manual profile, or runtime-reported capability.
- AgentPal does not scan the machine for projects or tools by itself.

## Next Links

- [Project-first connection](../04-runtime-guides/04-project-first-connection.md)
- [Thin project binding](../02-concepts/thin-project-binding.md)
- [Use with Claude Code](../04-runtime-guides/02-use-with-claude-code.md)
- [Use with Generic CLI Agent](../04-runtime-guides/03-use-with-generic-cli-agent.md)
