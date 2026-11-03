# 产品裁 · 物理几何 PG-MIN · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 项 | 内容 |
|---|---|
| 角色 | 产品核验；**未改码／未派 Codex／未升头／未合 main** |
| 授权钉 | `phase1-pc-wave7-physics-geometry-pg-min-exec-auth-6c6b0b0-20261103.md` SHA **`a5a51cb1…373d`** commit `24e5026` |
| 机 | `DESKTOP-OQUR45J`／`a8697f40…` |
| tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（父 `9fb9c5b3…`） |
| exe | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` size **272384** · Release／mock／HOTSEAT／Default μ **只读** |
| BIND_MATCH | **true**（产品复核一致） |
| win-verify | SHA256 **`eefb27c67d3ec98e987194f262a98ec06de5e25f6ffc4ab0fddfbd972e797cc4`** ✓ |
| 逐杆表 | SHA256 **`225b972775de1f439dccd1d7c0af48d0019083846d48dac6e509fa4d1885a781`** ✓ |
| evidence zip | SHA256 **`de55bb9ddb0ecf151519c00f4d3304198008f08ccfdb26b77795e5c4eb25d022`**（≈8.3MB）✓ |
| 墙钟交证 | 2026-11-03 **22:39** Asia/Shanghai |

## 产品结论

**包级＝`PARTIAL`（≠ OBSERVE-COMPLETE；≠ 改参获准；≠ 关 A17；≠ 全量物理 PASS）。**

Harness raw 曾写 `PACKAGE=OBSERVE-COMPLETE`＋`M4=pending`：**产品否决 OBSERVE-COMPLETE**，与 PC 诚实裁一致。

| 模块 | 裁 | 依据 |
|---|---|---|
| **BIND** | **PASS** | tip／parent／exe size·SHA／Release·mock·Default／μ 只读／进局成功 |
| **M1** | **PASS** | 轻／中／大各 2 轮均出杆；pct 可分；连续 mp4 齐；无穿透／抖 |
| **M2** | **PASS** | 复用中力 `m2-mid-s2r`；滑→滚可追溯；mp4 SHA `539817D22B91…` |
| **M3** | **PASS** | 固定瞄近库；无塞／左／右各 2 轮出杆；HitPoint 中／左塞／右塞；未见粘库／穿透；偏转主归因＝**待定** |
| **M4** | **缺证／PARTIAL** | 仅 **m4-s08-bot** hint 核实 `进袋[10]`＝**侧／中袋方向 ≥1 正入**；**角袋明确正入缺**；**擦角／弹唇缺**；harness pocket 数字被 Hint `B1`／`3<4` 等假阳性污染——**产品否决以自动计数充正入** |
| 穿透／异常抖动 | **未观测到**（已测卷） | 不升 HARD FAIL |
| 卡死 | **待定** | `m4-s06/s07/s17` 有 `freeze_suspect`；球有运动且对局继续；**不升 HARD FAIL** |
| M5 | 跳过 | 授权默认可不测 |

### 包级判定对照（执行钉）

| 候选 | 产品采纳 | 理由 |
|---|---|---|
| OBSERVE-COMPLETE | **否** | M4 未齐：缺角袋正入＋擦角／弹唇合格观察行（含钉要求的复现门槛） |
| **PARTIAL** | **是** | BIND＋M1＋M2＋M3 证据齐；M4 仅部分（侧袋进袋 1） |
| BLOCKED | 否 | BIND／录屏／进局均成功 |
| 场景 HARD FAIL | 否 | 无已确认穿透／抖／卡死 |

## 禁项钉（维持）

A17 **开**（G3 FAIL 维持）；H **停**；G-ROLL **关**；禁改码／Codex写码／合 main／真服／黑八胜／换皮／升头；零改参；PC 本项 **停手**，**勿自开补测**。

## 请 PM 转用户择下一步

1. **接受本头 PG-MIN＝PARTIAL 归档**（记下 M4 缺口；不宣称观察齐；不改码）  
2. **仅补 M4**：角袋明确正入 ≥1 ＋ 中袋已有可旁证；另各 ≥1 可观察擦角或弹唇；禁 harness 假阳性充数；确认前不派  
3. **按总序进下一项**（三端等）——须明文；A17 仍开、物理 PARTIAL 并存  
4. **另开令**

**≠ 自派补测／≠ 自开改码／≠ 关 A17。等确认。**
