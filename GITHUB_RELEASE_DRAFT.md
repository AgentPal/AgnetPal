# AgentPal v0.1.0-rc.1

AgentPal v0.1.0-rc.1 is the first public release candidate for AgentPal as a Pal layer and Pal Pack Standard practice for Markdown/JSON-capable agent runtimes.

AgentPal is not an Agent layer, not a multi-agent runtime, and not an execution layer. It gives an existing runtime a structured Pal Workspace for identity, knowledge, skills, context, memory boundaries, output contracts, coordination rules, review habits, summaries, and learning storage.

## What's Included

- AgentPal Workspace root files for initialization and release-safe navigation.
- Simple Pal Mode as the only active task-handling path in v0.1.0-rc.1.
- Mira as the default Main Pal, Leader Pal, Conductor, and secretary-style coordinator.
- Fast Route as the current clear-task handoff pattern, with Deep Conductor documented as future complex-workflow design only.
- R33 small-sample PalBench smoke validation showing initial evidence for clearer task packages, stronger verification awareness, lower file-scope context risk, and lower user routing burden.
- Official bundled Pal Packs: Mira, Atlas, Vega, Rhea, Quinn, Morgan, Harper, and Nova.
- Contacts and registry files as the source of truth for Pal discovery and `/pal Name` direct calls.
- Runtime Response Gate, AI routing judgement, Pal context slicing, asset loading budget, memory summary loading, and Task Package output contract protocols.
- Orchestration methodology research docs, Fugu-inspired method transfer notes, PalBench design, and future-oriented capability / context / isolation / shared-memory / routing-memory protocols.
- External project workgroup templates for binding AgentPal to a user project.
- Claude Code one-prompt project install using `.agentpal/`, `CLAUDE.md`, `AGENTS.md`, and `.claude/settings.local.json`.
- Generic CLI Agent one-prompt project install using `.agentpal/` and `AGENTS.md`.
- MIT License, contribution guide, release notes, checklist, resource index, and third-party notices.

## Current Status

- Release type: release candidate.
- Version: v0.1.0-rc.1.
- Runtime path: Simple Pal Mode only.
- Primary use: opening the AgentPal Workspace in Codex, Claude Code, or another runtime that can read Markdown and JSON.
- Required dependencies: none for AgentPal initialization.

## Known Limitations

- AgentPal does not include a desktop app, web UI, CLI, daemon, scanner, validator, installer, or service.
- AgentPal does not execute filesystem, system, publishing, account, or automation actions by itself; the host runtime performs execution and must provide evidence.
- Future subagent, remote agent, MCP-hosted agent, marketplace, and deep runtime-adapter designs are not active in v0.1.0-rc.1.
- Capability Inventory, Context Access List, Workflow Topology, Routing Reward Memory, PalBench, and Deep Conductor materials are design foundations only in v0.1.0-rc.1.
- Context Access List, Pal Isolation, Shared Memory, Routing Reward Memory, and PalBench now include R32 boundary-focused protocol/eval examples.
- The R33 PalBench report is small-sample smoke evidence only. It is not statistically significant and does not compare foundation models.
- Pal Packs are working assets for a runtime, not independent agent processes.
- Exact token metering is not provided in v0.1.0-rc.1; the workspace instead defines context budgets and asset loading reports.

## Getting Started

1. Download or clone the AgentPal Workspace.
2. Open the AgentPal directory in Codex, Claude Code, or another Markdown/JSON-capable agent runtime.
3. Paste or run `INIT_PROMPT.md`.
4. Start ordinary messages with Mira.
5. Use `/pal Name` to call a registered Pal directly, for example `/pal Harper`.

For Claude Code project-local setup:

```text
cd <your-project>
claude
```

Then paste `prompts/claude-code/install-agentpal-current-project.md` and provide `<path-to-AgentPal>`. The prompt updates `.claude/settings.local.json` `permissions.additionalDirectories`; `--add-dir` is a fallback / advanced option, not the required default.

For generic CLI Agents, paste `prompts/cli-agent/install-agentpal-current-project.md` inside `<your-project>`.

## Safety Notes

- Do not publish runtime-private memory, private state, real reports, customer data, internal development notes, secrets, tokens, credentials, or local absolute paths.
- Treat `contacts/` and `registry/` as the source of truth for Pal discovery.
- Keep future designs clearly marked as future, not active v0.1.0-rc.1 behavior.
- Use synthetic or placeholder data in public examples and templates.

## License

MIT License. See `LICENSE`.
