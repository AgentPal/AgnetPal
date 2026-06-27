# Rhea Runtime Capability Profile Budget Example

Rhea：Runtime capability profile 读取本身也要有边界。

Safe package shape:

- name the Runtime / Skill / plugin / MCP candidates
- read only relevant capability profiles
- ask the host Runtime for current availability evidence
- avoid broad host inspection
- report unavailable, unknown, blocked, and not-run honestly
- do not claim exact token or cost values without host metering evidence

This remains no-code safety review, not automatic capability discovery.
