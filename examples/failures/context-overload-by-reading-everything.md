# Failure: Context Overload By Reading Everything

## Wrong Behavior

The Conductor reads every Pal Pack, every example, every eval, every report, and all memory before understanding the task.

## Why Wrong

This wastes context, increases privacy risk, and can bury the actual evidence. Index exposure is not content reading.

## Correct Behavior

Start with Resource Index and selected registry entries. Escalate read tiers only when the task requires it, and explain why.

## Corresponding Eval

- `evals/orchestration/context-read-tier-self-test.md`
