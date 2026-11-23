# Cloud and Infrastructure

Modern applications often depend on cloud services, third-party tools, CI/CD systems, and external integrations.

## Common areas

### Cloud storage

Check whether storage buckets or blobs are:

- Publicly accessible
- Misconfigured
- Listing files
- Allowing unauthorized writes
- Exposing sensitive documents
- Using predictable names

Only test cloud assets if they are explicitly in scope.

### Cloud metadata

Cloud metadata services can be dangerous if an application allows SSRF from a cloud-hosted server.

Do not attempt to exploit cloud metadata unless the program explicitly authorizes it and provides safe testing guidance.

### Secrets exposure

Look for exposed secrets in authorized areas:

- JavaScript bundles
- Source maps
- Public repositories
- Configuration files
- Error messages
- API responses
- CI/CD artifacts

If you find a secret, do not use it beyond the minimum necessary to prove impact, and follow the program’s reporting instructions.

### Subdomain takeover

Subdomain takeover may occur when a DNS record points to a service that is no longer claimed or configured.

Check:

- Dangling CNAME records
- Dangling cloud-service records
- Unclaimed third-party services
- DNS misconfiguration

Only verify takeover according to the program’s rules.

### CI/CD exposure

Check for:

- Exposed `.git` directories
- Public repository leakage
- Exposed build artifacts
- Leaked tokens
- Public pipeline logs
- Dependency confusion risks

## Supply chain

Modern applications depend on many third-party packages.

Ask:

- Are dependencies outdated?
- Are packages publicly known to be vulnerable?
- Are dependencies pinned?
- Is there an integrity verification process?
- Can a malicious dependency affect the application?

## Configuration checklist

- [ ] Cloud storage reviewed
- [ ] Public buckets checked
- [ ] Secrets exposure checked
- [ ] JavaScript files reviewed
- [ ] Source maps reviewed
- [ ] Subdomain takeover checked
- [ ] CI/CD exposure checked
- [ ] Dependency risks reviewed
- [ ] Security headers reviewed
- [ ] TLS configuration reviewed

