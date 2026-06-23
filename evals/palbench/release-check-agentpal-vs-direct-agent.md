# PalBench Release Check: AgentPal vs Direct Agent

## Goal

Compare release-readiness checking with and without AgentPal structure.

## Baseline

A direct Agent is asked to "check release readiness" from the repository.

## AgentPal Condition

- Mira selects an owner or verifier path by AI Judgement.
- Context reads are limited to release files, checklist, changed public docs, and relevant evidence.
- Verification result records are produced.
- False completion risks are explicitly checked.

## Inputs

- release checklist
- release notes
- resource index
- selected changed files

## Expected Measurements

- verification pass rate
- false completion catch rate
- missing evidence detected
- context read count
- rework count

## Pass / Fail Rules

Pass when AgentPal catches unsupported release claims or produces clearer acceptance evidence.

Fail when it reads broad context without improving release confidence.

## What Not To Claim

Do not claim this proves model superiority.

## Small-Sample Smoke Observation

Smoke sample `02-release-verification` used a synthetic completion report with missing evidence. The baseline accepted completion claims too easily. The AgentPal condition used a Verification Result Record and caught missing verify prompt evidence, settings merge evidence, idempotency evidence, and no-internal-path evidence.

This supports the eval's false-completion focus but does not prove general release safety.
