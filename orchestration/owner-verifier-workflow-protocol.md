# Owner + Verifier Workflow Protocol

Owner + Verifier is a v0.3 no-code staged workflow for work where false completion risk, release quality, safety, or acceptance evidence matters.

It does not automatically run multiple Pals. A runtime may follow the package sequentially.

## When To Use

Use when:

- a release, safety, or quality gate needs evidence;
- the owner can produce the work but should not verify only its own conclusion;
- completion claims must be checked against files, command output, source evidence, or user acceptance criteria.

Do not use when:

- the task is simple, low-risk, and single-stage;
- no independent evidence is available;
- the user asked for a quick ordinary answer.

## Stages

1. Owner judgement stage:
   - owner Pal derives goal, scope, constraints, and acceptance criteria;
   - owner prepares or performs the main task package;
   - owner names evidence required for verification.
2. Evidence collection stage:
   - runtime or owner gathers current-state evidence;
   - not-run checks are labeled `not-run`;
   - missing evidence stays missing.
3. Verifier review stage:
   - verifier reads verification context, not only the owner conclusion;
   - verifier maps claims to evidence;
   - verifier returns pass, fail, partial, not-run, or blocked.
4. Summary stage:
   - Mira or owner summarizes outcome, gaps, next action, and routing memory candidate.

## Verifier Context

The verifier should receive:

- original goal or safe summary;
- owner task package;
- acceptance criteria;
- changed files or produced artifacts when relevant;
- command outputs or explicit `not-run`;
- known constraints and do-not-do list.

The verifier should not receive:

- unrelated private memory;
- raw secrets;
- drafts that are not needed for verification;
- only a completion report without evidence.

## Verifier Output

Required verifier fields:

- decision: `pass`, `fail`, `partial`, `not-run`, or `blocked`;
- evidence reviewed;
- claims proven;
- claims not proven;
- risks;
- required rework;
- next owner candidate.

## Boundary

Owner + Verifier is a no-code protocol. It does not create an automated CI system, scanner, validator, release robot, or parallel runtime.
