# Cco Examples & Algorithms Archive

A curated repository of official code examples, machine learning algorithms, data structures, network servers, and verification test suites written in **Cco (C--)**.

- **Compiler Repository**: [**Rohinthan/cco-lang**](https://github.com/Rohinthan/cco-lang)
- **Mathematical Correctness Report**: [`docs/ML_ALGORITHM_CORRECTNESS_VERIFICATION.md`](docs/ML_ALGORITHM_CORRECTNESS_VERIFICATION.md) — Independent Python/NumPy/scikit-learn verification for all 65 machine learning algorithms.

---

## Directory Structure

```
cco-examples/
├── codebase/                    # 244+ comprehensive Cco language examples & test cases
│   ├── 01_hello.cco ... 100_while_break.cco
│   ├── 101_while_continue.cco ... 180_struct_alignment_optimized.cco
│   ├── 181_enum_level_match.cco ... 220_cpp_strings_and_formatting.cco
│   ├── 221_cpp_intro_procedural_vs_oop.cco ... 233_live_socket_tcp_server.cco
│   ├── 234_scope_exit_control_flow_gauntlet.cco ... 240_stateful_map_db_http_server.cco
│   ├── 241_linear_regression_variants.cco
│   └── 242_top_level_script_hello.cco ... 244_top_level_script_array_sum.cco
│
├── algorithms/                  # 65 Machine Learning & Scientific Computing Implementations
│   ├── 01_linear_regression.cco ... 13_xgboost_lightgbm.cco
│   ├── 14_kmeans.cco ... 24_logistic_multinomial.cco
│   ├── 25_mlp.cco ... 38_mixture_of_experts.cco
│   ├── 39_a_star_search.cco ... 46_stochastic_gradient_descent.cco
│   └── 47_isolation_forest.cco ... 65_ivf_pq_vector_index.cco
│
├── tests/correctness/           # Subroutine & sensitivity test suites verified against Python
└── docs/                        # Formal verification documentation
```

---

## How to Build & Run Any Example

Use the Cco compiler built from the official [cco-lang](https://github.com/Rohinthan/cco-lang) repository.

### Top-Level Script Syntax (Python-Style Direct Execution)

Entry files can execute statements directly at the top level without boilerplate `fn main() -> int { ... return 0; }`:

```cco
// codebase/242_top_level_script_hello.cco
let greeting: string = "Hello, Cco World!";
let year: int = 2026;
print(greeting);
print(year);
```

Run directly:
```bash
cco codebase/242_top_level_script_hello.cco --run
```

Or compile to a native binary:
```bash
cco codebase/242_top_level_script_hello.cco -o hello
./hello
```

### Direct Execution & Compilation

Compile and execute any example in a single step to execute 

```bash
# Direct run
make cco
```

```bash
make install
```

And now can execute with cco on the file :

```bash
cco filename.cco -o filename 
```
and now run the bin 

```bash
```

---

## Verification & Memory Safety

- **Valgrind 0-Leak Verification**: All 65 algorithms and 240+ codebase programs pass `valgrind --leak-check=full` with 0 bytes leaked across all heap allocations.
- **Strict Standards Compliance**: Compiles cleanly under `-Wall -Wextra -Werror -pedantic-errors -std=c11 -lm`.
- **Numerical Reference Parity**: Cross-verified against NumPy 2.3.5, scikit-learn 1.9.0, and SciPy 1.18.1.
