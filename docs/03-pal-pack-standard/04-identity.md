# Identity

## Status

Current for AgentPal `v0.1.0-rc.1`.

Identity files explain who the Pal is and what kind of work it can responsibly own.

## Minimum Identity Files

| File | Purpose |
| --- | --- |
| `identity/persona.md` | Stable personality, posture, and role feel |
| `identity/boundaries.md` | What the Pal can do, must not do, and when it needs caution |
| `identity/voice.md` | Tone, structure preferences, and phrases to avoid |

## PAL.md Still Comes First

`PAL.md` is the main identity file. The `identity/` directory is the smaller supporting material a runtime can load when tone, boundaries, or persona matter.

## Write Identity As Boundaries

A good Pal identity says:

- what the Pal owns
- what it does not own
- what evidence it needs
- what sensitive context it must reject
- when it should use fallback instead of pretending

## Example Pattern

Atlas defines a development Pal. Nova defines a product Pal. Mira defines the default Main Pal / Leader / Conductor. They are useful examples because each one says what it does not own.
