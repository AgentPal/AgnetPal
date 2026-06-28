# Verification Checklist

Use `pass`, `fail`, `missing`, `not-run`, `blocked`, or
`requires-human-review`. Do not convert missing or unreviewed evidence into
`pass`.

| Check | Expected Result | Evidence |
| --- | --- | --- |
| Combined example directory exists | pass | `examples/combined-packs/content-ops-with-accounting-advisor/` |
| `combined-pack.json` parses | pass | Local JSON parse required. |
| `org_pack_ref` exists | pass | `examples/org-packs/content-ops-org-pack/` |
| `fde_pack_refs` exist | pass | `examples/fde-packs/accounting-advisor-fde-pack/` |
| PalSmith audit note exists | pass | `palsmith-audit-note.md` |
| Customer-private boundary exists | pass | `customer-private-boundary.md` |
| Thin binding relationship exists | pass | `thin-binding-relationship.md` |
| Recommended Pals are judgement inputs only | pass | `recommended-pals.md`, `combined-pack.json` |
| No credentials or secrets | pass | Public-safe example text only. |
| No customer-private leak | pass | No real customer records or facts included. |
| No connector / scanner / marketplace behavior | pass | False flags and boundary notes only. |
| No keyword routing behavior | pass | `keyword_routing_allowed=false`; recommendations are not routes. |
| Central roster unchanged | pass | `git diff -- workspace/organization/contacts` should be empty. |
| Official Pal `pal.json` unchanged | pass | `git diff -- official/pals/**/pal.json` should be empty. |
| Human review remains required | pass | Accounting FDE and combined pack require human review. |
