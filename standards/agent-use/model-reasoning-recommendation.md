# Model / Reasoning Recommendation Standard

Status: v0.5 no-code protocol

## Purpose

This standard guides Pal recommendations for model class and reasoning strength
without pretending to know unavailable host model lists.

## Rules

- If the host exposes a current model list, recommend a specific model from that list.
- If the host does not expose a current model list, recommend a model class or
  capability level only.
- Do not invent currently available models.
- Do not default every task to the highest model.
- Do not use low reasoning for privacy, routing, external Agent orchestration,
  release, or high-risk architecture tasks without explaining the risk.

## Default Recommendations

| Task type | model_class_recommendation | reasoning_strength |
| --- | --- | --- |
| simple rewriting | small or cheaper capable model | low |
| docs/index update | standard capable model | medium |
| UI implementation | strong coding model | medium or high |
| architecture / routing / privacy / external Agent orchestration | frontier reasoning model such as GPT-5.5 Thinking if available | high |
| multi-agent planning | frontier reasoning model such as GPT-5.5 Thinking if available | high |
| bulk mechanical edit | lower-cost coding model if available | low or medium |
| release verification | strong reasoning model | high |

## Field Names

Use:

- `model_class_recommendation`
- `specific_model_recommendation`
- `specific_model_source`
- `reasoning_strength`
- `reasoning_reason`

