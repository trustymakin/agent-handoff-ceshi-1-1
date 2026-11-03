# Wave7「三端对齐」· 范围／证据／缺项包 · TE-MIN · 2026-11-04

| 项 | 内容 |
|---|---|
| 角色 | 「三端对齐」**只出稿**：范围＋证据索引＋缺项；**确认前不派测／不改码／不硬派任何端**；确认＝只读盘点，烟测另授权 |
| 用户序（钉） | ① A17 → ② 物理几何 → ③ **三端对齐（本项只出稿）** → ④ 换皮 last |
| Codex 拍板 **B** | `phase1-pc-wave7-post-pgmin-next-priority-codex-advice-20261104.md`：优先进三端对齐范围稿；确认前不派测 |
| PM 硬派 | 只出范围／证据／缺项包（基线＋IN／OUT＋判据＋前序依赖）；定稿前可再经 Codex 只读；稿齐交 PM |
| 「三端」 | **PC／安卓／iOS**（对照 **BE 契约**）；**禁止**用 PC 结论断言三端都没做；分列写 |
| BE tip | **`16a7c3b`**（FULL `16a7c3bebc96ef4232e182f8aebe61b81cdb88f3`；S6／W19-S2 归档头；父链含 `b6816db`） |
| PC 跑头 | 短 **`6c6b0b0`**／FULL **`6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`**（父 `9fb9c5b`；**禁**升头／禁 `5d6987f`） |
| exe BIND | size **272384** · SHA256 `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E`（mock） |
| 安卓现行 tip | **`79b4f3b`**（FULL `79b4f3b34d03ad4c65d39ae3785f744ed3242694`；W19 tip⑦／S6 维持头；PR#73；**≠** PC `6c6b0b0`） |
| iOS 现行 tip | **`e10d02f`**（FULL `e10d02f6e16d9773740862a4a8169dd97c666237`；W19／S6 维持头；PR#71；**≠** PC `6c6b0b0`） |
| 环境闸 | mock／箱内证据优先 · **不合 main** · 不真服 · 不黑八胜 · 不升头 |
| 本包明确不是 | ≠改游戏码／改 μγ／停稳；≠Codex 写码；≠合 main；≠真服；≠黑八胜；≠换皮／桌布杆图终签；≠重开 A17／物理观察；≠重开方案 H；≠用 PC 断言三端；≠派 PC／安卓／iOS／测（确认前）；≠范围确认自动授权烟测／复跑 |
| Codex 只读审稿 | SHA256 `15799f10f7ba0472415baa9d0c680a5ea17cc7476785bb5e23e2cce1cdbcee12`（短 `15799f10…`）；session `01a1a236-75be-7e32-8542-c0cf6bd6caa3`；稿 `phase1-wave7-three-ends-alignment-scope-codex-review-20261104.md` |
| 本文件 | **v2 收紧定稿（待 PM 拍板）**＝按 Codex 审稿收紧 IN／授权／证据／包级判据／前序／文末 A；确认前不派测 |

对齐文档（规格／挂起源，只读）：

- `phase1-pc-wave7-post-pgmin-next-priority-codex-advice-20261104.md`（Codex **B**）
- `phase1-pc-wave7-physics-geometry-pg-min-6c6b0b0-problems-20261104.md`（物理 PARTIAL／到限归档；前序依赖旁证）
- `phase1-pc-wave7-a17-pocket-rail-acceptance-scope-20261103.md`（A17 开；G3 FAIL 维持）
- `phase1-pc-wave7-pr76-gap-confirm-body-93bfe45-20261102.md` · **§③ G-UI**／**P2**（三端视觉分列；未查项）
- `phase1-billiards-v12-4021539-w2-freeball-align-accept-20261028.md`（freeBall 本杆末清＝BE）
- `phase1-billiards-v12-4021539-soft-reg-w1-20261028.md`＋`…-soft-reg-w1-refresh-20261028.md`（W1 缺口／刷新）
- `phase1-wave7-soft-s3-three-ends-none-close-20261028.md`（soft S3 三端本波无）
- W19 rest-seed：PC `…-w19-rest-seed-*-55acb81.md` · 安卓 `…-79b4f3b.md` · iOS `…-e10d02f.md` · BE fixture／归档 `b6816db`→`16a7c3b`
- W7 design↔physics：安卓 `f63154f` · iOS `d9fe02b`（felt 2:1／残差；**不签视觉**）
- W21 sync-phase：BE `fcb6bd0` · PC `4229fb4` · 安卓 `b44c1f4` · iOS `50ca415`
- table-v0／摩擦：BE `418f138` · PC `b45b6ad` · 安卓 `38439ef` · iOS `7619e1f`（另 soft 升头 `5113043` 仅注释）
- 模板：`phase1-pc-wave7-physics-geometry-acceptance-scope-20261103.md`

资料目标锚：PR#76／soft-reg／各端 merge-gate＝对照 only；**历史有条件关 ≠ 本跑头自动复验 PASS**。

---

## 0 · 背景／基线 tip／闸门

> 本稿＝**产品范围包**。Codex 选 **B** 后进入「三端对齐」文案准备；**在 PM 拍板确认前：不派 PC、不派安卓、不派 iOS、不派测、不改码、不派 Codex 写码、不合 main。**（站立：分析／方案由 PM＋Codex 拍板，不转用户三选一。）

### 0.1 各端现行 tip（文档核；勿臆造）

| 端 | 现行 tip（短） | FULL（文档） | 核源（最新 accept／merge-gate／S6） | 备注 |
|---|---|---|---|---|
| **BE** | `16a7c3b` | `16a7c3bebc96ef4232e182f8aebe61b81cdb88f3` | `phase1-be-wave7-s6-smoke-merge-gate-16a7c3b.md`；W19-S2 archive | 父 `b6816db`；步进未改于 S2 归档 |
| **PC** | `6c6b0b0` | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` | A17／PG-MIN／G-ROLL 本头包；exe-bind | **跑头远新于** W19 证据 tip `55acb81`；禁 `5d6987f` |
| **安卓** | `79b4f3b` | `79b4f3b34d03ad4c65d39ae3785f744ed3242694` | W19 tip⑦ merge-gate＋S6 smoke | **≠** PC；PR#73 draft；未叠 `1383e68` |
| **iOS** | `e10d02f` | `e10d02f6e16d9773740862a4a8169dd97c666237` | W19 merge-gate＋S6 smoke | **≠** PC；PR#71 draft；物理祖先 `b3221a6` |

> **钉**：安卓／iOS **当前跑头以上表文档为准**；仓库内未见更新于 `79b4f3b`／`e10d02f` 的 Wave7 正式 tip 头升迁（S6 明确「维持」）。若远端 PR head 已前推而箱内未落 accept＝**待核**，本稿不臆造。

### 0.2 闸钉（维持）

| 闸 | 状态 |
|---|---|
| A17 | **开**（G3 FAIL 维持；G1／G2／G4／G5 保留不重测）＝**背景与缺口旁证**，不构成本包复测或重开授权 |
| 方案 H | **停**（不再自开）＝原状维持；仅旁证，不构成本包重开授权 |
| G-ROLL | **关**＠`6c6b0b0`＝原状维持；仅旁证，不构成本包重开授权 |
| 物理 PG-MIN | **PARTIAL／到限归档·停观察**（Codex C；问题清单已落）＝原状维持；仅旁证，不构成本包复测或重开授权 |
| μ／γ／停稳阈值 | **变更限制维持**；禁升 `5d6987f` |
| 合 main／真服／黑八胜／换皮 | **禁**（换皮仍 last） |
| 确认前派测／硬派端 | **禁**（本稿不派）；**范围确认≠烟测授权** |

### 0.3 本批口径（契约／状态机／常量／回放 · 非换皮）

优先跨端 **契约／状态机／常量／回放** 对齐核对；**不**做换皮视觉终签、**不**宣称全量 bit-identical、**不**做真机手感终签。

---

## 1 · 三端对齐验收范围

> **确认基线**：历史 Wave7 多项已「有条件并关」——本批＝在**各端现行 tip**上做**证据索引＋可观测复核对齐**（能只读核的只读核）；**不预先指定改码／追 bit／改 μ**。演示／祖先 tip ≠ 现行 tip PASS。
>
> **IN／授权（Codex 收紧）：** TE-MIN 本轮为 T0–T6 **只读盘点**；T1／T4 烟测**不**随范围确认自动获准，须另列固定用例、各端 tip／产物绑定及预期证据后确认；确认前不派测。
>
> **证据要求（Codex 收紧）：** 每项按适用端记录具体文件路径及章节／行号、证据 tip、现行 tip、结论与缺口。BE／PC／安卓／iOS 均核历史证据至现行头的继承依据；祖先关系或未见相关 diff 仅作旁证，不自动记现行头 PASS。

### 1.1 建议最小可核子集 vs 全量

| 包 | 覆盖 | 本批建议 |
|---|---|---|
| **TE-MIN**（建议） | tip 矩阵钉死 · freeBall 清时机跟 BE · table-v0 常量跟 BE · design↔physics／felt 2:1 锁测状态分列 · W21 相位门禁分列 · W19 rest／seed 跨端 Δ／remarks 盘点（**不宣称 bit-identical**） | **确认＝只读盘点范围**；烟测另授权；确认前不派 |
| **全量（后置）** | 跨端 bit-identical 终追 · 真机手感终签 · G-UI 视觉／交互全矩阵 · 换皮／桌布杆图 · cm 正式冻 · 真服 L5 · Soft／Sticky 体验签 · A17 移动端实槽接入终验 | **OUT／后置** |

### 1.2 按可观测／可证据项分条（三端分列）

| ID | 可观测／可证据项 | 规格锚 | PC | 安卓 | iOS | 本批建议 |
|---|---|---|---|---|---|---|
| **TE-00 tip 矩阵** | 各端现行 tip／父链／禁升头；证据 tip≠跑头须标明 | 用户钉；S6／W19 | 跑头 `6c6b0b0`；W19 证＠`55acb81` | `79b4f3b` | `e10d02f` | **IN＝最小**（只读钉表） |
| **TE-01 freeBall 清时机** | 合法 PlaceCue **不清**；**本杆末清**；跟 BE | W2 落锤页 | 有条件关＠`6c6efb1`；**现行 `6c6b0b0` 是否仍保持＝待核** | 有条件关＠`f6e6f0e`（软随 `3050020`） | 有条件关＠`dcccb68` | **IN＝最小**（只读证索引；烟测**不**随范围确认获准，须另授权；**不改码**） |
| **TE-02 table-v0 常量** | L×W 2.540×1.270；Default μ 1.45／2.90／4.50；MaxCue 8.0；Capture；`table_params_version` | BE `418f138`；W12 | 有条件关＠`b45b6ad`（静态／smoke） | 有条件关＠`38439ef` | 有条件关＠`7619e1f`（soft 升头 `5113043` 仅注释） | **IN＝最小**（静态／既有 unit·探针索引；**不宣称 cm**） |
| **TE-03 design↔physics** | felt 2:1；残差锁测；**不签视觉** | soft-reg #3；W7 | soft-reg 写「三端有条件并关」；**PC 专用 residual 锁测 tip 形态≠移动＝待核**（另有 W7 kitchen-highlight `d6f6269`≠本项） | 有条件关＠`f63154f` | 有条件关＠`d9fe02b` | **IN＝最小（分列）**；视觉终签 **OUT** |
| **TE-04 W21 相位** | `FreeBall && !CuePlaced`；PlaceCue 后 sync 非摆位 | W21；BE `fcb6bd0` | 有条件关＠`4229fb4` | 有条件关＠`b44c1f4` | 有条件关＠`50ca415` | **IN＝最小**（锁测／merge-gate 索引；现行 tip 继承＝待核 PC；烟测另授权） |
| **TE-05 rest／seed 回放** | G0–G5；跨端 Δ；**历史未宣称 bit-identical** | W19；soft-reg #9 | 有条件关＠`55acb81`（PC＝G2 golden）；**现行 `6c6b0b0` 未做 W19 专包复跑＝待核** | 有条件关＠`79b4f3b`（remarks：S05 pocketed／S07 any_rail） | 有条件关＠`e10d02f`（G2 remarks；Δsteps） | **IN＝最小＝盘点＋remarks 锁**；全量 bit 追 **OUT** |
| **TE-06 G-UI「未查」** | §③ G-UI-01～05／击点／HUD 三端分列 | pr76-gap §③；P2 | 多项已查／部分实现／DOC | 多为 **未查**＠`e10d02f`／`79b4f3b` 待查 | 同左 | **TE-MIN＝仅索引「未查」状态，不纳入可执行最小测集**（见 §1.3） |
| **TE-μγ** | 参数闸 | G-PHY-μγ | 维持 | 维持 | 维持 | **闸＝维持**（禁为对齐追参） |

### 1.3 G-UI 是否纳入 TE-MIN（写清）

| 项 | 裁定（起草判断） | 依据 |
|---|---|---|
| G-UI 全矩阵（袋口叠图／瞄准／力度取消／击点／HUD28） | **OUT／不入 TE-MIN 可执行项**；本轮**仅索引** | 本批优先契约／状态机／常量／回放；**交互项不等同换皮**；换皮／桌布杆图仍 last |
| G-UI「未查」行 | **IN＝仅缺项索引**（TE-E6）：维持三端分列「未查」，**禁止**用 PC 已查结论填安卓／iOS | pr76-gap P2／§③ |
| G-UI-02 收球槽 | **前序依赖 A17（PC）**；安卓／iOS 仍 **未查** 是否接入实体槽 | A17 开／G3 FAIL；不在本包重测 A17 |
| 换皮／桌布杆图 | **OUT＝last** | 用户序④ |

环境钉（若另授权烟测／开测）：各端**分列**核 tip；PC 另核 exe BIND；mock；**禁用**祖先 tip／demo 冒充现行 tip PASS；**禁用** PC 结论断言三端。范围确认本身**不**自动开测。

---

## 2 · 已有证据（路径／tip／结论）

图例：**可复用**＝范围／闸／remarks 口径；**仅参考（异 tip／异端）**＝不可挂靠现行跑头 PASS；**不足**＝现行 tip 未见专包。祖先关系或未见相关 diff **仅作旁证**，不自动记现行头 PASS；须核历史证据→现行头继承依据（路径／章节／行号＋证据 tip／现行 tip／结论／缺口）。

| # | 路径 | tip／龄 | 一句话结论 | 标记 |
|---|---|---|---|---|
| 1 | `phase1-pc-wave7-post-pgmin-next-priority-codex-advice-20261104.md` | Codex B＠`6c6b0b0` | 先进三端范围稿；确认前不派测 | **可复用**（优先级） |
| 2 | `phase1-billiards-v12-4021539-soft-reg-w1-refresh-20261028.md` | BE `b6816db`／PC `55acb81`／iOS `e10d02f`／安卓 `79b4f3b` | W2／W12／W7／W19 刷新：有条件并关；**不宣称 bit-identical** | **可复用**（状态总表）；PC 跑头已前移→实机 **仅参考** |
| 3 | `phase1-billiards-v12-4021539-w2-freeball-align-accept-20261028.md` | 产品落锤 | 清时机＝三端跟 BE 本杆末清 | **可复用**（契约） |
| 4 | PC／安卓／iOS W2 merge-gate（`6c6efb1`／`f6e6f0e`／`dcccb68`） | 各端 W2 tip | 有条件并关 freeBall 生命周期 | **可复用**（关闸口径）；PC→`6c6b0b0` **待核继承** |
| 5 | BE／三端 W12 table-v0（`418f138`／`b45b6ad`／`38439ef`／`7619e1f`） | W12 | 四端 table-v0 有条件齐；不宣称 cm | **可复用**（常量）；PC 现行头 **待核** |
| 6 | 安卓／iOS W7 design↔physics（`f63154f`／`d9fe02b`） | W7 | felt 2:1／残差锁测；不签视觉 | **可复用**（移动）；PC 对等 tip **待核** |
| 7 | 四端 W21（`fcb6bd0`／`4229fb4`／`b44c1f4`／`50ca415`） | W21 | FreeBall&&!CuePlaced 有条件并关 | **可复用**；PC 现行头 **待核** |
| 8 | W19 rest-seed 三端＋BE（`55acb81`／`79b4f3b`／`e10d02f`／`b6816db`→`16a7c3b`） | W19 | G0–G5 有条件关；remarks 锁；**不宣称 bit-identical** | **可复用**（回放口径／remarks）；PC 现行头 **不足／待核** |
| 9 | `phase1-wave7-soft-s3-three-ends-none-close-20261028.md` | `79b4f3b`／`55acb81`／`e10d02f` | soft S3 三端本波无关卷 | **可复用**（soft 口径） |
| 10 | `phase1-pc-wave7-pr76-gap-confirm-body-93bfe45-20261102.md` §③／P2 | PC `93bfe45`＋移动 tip 钉 | G-UI 三端分列；移动多项 **未查** | **可复用**（未查索引） |
| 11 | A17 scope／G3 FAIL／H 停 诸包 | PC `6c6b0b0` | A17 开；不重测 G1／2／4／5 | **前序依赖**（旁证）；≠本包关项 |
| 12 | PG-MIN problems `…-20261104.md` | PC `6c6b0b0` | PARTIAL／到限归档停观察 | **前序依赖**（旁证）；≠本包重开 |
| 13 | tip `6c6b0b0` 三端对齐专包／跨端 rest 复跑 | **`6c6b0b0`** | **未见** | **不足** |
| 14 | 安卓／iOS＠现行 tip 的 G-UI／收球槽实机接入证 | `79b4f3b`／`e10d02f` | **未见**（仍「未查」） | **不足** |

计数：**可复用**（口径／关闸）约 10 · **前序依赖** 2 · **本头／现行不足** 2+ · PC 继承多项 **待核**。

---

## 3 · 缺项清单

| 缺项ID | 缺什么 | 为何不能直接用旧证 | 建议 |
|---|---|---|---|
| **TE-E0** | PC `6c6b0b0` 对 W2／W12／W21／W19 语义的**继承旁证或烟测** | 关闸均在更旧 tip（`6c6efb1`／`b45b6ad`／`4229fb4`／`55acb81`） | 范围确认后 TE-MIN **只读** diff／既有证据索引；烟测须另授权；禁改码 |
| **TE-E1** | 三端现行 tip 一眼矩阵（含 FULL／父／PR／禁叠）已钉入本包；若远端 head≠箱内 | 远端可能前推 | 只读盘点／另授权开测前再 `rg`／merge-gate 核一次；不符则停 |
| **TE-E2** | 跨端 rest **bit-identical** | 历史明确不宣称；remarks 锁微差 | **OUT**；维持 soft-reg #9 |
| **TE-E3** | PC design↔physics residual **对等锁测**形态 | soft-reg 写三端齐；箱内 PC 未见与 `f63154f`／`d9fe02b` 同构 tip | **待核**；最小包以移动证＋PC 分列「待核」呈现，不编造 PASS |
| **TE-E4** | 真机手感／视觉终签 | 各关闸均不签 | **OUT／后置** |
| **TE-E5** | cm 正式冻／厨区校准表 | soft-reg #4 仍闸 | **OUT** |
| **TE-E6** | G-UI 安卓／iOS「未查」实查 | pr76-gap 钉未查 | **索引保留**；不入 TE-MIN 可执行；另包／换皮后置 |
| **TE-E7** | A17 移动端实体槽接入 | G-UI-02 未查；A17 仍开（PC） | **前序依赖**；本包不重测 A17、不冒充已通过 |
| **TE-E8** | 物理角袋 STRICT 正入等 PG 缺口 | PG-MIN PARTIAL 清单 | **前序依赖**；本包不重开物理观察 |
| **TE-ENV** | 各端 BIND／APK／探针与 tip MATCH | 历史宣称须重核 | 若另授权开测：分列重核 tip／产物 SHA；范围确认不自动开测 |

---

## 4 · 建议最小包 TE-MIN（**确认前不派**）

> 名称：**TE-MIN**（Three-Ends MIN）。本轮＝T0–T6 **只读盘点**；零改码；mock／箱内。  
> **IN／授权：** T1／T4 烟测**不**随范围确认自动获准，须另列固定用例、各端 tip／产物绑定及预期证据后确认；确认前不派测。  
> **确认前不派** PC／安卓／iOS／测／Codex 写码。  
> **前序／OUT（Codex 收紧）：** A17 开／G3 FAIL、H 停、G-ROLL 关、物理 C 停观察原状维持，仅作背景与缺口旁证，不构成本包复测或重开授权。T3 仅索引残差锁测，T5 仅盘点既有 G0–G5／remarks。G-UI 本轮仅索引；交互项不等同换皮，换皮仍 last。

| 步 | 内容 | 对齐 | 端 |
|---|---|---|---|
| T0 | 钉四端 tip 矩阵＋PC exe BIND；写明证据 tip≠跑头 | TE-00 | BE／PC／安卓／iOS |
| T1 | freeBall：索引 W2 关闸句；PC＠`6c6b0b0` **只读**继承核「摆位保旗＋杆末清」；烟测**不**随范围确认获准（须另列用例／tip·产物／预期证据后确认） | TE-01 | 分列 |
| T2 | table-v0：对照 BE `418f138` 常量表；各端既有 W12 锁测／snapshot 索引（不宣称 cm） | TE-02 | 分列 |
| T3 | design↔physics：安卓／iOS W7 关闸＋残差句；**仅索引残差锁测**；PC 分列标 **待核**（不编造） | TE-03 | 分列 |
| T4 | W21：四端门禁句索引；PC 现行头继承 **待核**；烟测**不**随范围确认获准（须另列用例／tip·产物／预期证据后确认） | TE-04 | 分列 |
| T5 | W19：**仅盘点既有** G0–G5／remarks（S05／S07／Δsteps）；**明确不宣称 bit-identical**；PC 现行头无复跑则标不足；不随本包复跑 | TE-05 | 分列 |
| T6 | 输出：本包更新裁／缺项回写；G-UI **本轮仅索引**（未查附录）；交互≠换皮 | TE-06 索引 | — |
| 交付 | win-verify 或「只读盘点裁」＋分列表；交 PM | — | — |
| 包级 | **ALIGN-INVENTORY-COMPLETE** 仅表示 T0–T5 各适用端均有可定位证据或明确缺证记录。另列核验结论：关键契约缺证为 **PARTIAL**，已证实背离为 **FAIL**；盘点完成不代表全量或现行头通过 | ≠ 改码获准；≠ 烟测自动获准 | — |

**OUT（钉死）**：全量 bit-identical；真机手感终签；换皮／桌布杆图；G-UI 可执行全矩阵（本轮仅索引）；cm 冻；真服；Soft／Sticky 体验签；改 μ／γ／DT；合 main；黑八胜；升头；重开 A17；重开物理观察；重开 H；重开 G-ROLL；用 PC 断言三端；范围确认自动授权烟测／复跑。

**不可 OUT 豁免**：若另授权复核中发现 freeBall 清时机／table-v0 常量与 BE **明显背离** → 记 **FAIL**／缺项，**仍不擅自改码**。关键契约缺证＝**PARTIAL**（与盘点完成分列）。

---

## 5 · 明确非本批

| 禁／非本批 | 说明 |
|---|---|
| **改码／改物理参数** | 含 μ／γ／DT／cloth／StopHold／jaw／Capture／积分次序追 bit |
| **Codex 写码** | 不派；定稿前 Codex **只读**须主人另派 |
| **合 main／真服／黑八胜** | — |
| **换皮／桌布杆图** | last |
| **重开 A17／H／G-ROLL／物理观察** | 前序状态维持 |
| **硬派 PC／安卓／iOS／测** | **确认前不派**；范围确认≠烟测／复跑授权 |
| **用 PC 结论填三端** | 禁 |

---

## 6 · 文末选项（供 **PM 拍板**；过程勿再问用户选型）

> **确认前不派测／不硬派任何端／不改码。** 确认 TE-MIN＝只读盘点范围；烟测／复跑须另授权。

- **A** · 确认 TE-MIN 范围及只读盘点；**不**自动授权烟测、复跑、改码或重开既有闸。
- **B** · 改范围（扩／缩 IN／OUT 后重出稿）
- **C** · 暂缓（维持只出稿；不派）

---

*产品验收范围包 v2 收紧定稿（待 PM 拍板）· 2026-11-04 Asia/Shanghai · Wave7 三端对齐 · Codex B＋审稿收紧 · 确认前不派*
