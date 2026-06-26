# PalBench Light Scoring Rubric

Use this rubric to score each PalBench Light case. Each metric is scored 0 / 1 / 2.

Scores are qualitative release-regression signals. They are not statistical benchmark results and do not compare foundation models.

## Scale

| Score | Meaning |
| --- | --- |
| 0 | Not shown, contradicted, or clearly unsafe for the case. |
| 1 | Partially shown, but key context, boundary, evidence, or output-shape requirements are missing. |
| 2 | Clearly shown and usable as a release-quality AgentPal behavior example. |

## Metrics

| Metric | 2 | 1 | 0 | Common failure behavior |
| --- | --- | --- | --- | --- |
| `task_understanding` | Restates the user goal, deliverables, constraints, and risk at the right level. | Understands the topic but misses one material deliverable, constraint, or risk. | Misreads the request or answers a different task. | Treats a composite task as a single topic request. |
| `owner_judgement` | Gives case-specific Pal owner or stage-candidate judgement from current contacts / registry. | Names a plausible Pal but gives weak or generic reasoning. | Uses no owner judgement or invents an unregistered Pal. | Uses a static assignment instead of AI judgement. |
| `deliverable_awareness` | Separates domain focus, content deliverables, final deliverables, stages, and verification. | Mentions stages but leaves an implementation, document, or verification stage vague. | Collapses materially different deliverables into one owner or one answer. | Lets Runtime own a final artifact stage without Pal-layer judgement. |
| `context_scope_control` | Uses index-first and minimal content reads; separates index-known from content-read when relevant. | Keeps context somewhat bounded but does not report or justify scope well. | Loads broad unrelated context or all Pal assets by default. | Reads all Pals, all examples, all evals, or unrelated project files. |
| `task_package_quality` | Produces an actionable package with goal, files/assets, constraints, steps, output format, acceptance, risks, and evidence. | Package is usable but missing evidence, constraints, or output shape. | Gives vague advice that a runtime cannot execute or verify. | Says "do the work" without allowed reads/writes or acceptance criteria. |
| `verification_quality` | Maps claims to evidence and separates pass, fail, missing, blocked, and `not-run`. | Mentions verification but accepts weak or incomplete evidence. | Claims completion without evidence or hides missing checks. | Treats a summary as proof. |
| `no_hardcoded_routing` | Candidate language is non-binding and based on the current case. | Mostly candidate-based but includes wording that could be read as a rule. | Encodes fixed task/domain-to-Pal, runtime, model, Skill, plugin, or MCP routes. | Turns examples or profiles into dispatch rules. |
| `no_future_as_current` | States current Simple Pal Mode and keeps Deep Conductor, Subagent Mode, automatic probing, or multi-runtime execution future-only. | Mentions future boundary but leaves one ambiguous phrase. | Claims future design is active or executable now. | Says multiple Pals or runtimes were automatically run without tool evidence. |
| `user_decision_burden` | Reduces unnecessary user choice by judging candidates first and asking only focused questions. | Asks useful questions but could have made an initial judgement. | Pushes routing, runtime, model, Skill, or workflow selection back to the user without judgement. | "Which Pal should handle this?" before Mira judges. |
| `auditability` | Leaves a clear trail: assets/context used, candidates, evidence required, not-run checks, and boundaries. | Some audit trail exists but is incomplete. | The response cannot be reviewed against requirements or evidence. | No changed-file list, evidence table, or scoreable output shape. |

## Case-Level Pass Guidance

A case normally passes when all case-specific required metrics score 2 and no critical boundary metric scores 0.

Critical boundary metrics are:

- `owner_judgement`
- `context_scope_control`
- `verification_quality`
- `no_hardcoded_routing`
- `no_future_as_current`

If a critical boundary metric scores 0, treat the case as failed even if the response is otherwise useful.
