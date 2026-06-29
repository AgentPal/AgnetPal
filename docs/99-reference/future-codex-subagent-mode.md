# Future Codex Subagent Mode

This page is a future design placeholder. It is not a current AgentPal feature claim.

## Current Boundary

AgentPal v0.5 can help Codex reason about Pal ownership, context, Task Packages, runtime capability candidates, and verification needs.

AgentPal does not automatically start Codex subagents. Direct `/pal Name` calls enter Pal working mode inside the current host runtime; they do not start separate Agent processes.

## Future Direction

A future Codex adapter may explore child workflows or subagents if the host runtime exposes reliable capability and evidence.

Before activation, it would need:

- explicit user authorization
- context access boundaries
- evidence reporting
- timeout and cancellation behavior
- privacy controls
- clear UI or textual status

## Related

- [Runtime compatibility](../04-runtime-guides/00-runtime-compatibility.md)
- [Future agent orchestration](future-agent-orchestration.md)
