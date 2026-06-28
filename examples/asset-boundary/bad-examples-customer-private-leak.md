# Bad Examples: Customer-private Leak

Date: 2026-06-28

These are fake examples. They are intentionally marked forbidden. They do not contain real customer data or real credentials.

## Forbidden Example 1: Real Customer Contract Summary

Fake bad input:

```text
Customer Alpha's contract has private pricing, renewal timing, and negotiation notes.
```

Verdict: forbidden public asset.

Why forbidden:

- customer-specific;
- contract material;
- pricing and negotiation context;
- not reusable without heavy generalization and review.

## Forbidden Example 2: Credential-like Deployment Note

Fake bad input:

```text
Use the customer's secret deployment value from their private vault and paste it into the workflow.
```

Verdict: forbidden public asset.

Why forbidden:

- refers to credentials;
- instructs unsafe handling;
- cannot be made public by masking a value.

## Forbidden Example 3: Internal System Screenshot

Fake bad input:

```text
Screenshot of a customer's internal approval dashboard with names, IDs, and private tickets visible.
```

Verdict: forbidden public asset.

Why forbidden:

- internal system screenshot;
- identifiable people and records;
- private project evidence.

## Forbidden Example 4: Private Meeting Transcript

Fake bad input:

```text
Meeting transcript with attendee names, private customer blockers, and action items copied into a public Org Pack example.
```

Verdict: forbidden public asset.

Why forbidden:

- unapproved meeting content;
- customer-specific blockers;
- private action items.

## Forbidden Example 5: Renamed But Reconstructable Case

Fake bad input:

```text
The customer name was changed, but exact dates, project sequence, rare role titles, and internal system names remain.
```

Verdict: forbidden public asset.

Why forbidden:

- simple renaming is not de-identification;
- reversible identifying clues remain;
- human review must reject publication.

## Forbidden Example 6: Deterministic Pal Route Table

Fake bad input:

```text
If a request mentions finance, always route to one fixed Pal. If it mentions writing, always route to another fixed Pal.
```

Verdict: forbidden public asset.

Why forbidden:

- deterministic semantic routing;
- bypasses AI owner judgement;
- conflicts with central roster and AgentPal routing policy.

## Forbidden Example 7: External Project Thick Binding

Fake bad input:

```text
Copy the Org Pack, Pal bodies, workflows, evals, and memory into every external project under project-local AgentPal folders.
```

Verdict: forbidden public asset.

Why forbidden:

- violates thin binding;
- copies central assets into external projects;
- risks leaking reusable and private material together.
