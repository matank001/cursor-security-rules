---
description: 
globs: 
alwaysApply: true
---
# Secure Development Principles

These rules define essential practices for writing and generating secure code.  
They apply universally — to manual development, automated tooling, and AI-generated code.

All violations must include a clear explanation of which rule was triggered and why, to help developers understand and fix the issue effectively.

## 1. Do Not Use Raw User Input in Sensitive Operations
- **Rule:** Untrusted input must never be used directly in file access, command execution, database queries, or similar sensitive operations.

## 2. Do Not Expose Secrets in Public Code
- **Rule:** Secrets such as API keys, credentials, private keys, or tokens must not appear in frontend code, public repositories, or client-distributed files.

## 3. Enforce Secure Communication Protocols
- **Rule:** Only secure protocols (e.g., HTTPS, TLS) must be used for all external communications.

## 4. Avoid Executing Dynamic Code
- **Rule:** Dynamically constructed code or expressions must not be executed at runtime.

## 5. Validate All External Input
- **Rule:** Inputs from users, external APIs, or third-party systems must be validated before use.

## 6. Do Not Log Sensitive Information
- **Rule:** Logs must not contain credentials, tokens, personal identifiers, or other sensitive data.

## 7. Prevent Disabling of Security Controls
- **Rule:** Security checks must not be disabled, bypassed, or suppressed without documented and reviewed justification.

## 8. Limit Trust in Client-Side Logic
- **Rule:** Critical logic related to permissions, authentication, or validation must not rely solely on client-side code.

## 9. Detect and Eliminate Hardcoded Credentials
- **Rule:** Credentials must not be hardcoded in source files, configuration, or scripts.