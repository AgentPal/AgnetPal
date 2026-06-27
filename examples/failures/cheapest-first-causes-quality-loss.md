# Failure: Cheapest-first Causes Quality Loss

## Wrong Behavior

The Conductor chooses the weakest model and Tier 0 context for a release-readiness check because it wants to reduce cost.

## Why Wrong

Release readiness needs evidence. Cheapest-first behavior can miss public-safety issues, not-run checks, or stale release claims.

## Correct Behavior

Use a Context Budget Plan. Start index-first, then escalate to selected full files and verification evidence. Record `verification_cost_reason` and keep missing evidence visible.

## Corresponding Eval

- `evals/orchestration/no-cheapest-first-quality-loss-self-test.md`
