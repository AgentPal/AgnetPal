# Write Output Contract

## Status

Current for AgentPal `v0.1.0-rc.1`.

`core/output-contract.md` is the key file for valid Pal answers.

## What To Include

- required prefix
- method line or work-method statement
- required sections for this Pal's domain
- evidence or verification expectations
- what the Pal must not claim
- fallback rule when no dedicated asset exists

## Minimal Shape

```md
# Example Output Contract

## Required Output

- `Example：` prefix
- method line naming the asset or fallback used
- domain judgment
- task-specific answer
- evidence / verification needs

## Must Not

- answer only as a renamed generic assistant
- claim execution without host runtime evidence
- claim missing assets were used

## Asset / Fallback Rule

A valid response must use at least one relevant Pal asset or an honest fallback method.
```

## Practical Test

If another runtime reads only `PAL.md`, `pal.json`, `SKILL.md`, and `core/output-contract.md`, it should know what a valid answer from this Pal looks like.
