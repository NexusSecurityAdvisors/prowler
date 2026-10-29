# Client Report Checklist

Use this checklist before any assessment report built from this tool goes to a Nexus Security Advisors client.

## 1. Authorization and scope

- [ ] Signed engagement letter / SOW covers this assessment
- [ ] Written authorization names the tenant(s), account(s), or environment(s) assessed
- [ ] Scope, exclusions, and assessment dates are stated in the report
- [ ] Assessment ran with read-only, least-privilege access as defined in the runbook

## 2. Evidence integrity

- [ ] Raw tool output (JSON/CSV/HTML) saved to the client's evidence folder with date and tool version
- [ ] Tool version and upstream commit recorded
- [ ] Hash (SHA-256) of raw output recorded
- [ ] No client data stored in this repository, a personal device, or an unapproved location

## 3. Findings quality

- [ ] Every finding validated: false positives removed, with a short reason
- [ ] Accepted risks and compensating controls noted, not deleted
- [ ] Each finding rated on the Nexus 5×5 likelihood × impact scale
- [ ] Each finding mapped to NIST CSF 2.0 (and CMMC / HIPAA / SOC 2 where in scope) — see `framework-mapping.md`
- [ ] Remediation written in plain English with an owner and a target date

## 4. Executive readiness

- [ ] One-page executive summary: overall posture, top 5 risks, recommended next 90 days
- [ ] No jargon without a one-line explanation
- [ ] Positive findings included (what is working)
- [ ] Limitations stated: point-in-time, automated checks, not a certification or audit opinion

## 5. Delivery

- [ ] Report uses Nexus branding (navy / steel-silver / blue) and the current template
- [ ] Peer review or second read completed
- [ ] Delivered through an encrypted channel; access limited to named client contacts
- [ ] Temporary credentials, app registrations, and service accounts created for the assessment removed or disabled, and removal confirmed with the client
- [ ] Retest / follow-up date scheduled

---

*Nexus Security Advisors · info@nexussecurityadvisors.com · nexussecurityadvisors.com*
