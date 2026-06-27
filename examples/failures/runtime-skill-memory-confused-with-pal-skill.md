# Failure: Runtime Skill Memory Confused With Pal Skill

## Wrong Behavior

A record says a Claude Code document Skill worked well, then the next task states that Morgan owns and executes that Skill.

## Why It Is Wrong

Runtime-installed Skills belong to the host Runtime. Pal-owned Skills are Pal methods, workflows, runbooks, and output contracts. The two layers must stay separate.

Previous Runtime Skill Usage Memory does not prove the Skill is installed in the current Runtime.

## Correct Behavior

- Put the document Skill under `runtime_skill_candidates`.
- Put Morgan's document judgement method under `pal_owned_skills_used`.
- Require current Runtime evidence before using the Skill.
- Write Runtime Skill Usage Memory only after actual use and verification.

## Corresponding Eval

`evals/orchestration/runtime-skill-usage-memory-self-test.md`
