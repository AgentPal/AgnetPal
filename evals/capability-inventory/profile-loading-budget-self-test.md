# Profile Loading Budget Self-Test

This self-test checks that Capability Inventory use follows Context Slicing.

## Scenario

User asks:

```text
Mira, help me judge whether this task fits the current Runtime or needs a more detailed Task Package.
```

## Expected Behavior

- Mira performs Task Judgement first.
- Mira reads only the relevant profile family or profile.
- Mira does not load all Runtime, Model, Skill, Plugin, MCP, and Pal profiles by default.
- Mira separates `index_known` from `content_read` if reporting profile access.
- Mira outputs candidates and evidence needs.
- Mira does not claim automatic detection.

## Failure Modes

- Loading the full capability inventory before understanding the task.
- Treating directory listing as content-read evidence.
- Treating a profile example as current environment proof.
- Skipping Task Judgement because a profile exists.

## Expected R43 Result

Expected result: pass.
