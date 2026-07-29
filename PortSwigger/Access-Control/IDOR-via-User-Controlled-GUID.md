# Broken Access Control via User-Controlled GUID

## Summary

The application contains a Broken Access Control vulnerability because it trusts a user-controlled GUID to determine which user's data should be returned.

By modifying the `userID` parameter and replacing the current user's GUID with another user's GUID, an attacker can access unauthorized user data.

## Impact

An attacker can modify the user-controlled GUID parameter to gain unauthorized access to another user's account.

This may allow the attacker to view sensitive information, such as account credentials, and potentially perform unauthorized actions depending on the application's functionality.

## Steps to Reproduce

1. Navigate to the target application.
2. Log in with a normal user account.
3. Intercept the request using Burp Suite.
4. Identify the user-controlled GUID parameter.
5. Replace the current user's GUID with the administrator's GUID.
6. Forward the modified request.
7. Observe that the administrator's account information is displayed.
8. Modify the password field type from `password` to `text` using Browser DevTools.
9. Retrieve the exposed password.
10. Log in using the administrator credentials.
11. Access the admin panel and delete the user `carlos`.

## Proof of Concept (PoC)

### Original Request

The original request contains the user-controlled GUID parameter.

![Original Request](screenshots/original-request.png)

### Modified Request

The GUID was replaced with the administrator's GUID.

![Modified Request](screenshots/modified-request.png)

### Unauthorized Account Access

The modified request allowed unauthorized access to the administrator account.

![Administrator Account Access](screenshots/admin-account-access.png)

### Password Exposure

The administrator's password was exposed by changing the password field type from `password` to `text`.

![Exposed Password](screenshots/exposed-password.png)

### Admin Panel Access

The administrator credentials were used to access the admin panel.

![Admin Panel Access](screenshots/admin-panel-access.png)

### Delete User

The user `carlos` was successfully deleted.

![Delete Carlos](screenshots/delete-carlos.png)

## Vulnerability Classification

- OWASP Top 10: A01 - Broken Access Control
- Vulnerability Type: IDOR (Insecure Direct Object Reference)

## Remediation

- Do not trust user-controlled identifiers for authorization decisions.
- Implement proper server-side authorization checks.
- Verify that the authenticated user has permission to access the requested resource.
- Use access control mechanisms on every sensitive operation.

## Tools Used

- Burp Suite
- Browser DevTools

## Tools Used

- Burp Suite
- Browser DevTools
