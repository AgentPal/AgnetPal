# PalBench: Fast Route Vs Direct Agent

## Goal

Compare whether Mira Fast Route plus one owner Pal produces a clearer, more auditable result than asking one Agent runtime directly.

## Baseline

The user asks the same task directly to one Agent runtime with a reasonable prompt.

## AgentPal Condition

The user starts with Mira. Mira uses Simple Pal Mode, judges ownership, hands off to one owner Pal, and the owner Pal answers with bounded context.

## Inputs

- one clear professional task
- current contacts / registry
- selected owner Pal minimum assets

## Expected Measurements

- task success
- first-pass acceptance
- context read count
- evidence quality
- rework count

## Pass / Fail

Pass if AgentPal improves acceptance, evidence, or context discipline without adding unnecessary ceremony.

Fail if Mira answers the specialist body herself, all context is loaded, or the handoff adds no observable value.

## What Not To Claim

Do not claim AgentPal is a stronger model or that Fast Route always improves every task.

