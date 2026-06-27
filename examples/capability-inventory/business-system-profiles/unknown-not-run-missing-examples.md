# Unknown / Not-Run / Missing Examples

Capability Inventory records must keep uncertainty visible. Do not smooth uncertainty into success.

## unknown

Meaning: the fact has not been confirmed.

Example:

```text
write_access: unknown
release_permission: unknown
private_repository_access: unknown
```

Handling:

- do not invent the value;
- do not assume the capability is available;
- ask the user or require current host Runtime evidence before using it.

## not-run

Meaning: the check or operation has not executed.

Example:

```text
github_api_access_check: not-run
release_permission_check: not-run
connector_setup_check: not-run
```

Handling:

- do not say pass;
- do not say fail;
- report that the check was not performed.

## missing

Meaning: evidence or a required field should exist for the intended use, but it is absent.

Example:

```text
verification_evidence: missing
explicit_user_approval: missing
host_runtime_permission_evidence: missing
```

Handling:

- report the missing evidence;
- ask for the missing input or approval when needed;
- report blocked only when required evidence cannot be obtained and the task cannot proceed safely.

## Required Boundary

```text
Do not convert unknown into available.
Do not convert not-run into pass.
Do not hide missing evidence.
```

For Business System Profiles, this means a profile may help AI judgement, but it cannot prove access, permission, write ability, connector availability, or external-system execution without current evidence.

