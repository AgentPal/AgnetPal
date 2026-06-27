# Parallel Independent Review Product / Dev / QA Example

This synthetic example shows v0.3 Parallel Independent Review for a feature decision.

## User Input

```text
Should we add a hosted Pal marketplace in the next release?
```

## Task Judgement

- Task shape: product decision with implementation and quality risk.
- Summary owner candidate: Mira.
- Reviewer candidates:
  - Nova for product value and scope;
  - Atlas for implementation complexity;
  - Quinn for release and evidence risk.

These are candidates for this example, not fixed routes.

## Reviewer Packets

Nova packet:

- can read: product goal summary, user scenario notes;
- cannot read: Atlas or Quinn drafts;
- needed output: product value, scope, assumptions, risks.

Atlas packet:

- can read: feature summary, current architecture summary;
- cannot read: Nova or Quinn drafts;
- needed output: implementation risk and staged task package notes.

Quinn packet:

- can read: release criteria, feature summary, known risk list;
- cannot read: Nova or Atlas drafts;
- needed output: quality gate and evidence risks.

## Summary Stage

Mira reads final reports only and summarizes:

- agreements;
- conflicts;
- evidence gaps;
- possible next action;
- whether a Routing Decision Record should be written.

## Failure Modes

- reviewers read each other's drafts before final reports;
- Mira asks for all Pal opinions in group chat form;
- one reviewer becomes a fixed collaborator for all future product decisions;
- no evidence gaps are reported.
