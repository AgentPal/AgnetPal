# R124 Org/FDE Combined Pack Usage Scenario Boundary Eval

## Purpose

Validate that the R124 usage scenario explains how a reusable Org Pack can be
combined with a reusable FDE Pack while preserving AgentPal's no-code asset
boundary, thin external project binding, central project record separation, and
AI judgement only routing model.

## Scope

In scope:

- `docs/04-usage-scenarios/org-fde-combined-pack-usage-scenario.md`
- `examples/combined-packs/content-ops-with-accounting-advisor/usage-walkthrough.md`
- `examples/combined-packs/content-ops-with-accounting-advisor/project-binding-walkthrough.md`
- `examples/combined-packs/content-ops-with-accounting-advisor/central-project-record-walkthrough.md`
- `examples/combined-packs/content-ops-with-accounting-advisor/combined-pack.json`
- `examples/combined-packs/content-ops-with-accounting-advisor/README.md`
- `agentpal.json`
- `RESOURCE_INDEX.md`

Out of scope:

- Changing central contacts.
- Changing official Pal identity metadata.
- Adding runtime programs, marketplace programs, connectors, scanners,
  validators, installers, API clients, daemons, automatic sync, or automatic
  execution.
- Copying Org Pack, FDE Pack, Pal Pack, workflow, memory, report, governance,
  capability inventory, or business-system directories into external project
  `.agentpal/` bindings by default.

## Required Assertions

| Assertion | Expected Result |
| --- | --- |
| Main usage scenario exists | Pass |
| Combined example usage walkthrough exists | Pass |
| Thin project binding walkthrough exists | Pass |
| Central project record walkthrough exists | Pass |
| Walkthroughs describe reusable example assets as public-safe | Pass |
| Walkthroughs keep customer-private evidence outside reusable assets | Pass |
| Walkthroughs keep external project `.agentpal/` binding thin | Pass |
| Walkthroughs point private project records to `workspace/projects/<project-id>/` | Pass |
| Recommended Pals remain AI judgement inputs only | Pass |
| No keyword route table, keyword map, domain map, or role map is introduced | Pass |
| No marketplace, connector, installer, scanner, validator, daemon, or API client is introduced | Pass |
| No credentials, tokens, cookies, secrets, passwords, or customer-private records are introduced | Pass |
| `agentpal.json` registers the usage scenario with false safety flags | Pass |
| `RESOURCE_INDEX.md` exposes the scenario and validation artifacts | Pass |
| Central contacts remain unchanged | Pass |
| Official Pal `pal.json` files remain unchanged | Pass |

## Manual Review Prompts

1. Does the scenario make clear that combined packs are no-code organization and
   expert-delivery assets, not executable integrations?
2. Does the project binding walkthrough describe only thin binding files and
   explicitly forbid copying reusable packs or private project records into the
   external project by default?
3. Does the central project record walkthrough describe private records as local
   workspace/private runtime records instead of public release examples?
4. Does every reference to owner Pals keep AI judgement as the routing
   mechanism rather than implying deterministic keyword routing?
5. Does the example remain safe for public release without real customer,
   accounting, finance, tax, payroll, credential, or business-system data?

## Expected Decision

R124 passes when all assertions above are satisfied by local file inspection and
JSON parsing, with no protected central contact or official Pal identity changes.
