# R144 Local Official Pal Asset Behavior Validation

Status: passed
Date: 2026-06-29

## Validation Summary

| Check | Result | Evidence |
| --- | --- | --- |
| Git branch/status captured | pass | `master...origin/master [ahead 97]`; R144 public files were local changes only before commit |
| Visible JSON parse | pass | 105 JSON files parsed, 0 failures |
| `agentpal.json` parse | pass | included in visible JSON parse |
| Central roster parse | pass | 9 registered Pals, 9 active registered Pals |
| Official Pal directory count | pass | 9 official Pal directories |
| Official Pal `pal.json` parse | pass | 9 parsed, 0 failures |
| R144 result files | pass | 9 files under `evals/palbench/v0.5/behavior/r144-official-pal-asset-results/` |
| R144 test rows | pass | 72 test rows found |
| Summary / issues / readiness files | pass | all expected R144 summary, issue, validation, and readiness files present |
| Central contacts unchanged | pass | `git status --porcelain=v1 -- workspace/organization/contacts` returned no changes |
| Official Pal assets unchanged | pass | `git status --porcelain=v1 -- official/pals` returned no changes |
| No executable or code paths added | pass | changed paths are Markdown / JSON / directory entries only |
| Internal report path leak scan | pass | 0 matches for private workspace markers, internal report directory names, or internal report path strings in the public tree |
| Hidden release claim scan | pass | 2 historical negative/context hits only: R74 `tag created in R74: no` and R143 validation note |
| Route program expansion scan | pass | raw hits are existing standards, schemas, and negative examples that forbid keyword routing; no active route map or new deterministic router was added |
| Forbidden true flags | pass | 0 matches for connector/scanner/marketplace/auto-execution/keyword-routing/credential/customer-private true flags |
| Credential-shaped string scan | pass | 10 raw matches, all documented fake `DO_NOT_USE_EXAMPLE_TOKEN` negative examples or prior validation notes |
| External `.agentpal/delivery-pack` write scan | pass | 0 delivery-pack directories found under sibling external project `.agentpal` paths |
| Clean-copy validation | pass | clean copy `../agentpal-r144-clean-20260629-133816`, robocopy exit 1, 105 JSON parsed, 9 result files, 72 test rows |

## Result Counts

| Metric | Count |
| --- | ---: |
| Official Pals tested | 9 |
| R144 tests executed | 72 |
| Pass | 72 |
| Partial | 0 |
| Fail | 0 |
| Blocked | 0 |
| Not-run | 0 |
| Blocker issues | 0 |
| High issues | 0 |
| Medium issues | 0 |
| Low issues | 0 |
| Note issues | 1 |

## R142 Path Note

The R144 prompt referenced R142 files under `evals/palbench/v0.5/behavior/`. The current repository stores the R142 matrices and rubric under `evals/palbench/v0.5/`. The run used the existing current paths and records the path drift as `R144-NOTE-01`.

## Remote Boundary

No `git push`, `git pull`, `git fetch`, tag creation, GitHub Release creation, GitHub API publication, or remote synchronization was performed.

## Decision

`ready_for_capability_writeback_behavior_tests`
