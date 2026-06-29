# R160 Release Claim Guard

Status: executed-local
Date: 2026-06-29

## Claimable Now

- AgentPal v0.5 is Codex-first.
- AgentPal is a no-code Pal organization layer, not an execution runtime.
- Codex normal chat and bounded background-thread review have real local evidence.
- Codex child/background thread records now use the R157/R159 enum boundary.
- Codex subagent has minimal startup/close evidence from R159.
- AgentPal can produce Plan Mode and Goal Mode recommendations with explicit `codex_mode`.
- R160 current active goal context produced bounded local evidence for Goal-style work.
- Claude Code has minimal handoff evidence only.
- CodeWhale has minimal no-write startup evidence only.
- Product Design and PDF direct-use have bounded fixture evidence.

## Must Not Claim

- Do not claim Claude Code full AgentPal host support.
- Do not claim OpenCode or Gemini support in this host.
- Do not claim GitHub, Notion, Lark, or Cloudflare write integrations have been validated.
- Do not claim HyperFrames CLI is available in this host.
- Do not claim AgentPal automatically starts subagents, external agents, connectors, scanners, daemons, background services, or deployments.
- Do not claim Plan Mode has manual UI acceptance evidence from R160.
- Do not claim Goal Mode has separate UI screenshot evidence from R160.
- Do not claim customer-private data can enter public examples or reusable Pal Packs.

## Safe Public Wording

```text
AgentPal v0.5 is validated primarily on a Codex-first path. Current local
evidence covers Codex Pal routing, bounded background-thread review, minimal
subagent evidence, explicit tool-directive records, and selected fixture-based
Skill/plugin workflows. Non-Codex hosts are tiered by evidence: Claude Code and
CodeWhale have minimal handoff/startup evidence; DeepSeek is version-only;
OpenCode and Gemini were unavailable in this host. External integrations such
as GitHub, Notion, Lark, and Cloudflare require separate authorization and
current host evidence before write claims.
```

