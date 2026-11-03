# A17 G3 · 方案 H **收紧再开（B PASS 后／SHORT_OF_3）**授权钉 · tip `37b7aef` · 2026-11-04 Asia/Shanghai

> **状态｜OPEN／PM 硬派＝开闸** · 2026-11-04 Asia/Shanghai  
> **本令＝以 tip `37b7aef`＋MOCK_SHOT_CLOCK=1＋HOTSEAT=0 再开收紧 H 只读取证**（吸收 H-短3＝FLIPPED_SHORT／n＝0；延钟隔离已 PASS）。**写码＝否。**

| 项 | 内容 |
|---|---|
| 来源 | **PM 硬派明文／Codex A**；advice `测试1.1/phase1-pc-wave7-a17-post-b-pass-next-codex-advice-20261104.md` SHA **`aea278e05972a162b18746dcffe488ff2dbbac5303b2227ab431de152182177c`**／handoff **`d77f4da`**；对照裁 `…-mock-shot-clock-120-37b7aef-product-cut-20261104.md` SHA **`57dee76bb61468f3bc2404cdd1a8d725a319d2217ad2e67b874da247a2f6e706`**／handoff **`5f7e2b7`** |
| 前轮结论 | H-短3＠`6c6b0b0`＝**FAIL／SHORT_OF_3_HUMAN_VERIFIED／FLIPPED_SHORT**（COUNTABLE_N＝0）；B 隔离核验＠`37b7aef`＝**PASS**（钟≈30／≈120＋递减为主证；「超时到0」未坐实**不**升本令前置）；**≠ G3 PASS／≠ 关 A17**；**本令不写码** |
| 测机 | `DESKTOP-OQUR45J`／`a8697f40-d1d2-4f9b-a183-5f06c4944b2b`（须在线；**须用户本人坐本机开打**） |
| Tip／BIND | tip **`37b7aef`** FULL **`37b7aefd25ec67e289097a801e95289b02a39eee`**／exe SHA **`C274B9747C957D16DAD21538DB16846EA4F836CC5371ADE7C9E9BA9D112E8600`** size **272384**；对照 `exe-bind-37b7aef-mock-shot-clock.txt`；**BIND 不匹配则停**；**禁升头／禁合 main** |
| 环境 | PowerShell **同进程**启客户端：`FINDTEAMMATES_API_MODE=mock`；`FINDTEAMMATES_BILLIARDS_HOTSEAT=0`；`FINDTEAMMATES_BILLIARDS_MOCK_SHOT_CLOCK=1`（行动钟≈**120s**） |
| 打手 | **仅用户本人**出杆入袋；**代打不计**；PC **只录不代打**；**禁** HOTSEAT／「本机代打」充数；**禁自动扫杆**；**禁 rematch 累加跨局**；**禁空清席循环** |
| 目标 | **同一局** ≥3 颗**三证一致**本人可核入袋（TurnPill＝轮到你*／代打＝false／Hint `进袋[N]`／**立刻** in-play `slot-after-N`＋`tray-N` 目视同构） |
| FLIP | 翻「本机代打」＝截断；该窗入袋**一律不计**；**不补算**；须再清席至本人席后方可续计（**仅按产品／PM 令**；禁自开空清循环） |
| 证据不足 | **维持 G3 FAIL／A17 开**；**不自动续轮** |
| 禁 | **写码**／烟测／换皮实施／合 main／真服／黑八胜／升头；空清席循环；注入／预置宣称 PASS；自动扫杆；G-ROLL **维持关**；物理 C **停**；TE-MIN **不重开** |
| 保留 | G1／G2／G4／G5；**A17 开直至再裁**；G-ROLL **关** |

## 流程硬序（不得颠倒）

1. **BIND_MATCH**＝true（tip／exe／size 锁上表；环境三变量已设；不匹配停）  
2. **试录 PASS**（≥10s **非空连续**全窗；禁空 mdat／slideshow；试录 **不得**顶替正式 REC）  
3. 正式 **REC／观察器 ACK 墙钟**（全窗连续实况已启并 ACK）  
4. **开打前确认代打＝关**（TurnPill／席位非「本机代打」；必要时清席／✕→离开再来一局→匹配至本人席——**一次到位，禁空清循环**）  
5. PC 就位先报产品＋PM（含上四条墙钟＋ClockText≈120）→ **产品／PM 再叫用户本人开打**  
6. 人打中：**每球立刻**截 in-play `slot-after-N`＋`tray-N` 并核 Hint；代打窗入袋**一律不计**；FLIP 截断不补算

未齐门闩 → **不得**叫用户开打；报 BLOCKED 原因。

## 三条硬门槛（收紧）

### 1. 连续全窗实况
- 正式 REC 须在用户开打**前**已 ACK；收证前保持全窗连续。  
- 禁空 mdat／slideshow；ffprobe 时长与墙钟大致吻合。

### 2. 人打口径（开打前代打＝关＋延钟）
- **开打前**须核：非「本机代打」席／TurnPill＝轮到你*（或等价本人席）；ClockText／行动钟≈**120**。  
- 计分入袋时刻不得为「对手B1 · 本机代打」或任何「本机代打」。  
- PC 不点拉杆、不代打、不开自动扫杆、**不自开 rematch／不空清循环**（清席仅按产品／PM 令）。  
- 无人到场 → **BLOCKED_NO_HUMAN_PLAYER**。

### 3. 槽帧＝Hint 同构（每球立刻）
- **每颗**拟计分入袋后**立刻**抓：`slot-after-N`＋`tray-N`（近距可读号）——**禁止**仅靠事后 HUD／post-hoc 凑数。  
- 三证：Hint 球号＝逐球表＝槽／tray 目视；任一不一致 → 该球**不计**，继续打到可核 ≥3。  
- 达 ≥3 后：全槽近距＋停稳／换手复核帧。

## 开跑门闩

**BIND_MATCH ＋ 试录 PASS ＋ 正式 REC／观察器 ACK ＋ 开打前代打＝关** → PC 就位先报 → **产品／PM 再叫用户开打**。

## 交付清单

1. `phase1-pc-wave7-a17-g3-plan-H-tight-short3-37b7aef-win-verify.md`（钉 tip／BIND／三环境变量／ClockText≈120／machineId／试录／正式 REC·观察器 ACK／开打前代打＝关墙钟／代打是否再现／FLIP 截断说明）  
2. 逐球表 `pocket-order-log-g3-plan-H-tight-short3-37b7aef.md`（墙钟／球号／TurnPill／Hint 原文／slot／tray 路径／COUNT|EXCLUDE）  
3. **连续实况** mp4（完整 SHA）；试录 mp4  
4. **每球** in-play `slot-after-N`／`tray-N` 帧＋达 3 后复核帧；evidence zip＋SHA256SUMS  
5. **明文**：本轮是否出现「本机代打」入袋（有则剔除；过程说明）；是否空清循环（须＝否）  
6. 写入 handoff `测试1.1/` 或交产品路径＋SHA；抄产品＋PM

## 产品再裁口径（预告）

- Observer／自称达 N **≠** 自动 PASS。  
- 连续录像／人打口径／球号同构 **任一条不过 → 本轮仍未通过**。  
- 证据不足 → **维持 G3 FAIL／A17 开**，**不自动续轮**。  
- 达成后方可产品再裁是否关 G3／A17。

## 生效

**本令已生效＝OPEN。** PM 硬派明文／Codex A；用户不停工。PC 按硬序备测；**就位前不叫用户开打**；**写码否**。
