# R162 to R163 Docs Restructure Readiness Decision

## Decision

`ready_for_r163_docs_directory_restructure`

## Basis

- `README.md` and `README.zh-CN.md` were rewritten for AgentPal v0.5.
- The public docs entry now explains AgentPal as a no-code Pal organization layer.
- The Skill / Pal / Agent relationship is explicit.
- Installation / initialization now points to `prompts/codex/initialize-agentpal-workspace.md`.
- `docs/README.md` is a user navigation entry instead of a historical evidence dump.
- Current runtime support is split into verified, limited, experimental, unavailable, and not generally validated.
- The official Pal table matches the current 10 registered official Pals.

## R163 Should Focus On

- Restructuring the broader `docs/` tree.
- Moving evidence-heavy docs out of the primary user path.
- Merging duplicated runtime guide locations.
- Keeping roadmap and research material separated from current behavior docs.
- Preserving R162 claim guards in all high-visibility docs.

## R163 Must Not Do Without New Authorization

- Push, pull, fetch, tag, or create GitHub Releases.
- Add runtime code, installer, scanner, daemon, connector, or marketplace functionality.
- Claim full non-Codex host acceptance without real host evidence.

