# R146 Local Deep Conductor E2E Behavior Validation

Status: passed
Date: 2026-06-29

## Validation Summary

| Check | Result | Evidence |
| --- | --- | --- |
| Git branch/status captured | pass | `master...origin/master [ahead 99]`; R146 files were local changes only before commit |
| Mode decision results exist | pass | `evals/palbench/v0.5/behavior/r146-deep-conductor-mode-decision-results.md` |
| Context / Task / Governance / Verification results exist | pass | `evals/palbench/v0.5/behavior/r146-context-task-governance-verification-results.md` |
| E2E results exist | pass | `evals/palbench/v0.5/behavior/r146-end-to-end-human-use-results.md` |
| Summary exists | pass | `evals/palbench/v0.5/behavior/r146-deep-conductor-e2e-behavior-summary.md` |
| Issues exists | pass | `evals/palbench/v0.5/behavior/r146-deep-conductor-e2e-behavior-issues.md` |
| All required tests executed | pass | 16 mode rows, 8 artifact rows, 10 E2E rows, 34 total rows |
| Visible JSON parse | pass | 105 JSON files parsed, 0 failures |
| `agentpal.json` parse | pass | included in visible JSON parse |
| Central roster parse | pass | 9 registered Pals, 9 active registered Pals |
| Official Pal directory count | pass | 9 official Pal directories |
| Official Pal `pal.json` parse | pass | 9 parsed, 0 failures |
| Central roster unchanged | pass | `git status --porcelain=v1 -- workspace/organization/contacts` returned no changes |
| Official Pal `pal.json` unchanged | pass | `git status --porcelain=v1 -- official/pals` returned no changes |
| No keyword routing | pass | raw hits are standards, schemas, negative examples, and R146 tests that forbid keyword routing; no active route map was added |
| No runtime scanner added | pass | no scanner-named changed path and no forbidden true flag |
| No connector / marketplace / program expansion | pass | no connector/scanner/marketplace/hub/daemon/installer/app/web changed path and no forbidden true flag |
| No executable code added | pass | changed paths are Markdown and JSON only |
| No credential leak | pass | 12 raw credential-shaped matches are the documented fake `DO_NOT_USE_EXAMPLE_TOKEN` negative example and prior validation notes |
| No customer-private leak | pass | raw customer-private matches are boundary standards, public-safe examples, and R146 prompt/regression rows; no real customer data was added |
| No internal path leak | pass | 0 matches for private workspace markers or internal report path strings in the public tree |
| No external project write | pass | 0 delivery-pack directories found under sibling external project `.agentpal` paths |
| Clean-copy validation | pass | clean copy `../agentpal-r146-clean-20260629-154500`, robocopy exit 1, 105 JSON parsed, 16/8/10 test rows |

## Result Counts

| Metric | Count |
| --- | ---: |
| Deep Conductor mode decision tests | 16 |
| Context / Task / Governance / Verification tests | 8 |
| End-to-end human-use tests | 10 |
| Total R146 tests executed | 34 |
| Pass | 34 |
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

The R146 prompt referenced R142 auto-test files under `evals/palbench/v0.5/behavior/`. The current repository stores the active R142 Deep Conductor and E2E matrix/rubric files under `evals/palbench/v0.5/`. The run used the existing current paths and records the path drift as `R146-NOTE-01`.

## Remote Boundary

No `git push`, `git pull`, `git fetch`, tag creation, GitHub Release creation, GitHub API publication, or remote synchronization was performed.

## Decision

`ready_for_auto_test_summary_and_fix_decision`
