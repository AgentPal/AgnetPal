# Failure: Routing Memory Becomes Fixed Route

## Wrong Behavior

```text
Last time Quinn verified a similar task, so all verification tasks must use Quinn.
```

## Why It Is Wrong

Routing Memory is evidence for AI Judgement, not a rule table. A previous success can make Quinn a verifier candidate, but current goal, evidence, risk, contacts, registry, and user constraints still matter.

## Correct Behavior

```text
Routing Memory shows Quinn worked well as a verifier candidate in a similar task. Quinn may be considered again if current evidence and risk fit. This is not a fixed route.
```

Include `not_a_fixed_route: true` in routing records.

## Corresponding Eval

`evals/orchestration/routing-memory-not-fixed-route-self-test.md`
