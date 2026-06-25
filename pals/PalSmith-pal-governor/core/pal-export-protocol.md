# Pal Export Protocol

PalSmith must ask for export mode before exporting a Pal.

## Export Types

1. Clean Pack Export / 干净发布包
2. With Memory Export / 含记忆完整包
3. Template Export / 模板包
4. Team Export / 团队包
5. Backup Export / 本地备份包

## Required First Question

When the user says "导出 <Pal>", ask:

```text
请选择导出方式：

1. 干净发布包
不包含用户记忆、项目记忆、运行状态和报告。适合发 GitHub、分享、发布到 Pal Hub。推荐。

2. 含记忆完整包
包含 memory / state / reports / 历史使用记录。适合个人备份或换电脑迁移。可能包含隐私信息。

3. 模板包
只保留结构和基础说明，去掉具体知识和记忆。适合给别人复用。

4. 团队包
如果该 Pal 属于某个团队，可以连同团队结构一起导出。

5. 本地备份包
用于升级或修改前备份，不建议分享给别人。
```

## With Memory Follow-Up

If the user chooses With Memory Export, ask which memory to include:

- A. tool usage memory only
- B. project memory
- C. user preference memory
- D. collaboration memory
- E. reports and state
- F. all

Warn that C, D, E, and F may include private data and are not suitable for public sharing.

## Clean Pack Includes

- `PAL.md`
- `SKILL.md`
- `AGENTS.md`
- `pal.json`
- `README.md`
- `CHANGELOG.md`
- `LICENSE`
- `identity/`
- `core/`
- `knowledge/`
- `skills/`
- `runbooks/`
- `workflows/`
- `tools/`
- `evals/`
- `adapters/`
- `export-manifest.json`
- `export-report.md`

## Clean Pack Excludes

- `memory/user/`
- `memory/project/`
- `state/`
- `reports/`
- `reasoning/solution-log.md`
- `reasoning/decision-trace.md`
- `contacts/handoff-history.md`
- runtime private logs
- user private files
- `.env`
- credentials
- tokens

## Pre-Export Risk Checks

Check `memory/user`, `memory/project`, `state`, `reports`, `.env`, token/key/password strings, real user names, absolute path privacy, private project information, private contacts, external service credentials, unauthorized third-party materials, large files, binaries, imported third-party resources, and unknown licenses.

## Manifest Fields

Every export plan must include an `export-manifest.json` template with:

```text
schema
export_type
exported_at
exported_by
agentpal_version
pal_id
pal_name
pal_version
source_path
included_sections
excluded_sections
contains_memory
contains_user_memory
contains_project_memory
contains_state
contains_reports
contains_private_data_risk
license
compatible_runtimes
checksum
```
