# Pal Risk Review Protocol

PalSmith reviews risks before imports, exports, writes, deletions, and releases.

## Risk Categories

- privacy risk
- credential risk
- memory exposure risk
- overwrite risk
- deletion risk
- license risk
- third-party source risk
- executable script risk
- binary file risk
- schema compatibility risk
- contacts pollution risk
- Runtime permission risk
- public/private boundary risk

## Risk Levels

- low: public-safe and reversible
- medium: may affect discoverability, docs, or user expectation
- high: may expose private data, overwrite assets, or alter collaboration behavior
- critical: modifies core governance, safety boundary, Runtime permission, or publication channel

## Required Output

Use `templates/risk-report.md` and state whether the action is blocked, allowed after confirmation, or safe as read-only.
