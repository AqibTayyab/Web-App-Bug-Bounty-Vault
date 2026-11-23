# Master Testing Checklist

Use this checklist for every authorized target.

## 1. Preparation

- [ ] Read the bug bounty policy
- [ ] Confirm in-scope domains and applications
- [ ] Confirm out-of-scope assets
- [ ] Confirm allowed testing methods
- [ ] Confirm reporting channel
- [ ] Confirm disclosure rules
- [ ] Create dedicated test accounts
- [ ] Set up Burp Suite and browser proxy
- [ ] Create a target folder
- [ ] Start a testing log

## 2. Reconnaissance

- [ ] Identify main domain and related domains
- [ ] Enumerate subdomains
- [ ] Resolve live hosts
- [ ] Identify IP addresses and hosting providers
- [ ] Identify CDN and WAF usage
- [ ] Review DNS records
- [ ] Check certificate transparency data
- [ ] Identify technologies and frameworks
- [ ] Discover JavaScript files
- [ ] Extract API endpoints from JavaScript
- [ ] Identify open API documentation
- [ ] Identify cloud storage exposure
- [ ] Identify third-party integrations
- [ ] Identify mobile API endpoints if in scope

## 3. Application mapping

- [ ] Create accounts for each available role
- [ ] Map registration and login flows
- [ ] Map password reset and account recovery
- [ ] Map user profile and settings
- [ ] Map all major features
- [ ] Identify admin panels
- [ ] Identify roles and permissions
- [ ] Identify sensitive objects
- [ ] Identify state-changing actions
- [ ] Identify file-upload features
- [ ] Identify payment or billing features
- [ ] Identify sharing and collaboration features
- [ ] Identify integrations and webhooks
- [ ] Identify AI/LLM features if present

## 4. Authentication

- [ ] Test registration validation
- [ ] Test username and email enumeration
- [ ] Test password policy enforcement
- [ ] Test login rate limits
- [ ] Test account lockout behavior
- [ ] Test password reset token handling
- [ ] Test email verification flows
- [ ] Test OTP implementation
- [ ] Test session creation
- [ ] Test session expiration
- [ ] Test logout behavior
- [ ] Test cookie security attributes
- [ ] Test MFA enforcement and bypass
- [ ] Test OAuth and SSO flows
- [ ] Test JWT validation and claims

## 5. Authorization

- [ ] Test horizontal access control
- [ ] Test vertical privilege escalation
- [ ] Test role-based access control
- [ ] Test object-level authorization
- [ ] Test function-level authorization
- [ ] Test multi-tenant isolation
- [ ] Test organization and team boundaries
- [ ] Test admin functionality with normal user accounts
- [ ] Test API endpoints directly
- [ ] Test hidden UI functionality
- [ ] Test parameter manipulation
- [ ] Test predictable identifiers
- [ ] Test access to other users’ files
- [ ] Test access to other users’ settings
- [ ] Test access to other users’ transactions

## 6. Input validation

- [ ] Test reflected XSS
- [ ] Test stored XSS
- [ ] Test DOM-based XSS
- [ ] Test SQL injection
- [ ] Test command injection
- [ ] Test template injection
- [ ] Test NoSQL injection where relevant
- [ ] Test SSRF
- [ ] Test file upload
- [ ] Test path traversal
- [ ] Test open redirects
- [ ] Test CSV injection where relevant
- [ ] Test HTML injection
- [ ] Test parameter pollution
- [ ] Test type confusion

## 7. Business logic

- [ ] Test negative quantities and prices
- [ ] Test zero-value transactions
- [ ] Test currency confusion
- [ ] Test discount abuse
- [ ] Test coupon reuse
- [ ] Test race conditions
- [ ] Test workflow skipping
- [ ] Test request replay
- [ ] Test one-time token reuse
- [ ] Test invitation abuse
- [ ] Test referral abuse
- [ ] Test refund abuse
- [ ] Test account recovery abuse
- [ ] Test email-change account takeover
- [ ] Test phone-change account takeover

## 8. API testing

- [ ] Enumerate API versions
- [ ] Test undocumented endpoints
- [ ] Test BOLA
- [ ] Test BFLA
- [ ] Test mass assignment
- [ ] Test excessive data exposure
- [ ] Test rate limiting
- [ ] Test pagination abuse
- [ ] Test GraphQL introspection
- [ ] Test GraphQL authorization
- [ ] Test GraphQL batching
- [ ] Test WebSocket authorization
- [ ] Test webhook security

## 9. Configuration

- [ ] Check security headers
- [ ] Check CSP
- [ ] Check HSTS
- [ ] Check cookie flags
- [ ] Check CORS configuration
- [ ] Check TLS configuration
- [ ] Check exposed admin panels
- [ ] Check debug endpoints
- [ ] Check source maps
- [ ] Check Swagger/OpenAPI documentation
- [ ] Check GraphQL introspection
- [ ] Check backup files
- [ ] Check `.env` exposure
- [ ] Check `.git` exposure
- [ ] Check subdomain takeover

## 10. LLM/GenAI testing

Only perform if explicitly authorized.

- [ ] Identify AI features
- [ ] Identify model inputs
- [ ] Identify model outputs
- [ ] Identify connected tools
- [ ] Identify RAG data sources
- [ ] Test direct prompt injection
- [ ] Test indirect prompt injection
- [ ] Test insecure output handling
- [ ] Test sensitive data disclosure
- [ ] Test excessive agency
- [ ] Test tool permission boundaries
- [ ] Test resource consumption
- [ ] Test cross-user data leakage

## 11. Reporting

- [ ] Confirm the issue is reproducible
- [ ] Confirm the asset is in scope
- [ ] Confirm the issue is not a duplicate
- [ ] Capture request and response evidence
- [ ] Capture screenshots or video
- [ ] Explain business impact
- [ ] Suggest remediation
- [ ] Submit through the official channel
- [ ] Do not disclose publicly without permission

