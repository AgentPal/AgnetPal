# Future Codex Subagent Mode

Future design only. Not active in AgentPal v0.1.0-rc.1.

## Current Boundary

AgentPal v0.1.0-rc.1 uses Simple Pal Mode only. Direct `/pal Name` calls do not start separate runtime processes.

No tool discovery or child workflow call is part of normal AgentPal v0.1.0-rc.1 task handling.

## Future Direction

A later runtime adapter may explore Codex child workflows, but it would need a separate permission model, evidence model, timeout/cancellation model, privacy boundary, and user-facing explanation before activation.

## Related

- [Future runtime adapters](../04-runtime-guides/99-future-runtime-adapters.md)
- [Future agent orchestration](future-agent-orchestration.md)
