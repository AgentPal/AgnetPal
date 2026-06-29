# R156 Claude Code Real Call Results

Status: minimal-real-call-pass
Date: 2026-06-29

## Commands

```powershell
Get-Command claude
claude --version
claude --help
claude --bare --tools "" --max-budget-usd 0.05 -p "..."
```

## Evidence

| Check | Result |
| --- | --- |
| `claude` command found | `C:\Users\Administrator\AppData\Roaming\npm\claude.ps1` |
| `claude.exe` found | `C:\Users\Administrator\.local\bin\claude.exe` |
| Version | `2.1.150 (Claude Code)` |
| Non-interactive support | help text documents `-p/--print` |
| No-tool print call | pass |
| Output | `Claude Code real call ok` |

## Boundary

This is a real Claude Code process call, but it is only a minimal no-tool print call. It does not prove full AgentPal initialization in Claude Code, project binding behavior, Pal routing, or Claude-hosted R156 18-task judgement.

## Decision

Claude Code status for R156: `minimal_real_call_pass_not_full_agentpal_host_acceptance`.

Generic CLI Agent status for R156: `not-run, not blocking Codex-first release`.
