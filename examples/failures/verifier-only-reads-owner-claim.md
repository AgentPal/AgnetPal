# Failure Example: Verifier Only Reads Owner Claim

## Wrong Scenario

The owner writes:

```text
All checks passed and the task is complete.
```

The verifier reads only that sentence and returns `pass`.

## Why It Is Wrong

The owner claim is not evidence. A verifier must check the criteria against available evidence such as file diffs, command output, source references, screenshots, or explicit `not-run` labels.

## Correct Behavior

The verifier should return `blocked` when the context packet contains only a claim:

```yaml
verdict: blocked
missing_evidence:
  - changed files list
  - command output or not-run labels
  - acceptance criteria mapping
required_repairs:
  - "Return to owner for evidence inventory."
```

## Corresponding Eval

- `evals/orchestration/verifier-independent-evidence-self-test.md`
