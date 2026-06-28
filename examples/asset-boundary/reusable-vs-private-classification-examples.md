# Reusable Vs Private Classification Examples

Date: 2026-06-28

These examples use fictional or generic material only. They are not customer facts.

## Example 1: Generic Checklist

Input:

```text
Before publishing an Org Pack, confirm no customer data, no credentials, no connector behavior, and no keyword routing.
```

Classification:

- `asset_type`: generic checklist
- `reusable_allowed`: true
- `customer_private`: false after review
- `can_be_deidentified`: not needed
- `default_storage`: `templates/` or `evals/`
- `publish_allowed`: true after review
- `requires_human_review`: true

Reason:

The checklist is generic and does not reveal a customer, project, system, account, or private event.

## Example 2: Fake Public Delivery Scenario

Input:

```text
Fictional Co wants a reusable intake workflow for a public demo. The workflow uses generic roles: requester, reviewer, delivery lead.
```

Classification:

- `asset_type`: fake public example
- `reusable_allowed`: true
- `customer_private`: false after review
- `can_be_deidentified`: not needed
- `default_storage`: `examples/`
- `publish_allowed`: true after review
- `requires_human_review`: true

Reason:

The scenario is explicitly fictional and uses generic roles.

## Example 3: Customer Project Requirement

Input:

```text
A named customer wants a workflow that matches its private approval chain and project roadmap.
```

Classification:

- `asset_type`: project requirement
- `reusable_allowed`: false by default
- `customer_private`: true
- `can_be_deidentified`: maybe
- `default_storage`: private project record
- `publish_allowed`: false
- `requires_human_review`: true

Reason:

The asset is tied to a real customer and private project context. A generic workflow pattern may be derived later after de-identification review.

## Example 4: Public-source Summary

Input:

```text
A short summary of a public vendor documentation page, with no copied article body and no private customer usage notes.
```

Classification:

- `asset_type`: public-source summary
- `reusable_allowed`: true
- `customer_private`: false after review
- `can_be_deidentified`: not needed
- `default_storage`: `knowledge/` or `research/`
- `publish_allowed`: true if copyright and citation rules are satisfied
- `requires_human_review`: true

Reason:

Public-source summaries can be reusable when they are short, cited when needed, and do not include private usage facts.

## Example 5: Meeting Notes

Input:

```text
A private project meeting includes decisions, attendee names, dates, and customer-specific action items.
```

Classification:

- `asset_type`: meeting minutes
- `reusable_allowed`: false by default
- `customer_private`: true
- `can_be_deidentified`: maybe
- `default_storage`: private project record or approved minutes store
- `publish_allowed`: false
- `requires_human_review`: true

Reason:

Meeting notes are private unless explicitly approved. A de-identified pattern may be created only after removing names, dates, customer-specific actions, and reversible details.

## Example 6: Org Pack Recommendation

Input:

```text
For a reusable FDE delivery pack, consider Mira for intake, PalSmith for asset governance, and Quinn for verification.
```

Classification:

- `asset_type`: Org Pack recommendation
- `reusable_allowed`: true
- `customer_private`: false after review
- `can_be_deidentified`: not needed
- `default_storage`: Org Pack / FDE Pack reusable area
- `publish_allowed`: true after review
- `requires_human_review`: true

Reason:

The recommendation is a judgement input, not a route. It does not modify central contacts or create deterministic dispatch.

## Example 7: De-identification Candidate

Input:

```text
A private support case contains a useful escalation pattern, but the source includes a customer's exact timeline and internal system names.
```

Classification:

- `asset_type`: de-identification candidate
- `reusable_allowed`: not yet
- `customer_private`: true at source
- `can_be_deidentified`: maybe
- `default_storage`: private project record until reviewed
- `publish_allowed`: false until de-identification and review pass
- `requires_human_review`: true

Reason:

The reusable lesson might be the escalation pattern, but exact timeline and system names must be removed or generalized.
