# Path Traversal

## Summary

The application contains a Path Traversal vulnerability because it does not properly validate user-controlled file path input.

An attacker can manipulate the `filename` parameter to access files outside the intended directory, including sensitive system files such as `/etc/passwd`.

---

## Impact

An attacker can access sensitive files outside the web root without authorization.

This may disclose system information, including usernames, user IDs, home directories, and login shells, which can assist an attacker in reconnaissance and planning further attacks.

---

## Steps to Reproduce

1. Navigate to the target application.
2. Intercept the image request using Burp Suite.
3. Identify the `filename` parameter.
4. Modify the parameter value to:

```text
/etc/passwd
```

5. Forward the modified request.
6. Observe that the application returns the contents of the `/etc/passwd` file.

---

## Proof of Concept (PoC)

### Original Request

The original request contains the user-controlled `filename` parameter.

![Original Request](screenshots/original-request.png)

### Modified Request

The `filename` parameter was modified to access the `/etc/passwd` file.

![Modified Request](screenshots/modified-request.png)

### Sensitive File Disclosure

The application returned the contents of the `/etc/passwd` file.

![Passwd File Disclosure](screenshots/passwd-file.png)

Screenshots showing:

1. The intercepted request.
2. The modified `filename` parameter.
3. The contents of the `/etc/passwd` file.
