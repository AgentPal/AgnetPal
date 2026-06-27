# Parallel Independent Review Self-Test

## Purpose

Check that v0.3 Parallel Independent Review preserves reviewer isolation and no-code staging.

## Required Assets

- `orchestration/parallel-independent-review-protocol.md`
- `templates/orchestration/parallel-review-packet.md`
- `examples/orchestration/parallel-independent-review-product-dev-qa-example.md`

## Pass Criteria

- each reviewer receives its own Context Packet;
- reviewers do not read each other's drafts;
- summary stage reads final reports only;
- candidates are not fixed routes;
- protocol states no automatic multithreading or Deep Conductor runtime.

## Failure Modes

- group-chat style collaboration;
- hidden draft sharing;
- fixed product/dev/QA collaborator map;
- simple task inflated into parallel review.

## Expected Result

Pass when isolated review, candidate language, and summary-stage synthesis are explicit.
