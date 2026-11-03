# A17 / G3 plan H-tight-short3 win-verify — tip 6c6b0b0

written: 2026-11-04 03:38:00 +08:00 Asia/Shanghai  
machine: DESKTOP-OQUR45J (a8697f40-d1d2-4f9b-a183-5f06c4944b2b)  
product: human-play record-only after reclear8; EXIT on FLIPPED; 代打窗不计; no rematch/auto-clear/cue

## OUTCOME

**OUTCOME=FAIL/SHORT_OF_3_HUMAN_VERIFIED (FLIPPED_SHORT)**  
**COUNTABLE_N=0**  
**balls=[]**  
**ready_for_win_verify=no**  
G3 FAIL / A17 stays open for product (video may still be judged offline).

## BIND

| field | value |
|-------|-------|
| tip | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` (short `6c6b0b0`) |
| plan | H-tight-short3 |
| exe sha256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` |
| BIND_MATCH | true (exe-bind-6c6b0b0-plan-H-tight-short3.txt) |

## Seat / flip walls

| event | wall Asia/Shanghai |
|-------|--------------------|
| seat_cleared reclear8 | **2026-11-04 03:31:42 +08:00** TurnPill=轮到你击球 Hint=击球·换手→A1 dai_da=false Clock=行动钟30秒 |
| FLIP_WALL (first 本机代打 this watch) | **2026-11-04 03:34:33 +08:00** TurnPill=轮到 对手B1 · 本机代打 |
| REC soft-stop | ~2026-11-04 03:37 +08:00 ffmpeg PID 201572 terminated |
| observer | PID 213272 left alive (poll-only) |

## Formal video index

| field | value |
|-------|-------|
| path (Win) | `C:\Users\ZYDN\Documents\Codex\2026-10-26\windows-hayo-pc-https-github-com\work\hayo-pc-6c6b0b0-win-runtime\shots-a17-g3-plan-H-tight-short3-6c6b0b0\plan-H-tight-short3-primary.mp4` |
| size | 632826204 bytes |
| SHA256 | `93d56253c10db83b4c6e79c9a6abee3098d1930237bbe8790dea05d8067589ed` |
| REC_stopped | true (PID 201572) |
| note | full mp4 not bundled in zip (~603 MiB); SHA+path only |

## COUNT rule (product)

COUNTABLE iff **all** of:
1. TurnPill matches `轮到你*`
2. 非代打 (`dai_da=false` / not `本机代打`)
3. Hint contains `进袋[N]` with ball id N≠0
4. slot-after-N.png + tray-N.png isomorphic frames present
5. **EXCLUDE** any pocket while 本机代打 window
6. **EXCLUDE** post-FLIP pockets (after first FLIP_WALL this seat)
7. self-claim without isomorphic frames is NOT evidence

## Per-ball table (reclear8 seat window)

| ball | wall | TurnPill | dai_da | Hint | slot/tray | verdict |
|------|------|----------|--------|------|-----------|---------|
| 6 | 03:34:36+ | 轮到 对手B1 · 本机代打 | true | 击球 进袋[6] · 连击 | none | **EXCLUDE 代打窗** |
| 7 | 03:34:40+ | 轮到 对手B1 · 本机代打 | true | 击球 进袋[7] · 连击 | none | **EXCLUDE 代打窗** |
| 10 | 03:35:01 | 轮到你击球 | false | 击球 进袋[10] · 连击 | frames/slot-after-10.png + tray-10.png (283605 B each) | **EXCLUDE post-FLIP** (FLIP_WALL=03:34:33; Join-null bug briefly continued watch; NOT claimed) |

**COUNTABLE list: (empty)** — n=0 < 3.

## Ledger / status paths

- pack ledger: `logs/human-pocket-ledger.txt`
- pack status: `logs/human-play-status.txt`
- pack seat: `logs/seat-cleared-reclear8.txt`
- pack STOP: `logs/STOP-EXIT-FLIPPED.txt`
- pack frames (incidental, not claimed): `frames/slot-after-10.png`, `frames/tray-10.png`
- on-machine shotDir: `...\shots-a17-g3-plan-H-tight-short3-6c6b0b0\`

## Notes

- Watch launched after reclear8 at 03:34:32; first HUD poll already FLIPPED at 03:34:33 → EXIT_FLIPPED mandatory; no rematch/cue/code change.
- exitflip script Write-Status Join-null on empty countable prevented clean `break`; forced STOP later; any post-FLIP human Hint进袋[10] frames archived for honesty but **not** countable.
- Product may judge formal mp4 offline; this pack reports HUD-rule COUNTABLE_N=0 only.
