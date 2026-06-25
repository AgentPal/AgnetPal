# Regression: GitHub Import Staging

GitHub imports must not install directly into `pals/`.

Required behavior:

- stage first
- classify resource type
- scan risks
- check license and ID conflict
- ask user confirmation
- add to contacts only if valid Pal Pack and confirmed
