# Authorization Testing

Authorization is often the most valuable bug bounty category.

Authentication answers: **Who are you?**

Authorization answers: **What are you allowed to do?**

OWASP’s Web Security Testing Guide includes dedicated sections for bypassing authorization schemas and privilege escalation. [web:29]

## Core question

For every request, ask:

> “Can this user perform this action on this object?”

## Horizontal access control

Horizontal access control determines whether one user can access another user’s data at the same privilege level.

Example:

```text
User A accesses:
GET /api/invoices/1001

User B changes ID:
GET /api/invoices/1002
```

If User B can view, modify, or delete User A’s invoice, that may be a serious access-control issue.

### Objects to test

- User profiles
- Orders
- Invoices
- Files
- Messages
- Documents
- Support tickets
- API keys
- Addresses
- Payment methods
- Organizations
- Projects
- Reports

## Vertical privilege escalation

Vertical privilege escalation occurs when a lower-privileged user can perform actions reserved for a higher-privileged role.

Example:

```text
Normal user calls:
POST /api/admin/users/delete
```

If the server accepts it, the application may have a privilege-escalation issue.

### Test areas

- Admin panels
- User management
- Role assignment
- System settings
- Billing controls
- Audit logs
- Internal APIs
- Debug endpoints
- Feature flags

## Function-level authorization

The frontend may hide admin buttons, but the backend must still enforce permissions.

Ask:

- Can I call the admin endpoint directly?
- Does the API validate the role?
- Does changing a parameter reveal hidden functionality?
- Does the mobile app expose additional endpoints?

## Object-level authorization

Object-level authorization checks whether a user can access a specific object.

Test by changing:

- User IDs
- Order IDs
- Invoice IDs
- File IDs
- UUIDs
- Slugs
- Emails
- Organization IDs
- Project IDs

## Multi-tenant isolation

In SaaS applications, tenant isolation is critical.

Test whether a user from Organization A can access:

- Organization B’s users
- Organization B’s projects
- Organization B’s invoices
- Organization B’s files
- Organization B’s settings
- Organization B’s API keys

## Business-role abuse

Test whether a user can:

- Invite themselves into a restricted organization
- Upgrade or downgrade their own role
- Assign themselves admin permissions
- Transfer ownership without authorization
- Access another organization’s resources
- Bypass approval workflows

## Authorization checklist

- [ ] Horizontal access control tested
- [ ] Vertical privilege escalation tested
- [ ] Object-level authorization tested
- [ ] Function-level authorization tested
- [ ] Multi-tenant isolation tested
- [ ] Role assignment tested
- [ ] Admin functionality tested
- [ ] API endpoints tested directly
- [ ] Hidden UI functionality tested
- [ ] File access tested
- [ ] Organization boundaries tested

