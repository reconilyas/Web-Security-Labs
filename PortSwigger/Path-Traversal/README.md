# Path Traversal Labs

A collection of my practical **Path Traversal vulnerability** write-ups from **PortSwigger Web Security Academy**.

This directory contains hands-on labs focused on identifying and exploiting file path manipulation vulnerabilities in web applications. Path Traversal vulnerabilities allow attackers to access files outside the intended directory by manipulating user-controlled file paths.

## About Path Traversal

Path Traversal (also known as Directory Traversal) occurs when an application improperly handles user-controlled file paths, allowing access to unauthorized files on the server.

Potentially exposed information may include:

* Application source code
* Configuration files
* Credentials
* Sensitive operating system files

## Completed Labs

### File Path Traversal - Simple Case

* Identifying vulnerable file path parameters.
* Accessing files outside the intended directory.

### Traversal Sequences Blocked with Absolute Path Bypass

* Bypassing traversal restrictions using absolute paths.
* Reading sensitive files from the server filesystem.

### Traversal Sequences Stripped Non-Recursively

* Exploiting incomplete input sanitization.
* Using crafted traversal sequences to bypass filtering.

### Traversal Sequences Stripped with URL Decode Bypass

* Bypassing security filters through encoding techniques.
* Testing alternative representations of traversal payloads.

### Validation of Start of Path

* Identifying weak path validation.
* Escaping the intended directory using crafted paths.

### File Extension Validation Bypass

* Bypassing file extension restrictions.
* Using null byte techniques to access unauthorized files.

## Skills Practiced

* File Path Analysis
* HTTP Request Manipulation
* Burp Suite
* Input Validation Testing
* File Disclosure Testing
* Web Vulnerability Reporting

## Tools Used

* Burp Suite
* Browser Developer Tools
* Linux Terminal
* Git & GitHub

## Repository Structure

```text id="8p6y3h"
Path-Traversal/
│
├── Lab-01-Path-Traversal/
│   ├── Path-Traversal.md
│   └── screenshots/
│
├── Lab-02-Path-Traversal/
│   ├── Path-Traversal.md
│   └── screenshots/
│
└── Lab-X-Path-Traversal/
    ├── Path-Traversal.md
    └── screenshots/
```

## Methodology

For each lab:

1. Analyze the application functionality.
2. Identify user-controlled file path input.
3. Intercept requests using Burp Suite.
4. Modify parameters to test path validation.
5. Confirm unauthorized file access.
6. Document the vulnerability with screenshots and technical details.

## Disclaimer

All testing was performed in authorized educational environments provided by PortSwigger Web Security Academy.

This repository is created for learning and demonstrating web security skills.
