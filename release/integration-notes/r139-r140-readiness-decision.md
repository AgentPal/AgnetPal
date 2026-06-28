# R139 / R140 Readiness Decision

Decision: ready_for_fresh_clone_usability_simulation.

R139 added the new-user onboarding entry path, first 30 minutes guide, first
AgentPal team walkthrough, FAQ, glossary, fresh-clone checklist, validation, and
evidence review.

## Evidence

- `START_HERE.md`
- `docs/00-overview/what-is-agentpal.md`
- `docs/01-getting-started/first-30-minutes.md`
- `examples/walkthroughs/first-agentpal-team/`
- `release/current/v0.5-fresh-clone-usability-checklist.md`
- `docs/00-overview/glossary.md`
- `docs/01-getting-started/faq.md`
- `release/fresh-clone-checks/r139-local-new-user-onboarding-validation.md`
- `evals/palbench/v0.5/r139-new-user-onboarding-evidence-review.md`

## Recommended R140

R140 should run a fresh-clone usability simulation:

- use a clean copy or fresh clone perspective;
- follow `START_HERE.md`;
- follow `docs/01-getting-started/first-30-minutes.md`;
- walk through `examples/walkthroughs/first-agentpal-team/`;
- record any confusing steps, missing links, or false assumptions;
- propose narrow documentation fixes if needed;
- keep GitHub Release, tag creation, push, pull, fetch, and remote publication
  out of scope unless the user separately authorizes them.

## R140 Must Not

R140 must not:

- publish remotely;
- create or modify tags;
- create or modify GitHub Releases;
- add runtime code, automation, connectors, scanners, validators, daemons,
  installers, marketplaces, or API clients;
- modify central contacts or official Pals;
- create real external project `.agentpal` records;
- use real customer data.
