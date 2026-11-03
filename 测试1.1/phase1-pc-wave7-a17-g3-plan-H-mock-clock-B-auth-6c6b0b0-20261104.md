# A17 G3 · H-短3 后 **B 最小 mock 延钟写码**授权钉 · tip 父锁 `6c6b0b0` · 2026-11-04 Asia/Shanghai

> **状态｜OPEN／PM 硬派＝开闸** · 2026-11-04 Asia/Shanghai  
> **本令＝限界写码**（隔离补丁＋静态／编译核验）。**本令不重跑 H／不空清席／不叫人打。**

| 项 | 内容 |
|---|---|
| 来源 | **PM 硬派明文／Codex B**；advice `测试1.1/phase1-pc-wave7-a17-g3-plan-H-tight-short3-next-codex-advice-20261104.md` SHA **`6b9a5fef19bbf3b2f7d72079014b9260800816f12eee474abced3010008d9edc`**／handoff **`63f5b4e`**；对照裁 SHA **`045fd911e07c20bd9cc383ad869dbb7685ffbf367fbbe66e9f94c00ef06c61b5`**／handoff **`9a883d7`** |
| 前轮结论 | H-短3＝**FAIL／SHORT_OF_3_HUMAN_VERIFIED（FLIPPED_SHORT）**；COUNTABLE_N＝**0**；维持 G3 FAIL／A17 开 |
| 执行 | **Codex工具人** · 本机 Codex CLI · **gpt-6.1-sol · Ultra**（禁 Composio 冒充） |
| Tip 父锁 | tip `6c6b0b0` FULL `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`；**叠提交**出隔离补丁；交包后**另列**候选 tip／exe SHA／BIND（**不升头／不合 main**） |
| 写码限界 | 仅 `clients/pc/src/FindTeammates.App/` 下：`Services/ApiClientSettings.cs`、`Services/Billiards/BilliardsActionClock.cs`、`Views/BilliardsMatchPage.xaml.cs` |
| 行为 | mock 延钟：开关**关**＝原 **30s**；开关**开**＝mock 专用 **120s**，且**显示与超时同源**；核实／复用 `FINDTEAMMATES_BILLIARDS_HOTSEAT=0` 生效 |
| 不改 | 球权／物理／槽·Hint／计数口径；G1–G5 规则文案；服务端 |
| 禁 | **重跑 H**／空清席／叫用户开打／烟测／升头／合 main／真服／黑八胜／换皮实施；G-ROLL **关**；物理 C **停**；TE-MIN **不重开** |
| 保留 | A17 **开**；G3 FAIL 维持至另裁；G-ROLL **关** |

## 交付（本令＝写码核验，非人打）

1. 限界 diff／说明：三文件改动要点；开关名／默认关；关＝30s／开＝120s；显示与超时同源证明  
2. `FINDTEAMMATES_BILLIARDS_HOTSEAT=0` 核实说明（何处读、默认／强制路径）  
3. **静态／编译核验**通过日志（本机 build；失败则 BLOCKED 原因）  
4. 交包后候选：新 tip SHA（若有）／exe SHA／size／BIND 期望值（**明文未升头／未合 main**）  
5. 写入 handoff `测试1.1/` 并回 SHA＋commit；抄产品＋PM

## 产品下一闸（预告，本令不做）

补丁交齐后：产品另出**隔离核验令**（编译／开 mock／钟显示 120；**仍不重跑 H／禁空清**）。再开 H 须另令。

## 生效

**本令已生效＝OPEN。** PM 硬派 B 明文；Codex 按限界写码核验；确认前产品不自派 H／空清。
