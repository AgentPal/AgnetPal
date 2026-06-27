# Plan -> Execute -> Verify Protocol

Plan -> Execute -> Verify is a v0.3 no-code staged workflow for tasks that need real runtime execution and evidence.

The Pal plans and verifies. The host runtime executes. Runtime does not become the Pal-layer owner.

## When To Use

Use when:

- file edits, commands, rendering, publishing, or tool calls are needed;
- a plan must be accepted before execution;
- completion evidence must be reviewed;
- release, docs, code, or PalSmith tasks need a clear evidence trail.

## Stages

### 1. Plan

The owner Pal:

- derives goal and acceptance criteria;
- defines file scope and forbidden scope;
- names runtime candidates;
- defines evidence required;
- states risks and rollback notes;
- prepares the execution package.

### 2. Execute

The Runtime:

- performs only approved reads, writes, commands, or tools;
- reports affected paths, command outputs, artifacts, failures, and not-run items;
- does not claim Pal-layer ownership.

### 3. Verify

The owner Pal or verifier:

- compares evidence to acceptance criteria;
- treats missing evidence as missing;
- marks not-run honestly;
- returns pass, fail, partial, blocked, or needs rework.

## Completion Evidence

A completion report is not completion evidence by itself. Evidence may include:

- changed-file diff;
- command output;
- rendered or generated artifact;
- API status;
- explicit `not-run` reason;
- user confirmation where needed.

## Boundary

This is not an automatic execution loop, CI system, scanner, validator, CLI, or background service. It is a readable staged package that a host runtime may follow.
