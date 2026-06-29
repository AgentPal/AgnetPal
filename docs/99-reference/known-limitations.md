# Known Limitations

AgentPal v0.5 is intentionally conservative about execution claims.

## Current Boundary

- AgentPal is a Pal layer and Pal workspace, not an Agent runtime.
- Codex is the verified first host.
- Claude Code has limited/minimal handoff evidence only.
- Generic CLI Agent is a compatibility path, not broad host acceptance.
- OpenCode and Gemini are unavailable in current evidence.
- DeepSeek is experimental/version-help only.
- Plan Mode UI evidence is unavailable.
- Goal Mode evidence is limited.
- External project writeback is not generally validated.
- AgentPal does not include a desktop app, web UI, CLI product, hosted service, daemon, scanner, validator, installer, connector system, marketplace, or app runtime.
- AgentPal does not provide exact token metering or cost calculation.
- Runtime actions require current host evidence.

## What This Means For Users

Use AgentPal when you want a structured Pal workspace that helps an existing host runtime reason about roles, context, capability, privacy, Task Packages, and verification.

Do not use AgentPal when you need:

- a standalone agent application
- production background orchestration
- automatic customer-system integration
- guaranteed multi-Agent execution
- automatic tool installation
- automatic external project writeback
- hosted Pal marketplace or discovery

## Related

- [Current status](../00-overview/01-current-status.md)
- [AgentPal vs Agent Runtime](../00-overview/03-agentpal-vs-agent-runtime.md)
- [Runtime compatibility](../04-runtime-guides/00-runtime-compatibility.md)
- [Public/private boundary](../03-pal-pack-standard/11-public-private-boundary.md)
