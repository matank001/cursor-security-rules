---
description: 
globs: 
alwaysApply: true
---
# Secure SQL Usage

These rules apply to all code that interacts with SQL databases, regardless of language or framework, including generated code.

All violations must include a clear explanation of which rule was triggered and why, to help developers understand and fix the issue effectively.  
Generated code must not violate these rules. If a rule is violated, a comment must be added explaining the issue and suggesting a correction.

## 1. Always Use Parameterized Queries and Prepared Statements
- **Rule:** Never construct SQL queries by concatenating or interpolating user input directly into the query string. Always use parameterized queries or prepared statements provided by your database library. Prepared statements ensure that user input is treated as data, not executable code, and are the most effective way to prevent SQL injection.
- **Example (unsafe, Python):**
  ```python
  cursor.execute(f"SELECT * FROM users WHERE username = '{username}'")
  ```
- **Example (safe, Python):**
  ```python
  cursor.execute("SELECT * FROM users WHERE username = ?", (username,))
  ```
- **Example (unsafe, PHP):**
  ```php
  $query = "SELECT * FROM users WHERE username = '" . $_GET['username'] . "'";
  $result = mysqli_query($conn, $query);
  ```
- **Example (safe, PHP - using prepared statements):**
  ```php
  $stmt = $conn->prepare("SELECT * FROM users WHERE username = ?");
  $stmt->bind_param("s", $_GET['username']);
  $stmt->execute();
  $result = $stmt->get_result();
  ```

## 2. Validate and Sanitize All Input
- **Rule:** All external input used in queries must be validated for type, length, and format. Apply allow-lists where possible.

## 3. Avoid Dynamic SQL Unless Absolutely Necessary
- **Rule:** Do not use dynamic SQL (e.g., building table or column names from user input) unless there is no alternative. If unavoidable, strictly validate and allow-list all dynamic parts.

## 4. Use Least Privilege Database Accounts
- **Rule:** Connect to the database using accounts with the minimum privileges required for the task. Never use admin or superuser accounts for application queries.

## 5. Do Not Expose Database Errors to Users
- **Rule:** Never return raw database error messages to end users. Log errors securely and show generic error messages instead.

## 6. Avoid Storing Sensitive Data in Plaintext
- **Rule:** Do not store passwords, tokens, or sensitive data in plaintext. Use strong, salted hashing for passwords and encryption for sensitive fields.

## 7. Close Database Connections Properly

- **Rule:** Always close database connections and cursors to avoid resource leaks and potential security issues.