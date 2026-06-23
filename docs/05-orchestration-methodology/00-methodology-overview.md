# Methodology Overview

AgentPal Pal Orchestration Methodology explains how the Pal layer organizes work for an existing agent runtime.

The method does not add model intelligence by itself. It improves how available intelligence is used: tighter task judgement, smaller context slices, clearer handoffs, explicit evidence, and reusable decision records.

## Status

- Current: Simple Pal Mode, AI-judged owner selection, Fast Route, Task Package, Context Slicing, and Asset Loading Budget.
- Future: Deep Conductor, Context Access List enforcement, Pal Isolation, Shared Memory, Routing Reward Memory, and external runtime orchestration.
- Research: PalBench measures whether AgentPal-style organization improves practical task handling, not whether one model is better than another.

## Why it exists

Direct agent use often leaves users with coordination work:

- choose the right specialist perspective
- decide which files to include
- decide whether a Skill or plugin is useful
- decide whether the answer needs verification
- keep track of what worked last time

AgentPal moves those decisions into a transparent Pal layer. Users can start with Mira, and AgentPal can organize the rest without hiding the reasoning.

## How it works

AgentPal separates the scheduling problem into small decisions:

- Task judgement: what is the goal, risk, ambiguity, and evidence need?
- Owner selection: which registered Pal should own the answer, if any?
- Context control: what is the smallest useful file, asset, and memory slice?
- Capability awareness: what runtime, model profile, reasoning strength, Skill, plugin, or MCP candidate may help?
- Handoff: should this be a direct Pal answer or a Task Package for execution?
- Verification: what evidence would prove completion?
- Learning: should the routing result become a future non-binding recommendation?

In v0.1.0-rc.1, these decisions stay inside Simple Pal Mode. They do not start separate agents.

## What it is not

- Not a task-domain route table.
- Not keyword routing.
- Not automatic runtime probing.
- Not a current multi-agent workflow engine.
- Not a comparison with outside systems.
- Not a claim that future designs are active now.

## Current and future map

| Concept | v0.1.0-rc.1 status | Notes |
| --- | --- | --- |
| Fast Route | Current | Clear owner handoff in Simple Pal Mode. |
| Task Package | Current | Compact execution or review handoff shape. |
| Context Slicing | Current | Read the smallest useful slice. |
| Asset Loading Budget | Current | Bounded file and asset loading rules. |
| Capability Inventory | Current as profiles and templates; future as richer inventory | Not an automatic scan. |
| Runtime / Model / Skill Awareness | Current as documented awareness; future as richer refresh | Unknown facts remain unknown until scanned. |
| Verification Result Record | Current as template and audit artifact | Does not prove completion without evidence. |
| Routing Decision Record | Current as template and audit artifact | Not a route rule. |
| Deep Conductor | Future | Not active in v0.1. |
| Pal Isolation and Shared Memory | Future | Design for independent judgement and safe reusable memory. |
