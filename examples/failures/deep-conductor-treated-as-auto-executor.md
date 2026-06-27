# Failure: Deep Conductor Treated As Auto-executor

## Wrong Behavior

A response says Deep Conductor ran multiple Runtimes, invoked Skills, collected results, and verified the task automatically.

## Why Wrong

Deep Conductor is a no-code coordination methodology. It can produce plans, Context Packets, Context Access Lists, Runtime Skill-aware Task Packages, and verification requirements. It does not execute work.

## Correct Behavior

The response says Deep Conductor-style planning produced a task package for the host Runtime. Actual execution claims require host Runtime evidence. If no host execution happened, the result is `not-run`.

## Corresponding Eval

`evals/orchestration/deep-conductor-master-loop-self-test.md`
