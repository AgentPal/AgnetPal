# Context Slicing

Context Slicing is AgentPal's method for loading only the context needed for the current task.

The goal is not to read everything. The goal is to read the right slice and make that slice auditable.

## Status

- Current: Active in v0.1.0-rc.1 for initialization, owner Pal loading, project file loading, and memory use.
- Future: Context Access Lists may make slices explicit per workflow step.
- Research: PalBench can measure content-read count, irrelevant context rate, and context access compliance.

## Why it exists

Large context is not automatically better context. Full-workspace loading can:

- waste tokens
- leak unrelated private information
- mix unrelated tasks
- make verification harder
- cause a Pal to answer from stale or irrelevant material

Context Slicing keeps the working set small and explainable.

## How it works

AgentPal separates context into levels:

- Root minimum: workspace guardrails, metadata, contacts, registry, Mira minimum assets, and the Runtime Response Gate.
- Owner Pal minimum: selected Pal identity, entry files, and Output Contract.
- Relevant Pal assets: one to three task-relevant Skills, knowledge cards, runbooks, workflows, or fallback method.
- Project slice: only files or directories needed for the task.
- Memory slice: zero to two relevant summaries by default, with privacy review.

AgentPal also separates:

- `index_known`: paths discovered through registry, index, or file listing
- `content_read`: files actually opened and used as content

## What it is not

- Not a command to read every file listed in an index.
- Not exact token metering.
- Not a privacy bypass.
- Not a claim that unknown files were reviewed.
- Not a reason to ignore user-provided context.

## Practical rule

If a file did not affect the current answer, do not load it just because it exists.

If a path is only known from an index, do not describe it as content that was read.

