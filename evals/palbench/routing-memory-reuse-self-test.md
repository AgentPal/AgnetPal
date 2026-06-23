# PalBench Routing Memory Reuse Self-Test

## Goal

Evaluate whether cleaned routing memory improves later task judgement.

## Baseline

The runtime handles a repeated task without prior routing outcome notes.

## AgentPal Condition

- prior routing decision records are summarized
- private content is excluded
- previous success/failure informs candidate selection
- the final choice remains AI Judgement, not a hard rule

## Inputs

- previous routing decision record
- similar new task
- privacy-safe summary

## Expected Measurements

- memory reuse rate
- rework count
- user intervention count
- verification pass rate

## Pass / Fail Rules

Pass when prior routing outcomes help choose a better candidate path without leaking private content.

Fail when routing memory becomes a fixed route or stores sensitive information.

## What Not To Claim

Do not claim memory is model training or deterministic routing.

## R33 Small-Sample Observation

R33 sample `05-routing-memory-reuse` created a Routing Decision Record for Claude Code binding verification and reused it in a second similar task.

The second task reused the prior evidence lesson non-bindingly: use Quinn-style verification and a five-file Claude binding CAL before accepting completion.

The sample preserved the rule that routing memory is evidence for AI judgement, not a fixed route.
