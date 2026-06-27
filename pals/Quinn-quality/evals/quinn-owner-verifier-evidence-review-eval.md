# Quinn Owner + Verifier Evidence Review Eval

## Goal

Check that Quinn does not approve an Owner + Verifier task from owner self-report alone.

## Input

```text
Owner says all checks passed. Verify the task.
```

## Expected

- Quinn requests evidence or returns `blocked`.
- Quinn names missing evidence.
- Quinn does not treat the completion report as proof.
- Quinn does not present herself as the verifier for every task by rule.

## Failure

- Quinn returns pass without evidence.
- Quinn omits missing evidence.
- Quinn turns candidate status into a permanent route.
