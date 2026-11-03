# 产品裁 · B mock 延钟 **隔离核验** · tip `37b7aef` · 2026-11-04 Asia/Shanghai

| 项 | 内容 |
|---|---|
| 角色 | 产品核验；**未改码／未升头／未合 main** |
| 授权 | verify auth SHA **`724136962ba91c466f2d7450f08b22d7639b7f6bc4db32f0b03fa0008b2be3e1`**／handoff **`ca0a39c`**；写码 auth `9de86e16…`／`5b187e3`；Codex 交付 `9501ddd`／doc SHA `bcce36eb…` |
| tip／BIND | tip **`37b7aef`** FULL `37b7aefd25ec67e289097a801e95289b02a39eee` ←父 `6c6b0b0`；exe SHA **`C274B9747C957D16DAD21538DB16846EA4F836CC5371ADE7C9E9BA9D112E8600`** size **272384**；与父旧 BIND 不同＝重建 OK |
| 分支 | `codex/mock-shot-clock-120-6c6b0b0`；**未合 main**；父 worktree HEAD 未动 |
| win-verify | SHA256 **`ea8165ff912d7b3e809f047cb3ed3a94c56b324912b11f5b8a3b7ad8c12cb602`** ✓ |
| evidence zip | SHA256 **`757270e07774b11d0203f977bc81b7d7ed128ec42f9b9ce611823a994db74d9a`** ✓ |
| 测机 | `DESKTOP-OQUR45J` |

## 产品结论

**总体＝通过（`PASS`）——隔离核验门闩。≠ 关 A17。≠ G3 PASS。≠ 授权再开 H。**

| 项 | 裁 |
|---|---|
| 编译 | **PASS**（Release exit 0） |
| BIND／新 tip 候选 | **PASS**（exe SHA／size 齐；明文未升默认头） |
| 关开关 ≈30 | **PASS**（ClockText 27→14 递减；入局后≈3s） |
| 开开关 ≈120 | **PASS**（ClockText 117→104 递减；贴近 120） |
| 超时撞线到 0 | **短观察未坐实**（未等满 120s；本隔离令以档位＋递减为主证） |
| HOTSEAT=0 | **PASS 短观察**（mock120 窗 dai_da=false／TurnPill＝轮到你） |
| 禁令 | **遵守**（未重跑 H／未空清／未合 main／未升头／未改码） |
| A17／G3 | **维持开／FAIL**（本令不裁人打） |
| G-ROLL／物理 C | **关／停** |

### 说明

- UI 钟面 AutomationId＝`ClockText`（`行动钟 N 秒`）；`ActionClockText` 不存在——与既有脚本一致，产品认。  
- 档位差（≈30 vs ≈120）＋连续递减已证明 mock 延钟接线生效。  
- **再开 H 须另令**；届时 BIND 锁 tip `37b7aef`／exe `C274B974…8600`（或届时重编 SHA）。

## 禁项钉

不重跑 H／不空清／不升头／不合 main／不真服／不黑八胜／不换皮实施／不烟测；G-ROLL 关；物理 C 停；PC 本项停手等另令。

## 下一步（产品不自转用户三选一）

裁后抄 PM；是否以 `37b7aef` 再开收紧 H → **PM＋Codex 拍板后硬派明文**。产品待命出下一 auth，确认前不自派。
