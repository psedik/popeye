# Popeye AI FAQ

## General Capabilities

### Can Popeye play chess (like Stockfish)?
**No.** Popeye is a **problem solver**, not a chess engine.

-   **It does not** play a game against a human or another engine.
-   **It does** calculate all variations to prove a specific stipulation (e.g., "White to mate in 2").
-   It solves for **truth/proof**, not for "best move in a game".

## Supported Variants

### Does Popeye support Crazyhouse (or Loop Chess)?
**No.** There is no native `Condition Crazyhouse` or "drop" mechanic in the codebase.

Closest approximations like **Circe Parachute** (passive return) or **SuperCirce** (immediate rebirth anywhere) do not replicate the active "reserve and drop" mechanic.

### Can it solve Endgame Studies ("Win" or "Draw")?
**Partially.**

-   **Tactical Studies:** Yes, if the "Win" is a forced sequence ending in **Mate** (`#`) or **Stalemate** (`=`) within a specific move count.
-   **Theoretical Studies:** No. Popeye does not support:
    -   Tablebases (Nalimov/Syzygy).
    -   Three-fold repetition detection.
    -   Generic "Eval +2.0" winning conditions.
-   It is a **truth-finder** for finite problems, not an analyst for infinite/positional games.
