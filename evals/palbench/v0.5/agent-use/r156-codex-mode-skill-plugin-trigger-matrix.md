# R156 Codex Mode / Skill / Plugin Trigger Matrix

Status: executed
Date: 2026-06-29

| Capability | Should trigger when | Should not trigger when | Actual trigger in R156 | Correct? | Reason |
| --- | --- | --- | --- | --- | --- |
| GitHub / gh-fix-ci | PR CI evidence or PR link is available and user authorizes remote inspection | PR link/repo missing or write action not authorized | Triggered as candidate only | correct | R156-02 asked for PR/repo/auth first |
| GitHub / gh-address-comments | Review threads/comments evidence is available | repo/PR missing or no auth | Triggered as candidate only | correct | R156-03 asked for repo/PR first |
| Product Design audit/get-context | URL/screenshot and audit brief are available | URL/image missing | Triggered as candidate only | correct | R156-04 and R156-05 required URL/image/brief |
| Product Design image-to-code | screenshot/image and target framework are available | image/framework/interaction missing | Triggered as candidate only | correct | R156-05 required screenshot and framework |
| HyperFrames / website-to-hyperframes | Website URL plus video goal/brand/audience is available | URL/brand missing | Triggered as candidate only | correct | R156-06 asked for URL/audience/style |
| Notion | User provides Notion page/database or pasted source and authorizes write | source/auth missing | Triggered as candidate only | correct | R156-07/R156-08 separated planning from Notion writes |
| Lark | User provides Lark docs/sheets/task/calendar targets and auth/scope is available | auth/scope/source missing | Triggered as candidate only | correct | R156-09 named object-specific Lark skills and required auth |
| documents/spreadsheets/presentations/pdf | Files are supplied and desired output is clear | files missing | Triggered as candidate only | correct | R156-10 asked for files/audience/pages |
| OpenAI docs | User asks for current OpenAI/Codex/API guidance | stable local-only advice is enough | Triggered as candidate with freshness caveat | correct | R156-11 avoided stale latest claims |
| skill-creator/plugin-creator | User creates Codex skill/plugin | Pal-owned Skill should go under owner Pal, not Codex skill by default | `skill-creator` candidate, PalSmith owner | correct | R156-12 kept Faye Skill under Pal-owned boundary |
| Cloudflare skills | User asks for Workers/Durable Objects/Wrangler architecture or deploy plan | user says no deploy or no auth for deploy | Triggered as architecture/scaffold candidate only | correct | R156-13 explicitly did not deploy |
| Browser control | User provides local URL and server is running | no URL/server evidence | Triggered as candidate only | correct | R156-14 required localhost URL |
| Codex Plan Mode | Need design/approval before edits or unclear high-risk scope | trivial rewrite | Partially explicit | partial | R156-01 used Task Package/Agent mode, not explicit Plan/Goal labels |
| Codex Goal Mode | User asks for sustained implementation with verification | missing repo/scope or user only asks for advice | Partially explicit | partial | Mode judgement was present but not always named as Goal Mode |
| Codex subthread/subagent | Independent review, parallel audit, or owner+verifier split adds value | simple rewrite or single-owner small task | Suggested ask-confirmation for R156-15 only | correct | No fake parallel execution |
| Claude Code | User has Claude Code and task benefits from Claude project/session workflow | not installed/not authenticated/not suited | Handoff prompt suggested; controller verified minimal call | partial | Tested thread did not know controller-level Claude evidence |
| CodeWhale personal skill | User asks for CodeWhale and local capability is confirmed | capability unknown or no approval | Triggered as candidate only | correct | R156-17 required confirmation/approval |
| Simple rewrite anti-trigger | No plugin/multi-Pal/heavy mode needed | complex writing strategy or brand constraints | No plugin/subthread, low reasoning, Harper direct rewrite | correct | R156-18 avoided heavy machinery |
