# Deep Conductor Future

Deep Conductor is AgentPal's future orchestration design for complex work that needs workflow topology, separated context, independent review, verification, and routing memory.

It is not active task handling in v0.1.0-rc.1.

## Status

- Current: Not active. v0.1 uses Simple Pal Mode, Fast Route, Single Owner, and Task Package.
- Future: Planned methodology for complex multi-step orchestration when runtime support, user authorization, evidence handling, privacy boundaries, and fallback rules are defined.
- Research: PalBench may simulate Deep Conductor patterns and compare them with ad hoc multi-step prompting.

## Why it exists

Some tasks are too complex for a single fast answer:

- several capability candidates must be compared
- independent review would reduce risk
- context must be separated by role
- execution evidence must be checked before acceptance
- the result should teach future routing decisions

Deep Conductor defines how AgentPal might organize those cases without turning the Pal layer into a hidden black box.

## How it works

Future Deep Conductor may combine:

- Task Judgement Packet
- Capability Inventory
- Workflow Topology
- Context Access List
- Task Package
- Pal Isolation
- Verification Result Record
- Routing Decision Record
- Routing Reward Memory

Possible future topologies include:

- owner plus verifier
- plan, execute, verify
- parallel independent review
- sequential chain
- best-of-N runtime comparison

Each topology must define context boundaries, output contracts, evidence requirements, cost controls, timeout behavior, user approval points, and fallback behavior.

## What it is not

- Not active in v0.1.0-rc.1.
- Not a current multi-agent runtime.
- Not automatic external agent orchestration.
- Not permission to spawn child workflows.
- Not a reason to show runtime-mode metadata in normal answers.
- Not a claim that complex workflows always improve results.

## Boundary rule

If a document describes Deep Conductor behavior, it must clearly mark it as future unless the behavior is also documented as active for the current release.

