# Application Mapping

Application mapping means understanding how the application works before attacking it.

## Why mapping matters

Most high-impact bugs are found by understanding:

- User roles
- Permissions
- Data ownership
- Business workflows
- API behavior
- Trust boundaries

A scanner may find low-hanging issues, but a human tester finds logic and authorization flaws by understanding the application.

## Map the application

Create a table like this:

| Feature | Endpoint | Roles | Data | Security question |
|---|---|---|---|---|
| View profile | `/api/users/{id}` | User, Admin | Name, email, phone | Can User A view User B’s profile? |
| Update email | `/api/users/{id}/email` | User, Admin | Email | Can a user change another user’s email? |
| Create invoice | `/api/invoices` | User, Admin | Amount, customer | Can a user create an invoice for another organization? |
| Delete file | `/api/files/{id}` | Owner, Admin | File | Can a user delete another user’s file? |

## Identify roles

Common roles include:

- Anonymous user
- Free user
- Paid user
- Team member
- Manager
- Moderator
- Organization admin
- Super admin
- API client
- Support agent

For each role, record:

- What they can view
- What they can create
- What they can update
- What they can delete
- What they cannot access

## Identify sensitive objects

High-value objects include:

- User accounts
- Password reset tokens
- API keys
- Payment information
- Invoices
- Orders
- Documents
- Private messages
- Internal reports
- Organization settings
- Admin configurations

## Identify trust boundaries

A trust boundary is where one component trusts another.

Examples:

- Browser to API
- API to backend service
- Backend to database
- Application to cloud storage
- Application to third-party API
- User-generated content to AI model
- AI model output to browser

Ask: **Does this component properly verify identity, authorization, and input?**

## Feature-based testing

For every feature, ask:

1. What is the intended behavior?
2. Who is allowed to use it?
3. What data does it access?
4. What actions does it perform?
5. What happens with unexpected input?
6. What happens if a step is skipped?
7. What happens if a request is repeated?
8. What happens if roles are changed?

## Mapping checklist

- [ ] All major features identified
- [ ] User roles identified
- [ ] Permissions documented
- [ ] Sensitive objects listed
- [ ] State-changing actions listed
- [ ] API endpoints documented
- [ ] Trust boundaries identified
- [ ] High-value areas prioritized

