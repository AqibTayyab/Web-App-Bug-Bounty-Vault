# 12-Month Roadmap

This roadmap assumes 1–2 hours of focused study per day. Adjust the pace to your available time.

## Month 1: Web fundamentals

### Learn

- HTTP methods, headers, cookies, status codes
- URL structure, encoding, and parameters
- Browser developer tools
- Same-Origin Policy
- CORS
- Sessions and cookies
- Basic JavaScript
- Linux command line
- Networking basics: DNS, IP, ports, proxies

### Practice

- Complete beginner PortSwigger labs
- Inspect requests in Burp Suite
- Build a simple personal notes system
- Practice reading HTTP requests and responses

### Outcome

You can explain what happens when a user logs in, submits a form, or calls an API.

## Month 2: Core vulnerabilities

### Learn

- Broken access control
- IDOR
- Authentication flaws
- Session management
- Privilege escalation
- Information disclosure
- Security misconfiguration

### Practice

- IDOR labs
- Authentication labs
- Access control labs
- Session management labs

### Outcome

You can identify and demonstrate access-control and authentication issues in a lab.

## Month 3: Injection and client-side issues

### Learn

- SQL injection
- Command injection
- Template injection
- XSS: reflected, stored, DOM-based
- CSRF
- Clickjacking
- Open redirects
- SSRF

### Practice

- SQL injection labs
- XSS labs
- CSRF labs
- SSRF labs

### Outcome

You understand where user input becomes dangerous and how to test safely.

## Month 4: APIs and authentication

### Learn

- REST APIs
- JSON
- BOLA
- BFLA
- Mass assignment
- Excessive data exposure
- OAuth 2.0
- OpenID Connect
- JWT
- API keys
- Rate limiting

### Practice

- API testing labs
- OAuth labs
- JWT labs
- GraphQL basics

### Outcome

You can test API endpoints beyond the visible user interface.

## Month 5: Reconnaissance

### Learn

- Passive reconnaissance
- Active reconnaissance
- Subdomain enumeration
- DNS records
- Certificate transparency
- JavaScript analysis
- API endpoint discovery
- Technology fingerprinting
- Cloud asset discovery

### Practice

- Build a recon checklist
- Practice on intentionally vulnerable lab targets
- Create a target-mapping template

### Outcome

You can turn a scope into an organized target map.

## Month 6: Business logic

### Learn

- Workflow abuse
- Race conditions
- Coupon and discount abuse
- Payment logic
- Invitation abuse
- Account recovery abuse
- Multi-step process bypass
- Rate-limit bypass

### Practice

- Analyze real-world writeups
- Practice on vulnerable applications
- Create business-logic test cases

### Outcome

You can think like an attacker, not just like a scanner.

## Month 7: Cloud and infrastructure

### Learn

- S3, GCS, and Azure Blob exposure
- Cloud metadata risks
- IAM basics
- Secrets exposure
- Subdomain takeover
- CI/CD exposure
- Dependency and supply-chain risks

### Practice

- Identify misconfigurations in lab environments
- Review exposed JavaScript files
- Practice secure configuration review

### Outcome

You can identify common infrastructure and configuration weaknesses.

## Month 8: LLM and GenAI security

### Learn

- Prompt injection
- Insecure output handling
- Excessive agency
- Sensitive data disclosure
- RAG security
- Agent and tool security
- Model supply-chain risks

### Practice

- Test intentionally vulnerable AI applications
- Map AI inputs and outputs
- Create an AI testing checklist

### Outcome

You can assess AI-powered features responsibly.

## Month 9: First real bug bounty target

### Do

- Select a public program with clear scope
- Read the policy twice
- Create test accounts
- Map the application
- Follow the master checklist
- Spend time on high-value features

### Goal

Complete one full testing cycle, even if you do not find a bounty-worthy bug.

## Month 10: Reporting and severity

### Learn

- Impact-first reporting
- Reproduction steps
- Evidence collection
- CVSS basics
- Severity justification
- Remediation recommendations

### Outcome

You can write a report that a triager can understand and reproduce.

## Month 11: Specialization

Choose one focus area:

- API security
- Mobile backend testing
- Cloud security
- JavaScript analysis
- GraphQL
- LLM/GenAI security
- OAuth and SSO

## Month 12: Consistency

### Do

- Test 3–5 targets
- Review all notes
- Improve your methodology
- Read quality disclosed reports
- Build a personal checklist library

## Long-term path: 2026–2030+

Technology will change, but these skills remain valuable:

- Understanding authorization
- Understanding trust boundaries
- Understanding business logic
- Understanding APIs
- Understanding identity
- Understanding cloud architecture
- Understanding AI integration risks

