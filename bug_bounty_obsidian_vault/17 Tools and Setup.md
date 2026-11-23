# Tools and Setup

## Operating system

Use one of the following:

- Kali Linux
- Parrot OS
- Ubuntu with security tools
- Windows with WSL2
- macOS with a Linux VM

Use a dedicated environment for security testing.

## Browser and proxy

### Burp Suite

Burp Suite is the main tool for intercepting and modifying web traffic.

Learn:

- Proxy
- Repeater
- Intruder
- Decoder
- Comparer
- Scanner, if available
- Extensions

### Firefox

Use Firefox with:

- FoxyProxy
- Developer tools
- Cookie editor
- JSON viewer

## Reconnaissance tools

Use tools only within authorized scope.

- `amass`
- `subfinder`
- `httpx`
- `nuclei`
- `ffuf`
- `gau`
- `waybackurls`
- `katana`
- `nmap`
- `dnsrecon`

## JavaScript analysis

Look for:

- API endpoints
- Hidden routes
- API keys
- Source maps
- Configuration values
- Role-based logic
- Third-party integrations

## Note-taking

Use Obsidian with folders such as:

```text
Bug Bounty/
├── Programs/
├── Targets/
├── Recon/
├── Findings/
├── Reports/
├── Learnings/
└── Templates/
```

## Evidence storage

Keep:

- Screenshots
- HTTP request/response evidence
- Tool output
- Video recordings
- Scope screenshots
- Report drafts

## Tool safety

- Do not run aggressive scans without permission.
- Do not test out-of-scope assets.
- Do not use tools that create excessive traffic.
- Do not store sensitive customer data unnecessarily.
- Do not share credentials, tokens, or private data.

