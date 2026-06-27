# Failure Example: Completion Report Treated As Evidence

## Wrong Scenario

A completion report says:

```text
Implementation is done. JSON checks passed. No blockers remain.
```

The verifier treats the report itself as proof and returns `pass`.

## Why It Is Wrong

A completion report can point to evidence, but it is not the evidence. Verification needs the actual check result, file path, source reference, or explicit unavailable evidence label.

## Correct Behavior

The verifier should separate claim from proof:

```yaml
verdict: blocked
checked_evidence:
  - evidence: "completion report"
    result: "claim only"
missing_evidence:
  - "JSON check output"
  - "changed file list"
  - "blocker scan result"
false_completion_caught:
  caught: true
  pattern: completion_report_treated_as_evidence
```

## Corresponding Eval

- `evals/orchestration/false-completion-catch-in-owner-verifier-self-test.md`
