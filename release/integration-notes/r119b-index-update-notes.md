# R119-B Index Update Notes

This file records shared-entry updates that should be integrated later after parallel R119 threads are reconciled.

R119-B intentionally did not modify shared entry files such as:

- `README.md`
- `README.zh-CN.md`
- `RESOURCE_INDEX.md`
- `agentpal.json`

R119-B also did not modify:

- `standards/org-pack/**`
- `official/pals/**`

## Suggested additions

Add FDE / Expert Delivery Pack references to shared navigation surfaces after integration review:

- FDE Pack standard: `standards/fde-pack/fde-pack-standard.md`
- Expert delivery boundary: `standards/fde-pack/expert-delivery-boundary.md`
- Base FDE template: `templates/fde-pack/base-fde-pack/`
- Accounting advisor public-safe example: `examples/fde-packs/accounting-advisor-fde-pack/`
- R119-B boundary eval: `evals/palbench/fde-pack/r119b-fde-pack-standard-boundary.md`
- R119-B validation: `release/fresh-clone-checks/r119b-local-fde-pack-standard-validation.md`

Suggested `agentpal.json` metadata after integration:

- `fde_pack_standard`
- `fde_pack_expert_delivery_boundary`
- `base_fde_pack_template`
- `accounting_advisor_fde_pack_example`
- `fde_pack_standard_eval`
- `fde_pack_standard_validation`
- `fde_pack_is_program: false`
- `fde_pack_connector_included: false`
- `fde_pack_marketplace_program_included: false`
- `fde_pack_keyword_routing_allowed: false`
- `fde_pack_requires_human_review: true`
- `fde_pack_customer_private_assets_allowed_in_public_pack: false`

## Boundary notes

R119-B establishes FDE Packs as no-code expert delivery assets. They are not programs, installers, marketplaces, connectors, scanners, validators, databases, API clients, auto sync engines, auto execution engines, or keyword routers.

FDE Packs may be referenced by Org Packs and may recommend Pals, workflows, runbooks, Org Packs, or Capability Inventory records as AI judgement inputs only.

The accounting advisor example is public-safe and intentionally excludes real tax data, customer accounts, customer ledgers, credentials, contracts, customer databases, and company-private financial information.
