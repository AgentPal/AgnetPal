# R160 to R161 Release Evidence Readiness Decision

Status: decision-recorded
Date: 2026-06-29

## Decision

`ready_for_release_evidence_with_limitations`

## Basis

- Codex-first evidence is sufficient for consolidation.
- Child-thread enum regression passed with a real Codex background thread.
- Goal-style work has active goal context evidence and bounded local write evidence.
- Plan Mode remains manual-script / UI-unavailable from the current execution layer.
- Claude Code remains minimal handoff only; full host acceptance was attempted but budget-blocked.
- Non-Codex and external integrations are clearly tiered as minimal, version-only, dry-run, not-run, or unavailable.
- Release claim guard explicitly states what must not be claimed.

## R161 Direction

R161 may consolidate release evidence, but must preserve limitations:

- Codex-first, not all-host full support.
- Claude Code minimal handoff, not full host acceptance.
- No OpenCode/Gemini support claim.
- No GitHub/Notion/Lark/Cloudflare write-integration claim without separate authorization and evidence.
- No remote publication claim unless actually performed later with explicit authorization.

