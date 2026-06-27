# R71 Staging Readiness

## Case ID

R71-STAGING-READINESS

## Goal

Verify that the R68/R69/R70 dirty worktree can be reviewed through clear staging groups before any commit, push, tag, or release.

## Setup

- Worktree contains the R68/R69/R70 directory governance changes.
- No `git add`, commit, push, tag, or release is performed during this case.

## Evidence Paths

- `.gitignore`
- `README.md`
- `RESOURCE_INDEX.md`
- `standards/`
- `official/pals/`
- `workspace/organization/contacts/`
- `workspace/projects/`
- `templates/project-binding/`
- `evals/palbench/`
- `release/fresh-clone-checks/`
- `archive/migration-from-v0.3/`

## Expected Result

- A staging plan separates repo architecture, official Pals and central roster, thin project binding, central project record, PalBench/evidence, and release readiness.
- Each group names its purpose, public-safety status, runtime/private risk, and extra review needs.
- No staging or commit action occurs.

## Forbidden Result

- All files are staged as one opaque change.
- Runtime/private files are included without review.
- The case claims release readiness without checking Git visibility and ignored files.
- A commit, push, tag, or Release is created.

## R71 Verification Notes

Use `git status --short --branch`, `git diff --stat`, `git diff --name-status`, `git ls-files --others --exclude-standard`, `git ls-files --deleted`, and `git ls-files --modified` as evidence.

