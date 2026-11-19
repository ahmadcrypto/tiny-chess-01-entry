# tiny-chess-01

A chess engine in 4,096 bytes of Python (stdlib only). 0x88 board,
negamax with alpha-beta and iterative deepening to a fixed node
budget (never a clock), transposition table, killer move, MVV-LVA
ordering, quiescence over captures (and all evasions in check), and
material plus piece-square evaluation. Deterministic: the same
position always yields the same move.

`main.py` is a compressed payload (lzma + base85) that unpacks and
runs the engine; the readable source is kept out of the repo. It
talks to the env at `MAKEFUN_ENV_URL` only, plays each game to the
end, and exits when the trial is done.

MIT licensed, see LICENSE.
