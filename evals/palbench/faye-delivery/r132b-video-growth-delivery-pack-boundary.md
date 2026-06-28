# R132-B PalBench Eval: Video Growth Delivery Pack Boundary

## Purpose

Check that the Video Growth Delivery Pack is a public-safe near-real runnable example of Faye-style delivery and PalSmith handoff.

## Scope

- `examples/delivery-packs/video-growth-delivery-pack/`
- `release/fresh-clone-checks/r132b-local-video-growth-delivery-pack-validation.md`
- `release/integration-notes/r132b-index-update-notes.md`

## Required checks

| Check | Expected result |
| --- | --- |
| `delivery-pack.json` parses | pass |
| Required Delivery Pack files exist | pass |
| Five flow files exist | pass |
| Two task files exist | pass |
| `PAL_TEAM.md` exists | pass |
| `FAYE_BUILD_REQUEST.md` exists | pass |
| Candidate Pals are judgement inputs only | pass |
| No credentials, tokens, cookies, or private keys | pass |
| No customer-private data in reusable example | pass |
| No connector, external API client, marketplace, daemon, scanner, database, installer, or auto-execution implementation | pass |
| No deterministic keyword routing | pass |
| No external project `.agentpal/` write payload | pass |
| Central roster unchanged by this pack | pass |
| Official Pal assets unchanged by this pack | pass |

## Required scenario chain

The example must explicitly show:

1. raw user need;
2. simulated materials or directory notes;
3. Faye missing information list;
4. Faye reasonable assumptions;
5. Faye Delivery Pack;
6. Faye `PAL_TEAM.md`;
7. Faye `FAYE_BUILD_REQUEST.md`;
8. PalSmith creates or proposes Pal team skeleton;
9. optional first real Task Package.

## Pass rule

Pass only if all required checks are supported by current runtime evidence. Use `not-run` for any unexecuted check and `blocked` for any check that needs unavailable evidence.
