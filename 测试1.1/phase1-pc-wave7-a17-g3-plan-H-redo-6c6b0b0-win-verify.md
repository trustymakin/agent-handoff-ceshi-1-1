# A17 G3 · Plan H REDO win-verify · tip `6c6b0b0` · Asia/Shanghai

**VERIFY ≠ product PASS.** Evidence pack only. Do **not** treat this as product gate close.

| 项 | 值 |
|---|---|
| tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` (short `6c6b0b0`) |
| BIND exe SHA256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` |
| BIND size | **272384** |
| BIND_MATCH | **true** (live re-verified before trial) |
| machine | DESKTOP-OQUR45J |
| machineId | `a8697f40-d1d2-4f9b-a183-5f06c4944b2b` |
| API_MODE / HOTSEAT | mock / app already running (prior HOTSEAT session; pid 198384 since 20:45:16 +08) |
| player present | **yes** (user seated; PM reported play done) |
| auth pin | `/workspace/billiards-playability/phase1-pc-wave7-a17-g3-plan-H-redo-auth-6c6b0b0-20261103.md` SHA `a08930a08ed50573a7b5fc4f94b36e5dbf1b2b484a1a97c7772fab6a2bd0db72` |
| pack write wall | **2026-11-03 21:34:01 +0800** (Asia/Shanghai) |

## Phase A — Trial continuous capture (FIXED redirects)
| 项 | 值 |
|---|---|
| verdict | **PASS** |
| method | `Start-Process -FilePath ffmpeg -RedirectStandardError/-Output` **FILE** redirects (fixes prior empty-mdat root cause) |
| wall_start | **2026-11-03 21:30:48 +08:00** |
| wall_end | **2026-11-03 21:31:00 +08:00** |
| path (win) | `...\shots-a17-g3-plan-H-redo-6c6b0b0\trial-12s.mp4` |
| path (box) | `_a17-g3-plan-H-redo-6c6b0b0/staging/trial-12s.mp4` |
| duration | **12.000 s** |
| size | **97486** bytes |
| SHA256 | `A1A0565B58791DE51C6317167FE818211FE4CA017CD88D354350D5E29772D0B8` |
| ffprobe | h264 1664x1116 · avg_frame_rate=15/1 · nb_frames/packets=**180** · sum_packet_bytes≈94573 |
| contrast prior FAIL | prior Plan H primary was **48-byte empty mdat** SHA `64D52708…` |
| note | Static UI → small bitrate; stream is real continuous video, **not** empty mdat / not 1fps stills collage |

## Phase B — Formal continuous REC
| 项 | 值 |
|---|---|
| formal_started | **NO** |
| FORMAL_RECORD | **MISSING / NEVER_STARTED** |
| REC_START | **n/a** |
| REC_END | **n/a** |
| continuous formal mp4 | **none** (do not fabricate) |
| reason | Trial PASS at 21:31:00 +08; fixed observer not yet launched; user/PM reported play done ≈21:32; STOP+HANDOFF before Start-GdiGrab formal |
| rematch | **no** (PC did not click) |
| inject / auto-scan / PC cue-fire | **no** |

## G3 scored evidence status
| 项 | 值 |
|---|---|
| counted have | `[]` |
| count | **0** |
| disqualified balls | none logged (no formal pocket poll); 本机代打 seat was active at harvest |
| G3 evidence status | **FAIL / BLOCKED_FORMAL_RECORD_MISSING** (VERIFY only; ≠ product PASS claim) |
| slot-after-1/2/3 | **missing** (no counted pockets under formal observer) |
| tray-1/2/3 | **missing** as numbered; post-hoc `*-final.png` / rest / handoff harvested |
| post-hoc frames SHA | `703CC82F8CCBC553696EE60911E49A2427737D8256248B1F2766CE36EA0F01F6` (identical PrintWindow captures at 21:33:14 +08) |

## 本机代打 (plain statement)
**YES, appeared.** At `2026-11-03 21:32:32 +08:00` TurnPill=`轮到 对手B1 · 本机代打` with Hint=`超时仅换手 → B1`. Later at `21:33:14 +08:00` TurnPill returned to `轮到你击球` / Hint=`超时仅换手 → A1`. No `进袋[…]` have list was present in UIA at harvest; therefore **no human-counted ≥3** can be asserted from this redo run.

## Honest continuous video status
- Trial 12s: **PASS** (real h264 @15fps).
- Formal match continuous reel: **MISSING**.
- Do **not** substitute trial or stills as formal play video.

## Deliverables
1. This win-verify
2. `pocket-order-log-g3-plan-H-redo-6c6b0b0.md`
3. Trial mp4 only (formal none)
4. Frames under `_a17-g3-plan-H-redo-6c6b0b0/frames/`
5. Evidence zip + SHA256SUMS.txt
