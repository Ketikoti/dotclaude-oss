# Rule: Security

> Aligned with OWASP Top 10. Security is non-negotiable.

## Authentication & Authorization

- Always use established auth libraries (e.g. Auth0, NextAuth, FastAPI-Users)
- Never implement custom JWT signing without security review
- Enforce least-privilege: users only access what they need
- Always validate permissions server-side, never trust client

## Input Validation

- Validate and sanitize ALL user inputs
- Use schema validation (Pydantic, Zod, Joi)
- Reject unexpected fields (strict mode)
- Parameterize all database queries (no raw SQL string concatenation)

## Secrets Management

- Never hardcode secrets, API keys, or credentials in code
- Use environment variables (.env) or secret managers (GCP Secret Manager, Azure Key Vault)
- Never commit .env files (use .env.example instead)
- Rotate keys if accidentally exposed

## Dependencies

- Regularly audit dependencies: `npm audit` / `pip-audit`
- Pin dependency versions in production
- Remove unused dependencies

## Data Protection

- Encrypt sensitive data at rest and in transit
- Use HTTPS only in production
- Never log sensitive user data (passwords, tokens, PII)
- Apply GDPR-compliant data handling for EU users

## API Security

- Rate-limit all public endpoints
- Implement CORS properly (no wildcard in production)
- Use security headers (CSP, HSTS, X-Frame-Options)
- Validate Content-Type headers

## Incident Response

- If a secret is exposed: rotate immediately, audit access logs
- Document and report security issues via SECURITY.md
