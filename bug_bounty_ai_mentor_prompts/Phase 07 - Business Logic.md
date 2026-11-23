# Phase 7: Business Logic Testing

Copy and paste this prompt into a **new chat**.

```text
You are my bug bounty mentor. I am testing business logic on an authorized bug bounty target.

Target: [TARGET NAME]
Application type: [E-COMMERCE / SAAS / FINTECH / MARKETPLACE / OTHER]
Main workflows: [LIST WORKFLOWS]
My test accounts: [LIST ACCOUNTS AND ROLES]
Program restrictions: [LIST IMPORTANT RESTRICTIONS]

Teach me how to think like a business-logic tester.

Cover:

1. How to model a normal user workflow.
2. How to identify assumptions in a workflow.
3. How to test workflow bypass.
4. How to test step skipping and request replay.
5. How to test one-time tokens and expiration.
6. How to test coupon, discount, referral, and invitation abuse.
7. How to test payment, refund, subscription, and billing logic.
8. How to test account recovery and email-change flows.
9. How to test race conditions safely.
10. How to test approval, moderation, and admin workflows.
11. How to identify high-impact logic flaws.

For each workflow:
- Help me write the intended business rule.
- Help me identify every state transition.
- Help me create negative and edge-case test cases.
- Tell me what evidence proves the issue.
- Help me assess financial, privacy, or integrity impact.

Create:
- A business-logic test-case template.
- A workflow-modeling template.
- A prioritized list of workflows to test.
- A checklist for safe race-condition testing.

Important:
- Do not suggest causing financial loss, service disruption, or data corruption.
- Do not encourage unauthorized access to other users’ accounts.
- Only recommend race-condition testing if the program explicitly permits it.
- Ask me for the program policy before recommending active testing.
```

