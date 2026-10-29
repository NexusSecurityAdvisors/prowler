# Prowler at Nexus Security Advisors

This is the Nexus Security Advisors fork of [prowler-cloud/prowler](https://github.com/prowler-cloud/prowler), the open-source cloud security posture tool (Apache-2.0).

**The upstream code is unchanged.** This `nexus/` folder adds how we use Prowler in client engagements.

## How Nexus uses it

| Engagement | Use |
|---|---|
| **Fractional vCISO** | Baseline and quarterly re-scans of client AWS, Azure, GCP, M365, and Google Workspace environments to track posture over time |
| **Compliance readiness** | Framework-specific scans (e.g., CIS, NIST CSF, NIST 800-171, HIPAA, SOC 2) as input to gap assessments |
| **Security posture assessment** | Automated evidence for the cloud portion of our NIST CSF 2.0 posture review |

Prowler output is **evidence, not the deliverable.** Every finding is validated, risk-rated, and translated into plain-English remediation before it reaches a client.

## Contents

| File | Purpose |
|---|---|
| [`assessment-runbook.md`](assessment-runbook.md) | Step-by-step client assessment procedure |
| [`framework-mapping.md`](framework-mapping.md) | How Prowler results map to NIST CSF 2.0, CMMC / 800-171, HIPAA, and SOC 2 |
| [`client-report-checklist.md`](client-report-checklist.md) | Quality gate before a report goes to a client |

## Keeping this fork current

Sync with upstream before every engagement (**Sync fork** on GitHub) and record the Prowler version used in the client evidence folder.

## Disclaimer

Automated scan results are a point-in-time view and do not constitute an audit opinion, certification, or legal advice.

---

**Nexus Security Advisors** · Fractional CISO and AI governance for SMBs · SDVOSB
[nexussecurityadvisors.com](https://nexussecurityadvisors.com) · [info@nexussecurityadvisors.com](mailto:info@nexussecurityadvisors.com)
