# R93-B Index Update Notes

This file records shared-entry updates that should be integrated after parallel R93 threads are reconciled.

R93-B intentionally did not modify shared entry files such as:

- `README.md`
- `RESOURCE_INDEX.md`
- `agentpal.json`
- `docs/README.md`
- `AGENTS.md`
- `PAL.md`
- `SKILL.md`

## Suggested Additions

Add the R93-B v0.4 real-usage regression plan references to shared navigation surfaces:

- test plan: `evals/palbench/v0.4/r93b-v0.4-real-usage-regression-test-plan.md`
- test matrix: `evals/palbench/v0.4/r93b-v0.4-test-matrix.md`
- validation: `release/fresh-clone-checks/r93b-v0.4-regression-test-plan-validation.md`

Suggested `agentpal.json` metadata after integration:

- `v0_4_real_usage_regression_test_plan`
- `v0_4_real_usage_regression_test_matrix`
- `v0_4_real_usage_regression_test_plan_validation`
- `v0_4_real_usage_regression_groups_required: 10`
- `v0_4_real_usage_regression_executes_repairs: false`
- `v0_4_real_usage_regression_modifies_shared_entries: false`
- `v0_4_real_usage_regression_allows_push_pull_fetch: false`
- `v0_4_real_usage_regression_allows_tag_or_release: false`
- `v0_4_real_usage_regression_allows_scanner_connector_runtime_probe: false`
- `v0_4_real_usage_regression_requires_not_run_missing_honesty: true`

## Boundary Notes

R93-B is a test-plan and test-matrix thread. It does not execute the full v0.4 regression suite, repair failures, update shared entry files, create runtime tools, create scanners, create connectors, run external business-system checks, or modify the central roster.

The full regression plan covers:

1. Local clean package / clean-copy
2. External project thin binding
3. Central Pal roster
4. No keyword routing
5. Official Pal integrity
6. Central project record
7. Capability Inventory
8. Business System governance chain
9. User reading path
10. Public safety / no internal leak

If R93-A assets are integrated, R93-B group 8 can treat the R93-A Change Review / Periodic Reconciliation Note as an optional governance-chain extension rather than a hard dependency.

