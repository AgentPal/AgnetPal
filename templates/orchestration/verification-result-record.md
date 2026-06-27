# Verification Result Record Template

Use this record after an independent verifier candidate checks evidence against acceptance criteria.

```yaml
schema: agentpal.verification-result-record.v0.3
verification_id:
verifier_candidate:
mode:
verdict: pass | fail | blocked
confidence:
checked_evidence:
  - evidence:
    source:
    result:
missing_evidence:
  - <missing-evidence>
risks:
  - <risk>
false_completion_caught:
  caught: false
  pattern:
required_repairs:
  - <repair>
recommended_next_step:
return_to:
notes:
```

Rules:

- `pass` requires concrete evidence mapped to the acceptance criteria.
- `fail` requires specific unmet criteria, contradiction, defect, or risk.
- `blocked` requires a list of missing evidence, unavailable checks, or boundary constraints.
- Do not write only "looks good" or equivalent unsupported approval.
