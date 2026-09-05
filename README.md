# Cco Examples & Algorithms Archive

A curated repository of official code examples, machine learning algorithms, data structures, network servers, and verification test suites written in **Cco (C--)**.

- **Compiler Repository**: [**Rohinthan/cco-lang**](https://github.com/Rohinthan/cco-lang)
- **Mathematical Correctness Report**: [`docs/ML_ALGORITHM_CORRECTNESS_VERIFICATION.md`](docs/ML_ALGORITHM_CORRECTNESS_VERIFICATION.md) — Independent Python/NumPy/scikit-learn verification for all 65 machine learning algorithms.

---

## Directory Structure

```
cco-examples/
├── codebase/                    # 240+ comprehensive Cco language examples & test cases
│   ├── 01_hello.cco ... 100_while_break.cco
│   ├── 101_while_continue.cco ... 180_struct_alignment_optimized.cco
│   ├── 181_enum_level_match.cco ... 220_cpp_strings_and_formatting.cco
│   ├── 221_cpp_intro_procedural_vs_oop.cco ... 233_live_socket_tcp_server.cco
│   ├── 234_scope_exit_control_flow_gauntlet.cco ... 240_stateful_map_db_http_server.cco
│   └── 241_linear_regression_variants.cco
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

### Mode A: Direct Execution (`--run`)

Compile and execute any example in a single step using `--run`:

```bash
# Direct run
/path/to/cco codebase/01_hello.cco --run
/path/to/cco algorithms/01_linear_regression.cco --run
```

#### Why Use `--run`?
Cco transpiles to portable ISO C11 rather than using an interpreter or virtual machine. The `--run` flag transpiles the `.cco` source code into intermediate C, invokes `gcc -O3 -Wall -Wextra -std=c11` in the background with math library linking (`-lm`), executes the native binary immediately, and forwards its exit status code.

### Mode B: Standalone Native Binary Compilation

For production compilation and deployment:

```bash
# Step 1: Transpile Cco to standard ISO C11
/path/to/cco algorithms/01_linear_regression.cco -o build/linear_regression.c

# Step 2: Compile to native machine binary
gcc -Wall -Wextra -Werror -pedantic-errors -std=c11 build/linear_regression.c -o build/linear_regression -lm

# Step 3: Run native executable
./build/linear_regression
```

---

## Verification & Memory Safety

- **Valgrind 0-Leak Verification**: All 65 algorithms and 240+ codebase programs pass `valgrind --leak-check=full` with 0 bytes leaked across all heap allocations.
- **Strict Standards Compliance**: Compiles cleanly under `-Wall -Wextra -Werror -pedantic-errors -std=c11 -lm`.
- **Numerical Reference Parity**: Cross-verified against NumPy 2.3.5, scikit-learn 1.9.0, and SciPy 1.18.1.
