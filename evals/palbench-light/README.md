# PalBench Light

PalBench Light is the v0.2 release regression suite for AgentPal behavior. It is a reusable Markdown case set for checking Agent usage workflows, Pal-layer organization, context scope, Task Package quality, handoff judgement, verification honesty, no-code boundary, runtime adapter stability, Capability Inventory use, and official Pal example references.

It is not a statistically significant benchmark, not a model benchmark, and not a comparison of GPT, Claude, Gemini, Fable, or any other underlying model. It does not prove AgentPal improves all tasks.

## Start Here

- `task-index.md`: case list and categories.
- `scoring-rubric.md`: shared 0 / 1 / 2 scoring.
- `case-template.md`: template for new cases.
- `palbench-light-suite-self-test.md`: release self-test for the suite itself.

## Categories

- `mira-first/`: default entry, owner judgement, release coordination, assignment explanation.
- `direct-pal/`: explicit `/pal Name` calls and fake-Pal prevention.
- `composite-deliverable/`: staged judgement for multi-deliverable work.
- `context-scope/`: Context Slicing and stage-level Context Access Lists.
- `verification/`: false completion, release evidence, and install/update proof.
- `palsmith/`: Pal and AI team creation, material ingestion, health repair.
- `runtime-adapters/`: thin binding and project-root separation.
- `capability-inventory/`: profiles as judgement inputs, not fixed routes.

## Run Notes

For each release dry run, record the case id, runtime, model when known, response or response summary, score per metric, judge notes, and `not-run` checks. Scores are qualitative regression signals only.

Current AgentPal behavior remains Simple Pal Mode. The cases do not activate Deep Conductor, Subagent Mode, automatic multi-runtime execution, scanners, validators, CLI, UI, or daemons.
