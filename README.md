# Web Application Bug Bounty Vault

A personal, Obsidian-ready knowledge base, cheat sheet collection, and AI-mentor prompt library for learning and practicing **authorized web application bug bounty hunting**.

This repository contains:

- A structured bug bounty learning roadmap
- A complete web application testing checklist
- Reconnaissance, mapping, authentication, authorization, API, business logic, cloud, and LLM/GenAI testing guides
- OWASP Web Top 10:2025 and OWASP LLM Top 10:2025 references
- Bug bounty cheat sheets
- Professional bug report templates
- AI mentor prompts divided into phases to avoid losing context in long chats
- Topic-specific learning prompts for use in new AI chats

## Important: Authorized Testing Only

This repository is for education and authorized security testing only.

Do **not** use this material to attack, access, disrupt, scan aggressively, or extract data from systems you do not own or are not explicitly authorized to test.

Always:

- Read the bug bounty program policy
- Stay within the defined scope
- Avoid denial-of-service, spam, social engineering, and destructive testing
- Protect sensitive data
- Report vulnerabilities through official channels
- Follow responsible disclosure rules

## Repository Structure

```text
2026 Bug Bounty Vault/
├── README.md
├── LICENSE
├── .gitignore
├── bug_bounty_obsidian_vault/
│   ├── 00 Home.md
│   ├── 01 Getting Started.md
│   ├── 02 12-Month Roadmap.md
│   ├── 03 Legal and Ethical Rules.md
│   ├── 04 Master Testing Checklist.md
│   ├── 05 Reconnaissance.md
│   ├── ...
│   └── 99 Templates/
├── bug_bounty_ai_mentor_prompts/
│   ├── 00 READ ME FIRST.md
│   ├── Phase 00 - Mentor Setup.md
│   ├── Phase 01 - Program Selection.md
│   ├── ...
│   └── 99 Quick Prompts.md
└── Bugbounty Cheatsheet/
    └── Bugbounty Cheatsheet/
        ├── Phase 1- HTTP Cheat Sheet.md
        ├── Phase 2- Reconnaissance Cheat Sheet.md
        └── Untitled 1.md
```

## How to Use in Obsidian

1. Download or clone this repository.
2. Open Obsidian.
3. Select **Open folder as vault**.
4. Choose the `bug_bounty_obsidian_vault` folder.
5. Copy the prompt and cheat-sheet folders into the same vault if you want everything in one place.

## Recommended Learning Order

1. Web fundamentals
2. Burp Suite
3. Linux and networking
4. Broken access control
5. Authentication
6. API security
7. Business logic
8. Input validation
9. SSRF and file upload
10. OAuth and SSO
11. GraphQL
12. Cloud security
13. LLM/GenAI security
14. Reconnaissance
15. Report writing
16. OWASP Top 10:2025
17. OWASP LLM Top 10:2025
18. JavaScript analysis
19. Bug bounty mindset

## References

- OWASP Top 10:2025: https://top10.owasp.org/2025/
- OWASP Top 10 for LLM Applications 2025: https://genai.owasp.org/resource/owasp-top-10-for-llm-applications-2025/
- OWASP Web Security Testing Guide: https://owasp.org/www-project-web-security-testing-guide/
- OWASP API Security Project: https://owasp.org/www-project-api-security/

## License

MIT License. See `LICENSE`.
