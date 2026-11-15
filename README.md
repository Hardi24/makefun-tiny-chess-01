# tiny-chess-01 entry

A chess engine in 4 KB of Python (MIT). 0x88 board, negamax with
alpha-beta, iterative deepening to a fixed node budget, transposition
table, killer + history move ordering, MVV-LVA captures, quiescence
search, null-move pruning, late-move reductions, check extensions and
a PeSTO-style tapered evaluation (middlegame piece-square tables with
a king phase blend, bishop pair, hash-based Zobrist keys).
Deterministic: no clock, no unseeded randomness. `main.py` is the
entry; `src.py` (uncommitted) is the readable source it was packed
from with `makefun compress`.

Local practice (kit harness, 6 games vs depth-2/3/4 and nodes-100k/
250k/500k anchors): v5c at 180k nodes/move — trial-0 Elo 1809
(5W 1D 0L), trial-1 Elo 1654 (5W 0D 1L), trial-2 Elo 1654
(5W 0D 1L); mean 1706, up from v3's 1451. Wall 986–1378 s
(< 1800 s), ~4.2 s/move average, max 6.7 s (< 10 s).
