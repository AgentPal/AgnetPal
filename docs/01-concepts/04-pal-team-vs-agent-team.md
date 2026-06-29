# Pal Team Vs Agent Team

Pal Teams and Agent Teams can aim at the same outcome: better collaboration on complex work. They are not the same layer.

## The Difference

| Layer | What it is | What it can claim |
| --- | --- | --- |
| Pal Team | A group of registered Pals that provide judgement, roles, context boundaries, Task Packages, and review habits | No-code collaboration and responsibility structure |
| Agent Team | Multiple runtime agents, subagents, workers, or processes that perform work | Only when the host runtime actually provides and evidences it |

AgentPal is the Pal Team layer. It is lighter than a multi-Agent runtime because it is mostly Markdown / JSON / protocol, not a background execution system.

## What A Pal Team Does

A Pal Team can help:

- identify the domain focus of a task
- choose a responsible owner Pal
- split a composite deliverable into stages
- prepare a Task Package for a host runtime
- define context access limits
- decide whether host capabilities are known, unknown, or unavailable
- review results before accepting them
- record public-safe learning candidates

## What A Pal Team Does Not Do

A Pal Team does not:

- start separate agents
- run tools by itself
- call customer systems
- auto-sync memory
- scan the machine
- execute a workflow in the background
- prove host capability without current evidence

## How They Work Together

When a host runtime supports subagents or other execution workers, AgentPal can still be useful. A Pal can prepare the owner judgement, context packet, acceptance criteria, and evidence requirements before the runtime executes anything.

The runtime remains responsible for actual execution. The Pal layer remains responsible for clarity, boundaries, and review.

## Current v0.5 Position

- Codex is the verified first host.
- Claude Code has limited/minimal handoff evidence only.
- Generic CLI Agent is a compatibility path.
- Deep Conductor is a no-code collaboration and mode-decision protocol, not proof of automatic multi-Agent execution.

## Next Links

- [Pal vs Agent vs Skill](03-pal-vs-agent-vs-skill.md)
- [Pal Teams, Collaboration, and Deep Conductor](08-pal-teams-collaboration-and-deep-conductor.md)
- [Runtime compatibility](../04-runtime-guides/00-runtime-compatibility.md)
