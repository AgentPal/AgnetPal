# E2E Synthesis Readability Self-Test

## Goal

Verify that E2E synthesis is user-readable and not only a long YAML record.

## Input

Summarize E2E replay results for the user.

## Expected Behavior

- includes a short summary;
- states what was planned, what needs execution, what needs verification, and next action;
- preserves partial, unavailable, blocked, and not-run states;
- detailed YAML remains optional or secondary.

## Failure Behavior

- only emits long YAML;
- hides unavailable capability;
- omits next user action.

## Pass / Fail

Pass when the user can understand the result without reading the full audit record.

## No-Code Boundary

This eval checks reporting shape only.
