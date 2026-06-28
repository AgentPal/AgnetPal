# R119-C Reusable / Private Asset Boundary PalBench

Date: 2026-06-28

## Purpose

Evaluate whether R119-C establishes a public-safe reusable versus customer-private asset boundary for Org Pack, FDE Pack, PalSmith, and Pal Asset work.

This is a no-code PalBench record. It does not execute scanners, validators, connectors, installers, marketplace programs, or routing engines.

## Evaluated Files

- `standards/asset-boundary/reusable-vs-customer-private-assets.md`
- `standards/asset-boundary/asset-classification-matrix.md`
- `standards/asset-boundary/deidentification-standard.md`
- `templates/asset-boundary/asset-classification-result-template.json`
- `templates/asset-boundary/customer-private-boundary-template.md`
- `examples/asset-boundary/reusable-vs-private-classification-examples.md`
- `examples/asset-boundary/bad-examples-customer-private-leak.md`

## Cases

| Case | Expected result | Evidence | Result |
| --- | --- | --- | --- |
| reusable asset definition exists | standard defines reusable asset and examples | reusable-vs-customer-private standard | pass |
| customer-private asset definition exists | standard defines customer-private asset and examples | reusable-vs-customer-private standard | pass |
| project-private record definition exists | standard defines default private project storage | reusable-vs-customer-private standard | pass |
| organization-internal record definition exists | standard separates internal from public reusable | reusable-vs-customer-private standard | pass |
| public example definition exists | standard defines public example | reusable-vs-customer-private standard | pass |
| de-identified example definition exists | standard defines de-identified example | reusable-vs-customer-private and de-identification standards | pass |
| forbidden public asset definition exists | standard defines forbidden public asset | reusable-vs-customer-private standard | pass |
| matrix fields complete | matrix includes required fields | asset-classification matrix | pass |
| JSON template parses | template is valid JSON | local parse | pass |
| JSON template defaults conservative | publish false, review true, credentials false, deidentified false, customer_private unconfirmed | JSON template | pass |
| bad examples are fake and forbidden | bad examples file states fake and marks examples forbidden | bad examples file | pass |
| no real credentials | no concrete secret values added | local text inspection | pass |
| no real customer data | examples are generic/fake | examples and bad examples | pass |
| no connector / scanner program | documents contain boundary terms only and no implementation | all R119-C files | pass |
| no keyword routing | no route-map fields or deterministic routing instructions added | all R119-C files | pass |
| external thin binding preserved | standards forbid default external `.agentpal/` asset copies | standard, template, examples | pass |

## Notes

The JSON template uses `customer_private: null` by default because `customer_private=false` is allowed only after review confirms no customer-private content. This preserves the R119-C requirement that unknown sensitivity must not be treated as public-safe.

## Decision

Decision: `pass`

R119-C establishes the reusable versus customer-private asset boundary needed before deeper Org Pack / FDE Pack delivery work.
