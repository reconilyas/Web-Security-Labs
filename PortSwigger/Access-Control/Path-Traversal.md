# Path Traversal

## Summary

The application contains a Path Traversal vulnerability because it does not properly validate user-controlled file path input.

An attacker can manipulate the `filename` parameter to access files outside the intended directory, including sensitive system files such as `/etc/passwd`.

## Impact

An attacker can access sensitive files outside the web root without authorization.

This may disclose system information, including usernames, user IDs, home directories, and login shells, which can assist an attacker in reconnaissance and planning further attacks.

## Steps to Reproduce

1. Navigate to the target application.
2. Intercept the image request using Burp Suite.
3. Identify the `filename` parameter.
4. Modify the parameter value to:

```text
/etc/passwd
