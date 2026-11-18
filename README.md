# tiny-chess-engine

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/feza992/tiny-chess-engine/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/feza992/tiny-chess-engine/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine that spends its nodes on forcing lines first. Instead of a plain alpha-beta search, it runs Principal Variation Search (null-window searches for every non-principal move, re-searched only when they look better), extends the search a ply whenever the side to move is in check, and orders moves with a transposition table, MVV-LVA captures and killer moves. The evaluation is structure-aware: material plus my own piece-square tables plus a pawn-structure term (passed pawns rewarded by advancement, doubled and isolated pawns penalised). Deterministic by design — a fixed node budget, no clock, no randomness — so a replayed trial plays the same moves.

## Run it

```sh
MAKEFUN_ENV_URL=http://127.0.0.1:8080 python3 -P -s main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
