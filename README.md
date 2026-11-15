# makefun-tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Hardi24/makefun-tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Hardi24/makefun-tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

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

## Run it

```sh
python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=b8hax0j7&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
