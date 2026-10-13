# Security Policy

ResolveOS handles personal documents, so security reports are taken seriously.

## Reporting a vulnerability

Please do **not** open a public issue. Instead, use GitHub's private reporting:
**Security tab > Report a vulnerability**.

Include what you found, how to reproduce it, and the potential impact. You can expect an initial response within 7 days.

## Scope

In scope: authentication, authorisation (one user accessing another user's data), file upload and storage, injection, and data exposure.

## Our commitments

- Uploaded files are stored privately and served through short-lived links.
- Uploaded documents are treated as untrusted input.
- Secrets are never stored in the repository.