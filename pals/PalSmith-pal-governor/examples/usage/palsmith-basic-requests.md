# PalSmith Basic Requests

## Create Pal

```text
/pal PalSmith 创建一个小红书运营 Pal
```

Expected behavior: PalSmith generates a Pal creation plan and asks for confirmation before file writes.

## Import Pal

```text
/pal PalSmith 从 GitHub 导入这个 Pal Pack
```

Expected behavior: PalSmith stages first, scans risk, classifies the resource, and asks installation questions.

## Export Pal

```text
/pal PalSmith 导出 Research Pal，不含记忆
```

Expected behavior: PalSmith uses Clean Pack Export, excludes memory/state/reports, prepares manifest fields, and requires Runtime evidence for packaging.
