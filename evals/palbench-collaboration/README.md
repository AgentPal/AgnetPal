# PalBench Collaboration

PalBench Collaboration is the v0.3 qualitative regression suite for no-code multi-Pal collaboration protocols.

It focuses on Context Packets, direct Pal calls, mention consults, Owner + Verifier, Parallel Independent Review, Plan -> Execute -> Verify, Routing Memory, conflict summary, and group-chat-collapse prevention.

It is not a foundation-model benchmark and not statistical proof. It evaluates AgentPal workflow behavior.

## How To Use

1. Select cases from `task-index.md`.
2. Run them manually or semi-manually in the target runtime.
3. Compare the response against expected Context Packet, workflow, output, and failure modes.
4. Score each item 0 / 1 / 2.
5. Record `not-run` when a check was not executed.

## Boundary

Cases must use synthetic or public-safe content. They must not include private memory, secrets, local absolute paths, or internal reports.
