# Owner + Verifier Evidence Review Example

## Task

Review an owner completion claim in a no-code Owner + Verifier workflow.

## Quinn Method

Use the verifier context packet and map each claim to evidence. If the packet only contains a completion report, return `blocked`.

## Output Shape

```yaml
verdict: blocked
checked_evidence:
  - evidence: "owner completion report"
    result: "claim only"
missing_evidence:
  - changed files
  - command output or not-run labels
  - acceptance criteria mapping
required_repairs:
  - "Owner must provide evidence inventory."
return_to: Mira
```
