# Plan -> Execute -> Verify Docs Update Example

This synthetic example shows a docs task using v0.3 Plan -> Execute -> Verify.

## User Input

```text
Add the v0.3 roadmap link to the docs index and verify the result.
```

## Plan Stage

Owner candidate: Mira, because this is documentation navigation and release-boundary coordination.

Runtime candidate: current host runtime for the file edit.

Plan:

- edit only selected docs index files;
- do not add runtime code;
- do not update tags or releases;
- verify links are relative and public-safe.

## Execute Stage

Runtime performs approved file edits and returns:

- affected paths;
- diff summary;
- checks run;
- not-run items.

## Verify Stage

Verifier candidate: Quinn or Mira depending on risk.

Verification:

- changed files match scope;
- no internal local paths;
- no future-as-current language;
- no runtime artifact additions;
- completion report is backed by diff and checks.

## Failure Modes

- Runtime edits unrelated docs;
- completion is claimed without diff evidence;
- Deep Conductor is described as active runtime behavior;
- verification accepts `not-run` checks as pass.
