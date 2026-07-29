# Path Traversal

## Summary

The application contains a Path Traversal vulnerability in the display of product images.

The vulnerability exists because the application does not properly validate the user-controlled `filename` parameter. Although the application attempts to enforce a specific file extension, the validation can be bypassed using a null byte injection.

By manipulating the `filename` parameter, an attacker can access files outside the intended directory, including sensitive system files such as `/etc/passwd`.

---

## Impact

An attacker can access unauthorized files from the server's filesystem.

Successful exploitation allows an attacker to read sensitive system files, which may expose information such as usernames, user IDs, home directories, and login shells.

This information can assist attackers during reconnaissance and further attack planning.

---

## Steps to Reproduce

1. Navigate to the vulnerable application.
2. Open a product page containing an image.
3. Intercept the image request using Burp Suite.
4. Locate the `filename` parameter.
5. Modify the parameter value to:

```text
../../../etc/passwd%00.jpg
```

6. Forward the modified request.
7. Observe that the application returns the contents of the `/etc/passwd` file.

---

## Proof of Concept (PoC)

### Original Request

The original image request contains the user-controlled `filename` parameter.

![Original Request](screenshots/original-request.png)

### Modified Request

The `filename` parameter was modified using Path Traversal and null byte injection to bypass the file extension validation.

![Modified Request](screenshots/modified-request.png)

### Sensitive File Disclosure

The application returned the contents of the `/etc/passwd` file.

![Passwd File Disclosure](screenshots/passwd-file.png)

Screenshots showing:

1. The intercepted request.
2. The modified `filename` parameter containing the Path Traversal payload.
3. The contents of the `/etc/passwd` file.


