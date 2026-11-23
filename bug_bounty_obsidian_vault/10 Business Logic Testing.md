# Business Logic Testing

Business logic vulnerabilities occur when an application performs an action that should not be allowed, even though every individual technical control appears to work.

## Why business logic matters

Automated tools often miss business logic flaws because they do not understand the application’s intended rules.

Examples:

- A user buys an item for negative price.
- A user reuses a one-time coupon.
- A user skips a payment step.
- A user transfers money twice using a race condition.
- A user changes their email and takes over another account.
- A user bypasses an approval workflow.

## How to find logic bugs

For every workflow, create a model:

```text
Normal workflow:
1. User adds item to cart
2. User applies coupon
3. User pays
4. Order is created
5. Confirmation email is sent
```

Then ask:

- Can step 2 be repeated?
- Can step 3 be skipped?
- Can step 4 occur without payment?
- Can step 5 be triggered for another user?
- Can the order amount be changed after payment?
- Can the same coupon be used by multiple accounts?

## High-value workflows

### Account recovery

Test:

- Password reset
- Email change
- Phone change
- MFA recovery
- Backup codes
- Account linking

### Payments

Test:

- Price manipulation
- Negative values
- Zero values
- Currency confusion
- Discount stacking
- Coupon reuse
- Refund abuse
- Subscription downgrade abuse
- Race conditions

### Invitations and referrals

Test:

- Self-invitation
- Duplicate invitations
- Invitation reuse
- Referral self-abuse
- Reward farming
- Organization joining abuse

### File and document access

Test:

- Accessing another user’s files
- Sharing links
- Download permissions
- File deletion
- File replacement
- Access after role change

## Race conditions

A race condition occurs when two or more requests execute in a way the application did not expect.

Examples:

- Redeeming one coupon multiple times
- Withdrawing money multiple times
- Claiming a reward multiple times
- Using one-time tokens multiple times

Only test race conditions when explicitly allowed and with extreme care. Avoid causing financial loss, service disruption, or data corruption.

## Workflow bypass

Ask:

- Can a required step be skipped?
- Can steps be performed in the wrong order?
- Can a request be replayed?
- Can a token be reused?
- Can client-side validation be bypassed?
- Can a hidden state be reached directly?

## Business logic checklist

- [ ] Account recovery tested
- [ ] Payment workflow tested
- [ ] Coupon and discount logic tested
- [ ] Referral logic tested
- [ ] Invitation logic tested
- [ ] File access logic tested
- [ ] Workflow order tested
- [ ] Token reuse tested
- [ ] Race conditions considered
- [ ] Role-change behavior tested

