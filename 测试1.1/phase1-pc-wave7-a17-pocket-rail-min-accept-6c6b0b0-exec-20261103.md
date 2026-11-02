# A17 收球槽／展示轨 · PC mock 最小验收执行稿 · tip `6c6b0b0` · 2026-11-03

| 项 | 内容 |
|---|---|
| 角色 | **人测／PC 硬派发执行稿**（G1–G5）；只验收、不改码 |
| 开闸 | 用户确认 **A＋C＋E**（2026-11-03）；原令见 `phase1-pc-wave7-a17-auth-ACE-20261103.md` |
| 范围包 | `phase1-pc-wave7-a17-pocket-rail-acceptance-scope-20261103.md`（已修订开测） |
| 写码 | **不授权改码**；失败先交证＋问题清单 |
| Codex | **不派** |
| 真服／合 main／换皮／物理 | **全部 OUT** |
| G-ROLL | **保持关闭** |
| 关包口径 | 只判定已覆盖项；**≠ A17 全量关闭** |

---

## 0 · BIND（启动前必核 · 不匹配则中止）

| 字段 | 钉 |
|---|---|
| tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` |
| tip short | `6c6b0b0` |
| parent | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| **禁 tip** | `5d6987f`（及历史禁 SHA） |
| exe SHA256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` |
| exe size | **272384** |
| 配置 | **Release** · **win-x64** |
| API | `FINDTEAMMATES_API_MODE=mock`（不接真服） |
| 参考 exe 路径（PC） | `...\hayo-pc-6c6b0b0-win-runtime\clients\pc\src\FindTeammates.App\bin\x64\Release\net8.0-windows10.0.19041.0\win-x64\FindTeammates.App.exe` |
| 参考 bind 旁证 | `exe-bind-6c6b0b0-g2.txt`（G-ROLL 旁证；本批复用同 tip／SHA／size） |

启动前核：`TIP_SHA.txt`／`git rev-parse HEAD`＝FULL tip；exe size＋SHA256 与上表一致 → 记 `BIND_MATCH=True`。任一不符 → **STOP**，不测。

OTP（mock）：`13800000001`／`123456`（与既有 mock 人测包一致）。优先**真人手操**合法进球；探针／预置／强制入袋若使用须单列，**不得**冒充 G1–G5 PASS。

---

## 1 · 用户原令（必须 verbatim 遵守）

确认按 A＋C＋E 执行，仅开展 6c6b0b0 的 PC mock A17 最小验收，不授权改码。条件：

1. G1–G5 为本批必测。G2 必须实际发生一次母球入袋，验证其不进入收球槽；仅截图显示槽内没有白球不算通过。
2. G3 至少覆盖 3 个目标球入槽，逐一核对球号，无漏球、重复或重叠；停球、换手后再次检查不重复追加。
3. G4 必须记录实际入袋先后并与槽序逐项对照，不能按球号排列冒充事件序。若未覆盖同杆多球入袋，要明确保留该覆盖缺口，不宣称全部顺序场景通过。不选「有限PASS／可不逐杆对序」。
4. G5 必须保留「旧局槽内有球→进入新局→空槽」证据。正文「可选新局清空」改为必测；不需要为此恢复合法黑八胜终测。
5. 回置未触达记未测，重连本批后置（A17-07 后置）。旧行号不当成本头已核证据，可暂不补；本批结束只判定已覆盖项目，不直接宣布 A17 全量关闭。

发现失败先交证据和问题清单，再决定是否修复。G-ROLL 保持关闭，不派 Codex、不改物理参数、不合 main、不接真服、不换皮。

---

## 2 · 步骤与通过标准（G1–G5）

### 预步 P0 · 环境

1. BIND 核过 → 启 Release mock → 登录 → 匹配进局。
2. 开局空槽截帧（`a17-g0-empty-slot-start.png`）。
3. 开连续录屏（建议覆盖整批 G1–G5；允许分段但须时间戳可拼）。

### G1 · 合法目标球入袋 → 槽位填入（A17-01）· **必测**

| 操作 | 通过 | 失败 |
|---|---|---|
| 手操瞄准拉杆，打进 ≥1 颗**合法目标球** | 入袋后底栏收球槽出现对应球号／芯片；截帧＋录屏含该杆 | 入袋后槽无填入／填错号／无可见芯片 |

证据：`a17-g1-pocket-in.png`（入袋瞬间或紧随）＋`a17-g1-slot-fill.png`（槽位特写）。

### G2 · 母球入袋 → 不进收球槽（A17-02）· **必测**

| 操作 | 通过 | 失败／不足 |
|---|---|---|
| **必须实际发生一次母球（白球）入袋**（刮库／自杀杆／自由球后误进等均可，注明情境） | 母球入袋过程可见；收球槽**始终无白球芯片**；对照母球入袋前／后槽位帧 | **仅**截图显示「槽内没有白球」、但本局从未发生母球入袋 → **不算通过**；母球芯片入槽 → FAIL |

证据：`a17-g2-cue-pocket-event.png`（母球入袋瞬间）＋`a17-g2-slot-no-cue.png`（紧随槽位）＋录屏片段标出母球入袋时刻。

### G3 · ≥3 目标球入槽 · 无漏／无重／无重叠（A17-03）· **必测**

| 操作 | 通过 | 失败 |
|---|---|---|
| 继续手打至槽内至少 **3** 个目标球；逐一核球号 | 球号与入袋集合一致；无漏球、无重复占位、无明显重叠 | 漏号／同号双占／重叠难辨 |
| 停球后、以及换手后再看槽 | **不**因停球／换手重复追加已入槽球 | 停球或换手后多出重复芯片 |

证据：`a17-g3-slot-ge3.png`；在 pocket-order log 中列出 ≥3 球号；停球／换手后再截一帧 `a17-g3-slot-after-rest-or-handoff.png`。

### G4 · 入袋事件序 ↔ 槽序逐项对照（A17-04）· **必测**

| 操作 | 通过 | 禁止／失败 |
|---|---|---|
| 边打边记「实际入袋先后」（事件序）；停稳后读槽内从左到右（或产品定义方向）顺序 | 事件序与槽序**逐项一致** | **禁止**按球号大小排列冒充事件序；**禁止**「有限PASS／可不逐杆对序」 |
| 同杆多球入袋 | 若本批打到：按实际入袋先后记入表并对照 | 若**未**覆盖同杆多球：在结论中**明确保留覆盖缺口**，**不宣称**全部顺序场景通过 |

证据：填下方「入袋先后／槽序对照表」＋对应帧／录屏时间码。

### G5 · 旧局有球 → 新局 → 空槽（A17-06）· **必测**

| 操作 | 通过 | 说明 |
|---|---|---|
| 旧局槽内已有 ≥1 球（G1／G3 即可）→ 进入新局（再来／回大厅再开／结算后再开，注明路径）→ 核新局空槽 | 证据链完整：**旧局槽有球帧 → 进入新局动作 → 新局空槽帧** | **必测**（原「可选新局清空」已改）；**不需要**为此恢复合法黑八胜终测；Mock 全员准备限制须注明，但空槽本身仍须核 |

证据：`a17-g5-old-slot-occupied.png` → `a17-g5-enter-new-match.png`（或录屏时间码）→ `a17-g5-new-empty-slot.png`。

### 附 · 回置／重连／行号（本批口径）

| 项 | 口径 |
|---|---|
| 回置移除（A17-05／G6） | 本局若触发回置：截「回置前槽有该号 → 回置后槽无该号」。**未触达＝记未测**，不冒充 PASS，不挡本批已覆盖项判定 |
| 重连（A17-07／G7） | **本批后置**；不测、不宣称通过 |
| 旧行号／实现钉（G8） | **可暂不补**；不当成本头已核证据 |

---

## 3 · 证据清单（交付前自检）

### 3.1 win-verify 字段（建议表头）

| 字段 | 填写 |
|---|---|
| Tag | `phase1-pc-wave7-a17-pocket-rail-min-accept-6c6b0b0` |
| Machine | （PC 主机名／id） |
| Recorded (Asia/Shanghai) | 起止时间 |
| tip FULL／short | `6c6b0b0…`／`6c6b0b0` |
| exe SHA256／size | 与 BIND 一致 |
| BIND_MATCH | True／False |
| API mode | mock |
| G1–G5 各结论 | PASS／FAIL／未测（仅回置可未测） |
| 同杆多球覆盖 | 有／无；若无＝**覆盖缺口保留** |
| Product 全量关闭 | **否**（本批 ≠ A17 全量关闭） |
| Code change／Codex | 无／未派 |

### 3.2 帧／录屏建议名

| 文件 | 用途 |
|---|---|
| `phase1-pc-wave7-a17-min-accept-6c6b0b0.mp4`（或分段） | 主录屏 |
| `a17-g0-empty-slot-start.png` | 开局空槽 |
| `a17-g1-pocket-in.png`／`a17-g1-slot-fill.png` | G1 |
| `a17-g2-cue-pocket-event.png`／`a17-g2-slot-no-cue.png` | G2 |
| `a17-g3-slot-ge3.png`／`a17-g3-slot-after-rest-or-handoff.png` | G3 |
| `a17-g4-slot-order.png` | G4 槽序特写 |
| `a17-g5-old-slot-occupied.png`／`a17-g5-enter-new-match.png`／`a17-g5-new-empty-slot.png` | G5 |
| `exe-bind-6c6b0b0-a17.txt` | 本批 BIND 快照 |

### 3.3 入袋先后／槽序对照表模板（G4 必填）

| # | 录屏时间码 | 事件（实际入袋） | 球号 | 同杆多球？ | 此刻槽序（左→右或注明方向） | 与事件序一致？ |
|---|---|---|---|---|---|---|
| 1 | | 目标球入袋 | | 否／是（第 n／m） | | Y／N |
| 2 | | | | | | |
| 3 | | | | | | |
| … | | （含一次母球入袋行，槽应**无**白） | 白／0 | | （槽内不应出现白） | |

结论行：事件序对照＝PASS／FAIL；同杆多球覆盖＝有／**缺口保留**。

---

## 4 · FAIL 处理

1. **立即停改码冲动**：不授权改码、不派 Codex、不改物理参数。
2. 交付：**证据**（帧／录屏／对照表／BIND）＋**问题清单**（现象、复现步骤、期望 vs 实际、影响 Gx）。
3. 由产品／PM 决定是否开修复闸；本执行稿**不**附实现方案。

---

## 5 · OUT／禁项

| OUT／禁 | 说明 |
|---|---|
| 改码／派 Codex | 禁 |
| 改物理／μγ／合 main | 禁 |
| 接真服 | 禁 |
| 换皮／槽壳材质 | 禁 |
| G-ROLL 重测／重录 | 禁（保持关闭） |
| 合法黑八胜终测 | 不恢复；G5 不依赖 |
| A17-07 重连 | 本批后置 |
| 旧行号补核 | 可暂不补 |
| PR#76 demo 当 PASS | 禁 |
| 「有限PASS／可不逐杆对序」用于 G4 | **禁** |
| 宣称 A17 全量关闭／全部顺序场景通过（在同杆多球未覆盖时） | **禁** |

---

## 6 · 交付物路径建议（`billiards-playability`）

| 交付 | 建议路径 |
|---|---|
| win-verify 汇总 | `/workspace/billiards-playability/phase1-pc-wave7-a17-pocket-rail-min-accept-6c6b0b0-win-verify.md` |
| 主录屏 | `/workspace/billiards-playability/phase1-pc-wave7-a17-min-accept-6c6b0b0.mp4` |
| 帧目录／zip | `/workspace/billiards-playability/_a17-min-accept-6c6b0b0/` 或 `…-evidence.zip` |
| pocket-order log | 可内嵌 win-verify，或 `phase1-pc-wave7-a17-min-accept-6c6b0b0-pocket-order-log.md` |
| BIND 快照 | `/workspace/billiards-playability/exe-bind-6c6b0b0-a17.txt` |
| 问题清单（若 FAIL） | `/workspace/billiards-playability/phase1-pc-wave7-a17-min-accept-6c6b0b0-problems.md` |
| 手递副本 | `/workspace/billiards-playability/_github-handoff-ceshi-1-1/测试1.1/`（测完再推证） |

Win 侧 shots 建议目录：  
`...\hayo-pc-6c6b0b0-win-runtime\shots-a17-pocket-rail-min-accept-6c6b0b0\`

---

## 7 · 页脚

**本批＝G1–G5 最小验收 @ tip `6c6b0b0` mock Release。**  
**结束 ≠ A17 全量关闭；≠ 合 main。失败＝证＋问题清单。不派 Codex、不改码、不改物理、G-ROLL 关闭。**

*人测／PC 执行稿 · 2026-11-03 Asia/Shanghai · A＋C＋E*
