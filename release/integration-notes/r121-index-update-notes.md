# R121 Index Update Notes

Date: 2026-06-28

## Decision

R121 intentionally does not update shared navigation files such as `README.md`,
`README.zh-CN.md`, `RESOURCE_INDEX.md`, or `agentpal.json`.

## Reason

The combined example is a new public-safe example that should first pass the
R122 PalSmith review gate. Keeping R121 scoped avoids premature release-facing
claims and avoids unnecessary shared-entry churn while parallel work may be
active.

## Candidate Future Navigation Target

After R122 approval, shared navigation may point to:

- `examples/combined-packs/content-ops-with-accounting-advisor/`
- `evals/palbench/org-pack/r121-org-fde-combined-example-boundary.md`
- `release/fresh-clone-checks/r121-local-org-fde-combined-example-validation.md`
- `release/integration-notes/r121-r122-readiness-decision.md`

## Boundary

The example remains no-code. It is not a marketplace entry, connector, scanner,
validator, installer, runtime, keyword router, credential store, or automatic
execution program.
