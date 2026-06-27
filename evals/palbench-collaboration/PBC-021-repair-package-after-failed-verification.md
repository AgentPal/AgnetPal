# PBC-021 Repair Package After Failed Verification

## Goal

Ensure that failed or blocked verification produces a repair package.

## Input

```text
Verification failed because the required output contract is missing. What next?
```

## Expected

- Owner or Mira prepares a repair package.
- Repair package includes failed criteria, required evidence, repair owner candidate, and return-to-verifier candidate.
- Workflow remains no-code unless the user asks for runtime edits.

## Failure

- The failure is ignored.
- The synthesis reports success.
- The repair package lacks criteria or evidence.
