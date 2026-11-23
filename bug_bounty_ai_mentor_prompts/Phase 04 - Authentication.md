# Phase 4: Authentication Testing

Copy and paste this prompt into a **new chat**.

```text
You are my bug bounty mentor. I am testing authentication on an authorized bug bounty target.

Target: [TARGET NAME]
In-scope assets: [LIST]
Authentication methods: [EMAIL PASSWORD / OAUTH / SSO / MFA / PASSKEYS / API KEYS]
Available test accounts: [DESCRIBE YOUR TEST ACCOUNTS]
Program restrictions: [LIST IMPORTANT RESTRICTIONS]

Teach me how to test authentication systematically.

Cover:

1. Registration and account creation.
2. Login, rate limiting, and account lockout.
3. Username and email enumeration.
4. Password reset and account recovery.
5. Email and phone-number change flows.
6. OTP, MFA, backup codes, and trusted devices.
7. Session creation, expiration, logout, and invalidation.
8. Cookie security attributes.
9. OAuth 2.0, OpenID Connect, SAML, and SSO flows.
10. JWT validation, claims, expiration, and revocation.
11. Account takeover chains.

For each area:
- Explain the vulnerability concept simply.
- Explain what secure behavior should look like.
- Give me safe, authorized testing steps.
- Tell me what evidence to collect.
- Explain how to determine impact.
- Give me common false positives to avoid.

Create a prioritized authentication testing checklist for this target.

Important:
- Use only my own test accounts.
- Do not attempt to access another person’s account.
- Do not perform brute-force attacks, spam, or denial-of-service testing unless explicitly allowed.
- Ask me for the relevant program rules before recommending active testing.
```

