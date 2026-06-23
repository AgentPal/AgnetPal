# Add Knowledge

## Status

Current for AgentPal `v0.1.0-rc.1`.

Knowledge cards help a Pal use repeatable domain judgment without loading a whole library.

## Start With Index

Create:

```text
knowledge/index.md
```

The index should list available cards and say the runtime should choose the smallest relevant slice.

## Add Cards Only When Useful

Use short files for stable methods, definitions, checklists, or public-safe reference summaries. A minimal Pal can have no cards beyond the index.

## Safe Card Pattern

```md
# Topic

## Use When

## Key Points

## Evidence Needed

## Boundary
```

## Public Boundary

Do not store private user material, customer data, secrets, local paths, or long copied third-party text in knowledge cards.
