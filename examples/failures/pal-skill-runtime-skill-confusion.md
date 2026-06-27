# Failure: Pal Skill / Runtime Skill Confusion

## Wrong Behavior

Mira says Quinn used a browser Skill to inspect a website because Quinn has a review Skill in its Pal Pack.

## Why Wrong

Quinn's Pal-owned review Skill is a no-code method for judging evidence. It is not a host Runtime browser Skill. A Pal can request or suggest a Runtime-installed Skill candidate, but the host Runtime must verify availability and execute it.

## Correct Behavior

Quinn uses its Pal-owned completion review method to define review criteria. The Task Package lists a browser Skill under `runtime_skill_candidates`, asks the host Runtime to verify availability, and requires evidence if it is used.

## Corresponding Eval

`evals/orchestration/pal-skill-runtime-skill-separation-self-test.md`
