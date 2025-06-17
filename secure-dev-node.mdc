---
description: 
globs: **/*.tsx,**/*.ts,**/*.js
alwaysApply: false
---
# Secure Node.js Development

These rules apply to all Node.js code in the repository and aim to prevent common security risks through disciplined use of input validation, output encoding, and safe APIs.

All violations must include a clear explanation of which rule was triggered and why, to help developers understand and fix the issue effectively.  
Generated code must not violate these rules. If a rule is violated, a comment must be added explaining the issue and suggesting a correction.

## 1. Do Not Use User Input in File Paths or Commands
- **Rule:** Never use `req.body`, `req.query`, or similar inputs directly in `fs`, `child_process`, or system-level calls.

## 2. Avoid `eval`, `Function`, and `vm` on Dynamic Input
- **Rule:** Do not use `eval()`, `new Function()`, or `vm.runInNewContext()` with user-controllable values.

## 3. Avoid Synchronous `child_process` and Shell Execution
- **Rule:** Do not use `execSync`, `spawnSync`, or shell execution functions with untrusted input. Avoid them unless strictly necessary and audited.

## 4. Use Environment Variables for Secrets
- **Rule:** Never hardcode secrets such as API Keys, private keys or credentials. Use environment variables and secure configuration loading.

## 5. Sanitize and Validate All External Input
- **Rule:** All inputs (query params, request bodies, headers) must be validated and sanitized before use in logic, queries, or file access.

## 6. Escape Output for HTML or CLI
- **Rule:** Escape dynamic output when inserting into HTML, Markdown, or command-line interfaces to prevent injection.

## 7. Avoid Insecure HTTP Libraries or Defaults
- **Rule:** Always use HTTPS for remote calls. Do not disable SSL validation or use `http` in production environments.

## 8. Keep Dependencies Updated and Scanned
- **Rule:** Regularly audit dependencies using `npm audit`, `yarn audit`, or tools like Snyk. Avoid packages that are deprecated or unmaintained.

## 9. Restrict Dangerous Globals and Prototypes
- **Rule:** Do not modify native prototypes (e.g., `Object.prototype`) or rely on global mutation patterns.

## 10. Use Strict Equality and Type Checks
- **Rule:** Avoid `==` and `!=`. Always use `===` and `!==` to prevent type coercion vulnerabilities.

## 11. Avoid Dynamic `require()`

- **Rule:** Do not use dynamic or user-derived values in `require()` calls. Use only static imports to load modules.