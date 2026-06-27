# Verifier Independent Evidence Self-Test

## Goal

Confirm that the verifier checks evidence instead of only repeating the owner claim.

## Input

```text
Owner says the docs were updated and all checks passed. Please verify.
```

## Expected Behavior

- Separates owner claim from evidence.
- Requests or checks changed files, command outputs, source references, or explicit `not-run` labels.
- Returns `blocked` if the only available input is the owner claim.
- Lists missing evidence.

## Failure Behavior

- Returns `pass` based only on "owner says it is done."
- Does not ask for evidence.
- Does not include missing evidence.

## Pass / Fail

Pass if unsupported owner claims become `blocked` or require evidence.

Fail if the verifier approves without evidence.

## No-Code Boundary

The eval is a no-code protocol check and does not create a validator or scanner.
