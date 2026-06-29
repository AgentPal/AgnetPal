# Methodology Overview

AgentPal Pal Orchestration Methodology explains how the Pal layer organizes work for an existing host runtime.

The method does not add model intelligence by itself. It improves how available intelligence is used: tighter task judgement, smaller context slices, clearer handoffs, explicit evidence, and reusable decision records.

## Current v0.5 Status

- Mira-first owner judgement.
- Fast Route for clear single-owner work.
- Task Package, Context Slicing, Asset Loading Budget, Verification Result Record, and Routing Decision Record.
- Capability Inventory from visible evidence, manual profiles, or runtime-reported profiles.
- Runtime / model / Skill awareness.
- Deep Conductor as no-code collaboration and mode-decision protocol.
- Host-dependent subagents, tools, plugins, MCP, model calls, and external Agents require current host evidence and user authorization.

## Why It Exists

Direct agent use often leaves users with coordination work:

- choose the right specialist perspective
- decide which files to include
- decide whether a Skill or plugin is useful
- decide whether the answer needs verification
- keep track of what worked last time

AgentPal moves those decisions into a transparent Pal layer. Users can start with Mira, and AgentPal can organize the rest without hiding the reasoning.

## How It Works

AgentPal separates the scheduling problem into small decisions:

- Task judgement: what is the goal, risk, ambiguity, and evidence need?
- Owner selection: which registered Pal should own the answer, if any?
- Context control: what is the smallest useful file, asset, and memory slice?
- Capability awareness: what host, model profile, reasoning strength, Skill, plugin, or MCP candidate may help?
- Handoff: should this be a direct Pal answer or a Task Package for execution?
- Verification: what evidence would prove completion?
- Learning: should the result become a memory candidate or future Skill?

These decisions do not start separate Agents by themselves.

## What It Is Not

- Not a task-domain route table.
- Not keyword routing.
- Not automatic runtime probing.
- Not a multi-Agent workflow engine.
- Not a comparison with outside systems.
- Not permission to run tools without host evidence and user authorization.

## Current Map

| Concept | v0.5 status | Notes |
| --- | --- | --- |
| Fast Route | Current | Clear owner handoff. |
| Task Package | Current | Compact execution or review handoff shape. |
| Context Slicing | Current | Read the smallest useful slice. |
| Asset Loading Budget | Current | Bounded file and asset loading rules. |
| Capability Inventory | Current as evidence/profile method | Not an automatic scan. |
| Runtime / Model / Skill Awareness | Current as documented awareness | Unknown facts remain unknown until confirmed. |
| Verification Result Record | Current as template and audit artifact | Does not prove completion without evidence. |
| Routing Decision Record | Current as template and audit artifact | Not a route rule. |
| Deep Conductor | Current as no-code decision protocol | Not automatic runtime execution. |
| Pal Isolation and Shared Memory | Host/future dependent | Requires evidence and governance before active execution. |
