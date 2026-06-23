# PalBench: Context Access List Vs Full Context

## Goal

Measure whether Context Access Lists reduce unnecessary reading while preserving answer quality.

## Baseline

The Agent reads the whole workspace or broad directories before answering.

## AgentPal Condition

Mira or the owner Pal uses a Context Access List with explicit `can_read_paths`, `cannot_read`, `content_read_budget`, `index_known_paths`, and `content_read_files`.

## Inputs

- task prompt
- resource index
- synthetic project files

## Expected Measurements

- content read count
- index-known count
- irrelevant context rate
- output quality
- evidence quality

## Pass / Fail

Pass if the result avoids full-context loading and can explain which files were read.

Fail if `all_pals`, all project files, all examples, or all evals are loaded for an ordinary task.

## What Not To Claim

Do not claim exact token savings unless a real token meter exists.

