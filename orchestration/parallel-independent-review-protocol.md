# Parallel Independent Review Protocol

Parallel Independent Review is a v0.3 no-code staged workflow for collecting separate Pal perspectives before synthesis.

It is not group chat and not automatic multithreaded execution.

## When To Use

Use when independent viewpoints materially improve the decision:

- product decisions;
- architecture tradeoffs;
- release risks;
- research conclusion review;
- high-cost or high-risk strategy choices.

Do not use when:

- one owner Pal can answer safely;
- the task is simple and low-risk;
- the user wants a short direct answer.

## Isolation Rules

- Each reviewer receives its own Context Packet.
- Each reviewer reads only its allowed context.
- Reviewers do not read each other's drafts.
- Reviewers do not read hidden reasoning or raw execution traces unless allowed.
- The summary stage reads final reports, not drafts.

## Workflow

1. Intake and task judgement.
2. Reviewer candidate selection from current contacts / registry.
3. Separate Context Packets for each reviewer.
4. Independent final reviewer reports.
5. Summary stage compares agreement, conflict, evidence gaps, and recommended next action.
6. Optional routing result record after user or verifier outcome is known.

## Reviewer Output

Each reviewer should return:

- judgement;
- evidence used;
- assumptions;
- risks;
- recommendation;
- confidence;
- gaps;
- what another Pal or runtime should check next.

## Summary Output

The summarizer should return:

- agreements;
- conflicts;
- evidence strength;
- missing context;
- decision options;
- recommended next action;
- verification requirement;
- routing memory candidate.

## Boundary

This workflow is a staged protocol only. It does not activate automatic Deep Conductor, subagents, external Agent calls, or runtime parallelism.
