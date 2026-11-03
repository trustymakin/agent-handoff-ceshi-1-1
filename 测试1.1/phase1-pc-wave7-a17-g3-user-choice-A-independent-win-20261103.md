# 用户定 A · G3 解除路径 · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 项 | 内容 |
|---|---|
| 来源 | 项目管理转用户定 **A** |
| 口径 | **先确认独立 Windows 测机及运行条件可用，再安排 G3 定向补测** |
| Tip／BIND | tip `6c6b0b0`／exe `7B6B6B1B…` size **272384** · mock；**不升头／不重编除非 BIND 失配另议** |
| 场景（就绪后） | 同局 ≥3 不同目标球入袋；连续记录入袋球号与槽内球号；核对停球／换手后状态；提前明确异常→立即留证 |
| 测机未就绪 | **维持阻断**；**不占用户电脑**；不授权改码；不派 Codex |
| G3 | **FAIL 记录保留**＋注明**覆盖不足／原因未最终确认** |
| A17 | **未关** |
| G-ROLL | **关** |
| 闸 | 不合 main／不升头／不真服／不黑八胜／不换皮 |

## 测机就绪判据（产品盯）

1. 存在**独立于用户日常机**的 Windows 测机（≠ 仅 `DESKTOP-OQUR45J`／「安静的电脑」占用户机）  
2. 该机**已连接**且可跑本 BIND WinUI3 exe  
3. PC 书面确认环境可用后，由产品**硬派**定向补测（沿用授权钉场景）

## 本轮盘点（2026-11-03 ~18:13 Asia/Shanghai）

| 源 | 状态 |
|---|---|
| ListMachines 桌面 | 仅 `DESKTOP-OQUR45J` **connected**（判＝用户机路径，**不得**作独立 Win） |
| iOS 机 | 与本项无关 |
| box | Linux，无法跑 BIND |
| 独立 Win 测机 | **未登记／未连接 → 未就绪** |

**裁定：继续 `ENV_BLOCKED_NO_INDEPENDENT_WIN`；不硬派 PC 开跑。**

依据原授权钉：`phase1-pc-wave7-a17-g3-targeted-retest-auth-6c6b0b0-20261103.md`；正式 BLOCKED 卷宗 SHA `CBADD598…9AF6`。
