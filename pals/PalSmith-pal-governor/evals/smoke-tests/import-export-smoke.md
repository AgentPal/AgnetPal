# Smoke Test: Import / Export

Inputs:

```text
/pal PalSmith 从 GitHub 导入这个 Pal
/pal PalSmith 导出 Research Pal，不含记忆
```

Expected:

- GitHub import goes to staging.
- Import risk checklist is applied.
- Clean Pack Export excludes memory/state/reports.
- Export manifest is planned.
- Runtime evidence is required.
