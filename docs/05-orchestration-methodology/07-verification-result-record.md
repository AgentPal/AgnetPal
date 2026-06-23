# Verification Result Record

A Verification Result Record captures whether an output has enough evidence to be accepted.

It separates completion claims from proof.

## Status

- Current: Available in v0.1.0-rc.1 as a template and audit artifact.
- Future: May become a required record in Deep Conductor workflows and release gates.
- Research: PalBench can measure false completion detection, verification pass rate, and evidence quality.

## Why it exists

Agent answers can sound complete even when evidence is missing.

A Verification Result Record gives AgentPal a small structure for asking:

- what output is under review?
- who or what verified it?
- what acceptance criteria apply?
- what evidence was checked?
- did the result pass, fail, warn, or remain inconclusive?
- is rework required?

## How it works

The record can capture:

- task summary
- output under review
- verifier type and id
- acceptance criteria
- evidence checked
- result
- false completion caught
- issues found
- rework required
- privacy or safety notes
- routing memory candidate

In v0.1, the record does not run checks by itself. It records checks and evidence that the current runtime, Pal, user, or checklist actually provided.

## What it is not

- Not proof by itself.
- Not a substitute for tests, command output, file diffs, or user review.
- Not a legal, safety, medical, finance, or security final signoff.
- Not an automatic verifier in v0.1.
- Not permission to claim completion without evidence.

## Acceptance rule

If evidence is missing, say the result is unverified, warning, failed, or inconclusive.

Do not downgrade an evidence gap into a stylistic note.

