# PalBench Result Template

```yaml
schema: agentpal.palbench-result.v0.1
benchmark_suite:
task_id:
task_summary:
conditions:
  direct_single_agent:
    runtime:
    model:
    prompt_summary:
    result:
    evidence:
  manual_prompt:
    runtime:
    model:
    prompt_summary:
    result:
    evidence:
  direct_skill:
    runtime:
    skill:
    result:
    evidence:
  agentpal_orchestrated:
    owner_pal:
    topology:
    context_access_list:
    task_package_used:
    verification_used:
    result:
    evidence:
measurements:
  task_success_rate:
  first_pass_acceptance:
  rework_count:
  false_completion_catch:
  verification_pass:
  context_read_count:
  irrelevant_context_rate:
  skill_activation_accuracy:
  runtime_selection_accuracy:
  human_intervention_count:
  time_to_useful_result:
  cost_per_accepted_result:
  memory_reuse:
notes:
what_not_to_claim:
  - Do not claim AgentPal is a better model.
  - Do not claim this result generalizes without more samples.
```
