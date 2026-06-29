# R158 to R159 Real Invocation Decision

Status: executed
Date: 2026-06-29

## Decision

`real_invocation_partial_pass_ready_for_r159_enum_tightening`

## Rationale

R158 proved that the current Codex host can perform safe local real calls and record dry-run/handoff boundaries:

- OpenAI official docs lookup succeeded.
- PDF fixture generation/extraction/render succeeded.
- Spreadsheet-style CSV analysis succeeded.
- DOCX structure generation succeeded, with render QA not-run because LibreOffice is unavailable.
- In-app Browser local fixture check succeeded through localhost.
- Product Design audit gate used current local screenshot evidence.
- Codex background thread creation succeeded.
- Claude Code minimal call succeeded but remains not full AgentPal host acceptance.

The only material weakness is strict `codex_mode` enum compliance in the real child thread: the child thread used `background_thread_review`, which is outside the R157 enum. This does not block a Codex-first release, but R159 should tighten child-thread prompt/validation language.

## Non-Codex Host Decision

- Claude Code: `minimal-real-call-pass-not-full-host-acceptance`
- Generic CLI Agent: `not-run, not blocking Codex-first release`

## R159 Recommended Target

R159 should focus narrowly on exact enum compliance and child-thread Decision Card output shape. It should not add runtime daemons, scanners, connectors, installers, external writes, or remote publication.

