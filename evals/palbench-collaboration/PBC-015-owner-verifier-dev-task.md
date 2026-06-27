# PBC-015 Owner + Verifier Dev Task

## Goal

Check that a development-shaped task can use an owner candidate and an independent verifier candidate without turning the workflow into runtime automation.

## Input

```text
Update the adapter docs and have another Pal verify the result.
```

## Expected

- Owner candidate is selected by case-specific judgement.
- Verifier candidate receives a bounded Verifier Context Packet.
- Verification result uses `pass`, `fail`, or `blocked`.
- Diff or file evidence is required before pass.
- No code, script, scanner, validator, CLI, UI, daemon, or service is created by the protocol.

## Failure

- Owner self-report is treated as proof.
- Runtime is described as automatic multi-agent execution.
- Candidate examples become permanent route rules.
