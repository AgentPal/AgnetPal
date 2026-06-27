# R71 Clean-Copy Validation

## Purpose

Record the R71 pre-release clean-copy checks for the R68/R69/R70 directory governance changes.

This is not a release, tag, commit, scanner, validator, installer, or automated background service. It is a manual/evidence checklist for a clean copy assembled from Git-visible files.

## Required Entry Paths

- `README.md`
- `AGENTS.md`
- `PAL.md`
- `SKILL.md`
- `agentpal.json`
- `RESOURCE_INDEX.md`
- `standards/boundaries/`
- `standards/project-binding/`
- `standards/organization/`
- `standards/routing-and-judgement/`
- `official/pals/`
- `workspace/organization/contacts/pals.json`
- `workspace/projects/projects.index.json`
- `workspace/projects/_template/project.json`
- `templates/project-binding/generic-codex/.agentpal/project.json`
- `templates/project-binding/generic-codex/.agentpal/AGENTPAL.md`
- `templates/project-binding/claude-code/`
- `docs/01-getting-started/bind-external-project.md`
- `docs/02-concepts/central-project-record.md`
- `evals/palbench/project-binding/`
- `evals/palbench/central-roster/`
- `evals/palbench/no-keyword-routing/`
- `archive/migration-from-v0.3/`

## Git-Visibility Expectations

- `official/pals/` public Pal Pack assets are visible to Git.
- `official/pals/*/state/*`, private memory, and non-placeholder reports are ignored or moved to archive.
- `workspace/projects/README.md`, `workspace/projects/projects.index.json`, and `workspace/projects/_template/**` are visible.
- Real `workspace/projects/<project-id>/` records are ignored by default.
- `release/fresh-clone-checks/` is visible.

## R71 Result

Checked on 2026-06-27.

- Clean copy location: local temporary directory, not recorded in public release evidence.
- File copy source: `git ls-files --cached --modified --others --exclude-standard`, filtered to files that exist in the current worktree.
- Copied file count: 2745
- Clean copy file count: 2745
- Required path check: pass, 0 missing paths.
- JSON parse: pass, 49 `.json` files parsed with 0 failures.
- Thin binding check: pass. Thin binding terms were present in project-binding templates and standards; required template paths existed in the clean copy.
- No keyword routing check: pass by classification. `keyword_map`, `domain_map`, and `role_map` hits were limited to forbidden, boundary, template-check, release-check, or regression-test contexts.
- Private/runtime leak check: pass. Probes for `.git`, root `.agentpal`, `exports`, private workspace project records, Pal private memory, and runtime state returned 0 leaks.
- Result: pass for R71 clean-copy preflight. This is not a remote fresh clone because R68/R69/R70/R71 changes are not committed yet.
