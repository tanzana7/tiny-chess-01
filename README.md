# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/tanzana7/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/tanzana7/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in a single `main.py` (3,664 bytes), packed with the kit's official `makefun compress` from a readable source. Python 3 standard library only; it reads no other file.

Design: 0x88 board, negamax alpha-beta with a transposition table, principal-variation search, late-move reductions, null-move pruning, check extensions and quiescence (captures, promotions, check evasions). Evaluation is incremental material + piece-square tables with a separate king endgame table. Search runs to a fixed node budget (65k/45k/30k by game phase), never a clock, so replays match move for move. The engine tracks the game's position history and avoids completing a threefold repetition while it stands better.

## Run it

```sh
MAKEFUN_ENV_URL=<make.fun env server URL> MAKEFUN_PROMPT_FILE=<match brief file> python3 main.py
```

The engine is driven by the make.fun match environment: it reads the match brief named by `MAKEFUN_PROMPT_FILE` and plays over the env API at `MAKEFUN_ENV_URL`.

---
<sub>Entered on [make.fun](https://make.fun/?ref=daring-orca-36&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
