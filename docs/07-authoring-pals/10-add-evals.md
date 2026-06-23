# Add Evals

## Status

Current for AgentPal `v0.1.0-rc.1`.

Evals are small self-checks for Pal behavior and release readiness.

## Minimum

Create:

```text
evals/definition-of-done.md
```

It should say what must be true before this Pal's work is considered complete.

## Useful Eval Checks

- The Pal uses its prefix.
- The Pal follows `core/output-contract.md`.
- The Pal uses an asset or honest fallback.
- The Pal does not claim execution without evidence.
- The Pal protects private memory, state, and reports.
- The Pal does not add non-Pals to contacts.

## Eval File Shape

```md
# Eval Name

## Scenario

## Expected Behavior

## Failure Conditions
```

## Small Is Fine

For `v0.1.0-rc.1`, small public-safe checks are more useful than large unverifiable benchmark claims.
