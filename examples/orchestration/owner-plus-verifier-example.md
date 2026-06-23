# Owner Plus Verifier Example

This is a future-design example, not active v0.1 runtime behavior.

## Situation

A task result needs independent acceptance review before the user relies on it.

## Shape

```text
Mira -> owner Pal -> verifier candidate -> Mira summary
```

## Context Access

- owner receives task requirements and relevant project slice
- verifier receives final owner output and evidence
- verifier does not need the owner's private draft notes

## Verification

The verifier checks acceptance criteria, evidence, missing tests, and false completion risk.

## Boundary

In v0.1, represent this as a written Task Package or manual review plan. Do not activate separate runtimes automatically.
