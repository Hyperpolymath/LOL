# Security Policy

## Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 0.1.x   | :white_check_mark: |

## Reporting a Vulnerability

**Please do not report security vulnerabilities through public GitHub issues.**

Instead, please report security vulnerabilities by emailing the maintainers
directly at the email addresses listed in the repository.

### What to Include

When reporting a vulnerability, please include:

1. **Description**: A clear description of the vulnerability
2. **Impact**: The potential impact of the vulnerability
3. **Steps to Reproduce**: Detailed steps to reproduce the issue
4. **Affected Versions**: Which versions are affected
5. **Suggested Fix**: If you have a suggested fix, please include it

### Response Timeline

- **Initial Response**: Within 48 hours
- **Status Update**: Within 1 week
- **Resolution Target**: Within 30 days for critical issues

### What to Expect

1. **Acknowledgment**: We will acknowledge receipt of your report
2. **Investigation**: We will investigate and validate the issue
3. **Updates**: We will keep you informed of our progress
4. **Credit**: We will credit you in the security advisory (if desired)
5. **Disclosure**: We follow coordinated disclosure practices

## Security Best Practices for Contributors

### Code Security

- Never commit secrets, API keys, or credentials
- Use environment variables for sensitive configuration
- Validate all input from external sources
- Follow the principle of least privilege
- Keep dependencies updated

### SPDX Headers

All source files must include SPDX license headers:

```
// SPDX-License-Identifier: MIT AND LicenseRef-Palimpsest-0.8
// SPDX-FileCopyrightText: 2024-2025 Ehsaneddin Asgari and Contributors
```

### Dependency Security

We use automated tools to monitor dependencies:

```bash
# Run security audit
just security

# Check for outdated packages
just outdated
```

## Security Features

### Container Security

Our Podman containers implement:

- Rootless execution
- Read-only root filesystem
- Dropped capabilities
- No new privileges flag

### Input Validation

All external input is validated:

- URL validation before fetching
- Language code validation (ISO 639)
- Content-type verification
- Size limits on downloads

## Known Security Considerations

### Web Crawling

- Rate limiting is enforced to respect source websites
- robots.txt is respected by default
- User-agent clearly identifies the crawler

### Data Handling

- Corpus data may contain sensitive religious content
- No personal data is collected or stored
- All data processing is local by default

## Security Contacts

For security-related questions that don't warrant a vulnerability report,
please open a discussion on GitHub with the "security" label.
