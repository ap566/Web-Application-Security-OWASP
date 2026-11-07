# Secure Coding and Remediation Recommendations

These are general defensive recommendations. Choose controls appropriate to the application and verify them through testing.

## Access control

- Enforce authorization on the server for every protected request.
- Deny access by default.
- Check the user's role, ownership, and permitted action for each object.
- Do not rely on hidden buttons or client-side checks.
- Test direct requests and attempts to access other users' records.

## Injection and XSS

- Use prepared statements / parameterized queries for database access.
- Avoid building shell commands from untrusted input.
- Prefer safe framework APIs and context-aware output encoding.
- Use textContent rather than assigning untrusted content to innerHTML.
- Apply a carefully tested Content Security Policy as an additional defence, not as a replacement for safe output handling.

## Authentication and sessions

- Store passwords with a dedicated password-hashing algorithm such as Argon2id or bcrypt.
- Offer MFA where appropriate and rate-limit authentication attempts.
- Use secure account recovery and avoid revealing whether an account exists.
- Regenerate session identifiers after login or privilege changes.
- Expire sessions appropriately and provide logout/session revocation.
- Set cookies with Secure, HttpOnly, and an appropriate SameSite value.

## Cryptography and sensitive data

- Use HTTPS/TLS for data in transit.
- Use vetted cryptographic libraries and modern algorithms.
- Keep keys and secrets out of source code and version control.
- Restrict access to secrets and rotate them when exposure is suspected.
- Avoid collecting or retaining sensitive data without a clear need.

## Configuration and dependencies

- Disable debug features and default accounts in production.
- Remove unused services, endpoints, and sample files.
- Apply security headers and least-privilege permissions.
- Maintain a dependency inventory and update vulnerable packages.
- Protect build pipelines, deployment credentials, and release artifacts.

## Logging and exception handling

- Log security-relevant events without recording passwords, tokens, or unnecessary personal data.
- Protect logs against unauthorized access and modification.
- Monitor repeated failures and unusual access patterns.
- Return safe, generic error messages to users; keep diagnostic detail in protected logs.
- Ensure failed operations do not leave data in an inconsistent state.

## Verification checklist

- [ ] Authorization is enforced server-side.
- [ ] Database queries use parameters.
- [ ] Untrusted output is safely encoded.
- [ ] Authentication and recovery flows are tested.
- [ ] Session cookies use appropriate security attributes.
- [ ] Secrets are not committed to the repository.
- [ ] Dependencies and configuration are reviewed.
- [ ] Security events are logged safely.
- [ ] Error handling does not expose sensitive internals.
- [ ] Fixes have been retested.

## References

- [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)
- [OWASP ASVS](https://owasp.org/www-project-application-security-verification-standard/)
