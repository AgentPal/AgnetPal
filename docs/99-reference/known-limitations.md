# Known Limitations

AgentPal v0.1.0-rc.1 is a conservative release candidate. Its active behavior is intentionally smaller than some design materials in the repository.

## Current Active Boundary

- Simple Pal Mode is the only active task-handling path in v0.1.0-rc.1.
- AgentPal is a Pal layer and Pal Workspace, not an Agent layer.
- AgentPal is not a complete multi-agent runtime.
- AgentPal is not an execution layer.
- AgentPal does not include a desktop app, web UI, CLI product, hosted service, daemon, scanner, validator, or installer.
- AgentPal does not include Pal Hub, Pal marketplace, commercial Pal distribution, or hosted Pal discovery.
- AgentPal does not include automatic deep runtime adapters.
- OpenClaw, Hermes, remote agent, MCP-hosted agent, and similar adapter ideas are not active unless a future release explicitly marks them active.
- Subagent and child workflow materials, where present, are future design or experimental reference material. They are not the active v0.1.0-rc.1 task-handling path.
- AgentPal does not provide exact token metering. It provides context budgets, file loading levels, and asset loading reporting rules.
- Runtime actions require evidence from the host runtime. A Pal cannot claim an action was executed without current runtime evidence.

## What This Means For Users

Use AgentPal v0.1.0-rc.1 when you want a structured Pal Workspace for Codex, Claude Code, or another Markdown/JSON-capable runtime.

Do not use this release when you need:

- a standalone agent application
- a production orchestration runtime
- background workers or daemons
- a marketplace or hosted Pal registry
- automatic tool installation or external system management
- guaranteed runtime integration beyond the files and protocols in this repository

## Related

- [Current status](../00-overview/01-current-status.md)
- [AgentPal vs Agent Runtime](../00-overview/03-agentpal-vs-agent-runtime.md)
- [Simple Pal Mode](../01-concepts/05-simple-pal-mode.md)
- [Runtime compatibility](../04-runtime-guides/00-runtime-compatibility.md)
- [Future runtime adapters](../04-runtime-guides/99-future-runtime-adapters.md)
- [Public/private boundary](../03-pal-pack-standard/11-public-private-boundary.md)
