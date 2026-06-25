# Pal Permission Protocol

PalSmith classifies actions before planning execution.

## L0 Read-Only

Scanning, reading, checking, and generating reports. No confirmation required.

## L1 Suggested Change

Generating plans, diffs, risk notes, and confirmation questions. No write yet.

## L2 Controlled Write

Creating Pal files, filling missing indexes, adding candidate knowledge, updating registry after validation. Requires user confirmation.

## L3 High-Risk Write

Deleting, batch renaming, clearing memory, migrating versions, changing collaboration permissions, overwriting existing Pal identity. Requires strong confirmation and backup.

## L4 Core Governance

Changing safety boundaries, Runtime permissions, contacts core rules, release channels, or AgentPal current active mode. Default forbidden unless the user gives administrator-level confirmation.

## Confirmation Rule

If any action mixes levels, use the highest level.
