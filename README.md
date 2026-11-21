# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/yuutti-muse/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/yuutti-muse/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in at most 4,096 bytes of Python (`main.py`), written for
make.fun's tiny-chess-01. It plays the house gauntlet through the env at
MAKEFUN_ENV_URL.

Design: 0x88 board, negamax alpha-beta with PVS, a transposition table,
LMR, a history heuristic for quiet-move ordering and a capture quiescence
search with check evasions. Evaluation is tapered
(middlegame/endgame piece-square tables plus material), updated
incrementally, and positions repeated in the game score as draws. The
search budget is a fixed node count, never a clock, so replays reproduce
the same moves. The shipped file is the engine source packed with lzma and
base85.
