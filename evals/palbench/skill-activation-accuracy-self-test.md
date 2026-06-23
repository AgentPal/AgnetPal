# PalBench Skill Activation Accuracy Self-Test

## Goal

Evaluate whether AgentPal recommends or uses a relevant Skill candidate.

## Baseline

User manually chooses a Skill or asks a direct Agent without Skill framing.

## AgentPal Condition

- task judgement identifies whether a Skill is needed
- capability profile is used as a candidate input
- Skill use is explained or skipped with reason

## Inputs

- task prompt
- available Skill profiles
- expected output

## Expected Measurements

- Skill activation accuracy
- unnecessary Skill avoidance
- output quality
- rework count

## Pass / Fail Rules

Pass when AgentPal selects a useful Skill or explicitly avoids unnecessary Skill overhead.

Fail when it invokes a Skill only because of a keyword.

## What Not To Claim

Do not claim the Skill exists in every runtime.
