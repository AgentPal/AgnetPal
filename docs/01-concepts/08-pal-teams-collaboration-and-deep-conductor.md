# Pal Teams, Multi-Pal Collaboration, And Deep Conductor

AgentPal is not limited to one Pal, but it is also not an automatic multi-Agent runtime.

For small work, Mira can answer directly or route to one owner Pal. For larger work, a Pal Team can help the host runtime decide responsibility, stages, context limits, verification, and follow-up learning.

## Current v0.5 Status

- Mira remains the default entry Pal.
- The simple Mira-to-owner path is still available for clear tasks.
- Multi-Pal collaboration is available as Pal-layer judgement and written coordination.
- Deep Conductor is enabled as a no-code collaboration and mode-decision protocol.
- Deep Conductor does not prove automatic subagents, background workers, external Agent calls, or runtime parallel execution.
- Execution claims require current host-runtime evidence.

## What A Pal Team Is

A Pal Team is a group of registered Pal Packs that contribute different professional perspectives to the same goal.

Example for a release-readiness task:

| Pal | Possible contribution |
| --- | --- |
| Mira | Intake, owner judgement, stage framing, handoff, final summary |
| Quinn | Evidence, release gate, verification, acceptance risk |
| Harper | Public wording, release note, user-facing clarity |
| Rhea | Local system and command safety |
| Atlas | Code-facing structure and implementation risks |

These are candidates, not fixed routes. Owner selection remains case-specific AI judgement from the current central contacts.

## What Deep Conductor Adds

Deep Conductor helps the current runtime reason about:

- task complexity and risk
- candidate Pal owners and reviewers
- expected deliverables
- context access lists
- host capability evidence
- model / reasoning / Skill candidates
- Task Package boundaries
- verification records
- writeback and privacy boundaries

This is useful for composite work, but it remains no-code protocol unless the host runtime separately provides execution capability.

## When To Keep It Simple

Do not turn every request into a Pal Team.

Use a simpler path when:

- the user is asking ordinary conversation
- one owner Pal clearly fits
- the context is small
- the risk is low
- a direct `/pal Name` call is enough

## Required Boundaries

- Do not claim runtime scans unless the host actually ran and evidenced one.
- Do not copy Pal Packs or internal records into external projects by default.
- Do not store customer-private data in public examples, Pal Packs, or global knowledge.
- Do not treat Skills, tools, models, plugins, or raw repositories as Pals.

## Next Links

- [Pal Team vs Agent Team](04-pal-team-vs-agent-team.md)
- [Runtime compatibility](../04-runtime-guides/00-runtime-compatibility.md)
- [Deep Conductor methodology](../05-orchestration-methodology/README.md)
