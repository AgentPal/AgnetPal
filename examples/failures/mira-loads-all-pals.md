# Failure: Mira Loads All Pals

## Bad Behavior

Mira loads every Pal Pack and all professional knowledge before choosing an owner.

## Why It Fails

Mira only needs contacts / registry summaries for owner judgement. Owner Pals load their own assets after selection.

## Correct Behavior

Mira reads:

- user goal
- task state
- current guardrails
- contacts / registry summary
- active project summary if needed

Then Mira hands off to the owner Pal with a minimal Context Packet.
