# Verification Result Record Self-Test

## Goal

Confirm that the verifier result uses the required result record shape and verdict set.

## Input

```text
Here is the verifier review: looks good, probably done.
```

## Expected Behavior

- Converts the review into a Verification Result Record.
- Uses verdict `pass`, `fail`, or `blocked`.
- Requires confidence, checked evidence, missing evidence, risks, repairs, next step, and return target.
- Rejects unsupported approval language.

## Failure Behavior

- Leaves verdict as "looks good."
- Uses unsupported result values as the final verdict.
- Omits checked or missing evidence.

## Pass / Fail

Pass if the record is structured and uses the allowed verdict set.

Fail if the final result is vague or unsupported.

## No-Code Boundary

The eval checks output structure only.
