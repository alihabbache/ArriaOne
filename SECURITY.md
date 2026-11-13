# Security Policy

## Scope

This is a **concept prototype** (ArriaOne). It is a static, single-file HTML/JavaScript application with no backend, no database, no authentication, and no real user data.

## What to report

Despite being a prototype, please report:

- Hardcoded secrets or tokens inadvertently committed to this repository
- Malicious third-party resource injection (supply-chain issues)
- Dangerous JavaScript patterns (XSS vectors, prototype pollution, etc.)
- Exposed personal data or PII in source code or commit history

## What is intentional (not a vulnerability)

- All data in `index.html` is **fictional** and hardcoded for demonstration purposes
- No real credentials, keys, or tokens are present
- The app runs entirely client-side with no network calls except Google Fonts

## Reporting

Please open a **private security advisory** via GitHub:  
[github.com/alihabbache/ArriaOne/security/advisories/new](https://github.com/alihabbache/ArriaOne/security/advisories/new)

Do **not** open a public issue for security findings.

## Response time

This is a personal prototype repository. Expect a response within **7 days**.
