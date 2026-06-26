# Official Pal Example Library Self-Test

This Markdown self-test checks the v0.2 first implementation of the official 9 Pal real task example library. It is not a script or automated validator.

## Scope

Check these official Pal task directories:

- `pals/Mira-main/examples/tasks/`
- `pals/Atlas-developer/examples/tasks/`
- `pals/Vega-research/examples/tasks/`
- `pals/Rhea-system/examples/tasks/`
- `pals/PalSmith-pal-governor/examples/tasks/`
- `pals/Quinn-quality/examples/tasks/`
- `pals/Morgan-document/examples/tasks/`
- `pals/Harper-writing/examples/tasks/`
- `pals/Nova-product/examples/tasks/`

## Required Checks

| Check | Expected result | Status |
| --- | --- | --- |
| Each official Pal has `examples/tasks/README.md` | pass | manual |
| Atlas, Vega, Rhea, Quinn, Morgan, Harper, and Nova each have at least 3 task examples | pass | manual |
| Mira has at least 4 task examples or equivalent R41 coverage | pass | manual |
| PalSmith has at least 4 task examples or equivalent R40 coverage | pass | manual |
| Every task example includes User Request | pass | manual |
| Every task example includes Task Judgement | pass | manual |
| Every task example includes Context Needs | pass | manual |
| Every task example includes Good Response Example | pass | manual |
| Every task example includes Bad Response Example | pass | manual |
| Every task example includes Verification / Acceptance Criteria | pass | manual |
| Every task example says candidates are not fixed routes | pass | manual |
| Every task example states current v0.2 does not auto-run Deep Conductor | pass | manual |
| Cross-Pal examples exist under `examples/orchestration/` | pass | manual |
| `docs/07-official-pals/official-pal-examples-index.md` exists | pass | manual |
| `docs/07-official-pals/official-pal-example-library-plan.md` lists current R42 status | pass | manual |
| `RESOURCE_INDEX.md` and `docs/README.md` link the official Pal examples index | pass | manual |

## Boundary Checks

| Boundary | Expected result |
| --- | --- |
| No fixed owner rules | Examples use candidates and staged judgement only. |
| No future-as-current | Deep Conductor and automatic multi-agent execution remain inactive. |
| Pal not Agent | Examples describe Pal ownership and Runtime execution separately. |
| Runtime not Pal | Runtime candidates execute only with permission and evidence. |
| No internal paths | Public examples do not contain private local paths or internal development directories. |
| No runtime code | R42 adds Markdown docs/examples/evals only. |

## Negative Patterns To Reject

Reject a change if a public example:

- treats examples as route rules;
- claims a Pal can execute filesystem operations without Runtime evidence;
- presents Deep Conductor as active current behavior;
- adds private user data, credentials, or local absolute paths;
- omits bad response or acceptance criteria.

## Expected Manual Result For R42

Expected result after R42 first implementation: pass, with later expansion still open for more specialized examples and PalBench Light cases.
