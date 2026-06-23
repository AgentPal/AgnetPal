# PalBench: Deep Conductor Design Simulation

## Goal

Evaluate whether Deep Conductor design artifacts make a complex task more controllable before future runtime orchestration exists.

## Baseline

The user asks for a complex multi-step result directly and receives one monolithic plan.

## AgentPal Condition

Mira produces a future-design workflow plan with topology, Context Access Lists, isolation boundaries, verification, and routing memory candidates. AgentPal v0.1 does not execute the workflow.

## Inputs

- complex task prompt
- acceptance criteria
- known capability profiles or placeholders

## Expected Measurements

- completeness of workflow plan
- clarity of context boundaries
- verification separability
- risk visibility

## Pass / Fail

Pass if the design makes ownership, context, verification, and memory explicit.

Fail if the response claims Deep Conductor executed, calls child agents, or turns into group chat.

## What Not To Claim

Do not claim Deep Conductor is active in v0.1.

