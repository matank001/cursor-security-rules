---
description: 
globs: **/*.py,**/*.ipynb,**/*.pyw
alwaysApply: false
---
# Secure Python Development

These rules apply to all Python code in the repository and aim to prevent common security risks through disciplined use of input validation, output encoding, and safe APIs.

All violations must include a clear explanation of which rule was triggered and why, to help developers understand and fix the issue effectively.

if code is in violation add a comment explaining why. 
don't generate code that violates these rules.

## 1. Do Not Use User Input in File Paths
- **Rule:** Never use `input()`, `request.args`, `request.form`, `sys.argv`, or similar sources directly in file paths or file operations.

## 2. Always Sanitize and Validate External Input
- **Rule:** All external input must be sanitized and validated before being used in logic, database queries, file access, or rendering.

## 3. Avoid `eval`, `exec`, and `compile` on Dynamic Input
- **Rule:** Do not use `eval()`, `exec()`, or `compile()` on any user-controllable input.

## 4. Use Constant-Time Comparison for Secrets
- **Rule:** Use `hmac.compare_digest()` for comparing secrets like tokens, passwords, or signatures to prevent timing attacks.

## 5. Do Not Log Sensitive Data
- **Rule:** Logs must not contain passwords, tokens, API keys, private keys, or personally identifiable information (PII).

## 6. Avoid Subprocess Calls with User Input
- **Rule:** Avoid using `os.system`, `subprocess.run`, or similar functions. Use parameterized APIs or sandboxed environments if needed.

## 7. Escape Output in Web Contexts
- **Rule:** When rendering user-generated content into HTML, JSON, or command-line output, always apply appropriate escaping.

## 8. Avoid Hardcoded Secrets
- **Rule:** Do not hardcode passwords, tokens, or secret keys in source code. Use environment variables or a secure configuration service.

## 9. Restrict Dynamic Imports
- **Rule:** Avoid `__import__()` or `importlib` with dynamic or user-controlled values.

## 10. Avoid Loose Type Comparisons in Security Logic
- **Rule:** Use strict type checks and avoid logic that relies on implicit truthiness (e.g., `if token == 0:`) when handling authentication or access control.

## 11. Do Not Use `pickle` with Untrusted Data

- **Rule:** Do not load or deserialize untrusted data using `pickle`, `cPickle`, or `dill`. Use safe formats like `json` or `pydantic` for structured data exchange.