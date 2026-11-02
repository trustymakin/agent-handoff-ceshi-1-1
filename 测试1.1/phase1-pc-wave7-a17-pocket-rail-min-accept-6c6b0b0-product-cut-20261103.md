# 产品裁 · A17 收球槽／展示轨最小验收 · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 项 | 内容 |
|---|---|
| 角色 | **产品侧核验整理**（只读 PC 证包／写本裁稿）；**未改码／未派 Codex／未合 main／未重测** |
| Tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（短 `6c6b0b0`） |
| 父 tip | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| exe BIND | size **272384** · SHA256 **`7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E`** · mtime `2026-11-03T02:48:30+08:00` · **BIND_MATCH=True** · mock＋HOTSEAT · **未重编** |
| 开测钉 | A＋C＋E（`phase1-pc-wave7-a17-auth-ACE-20261103.md`／acceptance-scope） |
| PC win-verify | `phase1-pc-wave7-a17-pocket-rail-min-accept-6c6b0b0-win-verify.md` |
| 问题清单 | `phase1-pc-wave7-a17-min-accept-6c6b0b0-problems.md` |
| 主测 pocket-order | `phase1-pc-wave7-a17-min-accept-6c6b0b0-pocket-order-log.md` |
| g3retry pocket-order | `phase1-pc-wave7-a17-min-accept-6c6b0b0-pocket-order-log-g3retry.md` |
| 证目录 | `/workspace/billiards-playability/_a17-min-accept-6c6b0b0/` |

---

## 产品结论（总裁）

**总体＝未通过／有限未关。**  
G3 **FAIL** 阻断本批 A17 最小验收包关闭。  
PC 已交主测＋g3supp＋g3retry 证据与 problems；**≠ product PASS**；**≠ A17 全量关闭**；**≠ 合 main**。  
**G-ROLL 保持关**（本批未重测）。换皮／物理／真服／黑八胜仍闸。  
**失败已有证＋问题清单；不授权改码／不派 Codex**，直至用户决定下一步。

---

## BIND／tip／SHA 核验（本机独立 `sha256sum`）

| 项 | 期望／宣称 | 本机核验 | 结果 |
|---|---|---|---|
| tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` | `exe-bind-6c6b0b0-a17.txt` 同行 | **✓** |
| exe SHA256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` | bind 文件＋verdict | **✓** |
| exe size | 272384 | bind 文件 | **✓** |
| BIND_MATCH | True | bind＋verdict＋win-verify | **✓ True** |
| API／HOTSEAT | mock＋HOTSEAT=1 | bind | **✓** |
| 主 mp4 | `0F55803582D99B215EE90C352803B55479AEAEF5DBD1DA5F60971C60DD2A7310` · 6349102 | `0f558035…7310` · 6349102 | **✓** |
| evidence zip | `35854813189AF91E55C90BA6D4E4FEB2E2B6393B088E8601D755328768841AAD` · 21949312 | `35854813…1aad` · 21949312 | **✓** |
| bind 文件 SHA | `159791DB8318D8BF4A37AFF8FA0B90A6D9732198612077C180DE58FE143F19C3` · 640 | `159791db…19c3` · 640 | **✓** |
| g3supp mp4 | `6CB2D0FA…2CFF` · 6243531 | 一致 | **✓** |
| g3retry mp4 | `A06D7A97…736A` · 8491361 | 一致 | **✓** |

禁 tip／禁 exe 未触（bind：`ban_DD02432A=False`／`ban_ADAEB7F8=False`／`ban_tip_5d6987f=False`）。

---

## 分项裁（G1–G5／A17-05／A17-07）

> 标签仅取 PC 书面证据；产品**不发明 PASS**。交叉源：`verdict-a17-min-accept.txt`、pocket-order、win-verify、problems、frames。

| ID | PC 标签 | 产品裁 | 证据要点 |
|---|---|---|---|
| **G1**（A17-01 入槽） | **PASS** | **PASS（本批覆盖）** | 合法目标球入袋；pocket-order `#3` mp4t=06:59 ball=`3`；帧 `a17-g1-pocket-in.png`／`a17-g1-slot-fill.png` |
| **G2**（A17-02 母球排除） | **PASS** | **PASS（本批覆盖）** | **实际发生**母球入袋（cue_scratch mp4t=02:12 与 06:00）；槽无白球芯片；帧 `a17-g2-cue-pocket-event.png`／`a17-g2-slot-no-cue.png`；符合 ACE「仅无白截图 alone ≠ PASS」 |
| **G3**（A17-03 ≥3 互异） | **FAIL** | **FAIL（阻断最小包关闭）** | 主测 `have=[3]`＝**球号 #3 一颗**（count=1），**不是**三颗；g3supp 未达；g3retry `G3_RETRY_PASS=False` count=0、终帧收球槽空；缺 after-rest／handoff 帧。根因见下 |
| **G4**（A17-04 事件序） | **PASS** | **PASS（已覆盖杆次）＋同杆多球覆盖缺口保留** | 主测事件序↔槽序一致 cum=`[3]`；**同杆多球＝无；覆盖缺口保留**；**不**宣称全部顺序场景通过 |
| **G5**（A17-06 新局清空） | **PASS** | **PASS（本批覆盖）** | 路径＝exit+new（Exit-And-Rematch）；旧局有球→进新局→新局空槽；帧 `a17-g5-old-slot-occupied.png`／`a17-g5-enter-new-match.png`／`a17-g5-new-empty-slot.png` |
| **A17-05 回置** | **未测** | **未测** | 本批未触达；不冒充 PASS；按 ACE 不挡「已覆盖项」判定，但 **G3 FAIL 已阻断最小包关闭** |
| **A17-07 重连** | 后置／不测 | **后置（不测／不宣称）** | 本批按 ACE 后置 |

### G3 失败根因（按书面证，不发明）

1. **语义钉**：主测 verdict `have=[3]`＝球号列表仅含 **#3**（count=1），**不是**「已有 3 颗」。与 pocket-order `#3 object_pocket balls=3` 一致；g3retry NOTE 亦钉此点。  
2. **主测**：全程仅 1 颗互异目标球入槽记录。  
3. **g3supp（06:35–06:52）**：未达 ≥3（过程 `have=0`）。  
4. **g3retry（06:53–07:43）**：跨 round 曾记 ball 10／9 单球入袋，但 rematch 清空后槽内从未同时 ≥3；终态 count=0 → 仍 FAIL。按「ONE focused then stop」**未开第三轮**。  
5. **期望未达**：槽内 ≥3 互异目标球＋停球／换手后不重复追加＋`a17-g3-slot-ge3.png`（现为失败终帧空槽）＋`a17-g3-slot-after-rest-or-handoff.png`（未拍）。

### G4 同杆多球

**无；覆盖缺口保留。** 即使 G4 对已覆盖杆次记 PASS，产品裁仍保留该缺口，禁止「全部顺序场景通过」宣称。

---

## 仍闸／不停手边界

| 项 | 状态 |
|---|---|
| A17 最小验收包关闭 | **否**（G3 FAIL 阻断） |
| A17 全量关闭 | **否** |
| product PASS／合 main | **否** |
| G-ROLL | **保持关**（本批未重测） |
| Codex／改码 | **否** — 失败→证据＋problems 已交；**不授权改码／不派 Codex** 直至用户决定 |
| 换皮／物理参数／真服／黑八胜终测 | **仍闸** |
| PC 本项 | **停手**（主测＋supp＋retry 已收；不自开第三轮） |

---

## 建议下一步（仅用户决定；产品不自派 Codex）

| 选项 | 内容 |
|---|---|
| **(a)** | PC **仅补 G3**：第三轮／补测（用户显式开闸后再派） |
| **(b)** | 交问题清单等修码开闸（用户授权改码／Codex 后再动） |
| **(c)** | 其它（用户另定） |

**产品侧不自派 Codex、不改码、不重测。**

---

## 交付索引

| 产物 | 路径 | SHA256（本机） | size |
|---|---|---|---|
| **本裁** | `phase1-pc-wave7-a17-pocket-rail-min-accept-6c6b0b0-product-cut-20261103.md` | （本文） | — |
| win-verify | `phase1-pc-wave7-a17-pocket-rail-min-accept-6c6b0b0-win-verify.md` | `5d50df8f870412c9ea3fc2df13a8a5a5371762c6472c1c42123df99679e7d104` | — |
| problems | `phase1-pc-wave7-a17-min-accept-6c6b0b0-problems.md` | `b32bcbb8d6be0369cccffafa296d2432303462edf7f1f070636f97765a138b09` | — |
| pocket-order | `phase1-pc-wave7-a17-min-accept-6c6b0b0-pocket-order-log.md` | `c99e48b9cb3566464dc491f24f10fcde8210d14102c77e55c6d4428f3b10d6d7` | — |
| BIND | `exe-bind-6c6b0b0-a17.txt` | `159791db8318d8bf4a37aff8fa0b90a6d9732198612077c180de58fe143f19c3` | 640 |
| 主 mp4 | `phase1-pc-wave7-a17-min-accept-6c6b0b0.mp4` | `0f55803582d99b215ee90c352803b55479aeaef5dbd1da5f60971c60dd2a7310` | 6349102 |
| evidence zip | `phase1-pc-wave7-a17-min-accept-6c6b0b0-evidence.zip` | `35854813189af91e55c90ba6d4e4feb2e2b6393b088e8601d755328768841aad` | 21949312 |
| 帧／日志／verdict | `_a17-min-accept-6c6b0b0/` | 见该目录 `SHA256SUMS.txt`／`DELIVERABLE-SHA256.txt` | — |

---

| 时（Asia/Shanghai） | 内容 |
|---|---|
| 2026-11-03 ~07:48 | 产品独立核 BIND／tip／mp4／zip SHA；交叉 G1–G5 书面证；裁＝**未通过／有限未关**（G3 FAIL 阻断）；不改码／不派 Codex；交 handoff `测试1.1/` |

*产品裁 · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai*
