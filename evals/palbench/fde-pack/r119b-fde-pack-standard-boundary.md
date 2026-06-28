# R119-B FDE Pack Standard Boundary Eval

Date: 2026-06-28

## Scope

This eval checks the FDE / Expert Delivery Pack standard foundation added by R119-B.

It does not execute FDE Packs, create connectors, create marketplace programs, scan systems, validate live customer systems, call external APIs, modify central roster, modify official Pals, or write into external project `.agentpal/`.

## Required checks

| Check | Expected result |
| --- | --- |
| Standard exists | `standards/fde-pack/fde-pack-standard.md` exists |
| Expert delivery boundary exists | `standards/fde-pack/expert-delivery-boundary.md` exists |
| Template exists | `templates/fde-pack/base-fde-pack/` required files exist |
| Example exists | `examples/fde-packs/accounting-advisor-fde-pack/` required files exist |
| Template `fde.json` parses | JSON parse pass |
| Example `fde.json` parses | JSON parse pass |
| Required flags present | Required safety flags are present in both JSON files |
| Required flags safe | `credentials_allowed=false`, `customer_private_assets_allowed_in_pack=false`, `external_projects_copy_assets_by_default=false`, `keyword_routing_allowed=false`, `connector_included=false`, `marketplace_program_included=false`, `requires_human_review=true` |
| No credentials | No credential assignment patterns in R119-B files |
| No customer private data | Example uses public-safe placeholders and exclusions only |
| No connector / marketplace | Text frames connector and marketplace as prohibited, not included |
| No keyword routing | Recommendations are AI judgement inputs only |
| Update policy exists | Template and standard include update policy |
| Verification checklist exists | Template and example include verification checklist |
| High-risk human review boundary exists | Accounting and other high-risk domains require human review |
| No shared entry modification | `README.md`, `README.zh-CN.md`, `RESOURCE_INDEX.md`, and `agentpal.json` unchanged by R119-B |
| No Org Pack practical structure changes | `standards/org-pack/**` unchanged by R119-B |
| No official Pal changes | `official/pals/**` unchanged by R119-B |

## Failure cases

The batch fails if it:

- stores real credentials, tokens, secrets, customer records, real contracts, real financial privacy, customer databases, or sensitive personal information;
- creates a connector, scanner, validator, installer, daemon, database, marketplace/hub program, auto sync engine, or auto execution engine;
- creates keyword routing maps, `keyword_map`, `domain_map`, or `role_map`;
- writes FDE Pack assets into external project `.agentpal/` by default;
- modifies central contacts;
- modifies official Pal `pal.json`;
- generates new official Pal `asset-manifest.json` files;
- continues the 9 Pal metadata / manifest rollout.

## Result vocabulary

Use:

- `pass`
- `fail`
- `missing`
- `not-run`
- `blocked`
- `requires-human-review`

Do not turn `missing`, `not-run`, or `requires-human-review` into `pass`.
