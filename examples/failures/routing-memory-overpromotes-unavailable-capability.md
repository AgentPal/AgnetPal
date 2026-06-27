# Failure Example: Routing Memory Overpromotes Unavailable Capability

## Bad Pattern

```yaml
next_time_recommendation: Always use an external Agent for this task type.
not_a_fixed_route: false
```

## Why It Fails

The previous task did not prove external Agent availability. If the host Runtime reported `unavailable`, `unknown`, or `blocked`, Routing Memory may record that fact only as candidate guidance.

## Correct Pattern

```yaml
unavailable_capabilities:
  - capability: external Agent handoff
    type: external agent
    status: unavailable
    evidence_or_reason: current host Runtime did not support approved external Agent calls
fallback_path:
  used: true
  description: manual handoff package
  result: partial
next_time_recommendation: Recheck host Runtime availability before considering external Agent handoff.
next_time_recommendation_is_candidate: true
not_a_fixed_route: true
```

## Regression Check

Routing Memory must never convert an unavailable capability into a mandatory future route.
