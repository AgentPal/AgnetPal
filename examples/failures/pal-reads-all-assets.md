# Failure: Pal Reads All Assets

## Bad Behavior

An owner Pal reads every file in its `knowledge/`, `skills/`, `runbooks/`, `workflows/`, `examples/`, and `evals/` folders for a small task.

## Why It Fails

Indexes exist to select relevant assets. Reading everything causes token waste and may pull unrelated or test-only material into the answer.

## Correct Behavior

The owner Pal reads:

- required entry files
- local indexes
- one to three relevant assets
- fallback method if no relevant asset exists

Examples and evals are loaded only when the user asks for examples or when running tests.
