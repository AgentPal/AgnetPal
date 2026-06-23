# Add Skills

## Status

Current for AgentPal `v0.1.0-rc.1`.

Pal-owned Skills are focused capabilities that belong to one Pal.

## Start With Index

Create:

```text
skills/index.md
```

It can say no formal Skills exist yet.

## Add A Formal Skill

```text
skills/<skill-id>/
├─ SKILL.md
└─ README.md
```

Use `SKILL.md` as the runtime entry and `README.md` for human notes.

## When To Create One

- The user explicitly asks to save a method as a Skill.
- Similar work repeats three or more times.
- The content is safe, sufficiently specified, and belongs to this Pal.

## Storage Rule

Save the Skill under the owner Pal's own `skills/` directory. Do not default to global runtime Skill directories.

## Discovery Boundary

Skills are not Pals and should not be added to Pal contacts.
