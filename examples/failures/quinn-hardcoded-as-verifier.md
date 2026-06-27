# Failure Example: Quinn Hardcoded As Verifier

## Wrong Scenario

A workflow says every verification task always uses Quinn, regardless of current contacts, task shape, user instruction, or available evidence.

## Why It Is Wrong

AgentPal owner and verifier selection is case-specific judgement. Quinn is a quality verifier candidate for many quality tasks, but not a permanent routing rule or the only possible verifier.

## Correct Behavior

The workflow should state:

```yaml
verifier_pal_candidate:
verifier_fit_reason:
candidates_not_fixed_routes: true
```

The verifier candidate should be selected from current contacts or registry for the current case.

## Corresponding Eval

- `evals/orchestration/no-hardcoded-verifier-self-test.md`
