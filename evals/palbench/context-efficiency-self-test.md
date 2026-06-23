# PalBench Context Efficiency Self-Test

## Goal

Verify that AgentPal improves or preserves context efficiency compared with direct broad loading.

## Baseline

A direct Agent is allowed to read a broad project or workspace context.

## AgentPal Condition

- uses `RESOURCE_INDEX.md` or local indexes as navigation
- records index-known paths separately from content-read files
- reads only task-relevant files

## Inputs

- same task prompt
- same project/workspace

## Expected Measurements

- index-known count
- content-read count
- skipped assets
- irrelevant context rate

## Pass / Fail Rules

Pass when AgentPal completes the task with smaller or better-justified content reads.

Fail when AgentPal reads all Pals, all memory, all examples, or all project files without need.

## What Not To Claim

Do not claim exact token savings unless a real token meter exists.

## Small-Sample Smoke Observation

Smoke sample `03-context-efficiency` compared a broad allowed context set with a five-file Context Access List for Claude Code install review.

Observed difference:

- baseline allowed 90+ candidate files across broad groups
- AgentPal condition used a five-file content-read budget
- unrelated Pal persona files, future design docs, private memory, and all-project reads were explicitly excluded

This is file-scope evidence only, not exact token measurement.
