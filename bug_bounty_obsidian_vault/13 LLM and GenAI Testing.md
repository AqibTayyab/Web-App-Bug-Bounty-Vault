# LLM and GenAI Testing

AI-powered applications introduce new security risks. OWASP’s Top 10 for LLM Applications 2025 focuses on risks specific to LLM-based systems, including insecure output handling and unbounded consumption. [web:3]

## First rule

Do not test AI features unless the bug bounty program explicitly includes them in scope.

Read the program’s AI-specific rules carefully. Some programs prohibit model abuse, jailbreak testing, or automated red-teaming.

## Map the AI feature

Identify:

- What the AI feature does
- What user input reaches the model
- What data the model can access
- What tools the model can use
- What actions the model can perform
- What output is shown to users
- Whether output is rendered as HTML or markdown

## Prompt injection

Prompt injection occurs when attacker-controlled input changes the behavior of an AI system.

### Direct prompt injection

The user directly provides malicious instructions in a prompt.

### Indirect prompt injection

Malicious instructions are hidden in content the AI processes, such as:

- Uploaded documents
- Web pages
- Emails
- Database records
- Support tickets
- File names
- User-generated content

### Testing mindset

Ask:

- Can untrusted content change model behavior?
- Can the model reveal system instructions?
- Can the model access unauthorized data?
- Can the model trigger an unintended action?
- Can the model bypass role restrictions?

## Insecure output handling

OWASP highlights that improper output handling can lead to browser-based XSS or CSRF, and backend issues such as SSRF, privilege escalation, or remote code execution. [web:3]

Ask:

- Is model output rendered as HTML?
- Is markdown converted into HTML?
- Are links automatically clickable?
- Are images loaded from model output?
- Is output inserted into the DOM?
- Is output passed to another system?

## Excessive agency

Excessive agency occurs when an AI system can perform actions beyond what the user intended or should be allowed to do.

Examples:

- Sending emails
- Deleting files
- Making purchases
- Accessing databases
- Calling internal APIs
- Modifying user settings
- Executing code

Ask:

- What tools can the model use?
- Who authorizes each action?
- Are actions reversible?
- Are high-impact actions confirmed by the user?
- Are permissions enforced outside the model?

## Sensitive data disclosure

Test whether the AI system can disclose:

- Other users’ data
- Internal documentation
- API keys
- System prompts
- Database records
- Confidential company information
- Previous conversation data

## RAG security

Retrieval-Augmented Generation systems retrieve information from documents or databases.

Test:

- Cross-tenant retrieval
- Unauthorized document access
- Document poisoning
- Indirect prompt injection
- Data leakage through answers
- Access-control enforcement

## AI testing checklist

- [ ] AI feature identified
- [ ] Model inputs mapped
- [ ] Model outputs mapped
- [ ] Tools and plugins identified
- [ ] RAG sources identified
- [ ] Direct prompt injection tested
- [ ] Indirect prompt injection tested
- [ ] Output handling tested
- [ ] Sensitive data disclosure tested
- [ ] Excessive agency tested
- [ ] Cross-user leakage tested
- [ ] Resource consumption reviewed

