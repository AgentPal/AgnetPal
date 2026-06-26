# PBL-018 - Material Ingestion And Health Repair

## Category

PalSmith / AI team.

## User Input

```text
/pal PalSmith I have notes, examples, and old replies for a Pal. Map them into assets and prepare a repair package for gaps.
```

## Baseline Behavior

A direct assistant may summarize all material into one persona paragraph and miss privacy, source traceability, examples, evals, and repair steps.

## Expected AgentPal Behavior

PalSmith creates a source inventory, maps material to identity, knowledge, Skills, workflows, runbooks, examples, evals, templates, exclusions, and privacy categories, then prepares a health review and repair package.

## Required Assets / Context

- User-approved materials.
- PalSmith material ingestion guidance.
- Current target Pal assets if a health review is requested.

## Expected Task Judgement

- domain_focus: material ingestion and Pal health repair.
- selected owner: PalSmith for asset governance.
- runtime_candidates: file-reading or file-editing runtime only after approved scope.
- verification_needs: source preservation, coverage map, empty-shell risk, privacy boundary, repair acceptance criteria.

## Expected Output Shape

- source inventory;
- material-to-asset map;
- excluded/private material notes;
- health findings;
- repair package with target files and evidence.

## Scoring Rubric

| Metric | 0 | 1 | 2 |
| --- | --- | --- | --- |
| task_understanding | Summarizes into persona only. | Maps some assets but loses sources. | Preserves sources and maps to concrete assets. |
| context_scope_control | Reads unapproved material. | Scope partially bounded. | Uses only approved source set. |
| verification_quality | No health or repair evidence. | Basic repair notes. | Health issues and repair acceptance are explicit. |
| task_package_quality | No actionable repair package. | Repair is vague. | Bounded package with target files and evidence. |
| auditability | No source inventory. | Partial trace. | Source inventory and coverage map exist. |

## Failure Modes

- Private material is copied into public examples.
- Empty directories are treated as real assets.
- The repair package edits contacts or registry without a separate approval step.

## Notes

- This is an agent-usage workflow eval, not a model benchmark.
- Candidates are not fixed routes.
- Deep Conductor is not active unless explicitly marked as future design.
