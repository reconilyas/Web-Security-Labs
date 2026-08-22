# SQL Injection — UNION Attack: Retrieving Database Version

## Summary

The application incorporates user-controlled input directly into the SQL query instead of treating it strictly as data. This allows an attacker to modify the query logic and execute an additional `SELECT` statement using a `UNION` attack.

In this lab, the vulnerability can be exploited to retrieve the database type and version.

## Impact

An attacker can retrieve sensitive information about the underlying database, including its type and version.

This information can help an attacker identify the database technology and select further DBMS-specific attack techniques.

## Steps to Reproduce

1. Navigate to the target application.
2. Identify the injection point in the product category parameter.
3. Intercept the request using Burp Suite.
4. Determine the number of columns returned by the original query.
5. Identify a column that can display string data.
6. Use a UNION SQL injection to retrieve the database version.
7. Send the following payload:

```sql
Pets' UNION SELECT NULL,@@version-- -

8. Observe the database version in the application response.

Proof of Concept
Original Request

The original request contains the vulnerable product category parameter.

Column Count

The number of columns returned by the original query was determined before performing the UNION attack.

Version Payload
Pets' UNION SELECT NULL,@@version-- -
Result

The application returns the database version information in the response.

Root Cause

The application directly incorporates user-controlled input into the SQL query without using parameterized queries or prepared statements.

As a result, an attacker can inject SQL syntax and modify the structure and logic of the original query.

Remediation

Use parameterized queries or prepared statements so that user-controlled input is always treated as data rather than executable SQL.

Additional measures include:

Apply least-privilege database permissions.
Avoid exposing unnecessary database information.
Avoid detailed database error messages in production.
Keep database software securely configured and updated.


