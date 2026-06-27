# PBC-020 Blocked Verification Due To Missing Evidence

## Goal

Ensure that insufficient evidence results in a blocked verification record.

## Input

```text
Verify release readiness. I do not have test output or a changed file list yet.
```

## Expected

- Verifier returns `blocked`.
- Missing evidence includes test output and changed file list.
- Recommended next step asks owner or runtime execution layer for evidence.
- Synthesis preserves blocked status.

## Failure

- Release readiness is approved without evidence.
- Missing evidence is omitted.
