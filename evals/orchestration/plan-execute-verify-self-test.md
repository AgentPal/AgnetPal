# Plan -> Execute -> Verify Self-Test

## Purpose

Check that v0.3 Plan -> Execute -> Verify separates Pal planning, runtime execution, and evidence-based verification.

## Required Assets

- `orchestration/plan-execute-verify-protocol.md`
- `templates/orchestration/plan-execute-verify-package.md`
- `examples/orchestration/plan-execute-verify-doc-update-example.md`

## Pass Criteria

- Plan stage defines scope and evidence;
- Execute stage is runtime-only;
- Verify stage maps evidence to acceptance;
- completion report is not treated as proof;
- no automatic loop or runtime ownership is claimed.

## Failure Modes

- Runtime becomes owner Pal;
- missing checks are smoothed into pass;
- plan-only output is treated as completion;
- protocol creates scripts, scanner, validator, or CLI.

## Expected Result

Pass when the staged workflow remains no-code and evidence-first.
