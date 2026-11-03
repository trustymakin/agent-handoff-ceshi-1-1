# A17 G3 定向补测 · win-verify · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 字段 | 值 |
|---|---|
| Role | **产品硬派 · 仅 G3 定向补测**（用户授权）；**未改码／未升头／未合 main／未派 Codex／未派修复** |
| Verdict | **BLOCKED**（独立测试环境不可达；**未**开跑 Mock；**未**强占用户电脑） |
| 授权钉 | `phase1-pc-wave7-a17-g3-targeted-retest-auth-6c6b0b0-20261103.md` |
| Tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（短 `6c6b0b0`） |
| parent | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| BIND exe 目标 | SHA256 `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` · size **272384** · mock＋HOTSEAT |
| BIND 本轮 | **未触 exe／未重绑**（环境未达开跑门槛；先验 `exe-bind-6c6b0b0-a17.txt` 仍钉上述 SHA） |
| G1／G2／G4／G5 | **保留**既有标签；**本批不重测** |
| A17 | **不关闭** |
| G-ROLL | **关** |
| PC 裁定 | **不**冒充 product PASS／FAIL／实现缺陷裁定；本文件＝环境 **BLOCKED** 卷宗 |

---

## 0 · 一句话

硬派要求 **「独立测试环境完成，不占用用户电脑」**；若只能占用户机／无法独立环境 → **BLOCKED**、写清阻塞、**勿强占**。当前无独立 Windows 测机；登记桌面仅用户机「安静的电脑」（`a8697f40-…`）且 **connected=false**；本助手 box 为 **Linux**，无法启动 WinUI3 BIND exe。故按授权收 **BLOCKED**，未开窗、未空录、未伪造 pocket-order／mp4。

---

## 1 · 环境检查（硬派当轮 · Asia/Shanghai ~08:16）

| 检查 | 结果 |
|---|---|
| 独立 Windows 测机／云 worker | **无**（ListMachines 无第二台 desktop） |
| 用户机「安静的电脑」`a8697f40-d1d2-4f9b-a183-5f06c4944b2b` | **connected=false**；且硬钉 **不占用用户电脑** → **不得**作为本轮执行面 |
| 本 box | Linux · **无** WinUI3／无可用 wine 跑 BIND exe |
| BIND 路径（先验 A17） | 落在用户机 `...\hayo-pc-6c6b0b0-win-runtime\...\FindTeammates.App.exe` — 属用户电脑工作区 |
| 强占用户电脑 | **未执行**（授权禁止） |

阻塞句（钉死）：**ENV_BLOCKED_NO_INDEPENDENT_WIN** — 独立测试环境未落实；禁占用户机；用户机亦离线。

---

## 2 · 场景与交付物（本轮均为未采集）

| 须交 | 状态 |
|---|---|
| 同一局 ≥3 互异编号目标球正常入袋 | **未测** |
| 禁中途 rematch／exit+new 清槽凑数 | **N/A**（未开跑） |
| 逐笔：入袋时间／球号／槽内球号／最终数组 | **无** pocket-order 本轮表 |
| 连续录屏 mp4 | **无** |
| 预置／强制注入单列 | **无**（未使用；亦未混称 PASS） |

**不得**把既有 main／g3supp／g3retry 证当作本轮定向补测结果（那些同局 object max＝1／0／1，且含 rematch 清槽）。

---

## 3 · 实现缺陷 vs 覆盖不足

本轮 **未**取得同局 ≥3 入袋新证 → **不能**把主判从 RCA／产品汇总裁的 **② 覆盖缺口** 翻成 **① 实现缺陷**。G3 **FAIL／未完成维持**。

---

## 4 · 解除阻塞（供产品裁）

任选其一后再硬派开跑：

1. 配已连接的 **独立 Windows 测机**（非用户日常占用机），并保证 tip `6c6b0b0` BIND exe 可落在该机；或  
2. 用户／产品 **书面改令**允许占用「安静的电脑」且该机 **在线**。

计划稿仍对齐 RCA §5（单局坚持、禁用 nofire-rematch 清槽、G3 帧入库前不启 G5）。

---

## 5 · 旁证指针（非本轮交付）

| 文件 | 说明 |
|---|---|
| `phase1-pc-wave7-a17-g3-targeted-retest-6c6b0b0-win-verify.md` | PM 授权当轮同结论草稿（SHA `D88BCB7A…C0E6`）；**以本文件为产品硬派正式交付名** |
| `phase1-pc-wave7-a17-g3-rca-6c6b0b0-20261103.md` | 主判② RCA |
| `phase1-pc-wave7-a17-g3-rca-product-cut-6c6b0b0-20261103.md` | 产品汇总裁 |

---

## 6 · 交产品

**VERIFY = BLOCKED**（环境）。无 pocket-order／无连续 mp4。请产品裁下一步。PC 停手；不改码；不合 main；A17 仍开；G-ROLL 关。
