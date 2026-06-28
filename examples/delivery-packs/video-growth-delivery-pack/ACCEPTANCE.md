# Acceptance

## Required acceptance checks

| Check | Expected status |
| --- | --- |
| Delivery Pack metadata parses | pass |
| Required files exist | pass |
| Five Flow Pack files exist | pass |
| Two Task Package files exist | pass |
| Candidate Pal team is present | pass |
| Faye Build Request is present | pass |
| Candidate Pals are judgement inputs only | pass |
| Human review is required before publishing | pass |
| No credentials or tokens | pass |
| No customer-private material | pass |
| No connector or external API client implementation | pass |
| No central roster modification | pass |
| No official Pal modification | pass |
| No external project `.agentpal/` write payload | pass |

## Content acceptance

- Product intro, founder talking, customer case, live clip, and publishing review flows are all represented.
- Research, scripting, brand, material, QA, publishing, and growth review perspectives are all represented.
- Missing information remains marked as missing, blocked, not-run, or requires-human-review.

## Human review gates

Human review is required for:

- customer-case permission;
- founder voice approval;
- product claim approval;
- source material permission;
- final publication;
- reusable learning promotion.

## Non-acceptance

This pack is not accepted if it contains credentials, customer-private data, implementation code for external systems, deterministic route tables, or central roster changes.
