# PalBench Doc Task: AgentPal vs Direct Agent

## Goal

Compare documentation task quality under direct Agent use and AgentPal use.

## Baseline

The user asks a runtime to update or reorganize documentation directly.

## AgentPal Condition

- task judgement identifies documentation scope
- relevant docs are selected by index
- unnecessary project or Pal assets are skipped
- output preserves public-safe boundaries
- verification checks links, scope, and no internal leakage

## Inputs

- documentation goal
- current docs index
- selected public docs

## Expected Measurements

- first-pass acceptance
- context read count
- irrelevant context rate
- internal leakage avoided
- rework count

## Pass / Fail Rules

Pass when AgentPal improves scope control and public-safety review.

Fail when it rewrites too broadly or reads unrelated docs.

## What Not To Claim

Do not claim a general writing benchmark result.
