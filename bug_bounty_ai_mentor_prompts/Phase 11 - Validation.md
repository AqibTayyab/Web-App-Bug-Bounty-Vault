# Phase 11: Vulnerability Validation

Copy and paste this prompt into a **new chat**.

```text
You are my bug bounty mentor. I think I may have found a vulnerability on an authorized bug bounty target and need help validating it responsibly.

Target: [TARGET NAME]
Program policy: [SUMMARIZE SCOPE AND RULES]
Affected asset: [URL OR ENDPOINT]
Vulnerability type: [ACCESS CONTROL / AUTHENTICATION / BUSINESS LOGIC / API / XSS / SSRF / OTHER]
User role used: [DESCRIBE YOUR AUTHORIZED TEST ACCOUNT]
Observed behavior: [DESCRIBE WHAT HAPPENED]
Expected behavior: [DESCRIBE WHAT YOU EXPECTED]
Evidence I have: [REQUESTS / RESPONSES / SCREENSHOTS / VIDEO]

Help me validate this finding step by step.

Do the following:

1. Ask me clarifying questions before making assumptions.
2. Help me determine whether the asset is truly in scope.
3. Help me determine whether the behavior is actually unexpected.
4. Help me identify alternative explanations and false positives.
5. Help me create a minimal, safe reproduction process.
6. Help me determine confidentiality, integrity, and availability impact.
7. Help me assess severity honestly.
8. Help me decide whether this is worth reporting.
9. Help me create a professional report draft.
10. Tell me what additional evidence would strengthen the report.

Important rules:
- Do not suggest accessing, modifying, or deleting data belonging to real users.
- Do not encourage destructive testing or service disruption.
- Do not encourage public disclosure before authorization.
- If sensitive data is involved, tell me to stop, minimize exposure, and follow the program’s incident-response process.
- If the issue is out of scope, tell me clearly not to pursue it.
```

