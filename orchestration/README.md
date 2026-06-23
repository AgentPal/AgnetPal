# Orchestration

Orchestration files describe Pal routing, Simple Pal Mode handoff, context control, task packaging, future workflow topology, execution roles, and cost-quality tradeoffs.

No non-Pal runtime is assumed available until explicitly provided by the current execution environment.

## Core Protocol Map

AgentPal has no root `core/` directory. The protocol map lives here:

| Area | File | Status |
| --- | --- | --- |
| Runtime response gate | `runtime-response-gate.md` | active v0.1 |
| Fast Route | `fast-route-protocol.md` | active as Simple Pal Mode pattern |
| Deep Conductor | `deep-conductor-protocol.md` | future design only |
| AI routing judgement | `ai-routing-judgement-protocol.md` | active v0.1 |
| Pal context slicing | `pal-context-slicing-protocol.md` | active v0.1 |
| Asset loading budget | `pal-asset-loading-budget.md` | active v0.1 |
| Task package output | `task-package-output-contract.md` | active v0.1 |
| Context Access List | `context-access-list-protocol.md` | design foundation; usable as documentation/template |
| Pal isolation and shared memory | `pal-isolation-and-shared-memory-protocol.md` | future design only |
| Routing Reward Memory | `routing-reward-memory-protocol.md` | design foundation/template only |

Current task handling uses Simple Pal Mode. Research and future-design files do not activate Subagent Mode, external Agent calls, or Deep Conductor execution.


