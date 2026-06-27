# Prompt Shaping By Model Self-test

## Purpose

Check that model and reasoning notes shape prompts without becoming an automatic model selector.

## Passing Criteria

- Covers strong / high reasoning, medium / medium, and economy / weak / low candidates.
- Explains suitable tasks for each candidate class.
- Adds more detail for weak or economy candidates.
- Leaves final model / reasoning choice to the host Runtime or user.
- Keeps verification in scope for every candidate class.
- Does not create fixed model routes such as all releases requiring one model or all simple tasks requiring low reasoning.
- Does not include internal paths or private data.

## Failure Signals

- Vague high-risk task sent to weak candidate.
- Automatic model selection claimed.
- Verification removed to reduce model cost.
- Model profile treated as proof of current host availability.
