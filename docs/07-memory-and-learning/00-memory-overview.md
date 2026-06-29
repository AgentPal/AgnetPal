# Memory Overview

AgentPal v0.5 treats memory as a governed writeback decision, not as automatic global recall.

Memory exists to preserve useful preferences, project facts, task lessons, routing evidence, and repeated methods. It must not leak private user data into public docs, Pal Packs, examples, or global knowledge.

## Memory Types

| Type | What it stores | Default boundary |
| --- | --- | --- |
| User memory candidate | Stable user preference or working habit | Private unless explicitly approved |
| Project memory candidate | Project-specific fact, decision, source map, or task record | Project record under `workspace/projects/<project-id>/` |
| Skill memory candidate | Repeated method that may become a Pal-owned Skill | Owner Pal review before public write |
| Public example | Sanitized reusable example | No customer-private data, credentials, or local secrets |

## Writeback Rule

Before writing any memory-like content, decide:

- Is this private user preference?
- Is this project-specific?
- Is this public release content?
- Does it contain customer data, credentials, private paths, or internal notes?
- Does the user authorize the write target?

If the answer is unclear, mark it as a memory candidate and ask for the correct target later.

## Example

User says:

```text
以后开发提示词包含模型和推理强度建议。
```

This is a user preference memory candidate. It should not be written into public AgentPal standards automatically.

User provides real CRM export rows. That is customer-private data. It must not enter public examples, Pal Packs, or global knowledge.

## Next Links

- [User memory](01-user-memory.md)
- [Project memory](02-project-memory.md)
- [Skill memory](03-skill-memory.md)
- [From repeated task to Skill](05-from-repeated-task-to-skill.md)
- [Public/private boundary](../03-pal-pack-standard/11-public-private-boundary.md)
