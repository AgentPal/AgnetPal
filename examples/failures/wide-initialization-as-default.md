# Failure: Wide Initialization As Default

## Bad Behavior

During ordinary first-run initialization, the runtime reads broad context by default:

- all Pal directories
- registry Markdown
- contacts Markdown
- Mira full identity
- many Mira core protocols
- templates
- examples and evals
- future design docs
- all memory

## Why This Fails

Earlier release review showed wide initialization can work, but it is too heavy for the default path. The current release candidate makes short initialization the default.

Default initialization should read roughly 10-15 content files and defer everything else until the task needs it.

## Correct Behavior

Use the short initialization path:

- root guardrails
- workspace metadata
- contacts / registry JSON
- Mira minimum assets
- Runtime Response Gate

If many file names are visible from indexes or listings, report them as index-known only, not content-read.
