# A17 G3 FAIL · 产品侧 RCA 草稿 · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 项 | 内容 |
|---|---|
| 角色 | **产品侧只读根因分析草稿**（待与 PC RCA 合并） |
| Tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（短 `6c6b0b0`） |
| 父 tip | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| exe BIND | size **272384** · SHA256 `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` · **BIND_MATCH=True** · mock＋HOTSEAT |
| 禁项 | **未重测／未改码／未派 Codex**（本草稿只读既有证） |
| 合并对象 | 等 PC RCA 到达后并稿；本稿 ≠ 最终闭环 RCA |
| 产品裁已出 | `phase1-pc-wave7-a17-pocket-rail-min-accept-6c6b0b0-product-cut-20261103.md`（总体未通过／G3 阻断） |

---

## 0 · 一句话结论（产品侧 binary）

**偏向 (B)：三轮（主测／g3supp／g3retry）在同一连续局内，收球槽从未同时达到 ≥3 颗互异目标球；现有证不足以支撑 (A)「多球已入袋但展示漏／覆写」。**  
G3 FAIL 首先表现为 **覆盖未达**（harness 入袋次数不足＋retry 跨 rematch 清空累计），而非已证实的展示轨缺陷。  
**待用户授权再改码**；在用户开闸前不修码、不派 Codex、不开盲第三轮。

---

## 1 · 分轮入袋／槽位表（仅既有证）

### 1.1 主测（06:04–06:32 Asia/Shanghai）

源：`phase1-pc-wave7-a17-min-accept-6c6b0b0-pocket-order-log.md` · `verdict-a17-min-accept.txt` · `logs/harness-stdout.txt`／`launch-console-a17-pocket-rail-min-accept.txt` · 帧 `a17-g1-*`／`a17-g2-*`／`a17-g3-slot-ge3.png`／`a17-g5-*`

| # | mp4t | 墙钟（log） | event | 入袋球号 | 累计 rail L→R（harness `eventBalls`） | chipEst（托盘像素估） | 帧／备注 |
|---|---|---|---|---|---|---|---|
| 1 | 02:12 | 06:07:21 | cue_scratch | （母球／0） | `[]` 空 | 0 | `a17-g2-cue-pocket-event.png`／`a17-g2-slot-no-cue.png`；槽无白 |
| 2 | 06:00 | 06:11:09 | cue_scratch | （母球／0） | `[]` 空 | 0 | 第二次刮库；仍无目标球累计 |
| 3 | 06:59 | 06:12:09 | object_pocket | **#3** | **`[3]`** | 0（像素估 underrun） | `a17-g1-pocket-in.png`／`a17-g1-slot-fill.png`：**视觉确认槽左一格为 #3**；此后至主测结束 **无第二颗** object_pocket |
| — | — | 06:32:01 | G3 判定 | — | have=`[3]` count=**1** | — | `G3=FAIL :: fewer than 3 object balls pocketed; have=[3]` |
| — | — | 06:32:29 | G5 rematch | — | 新局空槽 | 0 | `a17-g5-old-slot-occupied.png`（旧局有 #3）→ enter → `a17-g5-new-empty-slot.png` |

**主测目标球入槽集合＝{#3}，同时在槽＝1，未达 ≥3。**  
同杆多球＝**无；覆盖缺口保留**（G4 已钉）。

### 1.2 g3supp（06:35–06:52）

源：`logs/g3supp-stdout.txt`／`launch-console-a17-g3-supp.txt` · win-verify／problems · **无独立 pocket-order 文件**（本批未产出 g3supp pocket-order.md）

| 观察 | 证据 |
|---|---|
| 全程过程 `have=0`（各 SHOT 行） | g3supp-stdout：`=== SHOT s00 … have=0 ===` … `s15 … have=0 ===` |
| object_pocket | **0 条**（launch-console／stdout 未见 `OBJECT_POCKET`） |
| cue_scratch | s02 mp4t≈01:26；s08 mp4t≈05:07（仅母球入袋旁证） |
| 终态 | 未达 ≥3；problems：「g3supp 未达 ≥3（stdout 过程 `have=0`）」 |
| 对应 rail 槽球号 | **空／无目标球累计**（无 object 事件 → 无 rail 填入记录） |
| 独立终帧 | 本批未单列 g3supp 槽位命名帧；mp4：`phase1-pc-wave7-a17-min-accept-6c6b0b0-g3supp.mp4` |

### 1.3 g3retry（06:53–07:43）

源：`phase1-pc-wave7-a17-min-accept-6c6b0b0-pocket-order-log-g3retry.md` · `verdict-a17-g3-retry.txt` · `logs/g3retry-stdout.txt` · 帧 `a17g3r-g3-ge3-fail.png`（＝交付用 `a17-g3-slot-ge3.png`）

| # | mp4t | round | event | 入袋球号 | 该 round 内 rail L→R | 说明 |
|---|---|---|---|---|---|---|
| 1 | 05:11 | 1 | object_pocket | **#10** | `10` | log `OBJECT_POCKET balls=10 cum=10 count=1`；此后 round1 内 have=1，未见第 2／3 颗 |
| 2 | 16:36 | 2 | cue_scratch | 0 | （round2 起 have 自 0） | rematch 后清空累计 |
| 3 | 17:51 | 2 | cue_scratch | 0 | | |
| 4 | 18:48 | 2 | object_pocket | **#9** | `9` | `balls=9 cum=9 count=1`；round2 内仅 1 颗 |
| 5 | 37:56 | 3 | cue_scratch | 0 | have=0 | round3 无 object_pocket |
| 终 | — | 3 | — | — | **count=0** | `EVENT_BALLS=`；`G3_RETRY_PASS=False`；终帧收球槽**空** |

**跨 round 曾分别出现 #10、#9，但 rematch 清空后从未「同一连续局槽内同时 ≥3」。**  
终态 `G3_RETRY_BALLS=`／`G3_RETRY_COUNT=0`；NOTE 钉主测 `have=[3]`＝球号 3（count=1）。

---

## 2 · `have=[3]` 精确语义

| 说法 | 是否成立 |
|---|---|
| 「收球槽里只有球号 **#3** 一颗（count=1）」 | **是** ← 正确解读 |
| 「已经有 3 颗球／coverage≥3」 | **否** |
| 其它（如 chipEst=3、三槽占位） | **否** |

**证据链：**

1. 主测 verdict：`G3=FAIL :: fewer than 3 object balls pocketed; have=[3]`（`verdict-a17-min-accept.txt`）。  
2. Harness 源码（`_a17-min-accept-6c6b0b0/a17-pocket-rail-min-accept-6c6b0b0.ps1` L463–465）：  
   `Set-Result "G3" "FAIL" ("fewer than 3 object balls pocketed; have=[$([string]::Join(',', $eventBalls))]")`  
   → `have=[…]`＝**`$eventBalls` 球号列表的 join**，不是「已有 N 颗」的计数文案。  
3. `$eventBalls` 由 HintText 解析的 object_pocket 球号去重追加（同脚本 Observe-After-Shot）；主测仅追加一次 `3`。  
4. pocket-order `#3 object_pocket balls=3`／rail=`3` 与之一致。  
5. g3retry verdict NOTE：`have=[3] in main verdict meant ball number 3 (count=1), not three balls`。  
6. 帧 `a17-g1-slot-fill.png`：收球槽可见 **仅 #3**；顶栏剩余全色缺 3，与「一颗入槽」一致。

---

## 3 · 强制二选一（A vs B）

| 选项 | 含义 | 产品侧判定 |
|---|---|---|
| **(A)** | 多颗目标球确已入袋，但展示漏显／覆写／未刷新 | **不采信为当前主因** |
| **(B)** | 场景从未在同一连续局把 ≥3 颗互异目标球留在收球槽 | **偏向 (B)** |

### 偏 (B) 的理由（一句）

三轮书面事件序合计在任一连续局内 object 入槽最多 1 颗（主测 #3；supp 0；retry 各 round 最多 1），终帧／G5 新局亦为空槽或单号，**没有「≥3 已入口却槽空」的同局对照证**。

### 为何不够坐实 (A)

- 主测全程仅 **1** 次 `OBJECT_POCKET`；视觉帧与事件一致（槽有 #3）。  
- g3supp **0** 次 object_pocket。  
- g3retry 两颗目标球分属 **不同 rematch round**，脚本显式 `REMATCH_RESET_EVENT_BALLS`；ACE／G3 要求的是槽内同时 ≥3，不是跨局累计。  
- 终帧 `a17g3r-g3-ge3-fail.png`／交付 `a17-g3-slot-ge3.png`＝**空槽＋开局／未分彩态**，对应 retry 失败收尾，**不是**「三球已进却被 UI 擦掉」的抓拍。  
- 顶栏「未分彩」旁 1/2/3 小图标＝分彩前占位，**不可**误读为已入袋三球（桌上球架仍在）。

### 二元仍缺、需 PC RCA／后续补齐的点

| 缺什么 | 为何影响 A/B |
|---|---|
| 局内 `_pocketedOrder`／权威 `Balls.Pocketed` 快照（与 HintText 并行） | 若权威态曾 ≥3 而槽 UI＝0 → 可翻向 (A) |
| g3supp／主测后段「漏记 object_pocket」审计（Hint 解析失败？） | 若实际入袋未进 `$eventBalls` → 可能低估覆盖 |
| chipEst 恒 0 但 G1 帧可见 #3 | 说明 **像素估不可靠**；不能单靠 chipEst 证「槽空」；需人工帧／UIA 子树 |
| 同杆多球／连续三球可控进球路径 | 覆盖闸；不证明展示 bug |

**结论标签：偏向 (B)＝覆盖缺口；展示缺陷 (A)＝现证不足，留给 PC 用权威态交叉。**

---

## 4 · 缺陷 vs 覆盖 · 分支处理

### 4.1 产品侧主 lean＝**覆盖缺口（B）**

| 标记 | 内容 |
|---|---|
| 状态 | **incomplete（G3 未达）** |
| Blocker | G3／A17-03：同一连续局槽内 ≥3 互异目标球＋停球／换手后再核不重复追加；缺 `a17-g3-slot-after-rest-or-handoff.png`（因未达 ≥3 未拍） |
| 不停手边界 | G1／G2／G4（已覆盖杆）／G5 标签可保留；**不**宣称 A17 最小包关闭／product PASS／合 main |
| Codex／改码 | **否** — **待用户授权再改码** |

### 4.2 定向补测计划（禁止盲第三轮）

仅在用户开闸后执行；目标＝**一次连续局内**打进 ≥3 互异目标球并留下槽位证据，而不是再扫 aim 表碰运气。

1. **预置／选点（仍禁止 force-pocket 冒充 PASS）**  
   - 优先：开局后用**已验证可进**的近袋目标球序列（参考主测 #3、retry #10／#9 成功几何），人工或 harness **短序列三连进**。  
   - 若 mock 允许合法「摆球／练习」且 ACE 不禁：可声明 HelpersUsed，但仍须真实物理入袋。  
2. **中止条件**  
   - 一旦 `eventBalls.Count≥3` 且帧 `a17-g3-slot-ge3.png` 槽内可见 ≥3 互异号 → 立刻拍 `a17-g3-slot-after-rest-or-handoff.png` → 停猎。  
   - 单局 rematch **前**必须已完成 G3；**禁止**用跨 rematch 累计凑 3。  
3. **对照仪器**  
   - 并行记录：HintText pocket 列表、UIA `PocketTray` 子节点名／数、人工帧球号。  
   - 若 Hint≥3 且帧槽＜3 → **当场升级为 (A) 嫌疑**交 PC，停补测改证。  
4. **不做**  
   - 不再开「与 g3supp／g3retry 同构的长时 aim 扫射」第三轮。  
   - 不改物理／μγ、不换皮、不接真服、不重开 G-ROLL、不派 Codex（除非用户另令）。

### 4.3 若日后翻向缺陷 (A) · 只读定位（tip 源码可得）＋最小修提议

箱内只读：`/workspace/wt-pc-pr68` 含 tip `6c6b0b0` 对象。相关符号：

| 位置（tip `6c6b0b0`） | 作用 |
|---|---|
| `BilliardsMatchPage.xaml` L208–235 | `PocketTray` 实体槽（最多 15、注释无母球） |
| `BilliardsMatchPage.xaml.cs` `SyncPocketedOrder` ~L1481 | 按 `Balls.Pocketed` 且 `Id != CueId` 维护 `_pocketedOrder`；回置移除；截断 15 |
| 同文件 `RefreshPocketTray` ~L1497 | Clear → 按 `_pocketedOrder` Distinct 填 `TraySlot`／`MiniBall` |
| 调用点 ~L123／L503；新局 Clear ~L414 | 刷新／清空路径存在 |

**只读观感（非定罪）：** 现逻辑按权威 `Pocketed` 同步顺序并排除母球，**表面上符合 A17-01/02/04 骨架**；主测 G1 帧已证明至少单球入槽可见。  
**在 (B) 主 lean 下，不提出必改产品码。**  
若 PC RCA 用权威态证伪 (B) 并坐实 (A)，最小修候选方向（**待用户授权再改码**）：

1. 核对 `SyncPocketedOrder`／`RefreshPocketTray` 调用是否在「入袋结算／换手／停稳」全路径触发；补漏刷新。  
2. 查 `_pocketedOrder.Clear` 是否在非新局路径误清。  
3. Blast radius：仅 `BilliardsMatchPage` 收球槽 UI；回归 G1–G5＋母球排除＋新局清空；不动物理／G-ROLL。

**在用户书面授权前：不改码、不派 Codex。**

---

## 5 · 与 ACE／产品裁对齐

- ACE（A＋C＋E）：G3 须 ≥3 目标球入槽逐号核；停球／换手后再核。本批 **未满足** → 最小包不可关。  
- 产品裁：总体＝未通过／有限未关；G3 FAIL 阻断；失败已有证＋problems；选项 (a) 仅补 G3／(b) 等修码开闸／(c) 用户另定。  
- 本稿补强：钉 `have=[3]` 语义、分轮表、binary **B**、定向补测而非盲第三轮。

---

## 6 · 等 PC RCA 的关键项

| 项 | 是否阻塞本稿交付 | 说明 |
|---|---|---|
| PC 对 (A)/(B) 的工程侧确认 | **不阻塞**产品草稿交出；**阻塞最终并稿定罪** | 需权威 `Pocketed`／`_pocketedOrder` 或等价日志 |
| 展示刷新路径是否漏调 | 并稿时关键 | 源码骨架在，缺运行时 trace |
| Harness Hint 解析是否漏球 | 并稿时关键 | 影响「覆盖」计数是否低估 |
| 是否授权改码／定向补测 | 产品不自开 | 等用户／PM |

**等待 PC RCA：是（并稿与最终 A/B 钉死）；不等待亦可先把本产品草稿交 PM／用户作证据阅读。**

---

## 7 · 源文件索引

| 文件 | 用途 |
|---|---|
| `phase1-pc-wave7-a17-pocket-rail-min-accept-6c6b0b0-win-verify.md` | G1–G5 标签／G3 奇义／时间窗 |
| `phase1-pc-wave7-a17-min-accept-6c6b0b0-problems.md` | G3 问题清单 |
| `phase1-pc-wave7-a17-min-accept-6c6b0b0-pocket-order-log.md` | 主测事件序 |
| `phase1-pc-wave7-a17-min-accept-6c6b0b0-pocket-order-log-g3retry.md` | retry 事件序 |
| `_a17-min-accept-6c6b0b0/verdict-a17-min-accept.txt` | `have=[3]` 原文 |
| `_a17-min-accept-6c6b0b0/verdict-a17-g3-retry.txt` | retry FAIL＋NOTE |
| `_a17-min-accept-6c6b0b0/logs/*` | OBJECT_POCKET／have=／REMATCH |
| `_a17-min-accept-6c6b0b0/frames/a17-g1-slot-fill.png` 等 | 槽位视觉 |
| `phase1-pc-wave7-a17-pocket-rail-min-accept-6c6b0b0-product-cut-20261103.md` | 产品裁 |
| `phase1-pc-wave7-a17-pocket-rail-acceptance-scope-20261103.md`／exec／ACE | 验收口径 |
| tip 源（只读） | `/workspace/wt-pc-pr68` @ `6c6b0b0` · `RefreshPocketTray`／`SyncPocketedOrder` |

---

## 8 · 页脚

**本稿＝产品侧 G3 RCA 草稿 @ tip `6c6b0b0`。**  
Binary lean **(B)**：从未同局 ≥3 入槽。  
`have=[3]`＝球号列表仅 #3（count=1）。  
未重测／未改码／未派 Codex。  
**待用户授权再改码。** 与 PC RCA 合并后方可作最终工程定罪。

*产品 RCA 草稿 · 2026-11-03 07:55 Asia/Shanghai*
