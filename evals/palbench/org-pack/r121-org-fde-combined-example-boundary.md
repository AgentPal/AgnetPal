# R121 Org / FDE Combined Example Boundary Eval

## Purpose

This PalBench eval checks that R121 adds a public-safe Org Pack + FDE Pack
combined example without expanding AgentPal into a runtime, connector,
marketplace, scanner, validator, installer, keyword router, or external project
payload copier.

## Scope

In scope:

- `examples/combined-packs/content-ops-with-accounting-advisor/`
- `examples/org-packs/content-ops-org-pack/`
- `examples/fde-packs/accounting-advisor-fde-pack/`
- R121 validation and readiness records.

Out of scope:

- official Pal metadata rollout;
- central roster modification;
- external project `.agentpal/` asset writes;
- GitHub push, tag, or Release;
- connector, scanner, validator, installer, daemon, database, marketplace, hub,
  auto-sync, auto-discovery, auto-execution, credential storage, or keyword
  routing behavior.

## Required Checks

### 1. Combined Example Exists

Pass when `examples/combined-packs/content-ops-with-accounting-advisor/` exists
with `README.md`, `combined-pack.json`, composition notes, PalSmith audit notes,
customer-private boundary notes, thin-binding notes, and verification checklist.

### 2. JSON Parse

Pass when:

- `combined-pack.json` parses;
- its `org_pack_ref` exists;
- all `fde_pack_refs` exist;
- existing Org Pack and FDE Pack JSON files parse;
- central roster JSON parses.

### 3. PalSmith Audit Note Exists

Pass when `palsmith-audit-note.md` records:

- composition validity;
- missing fields;
- reusable / private boundary status;
- recommended fixes;
- blocked issues;
- no connector / no credentials / no keyword route;
- human review requirement.

### 4. Customer-private Boundary Exists

Pass when `customer-private-boundary.md` forbids real customer books, invoices,
contracts, tax materials, customer names, account tokens, API keys, identifiable
screenshots, and private project context, and points private material to
approved private records.

### 5. Thin Binding Preserved

Pass when `thin-binding-relationship.md` lists allowed thin binding files and
forbidden default thick-binding directories, and no external project receives
Org/FDE/Pal/workflow/memory/report/capability/business-system directories by
default.

### 6. No Credential Or Customer-private Leak

Pass when R121 public files contain no real credentials, tokens, customer data,
private project context, private meeting content, or reversible identifying
clues.

### 7. No Behavior Expansion

Pass when R121 files do not introduce active connector, scanner, validator,
installer, daemon, database, marketplace, hub, auto-sync, auto-discovery,
auto-execution, credential-store, or keyword-routing behavior.

### 8. Central Roster And Official Pal Unchanged

Pass when:

- central contacts still contain 9 registered Pals and 9 active Pals;
- `routing_policy=ai_judgement_only`;
- `keyword_routing_allowed=false`;
- `git diff -- workspace/organization/contacts` is empty;
- official Pal directories remain 9;
- all official Pal `pal.json` files parse;
- only PalSmith has `asset-manifest.json`;
- no official Pal `pal.json` diff exists.

## Expected Result

Expected result for R121: `pass`.

Any missing evidence must be reported as `missing`, `not-run`, or `blocked`.
