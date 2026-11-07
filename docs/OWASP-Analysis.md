# OWASP Top 10: 2025 – Analysis

## Purpose

The OWASP Top 10 is an awareness document describing important categories of web application security risk. It helps developers and testers understand common weaknesses. It is not a complete security checklist or a substitute for a risk assessment.

## 1. Broken Access Control

**Meaning:** The application does not correctly enforce what an authenticated user is allowed to view or change.

**Example:** A user changes an object identifier in a request and can view another user's record.

**Defences:** Enforce authorization on the server for every protected operation; deny by default; check ownership and role permissions; test horizontal and vertical access boundaries.

## 2. Security Misconfiguration

**Meaning:** Application, server, cloud, or framework settings are insecure or unnecessarily exposed.

**Example:** Debug mode or directory listing is enabled in production.

**Defences:** Use secure configuration baselines, remove defaults and unused features, set security headers, restrict administrative interfaces, and review configuration changes.

## 3. Software Supply Chain Failures

**Meaning:** Risks arise from compromised, vulnerable, or poorly controlled software dependencies, build systems, distribution, or update processes.

**Example:** An application includes an outdated dependency with a known security flaw.

**Defences:** Inventory dependencies, use trusted sources, pin and verify versions, review provenance, scan dependencies, and protect build and release pipelines.

## 4. Cryptographic Failures

**Meaning:** Sensitive data is not adequately protected because encryption, key management, or related controls are weak or incorrectly used.

**Example:** Sensitive information is transmitted without transport encryption or passwords are stored in plaintext.

**Defences:** Use TLS, modern vetted cryptographic libraries, strong password hashing such as Argon2id or bcrypt, and secure key storage and rotation.

## 5. Injection

**Meaning:** Untrusted data is interpreted as part of a command or query.

**Examples:** SQL injection, command injection, and cross-site scripting (XSS).

**Defences:** Use parameterized queries, avoid unsafe command construction, apply context-aware output encoding, use safe DOM APIs, and validate input as a supporting control.

## 6. Insecure Design

**Meaning:** Security requirements and threat scenarios were not adequately considered during design.

**Example:** A money-transfer workflow has no meaningful transaction limit or abuse controls.

**Defences:** Threat-model important features, define security requirements, use abuse cases, apply rate limits and business rules, and design authorization checks into workflows.

## 7. Authentication Failures

**Meaning:** Identity verification or account/session management can be bypassed or abused.

**Examples:** Weak password policy, ineffective account recovery, or inadequate protection against automated login attempts.

**Defences:** Use secure password hashing, MFA where appropriate, rate limiting, secure recovery flows, and safe session lifecycle management.

## 8. Software or Data Integrity Failures

**Meaning:** The application trusts software updates, code, or critical data without sufficient integrity verification.

**Example:** A deployment pipeline accepts an unverified build artifact.

**Defences:** Verify signatures and provenance, protect CI/CD permissions, review changes, and use trusted update mechanisms.

## 9. Security Logging and Alerting Failures

**Meaning:** Important security events are not recorded, monitored, or escalated effectively.

**Example:** Repeated failed login attempts are not logged or alerted.

**Defences:** Log relevant authentication and access-control events, protect logs from tampering, monitor suspicious patterns, and never log passwords or session secrets.

## 10. Mishandling of Exceptional Conditions

**Meaning:** Unexpected conditions, errors, and edge cases are handled in ways that create security weaknesses.

**Example:** An exception exposes internal paths, sensitive data, or leaves an operation in an unsafe partial state.

**Defences:** Fail safely, validate assumptions, use consistent error handling, avoid leaking implementation details, and test boundary and failure conditions.

## Core web concepts

### HTTP request and response

A browser sends an HTTP request containing a method, path, headers, and sometimes a body. The server processes it and returns a status code, headers, and an optional response body. HTTPS protects the connection using TLS.

Common methods include GET, POST, PUT, PATCH, and DELETE. Common status codes include 200, 201, 302, 400, 401, 403, 404, and 500.

### Cookies and sessions

A cookie is browser-stored data sent with matching requests. A session is server-side state associated with a client, commonly referenced by a session identifier in a cookie. Session identifiers must be unpredictable and protected. Use HttpOnly, Secure, and an appropriate SameSite attribute where suitable.

### Authentication and authorization

Authentication answers **who are you?** Authorization answers **what are you allowed to do?** Being logged in does not automatically grant access to every resource.

## Study and evidence log

Add your own completed lab observations below. Do not claim a vulnerability was found unless you reproduced it in an authorized lab.

| Date | Topic / lab | Observation | Evidence file | Status |
|---|---|---|---|---|
| YYYY-MM-DD | To be completed | Add your observation | screenshots/ | Not started |

## References

- [OWASP Top 10: 2025](https://owasp.org/Top10/2025/)
- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)
