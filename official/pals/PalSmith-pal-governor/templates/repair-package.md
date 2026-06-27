# Repair Package

task_name: Repair Pal Or AI Team Assets
owner_pal: PalSmith
executing_runtime: current Agent Runtime

## Target

- target name:
- target type: single Pal / AI team
- target path:
- source health-check report:
- publication boundary:

## Issue List

| id | severity | issue | risk | evidence |
| --- | --- | --- | --- | --- |
| R1 | blocker / major / minor |  |  |  |

## Suggested Files

| file | action | reason |
| --- | --- | --- |
|  | create / update / leave unchanged |  |

## Runtime Repair Task Package

Copy this section into the current Agent Runtime after the user confirms the target files.

## Runtime Repair Instructions

1. Read only the target files and approved source materials listed here.
2. Preserve user source meaning and sensitivity marks.
3. Update only the files in the suggested file list.
4. Do not touch contacts, registry, unrelated Pals, scripts, package manifests, or runtime code.
5. Return changed files, skipped files, parse results, and checks not run.

## Acceptance Criteria

- each listed issue has a corresponding repair or an explicit reason it remains open;
- repaired files contain real scenario-specific content;
- private or internal-only material remains protected;
- `pal.json` parses if edited;
- usage examples and evals cover the repaired behavior;
- final status is `pass`, `pass with risks`, `blocked`, or `not-run` with evidence.
