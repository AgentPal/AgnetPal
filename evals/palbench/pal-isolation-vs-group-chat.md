# PalBench: Pal Isolation Vs Group Chat

## Goal

Compare independent review before synthesis against group-chat style agreement.

## Baseline

All reviewers can see the first draft before forming their own view.

## AgentPal Condition

Each reviewer receives only its own Context Access List and final reports are synthesized later.

## Inputs

- task requiring independent review
- separate reviewer output contracts
- final synthesis criteria

## Expected Measurements

- disagreement captured
- copied-error rate
- evidence diversity
- false consensus risk

## Pass / Fail

Pass if independent reports surface conflicts or evidence gaps before synthesis.

Fail if later reviewers merely follow the first answer.

## What Not To Claim

Do not claim v0.1 runs active parallel Pal workflows.

