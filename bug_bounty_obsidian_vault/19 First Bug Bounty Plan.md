# First Bug Bounty Plan

This is a simple plan for your first authorized bug bounty target.

## Day 1: Choose a program

Select a public program with:

- Clear scope
- Clear policy
- Active triage
- Web application assets
- Reasonable reward table
- No confusing exclusions

Do not start with a highly competitive program if you are new. Start with a smaller, clearly scoped program.

## Day 2: Read the policy

Create a note with:

- In-scope domains
- Out-of-scope domains
- Allowed methods
- Prohibited methods
- Reporting rules
- Disclosure rules
- Reward criteria

## Day 3: Create accounts

Create:

- User A
- User B
- Premium user, if available
- Organization A
- Organization B
- Admin account, only if legally available through the application

## Day 4–5: Map the application

Document:

- Main features
- User roles
- Sensitive data
- API endpoints
- Admin functionality
- File-upload features
- Payment features
- Sharing features
- Integrations

## Day 6–7: Reconnaissance

Collect:

- Subdomains
- Live hosts
- JavaScript files
- API endpoints
- Technologies
- Cloud assets
- Public documentation

## Week 2: Authentication

Test:

- Registration
- Login
- Password reset
- Email change
- Session handling
- MFA
- OAuth
- JWT

## Week 3: Authorization

This is your highest-priority week.

Test:

- IDOR
- Privilege escalation
- Object-level authorization
- Function-level authorization
- Organization isolation
- File access
- Admin functionality

## Week 4: Business logic

Test:

- Payment workflows
- Coupons
- Referrals
- Invitations
- File sharing
- Account recovery
- Workflow bypass

## Week 5: APIs

Test:

- BOLA
- BFLA
- Mass assignment
- Excessive data exposure
- GraphQL
- Rate limits

## Week 6: Report and review

- Review all findings
- Remove false positives
- Write reports
- Submit valid findings
- Learn from triager feedback

## First-target mindset

Do not expect a bounty in your first week.

Your first goal is to complete a full methodology:

```text
Scope -> Recon -> Mapping -> Testing -> Reporting
```

If you follow this process consistently, your chances improve over time.

