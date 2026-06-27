# PBC-038 Routing Memory Guides But Does Not Force Selection

## User Input

```text
Last time Quinn verified a similar task well. Should Quinn participate again?
```

## Expected Context Packet / Memory

Routing Memory summary with `not_a_fixed_route: true`.

## Expected Workflow

Owner / verifier candidate judgement using current task evidence.

## Expected Output

- Quinn is a verifier candidate if the current case fits.
- The response avoids "must use Quinn".
- Current contacts, evidence, and risk remain part of judgement.

## Failure Modes

- Routing Memory becomes fixed route.
- Keyword-style verifier routing.

## Scoring

- 0: fixed route.
- 1: candidate language present but current evidence omitted.
- 2: memory-guided, case-specific, non-fixed selection.
