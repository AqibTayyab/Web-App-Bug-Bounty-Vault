# API and GraphQL Testing

Modern web applications rely heavily on APIs. The browser interface may hide functionality, but the API remains accessible.

## API testing mindset

For every API endpoint, ask:

- Who can call it?
- What object does it access?
- What action does it perform?
- What parameters does it accept?
- What data does it return?
- Is authorization enforced on the server?

## REST API testing

### Identify endpoints

Look for:

- `/api/`
- `/v1/`
- `/v2/`
- `/graphql`
- `/internal/`
- `/admin/`
- `/debug/`
- `/swagger`
- `/openapi.json`
- `/docs`

### Test BOLA

BOLA means **Broken Object Level Authorization**.

Example:

```text
GET /api/orders/12345
```

Change the object identifier and check whether another user’s object is returned.

### Test BFLA

BFLA means **Broken Function Level Authorization**.

Example:

```text
POST /api/admin/users/delete
```

Test whether a normal user can call an administrative function directly.

### Test mass assignment

Mass assignment occurs when an API accepts unexpected fields and applies them to an object.

Examples of fields to consider:

- `role`
- `is_admin`
- `verified`
- `active`
- `owner_id`
- `organization_id`
- `price`
- `permissions`

Only test fields that are safe, authorized, and non-destructive.

### Test excessive data exposure

Review API responses for:

- Password hashes
- API tokens
- Internal IDs
- Other users’ data
- Debug information
- Stack traces
- Configuration values
- Secrets

## GraphQL testing

GraphQL can expose a large attack surface because clients can request specific fields.

### Check

- Introspection enabled
- Field suggestions
- Authorization on individual fields
- Authorization on individual resolvers
- Batched queries
- Query depth limits
- Alias abuse
- Error messages
- Object-level authorization

## WebSocket testing

WebSockets maintain a persistent connection and may bypass normal HTTP request controls.

Check:

- Authentication during handshake
- Authorization for messages
- Cross-user message access
- Reconnection behavior
- Rate limiting
- Origin validation

## API checklist

- [ ] API documentation reviewed
- [ ] API versions identified
- [ ] BOLA tested
- [ ] BFLA tested
- [ ] Mass assignment tested
- [ ] Excessive data exposure tested
- [ ] Rate limits tested
- [ ] GraphQL authorization tested
- [ ] GraphQL introspection reviewed
- [ ] WebSocket authorization tested
- [ ] Webhook security reviewed

