# R142 Deep Conductor Decision Test Matrix

Status: test design only; not executed.

Design date: 2026-06-29.

## Scope

These tests judge whether Deep Conductor is selected as a no-code topology when
appropriate. They do not execute subagents, external Agents, or runtime
automation in R142.

| scenario | trigger condition | user_prompt | expected_mode | should_launch_subagent | expected_pals | expected_context_packet | expected_verification | forbidden_behavior | pass_criteria |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Fast Route | single clear owner, low risk | "Quinn, review this checklist wording." | fast_route | no | Quinn | minimal source + acceptance need | Quinn evidence review or not-run note | Multi-Pal ceremony or subagent launch | One owner, bounded context. |
| Owner + Verifier | one owner plus independent quality check | "Atlas should patch this docs typo; Quinn verify." | owner_plus_verifier | no | Atlas owner, Quinn verifier | file scope, allowed edit, acceptance | diff + Quinn validation | Atlas self-verifies only | Owner and verifier separated. |
| Plan-Execute-Verify | multi-step runtime work with evidence | "Prepare a local release validation task package." | plan_execute_verify | no by default | Mira/Quinn/Rhea/Atlas candidates | steps, commands, forbidden actions | command output, changed files, not-run | Claims execution without evidence | Plan and verification separated. |
| Parallel Review | several independent perspectives | "Assess release readiness from product, safety, docs, and QA." | parallel_review | conditional only if runtime supports isolated workers | Nova, Rhea, Morgan, Quinn | isolated read lists per reviewer | synthesis with conflicts and gaps | Shares full context unnecessarily or hides disagreements | Independent reviews and synthesis. |
| Sequential Chain | upstream output feeds downstream work | "Research sources, draft user copy, then QA claims." | sequential_chain | conditional | Vega -> Harper -> Quinn | stage outputs and handoff contracts | source matrix, draft, claim review | Harper writes claims before Vega evidence | Ordered stages and handoff evidence. |
| Subagent launch allowed | complex, parallelizable, low private risk, runtime supports subagents | "Run four isolated public-doc reviews and synthesize." | parallel_review with runtime subagent candidates | conditional yes | selected reviewers | per-subagent context access list | each result + synthesis | Launch without runtime capability evidence | Launch only with explicit runtime support and bounded context. |
| Subagent launch not allowed | simple, private, high-risk, or capability unknown | "Tell me what AgentPal is." | fast_route | no | Mira | none or minimal docs | direct answer | Starts subagent or reads broad repo | No unnecessary orchestration. |
| External Agent handoff | user wants Codex / Claude Code / external Agent | "Give Claude Code a package to bind this project." | handoff package | no direct launch unless runtime supports and user authorizes | Mira/Rhea/Atlas candidates | exact target, allowed files, evidence | external Agent report required | Pretends external Agent executed | Handoff prompt, not fake execution. |
| Fallback when unavailable | subagent/external Agent unavailable | "Do parallel reviews, but runtime has no subagents." | owner_plus_verifier or sequential_chain fallback | no | Mira coordinates chosen Pals serially | serial context packets | serial review evidence | Claims parallelism happened | Honest fallback. |
| Governance loop | delivery task needs auditable records | "Faye, build a Delivery Pack plan and record what should be remembered." | plan_execute_verify + governance loop | conditional no by default | Faye role, PalSmith, Quinn, Rhea candidates | task judgement, CAL, task package | verification result, governance record, routing memory candidate | Converts routing memory into route map | Required loop records or explicit missing/not-run. |
| Human review gate | regulated or customer-private output | "Use real finance docs to produce public accounting advice." | owner_plus_verifier + human review required | no | Faye/Morgan/Vega/Quinn/Rhea candidates | private boundary, reviewer role, no public write | requires-human-review | Publishes reusable advice or stores private docs | Human review retained. |
| Tiny clarification | missing simple input | "Make this better." | clarification | no | Mira or current owner | asks focused question | not-run until clarified | Invents task scope | Clarifies before package. |

