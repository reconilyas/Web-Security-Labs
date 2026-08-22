# Blind SQL Injection — Conditional Responses

## Summary

The application contains a blind SQL injection vulnerability in the tracking cookie used for analytics.

The results of the SQL query are not directly returned, but the application displays a `Welcome back` message when the injected condition evaluates to true. This difference in the response can be used to infer information from the database.

## Impact

An attacker can use conditional responses to extract sensitive information from the database, including user credentials.

## Steps to Reproduce

1. Navigate to the target application.
2. Identify the tracking cookie as the injection point.
3. Intercept the request using Burp Suite.
4. Inject a conditional SQL query into the tracking cookie.
5. Observe the application's response.
6. Use the response difference to determine information about the administrator's password.
7. Extract the required password information.
8. Use the recovered credentials to authenticate as the administrator.

## Proof of Concept

### Original Request

The original request contains the tracking cookie before the blind SQL injection is introduced.

![Original Request](screenshots/LAB6.01-original-request.png)

### Conditional Payload

A conditional SQL payload is inserted into the tracking cookie. The `Welcome back` response indicates that the tested condition is true.

![Conditional Payload](screenshots/LAB6.02-conditional-payload.png)

### Password Extraction

Repeated conditional checks are used to infer the administrator password from the application's responses.

![Password Extraction](screenshots/LAB6.03-password-extraction.png)

### Administrator Login

The recovered password is used to authenticate to the administrator account.

![Administrator Login](screenshots/LAB6.04-administrator-login.png)

## Root Cause

The application incorporates user-controlled cookie data directly into an SQL query without using parameterized queries or prepared statements.

## Remediation

Use parameterized queries or prepared statements so that user-controlled input is treated strictly as data.

Apply least-privilege database permissions and avoid exposing database-dependent response differences that could disclose sensitive information.
