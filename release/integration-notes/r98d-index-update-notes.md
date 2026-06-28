# R98-D Index Update Notes

## Summary

R98-D adds the first Pal Asset Resolver standard set:

- `standards/pal-asset/pal-loading-order-standard.md`
- `standards/pal-asset/pal-asset-resolver-standard.md`
- `examples/pal-asset/pal-asset-resolver-task-package.example.md`
- `evals/palbench/pal-asset/r98d-pal-asset-resolver-thin-binding-boundary.md`
- `release/fresh-clone-checks/r98d-local-pal-asset-resolver-validation.md`

## Suggested Future Index Updates

These are notes for a later single-thread integration pass. R98-D does not modify shared entry files.

Candidate index targets:

- `RESOURCE_INDEX.md`
- `README.md`
- `docs/00-overview/repository-structure.md`
- `docs/00-overview/capability-inventory-navigation.md`
- any future `standards/pal-asset/README.md`

Suggested additions:

- Add `standards/pal-asset/` as the home for no-code Pal asset loading and resolver standards.
- Add `examples/pal-asset/` as public-safe examples for Pal asset candidate resolution and task package recommendation.
- Add `evals/palbench/pal-asset/` as the PalBench surface for resolver and thin-binding boundary checks.

## Boundary Reminder

Do not turn the resolver standard into:

- keyword routing
- deterministic semantic routing
- resolver code
- scanner
- validator
- connector
- auto execution
- external project `.agentpal/` thick binding
- central roster modification

Org Pack recommendations and Capability Inventory records stay AI judgement inputs only.
