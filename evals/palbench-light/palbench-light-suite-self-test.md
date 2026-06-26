# PalBench Light Suite Self-Test

Use this self-test before a release or after changing PalBench Light cases.

This is a Markdown release check, not an automated validator or script.

## Required Checks

| Check | Expected result |
| --- | --- |
| Task index count | `task-index.md` lists at least 20 cases. |
| Case file existence | Every indexed case file exists under `evals/palbench-light/`. |
| User Input | Every case includes `## User Input`. |
| Baseline Behavior | Every case includes `## Baseline Behavior`. |
| Expected AgentPal Behavior | Every case includes `## Expected AgentPal Behavior`. |
| Scoring Rubric | Every case includes `## Scoring Rubric`. |
| Failure Modes | Every case includes `## Failure Modes`. |
| Not a model benchmark | Every case notes that it is an agent-usage workflow eval, not a model benchmark. |
| No hardcoded routing | Cases use candidates and negative examples only; they do not define task/domain-to-Pal rules. |
| No future-as-current | Deep Conductor, Subagent Mode, automatic probing, and multi-runtime execution remain future-only unless explicitly marked as future design. |
| No internal path leakage | Public cases do not contain private local paths, internal report directories, or sensitive credential material. |
| No runtime artifact | The suite adds Markdown only; it does not add scripts, CLIs, scanners, validators, installers, daemons, services, UI, or dependency manifests. |

## Manual Spot Checks

Run at least six dry-run reviews before a release:

- one Mira-first case;
- one direct `/pal Name` case;
- one composite deliverable case;
- one context-scope case;
- one verification / false-completion case;
- one PalSmith / AI team case.

For each dry run, record:

- case id;
- whether the user input is understandable;
- whether expected behavior is clear;
- whether scoring is usable;
- whether ambiguity was found;
- whether the case needs repair.

## Pass / Block Guidance

Pass when:

- all required checks are satisfied;
- dry-run notes show the selected cases are understandable and scoreable;
- any known ambiguity is documented with a repair decision.

Block when:

- fewer than 20 cases are indexed;
- a case file is missing;
- cases claim model benchmark significance;
- cases encode a fixed route as a real rule;
- cases claim future orchestration is active;
- public files contain internal paths or private data.
