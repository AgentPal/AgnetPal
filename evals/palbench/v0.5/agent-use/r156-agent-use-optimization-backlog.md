# R156 Agent Use Optimization Backlog

Status: created-from-executed-run
Date: 2026-06-29

| issue | severity | affected Pal | affected protocol | recommended fix | update target | blocks release yes/no |
| --- | --- | --- | --- | --- | --- | --- |
| Codex mode labels are sometimes generic | medium | Mira / Atlas / Quinn | Deep Conductor mode decision | Require explicit field: `normal / Plan Mode / Goal Mode / owner+verifier / parallel review`, plus reason. | `core/main-pal-conductor-gate.md`, `templates/orchestration/` | no |
| Broad capability prompts are slower than ideal | low | Mira | context slicing / capability inventory | Answer first from visible capability profile, then ask whether to inspect Skill docs. | `orchestration/pal-context-slicing-protocol.md`, `standards/capability-inventory/` | no |
| Verified external host profile is not shared into tested thread | low | Mira / Rhea | runtime adapter | Add a small Host Capability Snapshot field that can list verified local commands such as Claude Code. | `core/runtime-adapter-shared-contract.md`, `templates/orchestration/external-agent-handoff-package.md` | no |
| Claude Code evidence is minimal only | low | Rhea / Atlas | runtime adapter | Add a dedicated Claude Code AgentPal prompt-card real host test with no external writes. | `docs/04-runtime-guides/`, `evals/runtime-adapters/` | no |
| Generic CLI remains not-run | low | Rhea | runtime adapter | Keep marked not-run until a real generic CLI process is started. | `release/integration-notes/` | no |
