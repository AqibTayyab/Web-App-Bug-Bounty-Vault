# Phase 5: Authorization Testing

Copy and paste this prompt into a **new chat**.

```text
You are my bug bounty mentor. I am testing authorization on an authorized bug bounty target.

Target: [TARGET NAME]
In-scope assets: [LIST]
Application type: [SAAS / E-COMMERCE / MULTI-TENANT / SINGLE USER]
My test accounts: [LIST ACCOUNTS AND ROLES]
Features identified: [LIST MAIN FEATURES]
Program restrictions: [LIST IMPORTANT RESTRICTIONS]

Teach me how to find high-impact authorization vulnerabilities.

Cover:

1. Horizontal access control and IDOR.
2. Vertical privilege escalation.
3. Function-level authorization.
4. Object-level authorization.
5. Role-based access control.
6. Multi-tenant and organization isolation.
7. File and document access.
8. Admin functionality.
9. API endpoint authorization.
10. Hidden UI functionality.
11. Role assignment and ownership transfer.
12. Business-role abuse.

For each area:
- Explain the concept with a simple example.
- Show me how to build a test matrix.
- Teach me how to compare requests between authorized users.
- Explain how to identify object identifiers and access patterns.
- Tell me what evidence proves real impact.
- Help me avoid false positives.
- Explain how to distinguish an access-control bug from intended behavior.

Create:
- An authorization testing matrix.
- A prioritized list of high-value objects to test.
- A checklist for each user role.
- A method for documenting findings safely.

Important:
- I will only use accounts and objects I am authorized to access.
- Do not encourage me to access, modify, or delete another real user’s data.
- Ask me for the program scope and policy before recommending active testing.
```

