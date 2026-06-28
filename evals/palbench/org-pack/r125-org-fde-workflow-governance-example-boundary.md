# R125 Org/FDE Workflow Governance Example Boundary Eval

## Purpose

Validate that R125 adds public-safe no-code workflow and governance examples for
the Content Ops with Accounting Advisor Combined Pack without introducing
runtime execution, thick external project binding, keyword routing, customer
private data, credentials, or protected Pal metadata changes.

## Scope

In scope:

- `examples/combined-packs/content-ops-with-accounting-advisor/workflow-usage-example.md`
- `examples/combined-packs/content-ops-with-accounting-advisor/context-packet.example.md`
- `examples/combined-packs/content-ops-with-accounting-advisor/task-package.example.md`
- `examples/combined-packs/content-ops-with-accounting-advisor/governance-record.example.md`
- `examples/combined-packs/content-ops-with-accounting-advisor/verification-result.example.md`
- `examples/combined-packs/content-ops-with-accounting-advisor/README.md`
- `docs/04-usage-scenarios/org-fde-combined-pack-usage-scenario.md`
- `RESOURCE_INDEX.md`
- `agentpal.json`

Out of scope:

- GitHub sync, tags, or Release.
- Runtime code.
- Connectors, scanners, validators, daemons, installers, API clients, databases,
  marketplace programs, hubs, automatic sync, or automatic execution.
- Central roster edits.
- Official Pal identity metadata edits.
- Official Pal manifest rollout.
- Real customer project records or customer-private evidence.

## Required Assertions

| Assertion | Expected Result |
| --- | --- |
| Workflow usage example exists | Pass |
| Context packet example exists | Pass |
| Task package example exists | Pass |
| Governance record example exists | Pass |
| Verification result example exists | Pass |
| Combined example README links all R125 examples | Pass |
| `agentpal.json` registers all R125 usage paths | Pass |
| `RESOURCE_INDEX.md` lists all R125 examples and release artifacts | Pass |
| Examples preserve no-code status | Pass |
| Examples include no customer-private leak | Pass |
| Examples include no credentials or secret-like values | Pass |
| Examples add no connector, scanner, validator, marketplace, hub, installer, daemon, API client, database, auto sync, or auto execution behavior | Pass |
| Recommended Pals remain AI judgement input only | Pass |
| No `keyword_map`, `domain_map`, `role_map`, or deterministic route table is introduced | Pass |
| Thin binding is preserved | Pass |
| Central project record path remains placeholder-only | Pass |
| Human review is retained for accounting-adjacent professional conclusions | Pass |
| `not-run` and `missing` are not treated as pass | Pass |
| Central roster remains unchanged | Pass |
| Official Pal `pal.json` files remain unchanged | Pass |
| Only PalSmith has an official manifest-like file | Pass |

## Manual Review Prompts

1. Does the workflow example show `user request -> Mira explanation -> PalSmith
   review -> Org/FDE context packet -> human review -> central project record ->
   verification / governance record` without claiming execution?
2. Does the context packet use placeholders and storage classes instead of real
   customer data?
3. Does the task package keep owner and supporting Pals as AI judgement rather
   than keyword routing?
4. Does the governance record preserve human review and rejected/blocked
   conditions?
5. Does the verification result keep `not-run`, `missing`, and
   `requires-human-review` distinct from `pass`?

## Expected Decision

R125 passes when all required assertions are satisfied by local file inspection,
JSON parsing, protected-path diff checks, changed-file boundary scans, and
clean-copy validation.
