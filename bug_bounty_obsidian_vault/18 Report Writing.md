# Report Writing

A good bug bounty report is clear, reproducible, and focused on impact.

## Report structure

```text
Title
Severity
Affected asset
Vulnerability type
Summary
Impact
Steps to reproduce
Proof of concept
Evidence
Remediation
References
```

## Title examples

Bad:

```text
IDOR found
```

Good:

```text
Unauthorized access to other users’ invoices through object ID manipulation
```

## Summary

Explain the issue in one or two sentences.

Example:

```text
The invoice endpoint does not properly validate object ownership. 
An authenticated user can access another organization’s invoice by changing the invoice ID.
```

## Impact

Explain what an attacker can actually do.

Example:

```text
An attacker can view confidential invoices belonging to other organizations, 
including customer names, billing amounts, and payment details.
```

## Reproduction steps

Be specific:

1. Log in as User A.
2. Navigate to the invoices page.
3. Capture the request to `/api/invoices/1001`.
4. Send the request to Repeater.
5. Change the invoice ID to `1002`.
6. Observe that the response returns another organization’s invoice.

## Evidence

Include:

- Full HTTP request
- Full HTTP response
- Screenshots
- Short screen recording
- Relevant response fields
- Scope evidence

Do not include unrelated sensitive data.

## Remediation

Suggest a fix, such as:

```text
Enforce server-side object ownership checks before returning or modifying 
any invoice. Validate that the authenticated user belongs to the same 
organization as the requested invoice.
```

## Severity

Consider:

- Confidentiality
- Integrity
- Availability
- Number of affected users
- Ease of exploitation
- Authentication requirement
- Business impact

Do not inflate severity. A clear, honest report is more credible.

## Report quality checklist

- [ ] Clear title
- [ ] Correct severity
- [ ] Affected asset identified
- [ ] Reproduction steps complete
- [ ] Evidence included
- [ ] Business impact explained
- [ ] Remediation suggested
- [ ] No sensitive data exposed unnecessarily
- [ ] Submitted through official channel

