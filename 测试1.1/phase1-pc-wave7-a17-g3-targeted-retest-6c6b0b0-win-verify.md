# A17 G3 定向补测 · win-verify · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 字段 | 值 |
|---|---|
| Role | **G3 定向补测（用户经 PM 授权）** — 仅 G3；**未改码／未升头／未合 main／未派 Codex** |
| Verdict | **BLOCKED**（环境不可达；未开跑 Mock） |
| Tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（短 `6c6b0b0`） |
| parent | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| exe BIND 目标 | SHA256 `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` · size **272384** · mock＋HOTSEAT |
| BIND 文件 | `exe-bind-6c6b0b0-a17.txt`（先验 A17 钉死；本轮未重绑／未触 exe） |
| 授权要点 | 同局 ≥3 互异编号目标球正常入袋；**独立测试环境，不占用用户电脑**；须交逐笔入袋时间／球号／槽内球号／最终数组＋连续录屏；预置／注入单列；无法完成→**BLOCKED** |
| G1／G2／G4／G5 | **保留**既有 PASS 标签（本轮未重测） |
| A17 最小包 | **仍开／未关** |
| G-ROLL | **保持关闭** |
| PC 裁定 | **不**冒充 product PASS／FAIL；本文件＝环境 BLOCKED 卷宗 only |

---

## 0 · 一句话

授权要求 **独立 Windows 测环境且不占用用户电脑**；当前登记桌面仅有用户机「安静的电脑」（`a8697f40-…`），且 **离线**；本助手 box 为 **Linux**，无法启动 WinUI3 BIND exe。按授权「无法完成→BLOCKED」收口，**未**在用户机开窗、**未**空录、**未**假造入袋表。

---

## 1 · 环境检查（本轮）

| 检查 | 结果 |
|---|---|
| ListMachines 桌面 | 仅 `安静的电脑` / `a8697f40-d1d2-4f9b-a183-5f06c4944b2b` · **connected=false** |
| 其它 Windows 机／独立云 worker | **无** |
| 本 box OS | Linux `grok-bot-vm-…` · **无** wine／无 WinUI3 运行时 |
| BIND exe 路径（先验） | 用户机 `...\hayo-pc-6c6b0b0-win-runtime\...\FindTeammates.App.exe` — 属用户电脑工作区 |
| 占用用户电脑 | **授权禁止**（「独立测试环境，不占用用户电脑」） |
| 先验同类闸 | 2026-11-01 用户／PM：停占 DESKTOP-OQUR45J；独立 Win 测机未落实前合法胜等项 **BLOCKED**；PR#67 亦曾因无独立 Win 云机标待验证 |

---

## 2 · 未交付项（因 BLOCKED）

| 须交 | 状态 |
|---|---|
| 逐笔入袋时间／球号／槽内球号／最终数组 | **未采集** |
| 同局连续录屏 | **未录** |
| 预置／注入单列 | **N/A**（未开跑；无预置／注入动作） |
| `a17-g3-slot-ge3` 等多芯片帧 | **未拍** |

**不得**用既有 main／g3supp／g3retry 证冒充本轮定向补测结果（那些同局 max object＝1／0／1，且含 rematch 清槽）。

---

## 3 · 定向补测计划（就绪、未执行）

对齐 RCA §5（`phase1-pc-wave7-a17-g3-rca-6c6b0b0-20261103.md`）：

1. 单局坚持至 ≥3 互异 object pocket＋「收球」视觉确认；`eventBalls.Count < 3` 时禁用／大幅提高 `NOFIRE_STREAK → rematch`。
2. G3 帧入库前不启 G5 rematch。
3. HOTSEAT 保可合法进袋座位；分花色后只瞄合法花色。
4. PASS 证据闸：同 round pocket-order ≥3；`a17-g3-slot-ge3.png` 可读 ≥3 芯片；休息／换手后同集合复核。
5. BIND 钉 tip `6c6b0b0`／exe `7B6B6B1B…`；不改码；不合 main。

**阻塞解除条件（产品／PM／用户）：** 提供已连接的 **独立 Windows 测机**（非用户日常机，或用户书面改令允许占用「安静的电脑」并使其在线）后，方可按上表开跑。

---

## 4 · 标签维持

| 项 | 状态 |
|---|---|
| G3 | **FAIL／未完成维持**（本轮未覆盖；非新证翻盘） |
| G1／G2／G4／G5 | **保留 PASS** |
| A17 | **未关** |
| G-ROLL | **关** |
| tip／BIND | **未升头／未重编** |

---

## 5 · 交产品

本文件＝G3 定向补测 **BLOCKED** 卷宗。请产品裁：是否另配独立 Win 测机、或改令允许用户机、或维持 A17 开／G3 阻断。PC 停手等下一硬派。
