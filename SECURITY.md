# Security

## Scope
- This repository aims to encourage safe defaults.
- It does not guarantee secure operation.

## Security Posture
- Prefer file-based transparency over hidden automation.
- Prefer explicit confirmation over silent external action.
- Prefer minimal sensitive-data handling over convenience.

## Recommended Usage
- Keep secrets outside the repository.
- Require explicit confirmation before risky external actions.
- Treat health, finance, work, and private communications as sensitive by default.
- Keep public framework files separate from private runtime data.
- Review local tool permissions before connecting external systems.

## Out of Scope for V1
- Built-in email automation
- Built-in calendar automation
- Tool-specific runtime launchers
- Secret management implementations

## Reporting
- If you discover a security issue in the public framework, disclose it responsibly through the repository's issue or security process once published.
