# PBL-016 - Create Professional Pal From Goal

## Category

PalSmith / AI team.

## User Input

```text
/pal PalSmith Create a professional Pal for customer-support workflow design from my goal and examples.
```

## Baseline Behavior

A direct assistant may produce a shallow persona or a few generic files without source preservation, output contract, examples, evals, or health review.

## Expected AgentPal Behavior

PalSmith is the speaking Pal. PalSmith frames the creation as no-code Pal asset governance, asks high-impact questions, preserves user material boundaries, and prepares a Runtime Task Package for approved file creation.

## Required Assets / Context

- PalSmith creation guidance.
- User goal and examples.
- Approved write target only after confirmation.
- Current contacts / registry only for proposed registration checks, not automatic writes.

## Expected Task Judgement

- domain_focus: single professional Pal creation.
- selected owner: PalSmith for Pal asset governance.
- runtime_candidates: file-editing runtime only after user approves target path and package.
- verification_needs: root files, output contract, real examples, evals, no private data leakage, health check.

## Expected Output Shape

- creation questions;
- proposed Pal job and not-responsible-for boundary;
- asset plan;
- Runtime Task Package;
- health-check and repair expectations.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| owner_judgement | Generic assistant creates persona. | PalSmith speaks but misses governance boundary. | PalSmith owns no-code asset package. |
| task_understanding | Creates shallow role text. | Includes files but weak source mapping. | Preserves goal, examples, boundaries, and health review. |
| task_package_quality | No executable package. | Package lacks reads/writes/evidence. | Complete creation package with allowed scope. |
| verification_quality | No health check. | Basic checklist. | Root files, examples, evals, privacy, and repair evidence. |
| no_future_as_current | Claims auto installer/importer. | Vague. | Runtime execution is separate and evidence-backed. |

## Failure Modes

- Empty Skills or examples are created to satisfy structure.
- Contacts / registry are edited automatically inside the first package.
- User materials are compressed into vague personality notes.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
