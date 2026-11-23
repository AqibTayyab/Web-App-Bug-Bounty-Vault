# Authentication Testing

Authentication verifies **who** a user is. Authorization verifies **what** they are allowed to do.

A secure login system is not enough if password reset, email change, session handling, or MFA is weak.

## Test accounts

Create separate accounts:

- Account A: normal user
- Account B: normal user
- Account C: premium user, if available
- Account D: admin or moderator, if legally available
- Account E: organization/user from another tenant, if applicable

Never attempt to access another real person’s account.

## Registration

Check:

- Weak password acceptance
- Duplicate email handling
- Email verification bypass
- Username enumeration
- Phone-number enumeration
- Invitation-code abuse
- Mass assignment during registration
- Role manipulation during registration

## Login

Check:

- Username enumeration through different error messages or timing
- Brute-force protection
- Rate limiting
- Account lockout behavior
- CAPTCHA bypass
- Default credentials
- Credential stuffing protection
- Login redirect handling

## Password reset

This is one of the most valuable areas for account takeover.

Check:

- Token predictability
- Token reuse
- Token expiration
- Token binding to user and session
- Host-header manipulation
- Email parameter manipulation
- Response disclosure
- Reset link leakage
- Password change without proper verification
- Resetting another user’s password

## Email and phone change

Test whether changing an email or phone number can lead to account takeover.

Ask:

- Is the old email notified?
- Is verification required?
- Can the verification token be reused?
- Can the request be replayed?
- Can another user’s email be claimed?
- Can the process be bypassed?

## MFA and OTP

Check:

- OTP length and entropy
- OTP expiration
- OTP reuse
- OTP brute-force protection
- MFA bypass during password reset
- MFA bypass during account recovery
- Trusting device tokens
- Backup-code handling

## Sessions

Check:

- Session cookie flags: `Secure`, `HttpOnly`, `SameSite`
- Session fixation
- Session invalidation after password change
- Session invalidation after logout
- Concurrent session control
- Session expiration
- Session token predictability

## OAuth and SSO

OAuth is common in modern applications.

Check:

- Redirect URI validation
- State parameter validation
- Authorization-code reuse
- Token leakage in URLs or referrers
- Open redirect during OAuth flow
- Account linking abuse
- Pre-account takeover
- Insufficient email verification
- Token substitution

## JWT

Check:

- Signature verification
- Algorithm handling
- Expiration enforcement
- Audience and issuer validation
- Role claims
- Token revocation
- Sensitive data in JWT payload

## Authentication checklist

- [ ] Registration tested
- [ ] Login tested
- [ ] Password reset tested
- [ ] Email change tested
- [ ] Phone change tested
- [ ] OTP tested
- [ ] MFA tested
- [ ] Session handling tested
- [ ] OAuth tested
- [ ] SSO tested
- [ ] JWT tested

