# Popeye AI Context

## Purpose
This directory (`.ai/`) stores documentation, context, and instructions specifically for AI agents (Gemini, Claude, etc.) working on this repository.
Since the root repository is a legacy codebase with a specific structure, we keep our meta-analysis here to avoid polluting the source.

## Project Overview
**Popeye** is a chess problem solver (orthodox and fairy chess).
- **Language:** C (Legacy)
- **Build:** Makefiles
- **Docs:** `py-engl.txt` (User Manual), `readme.txt` (Build hints)

## Git Workflow & Strategy
We use a **"Maintainer + Contributor"** workflow to handle both personal extensions (AI docs) and potential upstream contributions.

### Remotes
- **`origin`** (`psedik/popeye`): Our writable fork. All pushes go here.
- **`upstream`** (`thomas-maeder/popeye`): The original repo. Read-only for us. We pull updates from here.

### Branches
- **`develop`**: **Mirror of Upstream.** Do not commit here directly.
    - Updates: `git checkout develop && git pull upstream develop`
- **`main`** (Current): **Our Version.**
    - Contains: `.ai/` directory, our configs, experimental features.
    - Updates: `git checkout main && git merge develop` (to get upstream fixes).
- **`fix-feature-name`**: **Contribution Branches.**
    - Create from: `develop` (not `main`!).
    - Use for: Bug fixes meant for Pull Request to upstream.

## Workflows
- **Build & Test:** [workflows/build_and_test.md](workflows/build_and_test.md)

## Key Locations
- `py-engl.txt`: The authoritative guide on input syntax (stipulations, conditions).
- `TESTS/`: Regression tests.
- `makefile.unx`: Unix build instructions.

## Coding Conventions
- This is a legacy C codebase.
- Maintain existing style (indentation, variable naming).
- Avoid C++ features unless explicitly modernizing.

## AI Instructions
- When analyzing code, reference `py-engl.txt` for domain logic.
- When creating tests, add them to `TESTS/` or `REGRESSIONTESTS/` following existing patterns.
