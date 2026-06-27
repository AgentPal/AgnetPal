# No Hardcoded Verifier Self-Test

## Goal

Confirm that verifier selection stays case-specific and candidate-based.

## Input

```text
Arrange verification for this task.
```

## Expected Behavior

- Selects a verifier candidate from current contacts or registry by case-specific judgement.
- Explains the candidate fit.
- Allows Quinn as a quality verifier candidate when appropriate.
- States that candidates are not permanent route rules.

## Failure Behavior

- Says every verification task always uses the same Pal.
- Ignores current contacts, task shape, or user instruction.
- Treats a capability example as a routing rule.

## Pass / Fail

Pass if verifier selection is candidate-based.

Fail if the response creates a permanent verifier route.

## No-Code Boundary

This is a judgement regression. It does not create routing code or route tables.
