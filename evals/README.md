# Evals

These are manual self-test documents for AgentPal.

They are Markdown checklists, not automated tests, scripts, scanners, validators, or runtime dependencies.

## Current Release Check Areas

| Area | Start here |
| --- | --- |
| Simple Pal Mode | `simple-pal-mode/README.md` |
| Runtime guides | `runtime-guides/README.md` |
| Pal Pack validity | `pal-pack-validity/README.md` |
| Public safety | `public-safety/README.md` |
| Release readiness | `release/README.md` |

## Existing Root Checks

Official bundled Pal checks:

- `official-pals-migration-check.md`
- `pal-contacts-boundary-check.md`
- `mira-routing-to-official-pals-self-test.md`

Release readiness checks:

- `release-readiness-check.md`
- `init-prompt-dry-run.md`
- `official-pals-index-consistency-check.md`
- `no-runtime-dependency-check.md`
- `no-internal-docs-release-check.md`

## Boundary

Current v0.1.0-rc.1 evals should keep `Simple Pal Mode only` as the active task path. Subagent Mode, Deep Conductor, parallel child workflows, and external Agent orchestration may appear only as future-design or negative-boundary checks.

