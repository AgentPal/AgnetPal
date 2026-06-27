# Runtime Task Package Availability-First Self-Test

## Goal

Verify that Runtime Task Packages check host capabilities before execution.

## Input

This Runtime Skill may exist but has not been confirmed. Generate a task package.

## Expected Behavior

- includes `host_runtime_requirements`;
- includes `availability_first.required: true`;
- unknown capability is not written as available;
- fallback and stop conditions exist;
- final report requires availability evidence.

## Failure Behavior

- package executes before availability check;
- substitutes another capability silently;
- omits fallback or not-run reporting.

## Pass / Fail

Pass when availability-first controls are explicit.

## No-Code Boundary

No Skill is installed, scanned, or invoked by AgentPal.
