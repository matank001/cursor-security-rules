---
description: 
globs: **/*.c,**/*.h
alwaysApply: false
---
# Secure C Development

These rules apply to all C source and header files in the repository and aim to prevent memory corruption, code injection, and unsafe system behavior.

All violations must include a clear explanation of which rule was triggered and why, to help developers understand and fix the issue effectively.  
Generated code must not violate these rules. If a rule is violated, a comment must be added explaining the issue and suggesting a correction.

## 1. Avoid Unsafe Functions
- **Rule:** Do not use functions like `gets`, `strcpy`, `sprintf`, or `scanf` with `%s`. Use bounded or safer alternatives like `fgets`, `strncpy`, or `snprintf`.

## 2. Always Validate Input Lengths
- **Rule:** Validate the length of user or external input before copying, storing, or processing it to prevent buffer overflows.

## 3. Initialize All Pointers and Memory
- **Rule:** All pointers and allocated memory must be explicitly initialized before use.

## 4. Check All Memory Allocations
- **Rule:** Check the result of `malloc`, `calloc`, or `realloc` for `NULL` before using the returned pointer.

## 5. Avoid Format String Vulnerabilities
- **Rule:** Never pass user-controlled strings directly as the format argument to functions like `printf`, `fprintf`, or `syslog`.

## 6. Free All Allocated Memory
- **Rule:** All dynamic memory must be properly freed to avoid memory leaks. Avoid double-free and use-after-free errors.

## 7. Do Not Trust Environment Variables
- **Rule:** Environment variables must not be used directly in sensitive operations like file access, exec calls, or security checks without validation.

## 8. Avoid System and Shell Calls with Input
- **Rule:** Do not use `system()`, `popen()`, or similar functions with user-controlled input. Use direct APIs when possible.

## 9. Limit Pointer Arithmetic and Casting
- **Rule:** Avoid unnecessary pointer arithmetic and type casting that can bypass bounds or type safety.

## 10. Use Static Analysis and Compiler Warnings
- **Rule:** Enable strict compiler warnings (`-Wall -Wextra -Werror`) and use static analysis tools (e.g., `clang-tidy`, `cppcheck`) to detect risky patterns.

