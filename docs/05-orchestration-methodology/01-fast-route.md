# Fast Route

Fast Route is AgentPal's current clear-task path.

When a request is bounded enough for one owner Pal, Mira makes a short ownership judgement, hands off, and stops. The owner Pal answers immediately in the same response using its own assets, Output Contract, and fallback rules.

## Status

- Current: Active in v0.1.0-rc.1 as part of Simple Pal Mode.
- Future: May become one topology inside a larger Deep Conductor workflow system.
- Research: PalBench can compare Fast Route against direct prompting for clarity, context control, and rework.

## Why it exists

Many tasks do not need a complex workflow. They need:

- the right owner
- a bounded context slice
- a clear answer or Task Package
- no unnecessary mode ceremony

Fast Route keeps the common path short while preserving the Pal boundary.

## How it works

1. Mira receives the user request.
2. Mira checks current contacts and registry.
3. Mira judges whether a registered Pal owns the work.
4. If yes, Mira says only the ownership judgement and handoff.
5. The owner Pal answers immediately.
6. The owner Pal loads only required identity files and relevant assets.
7. If execution evidence is needed, the owner Pal asks for it or writes a Task Package that names the required evidence.

Example shape:

```text
Mira: I judge this belongs to {Owner Pal} because {case-specific reason}. I am handing it to {Owner Pal}.

{Owner Pal}: I will handle it using {asset or fallback method}.
```

## What it is not

- Not a fixed mapping from task words to Pal names.
- Not Mira writing the specialist answer after handoff.
- Not a multi-agent workflow.
- Not a hidden external runtime call.
- Not a reason to skip verification when completion is claimed.

## Use Fast Route when

- one owner Pal can reasonably handle the work
- the task is clear enough to answer or package directly
- independent review would not materially improve the result
- context can be bounded
- risk is low or can be handled with explicit evidence requirements

## Avoid Fast Route when

- the task needs independent verification before acceptance
- several conflicting perspectives must remain isolated
- file writes, publishing, deletion, or risky system changes require explicit approval
- the current runtime, model, Skill, or plugin facts are unknown and materially affect the route

