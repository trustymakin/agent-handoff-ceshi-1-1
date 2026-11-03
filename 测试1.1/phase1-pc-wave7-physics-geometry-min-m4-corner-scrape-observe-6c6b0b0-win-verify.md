# PG-MIN physics-geometry · **M4 corner pot + scrape/lip limited** · tip `6c6b0b0` · win-verify

| 项 | 内容 |
|---|---|
| 墙钟 | 2026-11-03 23:47 → 2026-11-04 00:07 Asia/Shanghai（本轮；harness DONE 00:05:33） |
| 机 | DESKTOP-OQUR45J / `a8697f40-d1d2-4f9b-a183-5f06c4944b2b` |
| tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` |
| parent | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| exe SHA256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` |
| exe size | **272384** |
| BIND_MATCH | **true**（开测前＋harness 内各复核一次） |
| 模式 | Release / mock / HOTSEAT=1 / Default μ **只读**（零改参） |
| μ 声明 | Default 1.45/2.90/4.50 · Soft 1.05/2.10/3.20 · Sticky 1.95/3.80/6.00 · FixedDt 1/900 · **ZERO_PARAM_CHANGE** |
| 闸 | A17 OPEN · Plan H STOPPED · G-ROLL CLOSED · 无改码/无合 main/无真服/无升头 |
| 授权 | `phase1-pc-wave7-physics-geometry-m4-corner-scrape-auth-6c6b0b0-20261103.md` SHA `b45ed17fb545309011c123a92493f2933d34631872a69b817e867087e30f8f2a` · handoff `0be4e35` |
| 范围 | **仅**角袋正入＋擦角/弹唇确认；侧/中袋正入已 PASS **不重求**；M1–M3 **保留** |
| 上限 | **12 新杆 / 30 分钟硬停**（先到即停；本轮用满 12 杆 · ~20.5 分钟；**不自动续轮**） |
| Win shot dir | `...\hayo-pc-6c6b0b0-win-runtime\shots-physics-geom-m4-corner-scrape-6c6b0b0` |
| 包级 OUTCOME（诚实裁） | **PARTIAL／缺证** |

> Harness raw PACKAGE=`PARTIAL`；M4=`missing`（cornerClean=0；sideCleanRetained=1；cornerScrapeCand=4；sideScrapeCand=1）。**不**升 OBSERVE-COMPLETE：角袋明确正入仍缺；擦角/弹唇仍无「连续 mp4 看清接触」可采信确认（禁发明 scrape PASS）。

## BIND

| 检查 | 结果 |
|---|---|
| tip / parent | MATCH |
| exe SHA/size | MATCH 272384 / 7B6B6B1B… |
| Release/mock/Default | 是 |
| μ 只读 | 是（探针；未改参） |
| 进 mock 对局 | 成功（ENTER_ATTEMPT=1） |

## 逐模块

| 模块 | 状态 | 证据摘要 |
|---|---|---|
| **M1** | **RETAINED PASS** | 前裁；本轮不重跑 |
| **M2** | **RETAINED PASS** | 同上 |
| **M3** | **RETAINED PASS** | 同上 |
| **M4** | **缺证／missing** | 见下诚实复核 |

### 先验 VISUAL_REVIEW 复核（必先）

对 m4-only 包候选（角 s01/s02/s05/s06/s09/s24/s25；侧 s03/s04/s07/s15/s16/s17/s23）做了 dense head 抽帧（运动在 FFMPEG_START 后前几秒）＋ harness `*-motion*.png` 复核。详见 `prior-candidate-visual-review-6c6b0b0.md`。

**结论：无一升 scrape PASS** — 未见袋口清晰擦碰／弹唇定论帧。VISUAL_REVIEW ≠ PASS。

### 本轮新杆门槛（STRICT `进袋[n]`；禁 B1/A1/3\<4）

| 门槛 | 本轮 | 说明 |
|---|---|---|
| 角袋明确正入 ≥1 | **否** | 12 新杆 **零** `进袋[n]` 可归因角袋；cornerClean=0 |
| 中袋／侧袋明确正入 ≥1 | **已 PASS（保留）** | 不重求；引用 prior `m4-s10-scrTop` STRICT `进袋[4]` mp4 SHA `C241C33A08079C512448F055864CE7FDD8130D5C1327848EC9E5FF4AAB7DC759`（旁证 prior `m4-s08-bot` `进袋[10]`） |
| 角袋侧擦角／弹唇 ≥1 | **否（缺确认）** | 本轮 VISUAL_REVIEW 候选：`m4-s02-corBL`/`m4-s03-scrTL`/`m4-s07-corTR`/`m4-s09-scrTL2`；抽 motion 仍 **未**见袋口清晰接触 → **不升 PASS** |
| 中／侧袋侧擦角／弹唇 ≥1 | **否（缺确认）** | 本轮候选：`m4-s10-scrBot`（mp4 SHA `5F9178913765077C52EABE45D917189B58171F13A6E8E92CEA5923C036471D62`）；同上不升 PASS。`m4-s05-scrTop` 仅母球进袋（cue scratch）不计 |
| 关键对照 ≥2 轮 | **是** | brk + rematch brk2 两段；失败／hold_fail 全留 |
| 穿透／异常抖动／确认卡死 | **未确认 HARD FAIL** | `m4-s06-brk2` harness `freeze_suspect` → **待定**（有行程／对局继续；不升 HARD FAIL） |

#### 本轮核实进袋（STRICT）

| 杆 | hint 实意 | 可否计正入 |
|---|---|---|
| 全部 12 新杆 | 无字面 `进袋[`；含开球无效／空杆／换手／母球进袋／hold_fail | **否**（cue scratch 不计目标正入） |

## 穿透 / 抖动 / 卡死

| 项 | 判定 |
|---|---|
| 穿透 | **未观测到** |
| 异常抖动 | **未观测到** |
| 卡死 | `m4-s06-brk2`=`freeze_suspect` → **待定**，**不升 HARD FAIL** |

## 包级判定

| 候选 | 是否采纳 | 理由 |
|---|---|---|
| OBSERVE-COMPLETE（整包 PG-MIN） | **否** | 角袋正入仍缺；擦角/弹唇仍缺合格确认 |
| PARTIAL／缺证 | **是** | BIND 齐；M1–M3 保留；侧袋正入保留；本轮 12/30 硬停仍缺角袋＋确认擦唇 |
| BLOCKED | 否 | BIND／录屏／进局成功 |

## 产物

| 文件 | 路径 | SHA256 |
|---|---|---|
| win-verify（本文件） | `_physics-geom-pg-min-m4-corner-scrape-6c6b0b0/phase1-pc-wave7-physics-geometry-min-m4-corner-scrape-observe-6c6b0b0-win-verify.md` | 见文末 |
| per-shot table | `per-shot-table-physics-geom-m4-corner-scrape-6c6b0b0.md` | `f17db24d9ccda77480bf2d0177cc6f1dabf30c8dc6327601935c21e2c4d1c68b` |
| evidence zip | `physics-geom-m4-corner-scrape-6c6b0b0-evidence.zip` | `77c72730bf254b743bb7d2c03857483f2b73682293c79862b53d69f0909ce0c1` (size 9488809) |
| bind stamp | `exe-bind-6c6b0b0-physics-geom-m4-corner-scrape.txt` | `28be712c7fcb324da4df67da5d4710e75d1340b304b37796c15756dc99535267` |
| verdict | `verdict-physics-geom-m4-corner-scrape-6c6b0b0.txt` | `d07d1caf13588db377e3ec7dc69435e0421afd715f6407325eb0862d10761745` |
| prior VISUAL_REVIEW note | `prior-candidate-visual-review-6c6b0b0.md` | `c30c8dc8287be6488001001a3cb99340f86b62003ed10e3e19314e04b0b8a81d` |

### 本轮新杆 mp4 SHA（完整）

| id | SHA256 |
|---|---|
| m4-s00-brk | `42C4DA0DB9FD228D0E3D0AB3E8719FD3570F8226D3DDB86D38B5A546A2B61D40` |
| m4-s01-corTL | `FDBD32BAEA82CA06732B2265AC33766052DCA183504C73AB77AAFA30CC00032D` |
| m4-s02-corBL | `938208FFDFB40272E54FD13DC46C018DC29C3667935FCC123FDF34FB6D848F93` |
| m4-s03-scrTL | `DDB7EA4E643DBFB3B8C04D4F19D9E18129735969DB5927F33340D18E330ECA4E` |
| m4-s05-scrTop | `FAB814A70E01AE41145C0175B5B614849A0627017CD9ED117C8AF1FDEC785EBF` |
| m4-s06-brk2 | `AC1C18060026637E4CB823F4027A8B1239DC4E85420314E6C17540AE96C1FD5C` |
| m4-s07-corTR | `7485E4DC31812FAC02A86CE7EEC6B7C58EB3AD4577453EB910BF61E4E0B3C4B4` |
| m4-s08-corBR | `ACDC2C48D709AF3511DF3BBBE0699E0399D6100C3D43034E2F15EB49CC117E70` |
| m4-s09-scrTL2 | `20854BD72F8519ACF3E71F06C3C638D844037544CF3BAC38647AE2453F0B5B1A` |
| m4-s10-scrBot | `5F9178913765077C52EABE45D917189B58171F13A6E8E92CEA5923C036471D62` |

## 未做 / OUT

- 不重跑 M1–M3；不改码；不升头；不合 main；零改参
- 不把 VISUAL_REVIEW scrape 候选自动记 PASS（先验＋本轮均未升）
- 不把 cue scratch（母球进袋）记目标正入
- **硬停后不自动续轮**（即使用满 12 杆仍缺证）

## Gate snapshot（报告用）

| Gate | yes/no | shot ids |
|---|---|---|
| Corner clean pot | **no** | — |
| Side/mid clean pot | **yes (retained)** | prior `m4-s10-scrTop`；旁证 prior `m4-s08-bot` |
| Corner scrape/lip confirmed | **no** | candidates only: s02,s03,s07,s09（本轮）＋ prior corner cands |
| Side scrape/lip confirmed | **no** | candidates only: s10（本轮）＋ prior side cands |
| HARD FAIL (pen/jitter/freeze confirm) | **no** | freeze_suspect 待定: s06 |
| Shots used / minutes used | **12 / ~20.5** | hard stop hit (shot cap); wall remain ~9.5m unused for deliverables only |

### win-verify SHA256 (final · of body above this heading)
`ce5fc43401ebffbe9c75537d50457e3ff0d1e5b47bbcda12f8f1ac6e60528718`
