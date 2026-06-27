# Failure: Skips Verification To Save Token

## Wrong Behavior

The package omits tests, source checks, screenshots, or release evidence because verification would increase context.

## Why Wrong

Verification is necessary quality cost. Missing evidence cannot become a pass.

## Correct Behavior

Record the smallest sufficient verification context. If checks cannot run, mark `not-run` or `blocked`.

## Corresponding Eval

- `evals/orchestration/context-budget-plan-self-test.md`
- `evals/orchestration/context-usage-report-self-test.md`
