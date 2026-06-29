# Pal Orchestration Methodology

This directory explains AgentPal's no-code orchestration methodology.

AgentPal v0.5 organizes task ownership, context, capability awareness, runtime evidence, verification, memory candidates, and reusable records. It does this inside an existing host runtime. It is not a multi-Agent runtime and not an execution layer.

## Current Status

Current v0.5 methods include:

- Mira-first owner judgement
- Fast Route for clear single-owner tasks
- Task Packages
- Context Slicing
- Asset Loading Budget
- Capability Inventory as manual/runtime-reported profile evidence
- Runtime / model / Skill awareness
- Verification Result Records
- Routing Decision Records
- Context Packets
- Owner + Verifier no-code workflow
- Parallel Independent Review no-code workflow
- Deep Conductor as a no-code collaboration and mode-decision protocol
- Cross-Runtime Pal Memory guidance
- Runtime-installed Skill Orchestration guidance

These methods do not activate automatic runtime execution, subagents, external Agent calls, background services, scanner behavior, or connector behavior by themselves.

## Why It Exists

Users should not need to choose every Pal, runtime, model, Skill, plugin, context file, and verification path by hand for every task.

The methodology helps answer:

- who owns the work
- what context is enough
- which capability is known, unknown, or unavailable
- what runtime evidence is required
- what should be accepted, rejected, or marked not-run
- what can become a memory candidate or future Skill

## Agent-Use Decision

When a task may need execution, AgentPal should make an Agent-use Decision before claiming capability:

- Which Pal owns the task?
- Which runtime capability is required?
- Is that capability visible now, reported by the host, manually profiled, or unknown?
- What evidence will prove execution?
- What should happen if the capability is unavailable?

Runtime tools are execution support, not Pal owners.

## What It Is Not

- Not a stronger model claim.
- Not a hidden multi-Agent runtime.
- Not an automatic capability scanner.
- Not permission to run commands or tools without evidence and user authorization.
- Not a reason to load the full workspace by default.
- Not a route map from keywords to Pals.

## Documents

- [00 Methodology Overview](00-methodology-overview.md)
- [01 Fast Route](01-fast-route.md)
- [02 Task Package](02-task-package.md)
- [03 Context Slicing](03-context-slicing.md)
- [04 Asset Loading Budget](04-asset-loading-budget.md)
- [05 Capability Inventory](05-capability-inventory.md)
- [06 Runtime / Model / Skill Awareness](06-runtime-model-skill-awareness.md)
- [07 Verification Result Record](07-verification-result-record.md)
- [08 Routing Decision Record](08-routing-decision-record.md)
- [09 Deep Conductor Future](09-deep-conductor-future.md)
- [11 Pal Teams And Deep Conductor](11-pal-teams-and-deep-conductor.md)
- [Runtime-installed Skill Orchestration](runtime-installed-skill-orchestration-guide.md)
- [Cross-Runtime Pal Memory](cross-runtime-pal-memory.md)
