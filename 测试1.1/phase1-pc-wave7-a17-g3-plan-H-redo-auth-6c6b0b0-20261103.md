# A17 G3 · 方案 H **重做**授权钉 · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 项 | 内容 |
|---|---|
| 来源 | 用户经 PM 选 **A＝重做 H**；前轮产品裁 `phase1-pc-wave7-a17-g3-plan-H-6c6b0b0-product-cut-20261103.md` SHA `96e010d1…fdd9`＝未通过 |
| 前轮 FAIL 因 | ① gdigrab 空 mdat＋静帧 slideshow；② 入袋多为「对手B1·本机代打」≠人打；③ 槽帧球号与 Hint 不完全同构 |
| 测机 | `DESKTOP-OQUR45J`／`a8697f40-d1d2-4f9b-a183-5f06c4944b2b`（须在线；**须用户坐本机**） |
| Tip／BIND | tip `6c6b0b0` FULL `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`／exe SHA `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` size **272384** mock；BIND 不匹配则停 |
| 打手 | **仅用户本人出杆入袋**；PC **只录不代打**；**禁** HOTSEAT／「本机代打」充数 |
| 目标 | **同一局** ≥3 颗**不同编号**目标球正常入袋；禁 rematch／新局累加 |
| 时限 | 建议墙钟 ≤60 min；未达 ≥3 → 留证停，不盲加时 |
| 禁 | 改码／Codex／升头／合 main／真服／黑八胜／换皮；注入／预置宣称 PASS；自动扫杆 |
| 保留 | G1／G2／G4／G5；A17 **未关**直至本轮产品再裁；G-ROLL **关** |

## 相对前轮必须修的三条（硬门槛）

### 1. 连续全窗实况录像（禁 slideshow）
- 开局**前**起录，至槽复查完停。
- **禁止**空 mdat／48B 空文件／仅静帧拼成的 mp4。
- 交付 mp4 须为**真实连续画面**（肉眼可辨球运动／入袋过程）；ffprobe 时长与墙钟大致吻合，非 11s／1fps 静帧卷。
- 前轮根因参考：ffmpeg gdigrab stderr 无消费者 → 空 mdat。重做须：**有消费者读 ffmpeg 输出**，或改用本机可靠外置录屏（OBS／Win 游戏栏等），**先验 10s 试录**确认非空再开局。
- 可按时长切段，但段间无缝说明；入袋窗不得落在无画面缺口。

### 2. 人打口径（禁「本机代打」充数）
- 用户须坐在 `DESKTOP-OQUR45J` 前；**入袋时刻** TurnPill／日志 **不得**为「对手B1 · 本机代打」（或任何「本机代打」）作为计分入袋。
- 计分入袋必须来自**用户本人拖杆／出杆**的那一手；PC 不点拉杆、不代打、不开自动扫杆。
- 开跑前 PC 与用户对齐：若 HOTSEAT 对手座会自动出杆，须改座／关代打／或用户改打 A 座并确保入袋杆在用户手上——**否则不得开录冲分**。
- 无人到场 → **BLOCKED_NO_HUMAN_PLAYER**。

### 3. 槽帧球号与 Hint 同构可核
- 每颗计分入袋后立刻抓：`slot-after-N`＋`tray-N`（近距可读号）。
- 逐球表球号＝Hint `have` 序＝槽帧目视球号；三者不一致则该球**不计**关闸，继续打到可核的 ≥3。
- 达 ≥3 后：全槽近距＋停稳／换手复核帧。

## 交付清单

1. `phase1-pc-wave7-a17-g3-plan-H-redo-6c6b0b0-win-verify.md`（钉 tip／BIND／machineId／打手到场／试录先验／代打是否出现）
2. 逐球表 `pocket-order-log-g3-plan-H-redo-6c6b0b0.md`（墙钟／球号／入袋序／槽读／TurnPill 文案）
3. **连续实况** mp4（及 SHA）；若切段列齐
4. 槽／tray／rest／handoff 帧；evidence zip＋SHA256SUMS
5. 明文声明：本轮是否出现「本机代打」入袋（有则该球剔除或整轮 FAIL 过程）

## 产品再裁口径（预告）

- Observer Hint 达 3 **≠** 自动 PASS。
- 连续录像／人打口径／球号同构 **任一条不过 → 本轮仍未通过**。
- 达成后方可产品再裁是否关 G3／A17。

## 开跑门闩

1. BIND_MATCH=true  
2. 试录 ≥10s 非空连续画面已核  
3. 用户确认已坐本机且知「禁代打充数」  
4. 再开录开局  

未齐任一条 → 不得开跑；报 BLOCKED 原因。
