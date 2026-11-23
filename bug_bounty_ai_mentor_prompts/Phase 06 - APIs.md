# Phase 6: API and GraphQL Testing

Copy and paste this prompt into a **new chat**.

```text
You are my bug bounty mentor. I am testing APIs for an authorized bug bounty target.

Target: [TARGET NAME]
In-scope API assets: [LIST]
API type: [REST / GRAPHQL / GRPC / WEBSOCKET / MIXED]
Authentication method: [SESSION / API KEY / JWT / OAUTH]
Available roles: [LIST]
Program restrictions: [LIST IMPORTANT RESTRICTIONS]

Teach me how to test APIs systematically.

Cover:

1. API discovery and endpoint enumeration.
2. API versioning and legacy endpoints.
3. REST API request structure.
4. BOLA: Broken Object Level Authorization.
5. BFLA: Broken Function Level Authorization.
6. Mass assignment.
7. Excessive data exposure.
8. Rate limiting and resource consumption.
9. Pagination abuse.
10. GraphQL introspection, authorization, batching, and field-level access.
11. WebSocket authentication and authorization.
12. Webhook security.
13. API documentation and OpenAPI/Swagger review.

For each vulnerability:
- Explain it in simple language.
- Explain the secure implementation.
- Give me a safe testing approach.
- Tell me what evidence to collect.
- Explain how to assess impact.
- Give me common mistakes and false positives.

Create:
- An API testing checklist.
- A BOLA testing matrix.
- A GraphQL testing checklist.
- A prioritized API testing plan.

Important:
- Only test APIs explicitly listed in scope.
- Do not access, modify, or delete data belonging to real users.
- Do not perform high-volume or disruptive testing.
- Ask me to share the program policy before giving active-testing instructions.
```

