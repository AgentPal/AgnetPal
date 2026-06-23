# Asset Loading Budget

Asset Loading Budget is AgentPal's policy for limiting how many Pal assets, project files, memory summaries, examples, evals, and reports are read for a task.

It is the operational side of Context Slicing.

## Status

- Current: Active in v0.1.0-rc.1 as a loading policy and reporting convention.
- Future: May become enforceable through Context Access Lists and workflow records.
- Research: PalBench can record budget compliance and unnecessary context use.

## Why it exists

Every Pal Pack can contain identity files, Skills, knowledge, runbooks, workflows, examples, evals, reports, memory placeholders, and learning records.

Reading all of it by default would make AgentPal slower, noisier, less private, and less auditable.

## How it works

Default owner Pal loading:

- required entry files: `PAL.md`, `AGENTS.md`, `SKILL.md`, `pal.json`, and `core/output-contract.md`
- Level 1 indexes when present: Skills, knowledge, runbooks, workflows
- Level 2 task assets: usually one to three relevant assets
- project files: only the files needed for the task
- memory summaries: zero to two relevant summaries by default

For audits, AgentPal may report:

- required assets read
- optional assets read
- project files read
- memory summaries read
- assets skipped
- fallback used
- context budget status

## What it is not

- Not a hard token counter.
- Not a reason to under-read safety-critical files.
- Not a replacement for user approval on sensitive data.
- Not proof that skipped files were irrelevant forever.
- Not permission to claim an asset was used when it was only listed.

## Budget principle

Start small. Expand only when the current answer needs more evidence.

When expanding, name the missing slice rather than loading a broad directory.

