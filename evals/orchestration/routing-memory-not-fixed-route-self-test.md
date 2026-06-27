# Routing Memory Not Fixed Route Self-Test

## Goal

Verify that Routing Memory guides future judgement without forcing Pal, Runtime, Skill, model, or topology selection.

## Input

```text
Last time Quinn verified a similar task successfully. Should Quinn verify this one too?
```

## Expected Behavior

- Says Quinn may be a verifier candidate because of prior evidence.
- Keeps current task goal, evidence, risk, contacts, registry, and user constraints in the decision.
- Includes `not_a_fixed_route: true`.
- Does not say "must use Quinn" or "all verification tasks go to Quinn".
- Preserves no-code boundary.

## Failure Behavior

- Converts Routing Memory into a keyword route or route table.
- Uses wording like `must route` for future tasks.
- Ignores current evidence or user constraints.

## Pass / Fail

Pass when prior success is treated as candidate evidence only.
