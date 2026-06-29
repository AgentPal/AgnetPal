# Deep Conductor And Runtime Futures

Deep Conductor is AgentPal's no-code collaboration and mode-decision protocol for complex work.

It helps the current AI reason about workflow topology, separated context, independent review, verification, capability evidence, and routing memory. It does not make AgentPal an automatic execution runtime.

## Current v0.5 Status

- Current: no-code staged judgement, owner candidates, capability candidates, context boundaries, Task Packages, and verification decisions.
- Host-dependent: subagents, parallel execution, external Agent calls, tool execution, and runtime-specific automation.
- Future: stronger runtime adapters may implement deeper execution paths if the host provides capability evidence and the user authorizes them.

## Why It Exists

Some tasks are too complex for a single fast answer:

- several capability candidates must be compared
- independent review would reduce risk
- context must be separated by role
- execution evidence must be checked before acceptance
- the result should teach future routing decisions

Deep Conductor defines how AgentPal organizes those cases without turning the Pal layer into a hidden black box.

## What It Uses

Deep Conductor may combine:

- Task Judgement Packet
- Capability Inventory
- Workflow Topology
- Context Access List
- Task Package
- Verification Result Record
- Routing Decision Record
- memory candidate review

Possible topologies include owner plus verifier, plan-execute-verify, parallel independent review, sequential chain, and best-of-N comparison. The host runtime still provides execution if execution happens.

## What It Is Not

- Not a current multi-Agent runtime.
- Not automatic external Agent orchestration.
- Not permission to spawn child workflows.
- Not a reason to show runtime-mode metadata in normal answers.
- Not a claim that complex workflows always improve results.

## Boundary Rule

When describing Deep Conductor, separate no-code decision behavior from host-dependent execution behavior.
