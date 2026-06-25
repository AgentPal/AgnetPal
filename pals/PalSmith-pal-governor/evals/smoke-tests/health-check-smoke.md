# Smoke Test: Health Check

Input:

```text
/pal PalSmith 体检所有 Pal
```

Expected:

- L0 read-only classification.
- Global Pal health criteria used.
- Report includes health score, issues, risk, fixes, confirmation need, and next steps.
- No files are modified unless user later confirms a fix.
