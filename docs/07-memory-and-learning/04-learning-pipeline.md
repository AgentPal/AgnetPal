# Learning Pipeline

The learning pipeline turns useful task experience into reusable AgentPal assets without leaking private data.

## Pipeline

1. Notice a repeated pattern.
2. Classify it as user memory, project memory, Skill memory, workflow, runbook, example, eval, or report candidate.
3. Select the owner Pal or project record.
4. Remove private data, credentials, customer facts, and local-only paths.
5. Decide whether the target is private, project-local, team-local, or public.
6. Write only after the target and boundary are approved.
7. Mark evidence as `pass`, `partial`, `not-run`, `blocked`, `missing`, or `unknown`.

## What Can Become Reusable

- repeated intake questions
- context slicing patterns
- Task Package shapes
- review checklists
- failure cases
- output contracts
- safe examples
- Pal-owned Skills

## What Must Not Become Public

- real customer data
- credentials
- private project facts
- private user preferences
- internal reports not intended for release
- unverified runtime capability claims

## Next Links

- [Memory overview](00-memory-overview.md)
- [From repeated task to Skill](05-from-repeated-task-to-skill.md)
- [Public/private boundary](../03-pal-pack-standard/11-public-private-boundary.md)
