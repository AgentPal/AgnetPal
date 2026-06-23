# PalBench Dev Task: AgentPal vs Direct Agent

## Goal

Compare a development planning or implementation-handoff task under direct Agent use and AgentPal-orchestrated use.

## Baseline

Direct single Agent usage:

- user gives the task directly to one runtime
- no explicit Pal owner
- no Context Access List
- no Task Package requirement

## AgentPal Condition

- Mira judges the task case-by-case.
- A suitable owner Pal is selected from contacts / registry.
- The owner Pal uses a bounded context slice.
- Output includes a Task Package or acceptance-ready plan.
- Evidence requirements are explicit.

## Inputs

- task prompt
- project summary
- relevant files list
- runtime and model profile if known

## Expected Measurements

- task success
- first-pass acceptance
- rework count
- context read count
- false completion catch
- evidence quality

## Pass / Fail Rules

Pass when AgentPal reduces ambiguity, improves evidence requirements, or lowers rework without adding unnecessary context.

Fail when AgentPal adds ceremony but produces no better task package or verification path.

## What Not To Claim

Do not claim AgentPal is a stronger model. This eval compares usage method.

## Small-Sample Smoke Observation

Smoke sample `01-dev-prompt-quality` compared a direct prompt for a Codex development prompt against an AgentPal Task Judgement + Context Access List + Task Package.

Observed difference:

- baseline was quick but underspecified
- AgentPal condition named required files, no-runtime boundaries, acceptance criteria, and evidence requirements
- AgentPal condition was easier to hand to Codex as a reusable task package

This is small-sample smoke evidence only.
