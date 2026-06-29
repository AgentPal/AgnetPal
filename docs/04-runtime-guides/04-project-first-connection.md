# Project-First Connection

Project-first means the user's real project directory is the task context, while AgentPal is only the Pal workspace reference.

## Why This Matters

In a bound project:

- `active_project_root` is the external user project
- `agentpal_workspace_root` is the AgentPal workspace
- `agentpal_project_record` is the central record under `workspace/projects/<project-id>/`

When the user says "this project", answer about the external project. Do not treat the AgentPal workspace as the user's project.

## Claude Code Path

```text
cd <your-project>
claude
```

Then paste:

```text
prompts/claude-code/install-agentpal-current-project.md
```

Claude Code support is limited/minimal handoff, not full host acceptance.

## Generic CLI Path

```text
cd <your-project>
<your-cli-agent>
```

Then paste:

```text
prompts/generic-cli-agent/install-agentpal-current-project.md
```

Generic CLI support is a compatibility path, not a broad validation claim.

## Thin Binding Rule

The project-side `.agentpal/` folder should contain only lightweight binding files by default. It should not contain thick AgentPal workspace material such as:

- `.agentpal/pals/`
- `.agentpal/memory/`
- `.agentpal/reports/`
- `.agentpal/docs/`
- `.agentpal/evals/`
- `.agentpal/release/`
- `.agentpal/org-pack/`
- `.agentpal/fde-pack/`
- `.agentpal/delivery-pack/`

## Writeback Boundary

Project facts, derived knowledge, task records, reports, governance notes, and capability inventory should go to the central project record only after an explicit task and privacy check.

Customer-private data must not be written into public examples, Pal Packs, or global knowledge.

## Next Links

- [Bind an external project](../01-getting-started/bind-external-project.md)
- [Use with Claude Code](02-use-with-claude-code.md)
- [Use with Generic CLI Agent](03-use-with-generic-cli-agent.md)
