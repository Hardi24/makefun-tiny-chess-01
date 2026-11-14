# tiny-chess-01 entry

A chess engine in 4 KB of Python (MIT). 0x88 board, negamax with
alpha-beta, iterative deepening to a fixed node budget, transposition
table, killer + history move ordering, MVV-LVA captures, quiescence
search, incremental evaluation (material + piece-square tables +
bishop pair + king phase blend). Deterministic: no clock, no unseeded
randomness. `main.py` is the entry; `src.py` (uncommitted) is the
readable source it was packed from with `makefun compress`.
