# R135 / R136 Faye Extension Regression Execution Checklist

Status: execution checklist for R136.

## Boundary

R136 is local targeted regression only. It must not run push, pull, fetch, tag
creation, GitHub Release creation, or remote publication.

## Checklist

1. Confirm the working tree status and record current branch / HEAD.
2. Confirm all R132-R135 required files exist.
3. Run F1 Faye / Delivery Pack Standards review.
4. Run F2 Video Growth Delivery Pack Chain review.
5. Run F3 Sales CRM Delivery Pack Chain review.
6. Run F4 Faye -> PalSmith Handoff review.
7. Run F5 Deep Conductor Governance Loop review.
8. Run F6 Boundary / Safety scans.
9. Run F7 Shared Entry / Navigation review.
10. Run F8 Baseline Preservation review.
11. Parse all visible JSON files.
12. Parse all Delivery Pack JSON files.
13. Parse routing-memory-record JSON files.
14. Parse `agentpal.json`.
15. Parse central contacts.
16. Count central registered / active Pals.
17. Count official Pal directories.
18. Parse all official Pal `pal.json` files.
19. Count official asset manifests and confirm PalSmith is the only official
    Pal with a manifest.
20. Check `routing_policy` remains `ai_judgement_only`.
21. Check `keyword_routing_allowed` remains false where applicable.
22. Confirm central contacts have no R136 diff.
23. Confirm official Pal `pal.json` files have no R136 diff.
24. Scan public files for private local report path strings.
25. Scan for active route maps, connector/scanner/validator/marketplace program
    expansion, credential-like values, customer-private material, executable
    code additions, external project `.agentpal/delivery-pack`, and hidden
    remote-publication claims.
26. Create a clean temporary copy without `.git`.
27. Re-run required-file existence and JSON parse checks in the clean copy.
28. Record results, issues, validation evidence, and readiness decision.

## Failure Handling

- Blocker or high issue: stop refreshed completion claim and prepare a fix round.
- Medium issue: fix or explicitly defer before refreshed completion claim.
- Low issue: record and decide whether it can be deferred safely.
- Missing required evidence: mark the relevant group `fail` or `blocked`; do not
  substitute a neighboring file.

## Expected R136 Artifacts

- `evals/palbench/v0.5/r136-faye-extension-targeted-regression-results.md`
- `evals/palbench/v0.5/r136-faye-extension-targeted-regression-issues.md`
- `release/fresh-clone-checks/r136-local-faye-extension-targeted-regression-validation.md`
- `release/integration-notes/r136-r137-readiness-decision.md` or a refreshed
  completion-readiness decision if no fix round is needed.
