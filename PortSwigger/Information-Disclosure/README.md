# Information Disclosure

## Overview

Information Disclosure is a web security vulnerability where an application unintentionally reveals sensitive or useful information to unauthorized users.

The disclosed information may not always lead to an immediate compromise, but it can help attackers understand the application's internal structure, identify weaknesses, and perform further attacks.

## Common Examples

- Exposed Git repositories (`.git`)
- Backup files
- Configuration files
- Source code exposure
- Debug information
- Error messages revealing sensitive details
- Directory listing
- API keys and secrets
- User credentials
- Server and software version information

## Impact

Successful exploitation of Information Disclosure vulnerabilities may allow attackers to:

- Access sensitive information
- Discover internal application details
- Obtain credentials or secrets
- Understand the application's architecture
- Identify additional attack vectors
- Perform further attacks

## Prevention

To prevent Information Disclosure vulnerabilities:

- Remove sensitive files before deployment.
- Restrict access to sensitive directories such as `.git`.
- Disable unnecessary debug information in production.
- Configure proper error handling.
- Avoid exposing backup files.
- Protect sensitive data and credentials.
- Regularly review application configurations.

## Labs Completed

This directory contains my Information Disclosure lab reports and write-ups.

Each lab includes:

- Vulnerability Summary
- Impact Analysis
- Steps to Reproduce
- Proof of Concept (PoC)
- Screenshots
- Remediation

## Tools Used

- Burp Suite
- Feroxbuster
- Git
- git-dumper

## References

- PortSwigger Web Security Academy - Information Disclosure  
  https://portswigger.net/web-security/information-disclosure

- OWASP Web Security Testing Guide  
  https://owasp.org/www-project-web-security-testing-guide/
