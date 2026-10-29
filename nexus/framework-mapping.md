# Framework Mapping: Prowler Findings

How to map Prowler finding categories to the frameworks Nexus clients care about. This is a **family-level starting point**. Prowler's built-in compliance outputs give check-level mappings for many frameworks; validate each mapping against the specific control text before it goes into a client report.

| Prowler finding area | NIST CSF 2.0 | NIST SP 800-171 / CMMC L2 | HIPAA Security Rule | SOC 2 (TSC) |
|---|---|---|---|---|
| IAM, MFA, root/admin usage, key rotation | PR.AA | 3.1 Access Control, 3.5 Identification & Authentication | §164.312(a) Access control, §164.312(d) Authentication | CC6.1–CC6.3 |
| Encryption at rest / in transit, key management | PR.DS | 3.13 System & Communications Protection | §164.312(a)(2)(iv) Encryption, §164.312(e) Transmission security | CC6.1, CC6.7 |
| Logging, monitoring, alerting (e.g., audit trails, flow logs) | DE.CM, DE.AE | 3.3 Audit & Accountability | §164.312(b) Audit controls | CC7.2–CC7.3 |
| Secure configuration, public exposure, network rules | PR.PS, PR.IR | 3.4 Configuration Management, 3.13 SC | §164.308(a)(1) Security management process | CC6.6, CC8.1 |
| Vulnerability / patch posture, outdated runtimes | ID.RA, PR.PS | 3.11 Risk Assessment, 3.14 System & Information Integrity | §164.308(a)(1)(ii)(A) Risk analysis | CC7.1 |
| Backup, versioning, resilience | PR.DS, RC.RP | 3.8 Media Protection (backups), 3.6 Incident Response | §164.308(a)(7) Contingency plan | A1.2–A1.3 |
| Asset inventory, tagging, unused resources | ID.AM | 3.4 CM (baseline / inventory) | §164.310(d) Device & media controls | CC6.1 |

## Notes

- CMMC Level 2 practices align with NIST SP 800-171 requirements. Cite the 800-171 requirement number in reports.
- HIPAA is risk-based. Present findings as inputs to the client's risk analysis, not as pass/fail compliance.
- SOC 2 mapping depends on the client's own control set and their auditor's judgment. Use this mapping for readiness only.
