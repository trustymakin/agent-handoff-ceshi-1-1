# 产品裁 · A17 G3 定向补测 · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 项 | 内容 |
|---|---|
| 角色 | 产品核验整理；**未改码／未派 Codex／未重测** |
| 授权 | 仅 G3 定向补测；独立环境不占用户电脑 |
| Tip／BIND | 目标 tip `6c6b0b0`／exe `7B6B6B1B…` size 272384（本轮**未重绑／未开跑**） |
| **正式卷宗** | `phase1-pc-wave7-a17-g3-targeted-6c6b0b0-win-verify.md` · SHA256 **`CBADD598639EF49029B70880FB0BA8D8B58399F7BD151403918BD964B72A9AF6`**（本机核 ✓） |
| 先到卷宗 | `phase1-pc-wave7-a17-g3-targeted-retest-6c6b0b0-win-verify.md` · `D88BCB7A…C0E6`（同结论；正式名以硬派交付名为准） |
| 阻塞码 | **`ENV_BLOCKED_NO_INDEPENDENT_WIN`** |

## 产品结论

**总体＝BLOCKED（环境不可达），≠ PASS／≠ FAIL 翻盘。**  
独立 Win 测机未落实；「安静的电脑」离线；box＝Linux 无法跑 WinUI3。PC **未开跑／未空录／未假造入袋表／未占用户电脑**——裁定合规。

| 项 | 裁 |
|---|---|
| G3 定向补测 | **BLOCKED**（未覆盖） |
| G3 标签 | **FAIL／未完成维持**（无新证翻盘；未翻①） |
| G1／G2／G4／G5 | **保留**本批 PASS |
| A17 | **继续未关** |
| G-ROLL | **保持关** |
| 改码／升头／合 main | **未授权／未发生** |

**实现缺陷 vs 覆盖不足：本轮仍无法二分**；维持 RCA 主判②直至定向补测实际开跑。

## 解除阻塞（用户已定 **A** · 2026-11-03 ~18:13 Asia/Shanghai）

用户经 PM 选 **A**：先确认**独立 Windows 测机及运行条件可用**，再安排 G3 定向补测。  
站立令全文：`phase1-pc-wave7-a17-g3-user-choice-A-independent-win-20261103.md`。

| 项 | 现态 |
|---|---|
| 独立 Win | **未就绪**（ListMachines 仅用户机 `DESKTOP-OQUR45J` connected；禁占） |
| 动作 | **维持阻断**；产品盯测机；就绪后硬派 PC |
| 改令占用户机／维持永久阻断 | **未选** |

## 禁项钉

不派修复／不改码／不升头／不合 main／不接真服／不黑八胜／不换皮；G-ROLL 关；**不占用户电脑**。

**≠ 开跑；等独立 Win 就绪信号后再硬派。**
