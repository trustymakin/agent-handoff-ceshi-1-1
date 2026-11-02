# G2 pose-seamless win-verify (PC facts only)

**Tag:** phase1-pc-wave7-batch1-g-roll-g2-pose-seamless-6c6b0b0  
**Machine:** DESKTOP-OQUR45J (`a8697f40-d1d2-4f9b-a183-5f06c4944b2b`)  
**Recorded (Asia/Shanghai):** 2026-11-03T05:14:16+08:00 → 2026-11-03T05:17:05+08:00  
**PC result label:** 通过  
**Product PASS:** **NOT claimed.** `VERIFY-COMPLETE ≠ product PASS`. **G-ROLL remains open.**

## BIND table

| Field | Expected / pin | Observed | Match |
|------|----------------|----------|-------|
| tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` | yes |
| tip short | `6c6b0b0` | `6c6b0b0` | yes |
| parent | `9fb9c5b3d2b9890677df549c3f15083452356dda` | `9fb9c5b3d2b9890677df549c3f15083452356dda` | yes |
| exe SHA256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` | yes |
| exe size | 272384 | 272384 | yes |
| exe mtime | `2026-11-03T02:48:30+08:00` | `2026-11-03T02:48:30+08:00` | yes |
| ban DD02432A… | must NOT | False | ok |
| ban ADAEB7F8… | must NOT | False | ok |
| ban tip `5d6987f` | must NOT | False | ok |
| client | ~1650×1080 dpi 144 | DPI=144 targetClientPhys=1650x1080 | yes |
| `$N_CONTINUE` | 继续对局 (B64) | checked at script start | yes |
| **BIND_MATCH** | True | **True** | **yes** |

Exe path:  
`C:\Users\ZYDN\Documents\Codex\2026-10-26\windows-hayo-pc-https-github-com\work\hayo-pc-6c6b0b0-win-runtime\clients\pc\src\FindTeammates.App\bin\x64\Release\net8.0-windows10.0.19041.0\win-x64\FindTeammates.App.exe`

Bind file: `/workspace/billiards-playability/exe-bind-6c6b0b0-g2.txt`  
(Win mirror: `...\shots-g-roll-g2-pose-seamless-6c6b0b0\exe-bind-6c6b0b0-g2.txt`)

## Procedure (executed)

1. Pre-BIND on worktree `hayo-pc-6c6b0b0-win-runtime` → `BIND_MATCH=True` (abort path unused).
2. Launch mock HOTSEAT (`FINDTEAMMATES_API_MODE=mock` + `FINDTEAMMATES_BILLIARDS_HOTSEAT=1`); OTP `13800000001` / `123456`; enter match; Resize-Default; Bump-PowerMax.
3. Calibrate seed pull **without** recording until hold showed 松手出杆 (pct=74, aim=357).
4. **Start-GdiGrab ONE continuous session** (`-t 140`, client window ONLY 1672×1136 @ 20,20) **before** seed Inj-Up.
5. Inj-Up seed → Observe-Motion (fired=True, sliding→rest) → Wait-Rest → post-stop still → turn handoff to 对手B1 (handed=True) → after-handoff still → Wait-My → Calibrate next (pct=55, aim=341) → Inj-Up next → Observe-Motion (fired=True, rolling→rest).
6. Wait out single ffmpeg session; no concat / no splice.
7. Kill app; no idle HOLD. No code change / rebuild / Codex / merge.

## G2 chain facts (PC)

| Step | Fact |
|------|------|
| seed fired | **True** |
| seed pct / aim | **74** / **357** |
| post-stop turn | 轮到 对手B1 · 本机代打 |
| handoff | **True** (turn flip after invalid break) |
| after-handoff turn | 轮到 对手B1 · 本机代打 |
| next fired | **True** |
| next pct / aim | **55** / **341** |
| next phases | rolling（纯滚）→ rest（停） |
| t_from_seed_s (next fire) | ~39s inside same record |
| continuous mp4 | **yes** — one ffmpeg gdigrab, duration **140.000s**, nb_frames **4192**, single h264 stream, size 1881382 |
| rematch retry | not needed (attempt 1 succeeded) |

Visible chain in ONE uncut mp4: seed release → ball motion/stop → turn handoff (B1) → return to 轮到你击球 → next aim/pull → next fire motion. Index PNGs are optional stills only; main evidence is the continuous mp4.

## File list + SHA256

| File | SHA256 | Size |
|------|--------|------|
| `g-roll-g2-pose-seamless-6c6b0b0.mp4` | `5B1898F2FE28ED1208680E6FE3FCD7F59041B96F95E9A55AEBE22ECB6FA45135` | 1881382 |
| `g-roll-g2-pose-seamless-6c6b0b0-evidence.zip` | `1559382A6447CFA68DCB186871AD04155C727974F7F2A681D50DBB10CA70E2D2` | 5893666 |
| `exe-bind-6c6b0b0-g2.txt` | `162E3B47409DBEB6B21009E923547D6B0D74F27D6E90989F22374EE992304C8F` | 604 |

Box paths:
- `/workspace/billiards-playability/g-roll-g2-pose-seamless-6c6b0b0.mp4`
- `/workspace/billiards-playability/g-roll-g2-pose-seamless-6c6b0b0-evidence.zip`
- `/workspace/billiards-playability/exe-bind-6c6b0b0-g2.txt`
- `/workspace/billiards-playability/phase1-pc-wave7-batch1-g-roll-g2-pose-seamless-6c6b0b0-win-verify.md` (this file)
- Staging: `/workspace/billiards-playability/_g2-pose-seamless-6c6b0b0/` (script, fm-lib, verdict, console, keyframe PNG index, sha256-manifest)

Win shot dir:  
`C:\Users\ZYDN\Documents\Codex\2026-10-26\windows-hayo-pc-https-github-com\work\hayo-pc-6c6b0b0-win-runtime\shots-g-roll-g2-pose-seamless-6c6b0b0\`

Zip contents (evidence): continuous mp4, bind, verdict, launch-console, run-stdout, ffmpeg err log, script, and all phase1 PNG stills from the run.

## Notes / bans respected

- No code changes, no Release rebuild, no Codex, no merge main.
- Did **not** re-record axes v2 / prior nextfire segments as replacements.
- Did **not** splice clips; one gdigrab session only.
- Did **not** close G-ROLL; did **not** declare product PASS.
- App killed at end (`KILL pid=200700`); no idle HOLD.

## Verdict line (from Win)

```
G2_POSE_SEAMLESS|通过|seedFired=True seedPct=74 seedAim=357 handed=True ... nextFired=True nextPct=55 ... mp4sha=5B1898F2... demo_ne_pass=True VERIFY_COMPLETE_NE_PRODUCT_PASS=True G_ROLL_OPEN=True
```

**PC status: VERIFY-COMPLETE** (facts above). Product adjudication: out of scope for this dispatch.
