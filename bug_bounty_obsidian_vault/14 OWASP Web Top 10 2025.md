# OWASP Web Top 10:2025

OWASP Top 10:2025 is the current awareness standard for critical web application security risks. [web:1]

## The list

| Rank | Risk | What to test |
|---|---|---|
| A01 | Broken Access Control | IDOR, privilege escalation, tenant isolation, forced browsing |
| A02 | Security Misconfiguration | Debug endpoints, insecure headers, exposed docs, default settings |
| A03 | Software Supply Chain Failures | Vulnerable dependencies, exposed packages, build pipeline issues |
| A04 | Cryptographic Failures | Weak encryption, poor key handling, sensitive-data exposure |
| A05 | Injection | SQLi, command injection, template injection, XSS-related injection |
| A06 | Insecure Design | Missing controls, unsafe workflows, weak business rules |
| A07 | Authentication Failures | Weak login, session issues, MFA bypass, credential handling |
| A08 | Software or Data Integrity Failures | Unsafe updates, insecure deserialization, untrusted data |
| A09 | Logging and Alerting Failures | Missing audit logs, weak monitoring, insufficient incident response |
| A10 | Mishandling of Exceptional Conditions | Error leakage, unsafe fallback behavior, unhandled failures |

Source: OWASP Top 10:2025. [web:1][web:2]

## How to use it

Do not treat the OWASP Top 10 as a complete testing methodology. Use it as a prioritization framework.

For bug bounty, prioritize:

1. Broken access control
2. Authentication and account takeover
3. Business logic
4. API authorization
5. SSRF and file handling
6. Sensitive data exposure
7. Misconfiguration with impact
8. AI/LLM risks where applicable

## Important note

A missing security header is not automatically a vulnerability. Always demonstrate a realistic security impact.

