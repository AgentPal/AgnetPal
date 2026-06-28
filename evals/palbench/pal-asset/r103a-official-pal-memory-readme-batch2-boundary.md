# R103-A Official Pal Memory README Batch 2 Boundary

Date: 2026-06-28

## Purpose

This eval checks that R103-A adds only safe Nova and Vega memory README files
and does not expand official Pal behavior.

## Pass Criteria

- Nova and Vega paths are resolved from central roster, not guessed.
- `official/pals/Nova-product/memory/README.md` exists.
- `official/pals/Vega-research/memory/README.md` exists.
- The added README files include:
  - Purpose
  - What belongs here
  - What does not belong here
  - Current assets
  - Candidate memories / needs review
  - Relationship to reports
  - Project-private memory boundary
  - Related standards
  - Public safety boundary
  - External project boundary
- Nova and Vega root entries still exist.
- Nova and Vega `pal.json` files still parse.
- Central roster still parses.
- Central registered / active Pals remain 9 / 9.
- Official Pal directory count remains 9.
- No official Pal `pal.json` changes.
- No real official `asset-manifest.json` files are generated.
- No existing official Pal assets are moved, deleted, renamed, or rewritten.
- No keyword, domain, role, or deterministic route map is introduced.
- No scanner, validator program, daemon, connector, installer, marketplace, hub,
  auto-sync, or auto-execution behavior is introduced.
- No credentials, tokens, cookies, passwords, API keys, secrets, customer data,
  private project data, or private memory are introduced.
- No external project `.agentpal/` thick binding is introduced.
- Local clean-copy check passes.

## Fail Conditions

- Any file outside the R103-A allowed public scope changes.
- Any `pal.json` file changes.
- Any `asset-manifest.json` file appears under `official/pals/**`.
- Central contacts change.
- Added README files claim runtime execution, routing behavior, or external
  project asset copying.
- Added files contain real credentials or private project data.

## Required Evidence

Record evidence in:

- `release/fresh-clone-checks/r103a-local-official-pal-memory-readme-batch2-validation.md`
- `release/integration-notes/r103a-official-pal-memory-readme-batch2-summary.md`

