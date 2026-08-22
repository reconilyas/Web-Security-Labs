# SQL Injection

This directory contains my **PortSwigger Web Security Academy** SQL Injection lab write-ups.

The labs demonstrate different SQL injection techniques, including **UNION-based SQL injection, database information retrieval, blind SQL injection, error-based SQL injection, time-based SQL injection, and filter bypass techniques**.

## Labs

| Lab                                                                                                      | Technique                                |
| -------------------------------------------------------------------------------------------------------- | ---------------------------------------- |
| [Lab 01 — SQL Injection Hidden Data](Lab-01-SQL-Injection-Hidden-Data/)                                  | SQL injection in a `WHERE` clause        |
| [Lab 02 — UNION Attack: Oracle Version](Lab-02-SQL-Injection-UNION-Oracle-Version/)                      | UNION attack and Oracle database version |
| [Lab 03 — UNION Attack: MySQL and Microsoft](Lab-03-SQL-Injection-UNION-MySQL-Microsoft/)                | UNION attack and database version        |
| [Lab 04 — Listing Database Contents](Lab-04-SQL-Injection-Database-Contents/)                            | Retrieving database contents             |
| [Lab 05 — Multiple Values in a Single Column](Lab-05-SQL-Injection-Multiple-Values-Single-Column/)       | String concatenation                     |
| [Lab 06 — Blind SQL Injection: Conditional Responses](Lab-06-Blind-SQL-Injection-Conditional-Responses/) | Conditional responses                    |
| [Lab 07 — Visible Error-Based SQL Injection](Lab-07-SQL-Injection-Visible-Error-Based/)                  | Error-based SQL injection                |
| [Lab 08 — Blind SQL Injection: Time Delays](Lab-08-Blind-SQL-Injection-Time-Delays/)                     | Time-based SQL injection                 |
| [Lab 09 — XML Encoding Filter Bypass](Lab-09-SQL-Injection-XML-Encoding-Filter-Bypass/)                  | Filter bypass using XML encoding         |

## Skills Practiced

* Identifying SQL injection points
* Understanding SQL query structure
* UNION-based SQL injection
* Determining query column counts
* Identifying compatible columns
* Retrieving database information
* Enumerating database tables and columns
* Extracting sensitive data
* Blind SQL injection
* Conditional response analysis
* Error-based SQL injection
* Time-based SQL injection
* Input-filter bypass
* Using **Burp Suite** to intercept and modify requests

## Methodology

The general workflow used throughout these labs was:

```text
Identify Injection Point
        ↓
Understand the Original Query
        ↓
Test SQL Injection
        ↓
Determine Database Behavior
        ↓
Exploit the Vulnerability
        ↓
Verify the Result
        ↓
Document the Finding
```

## Tools

* **Burp Suite**
* **PortSwigger Web Security Academy**
* Web browser

## Disclaimer

These write-ups were created for **authorized security testing and educational purposes** using PortSwigger's intentionally vulnerable labs.

The techniques should only be used against systems where you have explicit permission to conduct security testing.

## References

* [PortSwigger Web Security Academy — SQL Injection](https://portswigger.net/web-security/sql-injection)
* [PortSwigger Web Security Academy — SQL Injection Labs](https://portswigger.net/web-security/sql-injection#labs)
