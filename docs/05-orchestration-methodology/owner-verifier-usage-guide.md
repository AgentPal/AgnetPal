# Owner + Verifier Usage Guide

Owner + Verifier is a v0.3 no-code workflow for tasks that need a responsible owner and an independent evidence check before the result is accepted.

The owner Pal understands the user goal, prepares the task package or deliverable, and states the completion claim. The verifier Pal checks evidence against criteria and returns `pass`, `fail`, or `blocked`.

## When To Use A Verifier

Use a verifier when:

- release, safety, quality, privacy, or acceptance risk is meaningful;
- the owner produced a completion claim that should not be accepted on trust;
- evidence exists in files, command output, source references, screenshots, or user criteria;
- false completion would be costly or confusing.

## When Not To Use A Verifier

Skip the workflow when:

- the task is ordinary chat, brainstorming, or low-risk explanation;
- the user asked for a quick consult;
- there is no independent evidence to check;
- a single owner answer is enough and the user did not ask for acceptance review.

## Owner Responsibilities

The owner Pal should:

- judge the task shape and owner fit;
- define scope, constraints, and acceptance criteria;
- produce the work or owner task package;
- list evidence needed for verification;
- label missing or not-run checks honestly;
- create a repair package if verification fails or is blocked.

## Verifier Responsibilities

The verifier Pal should:

- use a bounded Verifier Context Packet;
- inspect evidence, criteria, files, test results, or source references as available;
- avoid relying only on the owner conclusion;
- request missing evidence when needed;
- produce a Verification Result Record with verdict `pass`, `fail`, or `blocked`.

## Verification Context vs Owner Context

Owner context is optimized for doing the work: goal, scope, constraints, candidate owner, task package, and output requirements.

Verification context is optimized for checking the work: owner claim, expected deliverables, acceptance criteria, evidence to check, allowed files, blocked reads, known risks, false completion patterns, and required result format.

The verifier does not need full chat history by default. The verifier also does not default to private memory or unrelated Pal assets.

## Result Meanings

- `pass`: evidence supports the checked acceptance criteria.
- `fail`: evidence shows a required criterion is unmet or contradicted.
- `blocked`: evidence is missing, unavailable, outside allowed scope, or unsafe to inspect.

`blocked` is the honest result when the verifier cannot prove the claim. It should include missing evidence and recommended next step.

## False Completion Patterns

Watch for:

- completion reports treated as proof;
- "all checks passed" with no command output or artifact evidence;
- checks omitted or hidden as if they ran;
- owner and verifier both relying on the same unsupported summary;
- release readiness claimed before blockers are inspected;
- candidate Pals treated as permanent route rules.

## Synthesis

Mira or the current owner summarizes:

- the owner claim;
- the verifier verdict;
- evidence checked;
- missing evidence and risks;
- required repairs;
- recommended next step.

The synthesis must preserve a `fail` or `blocked` verdict. It may not smooth it into a pass.

## Boundary

Owner + Verifier is a no-code staged workflow. It does not automatically run background multi-agent execution, Subagents, external Agents, or multiple runtimes. A runtime may only act as an evidence or file execution layer under the current task package.

Quinn is a common quality verifier candidate, but not the only verifier. The selected verifier candidate is decided case by case from the current contacts or registry.
