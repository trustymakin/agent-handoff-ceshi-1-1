# A17 G3 本地定向 · 证包索引＋未达≥3 原因分析 · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 项 | 内容 |
|---|---|
| 角色 | PC **只读补齐**：本次录像／逐球记录索引 ＋ 未达≥3 原因分析；**不改码／不开下一轮／不冒充产品方案** |
| 用户定 | A｜先交证＋方案；G3 维持 FAIL；A17 开；更稳同局补测方案 **由产品出**（须写明是否测试辅助／是否改码或数据）；**用户确认前不开下一轮** |
| 产品已裁 | G3 本地定向＝**FAIL**（同局 max=2＜3）；合规未 rematch／未 inject |
| Tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（短 `6c6b0b0`） |
| BIND | exe SHA256 `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` · size **272384** · BIND_MATCH=**True** |
| 机 | `DESKTOP-OQUR45J`／`a8697f40-d1d2-4f9b-a183-5f06c4944b2b` |
| 主 win-verify | `phase1-pc-wave7-a17-g3-targeted-local-6c6b0b0-win-verify.md` SHA256 `B8A6212361B5C2BBA9646EAA574D329910CFCD76975EE507ED9FA6D4AF6F0B64` |

---

## 1 · 本次证包索引（录像＋逐球）

### 1.1 逐球记录（同局 round=1）

来源：`pocket-order-log-g3-targeted-local-6c6b0b0.md` SHA256 `29E1EEBE62D8916693AF937DD3F9835C9CC3139F97AE0B039054068D8AEB6616`

| # | 墙钟 Asia/Shanghai | mp4t（harness 自启钟） | event | 球号 | 槽内累计（event cum） | 帧 |
|---|---|---|---|---|---|---|
| 1 | 2026-11-03 **19:29:10** +08:00 | 21:25 | object_pocket | **#5** | `5` | `frames/a17-g3-slot-after-1.png` SHA `F0DA3CAC…0352` |
| 2 | 2026-11-03 **20:00:24** +08:00 | 52:39 | object_pocket | **#2** | `5,2` | `frames/a17-g3-slot-after-2.png` SHA `4C48A0E9…3AED` |
| 3 | 2026-11-03 **20:19:28** +08:00 | 71:43 | cue_scratch | — | `5,2` | end `frames/a17-g3-slot-ge3.png` SHA `22D29C3E…B322`（槽仍仅两芯片，非≥3） |

- 最终数组 `eventBalls=[5,2]` · count=**2** · `G3_PASS=False`
- rematch_used=**False** · inject_used=**False** · rounds=**1** · shots=**70**
- 分彩旁证：#5 入袋后 Hint「分彩 solid」；LeftSuit 全色 余 6→#2 后再余 5；RightSuit 花色全程余 7（本局未进花色目标球）

### 1.2 录像（连续分段；未拼接成单卷）

| 段 | 路径 | SHA256 | size | 墙钟覆盖（约） | 备注 |
|---|---|---|---|---|---|
| primary | `phase1-pc-wave7-a17-g3-targeted-local-6c6b0b0.mp4` | `1896E52AFC019ACB89FA11B614A6919B1B769AE1DE2A17C9C76191D280508367` | 11795838 | 19:07:45–~19:27:45 | harness `-t 1200`；**未盖住** #5/#2 入袋时刻 |
| cont2 | `_a17-g3-targeted-local-6c6b0b0/…-cont2.mp4` | `B81F25BB5841C4DF1D04B5B342BAE4AA2AF38F879D87F82AAC0FF6B18FAD6CD6` | 2359344 | 19:32:45–19:43:37 | Soft-Refresh 小窗；#5 在 primary 结束与 cont2 之间短间隙（有帧＋Hint 证） |
| cont3 | `_a17-g3-targeted-local-6c6b0b0/…-cont3.mp4` | `470505EC5D535FC08DF2B7393890EAE24E9694C4E672B312061D2FA5E7E8607D` | 7309903 | 19:44:35–~20:09:35 | **含 #2 入袋**墙钟窗 |
| evidence zip | `phase1-pc-wave7-a17-g3-targeted-local-6c6b0b0-evidence.zip` | `092A335BF73545C792A6DB268D76D0ACDB22EB4220EBB94628BF93A14DFA15BF` | — | — | 含 bind／logs／frames／scripts 等 |

**录屏缺口（诚实钉死，非剪辑造假）：** 单文件未覆盖全程；入袋以 pocket-order＋Hint／帧为主证，分段 mp4 为同局连续旁证。下一轮产品方案若要求「单卷全程 continuous」，须单列录制时长／分段策略。

### 1.3 其它钉

| 文件 | SHA256 |
|---|---|
| bind | `7D0909DE7CC45921FF3215C0485750ED5C35A7B02C4237DA9B63104FAB10FCCE` |
| verdict txt | `60ED19A6327DB76612BDD3C59B4A5779AE078C991FF54D7AE134CD9C7B75D243` |
| auth nail local-desktop | `42FEAB5B175296C25EA8060CB691D7C2894846C740A0604A680C288CE1BD5F6B` |
| 日志 | `_a17-g3-targeted-local-6c6b0b0/logs/launch-console-…`／`harness-stdout.txt` |

---

## 2 · 未达≥3 原因分析（PC 观察；供产品写方案）

### 2.1 主因（钉）

**仍是同局目标球入袋覆盖不足（②），不是已证「≥3 已入袋但收球槽漏显／覆写」（①）。**

证据：70 杆同局、禁 rematch，object_pocket 仅 2 次（#5、#2）；视觉槽两芯片与 event cum 一致；从未出现第三颗互异目标球入袋事件，故多芯片轨 UI **仍未测到**。

### 2.2 贡献因子（按权重）

| # | 因子 | 证 |
|---|---|---|
| 1 | **合法进袋率极低** | 70 shot 仅 2× OBJECT_POCKET；大量「空杆／先碰非己方／母球进袋」→ 自由球交接，日志多次 `犯规：…→换手+自由球` |
| 2 | **HOTSEAT 代打占时长** | 分花色后长时间 `轮到 对手B1 · 本机代打`；B1 侧亦多犯规，A1 有效瞄准窗被切碎 |
| 3 | **分花色后只剩全色可进** | #5 solid 后全色余 6；#2 后再余 5；花色余 7 未动——合法目标集合变窄，目录瞄准未显著抬升进袋率 |
| 4 | **#5→#2 间隔 ~31 min** | 19:29→20:00 之间仅维持 have=1；说明「禁 rematch」已做到同局累积，但物理进袋仍稀 |
| 5 | **录屏策略次要** | primary 20 min 截断不影响「是否进了第 3 球」的判定（日志／帧已证只有 2）；但削弱「单卷目视」体验 |

### 2.3 已排除／未支持

| 说法 | 本轮 |
|---|---|
| rematch 清槽导致跨局假累积 | **否**（rematch=False，rounds=1） |
| inject／预置冒充 PASS | **否** |
| 已有 ≥3 入袋但槽 UI 丢球 | **无事件** → 不能翻① |
| BIND／错 tip | **否**（BIND_MATCH=True） |

---

## 3 · 给产品写「更稳同局补测方案」的输入（PC 不立项、不开跑）

产品方案文内须自书：**是否测试辅助**、**是否改码或数据**；**用户确认前 PC 不开下一轮**。下列仅为观察选项，**非**硬派：

| 方向 | 说明 | 辅助？ | 改码／数据？ |
|---|---|---|---|
| A. 加长同局＋改进瞄准目录／功率近袋 | 仍真实物理；提高 ≥3 概率 | 测具策略，通常否产品码 | 否码；或否 |
| B. 人辅／半自动指定合法球近袋轻打 | 加速覆盖 | **是**测试辅助 → 须单列 | 否码 |
| C. Mock 预置／开局多球已近袋或强制 pocket 事件 | 最快验多芯片轨 | **是** inject → 须单列，不得混正常 PASS | 或需 **数据／mock 钩子**（产品裁是否算改数据） |
| D. 改收球轨实现后再测 | 仅当①被证明 | — | **改码** → 须 Codex 闸 |

PC 建议产品方案至少写清：成功闸（同局≥3＋帧）、禁 rematch、录屏是否要求单卷全程、辅助／inject 单列规则、是否动 tip／exe。

---

## 4 · 状态

| 项 | 状态 |
|---|---|
| G3 | **FAIL 维持** |
| A17 | **开** |
| G-ROLL | **关** |
| 改码／升头／合 main／Codex | **否** |
| 下一轮 | **不开**；等产品方案＋用户确认后再硬派 |

本文件＝证包索引＋原因分析交产品；PC 停手。
