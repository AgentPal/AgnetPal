# PalBench Light Task Index

This index lists the first R44 PalBench Light release regression cases.

PalBench Light evaluates Agent usage workflow behavior, not foundation-model capability. Cases are release-regression prompts and expected behavior records, not statistical benchmark samples.

## Summary

| Category | Count | Directory |
| --- | ---: | --- |
| Mira-first | 3 | `mira-first/` |
| Direct `/pal Name` | 3 | `direct-pal/` |
| Composite deliverable | 3 | `composite-deliverable/` |
| Context scope / CAL | 3 | `context-scope/` |
| False completion / verification | 3 | `verification/` |
| PalSmith / AI team | 3 | `palsmith/` |
| Runtime adapters | 3 | `runtime-adapters/` |
| Capability Inventory | 3 | `capability-inventory/` |
| Total | 24 |  |

## Cases

| ID | Category | File | Focus |
| --- | --- | --- | --- |
| PBL-001 | Mira-first | `mira-first/PBL-001-ordinary-next-step-judgement.md` | Ordinary task next-step judgement. |
| PBL-002 | Mira-first | `mira-first/PBL-002-composite-staged-judgement.md` | First Pal staged judgement for composite work. |
| PBL-003 | Mira-first | `mira-first/PBL-003-release-check-organization.md` | Release check organization without overclaiming readiness. |
| PBL-004 | Direct `/pal Name` | `direct-pal/PBL-004-direct-atlas-dev-task-package.md` | `/pal Atlas` development task package. |
| PBL-005 | Direct `/pal Name` | `direct-pal/PBL-005-direct-vega-research-task.md` | `/pal Vega` source-grounded research task. |
| PBL-006 | Direct `/pal Name` | `direct-pal/PBL-006-direct-quinn-completion-review.md` | `/pal Quinn` completion evidence review. |
| PBL-007 | Composite deliverable | `composite-deliverable/PBL-007-research-report-html-page.md` | Research plus report plus HTML page. |
| PBL-008 | Composite deliverable | `composite-deliverable/PBL-008-product-dev-acceptance-package.md` | Product requirements plus development package plus acceptance. |
| PBL-009 | Composite deliverable | `composite-deliverable/PBL-009-writing-research-release-copy.md` | Writing plus research plus release copy. |
| PBL-010 | Context scope / CAL | `context-scope/PBL-010-minimal-pal-asset-loading.md` | Only necessary Pal assets are read. |
| PBL-011 | Context scope / CAL | `context-scope/PBL-011-no-load-all-official-pals.md` | Avoid loading all official Pals. |
| PBL-012 | Context scope / CAL | `context-scope/PBL-012-stage-level-context-access-list.md` | Stage-level Context Access Lists. |
| PBL-013 | Verification | `verification/PBL-013-completion-report-missing-evidence.md` | Completion report lacks proof. |
| PBL-014 | Verification | `verification/PBL-014-release-checklist-unsupported-pass.md` | Release checklist claims pass without files. |
| PBL-015 | Verification | `verification/PBL-015-install-prompt-update-missing-verify.md` | Install prompt update lacks verify prompt evidence. |
| PBL-016 | PalSmith | `palsmith/PBL-016-create-professional-pal-from-goal.md` | Create a professional Pal from user goal. |
| PBL-017 | PalSmith | `palsmith/PBL-017-create-ai-team-from-goal.md` | Create a small AI team from user goal. |
| PBL-018 | PalSmith | `palsmith/PBL-018-material-ingestion-and-health-repair.md` | User material ingestion plus health repair package. |
| PBL-019 | Runtime adapters | `runtime-adapters/PBL-019-claude-code-thin-binding.md` | Claude Code thin binding. |
| PBL-020 | Runtime adapters | `runtime-adapters/PBL-020-generic-cli-thin-binding.md` | Generic CLI thin binding. |
| PBL-021 | Runtime adapters | `runtime-adapters/PBL-021-active-project-root-separation.md` | Active project root and AgentPal workspace root separation. |
| PBL-022 | Capability Inventory | `capability-inventory/PBL-022-profile-as-judgement-input.md` | Capability profile as judgement input. |
| PBL-023 | Capability Inventory | `capability-inventory/PBL-023-profile-used-as-fixed-route.md` | Negative case: profile used as fixed route. |
| PBL-024 | Capability Inventory | `capability-inventory/PBL-024-profile-loading-budget.md` | Load only relevant profiles. |

## Coverage Notes

- Cases reference current contacts / registry and official Pal examples as learning assets, not dispatch rules.
- Runtime adapters are tested as thin bindings that point back to AgentPal workspace core gates.
- Capability profiles are illustrative unless a user or maintainer marks a concrete environment profile as maintained.
- Current AgentPal behavior remains Simple Pal Mode. These cases do not activate Deep Conductor, Subagent Mode, automatic multi-agent execution, scanners, validators, UI, CLI, installers, or daemons.
