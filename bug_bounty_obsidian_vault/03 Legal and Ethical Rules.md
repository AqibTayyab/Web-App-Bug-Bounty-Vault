# Legal and Ethical Rules

## Non-negotiable rule

**Never test a system without authorization.**

A website being public does not mean you are allowed to test it. Always use:

- Official bug bounty programs
- Vulnerability disclosure programs
- Your own lab or systems
- Systems where you have explicit written permission

## Read the program policy

Before testing, read:

- Scope
- Out-of-scope assets
- Allowed testing methods
- Prohibited testing methods
- Reporting rules
- Disclosure rules
- Safe-harbor terms
- Reward criteria
- Contact method

HackerOne states that assets outside a program’s control are generally not authorized for testing, and Bugcrowd documentation emphasizes official communication channels and disclosure policies. [web:16][web:20]

## Scope discipline

Only test assets explicitly listed as in scope.

Examples:

- If `api.example.com` is in scope but `dev.example.com` is not, do not test `dev.example.com`.
- If a program allows only `*.example.com`, confirm the wildcard rules carefully.
- If mobile apps are out of scope, do not test them.
- If third-party services are out of scope, do not test them.

## What is usually prohibited

Many programs prohibit:

- Denial-of-service attacks
- Spamming
- Social engineering
- Phishing
- Physical attacks
- Testing other users’ accounts without permission
- Accessing, downloading, or exposing real customer data
- Destructive testing
- Automated scanning at high volume
- Testing third-party services
- Public disclosure without permission

## Data handling

If you accidentally access sensitive data:

- Stop immediately.
- Do not download, copy, share, or publish it.
- Take only the minimum evidence needed to prove the issue.
- Report it promptly through the authorized channel.
- Follow the program’s incident-response instructions.

## Legal awareness: know, but do not do

You should understand that attackers may attempt:

- Unauthorized access
- Credential stuffing
- Data theft
- Phishing
- Malware distribution
- Dark-web data trading
- Extortion
- Infrastructure abuse

Knowing that these activities exist helps you understand attacker behavior, but you must not perform them. Your role is to improve security through authorized testing and responsible disclosure.

## Ethical mindset

Ask yourself:

- Would the program owner approve this action?
- Could this action harm real users?
- Am I accessing data I should not access?
- Am I causing disruption?
- Am I following the written rules?
- Can I explain every action I took?

If the answer is uncertain, stop and ask the program through its official support channel.

## Safe harbor

Safe harbor does not automatically protect you from every action. It usually applies only when you:

- Stay within scope
- Follow the program rules
- Avoid privacy violations
- Avoid service disruption
- Use authorized communication channels
- Report responsibly

Bugcrowd’s documentation describes safe harbor and disclosure expectations; read the exact policy for every program. [web:20][web:23]

## Personal testing log

Maintain a log containing:

- Date and time
- Target and scope
- Actions performed
- Tools used
- Findings
- Evidence location
- Reports submitted
- Program responses

This protects you and improves your learning.

