# Use With Claude Code

Claude Code is a limited project-first path for AgentPal v0.5. Full AgentPal host acceptance is not claimed.

## Start From The User Project

```text
cd <your-project>
claude
```

Then paste:

```text
prompts/claude-code/install-agentpal-current-project.md
```

The prompt asks for the local AgentPal workspace path if the path was not already provided.

## Expected Binding Surface

The prompt should create or update lightweight project files:

- `.agentpal/project.json`
- `.agentpal/AGENTPAL.md`
- protected AgentPal block in `AGENTS.md`
- protected AgentPal block in `CLAUDE.md`
- local `.claude/settings.local.json` when additional directory access is needed

`.claude/settings.local.json` is local machine configuration and should not be committed.

## What It Preserves

- The current user project remains the active task context.
- The AgentPal workspace is a reference workspace.
- Pal discovery comes from AgentPal central contacts.
- Project memory and derived records belong in the central project record, not in the external project's `.agentpal/` folder by default.

## Evidence Boundary

- Minimal Claude Code handoff evidence exists.
- `claude --bare -p` success is minimal call evidence only.
- Full host acceptance is not claimed.
- Subagent execution, external Agent execution, tool calls, and writeback require current Claude Code evidence or explicit authorization.

## Fallback Access

If Claude Code cannot read the AgentPal path after local settings are written, restart Claude Code in the project or temporarily use the host's documented additional-directory option.

## Next Links

- [Open in Claude Code](../02-getting-started/03-open-in-claude-code.md)
- [Project-first connection](04-project-first-connection.md)
- [Thin project binding](../02-concepts/thin-project-binding.md)
