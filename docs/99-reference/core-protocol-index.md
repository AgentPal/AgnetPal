# Core Protocol Index

This page indexes key AgentPal protocols for v0.5 users and maintainers.

## Current Protocols

| Protocol | Purpose |
| --- | --- |
| `core/agentpal-core-gate.md` | Shared core response gate for runtime adapters |
| `orchestration/runtime-response-gate.md` | User-facing answer validity, routing, language, safety, and evidence gate |
| `orchestration/ai-routing-judgement-protocol.md` | Case-specific owner judgement; no keyword routing |
| `orchestration/pal-context-slicing-protocol.md` | Load the smallest useful context slice |
| `orchestration/agent-instruction-file-loading-policy.md` | Controls instruction file loading |
| `orchestration/pal-asset-loading-budget.md` | Bounded Pal asset loading rules |
| `orchestration/task-package-output-contract.md` | Task Package structure and evidence expectations |
| `orchestration/pal-owned-skill-storage-protocol.md` | Stores formal Pal-owned Skills under the owner Pal |
| `orchestration/specialist-pal-asset-loading-protocol.md` | Loads selected owner Pal assets only |

## Boundary

Protocols guide the host runtime. They do not create a scanner, connector, daemon, app runtime, or automatic multi-Agent execution layer.

## Next Links

- [Core protocols](../03-pal-pack-standard/03-core-protocols.md)
- [Runtime compatibility](../04-runtime-guides/00-runtime-compatibility.md)
- [Methodology overview](../05-orchestration-methodology/00-methodology-overview.md)
