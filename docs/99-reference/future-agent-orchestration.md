# Future Agent Orchestration

This page is about host-dependent execution futures. It is not a current feature claim.

## Current Boundary

AgentPal v0.5 is a Pal layer. It is not an Agent runtime, not a multi-Agent runtime, and not an execution layer.

Deep Conductor is current as no-code collaboration and mode-decision protocol. It does not start external Agents or background workflows by itself.

## Possible Future Scope

A later runtime adapter may explore:

- child workflows
- subagents
- non-Pal execution runtimes
- MCP-hosted agents
- remote agent services
- runtime-specific execution packages

Any such layer would need its own permission model, evidence model, timeout/cancellation model, privacy boundary, and user-facing status before activation.

## Related

- [Runtime compatibility](../04-runtime-guides/00-runtime-compatibility.md)
- [Known limitations](known-limitations.md)
