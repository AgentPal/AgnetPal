# Git Tag And Release Process

This page records the release-process boundary for v0.1.0-rc.1.

## Observed Local Git Evidence

During this documentation pass, the repository showed:

- local tag: `v0.1.0-rc.1`
- tagged commit observed: `f2abd6f8a0635f0501c86c6951939a23d92816cc`
- commit subject observed: `chore: finalize AgentPal v0.1.0-rc.1 release`
- commit date observed: `2026-06-24T03:30:10+08:00`

No remote output was available from the observed repository state, and no online GitHub Release was created or verified during this pass.

The working tree may contain documentation changes after the observed local tag. If so, maintainers should commit those final contents and retag `v0.1.0-rc.1` before publishing.

## Maintainer Process

Before publishing:

1. Confirm the working tree contains only intended public release files.
2. Run public-safe review for secrets, private state, local paths, and future-feature overclaims.
3. Confirm Markdown and JSON files required for the release are valid enough for publication.
4. Commit the final intended release contents.
5. Create or update the annotated `v0.1.0-rc.1` tag to point to the intended release commit.
6. Create the GitHub repository if it does not exist yet.
7. Add the intended `origin` remote.
8. Push the release commit to the intended branch.
9. Push tag `v0.1.0-rc.1`.
10. Create the GitHub Release from the pushed tag.
11. Paste or adapt `GITHUB_RELEASE_DRAFT.md` into the release body.
12. Confirm the release page links to the intended tag and commit.

## Do Not Overstate

Do not write that v0.1.0-rc.1 has been published online until the tag has been pushed and the GitHub Release page exists.

Do not treat a local tag as proof of a remote release.
