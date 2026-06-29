# Use With Generic CLI Agent

Generic CLI Agent support is a compatibility path, not a full host acceptance claim.

Use this path only when the CLI agent can read local files, follow Markdown / JSON instructions, keep project context stable, and report real execution evidence.

## Start From The User Project

```text
cd <your-project>
<your-cli-agent>
```

Then paste:

```text
prompts/generic-cli-agent/install-agentpal-current-project.md
```

The prompt asks for the local AgentPal workspace path if the path was not already provided.

## Expected Binding Surface

The generic path should create or update:

- `.agentpal/project.json`
- `.agentpal/AGENTPAL.md`
- protected AgentPal block in `AGENTS.md`

It should not create Claude-specific files unless the user explicitly asks or the project already requires them.

## Required Host Behavior

The CLI agent must be able to:

- keep the current project as `active_project_root`
- treat AgentPal as `agentpal_workspace_root`
- read central contacts when Pal discovery is needed
- avoid copying Pal Packs, docs, evals, memory, reports, or release files into the project
- separate known, unknown, and unavailable capability
- provide evidence for any file write, command, tool call, or external action

## Current Limits

- Broad Generic CLI host acceptance is not claimed.
- Runtime-specific slash commands may not exist.
- Tool, plugin, model, MCP, or Skill capability must come from the current host, not from AgentPal assumption.
- Deep Conductor remains a no-code decision protocol unless the host separately provides execution capability.

## Next Links

- [Runtime compatibility](00-runtime-compatibility.md)
- [Project-first connection](04-project-first-connection.md)
- [Thin project binding](../02-concepts/thin-project-binding.md)
