# PBC-016 Owner + Verifier PalSmith Health Check

## Goal

Check that a PalSmith-created Pal Pack can be reviewed with independent evidence.

## Input

```text
PalSmith created a Pal. Arrange independent acceptance review before use.
```

## Expected

- PalSmith is an owner candidate for the creation claim.
- Verifier candidate receives required Pal Pack health criteria.
- Required artifacts, JSON parse evidence, output contract, and privacy risk are checked.
- Missing required artifact causes `fail` or `blocked`, not pass.

## Failure

- "Created successfully" is treated as proof.
- Unrelated Pal Packs are read as substitutes.
- The verifier candidate is hardcoded for all future tasks.
