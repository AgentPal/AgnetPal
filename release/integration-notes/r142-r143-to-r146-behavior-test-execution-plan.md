# R142 / R143-R146 Behavior Test Execution Plan

Status: ready for staged execution.

Date: 2026-06-29.

## R143: Mira / PalSmith / Faye Core Entry Tests

Execute:

- Mira identity, onboarding, route judgement, Context Packet, memory candidate,
  and remote-publication boundary tests.
- PalSmith Pal creation, asset review, manifest pilot, no-code governance, and
  central roster mutation boundary tests.
- Faye role/workflow tests through Delivery Pack, Faye to PalSmith handoff, and
  no official-Pal claim checks.

Expected outputs:

- R143 results
- R143 issues
- R143 validation
- R144 readiness decision

## R144: Official Pal Knowledge / Skill / Workflow / Memory Tests

Execute behavior tests for:

- Atlas
- Quinn
- Morgan
- Nova
- Vega
- Harper
- Rhea
- plus any remaining Mira / PalSmith cases not completed in R143

Expected outputs:

- R144 results
- R144 issues
- fixes if required
- R145 readiness decision

## R145: Capability Inventory And Writeback Tests

Execute:

- runtime/model/reasoning/plugin/Skill capability profile tests;
- unknown / not-run / missing handling;
- model and reasoning recommendation tests;
- Memory / Knowledge / Skill / Workflow / Runbook / Report / Project Record
  writeback destination tests;
- readback and reuse tests.

Expected outputs:

- R145 results
- R145 issues
- capability/writeback validation
- R146 readiness decision

## R146: Deep Conductor And End-to-End Human-Use Tests

Execute:

- Fast Route
- Owner + Verifier
- Plan-Execute-Verify
- Parallel Review
- Sequential Chain
- subagent allowed / not allowed / fallback
- external Agent handoff
- governance loop
- 10 end-to-end human-use scenarios

Expected outputs:

- R146 results
- R146 issues
- R146 validation
- R147 readiness decision

## R147: Summary, Fixes, And Final Release Decision Gate

R147 should summarize R143-R146, apply or route targeted fixes, rerun failing
groups when needed, and decide whether AgentPal can enter final remote
publication decision. It must still not publish remotely unless separately
authorized.

