# Cco Examples & Algorithms Archive

A curated repository of official code examples, algorithms, data structures, network servers, and test suites written in **Cco (C--)**.

---

## Directory Structure

```
cco-examples/
├── algorithms/                  # Core algorithms & scientific computing implementations
│   └── 01_linear_regression.cco # Linear regression (OLS, Ridge/L2, Lasso/L1, ElasticNet)
│
├── codebase/                    # 240+ Comprehensive Cco language examples & test cases
│   ├── 01_hello.cco ... 100_while_break.cco
│   ├── 101_while_continue.cco ... 180_struct_alignment_optimized.cco
│   ├── 181_enum_level_match.cco ... 220_cpp_strings_and_formatting.cco
│   ├── 221_cpp_intro_procedural_vs_oop.cco ... 233_live_socket_tcp_server.cco
│   ├── 234_scope_exit_control_flow_gauntlet.cco ... 240_stateful_map_db_http_server.cco
│   └── 241_linear_regression_variants.cco
│
└── README.md
```

---

## How to Build & Run Any Example

Use the Cco compiler from the official [cco-lang](https://github.com/Rohinthan/cco-lang) repository:

```bash
# Compile to C and native binary
/path/to/cco codebase/01_hello.cco -o build/hello.c
gcc -Wall -Wextra -Werror -pedantic-errors -std=c11 build/hello.c -o build/hello -lm

# Run executable
./build/hello
```
