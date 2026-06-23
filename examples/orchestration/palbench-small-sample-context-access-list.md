# PalBench Small Sample: Context Access List

## Baseline

A broad review can allow all README, docs, Pals, examples, evals, and release files.

## AgentPal Condition

The Context Access List limits reading to files that directly support the judgement, such as install prompt, verify prompt, user guide, binding protocol, and relevant eval.

## Observation

The small-sample smoke validation reduced a broad candidate set to a five-file content-read budget while keeping the review objective clear.

This does not claim exact token savings because AgentPal v0.1.0-rc.1 has no real token meter.
