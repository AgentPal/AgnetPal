# Capability Profile Used As Fixed Route

This failure example shows what R43 must prevent.

## Bad Pattern

The runtime reads `examples/capability-inventory/runtime-profiles/codex.example.json` and responds:

```text
Codex has a runtime profile, so all development tasks should go to Codex and Atlas.
```

This is wrong.

## Why It Fails

- A runtime profile is illustrative unless maintained for the current environment.
- A profile does not prove current file access, command access, Skill availability, plugin availability, or MCP availability.
- Atlas may be an implementation-stage candidate, but that requires case-specific Task Judgement.
- Runtime is an execution layer candidate, not a Pal owner.

## More Failure Variants

- Seeing a model profile and forcing high reasoning for every task.
- Seeing a Skill profile and invoking the Skill without permission or evidence.
- Seeing a Pal profile and treating it as a permanent owner rule.
- Reading all profiles by default before understanding the user task.

## Correct Pattern

1. Perform Task Judgement first.
2. Decide whether a profile would help.
3. Read the smallest relevant profile.
4. Treat the profile as one input.
5. Output candidates and evidence needs.
6. Keep current v0.2 in Simple Pal Mode.

## Acceptance Criteria

- The response uses candidate language.
- Current Runtime evidence is required for execution claims.
- No profile becomes a task/domain route table.
- No automatic scanning or Deep Conductor behavior is claimed.
