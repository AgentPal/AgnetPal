# R160 Capability Status Classification

Status: executed-local
Date: 2026-06-29

## Classification Table

| capability | status | evidence_path | can_claim_publicly | public_wording | forbidden_wording |
| --- | --- | --- | --- | --- | --- |
| Codex normal chat | full_pass | R159/R160 current-thread evidence | yes | AgentPal is validated first for Codex normal chat and Pal routing workflows. | Codex autonomously executes all Pal workflows. |
| Codex background thread | full_pass | `r160-subagent-child-thread-regression-results.md` | yes | Codex background child-thread evidence exists for bounded read-only review. | AgentPal automatically starts background workflows. |
| Codex subagent | minimal_pass | `r159-child-thread-decision-records.md` | with_condition | A Codex subagent was started and closed in R159 for bounded anti-trigger evidence. | AgentPal has a general-purpose subagent runtime. |
| Codex Plan Mode | recommendation_only | `r160-plan-goal-mode-manual-evidence.md` | with_condition | AgentPal can recommend Plan Mode and provides a manual Plan Mode test script. | Plan Mode has fully passed manual host acceptance. |
| Codex Goal Mode | minimal_pass | `fixtures/r160/goal-mode-validation-note.md` | with_condition | R160 ran under active goal context and wrote bounded local evidence. | Goal Mode has separate UI-captured acceptance evidence. |
| Claude Code | minimal_pass | `r160-claude-code-host-acceptance-results.md` | with_condition | Claude Code minimal AgentPal handoff has passed; full host acceptance remains unproven. | Claude Code full AgentPal support is validated. |
| CodeWhale | minimal_pass | `fixtures/r159/codewhale-minimal-startup-evidence.json` | with_condition | CodeWhale minimal no-write startup evidence exists. | CodeWhale full AgentPal host support is validated. |
| DeepSeek / DeepSeek-TUI | version_only | `fixtures/r159/deepseek-tui-startup-evidence.json` | with_condition | DeepSeek / DeepSeek-TUI were visible by version/help probe only. | DeepSeek AgentPal handoff is validated. |
| OpenCode | unavailable | R160 PATH probe | no | OpenCode was unavailable in this host. | OpenCode is supported/validated. |
| Gemini | unavailable | R160 PATH probe | no | Gemini CLI was unavailable in this host. | Gemini support is validated. |
| GitHub | dry_run_only | R158/R160 probe; `gh` unavailable | with_condition | GitHub work remains dry-run or app-mediated unless separately authorized and evidenced. | GitHub publication or PR workflows are fully validated. |
| Notion | dry_run_only | visible plugin tools; no authorized target | with_condition | Notion can be treated as a candidate integration with authorization and target evidence. | Notion write integration has been validated. |
| Lark | dry_run_only | visible Lark skills; no authorized target | with_condition | Lark can be treated as candidate capability with explicit authorization and target evidence. | Lark write integration has been validated. |
| Cloudflare | dry_run_only | visible skills; `wrangler` unavailable | with_condition | Cloudflare workflows remain dry-run/handoff unless tools and authorization are available. | Cloudflare deploy integration has passed. |
| HyperFrames | unavailable | R160 PATH probe | no | HyperFrames CLI was unavailable in this host. | HyperFrames rendering is validated in this host. |
| Product Design | minimal_pass | `fixtures/r159/product-design-direct-use-evidence.json` | with_condition | Product Design audit direct-use was validated on a local screenshot fixture. | All Product Design workflows are fully validated. |
| PDF / documents / spreadsheets / presentations | minimal_pass | R158/R159 fixture evidence and visible Skills | with_condition | Local document-family Skill evidence exists for selected fixtures. | Every file workflow is fully validated. |
| Browser | minimal_pass | R158 browser evidence | with_condition | Browser capability has bounded local evidence from R158. | Browser automation is universally available and validated. |

