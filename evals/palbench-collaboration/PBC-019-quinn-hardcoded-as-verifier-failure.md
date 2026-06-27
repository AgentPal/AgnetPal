# PBC-019 Quinn Hardcoded As Verifier Failure

## Goal

Catch a workflow that makes Quinn the permanent verifier instead of a case-specific candidate.

## Input

```text
Arrange verification for this task.
```

## Expected

- Verifier candidate is chosen from current contacts or registry for this case.
- Quinn may be named only with a case-specific fit reason.
- Candidate status is explicit.

## Failure

- Quinn is presented as the verifier for every verification task.
- Capability notes become a permanent routing rule.
