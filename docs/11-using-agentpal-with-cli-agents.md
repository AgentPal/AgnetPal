# Using AgentPal With Generic CLI Agents

This guide is for Markdown/JSON-capable CLI Agents such as CodeWhale, Gemini CLI, or similar runtimes.

## Recommended Workflow

```text
cd <your-project>
<your-cli-agent>
```

Then paste:

```text
Please connect AgentPal to the current project.
AGENTPAL_HOME = <path-to-AgentPal>
```

Or paste the full prompt from:

```text
prompts/cli-agent/install-agentpal-current-project.md
```

## What The Prompt Does

The generic one-prompt install creates or updates:

- `.agentpal/`
- `AGENTS.md`

It does not depend on Claude Code `.claude/settings.local.json`.

It does not create `CLAUDE.md` unless Claude Code is detected or the user explicitly asks.

Runtime-specific files such as `GEMINI.md` or `CODEWHALE.md` may be added in the future or created only when a project already uses that standard.

## Runtime Boundary

AgentPal v0.1.0-rc.1 uses Simple Pal Mode only.

AgentPal is a Pal layer, not an Agent runtime, not a multi-agent runtime, and not an execution layer.

The host CLI Agent reads and writes files, runs commands, or calls tools. AgentPal provides Pal identity, routing, context, output contracts, and asset loading rules.

## Context Boundary

The project binding is lightweight:

- `.agentpal/project.json` records the current project root and AgentPal workspace root
- `AGENTS.md` contains a protected AgentPal block
- contacts / registry are used for Pal discovery
- selected Pal assets are loaded on demand

Do not copy all Pal Packs into the project.

Do not import the whole AgentPal workspace into the project instruction file.

Project questions mean `<your-project>`, not the AgentPal workspace.
