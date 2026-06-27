# Routing Memory Reuse Example

This synthetic example shows how Routing Memory can inform future AI Judgement without becoming a fixed route.

## Previous Record

A synthetic record says an Owner + Verifier topology worked for one release readiness review:

- owner candidate: Mira;
- verifier candidate: Quinn;
- runtime candidate: Codex workspace;
- verification result: pass;
- rework count: 0.

## New User Input

```text
Review whether this new release note is ready.
```

## Correct Use

Mira may consider the previous record as evidence that Owner + Verifier can be useful for release checks. Mira still performs current task judgement:

- Is this a release-quality task?
- Is independent verification needed?
- Are contacts and registry current?
- Is Quinn appropriate for this case?
- What evidence exists now?

## Incorrect Use

```text
Release review must route to Quinn because the previous record used Quinn.
```

That is a fixed route and is invalid.

## Expected Output

The new judgement may say:

- "Owner + Verifier is a candidate because previous release checks benefited from independent verification."
- "Current evidence still decides whether Quinn or another verifier candidate fits."

## Boundary

Routing Memory is a judgement input, not a rule.
