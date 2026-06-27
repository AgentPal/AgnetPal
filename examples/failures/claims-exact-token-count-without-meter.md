# Failure: Claims Exact Token Count Without Meter

## Wrong Behavior

The Context Usage Report says the task used an exact token count even though the host Runtime did not provide metering evidence.

## Why Wrong

AgentPal's Context Usage Report is qualitative and auditable, not an exact token meter or cost calculator.

## Correct Behavior

Use `not_exact_token_count: true` and report read tiers, file counts, memory used, profiles read, Runtime Skills used, and verification context.

## Corresponding Eval

- `evals/orchestration/no-token-meter-claim-self-test.md`
