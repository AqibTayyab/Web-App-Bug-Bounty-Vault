# Old vs Modern Bug Bounty Methodology

## What has changed

| Area | Older methodology | Modern methodology |
|---|---|---|
| Target | Static website | SPA, API, mobile backend, cloud, microservices |
| Main focus | SQLi, XSS, CSRF | Access control, APIs, business logic, cloud, identity |
| Recon | Subdomains and directories | JavaScript analysis, API discovery, cloud assets, secrets |
| Authentication | Password and session testing | OAuth, OIDC, SSO, JWT, passkeys, MFA |
| Authorization | Basic IDOR | Multi-tenant isolation, object-level and function-level authorization |
| Testing | Manual browser testing | Manual testing plus controlled automation |
| AI | Not common | LLM, RAG, agents, plugins, prompt injection |
| Reporting | Basic PoC | Impact-first, reproducible, professional report |
| Scope | Often unclear | Strict scope, safe harbor, disclosure rules |

## What has not changed

These principles remain constant:

- Authorization must be enforced on the server.
- User input must be validated and encoded correctly.
- Sensitive data must be protected.
- Security cannot depend only on the frontend.
- Business logic must be tested by humans.
- Impact matters more than technical novelty.

## Modern testing order

1. Read scope and policy.
2. Perform reconnaissance.
3. Map application and roles.
4. Test authentication.
5. Test authorization.
6. Test APIs.
7. Test business logic.
8. Test input handling.
9. Test cloud and configuration.
10. Test AI features if authorized.
11. Write a professional report.

## What to prioritize

For most web bug bounty targets, spend the most time on:

- Broken access control
- IDOR
- Privilege escalation
- Account takeover
- Payment and billing logic
- API authorization
- Organization and tenant isolation
- File access
- Password reset
- OAuth misconfiguration
- AI feature abuse

## Why access control is king

A missing security header may be low impact. A broken access-control issue may allow one user to access another user’s private data, modify account settings, or perform administrative actions.

That is why OWASP places Broken Access Control first in its 2025 web list. [web:1][web:2]

