# No Token Meter Claim Self-test

## Purpose

Ensure AgentPal context budget artifacts do not pretend to be exact metering tools.

## Passing Criteria

- Context Budget Plan contains `not_a_token_meter: true`.
- Context Usage Report contains `not_exact_token_count: true`.
- Exact token / cost numbers appear only if the host Runtime provides evidence, and that evidence is named separately.
- The package remains Markdown / JSON protocol content only.
- It does not create calculators, runtime code, services, daemons, scanners, validators, installers, UI, databases, or automated model routing.
- It preserves no-code Deep Conductor boundaries.
- It excludes internal paths and private data.

## Failure Signals

- Claims exact token count from qualitative tiers.
- Calculates cost without host evidence.
- Treats Context Usage Report as a billing record.
- Uses token metering claims to skip verification.
