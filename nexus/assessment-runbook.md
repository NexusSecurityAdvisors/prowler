# Prowler Assessment Runbook

Procedure for running Prowler in a Nexus client engagement. Always check the [upstream documentation](https://docs.prowler.com/) for current flags and provider requirements.

## 0. Before you start

- [ ] Signed SOW and written authorization naming the cloud accounts / subscriptions / projects in scope
- [ ] Client contact available during the scan window
- [ ] Evidence folder created: `<Client>/<YYYY-MM-DD>-prowler/`

## 1. Access (read-only, least privilege)

Ask the client to provision **temporary, read-only** access. Never use a client's personal or admin credentials.

| Provider | Typical access (confirm against upstream docs) |
|---|---|
| AWS | Cross-account role with the AWS managed `SecurityAudit` and `ViewOnlyAccess` policies |
| Azure / M365 | App registration or user with Reader-level / read-only directory roles |
| GCP | Service account with Viewer / Security Reviewer roles |

Record who created the access, when, and when it will be removed.

## 2. Prepare

```bash
pip install prowler        # or use the official container image
prowler -v                 # record the version
prowler <provider> --list-compliance   # confirm framework IDs available
```

## 3. Run

```bash
# Full posture scan
prowler <provider> --output-formats csv json-ocsf html

# Framework-specific scan for readiness work (use an ID from --list-compliance)
prowler <provider> --compliance <framework_id>
```

Save everything from the `output/` folder to the client evidence folder and record a SHA-256 hash of each file.

## 4. Triage

1. Sort by severity (critical / high first).
2. Validate each finding against the live environment; mark false positives with a reason.
3. Group related findings into a single root-cause finding where it makes the report clearer.
4. Rate each on the Nexus 5×5 likelihood × impact scale.
5. Map to frameworks using [`framework-mapping.md`](framework-mapping.md).

## 5. Report and close out

- Complete [`client-report-checklist.md`](client-report-checklist.md).
- Ask the client to remove the temporary role / app registration; confirm in writing.
- Schedule the re-scan (quarterly for vCISO clients).
