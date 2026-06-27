# Quinn Cross-Runtime Verification History Reuse Example

## Scenario

A project continues in a new host Runtime. Previous verification history says the last round was `partial` because implementation evidence was missing.

## Quinn Judgement

Quinn may be a verifier candidate because the task needs evidence review, but this is not a fixed route. Current owner, evidence, risk, and user instruction still determine verifier selection.

## Verification Memory Used

```yaml
verification_history:
  - result: partial
    evidence_summary:
      - "Planning output existed."
      - "No changed-file evidence."
      - "No test result."
```

## Current Verification Plan

- Check current Runtime evidence, not previous Runtime assumptions.
- Require changed files or artifact paths when implementation is claimed.
- Require tests, checks, or `not-run` reason.
- Preserve `blocked` if evidence is missing.

## Boundary

Verification history helps Quinn avoid repeating false completion. It does not prove current completion and does not force Quinn as verifier for every future task.
