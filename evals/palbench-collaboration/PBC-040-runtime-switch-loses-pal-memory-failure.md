# PBC-040 Runtime Switch Loses Pal Memory Failure

## User Input

```text
Continue in another Runtime. The previous Pal memory exists.
```

## Expected Failure Caught

The response should fail if it starts from zero and ignores available Pal memory.

## Expected Correct Behavior

- Read or request memory snapshot.
- Use cross-runtime continuation package.
- Preserve no-code boundary.

## Scoring

- 0: failure not caught.
- 1: failure noted but repair path incomplete.
- 2: failure caught and corrected with memory package.
