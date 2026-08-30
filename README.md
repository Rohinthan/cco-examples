# Cco Examples & Algorithms Archive

A curated repository of official code examples, algorithms, data structures, network servers, and test suites written in **Cco (C--)**.

---

## Structure & Categories

- **01 - 100**: Language Fundamentals (Variables, Control Flow, Functions, Recursion, Memory Basics)
- **101 - 180**: Data Structures & OOP (Arrays, Strings, Structs, Classes, Methods, Enums, Match Expressions)
- **181 - 220**: Memory Management, Pointers, Scope Lifecycles, and System I/O
- **221 - 233**: Advanced Systems Programming & Networking (HTTP Servers, Binary Protocols, Socket APIs)
- **234 - 240**: Compiler Verification Gauntlet & Stateful In-Memory Database Servers
- **241+**: Machine Learning & Scientific Computing Algorithms (Linear Regression, etc.)

---

## How to Build & Run Any Example

Use the Cco compiler from the [cco-lang](https://github.com/Rohinthan/cco-lang) repository:

```bash
# Compile to C and native binary
/path/to/cco <example_file>.cco -o build/out.c
gcc -Wall -Wextra -Werror -pedantic-errors -std=c11 build/out.c -o build/out -lm

# Run executable
./build/out
```
