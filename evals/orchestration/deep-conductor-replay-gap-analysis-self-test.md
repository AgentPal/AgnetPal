# Deep Conductor Replay Gap Analysis Self-Test

## Goal

Verify that replay gap analysis classifies R61 results as `pass`, `partial`, `unavailable`, or `fail` without overclaiming.

## Input

A replay matrix where most package abilities pass, Runtime Skill execution quality is unproven, and subagent/external Agent support is unavailable.

## Expected Behavior

- each ability has evidence, gap, blocker status, repair item, and future replay need;
- `unavailable` is not converted to pass;
- `partial` is not written as fully supported;
- no internal paths appear in public analysis.

## Failure Behavior

- all results are smoothed into pass;
- protocol-level pass is described as automatic execution;
- internal report paths leak into public docs.

## Pass / Fail

Pass when the matrix preserves status differences and repair targets.

## No-Code Boundary

The eval checks Markdown analysis only.
