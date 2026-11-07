# Web Application Security – OWASP Top 10

A practical cybersecurity learning project covering how web applications work, the OWASP Top 10, safe vulnerability testing, secure coding, remediation, and reporting.

## Project objectives

- Understand HTTP requests and responses, cookies, sessions, authentication, and authorization.
- Study the OWASP Top 10: 2025.
- Practise identifying and testing vulnerabilities only in intentionally vulnerable labs or systems where written permission has been granted.
- Document findings, fixes, and retest results.
- Prepare a short demonstration walkthrough.

## Repository structure

- `docs/OWASP-Analysis.md` – OWASP Top 10 overview and study notes.
- `reports/Vulnerability-Report-Template.md` – reusable vulnerability report template.
- `docs/Remediation-Recommendations.md` – secure coding and remediation guidance.
- `docs/Demo-Walkthrough.md` – demonstration plan.
- `lab/README.md` – safe lab scope and workflow.

## OWASP Top 10: 2025

1. Broken Access Control
2. Security Misconfiguration
3. Software Supply Chain Failures
4. Cryptographic Failures
5. Injection
6. Insecure Design
7. Authentication Failures
8. Software or Data Integrity Failures
9. Security Logging and Alerting Failures
10. Mishandling of Exceptional Conditions

Cross-Site Scripting (XSS) is covered in the Injection category in the 2025 list.

## Safe practice environment

Use intentionally vulnerable training applications and labs, such as [PortSwigger Web Security Academy](https://portswigger.net/web-security). Do not scan, probe, exploit, or access real websites or accounts without explicit authorization.

## Lab method

**Identify → Test → Fix → Retest → Document**

For every finding, record the affected component, evidence, impact, severity, remediation, and retest result. Do not include real credentials, session tokens, personal data, or private secrets in this repository.

## Current status

This repository contains starter documentation and templates. Add only findings that you have personally reproduced in an authorized lab, and clearly label exercises that are not yet completed.

## References

- [OWASP Top 10: 2025](https://owasp.org/Top10/2025/)
- [PortSwigger Web Security Academy](https://portswigger.net/web-security)
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)
