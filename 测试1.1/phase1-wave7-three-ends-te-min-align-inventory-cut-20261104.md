# Wave7「三端对齐」· TE-MIN v2 只读盘点裁 · 2026-11-04

| 项 | 内容 |
|---|---|
| 角色 | 产品经理助手 · **只读盘点裁**（ALIGN inventory cut） |
| 授权 | PM 拍板 **A**＝确认 TE-MIN v2 范围及只读盘点；scope SHA `97ac5d67f2a8a489f8c7a009b0088bf51104079c1a53d41598c54e16f569c8eb`／handoff `4ef729a` |
| 本轮 | **仅**文档／证据索引盘点；**不开** T1／T4 烟测；不改码／不合 main／不真服／不黑八胜／不换皮／不升头／不派 PC／安卓／iOS 跑测／不派 Codex 写码 |
| 范围锚 | `phase1-wave7-three-ends-alignment-acceptance-scope-20261104.md`（TE-00～TE-06／T0–T6） |
| 缺项表 | 同目录 `phase1-wave7-three-ends-te-min-gaps-20261104.md`（本文引用） |
| 基线 tip | BE `16a7c3b`／PC `6c6b0b0`／安卓 `79b4f3b`／iOS `e10d02f` |
| 证据根 | `/workspace/billiards-playability/`（箱内）＋ handoff `测试1.1/` |
| 继承钉 | 历史证据→现行头：祖先／未见相关 diff **仅旁证**，**不**自动记现行头 PASS |
| 时区 | 2026-11-04 Asia/Shanghai（UTC+8） |

---

## 0 · 闸钉（维持 · 旁证 only · 本包不重开）

| 闸 | 状态 | 本包 |
|---|---|---|
| A17 | **开**（G3 FAIL 维持；G1／G2／G4／G5 保留不重测） | 旁证；不复测／不重开 |
| 方案 H | **停** | 旁证；不重开 |
| G-ROLL | **关**＠`6c6b0b0` | 旁证；不重开 |
| 物理 PG-MIN | **PARTIAL／到限归档·停观察** | 旁证；不重开观察 |
| μ／γ／停稳／合 main／真服／黑八胜／换皮 | **禁／维持** | 不变 |
| T1／T4 烟测 | **不开**（须另授权） | 本轮只索引 |

---

## 1 · 包级判定

| 判据 | 结论 |
|---|---|
| **ALIGN-INVENTORY-COMPLETE** | **是** — T0–T5 各适用端均有**可定位证据**或**明确缺证记录**（见 §2） |
| **核验（分列）** | **PARTIAL** — 关键契约在 PC 现行头 `6c6b0b0` 对 W2／W12／W21／W19 **缺现行头专证／继承未核实**；PC design↔physics 对等残差锁测形态 **缺／待核**；安卓／iOS 对 W2／W12／W7／W21 亦为祖先旁证（证据 tip≠现行头），不自动 PASS |
| **已证实背离 FAIL** | **未见**（本轮只读未发现 freeBall 清时机／table-v0 常量与 BE **已证实**背离） |
| 盘点完成 ≠ | ≠ 全量通过；≠ 现行头 PASS；≠ 烟测／复跑／改码获准；≠ 重开既有闸 |

**包级一句话：ALIGN-INVENTORY-COMPLETE + 核验 PARTIAL（关键契约缺现行头证；无已证实 FAIL 背离）。**

---

## 2 · 分列盘点（TE-00～TE-06／T0–T6）

> 每项：路径＋章节／行号（尽量）、证据 tip、现行 tip、结论、缺口。路径相对 `/workspace/billiards-playability/`（箱内证据主源）；handoff 副本另注。

### TE-00／T0 · tip 矩阵钉死

| 端 | 路径＋锚 | 证据 tip | 现行 tip | 结论 | 缺口 |
|---|---|---|---|---|---|
| **BE** | `phase1-be-wave7-s6-smoke-merge-gate-16a7c3b.md` L1–L14（「维持 `16a7c3b`／不升」）；`phase1-be-wave7-w19-s2-archive-merge-gate-16a7c3b.md` L1–L14（父 `b6816db`） | `16a7c3b` | `16a7c3b` | **钉死 MATCH**（S6／W19-S2 归档头） | 远端 PR head 若前推＝待核（箱内未见更新） |
| **PC** | 范围稿 `…-acceptance-scope-20261104.md` §0.1 L48；`测试1.1/exe-bind-6c6b0b0-a17.txt` L1–L16／`exe-bind-6c6b0b0-physics-geom-pg-min.txt`（tip FULL／parent `9fb9c5b`／size **272384**／SHA256 `7B6B6B1B…DB2E`／BIND_MATCH） | 跑头证＝`6c6b0b0`；W19 证＠`55acb81`（≠跑头） | `6c6b0b0` | **跑头＋exe BIND 钉死**；证据 tip≠跑头已标明 | 禁升 `5d6987f`；W19 等专包＠旧 tip 见 TE-E0 |
| **安卓** | `phase1-android-wave7-s6-smoke-merge-gate-79b4f3b.md` L1–L10；`phase1-android-wave7-w19-tip7-merge-gate-79b4f3b.md` L1–L12（未叠 `1383e68`） | `79b4f3b` | `79b4f3b` | **钉死 MATCH**（W19 tip⑦／S6 维持） | ≠ PC；PR#73 draft |
| **iOS** | `phase1-ios-wave7-s6-smoke-merge-gate-e10d02f.md` L1–L10；`phase1-ios-wave7-w19-rest-seed-merge-gate-e10d02f.md` L1–L14（物理祖先 `b3221a6`） | `e10d02f` | `e10d02f` | **钉死 MATCH**（W19／S6 维持） | ≠ PC；PR#71 draft |

**TE-00 结论：** 四端 tip 矩阵＋PC exe BIND **只读钉表完成**。

---

### TE-01／T1 · freeBall 清时机（跟 BE 本杆末清）

| 端 | 路径＋锚 | 证据 tip | 现行 tip | 结论 | 缺口 |
|---|---|---|---|---|---|
| **契约** | `phase1-billiards-v12-4021539-w2-freeball-align-accept-20261028.md` L12–L16／L32–L34（合法 PlaceCue **不清**；**本杆末清**；三端跟 BE） | 产品落锤 2026-10-28 | — | **契约可复用** | — |
| **BE** | 同上＋历史 BE `phase1-be-pr76-w2-freeball-align-b3fe451.md`（权威语义） | `b3fe451`（语义） | `16a7c3b` | 契约钉 BE 本杆末清；现行头为 W19 归档头（文档称步进未改＝**旁证**） | 现行头无 W2 专包复跑；**不**自动 PASS |
| **PC** | `phase1-pc-wave7-w2-merge-gate-6c6efb1.md` L9–L24（PlaceCue 保旗／本杆末清；有条件并关） | `6c6efb1` | `6c6b0b0` | **历史有条件关**；证据 tip≪现行头 | **缺证／待核继承**（TE-E0）；烟测**不开** |
| **安卓** | `phase1-android-wave7-w2-merge-gate-f6e6f0e.md` L9–L24；`phase1-android-w2-freeball-align-accept-f6e6f0e.md` L11–L19；软随 `phase1-android-wave7-soft-follow-merge-gate-3050020.md` L1–L24（Remote PlaceCue 不清） | `f6e6f0e`（软随 `3050020`） | `79b4f3b` | **历史有条件关**；现行头为其后裔（W19 tip⑦）＝**祖先旁证** | 不自动现行头 PASS；烟测不开 |
| **iOS** | `phase1-ios-wave7-w2w3w7-merge-gate-dcccb68.md` L9–L24（W2 A–E 有条件通过） | `dcccb68` | `e10d02f` | **历史有条件关**；祖先旁证 | 不自动现行头 PASS；烟测不开 |

**TE-01 结论：** 契约清晰；三端历史有条件关可索引；**PC／移动现行头均未专证 → 缺证记录齐；烟测另授权。** 未见已证实背离。

---

### TE-02／T2 · table-v0 常量（跟 BE）

| 端 | 路径＋锚 | 证据 tip | 现行 tip | 结论 | 缺口 |
|---|---|---|---|---|---|
| **BE** | `phase1-be-wave7-w12-table-friction-merge-gate-418f138.md` L11–L21（L×W **2.540×1.270**；Default **1.45／2.90／4.50**；MaxCue **8**；Capture；`table_params_version=table-v0`；**不宣称 cm**） | `418f138` | `16a7c3b` | 权威常量表有条件关＠`418f138`；现行头后裔＝旁证 | 现行头无 W12 专复跑 |
| **PC** | `phase1-pc-wave7-w12-table-v0-merge-gate-b45b6ad.md` L11–L21（`TableParamsVersion=table-v0`；无物理数值改；不宣称 cm） | `b45b6ad` | `6c6b0b0` | **历史有条件关** | **现行头待核／缺证**（TE-E0） |
| **安卓** | `phase1-android-wave7-w12-table-v0-merge-gate-38439ef.md` L11–L24（PARAM=table-v0；MaxCue 8.0；摩擦 1.45／2.90／4.50） | `38439ef` | `79b4f3b` | **历史有条件关**；祖先旁证 | 不自动现行头 PASS；不宣称 cm |
| **iOS** | `phase1-ios-wave7-w12-table-v0-merge-gate-7619e1f.md` L11–L21；soft 升头 `phase1-ios-wave7-w12-soft-comment-tip-elevate-5113043.md` L1–L16（仅注释） | `7619e1f`（soft `5113043`） | `e10d02f` | **历史有条件关**；祖先旁证 | 不自动现行头 PASS |

**TE-02 结论：** 四端历史 table-v0 有条件齐可索引；**不宣称 cm**；PC 现行头缺专证＝缺证记录。未见已证实常量背离。

---

### TE-03／T3 · design↔physics（felt 2:1／残差锁测；**仅索引**；不签视觉）

| 端 | 路径＋锚 | 证据 tip | 现行 tip | 结论 | 缺口 |
|---|---|---|---|---|---|
| **总表** | `phase1-billiards-v12-4021539-soft-reg-w1-refresh-20261028.md` L15（「W7 三端有条件并关」；视觉仍不签） | soft-reg＠`55acb81`／移动 tip | — | 口径可复用；**不**＝现行头 PASS | — |
| **安卓** | `phase1-android-wave7-w7-design-physics-merge-gate-f63154f.md` L11–L22；product-accept 同 tip L21–L34（Residual 锁测6；felt 同比 2.0） | `f63154f` | `79b4f3b` | **历史有条件关＝残差锁测可索引**；祖先旁证 | 不签视觉；不自动现行头 PASS |
| **iOS** | `phase1-ios-wave7-w7-design-physics-merge-gate-d9fe02b.md` L11–L22；product-accept L21–L32（feltRect 强制物理 2:1；球径残差仅锁） | `d9fe02b` | `e10d02f` | **历史有条件关＝残差／felt 2:1 可索引**；祖先旁证 | 不签视觉；不自动现行头 PASS |
| **PC** | soft-reg 写「三端齐」；箱内 PC 对等残差锁测 **未见** 与 `f63154f`／`d9fe02b` 同构；另有 `phase1-pc-wave7-w7-soft-kitchen-highlight-merge-gate-d6f6269.md` L11–L21（厨区高亮＝**≠本项**） | `d6f6269`≠本项 | `6c6b0b0` | **分列待核／缺对等残差锁测形态** | **TE-E3**；不编造 PASS |

**TE-03 结论：** 移动残差锁测可索引；PC 对等形态 **缺证**；视觉终签 OUT。T3＝仅索引，本轮不复跑。

---

### TE-04／T4 · W21 相位（`FreeBall && !CuePlaced`）

| 端 | 路径＋锚 | 证据 tip | 现行 tip | 结论 | 缺口 |
|---|---|---|---|---|---|
| **BE** | `phase1-be-wave7-w21-merge-gate-fcb6bd0.md` L11–L22（derivePhase／refreshPhase → `FreeBall && !CuePlaced`；PlaceCue 后 sync→my_turn） | `fcb6bd0` | `16a7c3b` | **历史有条件关**；现行头后裔＝旁证 | 无 W21 现行头专复跑 |
| **PC** | `phase1-pc-wave7-w21-sync-phase-merge-gate-4229fb4.md` L11–L22；handoff `phase1-pc-w21-sync-phase-4229fb4-handoff.md` L6–L21（`IsPlacingFreeBall`） | `4229fb4` | `6c6b0b0` | **历史有条件关** | **现行头继承待核／缺证**；烟测不开 |
| **安卓** | `phase1-android-wave7-w21-merge-gate-b44c1f4.md` L11–L22（相位锁测4；主码已 cueInHand） | `b44c1f4` | `79b4f3b` | **历史有条件关**；祖先旁证 | 不自动现行头 PASS；烟测不开 |
| **iOS** | `phase1-ios-wave7-w21-merge-gate-50ca415.md` L1–L27（主验 `50ca415`；tip 头曾升 `d93c499`；门禁 FreeBall&&!CuePlaced） | `50ca415`／`d93c499` | `e10d02f` | **历史有条件关**；祖先旁证 | 不自动现行头 PASS；烟测不开 |

**TE-04 结论：** 四端门禁句可索引；PC 现行头 **缺证**；烟测**不开**。未见已证实背离。

---

### TE-05／T5 · W19 rest／seed（**仅盘点** G0–G5／remarks；不宣称 bit-identical；不复跑）

| 端 | 路径＋锚 | 证据 tip | 现行 tip | 结论 | 缺口 |
|---|---|---|---|---|---|
| **口径** | `phase1-billiards-v12-4021539-soft-reg-w1-refresh-20261028.md` L14／L21／L23–L26（不宣称 bit-identical；S05 pocketed／S07 any_rail＝remarks） | soft-reg | — | **remarks 锁可复用** | 全量 bit **OUT** |
| **BE** | `phase1-be-wave7-w19-s2-archive-merge-gate-16a7c3b.md` L12–L25（归档；不改步进；fixture MATCH）；父链 fixture＠`b6816db` | `16a7c3b`（归档）／`b6816db` | `16a7c3b` | **证据＝现行头**（归档）；G0–G5 历史有条件关可索引 | 不宣称 bit-identical／cm |
| **PC** | `phase1-pc-wave7-w19-rest-seed-merge-gate-55acb81.md` L15–L31（G0–G5 全过；G2 S01/S04＝跨端 golden） | `55acb81` | `6c6b0b0` | **历史有条件关＠旧 tip**；现行头 **未见 W19 专包复跑** | **不足／待核**（TE-E0）；本包**不复跑** |
| **安卓** | `phase1-android-wave7-w19-tip7-merge-gate-79b4f3b.md` L17–L28；`phase1-android-w19-rest-seed-accept-79b4f3b.md` L52–L64（G0–G5；remarks：S05 pocketed／S07 any_rail） | `79b4f3b` | `79b4f3b` | **证据＝现行头**；G0–G5＋remarks **可盘点** | 不宣称 bit-identical |
| **iOS** | `phase1-ios-wave7-w19-rest-seed-merge-gate-e10d02f.md` L16–L24；product-accept L22–L29（G2 remarks；Δsteps=+44／+45；S04≤1e-3） | `e10d02f` | `e10d02f` | **证据＝现行头**；G0–G5＋remarks／Δsteps **可盘点** | 不宣称 bit-identical |

**TE-05 结论：** 安卓／iOS／BE 现行头可盘点 G0–G5／remarks；PC 现行头 **缺 W19 复跑证**＝明确缺证；**不宣称 bit-identical**；本包不复跑。

---

### TE-06／T6 · G-UI「未查」**仅索引**（不入可执行最小测集；交互≠换皮）

| 项 | 路径＋锚 | PC | 安卓 | iOS | 本轮 |
|---|---|---|---|---|---|
| G-UI-01～05／击点／HUD28 | `phase1-pc-wave7-pr76-gap-confirm-body-93bfe45-20261102.md` **§③** L72–L81；**P2** L104 | 多项已查／部分实现／DOC＠`93bfe45`（≠现行 `6c6b0b0` 复验） | **未查**＠`79b4f3b` | **未查**＠`e10d02f` | **仅索引**；禁用 PC 填三端 |
| G-UI-02 收球槽 | 同上 L77／L83+；前序 A17 开／G3 FAIL | PC 部分实现／A17 未完整验收 | **未查**实体槽接入 | **未查** | 前序依赖；本包不重测 A17 |
| 换皮／桌布杆图 | 用户序④；OUT | — | — | — | **OUT＝last** |

**TE-06 结论：** 「未查」状态已索引入缺项表（TE-E6／E7）；**不纳入 TE-MIN 可执行测集**。

---

### 旁证／环境（非 TE 关项）

| # | 路径 | 用途 |
|---|---|---|
| soft S3 | `phase1-wave7-soft-s3-three-ends-none-close-20261028.md` | soft 本波无关卷口径 |
| soft-reg 刷新 | `phase1-billiards-v12-4021539-soft-reg-w1-refresh-20261028.md` | W2／W7／W12／W19 状态总表 |
| PG-MIN problems | `phase1-pc-wave7-physics-geometry-pg-min-6c6b0b0-problems-20261104.md` | 物理前序 PARTIAL 旁证 |
| Codex B | `phase1-pc-wave7-post-pgmin-next-priority-codex-advice-20261104.md` | 先进三端范围；确认前不派测 |
| A17 scope | `phase1-pc-wave7-a17-pocket-rail-acceptance-scope-20261103.md` | A17 开旁证 |

---

## 3 · 各 TE 一行结论

| ID | 一行结论 |
|---|---|
| **TE-00** | 四端 tip＋PC exe BIND 只读钉死完成（MATCH／标明异 tip） |
| **TE-01** | 契约＝本杆末清可复用；三端历史有条件关可索引；PC／移动现行头缺专证＝缺证；烟测不开；无已证实 FAIL |
| **TE-02** | 四端历史 table-v0 有条件齐可索引；不宣称 cm；PC 现行头缺证；无已证实 FAIL |
| **TE-03** | 安卓／iOS 残差／felt 2:1 锁测可索引；PC 对等形态缺／待核；视觉 OUT；仅索引 |
| **TE-04** | 四端 W21 门禁句可索引；PC 现行头继承待核；烟测不开；无已证实 FAIL |
| **TE-05** | BE／安卓／iOS＠现行头可盘点 G0–G5／remarks；PC＠`6c6b0b0` 无 W19 复跑＝不足；不宣称 bit-identical；不复跑 |
| **TE-06** | G-UI 未查／收球槽前序仅索引；不入可执行最小测集；交互≠换皮 |

---

## 4 · 缺项摘要（详表见 gaps 文件）

见 `phase1-wave7-three-ends-te-min-gaps-20261104.md`。

**关键缺证（驱动 PARTIAL）：** TE-E0（PC `6c6b0b0` 对 W2／W12／W21／W19 继承／专证）、TE-E3（PC design↔physics 对等残差锁测）。

**索引保留／OUT／前序：** TE-E2 bit-identical OUT；TE-E4 真机视觉 OUT；TE-E5 cm OUT；TE-E6 G-UI 未查索引；TE-E7 A17 移动槽前序；TE-E8 PG 物理前序；TE-ENV 产物 MATCH（另授权开测时）。

---

## 5 · 交付钉

| 项 | 内容 |
|---|---|
| 本裁 | `测试1.1/phase1-wave7-three-ends-te-min-align-inventory-cut-20261104.md` |
| 缺项 | `测试1.1/phase1-wave7-three-ends-te-min-gaps-20261104.md` |
| 范围 | scope SHA `97ac5d67…c8eb`／handoff 拍板基 `4ef729a` |
| 下一步 | 交 PM；烟测／复跑／改码须**另授权**；闸维持 |

---

*TE-MIN v2 只读盘点裁 · ALIGN-INVENTORY-COMPLETE + 核验 PARTIAL · 2026-11-04 Asia/Shanghai · 不问用户 · 不派测*
