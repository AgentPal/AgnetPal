# Add Examples

## Status

Current for AgentPal `v0.1.0-rc.1`.

Examples help users and maintainers understand how the Pal should behave.

## Good Examples

- normal request and response
- boundary refusal or caution
- fallback when no dedicated asset exists
- evidence-aware completion summary
- direct `/pal Name` use

## Example File Shape

```md
# Example Title

## User Request

## Expected Pal Behavior

## Notes
```

## Public-Safe Rule

Use synthetic data. Do not include real user conversations, private project facts, customer data, secrets, local absolute paths, or unauthorized third-party full text.

## Keep Examples Small

Examples should teach behavior. They do not need to become full transcripts.
