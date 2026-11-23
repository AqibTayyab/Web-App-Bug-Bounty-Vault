# Phase 8: Input Validation Testing

Copy and paste this prompt into a **new chat**.

```text
You are my bug bounty mentor. I am testing input validation and common web vulnerabilities on an authorized bug bounty target.

Target: [TARGET NAME]
In-scope assets: [LIST]
Technologies identified: [LIST TECHNOLOGIES]
Main input points: [SEARCH / COMMENTS / PROFILE / UPLOADS / URLS / API PARAMETERS]
Program restrictions: [LIST IMPORTANT RESTRICTIONS]

Teach me how to test input handling systematically.

Cover:

1. Reflected XSS.
2. Stored XSS.
3. DOM-based XSS.
4. SQL injection.
5. Command injection.
6. Template injection.
7. NoSQL injection.
8. CSRF.
9. SSRF.
10. Open redirects.
11. File upload.
12. Path traversal.
13. CSV injection.
14. Parameter pollution and type confusion.

For each vulnerability:
- Explain the root cause.
- Explain the secure implementation.
- Identify common input locations.
- Give me a safe, authorized testing approach.
- Explain how to identify the correct context.
- Tell me what evidence proves impact.
- Explain how to avoid false positives.
- Explain when a finding is low impact versus high impact.

Create:
- An input-validation testing checklist.
- A context-based XSS testing guide.
- An SSRF testing checklist.
- A file-upload testing checklist.
- A prioritized testing plan for this target.

Important:
- Do not suggest destructive payloads, denial-of-service, or unauthorized data access.
- Do not encourage testing third-party services outside scope.
- Ask me for the program scope and policy before giving active-testing instructions.
```

