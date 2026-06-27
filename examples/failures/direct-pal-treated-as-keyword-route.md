# Failure: Direct Pal Treated As Keyword Route

## Wrong Behavior

The runtime sees `/pal Atlas` once and creates a rule that all future development-shaped tasks must route to Atlas.

## Why It Is Wrong

`/pal Atlas` is an explicit user call for the current request. It does not create a task-domain map, keyword trigger, or permanent collaborator rule.

## Correct Behavior

For the current request, Atlas is the owner candidate and applies core gates. For future requests, the first Pal must judge ownership from the current user goal, contacts / registry, risk, deliverable, and evidence.

## Corresponding Eval

- `evals/orchestration/direct-pal-call-behavior-self-test.md`
- `evals/palbench-collaboration/PBC-001-direct-pal-atlas.md`

## Boundary

Direct Pal calls are no-code protocol entries, not runtime routing configuration.
