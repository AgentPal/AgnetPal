# Current Status

AgentPal v0.1.0-rc.1 is a release candidate for the AgentPal Workspace and Pal Pack Standard practice.

## Active In This Release

- Markdown/JSON AgentPal Workspace.
- Simple Pal Mode only.
- Mira as the default Main Pal.
- Official bundled Pal Packs: Mira, Atlas, Vega, Rhea, Quinn, Morgan, Harper, and Nova.
- `/pal Name` direct calls through contacts and registry.
- Runtime Response Gate and Pal Mode validity rules.
- Context slicing, asset loading budgets, memory summary loading, and Task Package output contracts.
- External project workgroup templates.
- Public-safe release files, examples, evals, prompts, and templates.

## Not Active In This Release

- Desktop app.
- Web UI.
- Marketplace or hosted Pal Hub.
- Automatic installer, daemon, scanner, validator, or service.
- Execution engine owned by AgentPal.
- Active multi-agent runtime.
- Active child workflow or subagent orchestration.
- Deep runtime adapters for external agent platforms.

## Runtime Responsibility

AgentPal does not execute real filesystem, system, publishing, account, or automation actions by itself. The host runtime performs actions and must provide evidence when it claims something was done.

## Documentation Responsibility

Public docs should describe the current release conservatively. Future design material can exist, but it must be marked as future and must not affect normal v0.1.0-rc.1 usage.

## Related

- [What is AgentPal?](00-what-is-agentpal.md)
- [AgentPal vs agent runtime](03-agentpal-vs-agent-runtime.md)
- [Simple Pal Mode](../01-concepts/05-simple-pal-mode.md)
- [Known limitations](../99-reference/known-limitations.md)
