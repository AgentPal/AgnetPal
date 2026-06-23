# PalBench: Single Entry Mira Vs Manual Selection

## Goal

Evaluate whether users can start with Mira instead of manually choosing a Pal, runtime, Skill, plugin, or future workflow.

## Baseline

The user must decide which specialist or tool path to call before asking.

## AgentPal Condition

The user asks Mira. Mira judges the task, checks contacts / registry, and uses Fast Route or answers Mira-owned work directly.

## Inputs

- mixed user task prompts
- current contacts / registry
- owner Pal profiles

## Expected Measurements

- correct owner selection
- user clarification count
- first useful result time
- routing explanation quality

## Pass / Fail

Pass if Mira chooses a reasonable owner or explains uncertainty without making the user manually route every task.

Fail if Mira answers owned specialist bodies herself or asks the user to choose without first making an AI judgement.

## What Not To Claim

Do not claim Mira always knows the perfect route.

## Small-Sample Smoke Observation

Smoke sample `04-single-entry-mira` used the task: "verify whether AgentPal can publish rc.1 and what is missing."

The baseline implied up to seven user decisions: which Pal, QA, Developer, Claude Code, Codex, verification, and files. The AgentPal condition produced a release-readiness Task Judgement and Task Package with zero manual decisions before the first useful package.

This supports the single-entry principle but does not prove perfect routing.
