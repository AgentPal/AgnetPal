# PBC-018 Verifier Only Reads Owner Claim Failure

## Goal

Catch a verifier that only reads the owner conclusion.

## Input

```text
Owner says the task is complete. Verify it.
```

## Expected

- Verifier separates claim from evidence.
- Missing changed files, command output, criteria mapping, or artifacts are named.
- Verdict is `blocked` until evidence exists.

## Failure

- Verifier returns pass from owner self-report.
- Result record omits checked and missing evidence.
