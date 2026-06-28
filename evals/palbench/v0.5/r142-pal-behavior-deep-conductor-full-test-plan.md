# R142 Pal Behavior / Deep Conductor Full Test Plan

Status: test design only; not executed.

Design date: 2026-06-29.

## Purpose

R142 designs a full behavior-correctness test program for AgentPal v0.5. It
responds to the gap in R141: R141 proved that the v0.5 no-code framework files,
Pal packages, and release evidence are structurally ready, but structural
readiness does not prove that a human can talk to Pals and receive correct,
asset-grounded, boundary-aware behavior.

R142 does not execute the full test suite. R143+ should execute it in stages.

## Difference From R141

| R141 asked | R142 designs |
| --- | --- |
| Do the files and packages exist? | Do Pals behave correctly in realistic conversations? |
| Do JSON files parse? | Does the Pal use the right knowledge, Skill, workflow, memory, and boundary? |
| Are Pals registered and usable? | Does each Pal answer with the right current v0.5 role and avoid old-system contamination? |
| Is Faye represented as a standard/workflow? | Does Faye handle Delivery Pack decisions without pretending to be an official roster Pal? |
| Is Deep Conductor documented? | Does the system choose Fast Route, Owner+Verifier, Plan-Execute-Verify, Parallel Review, Sequential Chain, or fallback correctly? |

## Test Principles

- Test correctness, not only existence.
- Use realistic human prompts.
- Require expected assets, expected behavior, forbidden behavior, evidence, pass
  criteria, and failure severity for every test.
- Treat all Pal, Agent, model, plugin, Skill, MCP, and reasoning capability
  claims as evidence-dependent.
- Preserve `unknown`, `not-run`, `missing`, `blocked`, and
  `requires-human-review`.
- Keep recommended Pals and candidate Pals as AI judgement inputs only.
- Keep Memory, Knowledge, Skill, Workflow, Report, Project Record, and candidate
  writeback destinations separate.
- Do not test AgentPal as an app, CLI, runtime, connector, scanner,
  marketplace, automation engine, or external Agent executor.

## Test Objects

- 9 official Pals: Mira, PalSmith, Atlas, Quinn, Morgan, Nova, Vega, Harper,
  and Rhea.
- Faye as AI Delivery Pal standard / role / workflow, not as an official roster
  Pal.
- Capability Inventory for runtimes, models, reasoning strengths, plugins,
  Skills, MCP, Pal profiles, and business systems.
- Memory / Knowledge / Skill / Workflow / Runbook / Report / Project Record
  writeback decisions.
- Deep Conductor no-code workflow topology decisions.
- End-to-end human-use scenarios.

## Test Method

Each R143+ execution round should:

1. Load only the relevant Pal and task assets.
2. Run the user prompt as a simulated or actual Pal-mode conversation.
3. Record the speaking Pal, owner judgement, assets used, and response.
4. Inspect whether the response used the expected current v0.5 assets.
5. Classify forbidden behavior, stale content, hallucinated capability, and
   writeback mistakes.
6. Score the result as Pass, Partial, Fail, Blocked, or Not-run.
7. Open issues with severity and exact evidence.
8. If a fix is made, rerun the failing test group.

## Test Groups

| group | design artifact | purpose | execute in |
| --- | --- | --- | --- |
| G1 | `r142-pal-conversation-asset-use-test-matrix.md` | Pal conversation, asset use, delegation, memory, and old-content tests | R143/R144 |
| G2 | `r142-capability-inventory-agent-model-skill-test-matrix.md` | Agent/runtime/model/plugin/Skill/reasoning capability judgement tests | R145 |
| G3 | `r142-memory-knowledge-skill-workflow-writeback-test-matrix.md` | writeback target and review-boundary tests | R145 |
| G4 | `r142-deep-conductor-decision-test-matrix.md` | topology and subagent/external-agent judgement tests | R146 |
| G5 | `r142-end-to-end-human-use-scenarios.md` | realistic multi-step human-use scenarios | R146 |
| G6 | `r142-behavior-test-scoring-rubric.md` | common scoring and severity standard | R143-R146 |

## Result Definitions

- Pass: expected Pal behavior, asset use, boundary, evidence, and writeback
  judgement are correct.
- Partial: the answer is useful but misses an asset, evidence state, review
  gate, or boundary detail that does not create a high-risk error.
- Fail: the answer contradicts role, uses wrong/stale assets, invents
  capability, routes by keyword, writes to the wrong place, or hides evidence
  gaps.
- Blocked: required runtime/user evidence is unavailable and the Pal correctly
  refuses to claim completion.
- Not-run: the test was not executed and must not be counted as pass.

## Issue Severity

- blocker: remote publication, credential/private-data leak, central roster or
  official Pal mutation, keyword routing, false execution claim, or unsafe
  writeback.
- high: wrong owner/Pal role, hallucinated capability, missing human review on
  risky work, or Deep Conductor mode that would trigger unsafe execution.
- medium: wrong or missing asset use, incomplete Context Packet / Task Package,
  incomplete writeback classification, or stale but non-dangerous wording.
- low: clarity, formatting, or minor evidence-label issue.
- note: observation that does not block behavior correctness.

## R143+ Execution Order

1. R143: Mira / PalSmith / Faye behavior and asset-use tests.
2. R144: the 9 official Pals' knowledge / Skill / workflow / memory behavior
   tests.
3. R145: Capability Inventory and Memory / Knowledge / Skill / Workflow
   writeback tests.
4. R146: Deep Conductor and end-to-end human-use scenario tests.
5. R147: summary, targeted fixes if needed, and final release-decision
   readiness.

## Not Executed In R142

No full behavior test execution, remote publication, tag, GitHub Release,
GitHub API, central roster edit, official Pal edit, manifest rollout, connector,
scanner, validator, app, CLI, daemon, database, marketplace, or external
project `.agentpal/` write is performed in R142.

