# What Is AgentPal?

AgentPal is a no-code AI organization framework for existing agent runtimes.
It gives a runtime a Pal layer: identities, knowledge, skills, memory rules,
context rules, output contracts, workflows, verification habits, and
coordination protocols.

AgentPal is not a standalone app, CLI, connector, scanner, installer, daemon,
marketplace, or automation runtime. Real execution still belongs to Codex,
Claude Code, OpenCode, OpenHands, or another host runtime.

## Pal

A Pal is a working companion. A Pal is not one skill and not a new agent
process. It is a reusable bundle of role identity, knowledge, skills, workflow
rules, context loading rules, and output expectations.

## Mira

Mira is the default Main Pal, Leader Pal, and Conductor. Ordinary messages start
with Mira. Mira decides whether to answer directly, ask a focused question,
prepare a Task Package, or hand off to a registered specialist Pal.

## PalSmith

PalSmith is the no-code Pal asset governance Pal. PalSmith helps create,
inspect, improve, version, and review Pal assets and Pal team blueprints. It
does not automatically edit central contacts or publish assets.

## Faye

Faye is the AI Delivery Pal pattern. Faye turns a business goal into a Delivery
Pack, Pal Team Blueprint, Faye Build Request, first Task Packages, acceptance
notes, training notes, and review records. Faye is not a connector or executor.

## Org Pack

An Org Pack describes reusable AI organization structure: roles, workflows,
runbooks, governance notes, and recommended Pal perspectives. Recommendations
are AI judgement inputs only, not fixed routes.

## FDE Pack

An FDE Pack describes reusable expert delivery method. It may include delivery
scope, reusable assets, review requirements, update policy, and customer-private
boundaries. It is not a program or API client.

## Delivery Pack

A Delivery Pack describes how one business goal should be delivered. It can
contain a project description, flows, task packages, a Pal team blueprint,
integration notes, acceptance notes, training notes, and reports.

## Thin Binding

Thin binding connects an external project to AgentPal without copying the whole
AgentPal workspace into that project. The external project gets only small
binding files and protected instruction blocks that point back to AgentPal.

## Central Project Record

The central project record lives under `workspace/projects/<project-id>/` in
the AgentPal Workspace. It is the default place for project memory, source maps,
derived knowledge, task packages, verification records, governance notes, and
capability inventory.

## Deep Conductor / Governance Loop

Deep Conductor is a no-code protocol set for complex delivery governance. It
uses task judgement, missing-information handling, Context Access Lists,
workflow plans, Task Packages, verification records, and governance records. It
is not an automatic runtime engine.
