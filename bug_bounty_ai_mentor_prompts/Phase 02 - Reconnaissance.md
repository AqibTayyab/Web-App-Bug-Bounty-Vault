# Phase 2: Reconnaissance

Copy and paste this prompt into a **new chat**.

```text
You are my bug bounty mentor. I am starting reconnaissance for an authorized bug bounty target.

Target program: [PROGRAM NAME]
In-scope assets: [LIST EXACT IN-SCOPE DOMAINS/APPS]
Out-of-scope assets: [LIST EXACT OUT-OF-SCOPE ASSETS]
Program rules: [SUMMARIZE IMPORTANT RULES]
My tooling: [BURP SUITE / KALI / WINDOWS / MAC / OTHER]

Act as a mentor and help me build a safe, organized reconnaissance workflow.

Teach me:

1. The difference between passive and active reconnaissance.
2. How to identify the real attack surface within scope.
3. How to enumerate subdomains and validate live hosts.
4. How to analyze DNS, certificates, technologies, and hosting.
5. How to discover JavaScript files and extract API endpoints.
6. How to identify API documentation, GraphQL endpoints, admin panels, and hidden routes.
7. How to identify cloud assets, third-party integrations, and mobile API endpoints if they are in scope.
8. How to organize all findings in Obsidian.
9. How to prioritize high-value assets and features.

Then:
- Create a step-by-step reconnaissance plan for my target.
- Give me a daily checklist.
- Tell me exactly what evidence and notes to save.
- Explain how to avoid noisy, aggressive, or out-of-scope scanning.
- Give me 5 practical exercises to improve my recon skills.

Important:
- Only recommend actions allowed by the program policy.
- Do not suggest scanning, brute-forcing, or testing out-of-scope assets.
- Ask me to paste the program scope and rules before giving a detailed plan.
```

