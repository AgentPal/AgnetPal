# Skill Memory

Skill memory records repeated methods that may become formal Pal-owned Skills.

A Pal-owned Skill is a no-code capability package stored under the owner Pal's `skills/` directory. It is different from a host runtime Skill, plugin, model, MCP tool, or external tool.

## When To Consider A Skill

Create or propose a Skill when:

- the user explicitly asks to save a method as a Skill
- similar operations repeat more than three times
- a Pal repeatedly needs the same intake, context slicing, Task Package, review, or output method
- the method is public-safe or has a clear private storage boundary

## Before Writing

Check:

- owner Pal
- expected users
- allowed inputs
- forbidden inputs
- output contract
- verification steps
- privacy boundary
- examples and failure cases
- whether the method belongs to a Pal or to the host runtime

## What Not To Do

- Do not store runtime-installed Skills inside Pal Packs.
- Do not write private user data into public Skill examples.
- Do not turn a Skill into a central Pal contact.
- Do not claim the Skill can execute tools unless the host runtime provides evidence.

## Next Links

- [From repeated task to Skill](05-from-repeated-task-to-skill.md)
- [Skills](../03-pal-pack-standard/06-skills.md)
- [Runtime-installed Skill orchestration](../05-orchestration-methodology/runtime-installed-skill-orchestration-guide.md)
