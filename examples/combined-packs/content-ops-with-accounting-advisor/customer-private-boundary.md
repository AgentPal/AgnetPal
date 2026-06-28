# Customer-private Boundary

## Public-safe Status

This combined pack is a public-safe example. It must remain publishable,
de-identified, and reusable.

## Forbidden In This Reusable Pack

Do not include:

- real customer books;
- real invoices, receipts, contracts, purchase orders, or statements;
- real ledgers, tax materials, payroll records, audit materials, or bank data;
- real customer names, company names, account names, contact names, or account
  identifiers;
- customer accounting system URLs, IDs, exports, screenshots, or database
  details;
- platform accounts, credentials, tokens, cookies, passwords, API keys, private
  keys, connection strings, or secrets;
- identifiable screenshots or screen recordings;
- private project context, private project memory, private reports, private
  meeting notes, or customer-specific business rules.

## Approved Private Targets

Customer-private material belongs in one of these approved locations:

- `workspace/projects/<project-id>/`
- an approved customer-private delivery record;
- an approved private evidence store.

The reusable combined pack may contain a pointer to the storage class, but it
must not contain the private record body or a private path when the path itself
would reveal customer identity.

## High-risk Human Review

Accounting, tax, payroll, audit, compliance, and financial reporting work needs
qualified human review before customer use. Missing evidence stays `missing`.
Unreviewed customer material stays `requires-human-review`.
