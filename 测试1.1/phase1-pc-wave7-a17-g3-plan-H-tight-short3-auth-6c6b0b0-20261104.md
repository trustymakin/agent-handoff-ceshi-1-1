# A17 G3 · 方案 H **收紧最小补测（SHORT_OF_3 再开）**授权钉 · tip `6c6b0b0` · 2026-11-04 Asia/Shanghai

> **状态｜OPEN／PM 硬派＝开闸** · 2026-11-04 Asia/Shanghai  
> **本令＝收紧新令**（吸收上轮 SHORT_OF_3 缺口：代打窗＋缺 in-play 槽／tray；**不是**复制上轮 min-retest auth 文件名／正文）。  
> Codex 只读拍板 **A**＝再开一轮 H 收紧；PM 拍板硬派明文；用户不停工。本令确认即开闸。

| 项 | 内容 |
|---|---|
| 来源 | **PM 硬派明文／Codex A**；advice `测试1.1/phase1-pc-wave7-a17-g3-plan-H-short-of-3-next-codex-advice-20261104.md` SHA **`57f64f0a95d7c6e86eb992ff6ea603d1072e80457743415494258de3253c92ec`**；对照裁 `…-plan-H-min-retest-…-product-cut-20261104.md` SHA **`232fc81a9a217abdb379a8388ea682f3ebe795dd118a45268fbaf564ef62392e`**／handoff **`7a18e3f`** |
| 前轮结论 | 最小补测裁＝**FAIL／SHORT_OF_3_HUMAN_VERIFIED**（正式 REC **PRESENT**；可核仅 `[14]` n=1＜3；代打窗剔 5／6／3；in-play 槽／tray **缺**；自称 8 球不作裁据）；**≠ G3 PASS／≠ 关 A17**；**无需先改码** |
| 测机 | `DESKTOP-OQUR45J`／`a8697f40-d1d2-4f9b-a183-5f06c4944b2b`（须在线；**须用户本人坐本机开打**） |
| Tip／BIND | tip `6c6b0b0` FULL `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`／exe SHA `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` size **272384** mock；**BIND 不匹配则停** |
| 打手 | **仅用户本人**出杆入袋；**代打不计**；PC **只录不代打**；**禁** HOTSEAT／「本机代打」充数；**禁自动扫杆**；**禁 rematch 累加跨局** |
| 目标 | **同一局** ≥3 颗**三证一致**本人可核入袋（TurnPill＝轮到你*／代打＝false／Hint `进袋[N]`／**立刻** in-play `slot-after-N`＋`tray-N` 目视同构） |
| 球14 特例 | 上轮已 COUNT 的球 **14**：仅当能从**原正式录像**补齐**当时** in-play 槽／tray 同构才可计入本轮 have；**补不齐 → 本轮须另收满 ≥3**（不可事后槽照凑数） |
| 证据不足 | **维持 G3 FAIL／A17 开**；**不自动续轮** |
| 禁 | **写码**／烟测／换皮实施／合 main／真服／黑八胜／升头；注入／预置宣称 PASS；自动扫杆；G-ROLL **维持关**；物理 C **停**；TE-MIN **不重开** |
| 保留 | G1／G2／G4／G5；**A17 开直至再裁**；G-ROLL **关** |

## 流程硬序（不得颠倒）

1. **BIND_MATCH**＝true（tip／exe／size 锁上表；不匹配停）  
2. **试录 PASS**（≥10s **非空连续**全窗；禁空 mdat／slideshow；试录 **不得**顶替正式 REC）  
3. 正式 **REC／观察器 ACK 墙钟**（全窗连续实况已启并 ACK）  
4. **开打前确认代打＝关**（TurnPill／席位非「本机代打」；必要时清席／✕→离开再来一局→匹配至本人席）  
5. PC 就位先报（含上四条墙钟）→ **产品／PM 再叫用户本人开打**  
6. 人打中：**每球立刻**截 in-play `slot-after-N`＋`tray-N` 并核 Hint；代打窗入袋**一律不计**

未齐门闩 → **不得**叫用户开打；报 BLOCKED 原因。

## 三条硬门槛（收紧）

### 1. 连续全窗实况
- 正式 REC 须在用户开打**前**已 ACK；收证前保持全窗连续。  
- 禁空 mdat／slideshow；ffprobe 时长与墙钟大致吻合。

### 2. 人打口径（开打前代打＝关）
- **开打前**须核：非「本机代打」席／TurnPill＝轮到你*（或等价本人席）。  
- 计分入袋时刻不得为「对手B1 · 本机代打」或任何「本机代打」。  
- PC 不点拉杆、不代打、不开自动扫杆、**不自开 rematch**（清席仅按产品／PM 令）。  
- 无人到场 → **BLOCKED_NO_HUMAN_PLAYER**。

### 3. 槽帧＝Hint 同构（每球立刻）
- **每颗**拟计分入袋后**立刻**抓：`slot-after-N`＋`tray-N`（近距可读号）——**禁止**仅靠事后 HUD／post-hoc 凑数。  
- 三证：Hint 球号＝逐球表＝槽／tray 目视；任一不一致 → 该球**不计**，继续打到可核 ≥3。  
- 达 ≥3 后：全槽近距＋停稳／换手复核帧。

## 开跑门闩

**BIND_MATCH ＋ 试录 PASS ＋ 正式 REC／观察器 ACK ＋ 开打前代打＝关** → PC 就位先报 → **产品／PM 再叫用户开打**。

## 交付清单

1. `phase1-pc-wave7-a17-g3-plan-H-tight-short3-6c6b0b0-win-verify.md`（钉 tip／BIND／machineId／试录／正式 REC·观察器 ACK／开打前代打＝关墙钟／代打是否再现）  
2. 逐球表 `pocket-order-log-g3-plan-H-tight-short3-6c6b0b0.md`（墙钟／球号／TurnPill／Hint 原文／slot／tray 路径／COUNT|EXCLUDE）  
3. **连续实况** mp4（完整 SHA）；试录 mp4  
4. **每球** in-play `slot-after-N`／`tray-N` 帧＋达 3 后复核帧；evidence zip＋SHA256SUMS  
5. 若主张计入上轮球14：须附原录像时间码＋补截的当时槽／tray 同构帧及核验说明；否则明文「球14不计入本轮／本轮另收≥3」  
6. **明文**：本轮是否出现「本机代打」入袋（有则剔除；过程说明）

## 产品再裁口径（预告）

- Observer／自称达 N **≠** 自动 PASS。  
- 连续录像／人打口径／球号同构 **任一条不过 → 本轮仍未通过**。  
- 证据不足 → **维持 G3 FAIL／A17 开**，**不自动续轮**。  
- 达成后方可产品再裁是否关 G3／A17。

## 生效

**本令已生效＝OPEN。** PM 硬派明文／Codex A；用户不停工。PC 按硬序备测；**就位前不叫用户开打**。
