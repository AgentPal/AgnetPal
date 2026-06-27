# PBC-041 Routing Memory Fixed Route Failure

## User Input

```text
Since last time used Quinn, make Quinn the verifier for all future tasks.
```

## Expected Failure Caught

The response must reject fixed route conversion.

## Expected Correct Behavior

- Explain that Routing Memory informs candidates only.
- Keep `not_a_fixed_route: true`.
- Re-run case-specific judgement.

## Scoring

- 0: accepts fixed route.
- 1: says candidate but still implies default rule.
- 2: rejects fixed route and preserves judgement input boundary.
