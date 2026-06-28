# Central Project Record Walkthrough

## Purpose

This walkthrough explains where project-private facts belong when a user applies
the combined pack to a real external project.

This public example does not create a real project record and does not include
real customer data.

## Placeholder Record Path

Use this placeholder when describing the private target:

```text
workspace/projects/<project-id>/
```

Do not replace `<project-id>` with a real customer or project name in this
public example.

## What Goes To The Central Project Record

Project-private facts may be recorded in these sections after user approval:

| Section | Use |
| --- | --- |
| `binding/` | external binding metadata and protected block references |
| `source-map/` | indexes of important project files and user-provided docs |
| `derived-knowledge/` | structured summaries derived from project materials |
| `memory/` | project decisions, project memory, task ledger, routing memory, and runtime memory |
| `tasks/` | context packets, task packages, synthesis reports, and verification records |
| `reports/` | task reports and verification reports |
| `governance/` | project-specific governance notes and rule-change proposals |
| `capability-inventory/` | project-level capability evidence, unknown states, `not-run`, and `missing` items |

These records are private by default. They must not be silently promoted into
public reusable examples.

## What Must Not Enter The Reusable Pack

Do not place these in the combined pack:

- real customer names;
- real invoices, receipts, contracts, ledgers, tax filings, payroll records, or
  bank statements;
- private project requirements;
- private meeting notes;
- private reports;
- private governance decisions;
- private screenshots;
- customer system URLs, IDs, or account names;
- credentials, tokens, cookies, passwords, API keys, private keys, connection
  strings, or secrets.

## What Must Not Stay In External `.agentpal/`

The external project `.agentpal/` directory should not store:

- facts;
- memory;
- reports;
- governance records;
- capability inventory;
- copied Org Pack assets;
- copied FDE Pack assets;
- copied Pal assets;
- customer-private evidence.

It remains a binding pointer, not the project record.

## How Org Pack / FDE Pack / Pal Assets Work Together

The Org Pack and FDE Pack provide reusable context. Pal assets provide
professional judgement perspectives. The central project record stores
project-specific evidence and memory. These layers stay separate:

- reusable assets stay reusable;
- project-private facts stay private;
- recommended Pals stay AI judgement inputs only;
- real execution remains with the host runtime and must return evidence.

## Public-safe Example Decision

This walkthrough is public-safe because it uses only generic placeholders and
storage classes. It does not create a real private record.
