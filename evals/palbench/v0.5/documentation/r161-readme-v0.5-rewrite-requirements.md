# R161 README v0.5 Rewrite Requirements

## Required Public Positioning

The v0.5 README rewrite must say:

- AgentPal is a no-code Pal organization layer.
- AgentPal is not an Agent runtime, scanner, daemon, connector layer, marketplace, app runtime, or external-system executor.
- Current release posture is Codex-first.
- Current official Pal roster contains 10 Pals, including Faye.
- Mira is the default entry Pal.
- Faye can help with business landing / workflow design / Task Package shaping, but does not execute customer systems.

## Required Evidence Limits

The README rewrite must preserve these limits:

- Claude Code: minimal handoff evidence only, not full host acceptance.
- Generic CLI agents: not a blocking target for Codex-first release unless separately tested.
- OpenCode and Gemini: unavailable in current evidence; do not claim support.
- Plan Mode: UI unavailable in R160 evidence.
- Goal Mode: limited active-goal evidence, not full UI capture support.
- External project writeback: do not claim broad validated writeback.
- Customer data: customer-private; never use as public examples or Pal Pack knowledge.

## Required Entry Paths

Use these entry paths:

- Quick start: `START_HERE.md`
- Codex initialization prompt: `prompts/codex/initialize-agentpal-workspace.md`
- Central contacts: `workspace/organization/contacts/pals.json`
- Resource navigation: `RESOURCE_INDEX.md`

Do not reintroduce `INIT_PROMPT.md`.

## Content To Remove From README Body

- Long historical release logs.
- v0.2 / v0.3 / v0.4 roadmap-heavy language as current behavior.
- Unsupported non-Codex host claims.
- Any wording implying automatic multi-agent execution.
- Any wording implying connector / runtime scan / daemon / external app sync.
- Any first-entry path that asks users to load broad evals or research docs.

## Suggested README Shape For R162

1. What AgentPal is.
2. Current v0.5 boundaries.
3. Who the 10 Pals are.
4. How to initialize in Codex.
5. How to bind an external project with thin binding.
6. What is evidence-backed today.
7. What is future / not yet supported.
8. Links to deeper docs and evidence archive.

