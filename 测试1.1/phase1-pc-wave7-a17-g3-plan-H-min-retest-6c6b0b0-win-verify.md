# A17 G3 · Plan H **最小补测** win-verify · tip `6c6b0b0` · Asia/Shanghai

**VERIFY ≠ product PASS.** Evidence pack only. Do **not** treat this as product gate close / G3 PASS / A17 close.

| 项 | 值 |
|---|---|
| tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` (short `6c6b0b0`) |
| BIND exe SHA256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` |
| BIND size | **272384** |
| BIND_MATCH | **true** (live reconfirm before trial + formal) |
| machine | DESKTOP-OQUR45J |
| machineId | `a8697f40-d1d2-4f9b-a183-5f06c4944b2b` |
| API_MODE / HOTSEAT | mock / record-only (PC **did not** cue-fire / inject / rematch) |
| player present | **yes** (human play released after seat-clear **2026-11-04 02:25:22 +08**) |
| auth pin | `_github-handoff-ceshi-1-1/测试1.1/phase1-pc-wave7-a17-g3-plan-H-min-retest-auth-6c6b0b0-20261104.md` SHA `8c73a0acb4ddd226cea9cb6d30cc7f26cf8822669fb7b96c28157269c6cf55c5` |
| pack write wall | **2026-11-04 02:31:59 +0800** (Asia/Shanghai) |
| user self-claim | 「进了8球」= **SELF-REPORT only** — **not** cut basis; **not** written as verified |

## Phase A — Trial continuous capture
| 项 | 值 |
|---|---|
| verdict | **PASS** |
| method | Start-Process FILE RedirectStandardError/Output |
| wall_start | **2026-11-04 01:49:24 +08:00** |
| wall_end | **2026-11-04 01:49:37 +08:00** |
| path (win) | `...\shots-a17-g3-plan-H-min-retest-6c6b0b0\trial-12s.mp4` |
| path (box) | `_a17-g3-plan-H-min-retest-6c6b0b0/staging/trial-12s.mp4` (+ pack root copy) |
| duration | **12 s** |
| size | **343891** |
| SHA256 | `83053F63A55C86869BC95D3A3FCFE1257B7B85C8C28B1D1C5817512436B1951B` |
| ffprobe | h264 · avg_frame_rate=15/1 · nb_frames=**180** |
| note | Trial only; **must not** substitute for formal REC |

## Phase B — Formal continuous REC (**HAS formal REC**)
| 项 | 值 |
|---|---|
| formal_started | **YES** |
| FORMAL_RECORD | **PRESENT** |
| REC_START | **2026-11-04 01:50:16 +08:00** (ffmpeg PID **225240**; OBSERVER_ACK same wall) |
| REC_END | **2026-11-04 02:30:20 +08:00** (mp4 mtime proxy; stop note wall 02:30:35; CloseMainWindow failed → soft taskkill; PID gone by 02:30:25 check; **no** Stop-GdiGrab) |
| continuous formal mp4 | `staging/plan-H-min-retest-primary.mp4` |
| duration | **2405.333 s** (~40.09 min) |
| size | **52222418** bytes |
| SHA256 | `C9807FB8DD514E3B7B7F309A1BB75BAB4D22479D60F0F4A595CEE7F330B967B1` |
| ffprobe | h264 **2498×1676** · avg_frame_rate=**15/1** · nb_frames/**nb_read_packets**=**36080** |
| rematch | **no** |
| inject / auto-scan / PC cue-fire / Bump | **no** |
| poll-only observer | PID **222896** stopped after REC (record-only) |

## G3 scored evidence status
| 项 | 值 |
|---|---|
| counted have | `[14]` |
| countable_n | **1** |
| ≥3 human same-match met? | **NO** (1 ＜ 3) |
| disqualified / excluded 代打 pockets | ball **5** @02:26:18; ball **6** @02:26:52; ball **3** @02:28:16 (all TurnPill=`对手B1 · 本机代打`) |
| G3 evidence status | **FAIL / SHORT_OF_3_HUMAN_VERIFIED** (formal REC present; only **1** verifiable human pocket; slot/tray isomorphism frames missing) — VERIFY only; **≠** product PASS |
| slot-after-1/2/3 | **missing** (not captured in-play) |
| tray-1/2/3 | **missing** |
| post-hoc frames | `frames/pocket14-approx-t2212s.png` · `frames/final-hud-printwindow.png` · `frames/primary-last-frame.png` · pre/rec-start PNGs |

## 本机代打 (plain statement)
**YES, appeared** during the scored human-play window after seat-clear (and earlier pre-seat timeout windows).  
Three `进袋[N]` events under `本机代打` were **excluded** from countable have (5 / 6 / 3).  
One human `进袋[14]` under `轮到你击球` was **counted**.

## Honest continuous video status
- Trial 12s: **PASS** (real h264 @15fps).
- Formal match continuous reel: **PRESENT** (real h264 @15fps, ~40 min, SHA above). Do **not** substitute trial for formal.
- Video index: formal covers seat-clear 02:25:22 through REC_END ~02:30:20; pocket14 ≈ t=2212s from REC_START (approx frame `pocket14-approx-t2212s.png`).

## Deliverables
1. This win-verify (repo root + pack copy)
2. `pocket-order-log-g3-plan-H-min-retest-6c6b0b0.md`
3. Formal mp4 + trial mp4
4. Frames under `_a17-g3-plan-H-min-retest-6c6b0b0/frames/`
5. Evidence zip + SHA256SUMS.txt
6. seat-cleared / jiwei-status / console excerpt / trial sha note
