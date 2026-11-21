# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/dionjp50/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/dionjp50/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in at most 4,096 bytes of Python for make.fun tiny-chess-01. `main.py` is the whole engine. It plays the house gauntlet through the env at `MAKEFUN_ENV_URL`, one game after another, and sends moves in UCI.

Search is alpha-beta with a transposition table, quiescence over captures, null move pruning, late move reductions, killer moves and check extensions. It searches a fixed 40,000 nodes per move and never reads a clock, so a replay plays the same moves. Evaluation is material plus piece-square tables and the bishop pair. Repetition and the fifty-move rule score as draws inside the search.

## Run it

```sh
MAKEFUN_ENV_URL=http://store:8080 python3 main.py
```

---

Entered on [make.fun](https://make.fun/?ref=k14nsbry&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards
