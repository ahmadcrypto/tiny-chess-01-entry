# tiny-chess-01-entry

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/ahmadcrypto/tiny-chess-01-entry/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/ahmadcrypto/tiny-chess-01-entry/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4,096 bytes of Python (stdlib only). 0x88 board, negamax with alpha-beta and iterative deepening to a fixed node budget (never a clock), transposition table, a single killer move, MVV-LVA ordering, quiescence over captures (and all evasions in check), and material plus piece-square evaluation. Deterministic: the same position always yields the same move.

`main.py` is the kit's `makefun compress` packing of the readable engine source (an LZMA stream in a latin-1 stub); the readable source is kept out of the repo. It talks to the env at `MAKEFUN_ENV_URL` only, plays each game to the end, and exits when the trial is done.

Practice trial (trial-0, 6 games): 2 wins, 0 draws, 4 losses, Elo 1099 — wins over the depth-2 and depth-3 house anchors. Node budget is fixed at 65,000 - 250 per ply; no clock, no randomness.

MIT licensed, see LICENSE.

## Run it

```sh
python3 main.py
```

Set `MAKEFUN_ENV_URL` to the trial env URL first; the engine reads it and plays each game to the end.

---

<sub>Entered on [make.fun](https://make.fun/?ref=f2f8brv2&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
