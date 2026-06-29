# Open In Claude Code

Claude Code is documented as a limited project-first path for AgentPal v0.5. Full AgentPal host acceptance is not claimed.

Use this when you want Claude Code to work in an external project while reading AgentPal as a Pal workspace reference.

## Project-First Path

Start in the real user project:

```text
cd <your-project>
claude
```

Then paste the prompt from:

```text
prompts/claude-code/install-agentpal-current-project.md
```

The prompt is intended to be copy-paste ready. It asks for your local AgentPal workspace path unless you already provided one clearly.

## What The Prompt Should Do

The project connection should create or update only lightweight binding surfaces:

- `.agentpal/project.json`
- `.agentpal/AGENTPAL.md`
- protected AgentPal block in `AGENTS.md`
- protected AgentPal block in `CLAUDE.md`
- local `.claude/settings.local.json` when Claude Code needs an additional readable directory

The external project remains the active project. AgentPal remains a reference workspace.

## What It Must Not Do

It must not copy AgentPal Pal Packs, docs, evals, release files, memory, reports, internal task records, or central roster files into the external project.

It must not claim Claude Code can run every AgentPal behavior unless that behavior has current evidence from the actual Claude Code session.

## Current Evidence Boundary

- Minimal Claude Code handoff evidence exists.
- Full host acceptance is not claimed.
- `claude --bare -p` style success is only minimal call evidence.
- Subagent execution, external Agent execution, MCP/plugin calls, and tool actions require current Claude Code evidence or explicit user authorization.

## Next Links

- [Claude Code runtime guide](../04-runtime-guides/02-use-with-claude-code.md)
- [Project-first connection](../04-runtime-guides/04-project-first-connection.md)
- [Thin project binding](../02-concepts/thin-project-binding.md)
