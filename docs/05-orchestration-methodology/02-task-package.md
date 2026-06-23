# Task Package

A Task Package is AgentPal's compact handoff format for work that must be executed, reviewed, or continued by a runtime, Pal, Skill, plugin, or human maintainer.

It turns Pal judgement into an actionable package.

## Status

- Current: Active in v0.1.0-rc.1 as a handoff and compression method.
- Future: May become a required unit inside Deep Conductor topologies.
- Research: PalBench can score Task Packages for clarity, acceptance criteria, evidence quality, and rework prevention.

## Why it exists

Long conversations and broad instructions are easy to misunderstand. A Task Package states the work in a shape that can be executed and verified.

It helps preserve:

- goal
- bounded context
- owner perspective
- constraints
- steps
- acceptance criteria
- risks
- do-not-do rules
- evidence required

## How it works

A Task Package uses this shape:

```text
Task Package
- Goal
- Context summary
- Relevant files / assets
- Asset loading note
- Owner Pal perspective
- Constraints
- Steps
- Output format
- Acceptance criteria
- Risks
- Do not do
- Evidence required
```

The package should distinguish:

- paths known from an index or file list
- files actually read as content
- assumptions not yet verified
- evidence that must exist before completion can be claimed

## What it is not

- Not an execution claim.
- Not proof that files were changed, tests passed, or content was published.
- Not a license to read the full workspace.
- Not a substitute for user approval on high-risk actions.
- Not a hidden prompt for external agents unless a runtime explicitly executes it with evidence.

## Good Task Package behavior

A good Task Package is small enough to act on and specific enough to verify.

It should say:

- what to change or inspect
- where to look
- what not to touch
- how to report the result
- which evidence will count

If evidence is unavailable, the result remains unverified.

