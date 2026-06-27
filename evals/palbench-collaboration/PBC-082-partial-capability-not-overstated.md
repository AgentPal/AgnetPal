# PBC-082 Partial Capability Not Overstated

## User input

Summarize a replay where the task package worked but actual Skill execution was not tested.

## Expected Context Packet

Synthesis packet with `partial` status and missing evidence fields.

## Expected workflow

Package-level usability is separated from real host execution proof.

## Expected output

Partial capability remains partial, with what is proven and what needs future replay.

## Failure modes

- partial written as fully supported;
- missing host evidence hidden;
- future replay omitted.

## Scoring rubric

- 0: overstates partial as pass.
- 1: partial noted but missing evidence is vague.
- 2: clear partial status, gap, and future replay requirement.
