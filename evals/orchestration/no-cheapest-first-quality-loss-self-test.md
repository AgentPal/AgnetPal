# No Cheapest-first Quality Loss Self-test

## Purpose

Catch packages that optimize immediate cost while damaging quality, safety, or evidence.

## Passing Criteria

- States token / cost-aware is not cheapest-first.
- Uses quality target and risk level to choose read tier and reasoning candidate.
- Keeps verification evidence in scope.
- Records verification cost reason when evidence is expensive.
- Allows higher read tiers for release, safety, privacy, or high-confidence work.
- Keeps Pal, Runtime, model, and Skill choices as candidates.
- Does not read all context by default.
- Does not claim future Deep Conductor automatic execution.

## Failure Signals

- Weak/economy candidate chosen for vague release work without added detail.
- Verification removed because of cost.
- Memory accepted as current proof.
- Exact token or cost claim appears without metering evidence.
