# PG-MIN physics-geometry · **M4-only** observe · tip `6c6b0b0` · win-verify

| 项 | 内容 |
|---|---|
| 墙钟 | 2026-11-03 23:38:03 +0800 Asia/Shanghai（harness 收尾）／裁稿 23:41 Asia/Shanghai |
| 机 | DESKTOP-OQUR45J / `a8697f40-d1d2-4f9b-a183-5f06c4944b2b` |
| tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` |
| parent | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| exe SHA256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` |
| exe size | **272384** |
| BIND_MATCH | **true** |
| 模式 | Release / mock / HOTSEAT=1 / Default μ **只读**（零改参） |
| μ 声明 | Default 1.45/2.90/4.50 · Soft 1.05/2.10/3.20 · Sticky 1.95/3.80/6.00 · FixedDt 1/900 · **ZERO_PARAM_CHANGE** |
| 闸 | A17 OPEN · Plan H STOPPED · G-ROLL CLOSED · 无改码/无合 main/无真服/无升头 |
| 授权 | `phase1-pc-wave7-physics-geometry-pg-min-m4-only-auth-6c6b0b0-20261103.md` SHA `a31467674b7111ded7b1c13831239d4741fd4a60a12e1427519d3af648f366e7` |
| 范围 | **仅补 M4**；M1–M3 **保留**前裁 PARTIAL（不重跑） |
| Win shot dir | `...\hayo-pc-6c6b0b0-win-runtime\shots-physics-geom-m4-only-6c6b0b0` |
| 包级 OUTCOME（诚实裁） | **PARTIAL／缺证** |

> Harness raw PACKAGE=`PARTIAL`；M4=`pending`（cornerClean=0 sideClean=1；scrape 仅 VISUAL_REVIEW 候选）。**不**升 OBSERVE-COMPLETE：角袋明确正入仍缺；擦角/弹唇未获「连续 mp4 看清接触」的可采信确认（禁发明 scrape 旗）。

## BIND

| 检查 | 结果 |
|---|---|
| tip / parent | MATCH |
| exe SHA/size | MATCH 272384 / 7B6B6B1B… |
| Release/mock/Default | 是 |
| μ 只读 | 是（BilliardsPhysicsContract.cs 探针；未改参） |
| 进 mock 对局 | 成功（ENTER_ATTEMPT=1） |

## 逐模块

| 模块 | 状态 | 证据摘要 |
|---|---|---|
| **M1** | **RETAINED PASS** | 前裁 PARTIAL：`_physics-geom-pg-min-6c6b0b0/phase1-pc-wave7-physics-geometry-min-observe-6c6b0b0-win-verify.md`；本轮 **不重跑** |
| **M2** | **RETAINED PASS** | 同上 |
| **M3** | **RETAINED PASS** | 同上 |
| **M4** | **缺证／pending** | 见下诚实复核 |

### M4 诚实复核（STRICT `进袋[n]`；禁 B1/A1/3\<4 假阳性）

本轮 harness 重写 `Parse-PocketedStrict`：仅匹配字面 `进袋[n]`（n=0..15）。前轮数字刮取假阳性路径已废除。

| 门槛 | 本轮 | 说明 |
|---|---|---|
| 角袋明确正入 ≥1 | **否** | 26 杆无任何 `进袋[n]` 可归因角袋；cornerClean=0 |
| 中袋／侧袋明确正入 ≥1 | **是** | **本轮** `m4-s10-scrTop` hint  verbatim：`击球 进袋[4] · 分彩 solid · 连击`（收球栏球4）；mp4 SHA `C241C33A08079C512448F055864CE7FDD8130D5C1327848EC9E5FF4AAB7DC759`。旁证：前轮 PARTIAL `m4-s08-bot` `进袋[10]` 仍可引用 |
| 角袋侧擦角／弹唇 ≥1 | **否（缺确认）** | harness 记 corner VISUAL_REVIEW 候选 7（如 s01/s02/s05/s06/s09/s24/s25）；**未**把候选升 scrape PASS。抽帧未见「袋口清晰擦碰」定论；禁发明 |
| 中／侧袋侧擦角／弹唇 ≥1 | **否（缺确认）** | side VISUAL_REVIEW 候选 7（如 s03/s04/s07/s15/s16/s17/s23）；同上，不升 scrape PASS |
| 关键对照 ≥2 轮 | **是** | brk / brk2 / brk3 三段 rematch；逐杆连续 mp4（有出杆者）+ 逐杆表 |
| 穿透／异常抖动／确认卡死 | **未确认 FAIL** | 见下 |

#### 本轮核实进袋（STRICT）

| 杆 | hint 实意 | 可否计正入 |
|---|---|---|
| m4-s10-scrTop | **击球 进袋[4] · 分彩 solid · 连击** | **是 → 侧／中袋方向正入 ≥1** |
| 其余 25 杆 | 无 `进袋[`；含开球无效／空杆／换手 B1／母球进袋等 | 否（含 cue scratch 不计目标正入） |

结论：M4 本轮新增 **≥1 侧袋方向明确进袋（球4）**；**角袋正入仍缺**；**擦角／弹唇仍缺合格确认行**（仅有 VISUAL_REVIEW 候选 + 连续 mp4 留审）。禁止用全弹出凑正入——本批未用。

## 穿透 / 抖动 / 卡死

| 项 | 判定 |
|---|---|
| 穿透 | **未观测到** |
| 异常抖动 | **未观测到** |
| 卡死 | harness 对 `m4-s01-corTL`、`m4-s16-sideBot2` 打了 `freeze_suspect`（相位长时间不切启发式）；**非确认卡死**——有行程且对局继续。记 **待定**，**不升 HARD FAIL** |

## 包级判定

| 候选 | 是否采纳 | 理由 |
|---|---|---|
| OBSERVE-COMPLETE（整包 PG-MIN） | **否** | M4 仍缺角袋正入 + 擦角／弹唇合格确认 |
| PARTIAL／缺证 | **是** | BIND 齐；M1–M3 保留；M4 仅侧袋正入 1 + scrape 候选未确认 |
| BLOCKED | 否 | BIND／录屏／进局成功 |

## 产物

| 文件 | 路径 | SHA256 |
|---|---|---|
| win-verify（本文件） | `_physics-geom-pg-min-m4-only-6c6b0b0/phase1-pc-wave7-physics-geometry-min-m4-only-observe-6c6b0b0-win-verify.md` | 见文末 |
| per-shot table | `_physics-geom-pg-min-m4-only-6c6b0b0/per-shot-table-physics-geom-m4-only-6c6b0b0.md` | `a44463b1bd5c0d45a34eb1c7dbd700c6c5e16e9f59dccfef5b227492335f853c` |
| evidence zip | `_physics-geom-pg-min-m4-only-6c6b0b0/physics-geom-m4-only-6c6b0b0-evidence.zip` | `6b03515d7262d67cf78edb1c6ea3409d52ec96dc8cac54418c7a75f0bd61cde4` (size 15825992) |
| bind stamp | `exe-bind-6c6b0b0-physics-geom-m4-only.txt` | `6a540a16b97435a3cb8199a8aa9eb35ffb18774589acade1750e6d532af8991a` |
| harness console | `launch-console-physics-geom-m4-only-6c6b0b0.txt` | — |
| verdict | `verdict-physics-geom-m4-only-6c6b0b0.txt` | `9d56597e94fe80418da258bfd41c120ca86068091151a28c6b2cf99f2362c999` |

## 未做 / OUT

- 不重跑 M1–M3；不改码；不升头；不合 main；零改参；无 rematch-cheat（仅 Exit→再匹配）
- 不把 VISUAL_REVIEW scrape 候选自动记 PASS
- 不把 cue scratch（母球进袋）记目标正入

## 主归因（已测不适）

- M4：侧袋正入可复现路径存在（本轮球4 + 前轮球10）；角袋／擦唇证据不足 → 主归因 **待定**（不预设改 pocket / μ）

### Gate snapshot（报告用）

| Gate | yes/no | shot ids |
|---|---|---|
| Corner clean pot | **no** | — |
| Side/mid clean pot | **yes** | `m4-s10-scrTop`（本轮）；旁证 prior `m4-s08-bot` |
| Corner scrape/lip confirmed | **no** | candidates only: s01,s02,s05,s06,s09,s24,s25 |
| Side scrape/lip confirmed | **no** | candidates only: s03,s04,s07,s15,s16,s17,s23 |
| HARD FAIL (pen/jitter/freeze confirm) | **no** | freeze_suspect 待定: s01,s16 |

### win-verify SHA256 (final · of body above this heading)
`8a98e3f26d41b4b08f2e6a0235fb63fdf8750baa228b3f4010ca0f7e071f6dfc`
