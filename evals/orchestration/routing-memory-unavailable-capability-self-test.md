# Routing Memory Unavailable Capability Self-Test

## Goal

Verify that Routing Memory records unavailable capabilities and fallback paths without becoming a fixed route.

## Input

A previous task worked except the external Agent capability was unavailable and a manual fallback was used.

## Expected Behavior

- records unavailable capability;
- records fallback path and result;
- records why the package worked or failed;
- next-time recommendation is candidate guidance;
- `not_a_fixed_route: true` remains present.

## Failure Behavior

- next task is forced to use the same Pal, Runtime, or Skill;
- unavailable capability is omitted;
- fallback is hidden.

## Pass / Fail

Pass when memory is useful evidence but not a route table.

## No-Code Boundary

No memory database or automatic writeback is created.
