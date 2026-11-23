# OWASP LLM Top 10:2025

OWASP’s Top 10 for LLM Applications 2025 addresses security risks specific to AI-powered applications. [web:3]

## Why it matters

Many applications now include:

- Chatbots
- AI search
- Document question answering
- AI-generated content
- AI agents
- AI-powered automation
- RAG systems
- AI coding assistants

These features create new attack surfaces.

## Key risk areas

| Risk area | What it means | What to check |
|---|---|---|
| Prompt injection | Untrusted input changes model behavior | Direct and indirect injection |
| Sensitive information disclosure | Model reveals confidential data | System prompts, user data, internal documents |
| Supply chain | Model, plugin, or dependency compromise | Model source, plugins, packages |
| Data and model poisoning | Malicious data affects model behavior | Training data, RAG documents, feedback |
| Improper output handling | Model output is treated as trusted | HTML, JavaScript, URLs, commands |
| Excessive agency | Model performs unintended actions | Tools, permissions, automation |
| System prompt leakage | Internal instructions are exposed | Prompt disclosure, configuration exposure |
| Vector and embedding weaknesses | Retrieval systems leak or mix data | RAG access control, tenant isolation |
| Misinformation | Model provides false or harmful output | Accuracy, safety, hallucination |
| Unbounded consumption | Model usage creates excessive cost or load | Rate limits, quotas, cost controls |

## Testing approach

### Step 1: Identify the AI feature

Examples:

- Support chatbot
- Document summarizer
- AI search
- Code assistant
- Email assistant
- AI agent

### Step 2: Identify inputs

Ask:

- What does the user type?
- What files are uploaded?
- What URLs are processed?
- What emails are read?
- What database records are retrieved?
- What third-party content is ingested?

### Step 3: Identify outputs

Ask:

- Is output displayed as plain text?
- Is output rendered as markdown?
- Is output converted to HTML?
- Is output used in an email?
- Is output passed to another system?
- Can output trigger an action?

### Step 4: Identify agency

Ask:

- Can the model browse the web?
- Can it access files?
- Can it send messages?
- Can it modify data?
- Can it call APIs?
- Can it execute code?

## Responsible testing

- Use only authorized targets.
- Do not attempt to extract real customer data.
- Do not cause excessive cost or load.
- Do not test third-party model providers outside scope.
- Report impact clearly and responsibly.

