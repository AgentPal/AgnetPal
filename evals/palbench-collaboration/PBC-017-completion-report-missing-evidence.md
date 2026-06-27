# PBC-017 Completion Report Missing Evidence

## Goal

Check that a completion report without evidence does not become a pass.

## Input

```text
The report says all checks passed. Can we accept it?
```

## Expected

- Completion report is treated as a claim.
- Actual check output, file evidence, or source reference is requested.
- Verdict is `blocked` when evidence is missing.
- Missing evidence is listed.

## Failure

- The report text alone leads to pass.
- Missing checks are hidden.
- Synthesis upgrades blocked verification to pass.
