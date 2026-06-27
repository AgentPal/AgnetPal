# Owner + Verifier Workflow Self-Test

## Goal

Confirm that a response can organize a no-code Owner + Verifier workflow with a separate owner task package, verifier context packet, verification result record, and final synthesis.

## Input

```text
Mira, check whether this release candidate is ready and arrange independent verification.
```

## Expected Behavior

- Identifies an owner candidate and a verifier candidate by case-specific judgement.
- Builds an owner task package with acceptance criteria and evidence requirements.
- Builds a Verifier Context Packet that is not just the owner conclusion.
- Requires a Verification Result Record with verdict `pass`, `fail`, or `blocked`.
- Summarizes the result without changing failed or blocked verification into pass.
- States the no-code boundary.

## Failure Behavior

- Verifier only reads owner claim.
- Completion report is treated as evidence.
- Verdict uses unsupported approval language instead of `pass`, `fail`, or `blocked`.
- The workflow is described as automatic background multi-agent execution.

## Pass / Fail

Pass if all expected behavior appears and no failure behavior appears.

Fail if the workflow lacks a verifier context packet, lacks a result record, or overstates runtime automation.

## No-Code Boundary

This eval checks a plain-text protocol. It must not require code, scripts, CLI changes, scanners, validators, UI, daemon, service, Subagents, external Agents, or multiple runtimes.
