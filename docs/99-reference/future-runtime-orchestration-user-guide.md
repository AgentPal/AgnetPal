# Future Runtime Orchestration User Guide

Future design only. Not active in AgentPal v0.1.0-rc.1.

## Current User Expectation

In AgentPal v0.1.0-rc.1:

- Ordinary messages go to Mira.
- `/pal Name` enters the selected Pal's working mode.
- No separate runtime workflow is started or claimed by AgentPal.
- No runtime-mode metadata is shown in normal answers.

## Future Direction

A later AgentPal version may design an orchestration layer that coordinates child workflows or external execution runtimes. Until that design exists, users should evaluate AgentPal by whether Simple Pal Mode routes to the correct Pal and uses the correct Pal assets.

## Related

- [Future runtime adapters](../04-runtime-guides/99-future-runtime-adapters.md)
- [Known limitations](known-limitations.md)
