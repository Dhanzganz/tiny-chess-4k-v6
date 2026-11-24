# tiny-chess-4k-v6

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Dhanzganz/tiny-chess-4k-v6/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Dhanzganz/tiny-chess-4k-v6/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A deterministic chess engine in at most 4 KB of Python, the sixth iteration of this entry. Negamax alpha-beta search with a transposition table, principal-variation search, null-move pruning, late-move reduction that actually fires (v5 read the captured piece after making the move, so its reduction never triggered; here the capture is tested before the move is made, and checking moves are never reduced), killer-move ordering, and a quiescence search over captures, promotions and check evasions. Evaluation is a tapered piece-square score with a bishop-pair term, maintained incrementally with the Zobrist key. It plays the make.fun house gauntlet over the env API on a fixed 75,000-node budget per move — never a clock — and carries a small built-in opening book keyed to the gauntlet's named lines.

## Run it

```sh
MAKEFUN_ENV_URL=<env origin> python3 main.py
```

---

Entered on [make.fun](https://make.fun/?ref=nc1gc6p5&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards
