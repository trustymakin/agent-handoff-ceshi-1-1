# PG-MIN physics-geometry observe · tip `6c6b0b0` · win-verify

| 项 | 内容 |
|---|---|
| 墙钟 | 2026-11-03 22:39:43 +0800 Asia/Shanghai |
| 机 | DESKTOP-OQUR45J / `a8697f40-d1d2-4f9b-a183-5f06c4944b2b` |
| tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` |
| parent | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| exe SHA256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` |
| exe size | **272384** |
| BIND_MATCH | **true** |
| 模式 | Release / mock / HOTSEAT=1 / Default μ **只读**（零改参） |
| μ 声明 | Default 1.45/2.90/4.50 · Soft 1.05/2.10/3.20 · Sticky 1.95/3.80/6.00 · FixedDt 1/900 · **ZERO_PARAM_CHANGE** |
| 闸 | A17 OPEN · Plan H STOPPED · G-ROLL CLOSED · 无改码/无合 main/无真服/无升头 |
| Win shot dir | `...\hayo-pc-6c6b0b0-win-runtime\shots-physics-geom-pg-min-6c6b0b0` |
| 包级 OUTCOME（诚实裁） | **PARTIAL** |

> Harness raw verdict wrote `PACKAGE=OBSERVE-COMPLETE` with M4=pending. **PC 产品裁否决 OBSERVE-COMPLETE**：M4 缺合格「角袋明确正入 + 擦角/弹唇」证据行（见下）。本文件 OUTCOME=**PARTIAL**。

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
| **M1** | **PASS** | 同瞄空廊 light/mid/hard 各 2 轮均出杆；pct light=[20,20] mid=[47,47] hard=[74,86]；avg maxDist L/M/H≈532/760/651；行程可分；每杆连续 mp4 |
| **M2** | **PASS** | 复用中力杆 `m2-mid-s2r`；连续录 mp4 SHA `539817D22B91…`；HUD 相位 sliding→rolling 可追溯（rest 本杆未稳定打到；停球由出杆后结算/换手可见）；M1 mid 两行亦有 slide+roll |
| **M3** | **PASS** | 固定近库瞄 (dx=30,dy=170) 中力；无塞/左塞/右塞各 2 轮均出杆；HitPointText=中/左塞/右塞；连续 mp4 齐；未见明确粘库/穿透；偏转对比留待帧审（主归因=待定） |
| **M4** | **缺证** | 见诚实复核 |

### M4 诚实复核（不可把 harness 自动 pocket 计数当正入）

Harness `Parse-PocketedFromHint` 用正则抽数字，被 hint 中的 `B1`/`A1`/`3<4`/`0<4` **污染**，多数 `pocketed=1` 为假阳性。

| 杆 | hint 实意 | 可否计正入 |
|---|---|---|
| m4-s00-brk | **开球无效（无入袋…）** | 否 |
| m4-s01/02/03/05/06/07/12/17 等 | 「击球 · 换手 → B1」或空杆犯规 | 否（B1 假阳性） |
| m4-s08-bot | **击球 进袋[10] · 分彩 stripe · 连击** | **是 → 中袋/边袋侧正入 ≥1** |
| m4-s11-scratchT | 开球无效（无入袋…） | 否 |
| m4-s16-bl2 | 犯规：母球进袋 | 否（scratch，非目标正入） |
| scrape/lip | cornerScrape=0 sideScrape=0；无合格擦角/弹唇连续观察行 | **缺** |
| 角袋明确正入 | 无经 hint 核实的角袋进袋句 | **缺** |

结论：M4 仅有 **≥1 侧袋/中袋方向明确进袋（球10）**；**角袋正入缺证**；**擦角/弹唇缺证**。禁止用「全弹出」凑正入——本批亦未用。

## 穿透 / 抖动 / 卡死

| 项 | 判定 |
|---|---|
| 穿透 | **未观测到**（已测 M1–M3 + M4 出杆卷） |
| 异常抖动 | **未观测到** |
| 卡死 | harness 对 m4-s06/s07/s17 打了 `freeze_suspect`（相位长时间不切启发式）；**非确认卡死**——球有运动且对局继续。记 **待定**，**不升 HARD FAIL**。无空 `FAIL_FLAGS` 可采信条目。 |

## 包级判定

| 候选 | 是否采纳 | 理由 |
|---|---|---|
| OBSERVE-COMPLETE | **否** | M4 缺角袋正入 + 擦角/弹唇合格行 |
| PARTIAL | **是** | BIND+M1+M2+M3 证据齐（含复现）；M4 仅部分（侧袋进袋 1） |
| BLOCKED | 否 | BIND/录屏/进局均成功 |

## 产物

| 文件 | 路径 | SHA256 |
|---|---|---|
| win-verify（本文件） | `_physics-geom-pg-min-6c6b0b0/phase1-pc-wave7-physics-geometry-min-observe-6c6b0b0-win-verify.md` | 见 `physics-geom-pg-min-DELIVERABLE-SHA256.txt` |
| per-shot table | `_physics-geom-pg-min-6c6b0b0/per-shot-table-physics-geom-pg-min-6c6b0b0.md` | `225b972775de1f439dccd1d7c0af48d0019083846d48dac6e509fa4d1885a781` |
| evidence zip | `_physics-geom-pg-min-6c6b0b0/physics-geom-pg-min-6c6b0b0-evidence.zip` | `de55bb9ddb0ecf151519c00f4d3304198008f08ccfdb26b77795e5c4eb25d022` (size 8727849) |
| bind stamp | `exe-bind-6c6b0b0-physics-geom-pg-min.txt` | — |
| harness console | `launch-console-physics-geom-pg-min-6c6b0b0.txt` | — |

## 未做 / OUT

- M5 入堆：跳过（授权默认可不测）
- 贴库专项 / 叠球 / 定量 μ / 六袋全矩阵 / Soft·Sticky / γ / G-ROLL / A17 / Plan H / 黑八胜 / 真服 / 换皮 / 改码：OUT
- 无 rematch-cheat；仅 Exit→再匹配开局

## 主归因（已测不适）

- M1–M3：`no_obvious_discomfort`；力度可分 → 主归因 **待定**（不预设改 power-map/μ）
- M4：证据不足角袋/擦角；唯一核实进袋=球10 → 主归因 **待定**

### win-verify SHA256 (final · of body above this heading)
`ba905b68acb4cb98e2e8f88f8ce89ad90ca658c00d0a5d39731690027f34a793`
