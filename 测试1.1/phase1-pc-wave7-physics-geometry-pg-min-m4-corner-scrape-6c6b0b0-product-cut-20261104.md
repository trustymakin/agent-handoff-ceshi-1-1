# 产品裁 · 物理几何 PG-MIN **M4 角袋＋擦唇有限补证** · tip `6c6b0b0` · 2026-11-04 Asia/Shanghai

| 项 | 内容 |
|---|---|
| 角色 | 产品核验；**未改码／未派 Codex 写码／未升头／未合 main／未硬派 PC** |
| 授权钉 | `…-m4-corner-scrape-auth-…` SHA **`b45ed17fb545309011c123a92493f2933d34631872a69b817e867087e30f8f2a`** · handoff `0be4e35`（Codex 选 A · 12 杆／30min 先到即停 · 到限不自续） |
| 机 | `DESKTOP-OQUR45J`／`a8697f40…` |
| tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（父 `9fb9c5b3…`） |
| exe | `7B6B6B1B…DB2E` size **272384** · Release／mock／HOTSEAT／Default μ **只读** |
| BIND_MATCH | **true** |
| win-verify | SHA256 **`2eee9d68a8136a8d12d782db8bb689c20f8d37ca21ed2cdc4a00bf531bb2c58d`** ✓ |
| 逐杆表 | SHA256 **`f17db24d9ccda77480bf2d0177cc6f1dabf30c8dc6327601935c21e2c4d1c68b`** ✓ |
| evidence zip | SHA256 **`77c72730bf254b743bb7d2c03857483f2b73682293c79862b53d69f0909ce0c1`**（≈9.0MB）✓ |
| verdict | SHA256 **`d07d1caf13588db377e3ec7dc69435e0421afd715f6407325eb0862d10761745`** ✓ |
| exe-bind | SHA256 **`28be712c7fcb324da4df67da5d4710e75d1340b304b37796c15756dc99535267`** ✓ |
| 墙钟交证 | 2026-11-03 **23:47** → 2026-11-04 **00:08** Asia/Shanghai（12 杆硬停 · ~20.5min；不自续） |

## 产品结论

**包级＝`PARTIAL／到限归档`（≠ OBSERVE-COMPLETE；≠ 改参获准；≠ 关 A17；≠ 自续）。**

| 模块 | 裁 | 依据 |
|---|---|---|
| **BIND** | **PASS** | tip／exe／Release·mock·Default／μ 只读／进局；BIND_MATCH=true |
| **M1–M3** | **RETAINED PASS** | 前裁保留；本轮不重跑 ✓ |
| **M4 侧／中袋正入** | **PASS（保留）** | 前轮 STRICT `进袋[4]`＠`m4-s10-scrTop`；旁证 `进袋[10]`＠`m4-s08-bot`；本轮不重求 |
| **M4 角袋明确正入** | **缺** | cornerClean=0；本轮 12 新杆 **零**字面 `进袋[n]` 可归因角袋 |
| **M4 擦角／弹唇** | **缺确认** | 仅 VISUAL_REVIEW 候选（本轮角 s02/s03/s07/s09；侧 s10）；先验＋本轮抽帧均**未**升 scrape PASS；产品不采「候选＝PASS」 |
| 穿透／抖 | **未观测** | 不升 HARD FAIL |
| 卡死 | **待定** | `freeze_suspect`＠`m4-s06-brk2`；有行程／对局继续；**不升 HARD FAIL** |

### 包级判定

| 候选 | 采纳 | 理由 |
|---|---|---|
| OBSERVE-COMPLETE | **否** | 仍缺角袋正入＋擦角／弹唇合格确认 |
| **PARTIAL／到限归档** | **是** | BIND＋M1–M3 齐；侧／中袋 PASS 保留；12／30 先到（杆数）硬停仍缺角袋＋确认擦唇；**不自动续轮** |
| BLOCKED | 否 | 执行成功 |

## 禁项钉（维持）

A17 **开**；H **停**；G-ROLL **关**；禁改码／Codex写码／合 main／真服／黑八胜／换皮／升头；零改参；PC 本项 **停手**，**勿自开补测／勿自续轮**。

## 下一步

按站立令（分析／下一步若需再问 Codex；过程勿再问用户选型）：**产品转 PM**；确认前 **不自派 PC**、不宣称 OBSERVE-COMPLETE。分析／是否再补若需，再问 Codex（本机 CLI sol·Ultra 只读）。

## 已核 SHA（本机 `sha256sum`）

| 文件 | SHA256 |
|---|---|
| win-verify | `2eee9d68a8136a8d12d782db8bb689c20f8d37ca21ed2cdc4a00bf531bb2c58d` |
| per-shot-table | `f17db24d9ccda77480bf2d0177cc6f1dabf30c8dc6327601935c21e2c4d1c68b` |
| evidence.zip | `77c72730bf254b743bb7d2c03857483f2b73682293c79862b53d69f0909ce0c1` |
| verdict | `d07d1caf13588db377e3ec7dc69435e0421afd715f6407325eb0862d10761745` |
| exe-bind | `28be712c7fcb324da4df67da5d4710e75d1340b304b37796c15756dc99535267` |
| DELIVERABLE-SHA256.txt | `fbdc6c733c83c27adf1871511d27d489bf22cc00d2ce053ced4a1a893909ddc1` |
| prior-candidate-visual-review | `c30c8dc8287be6488001001a3cb99340f86b62003ed10e3e19314e04b0b8a81d` |
| auth（开测钉） | `b45ed17fb545309011c123a92493f2933d34631872a69b817e867087e30f8f2a` |

### 门闩状态

| Gate | 状态 |
|---|---|
| A17 | **开** |
| Plan H | **停** |
| G-ROLL | **关** |
| 改码／合 main／真服／升头／换皮／黑八胜 | **禁** |
| 零改参 | **是** |
| 物理几何 OBSERVE-COMPLETE | **否**（仍 PARTIAL） |
| 本轮自续 | **否**（到限归档） |
