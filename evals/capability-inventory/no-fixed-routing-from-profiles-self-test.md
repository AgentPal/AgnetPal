# No Fixed Routing From Profiles Self-Test

This self-test checks that Capability Inventory profiles do not become route tables.

## Reject If

Reject a change if profile docs or examples state that:

- a task type belongs to a Pal without case-specific judgement;
- a runtime should always execute a category of work;
- a model profile forces a reasoning level for every task;
- a Skill profile triggers automatic Skill execution;
- a plugin or MCP profile triggers automatic external tool use;
- a Pal profile replaces contacts, registry, PAL.md, or output contract reading.

## Accept If

Accept when docs and examples use:

- candidate language;
- current evidence requirements;
- Task Judgement before profile use;
- Context Slicing for profile loading;
- Simple Pal Mode boundary.

## R43 Negative Example

`examples/failures/capability-profile-used-as-fixed-route.md` should exist and explain why profiles are judgement inputs, not routes.

## Expected R43 Result

Expected result: pass.
