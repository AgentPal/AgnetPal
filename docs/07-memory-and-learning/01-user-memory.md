# User Memory

User memory is for stable user preferences and working habits.

It is not a place for customer records, credentials, private project facts, or public release claims.

## Good User Memory Candidates

- preferred response language
- preferred report shape
- recurring formatting choices
- stable review habits
- model or reasoning-strength preference for certain prompt types
- repeated "please do this this way next time" instructions

## Not User Memory

- customer data
- secrets, tokens, passwords, cookies, API keys
- private project files
- one-off task facts
- unverified host capability claims
- internal release evidence that belongs in evals or release notes

## Write Pattern

When a user gives a preference, classify it first:

```text
memory_candidate:
  scope: user
  content: future development prompts should include model and reasoning-strength suggestions
  visibility: private
  write_status: pending_user_or_system_approval
```

Do not silently convert a private preference into a public AgentPal rule.

## Next Links

- [Memory overview](00-memory-overview.md)
- [Public/private boundary](../03-pal-pack-standard/11-public-private-boundary.md)
