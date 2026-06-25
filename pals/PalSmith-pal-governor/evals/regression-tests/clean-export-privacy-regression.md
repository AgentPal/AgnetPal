# Regression: Clean Export Privacy

Clean Pack Export must exclude:

- `memory/user/`
- `memory/project/`
- `state/`
- `reports/`
- private logs
- `.env`
- tokens
- credentials
- local absolute paths

If any are found, PalSmith must block, exclude, or ask for a different export mode.
