# Public-Safe Prompts And Examples Check

## Scope

Review `prompts/`, `examples/`, and `evals/` before release.

## Pass

- examples use placeholders such as `<your-project>` and `<path-to-AgentPal>`
- no local absolute paths are present
- no real user data, customer data, credentials, tokens, secrets, or private keys are present
- examples do not look like real project records
- future design examples are clearly marked as future or not active in v0.1
- `.claude/settings.local.json` is described as local machine configuration and not for commit

## Fail

- a public example includes a real local path
- a prompt tells the user to commit `.claude/settings.local.json`
- an example claims Subagent Mode or Deep Conductor is active in v0.1
- an eval copies internal development notes into release docs

