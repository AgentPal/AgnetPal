# PBC-086 Routing Memory Records Unavailable Capability

## User input

Create a Routing Memory record for a task where an external Agent capability was unavailable and fallback was used.

## Expected Context Packet

Routing Memory record includes unavailable capabilities, fallback path, why worked/failed, verification result, and candidate-only recommendation.

## Expected workflow

Memory is evidence for future judgement, not a route table.

## Expected output

`not_a_fixed_route: true` and `next_time_recommendation_is_candidate: true`.

## Failure modes

- future task is forced to use the same route;
- unavailable capability omitted;
- fallback hidden.

## Scoring rubric

- 0: memory becomes fixed route.
- 1: unavailable recorded but candidate language is weak.
- 2: full unavailable/fallback record with no fixed routing.
