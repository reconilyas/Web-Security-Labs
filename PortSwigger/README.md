# PortSwigger Web Security Labs

A collection of my practical web security lab write-ups from **PortSwigger Web Security Academy**.

This repository documents my learning journey in web application security through hands-on exploitation, vulnerability analysis, and security reporting.

## About

Each lab contains:

* Vulnerability description
* Impact analysis
* Steps to reproduce
* Proof of Concept (PoC)
* Screenshots demonstrating exploitation
* Security recommendations

## Completed Topics

### Access Control

Labs covering authorization vulnerabilities, including:

* Broken Access Control
* User-Controlled GUID
* Role ID Manipulation
* Request Parameter Access Control
* Privilege Escalation

### Information Disclosure

Labs covering unintended exposure of sensitive information, including:

* Backup Files
* Debug Pages
* Error Messages
* Version Control History
* Sensitive Data Exposure

### Path Traversal

Labs covering file path manipulation vulnerabilities, including:

* Reading sensitive system files
* Bypassing path validation
* Accessing unauthorized files

## Tools Used

* Burp Suite
* Browser Developer Tools
* Linux Terminal
* Git & GitHub

## Skills Practiced

* HTTP Request Analysis
* Web Application Testing
* Vulnerability Identification
* Exploitation Techniques
* Security Reporting
* OWASP Top 10 Concepts

## Repository Structure

```
PortSwigger/
│
├── Access-Control/
│   └── Lab-X/
│       ├── Report.md
│       └── screenshots/
│
├── Information-Disclosure/
│   └── Lab-X/
│       ├── Report.md
│       └── screenshots/
│
└── Path-Traversal/
    └── Lab-X/
        ├── Report.md
        └── screenshots/
```

## Methodology

For each vulnerability, I follow this process:

1. Understand the vulnerability behavior.
2. Analyze HTTP requests and responses.
3. Identify the vulnerable parameter or functionality.
4. Exploit the vulnerability in a controlled lab environment.
5. Document the findings with a professional security report.

## Learning Resources

* PortSwigger Web Security Academy
  https://portswigger.net/web-security

* OWASP Top 10
  https://owasp.org/www-project-top-ten/

## Disclaimer

All testing and exploitation techniques documented in this repository were performed in authorized educational environments provided by PortSwigger Web Security Academy.

This repository is intended for learning and demonstrating web security skills.
