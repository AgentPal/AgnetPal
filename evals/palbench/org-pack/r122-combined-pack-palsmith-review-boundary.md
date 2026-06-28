# R122 Combined Pack PalSmith Review Boundary Eval

## Purpose

This PalBench eval checks that R122 adds a PalSmith-style review gate for the
R121 Org Pack + FDE Pack combined example without expanding AgentPal into a
runtime, connector, scanner, validator, marketplace, installer, daemon,
database, credential store, keyword router, or external project payload copier.

## Scope

In scope:

- R122 pre-gate.
- R122 PalSmith-style review report.
- R122 reusable/private classification review.
- R122 approval checklist.
- R122 issues file.
- R122 validation and R123 readiness decision.
- Existing R121 combined example.

Out of scope:

- GitHub push, pull, fetch, tag, or Release.
- Official Pal metadata rollout.
- Central roster modification.
- External project `.agentpal/` asset writes.
- Marketplace, connector, scanner, validator, installer, daemon, database,
  auto-sync, auto-discovery, auto-execution, or keyword-routing behavior.

## Required Checks

### 1. Review Gate Artifacts Exist

Pass when these files exist:

- `release/fresh-clone-checks/r122-pre-combined-pack-palsmith-review-gate.md`
- `release/integration-notes/r122-combined-pack-palsmith-review-report.md`
- `release/integration-notes/r122-combined-pack-reusable-private-classification-review.md`
- `release/integration-notes/r122-combined-pack-approval-checklist.md`
- `release/integration-notes/r122-combined-pack-review-issues.md`
- `evals/palbench/org-pack/r122-combined-pack-palsmith-review-boundary.md`
- `release/fresh-clone-checks/r122-local-combined-pack-palsmith-review-validation.md`
- `release/integration-notes/r122-r123-readiness-decision.md`

### 2. Combined Example Still Valid

Pass when the combined example still exists, `combined-pack.json` parses,
`org_pack_ref` exists, and all `fde_pack_refs` exist.

### 3. No Private Or Credential Leak

Pass when R122 and combined example files contain no real credentials, tokens,
customer data, private project context, private meeting content, screenshots, or
reversible identifying clues.

### 4. No Behavior Expansion

Pass when R122 does not add connector, scanner, validator, installer, daemon,
database, marketplace, hub, credential-store, auto-sync, auto-discovery,
auto-execution, or active keyword-routing behavior.

### 5. Recommended Pals Are Not Route Maps

Pass when recommended Pals remain AI judgement inputs only and no
`keyword_map`, `domain_map`, `role_map`, deterministic dispatch table, or
content-to-Pal route table exists.

### 6. Thin Binding Preserved

Pass when external projects remain thin-bound and no default
`.agentpal/org-pack/`, `.agentpal/fde-pack/`, `.agentpal/pals/`,
`.agentpal/workflows/`, `.agentpal/memory/`, `.agentpal/reports/`,
`.agentpal/capability-inventory/`, or `.agentpal/business-systems/` payload is
created.

### 7. Central Roster And Official Pal Unchanged

Pass when central contacts parse, registered / active Pals remain `9 / 9`,
`routing_policy=ai_judgement_only`, `keyword_routing_allowed=false`, official
Pal dirs remain `9`, all official Pal `pal.json` files parse, only PalSmith has
`asset-manifest.json`, and protected diffs are empty.

## Expected Result

Expected result for R122: `pass`.

Any missing evidence must be reported as `missing`, `not-run`, or `blocked`.
