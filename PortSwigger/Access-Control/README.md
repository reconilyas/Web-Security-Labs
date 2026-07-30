# Access Control Labs

A collection of my practical **Access Control vulnerability** write-ups from **PortSwigger Web Security Academy**.

This directory contains hands-on labs focused on identifying and exploiting authorization flaws in web applications. Each lab documents the vulnerability, exploitation process, and security impact.

## About Access Control

Access Control determines what actions and resources a user is allowed to access after authentication.

Broken Access Control occurs when an application fails to properly enforce authorization rules, allowing users to access functionality or data that should be restricted.

## Completed Labs

### Broken Access Control via Request Parameter

* Manipulating client-controlled parameters to gain unauthorized privileges.
* Testing whether authorization decisions are enforced server-side.

### Broken Access Control via User-Controlled GUID

* Identifying insecure direct object references.
* Accessing resources belonging to other users by modifying identifiers.

### Role ID Manipulation

* Modifying role-related parameters.
* Escalating privileges by changing user role values.

### Custom HTTP Header Authentication Bypass

* Analyzing authentication decisions based on HTTP headers.
* Testing whether headers can be manipulated to bypass restrictions.

### URL / Method / Referer-Based Access Control Issues

* Testing access control mechanisms based on:

  * URLs
  * HTTP methods
  * Referer headers

## Skills Practiced

* HTTP Request Analysis
* Authorization Testing
* Burp Suite
* Parameter Manipulation
* Privilege Escalation Testing
* Access Control Bypass Techniques
* Security Report Writing

## Tools Used

* Burp Suite
* Browser Developer Tools
* Git & GitHub

## Repository Structure

```text
Access-Control/
│
├── Lab-01/
│   ├── Report.md
│   └── screenshots/
│
├── Lab-02/
│   ├── Report.md
│   └── screenshots/
│
└── Lab-X/
    ├── Report.md
    └── screenshots/
```

## Methodology

For each lab:

1. Analyze the application's behavior.
2. Identify the authorization mechanism.
3. Intercept and modify HTTP requests.
4. Test for authorization weaknesses.
5. Document the vulnerability with screenshots and a technical report.

## Disclaimer

All testing was performed in authorized educational environments provided by PortSwigger Web Security Academy.

This repository is for learning and demonstrating web security skills.
