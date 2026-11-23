# Reconnaissance

Reconnaissance means understanding the target before testing it. OWASP’s Web Security Testing Guide emphasizes identifying the applications, hosts, endpoints, and technologies that make up the attack surface before assessing authentication, authorization, or business logic. [web:24]

## Objective

Answer these questions:

- What assets exist?
- Which assets are authorized for testing?
- What technologies are used?
- What APIs and endpoints exist?
- What user roles exist?
- What sensitive data and actions exist?
- Where are the trust boundaries?

## Types of reconnaissance

### Passive reconnaissance

Passive reconnaissance uses publicly available information without directly interacting aggressively with the target.

Examples:

- Search engine results
- Certificate transparency logs
- DNS records
- Public code repositories
- Public documentation
- Archived pages
- Job postings
- Public API documentation

### Active reconnaissance

Active reconnaissance interacts with the target to identify live services and endpoints.

Examples:

- DNS resolution
- HTTP requests
- Subdomain enumeration
- Port scanning within authorized scope
- Directory and endpoint discovery
- Technology fingerprinting

Always follow the program’s rules on scanning, rate limits, and prohibited methods.

## Recon workflow

### Step 1: Understand scope

Create a scope file:

```text
In scope:
- example.com
- *.example.com
- api.example.com
- Mobile application

Out of scope:
- third-party.example.com
- support.example.com
- DoS testing
- Social engineering
```

Never assume a domain is in scope because it looks related to the main company.

### Step 2: Identify domains

Collect:

- Root domain
- Subdomains
- Wildcard domains
- Acquisition domains
- Regional domains
- API domains
- CDN domains
- Mail domains

### Step 3: Identify live assets

For each discovered domain:

- Resolve DNS
- Check whether the host responds
- Identify HTTP/HTTPS services
- Identify redirects
- Identify technologies
- Identify certificates
- Identify cloud hosting

### Step 4: Discover JavaScript and APIs

Modern applications often expose useful information in JavaScript.

Look for:

- API base URLs
- Endpoint paths
- GraphQL endpoints
- WebSocket endpoints
- Configuration values
- Feature flags
- Third-party keys
- Source maps
- Hidden routes
- Role-based UI logic

### Step 5: Map users and features

Create a simple map:

```text
Public user
- Register
- Login
- Browse products
- Purchase

Authenticated user
- Profile
- Orders
- Uploads
- Support tickets

Admin
- User management
- Reports
- Settings
```

### Step 6: Identify high-value areas

Prioritize:

- Authentication
- Password reset
- Account settings
- Admin panels
- Payment flows
- File uploads
- API endpoints
- Sharing features
- Invitation systems
- Organization switching
- AI features
- Integrations

## Recon checklist

- [ ] Scope documented
- [ ] Domains collected
- [ ] Subdomains enumerated
- [ ] Live hosts identified
- [ ] Technologies identified
- [ ] JavaScript files collected
- [ ] API endpoints extracted
- [ ] Cloud assets checked
- [ ] Public documentation reviewed
- [ ] User roles identified
- [ ] Features mapped
- [ ] High-value areas prioritized

## Important warning

Do not treat every finding from recon as a vulnerability. A subdomain, open port, or exposed JavaScript file is only interesting if it leads to a real security impact within scope.

