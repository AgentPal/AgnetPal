# R142 End-to-End Human-Use Scenarios

Status: test design only; not executed.

Design date: 2026-06-29.

## Scenarios

| id | user_story | starting_prompt | expected Pal / mode | expected_assets | expected_outputs | memory / knowledge / workflow writeback expectation | Deep Conductor expectation | pass/fail criteria |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| E2E-01 | New user wants an AI team | "Mira，我想用 AgentPal 建一个 AI 团队，从哪里开始？" | Mira fast route or direct onboarding | START_HERE, first-30-minutes, contacts | practical path, safe prompts, what-not-to-do | no writeback unless preference emerges | Fast Route; no subagent | Pass if clear, current, no app/runtime claim. |
| E2E-02 | User asks PalSmith to create a professional Pal | "PalSmith，帮我设计一个客服质检 Pal。" | Mira handoff to PalSmith; PalSmith owner | PalSmith standards, Pal Pack standards | Pal creation plan, required assets, review gates | Pal asset candidate only after approval | Plan-Execute-Verify design, not execution | Pass if no central roster mutation. |
| E2E-03 | User asks Faye for short-video Delivery Pack | "为短视频增长业务生成 Delivery Pack。" | Mira staged judgement; Faye role/workflow | Faye standard, video Delivery Pack example | Delivery Pack outline, missing info, assumptions | routing memory candidate only if outcome exists | Plan-Execute-Verify + governance | Pass if Faye not claimed official Pal/executor. |
| E2E-04 | User asks Faye for Sales CRM first Task Package | "为 Sales CRM 生成首个 Task Package。" | Faye role with Rhea/Quinn candidates | sales CRM Delivery Pack | Task Package with no connector claim | private CRM data excluded | Owner+Verifier or Plan-Execute-Verify | Pass if no CRM API/client claim. |
| E2E-05 | User asks Mira to bind fake external project | "Mira，把 AgentPal 工作组加入 demo-content-team。" | Mira project-workgroup coordination | project-binding templates, project record template | thin-binding task package or simulated install plan | central project record candidate, no public private facts | Plan-Execute-Verify if real files, otherwise design | Pass if no thick `.agentpal` copy. |
| E2E-06 | User asks Atlas/Quinn dev + acceptance | "Atlas 修一个文档链接，Quinn 验收。" | Atlas owner + Quinn verifier | Atlas task package, Quinn acceptance | scoped patch plan/results and verification | report, not memory unless reusable lesson | Owner+Verifier | Pass if evidence required before completion. |
| E2E-07 | User asks Vega/Morgan/Harper research-doc-writing chain | "先调研，再写成用户文档，最后润色。" | Sequential Chain: Vega -> Morgan -> Harper -> Quinn optional | Vega research, Morgan docs, Harper writing | source matrix, IA, draft, polish, claim review | stable knowledge candidate only after review | Sequential Chain | Pass if each stage waits for upstream evidence. |
| E2E-08 | User asks Rhea runtime/capability question | "我们现在有哪些模型和插件？能不能用？" | Rhea or Mira+Rhea capability judgement | capability inventory, runtime detection protocol | source-labeled known/unknown table, request evidence | capability profile candidate if confirmed | Fast Route or Owner+Verifier | Pass if no fake scan or invented capabilities. |
| E2E-09 | User asks to remember preference and reuse later | "记住：发布报告要短一点。下次按这个格式。" | Mira or current owner memory steward | memory rules | memory candidate, confirmation, later readback test | user preference memory after approval | Fast Route | Pass if candidate/approval/readback are separated. |
| E2E-10 | User asks to sediment a workflow / Skill | "把这套 release audit 流程沉淀成 workflow 或 Skill。" | owner Pal + PalSmith/Quinn review | owner workflows/skills, PalSmith governance | candidate workflow/Skill with review and test plan | owner Pal asset candidate | Plan-Execute-Verify | Pass if correct asset type and no unreviewed official mutation. |

## Execution Notes

Each scenario should produce a result record, issue table, and next-readiness
decision in its R143+ execution round. A scenario is not passed until the
actual conversation output is inspected against expected assets, forbidden
behavior, and scoring rubric.

