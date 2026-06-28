# Org / FDE Composition

## Composition Summary

This combined example references:

- Org Pack: `examples/org-packs/content-ops-org-pack/`
- FDE Pack: `examples/fde-packs/accounting-advisor-fde-pack/`

The Org Pack supplies the reusable content operations organization pattern. The
FDE Pack supplies the reusable accounting advisor expert delivery method. The
combined pack keeps them as references and does not copy their private
adaptations, customer evidence, Pal bodies, central contacts, or external
project bindings.

## Org-derived Assets

The content operations Org Pack contributes:

- `README.md` for public-safe orientation.
- `ORG.md` for reusable organization purpose, role model, workflow candidates,
  governance, and runtime boundary.
- `org.json` for public-safe metadata and false safety defaults.
- `recommended-pals.md` for Pal perspectives as AI judgement inputs only.
- `workflow-map.md` for reusable workflow candidates.
- `private-boundary.md` for customer-private exclusions.

These assets help the current Brain or Runtime frame content operations work.
They do not assign owners by keyword, modify contacts, publish content, call
systems, or create execution behavior.

## FDE-derived Assets

The accounting advisor FDE Pack contributes:

- `README.md` and `FDE.md` for public-safe expert delivery orientation.
- `fde.json` for metadata, high-risk review status, and false safety defaults.
- `reusable-assets.md` for public-safe accounting advisory checklists.
- `customer-private-boundary.md` for accounting privacy exclusions.
- `verification-checklist.md` for evidence and review states.

These assets can guide accounting-adjacent content work such as preparing a
management-report narrative or close-readiness brief. They do not provide final
accounting, tax, payroll, audit, or financial reporting conclusions without
qualified human review.

## Customer-private Records

Customer-private records stay outside this reusable combined pack. Approved
targets include:

- `workspace/projects/<project-id>/`
- an approved customer-private delivery record;
- an approved private evidence store.

The reusable example may reference that those records are needed. It must not
copy their contents.

## PalSmith Audit Role

PalSmith audits the composition as no-code asset governance:

- confirm the referenced Org Pack and FDE Pack exist;
- confirm `combined-pack.json` parses;
- confirm recommendations are AI judgement inputs only;
- confirm customer-private exclusions are explicit;
- confirm external projects remain thin-bound;
- confirm no connector, scanner, marketplace, credential store, or automatic
  execution behavior is introduced.

## Thin Binding Relationship

An external project may keep only thin binding files that point back to the
AgentPal Workspace. The combined pack itself belongs in the AgentPal Workspace
public example area, not inside the external project `.agentpal/` directory by
default.
