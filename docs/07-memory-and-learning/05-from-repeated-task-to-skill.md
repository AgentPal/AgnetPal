# From Repeated Task To Skill

Repeated task learning turns a useful method into a formal Pal-owned Skill only when the boundary is clear.

## Current Rule

Create or propose a formal Skill when:

- the user explicitly asks to save the method as a Skill; or
- similar operations happen more than three times and the method is stable enough to reuse.

The Skill belongs under the owner Pal's own `skills/` directory.

## Promotion Steps

1. Identify the repeated method.
2. Select the owner Pal.
3. Remove private data and local-only facts.
4. Define inputs, outputs, forbidden claims, and verification.
5. Add examples only if they are public-safe.
6. Mark runtime capability as candidate or required evidence, not as assumed availability.
7. Write the Skill only after the target and scope are approved.

## Example

A user repeatedly asks Faye to turn business scenarios into:

- scenario summary
- user flow
- data list
- interface list
- risk list
- missing information
- Task Package

That pattern may become a Faye-owned Skill. It should not be stored as a generic runtime Skill, a connector, or a public example containing real customer data.

## Next Links

- [Skill memory](03-skill-memory.md)
- [Skills](../03-pal-pack-standard/06-skills.md)
- [Public/private boundary](../03-pal-pack-standard/11-public-private-boundary.md)
