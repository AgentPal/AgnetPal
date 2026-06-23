# Pal Isolation And Shared Memory Future

Pal Isolation and Shared Memory are future AgentPal design concepts for complex workflows.

Isolation keeps independent judgement independent. Shared Memory keeps safe, cleaned lessons available for later work.

## Status

- Current: Not active as enforced runtime behavior in v0.1.0-rc.1. Current behavior uses Simple Pal Mode and bounded context loading.
- Future: May support independent review stages, controlled cross-reading, cleaned workflow memory, and routing feedback.
- Research: PalBench can evaluate isolation integrity, memory reuse, false consensus reduction, and rework reduction.

## Why it exists

When several perspectives review the same task, they can accidentally copy each other's assumptions. This creates agreement without real verification.

Isolation is meant to prevent:

- first-answer anchoring
- copied mistakes
- false consensus
- unnecessary context expansion
- reviewers reading each other's drafts before forming their own judgement

Shared Memory solves a different problem: useful lessons should not disappear after the task, but raw private context should not be spread.

## How it works

Future Pal Isolation may define:

- which recipient may read which files
- which prior outputs are hidden until synthesis
- when drafts can be shared
- which verifier checks evidence
- what the summary step may merge

Future Shared Memory may store cleaned records such as:

- routing success or failure
- runtime fit
- model or reasoning fit
- Skill usefulness
- verification outcome
- user acceptance
- rework reason

Shared Memory must exclude secrets, credentials, raw private messages, unrelated personal memory, customer data, and full project files unless explicitly approved and safe.

## What it is not

- Not active isolation enforcement in v0.1.
- Not a shared scratchpad for every Pal to read everything.
- Not private memory replication.
- Not a way to store secrets or raw user data.
- Not a reason to skip Context Slicing.
- Not a replacement for Routing Decision Records or Verification Result Records.

## Future acceptance rule

A future isolated workflow should be able to show:

- what each participant could read
- what each participant could not read
- whether drafts remained independent until synthesis
- what memory was written
- why the memory is safe to reuse

