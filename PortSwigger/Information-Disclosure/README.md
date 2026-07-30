# Information Disclosure Labs

A collection of my practical **Information Disclosure vulnerability** write-ups from **PortSwigger Web Security Academy**.

This directory contains hands-on labs focused on identifying and exploiting situations where an application unintentionally reveals sensitive information. Information disclosure can expose user data, application details, source code, credentials, or technical information that may help attackers perform further attacks.

## About Information Disclosure

Information Disclosure occurs when a web application reveals information that should not be accessible to users.

Examples include:

* Exposed backup files
* Debug information leakage
* Detailed error messages
* Source code exposure
* Version control history exposure
* Sensitive credentials disclosure

## Completed Labs

### Backup Files

* Discovering publicly accessible backup files.
* Analyzing exposed application files and sensitive data.

### Custom HTTP Header Authentication Bypass

* Testing authentication mechanisms based on HTTP headers.
* Identifying insecure trust in client-controlled headers.

### Debug Page

* Finding exposed debugging information.
* Identifying hidden endpoints and sensitive application details.

### Error Messages

* Analyzing verbose error messages.
* Extracting useful technical information from application responses.

### Version Control History

* Discovering exposed version control files.
* Recovering sensitive information from repository history.

## Skills Practiced

* Information Leakage Identification
* HTTP Response Analysis
* Burp Suite
* Source Code Analysis
* Sensitive Data Discovery
* Web Application Testing
* Security Reporting

## Tools Used

* Burp Suite
* Browser Developer Tools
* Git & GitHub
* Linux Terminal

## Repository Structure

```text
Information-Disclosure/
│
├── Lab-01-Backup-Files/
│   ├── Backup-Files.md
│   └── screenshots/
│
├── Lab-02-Custom-HTTP-Header-Authentication-Bypass/
│   ├── Custom-HTTP-Header-Authentication-Bypass.md
│   └── screenshots/
│
├── Lab-03-Debug-Page/
│   ├── Debug-Page.md
│   └── screenshots/
│
├── Lab-04-Error-Messages/
│   ├── Error-Messages.md
│   └── screenshots/
│
└── Lab-05-Version-Control-History/
    ├── Version-Control-History.md
    └── screenshots/
```

## Methodology

For each lab:

1. Analyze the application behavior.
2. Identify the information disclosure source.
3. Capture and analyze HTTP requests and responses.
4. Extract the exposed information.
5. Document the vulnerability with a technical report and screenshots.

## Disclaimer

All testing was performed in authorized educational environments provided by PortSwigger Web Security Academy.

This repository is created for learning, practice, and demonstrating web security skills.

