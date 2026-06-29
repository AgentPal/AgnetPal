# R157 Agent-use Decision Protocol Enhancement Summary

Status: executed
Date: 2026-06-29

## Protocols Added

- `standards/agent-use/agent-use-decision-card.md`
- `standards/capability-inventory/host-capability-snapshot.md`
- `standards/agent-use/skill-plugin-invocation-record.md`
- `standards/agent-use/codex-mode-selection-matrix.md`
- `standards/agent-use/model-reasoning-recommendation.md`
- `standards/agent-use/subthread-subagent-decision.md`
- `standards/agent-use/claude-code-handoff-acceptance-card.md`
- `standards/agent-use/pal-pre-execution-self-question-checklist.md`
- `standards/deep-conductor/agent-use-mode-decision-protocol.md`

## Templates Added

- `templates/agent-use/agent-use-decision-card-template.md`
- `templates/capability-inventory/host-capability-snapshot-template.json`
- `templates/agent-use/skill-plugin-invocation-record-template.md`
- `templates/agent-use/claude-code-handoff-prompt.md`

## Pal Assets Updated

- `official/pals/Mira-main/PAL.md`
- `official/pals/Mira-main/SKILL.md`
- `official/pals/Rhea-system/PAL.md`
- `official/pals/Rhea-system/SKILL.md`
- `official/pals/Atlas-developer/PAL.md`
- `official/pals/Atlas-developer/SKILL.md`
- `official/pals/Quinn-quality/PAL.md`
- `official/pals/Quinn-quality/SKILL.md`
- `official/pals/PalSmith-pal-governor/PAL.md`
- `official/pals/PalSmith-pal-governor/SKILL.md`
- `official/pals/Faye-delivery/PAL.md`
- `official/pals/Faye-delivery/SKILL.md`

## Prompts / Runtime Guides Updated

- `prompts/codex/initialize-agentpal-workspace.md`
- `prompts/claude-code/README.md`
- `prompts/generic-cli-agent/README.md`
- `prompts/cli-agent/README.md`
- `docs/04-runtime-guides/01-use-with-codex.md`
- `docs/04-runtime-guides/02-use-with-claude-code.md`
- `docs/04-runtime-guides/03-use-with-generic-cli-agent.md`
- `core/main-pal-conductor-gate.md`
- `core/runtime-adapter-shared-contract.md`
- `standards/capability-inventory/runtime-detection-protocol.md`
- `standards/capability-inventory/plugin-scan-protocol.md`
- `standards/capability-inventory/README.md`
- `standards/deep-conductor/README.md`

## R156 Issues Addressed

| R156 issue | R157 response |
| --- | --- |
| Codex mode labels were sometimes generic | Added explicit `codex_mode` enum and mode matrix; Mira/Atlas/core now require explicit mode labels for complex execution-shaped tasks. |
| Host capability snapshot was not shared | Added Host Capability Snapshot standard/template and assigned Rhea ownership. |
| Skill/plugin remained recommendation-only | Added Skill / Plugin Invocation Record with `real_call`, `dry_run`, `handoff_only`, `prompt_inspection`, `not_invoked`, and `blocked`. |
| Response latency for broad capability prompts | Added quick-answer path: answer from visible capability evidence first, then ask whether to inspect deeper Skill/plugin docs. |
| Claude Code minimal call could be overclaimed | Added Claude Code Handoff Acceptance Card and explicit minimal-call versus full-host acceptance boundary. |

## Remaining Gaps

- Full Claude Code AgentPal host acceptance remains not-run.
- Generic CLI Agent real host acceptance remains not-run.
- Real Skill/plugin/mode invocation is not started in R157; it is deferred to R158.

## No-code Boundary Confirmation

R157 added and updated Markdown/JSON protocol assets only. It did not add CLI,
scanner, daemon, connector, installer, runtime dependency, API client,
marketplace, database, or executable code. It did not execute remote writes.

