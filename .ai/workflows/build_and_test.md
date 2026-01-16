# Workflow: Build & Test Popeye

## 1. Prerequisites
- **Compiler:** GCC (tested with `gcc` on macOS/Linux)
- **Make:** GNU Make

## 2. Compilation
To build the `py` executable from source:

```bash
# In the root directory
make -f makefile.unx
```

-   **Note:** The build process generates many warnings (legacy codebase). This is normal.
-   **Output:** The command produces a binary named `py` in the root directory.

## 3. Running Popeye
To run the solver, pass an input file (`.inp`) as an argument:

```bash
./py EXAMPLES/grid.inp
```

## 4. Verification
Popeye outputs the solution directly to standard output.
Example success output:

```text
  1.a7-a5   2.a5-a4   3.a4-a3   4.a3-a2   5.a2-a1=Q   6.Qa1-a4   7.Qa4-c6 #

solution finished. Time = 0.009 s
```

## 5. Cleaning
To remove build artifacts:

```bash
make -f makefile.unx clean
```
