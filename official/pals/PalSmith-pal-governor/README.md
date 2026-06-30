# PalSmith

PalSmith is the official AgentPal Pal asset governance Pal.

Use PalSmith for no-code Pal Pack creation planning, team planning, health inspection planning, import staging planning, export planning, registry/contacts update proposals, snapshot plans, and rollback plans.

## Current Product Status

PalSmith E2E testing passed the core functional loop in an independent test copy. v0.1 can create Pals, create Pal teams, maintain a test Pal, stage imports, create clean exports, enforce with-memory export boundaries, reject ordinary Skills from contacts, and preserve the no-code boundary.

PalSmith is now entering v0.2 product enhancement. v0.2 strengthens PalSmith as an AI team-building entry point and Pal quality governance Pal: Pal quality inspection, responsibility conflict detection, capability maps, team design, version governance, Eval Lab, and lifecycle workflow.

R40 adds the first v0.2 end-to-end creation productization slice: copyable first-Pal and AI-team task packages, user material ingestion mapping, Pal and AI team health-check runbooks, repair package templates, realistic demos, and an expanded self-test. This is a started / first implementation state, not full v0.2 completion.

This is not a final release state; v0.1 publication is paused while v0.2 is developed.

v0.3 extends PalSmith into an AI Team Builder, team governance guide, cross-Pal review coordinator, publish quality gate, runtime call verification workflow, and GitHub import verification workflow. These remain no-code Runtime Task Package workflows.

v0.4 improves the user-facing path with a 5-minute quickstart, quickstart cheatsheet, AI team blueprints, a 10-minute demo script, a readiness matrix, and a v0.4 regression test plan.

R16 v0.4-fix upgrades PalSmith from file-completeness governance to job fitness governance. PalSmith now inspects whether a Pal can do its declared job, whether its knowledge and skills match real scenarios, whether user materials were preserved without over-compression, and whether optional web research should be turned into traceable knowledge assets before creation or repair.

R17 quality testing in a separate test copy verified that PalSmith can create a job-shaped test Pal with source inventory, source coverage matrix, concrete knowledge, skills, workflows, templates, evals, user material preservation, and a real task simulation. The formal workspace does not include that test Pal or test reports; it keeps only reusable improvements such as the source coverage template and long-material ingestion example.

R168 upgrades PalSmith into a composite Pal creation architect. PalSmith can now plan Human-to-Pal, Voice-to-Pal, Role-to-Pal, Human + Role-to-Pal, Book-to-Pal, Doc-to-Pal, Team-to-Pal, Knowledge-to-Pal, Skill-to-Pal, Agent-to-Pal, and Library-to-Workgroup creation without adding runtime code or automatic registration behavior.

R170 adds user-facing documentation, copyable prompts, and examples for composite Pal creation. These examples are not official Pals and do not prove independent host dialogue acceptance; R169 evidence is local manual asset simulation.

R179 adds a no-code draft-to-user-custom Pal installation flow. This lets PalSmith plan how a reviewed draft Pal Pack can become a user custom Pal under a private-by-default user custom area, without promoting it to official Pal status, without writing central contacts, and without building an installer or runtime service.

## Current Boundary

PalSmith is not a CLI or built-in software tool. It does not scan, validate, import, export, install, package, or restore files by itself.

PalSmith generates Runtime Task Packages. The current Agent Runtime, such as Codex or Claude Code, performs approved file operations and reports evidence.

PalSmith collaboration is selected by current Pal + current Brain / AI judgement. AgentPal Core does not do keyword routing, and Mira is the default entry Pal rather than the only Pal that can call PalSmith.

Task package examples live in `examples/task-packages/`. Reusable task package templates live in `templates/task-packages/`. Their indexes are `examples/task-packages/README.md` and `templates/task-packages/README.md`.

Draft-to-custom installation planning is governed by `core/custom-pal-installation-protocol.md`. The default suggested target is `workspace/resources/user-pals/<pal-id>/`, but PalSmith must present an installation plan and receive explicit user confirmation before any Runtime write.

Release readiness is checked through Markdown evals, including `evals/palsmith-release-scope-eval.md`.

Docs entry points:

- `docs/PalSmith.md`
- `docs/06-palsmith/README.md`
- `docs/06-palsmith/palsmith-end-to-end-productization.md`
- `docs/03-pal-pack-standard/14-runtime-task-package.md`
- `docs/07-authoring-pals/12-use-palsmith.md`
- `docs/07-authoring-pals/13-palsmith-end-to-end-workflows.md`
- `evals/palbench/v0.5/documentation/archive/docs/08-release-candidate/05-no-code-release-checklist.md`
- `evals/palbench/v0.5/documentation/archive/docs/08-release-candidate/06-palsmith-release-scope-review.md`
- `evals/palbench/v0.5/documentation/archive/docs/08-release-candidate/11-palsmith-e2e-test-summary.md`
- `docs/07-authoring-pals/14-palsmith-pal-lifecycle.md`
- `docs/07-authoring-pals/15-palsmith-quickstart-ai-team.md`
- `docs/07-authoring-pals/16-palsmith-demo-script.md`
- `evals/palbench/v0.5/documentation/archive/docs/08-release-candidate/12-palsmith-v0.4-regression-test-plan.md`
- `pals/PalSmith-pal-governor/examples/ai-team-blueprints/README.md`
- `pals/PalSmith-pal-governor/core/pal-readiness-matrix.md`
- `pals/PalSmith-pal-governor/core/pal-quality-inspection-protocol.md`
- `pals/PalSmith-pal-governor/core/user-material-ingestion-protocol.md`
- `pals/PalSmith-pal-governor/core/content-preservation-protocol.md`
- `pals/PalSmith-pal-governor/core/web-research-to-knowledge-protocol.md`
- `pals/PalSmith-pal-governor/skills/README.md`
- `pals/PalSmith-pal-governor/knowledge/README.md`
- `pals/PalSmith-pal-governor/templates/source-coverage-report-template.md`
- `pals/PalSmith-pal-governor/templates/task-packages/create-first-professional-pal.md`
- `pals/PalSmith-pal-governor/templates/task-packages/create-ai-team-from-goal.md`
- `pals/PalSmith-pal-governor/templates/user-material-ingestion-map.md`
- `pals/PalSmith-pal-governor/templates/health-check-report.md`
- `pals/PalSmith-pal-governor/templates/repair-package.md`
- `pals/PalSmith-pal-governor/workflows/user-material-ingestion-to-pal-assets.md`
- `pals/PalSmith-pal-governor/runbooks/classify-user-materials.md`
- `pals/PalSmith-pal-governor/runbooks/pal-health-check.md`
- `pals/PalSmith-pal-governor/runbooks/ai-team-health-check.md`
- `pals/PalSmith-pal-governor/examples/task-packages/example-long-user-material-ingestion.md`
- `pals/PalSmith-pal-governor/examples/create-first-professional-pal.md`
- `pals/PalSmith-pal-governor/examples/create-ai-team-from-user-goal.md`
- `pals/PalSmith-pal-governor/evals/palsmith-e2e-creation-self-test.md`

## Direct Call Examples

```text
/pal PalSmith 创建一个小红书运营 Pal
/pal PalSmith 创建一个跨境电商运营团队
/pal PalSmith 体检所有 Pal
/pal PalSmith 从 GitHub 导入这个 Pal
/pal PalSmith 导出 Research Pal，不含记忆
/pal PalSmith 我想搭建一个 AI 团队帮我做跨境电商
/pal PalSmith 这个 Pal 怎么感觉不好用
/pal PalSmith 用这些资料创建一个可实际工作的私域运营 Pal
/pal PalSmith 给这个 Pal 补行业知识，但保留来源和不确定性
/pal PalSmith 创建一个马斯克思维的产品经理 Pal，并保持公开来源边界
/pal PalSmith 创建一个韩立性格和说话风格的风险审查 Pal，注意版权边界
/pal PalSmith 把我们公司售前专家的经验蒸馏成售前 Pal，先判断隐私和授权
/pal PalSmith 检查 PalSmith 自己是不是技能很多但内容空
/pal PalSmith 这几个 Pal 职责是不是重复
/pal PalSmith 这个团队可以发布吗
/pal PalSmith 这个 Pal 是否真的能被 /pal 调用
/pal PalSmith 请把这个草稿 Pal Pack 安装为我的用户自定义 Pal，先输出安装计划，不要写 official/pals，也不要改 contacts
```

## Composite Creation User Path

Users can start with one sentence. PalSmith should infer the creation mode, state assumptions, ask no more than three focused questions, and output a creation plan before any Runtime file write.

User-facing entry points:

- `docs/PalSmith.md`
- `docs/06-palsmith/README.md`
- `examples/palsmith/composite-pal-creation-examples.md`
- `prompts/palsmith/create-composite-pal.md`

Composite creation keeps source boundaries clear. Public-source-inspired, style-inspired, and organization-internal expert Pals have different publication rules. Organization-internal expert Pals default to private internal use, not public Marketplace listing.

## Safety Boundary

Controlled writes require explicit user confirmation. With-memory export requires strong confirmation and a privacy report. Imported scripts are never executed as part of PalSmith planning. Registry and contacts changes are separate proposals, and ordinary Skills cannot enter contacts.

## Real Task Examples

See `examples/tasks/` for v0.2 PalSmith task examples. These are non-binding examples for Pal creation, AI team design, material ingestion, and Pal health repair packages.
