# Schema Checklist

- [ ] `pal.json` parses as JSON.
- [ ] `schema` is present.
- [ ] `id` is stable and unique.
- [ ] `name` and `display_name` are present.
- [ ] `directory_name` matches the directory.
- [ ] `type` is `pal-pack`.
- [ ] `version` is present.
- [ ] `direct_call` uses `/pal Name`.
- [ ] `aliases` do not conflict with registered Pals.
- [ ] `collaboration.discoverable` is explicit.
- [ ] `collaboration.contactable` is explicit.
- [ ] at least one collaboration mode is enabled if the Pal should enter contacts.

If no project-level JSON schema file exists, use the current official Pal `pal.json` pattern as compatibility reference.
