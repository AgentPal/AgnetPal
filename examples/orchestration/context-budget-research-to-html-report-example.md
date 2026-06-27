# Context Budget Research To HTML Report Example

## User Input

Research a trend, write a report, and prepare an HTML page package.

## Context Budget Plan

```yaml
schema: agentpal.context_budget_plan.v0.1
budget_id: cbp-research-html-example
task_type: composite
risk_level: medium
quality_target: usable
latency_preference: balanced
cost_sensitivity: medium
initial_read_tier: 1
max_read_tier: 4
index_known_paths: [docs index, source inventory index, design template index]
memory_to_use: [prior approved research brief summary]
profiles_to_read: [research Runtime profile, browser Skill profile, document Skill profile]
summary_sources: [source inventory summaries]
full_content_required:
  - path: selected source notes
    reason: claims need source-backed evidence
forbidden_context: [unrelated user documents, private notes, full chat history]
runtime_skill_candidates: [browser research Skill candidate, HTML preview Skill candidate]
verification_context: [source list, claim-evidence matrix, rendered-page evidence]
not_a_token_meter: true
```

## Prompt Shaping Notes

Use medium / medium for the bounded report package after research questions are clear. Use stronger reasoning if source contradictions appear. HTML implementation package should include file boundaries and acceptance criteria.

## Runtime Skill Candidates

Browser or web research candidates may reduce manual source gathering. HTML preview candidates may reduce rework. The host Runtime must confirm availability.

## Verification Plan

Verify source freshness, claim support, and page render evidence. Missing browser evidence is `not-run`, not a pass.

## Context Usage Report

Record summaries reused, full sources opened, Runtime Skills used or not-run, and verification evidence.

## Routing Memory Candidate

Record that research-to-HTML tasks benefit from index-first source selection and a separate verification context. Do not turn this into a fixed Vega / Atlas route.

## No-code Boundary Note

The example describes a package. AgentPal does not browse, build, preview, or deploy by itself.
