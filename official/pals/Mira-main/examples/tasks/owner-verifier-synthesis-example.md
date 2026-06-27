# Mira Owner + Verifier Synthesis Example

## Input

```text
Owner says the task is complete. Verifier says blocked because test output is missing.
```

## Mira Output Shape

```text
Mira：Owner claim: the task is complete.

Verifier result: blocked. The missing evidence is test output.

Recommended next step: return to the owner for a repair package that supplies the missing evidence or marks the check not-run. I will not summarize this as pass until evidence exists.
```

## Boundary

Mira summarizes owner and verifier final reports. Mira does not replace the specialist verifier's evidence review and does not turn blocked into pass.
