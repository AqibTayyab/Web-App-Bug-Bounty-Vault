# Getting Started

## Your goal

Your goal is not to find hundreds of random bugs. Your goal is to become a **methodical web application security tester** who can:

- Understand an application.
- Map its attack surface.
- Identify high-impact vulnerabilities.
- Validate findings safely.
- Communicate impact clearly.
- Follow program rules.

## What you need to learn

You do not need to memorize every exploit. You need to understand these foundations:

### 1. How the web works

Learn:

- HTTP and HTTPS
- Requests and responses
- Methods: GET, POST, PUT, PATCH, DELETE
- Headers, cookies, parameters, and body formats
- Status codes
- Sessions and authentication
- Same-Origin Policy
- CORS
- Cookies, localStorage, and sessionStorage
- JavaScript and the DOM
- JSON and REST APIs

### 2. How applications are built

Learn the basic architecture:

```text
Browser / Mobile App
        |
     Frontend
        |
       API
        |
   Backend logic
        |
Database / Cloud / Third-party services
```

Most modern bugs happen where one layer trusts another layer too much.

### 3. Security thinking

Always ask:

- Who can access this feature?
- What data can they access?
- What actions can they perform?
- Can a user access another user’s data?
- Can a low-privileged user perform an admin action?
- Can a workflow be skipped, reversed, or repeated?
- Is input validated on the server, not only in the browser?
- Is sensitive data exposed in responses, logs, URLs, or files?

## Minimum tool setup

Install and learn:

- Kali Linux, Parrot OS, or a Linux virtual machine
- Burp Suite Community or Professional
- Firefox with FoxyProxy
- A password manager
- A note-taking system, preferably Obsidian
- A dedicated bug bounty folder for evidence and reports

Do not begin with expensive paid courses. Start with free, structured practice:

- PortSwigger Web Security Academy
- OWASP Juice Shop
- DVWA
- TryHackMe
- HackTheBox
- PicoCTF

## Daily practice routine

Spend at least 60–90 minutes daily:

- 30 minutes: learn one concept
- 30 minutes: practice labs
- 15 minutes: write notes
- 15 minutes: review previous notes

## Beginner mistakes

- Testing random websites without permission
- Running aggressive scanners on production systems
- Reporting missing security headers as critical bugs
- Reporting theoretical issues without impact
- Copying payloads without understanding them
- Ignoring business logic
- Not reading the program policy
- Giving up after one week

## Success rule

Learn one vulnerability deeply, practice it, document it, then move to the next one.

