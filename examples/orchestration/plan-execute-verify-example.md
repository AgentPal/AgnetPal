# Plan Execute Verify Example

This is a future-design example.

## Situation

The task needs a plan, real execution by a runtime, and evidence review.

## Shape

```text
planner Pal -> execution runtime -> verifier -> summary
```

## Context Access

- planner receives requirements and selected project slice
- execution runtime receives a Task Package
- verifier receives execution evidence and acceptance criteria

## Why It Helps

Planning, execution, and verification are separated so completion claims can be checked.

## v0.1 Boundary

AgentPal v0.1 can write the Task Package, but it does not run an automated multi-runtime workflow.
