# A17 G3 FAIL · 产品最终 RCA 并稿（product-cut）· tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 项 | 内容 |
|---|---|
| 角色 | **产品最终并稿**＝PC RCA ＋ 产品草稿合并；**只读既有证**；**未重测／未改码／未派 Codex／未合 main** |
| Tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（短 `6c6b0b0`） |
| 父 tip | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| exe BIND | size **272384** · SHA256 `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` · **BIND_MATCH=True** · mock＋HOTSEAT |
| BIND 文件 | `exe-bind-6c6b0b0-a17.txt` SHA `159791DB…19C3` |
| PC RCA | `phase1-pc-wave7-a17-g3-rca-6c6b0b0-20261103.md` · **verified SHA256 `10C327D719213A9940389BEA600F866AA23246AA4619A14E10A8F3124A533E4B`** |
| 产品草稿 | `phase1-pc-wave7-a17-g3-rca-product-draft-6c6b0b0-20261103.md` |
| 先验产品裁 | `phase1-pc-wave7-a17-pocket-rail-min-accept-6c6b0b0-product-cut-20261103.md`（总体未通过／G3 阻断） |
| 交叉源 | win-verify／problems／pocket-order（main＋g3retry）／verdict／frames／logs |

---

## 0 · 主判（钉死）

### **主判：② 场景未覆盖（覆盖缺口／B）**

与 PC RCA **对齐**：**不是**已证的 **① 展示漏显／覆写／未刷新**。

一句话：主测＋g3supp＋g3retry 在**任一连续对局**内，收球槽「收球」从未同时留下 ≥3 颗互异目标球芯片；单球 #3 入槽可见且与 G1／G5 帧一致；多球 miss／overwrite **未测到、未证明**。

| 选项 | 含义 | 并稿裁定 |
|---|---|---|
| **②／(B)** | 场景从未同局 ≥3 入槽 | **主判** |
| **①／(A)** | 多球已入袋但展示漏／覆写 | **不采信为当前主因**（现证不足） |

日后仅当**定向同局补测**先打进 ≥3 互异目标球、且槽 UI 仍不填／丢球时，方可翻向 ① 并再谈只读定位／改码。

---

## 1 · `have=[3]` 语义（已锁）

**`have=[3]`＝球号列表仅含球 #3（count=1）。不是「已经有三颗球」。**

| 说法 | 是否成立 |
|---|---|
| 收球槽／`$eventBalls` 只有球号 **#3** 一颗（count=1） | **是** |
| 已有 3 颗／coverage≥3 | **否** |
| chipEst=3 或三槽占位 | **否** |

证据链（PC＋产品一致）：

1. 主测 verdict：`G3=FAIL :: fewer than 3 object balls pocketed; have=[3]`（同时 `event_balls=3`＝标量球号，非「三颗」）。
2. Harness：`have=[$([string]::Join(',', $eventBalls))]`；闸＝`$eventBalls.Count -ge 3` → 括号内为**球号 join**。
3. Hint `入袋[3]` → 列表 `[3]` 一元素；pocket-order `#3 object_pocket`／rail=`3`。
4. g3retry NOTE：`have=[3] in main verdict meant ball number 3 (count=1), not three balls`。
5. 帧 `a17-g1-slot-fill.png`／`a17-g5-old-slot-occupied.png`：槽内可见**仅 #3**。

歧义 **关闭**。

---

## 2 · 分轮紧凑表（入袋号／时间／槽累计）

> rail 累计＝harness `eventBalls`（HintText 解析 cum），**非**实时 UIA 托盘枚举。chipEst 常低估；视觉以帧为准。

### 2.1 main（`a17-pocket-rail-min-accept` · FFMPEG ~06:05:09 · 判 G3@06:32:01）

| # | mp4t | 墙钟 Asia/Shanghai | event | 入袋 | slot cum | 备注 |
|---|---|---|---|---|---|---|
| 1 | 02:12 | ~06:07:21 | cue_scratch | — | *(empty)* | 母球；槽无白 |
| 2 | 06:00 | ~06:11:09 | cue_scratch | — | *(empty)* | 第二次刮库 |
| 3 | 06:59 | ~06:12:09 | **object_pocket** | **#3** | **`3`** | 视觉槽左一格 #3；此后无第二颗 object |
| — | — | 06:32:01 | G3 判定 | — | have=`[3]` **count=1** | FAIL |
| — | — | ~06:32+ | G5 rematch | — | 新局空槽 | 预期清槽 |

**同局目标球 max＝1（#3）。**

### 2.2 g3supp（06:35–06:52）

| # | mp4t | 墙钟 | event | 入袋 | slot cum | 备注 |
|---|---|---|---|---|---|---|
| 1 | 01:26 | ~06:37:37 | cue_scratch | — | — | |
| 2 | 05:07 | ~06:41:19 | cue_scratch | — | — | |
| — | — | 全程 | object_pocket | **无** | have=0 | 无独立 pocket-order 对象事件表 |

**同局目标球 max＝0。**

### 2.3 g3retry（FFMPEG ~06:55:12 · 至 07:43；mp4 约截于 ~07:08）

| # | mp4t | 墙钟 | round | event | 入袋 | 该 round slot cum | 备注 |
|---|---|---|---|---|---|---|---|
| 1 | 05:11 | ~07:00:23 | 1 | object_pocket | **#10** | **`10`** | count=1；未见第 2／3 |
| — | — | ~07:10:51 | 1→2 | **rematch** | — | **RESET** | NOFIRE_STREAK；清槽 |
| 2 | 16:36 | ~07:11:48 | 2 | cue_scratch | — | empty | |
| 3 | 17:51 | ~07:13:03 | 2 | cue_scratch | — | — | |
| 4 | 18:48 | ~07:14:00 | 2 | object_pocket | **#9** | **`9`** | count=1 |
| — | — | ~07:32:37 | 2→3 | **rematch** | — | **RESET** | |
| 5 | 37:56 | ~07:33:08 | 3 | cue_scratch | — | — | |
| end | — | 07:43:22 | 3 | — | — | **count=0** | 终帧槽空；`G3_RETRY_PASS=False` |

**任一连续局目标球 max＝1；跨 round 并集 {10,9}（＋主测 #3）≠ 合法 G3 证**（rematch 故意清槽）。

| Run | 同局 object max | 槽同时 ≥3？ |
|---|---|---|
| Main | 1（#3） | **否** |
| g3supp | 0 | **否** |
| g3retry r1／r2／r3 | 1／1／0 | **否** |

---

## 3 · 状态钉（G1–G5／A17／G-ROLL／禁项）

| 项 | 状态 |
|---|---|
| **G1** | **保持 PASS**（本批覆盖） |
| **G2** | **保持 PASS**（本批覆盖；真实 cue_scratch＋槽无白） |
| **G3** | **FAIL 维持**（阻断最小包关闭） |
| **G4** | **保持 PASS（已覆盖杆）**；同杆多球＝无／覆盖缺口保留 |
| **G5** | **保持 PASS**（本批覆盖；exit+new 清槽） |
| A17-05 回置 | 未测 |
| A17-07 重连 | 后置 |
| **A17 最小包** | **仍开／未关**（G3 阻断） |
| A17 全量／product PASS／合 main | **否** |
| **G-ROLL** | **保持关闭** |
| 换皮／物理／真服／黑八胜 | 仍闸 |

### 禁项清单（本并稿延续）

| 禁 | 内容 |
|---|---|
| 禁 tip | `5d6987f`（及历史禁 SHA） |
| 禁 exe（bind 已核未触） | `ban_DD02432A=False`／`ban_ADAEB7F8=False`／`ban_tip_5d6987f=False` |
| 禁操作 | **未重测**；**未改码**；**未派 Codex**；**未合 main**；**禁止盲第三轮**（与主／supp／retry 同构 aim 扫射） |
| 禁宣称 | ≠ product PASS；≠ A17 最小包／全量关闭；跨 rematch 累计 ≠ G3 |

---

## 4 · 定向补测计划（**未执行／待用户授权**）

来源：PC RCA §5 ＋ 产品草稿 §4.2。**≠ 盲第三轮**；本并稿**不执行**。

目标：在**同一连续对局**内打进并保留 ≥3 互异目标球于「收球」，留下帧证；中途 **禁止 rematch 清槽凑数**。

1. **停在同一局**直到 ≥3 互异 object_pocket **且**帧确认槽内 ≥3 芯片可读号。  
   - `eventBalls.Count < 3` 时 **禁用**（或远高于 8）`NOFIRE_STREAK → Exit-And-Rematch`。  
   - 中途结算：不为凑 G3 而 rematch；宁作覆盖未达中止，勿跨局假累计。
2. **G5／exit 前先完成 G3 帧银行**（`a17-g3-slot-ge3.png`＋`a17-g3-slot-after-rest-or-handoff.png`）。
3. HOTSEAT：保持可合法进球座位；分彩后只瞄合法花色以提高入袋率（仍真实物理，**禁止 force-pocket 冒充 PASS**）。
4. 对照仪器：HintText 列表 ＋ UIA PocketTray 子节点 ＋ 人工帧球号并行。  
   - 若 Hint／权威态 ≥3 而帧槽 ＜3 → **当场升级为 ① 嫌疑**，停补测改证，再谈只读码位。
5. **不做**：同构长时 aim 扫射第三轮；改物理／μγ；换皮；真服；重开 G-ROLL；在未证 ① 前改码／派 Codex。

### 改码／Codex 闸

**明确：当前不授权任何 code-change／不派 Codex。**  
仅当定向补测**先证明**「同局多球已入袋但收球轨未填／丢／覆写」后，方可讨论只读定位与最小修（候选：`SyncPocketedOrder`／`RefreshPocketTray`／误 Clear）——仍须**另一次用户书面授权**。

---

## 5 · 交付索引

| 产物 | 路径 | 备注 |
|---|---|---|
| **本并稿** | `phase1-pc-wave7-a17-g3-rca-product-cut-6c6b0b0-20261103.md` | 最终产品 summary cut |
| PC RCA | `phase1-pc-wave7-a17-g3-rca-6c6b0b0-20261103.md` | SHA `10C327D7…3E4B`（已核） |
| 产品草稿 | `phase1-pc-wave7-a17-g3-rca-product-draft-6c6b0b0-20261103.md` | 并入本裁后仅作溯源 |
| 产品裁（先验） | `phase1-pc-wave7-a17-pocket-rail-min-accept-6c6b0b0-product-cut-20261103.md` | 总体未通过 |
| win-verify | `phase1-pc-wave7-a17-pocket-rail-min-accept-6c6b0b0-win-verify.md` | |
| problems | `phase1-pc-wave7-a17-min-accept-6c6b0b0-problems.md` | |
| pocket-order | `…-pocket-order-log.md`／`…-g3retry.md` | |
| 证目录 | `_a17-min-accept-6c6b0b0/` | verdict／logs／frames／mp4 |

---

## 6 · 页脚 · 请用户择一

**本并稿＝产品最终 G3 RCA product-cut @ tip `6c6b0b0`。**  
主判 **② 场景未覆盖（覆盖缺口）**；① 展示缺陷 **未证**。  
`have=[3]`＝仅球号 **#3**（count=1）。  
G1／G2／G4／G5 保持；G3 FAIL 维持；A17 仍开；G-ROLL 关闭。  
**未重测／未改码／未派 Codex。定向补测＝未执行／待用户授权。**

请用户选择：

| 选项 | 内容 |
|---|---|
| **(i)** | **授权仅跑定向 G3 补测**（同连续局 ≥3、禁中途 rematch 清槽凑数；仍不改码／不派 Codex） |
| **(ii)** | **仍 hold**（保持现状；不补测、不改码） |
| **(iii)** | **其它**（用户另定） |

*产品最终 RCA 并稿 · 2026-11-03 ~07:57 Asia/Shanghai · 可转发 PM／用户*
