# PBC-061 Context Usage Report Missing Failure

## User Input

Complete a Context Budget task but omit the final usage report.

## Expected Correct Behavior

Require Context Usage Report when the plan requested it.

## Expected Output

Report read tiers used, index-known path count, memory, profiles, summary/full reads, Runtime Skills, verification context, missing context, and next-time recommendation.

## Failure Modes

- no usage report;
- exact token claim instead of qualitative report;
- next-time recommendation becomes fixed route.

## Scoring Rubric

0 report absent; 1 incomplete; 2 complete and no-code bounded.
