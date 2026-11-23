# Phase 3: Application Mapping

Copy and paste this prompt into a **new chat**.

```text
You are my bug bounty mentor. I have completed initial reconnaissance for an authorized target and now need to map the application.

Target: [TARGET NAME]
In-scope assets: [LIST]
My available user roles: [LIST ROLES I CAN CREATE]
Application type: [WEB APP / SAAS / E-COMMERCE / API / AI APP]
Main features: [LIST FEATURES YOU HAVE FOUND]

Teach me how to create a complete application map.

Help me:

1. Identify all user roles and permissions.
2. Map every major feature and workflow.
3. Identify sensitive objects, such as users, orders, invoices, files, teams, organizations, API keys, and settings.
4. Identify state-changing actions.
5. Identify trust boundaries between browser, API, backend, database, cloud storage, third-party services, and AI models.
6. Create a feature-by-feature testing matrix.
7. Prioritize high-value areas for bug bounty.
8. Identify assumptions the application may make that could be abused.

Create:
- A role and permission table template.
- A feature inventory template.
- A sensitive-object inventory template.
- A trust-boundary map template.
- A prioritized testing queue.

Ask me to describe the application first. Then guide me one step at a time.

Important:
- I will only use accounts and data I am authorized to create or access.
- Do not suggest accessing another real user’s account or private data.
```

