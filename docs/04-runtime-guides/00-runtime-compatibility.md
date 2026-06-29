# Runtime Compatibility

AgentPal v0.5 is a Pal layer, not an execution layer.

Compatibility means a host runtime can read the AgentPal workspace, follow Markdown / JSON instructions, preserve project context, and report execution evidence honestly. It does not mean AgentPal provides a native plugin, connector, daemon, scanner, marketplace, app runtime, or automatic multi-Agent engine.

## Current Host Status

| Host / mode | v0.5 status | What to claim |
| --- | --- | --- |
| Codex | Codex-first verified | Current primary path for AgentPal initialization and real host confirmation |
| Claude Code | limited/minimal handoff | Usable project-first guidance exists; full host acceptance is not claimed |
| Generic CLI Agent | compatibility path | Prompt-based path exists for capable CLI agents; broad host acceptance is not claimed |
| OpenCode / Gemini | unavailable in current evidence | Do not claim current support |
| DeepSeek | experimental/version-help only | Do not claim stable host support |
| Plan Mode UI | unavailable in current UI evidence | Do not claim UI-verified support |
| Goal Mode | limited | Use only where current evidence supports it |

## What A Compatible Runtime Must Do

A compatible host should be able to:

- read local Markdown and JSON files
- keep `active_project_root` separate from `agentpal_workspace_root`
- follow Mira-first and `/pal Name` instructions
- load bounded Pal context instead of the whole repository
- distinguish known, unknown, and unavailable capability
- report real execution evidence before claiming actions
- preserve privacy and writeback boundaries

## Capability Evidence

Host capability may come from:

- visible current runtime evidence
- a user-maintained manual capability profile
- a runtime-reported profile or explicit tool list

AgentPal must not invent a runtime scan. If capability is unknown, say it is unknown.

## Common Boundary

- AgentPal is not a deep plugin for every host.
- AgentPal does not guarantee identical behavior across runtimes.
- Deep Conductor is a no-code collaboration and mode-decision protocol, not automatic runtime execution.
- Subagent execution, external Agent execution, tool calls, model calls, and file writes require host capability and current evidence.

## Next Links

- [Use with Codex](01-use-with-codex.md)
- [Use with Claude Code](02-use-with-claude-code.md)
- [Use with Generic CLI Agent](03-use-with-generic-cli-agent.md)
- [Project-first connection](04-project-first-connection.md)
