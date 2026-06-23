# Write Root SKILL.md

## Status

Current for AgentPal `v0.1.0-rc.1`.

The root `SKILL.md` lets Skill-aware runtimes discover the Pal Pack. It is not the same as a normal single-purpose Skill.

## Required Message

Say clearly:

```text
This is a Pal Pack entry, not a single ordinary Skill.
```

## Minimal Shape

```md
---
name: example-role-pal
description: Use Example as a Role Pal for clear task family.
version: 0.1.0
type: pal-pack
---

# Example Pal Entry

This is a Pal Pack entry, not a single ordinary Skill.

## Use When

- Use for specific task family.

## Read Order

Read PAL.md, pal.json, AGENTS.md, core/output-contract.md, core/task-loop.md, identity/, and relevant indexes.

## Boundary

Real file edits, commands, publishing, deletion, or system changes require the host runtime and evidence.
```

## Pal-Owned Skills

Formal Skills created later go under `skills/<skill-id>/SKILL.md`, not into the root `SKILL.md`.
