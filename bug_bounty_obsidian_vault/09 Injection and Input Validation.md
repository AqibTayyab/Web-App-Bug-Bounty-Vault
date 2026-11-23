# Injection and Input Validation

Injection occurs when untrusted input is interpreted as code, command, query, template, or markup.

The key principle is: **never trust client-side validation alone.**

## SQL injection

SQL injection occurs when user input changes the structure of a database query.

### Where to test

- Login forms
- Search fields
- Filters
- Sorting parameters
- API parameters
- JSON fields
- HTTP headers
- Cookies
- Export features
- Reporting features

### Testing mindset

Ask:

- Does the application build SQL queries using user input?
- Does it use parameterized queries?
- Are database errors exposed?
- Can input alter query logic?

Do not run destructive database commands. Use safe, minimal proof-of-concept methods and follow program rules.

## Command injection

Command injection occurs when user input is passed into an operating-system command.

### Common areas

- File conversion
- PDF generation
- Image processing
- Import/export
- Ping or network tools
- Document processing
- Server-side scripts

### Testing mindset

Ask:

- Does the application pass user-controlled filenames or parameters to a shell command?
- Are filenames sanitized?
- Are allowed file types enforced on the server?
- Are commands executed with least privilege?

## XSS

Cross-site scripting occurs when attacker-controlled input is executed in another user’s browser.

### Types

- Reflected XSS
- Stored XSS
- DOM-based XSS

### Where to test

- Search fields
- Comments
- Profiles
- File names
- Email templates
- Markdown editors
- Chat messages
- Support tickets
- URL parameters
- JSON responses rendered by JavaScript

### Testing mindset

Identify the output context:

- HTML body
- Attribute
- JavaScript string
- URL
- CSS
- Markdown
- JSON

A payload that works in one context may not work in another.

## CSRF

CSRF forces an authenticated user’s browser to send an unwanted state-changing request.

### Test areas

- Email change
- Password change
- Profile update
- Fund transfer
- Invitation acceptance
- Role change
- API-key creation
- Account deletion

### Testing mindset

Ask:

- Does the endpoint require a CSRF token?
- Is the token validated server-side?
- Are cookies restricted with `SameSite`?
- Can the action be performed cross-origin?

## SSRF

Server-Side Request Forgery occurs when an application makes a request to a user-controlled URL.

### Common areas

- URL preview
- Webhook configuration
- File import
- PDF generation
- Image fetching
- Integration setup
- Export features

### Testing mindset

Ask:

- Can the server access internal services?
- Can it access cloud metadata services?
- Can it access private IP ranges?
- Are redirects followed?
- Are DNS rebinding protections present?

Only test SSRF within the program’s authorized rules.

## File upload

File upload can be dangerous when the server trusts user-controlled filenames, content, or metadata.

### Test areas

- File extension validation
- Content-type validation
- File-size limits
- File storage location
- Filename handling
- Path traversal
- SVG rendering
- Image processing
- ZIP extraction
- Malicious file scanning

### Testing mindset

Ask:

- Where is the file stored?
- Can the file be accessed directly?
- Is the file served with a safe content type?
- Is execution prevented?
- Are filenames sanitized?
- Can a user access another user’s uploaded file?

## Input validation checklist

- [ ] SQL injection tested
- [ ] Command injection tested
- [ ] Template injection considered
- [ ] Reflected XSS tested
- [ ] Stored XSS tested
- [ ] DOM XSS tested
- [ ] CSRF tested
- [ ] SSRF tested
- [ ] File upload tested
- [ ] Path traversal tested
- [ ] Open redirects tested
- [ ] Server-side validation confirmed

