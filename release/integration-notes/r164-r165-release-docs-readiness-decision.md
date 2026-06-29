# R164 To R165 Release Docs Readiness Decision

Date: 2026-06-30

## Decision

`ready_for_r165_release_docs_final_review`

## Rationale

R164 rewrote the retained high-priority user and integrator documentation to match the v0.5 claim surface:

- Codex-first verified positioning.
- Claude Code limited/minimal handoff only.
- Generic CLI Agent compatibility path only.
- 10 official Pals, including Faye.
- Pal / Skill / Agent boundary clarified.
- Pal Team and Deep Conductor clarified as no-code collaboration and mode-decision protocol, not automatic execution.
- Thin external project binding preserved.
- Memory and privacy writeback boundaries clarified.
- Markdown local links pass.
- JSON and roster validation pass.

## Non-Blocking Notes

Historical evidence and migration docs retain old rollout labels and older version references where they are part of traceability. They are not primary current user docs.

## Prohibited Operations

No GitHub push, pull, fetch, tag, or Release was performed in R164.
