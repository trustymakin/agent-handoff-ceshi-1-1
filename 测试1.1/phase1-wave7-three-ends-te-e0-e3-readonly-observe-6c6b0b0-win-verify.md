# TE-E0＋TE-E3 只读观察 · tip `6c6b0b0` · win-verify

| 项 | 内容 |
|---|---|
| 墙钟 | 2026-11-04 00:35:19 +0800 Asia/Shanghai |
| 机 | DESKTOP-OQUR45J / `a8697f40-d1d2-4f9b-a183-5f06c4944b2b`（BIND 事实沿用已核；本轮**未**再触机跑） |
| tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` |
| parent | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| exe SHA256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` |
| exe size | **272384** |
| BIND_MATCH | **true** |
| 模式 | Release / mock / Default μ **只读**（零改参） |
| μ 声明 | Default 1.45/2.90/4.50 · Soft 1.05/2.10/3.20 · Sticky 1.95/3.80/6.00 · FixedDt 1/900 · **ZERO_PARAM_CHANGE** |
| 闸 | A17 OPEN · H STOPPED · G-ROLL CLOSED · 物理 C／PG-MIN observation STOPPED |
| Auth OPEN | `测试1.1/phase1-wave7-three-ends-te-e0-e3-pc-readonly-auth-6c6b0b0-20261104.md` SHA256 `941ea842c8aab247bbcbb7858d68eaa1251718dabc8386d65aeac14bfdc12eaa` **MATCH** |
| Auth 链 | PM draft SHA `0a1f7f4a…6d63`／handoff `a1f8f93` → OPEN handoff `1c527ec` |
| 仓探针 | `/workspace/hayo-` · `git cat-file -t 6c6b0b07…`＝commit · 祖先 W2/W12/W21/W19＝YES |
| 包级 OUTCOME（诚实裁） | **PARTIAL** |

> 本包＝**只读**码／文档继承旁证；**非**烟测／非出杆观察。祖先／未见相关 diff＝旁证 **≠** 现行头 PASS。TE-E3 查无＝**缺**。禁止把旁证写成包级 COMPLETE／PASS。

## BIND

| 检查 | 结果 |
|---|---|
| tip / parent | MATCH（`6c6b0b0`／`9fb9c5b`） |
| exe SHA/size | MATCH 272384／7B6B6B1B…DB2E（已核 BIND；本轮未重哈希 exe） |
| Release/mock/Default | 是（模式钉） |
| μ 只读／ZERO_PARAM_CHANGE | 是 |
| Auth OPEN SHA | MATCH `941ea842…12eaa` |
| 本轮触机跑／烟测 | **否**（授权禁 T1／T4） |

## TE-E0 · 现行头继承旁证（4 行）

| # | 项 | 路径／行号 | 证据 tip | 现行 tip | 结论与缺口 |
|---|---|---|---|---|---|
| 1 | **W2** freeBall（本杆末清／PlaceCue 保旗） | `BilliardsEngine.cs` L165–167 保旗；末清 L291–292／319–320／376–377／483–484／504–505；`billiards-freeball-slice-a.md` L5–10／15–17；闸 `phase1-pc-wave7-w2-merge-gate-6c6efb1.md` L9–24 | `6c6efb1`（祖先 YES；Engine／PlayPhase 无相关 diff→tip） | `6c6b0b0` | **旁证有**；**≠ PASS**；缺口＝缺 tip 专证／禁烟测未复跑 |
| 2 | **W12** table-v0 | `BilliardsPhysicsContract.cs` L11／17／70／73／97／100–104；`PlaySmoke.cs` L350–420（未执行）；闸 `phase1-pc-wave7-w12-table-v0-merge-gate-b45b6ad.md` L11–21 | `b45b6ad`（祖先 YES；table-v0／μ／台尺未见数值改） | `6c6b0b0` | **旁证有**；**≠ PASS**；不宣称 cm；缺口＝缺 tip 专证／禁烟测未复跑 |
| 3 | **W21** 相位（`FreeBall && !CuePlaced`） | `BilliardsPlayPhase.cs` L32／43；`BilliardsMatchStateFrames.cs` L53；`BilliardsLocalAuthority.cs` L231–236；闸 `phase1-pc-wave7-w21-sync-phase-merge-gate-4229fb4.md` L11–22 | `4229fb4`（祖先 YES；相位相关路径无 diff→tip） | `6c6b0b0` | **旁证有**；**≠ PASS**；缺口＝缺 tip 专证／禁烟测未复跑 |
| 4 | **W19** rest-seed | `RestSeedReplay.cs` L7–15／130–143；fixture SHA `c2aba546…e91d` tip＝`55acb81` MATCH（0 diff）；闸 `phase1-pc-wave7-w19-rest-seed-merge-gate-55acb81.md` L15–31 | `55acb81`（祖先 YES；其后 GAP-FRICTION-01 改 G2 锁） | `6c6b0b0` | **旁证部分有**（harness＋fixture）；**≠ PASS**；缺口＝S01/S04 golden 相对闸 tip 已改写；缺 tip 专包复跑；不宣称 bit-identical；本轮不复跑 |

### TE-E0 方法摘要

- 探针仓：`/workspace/hayo-`（`git show 6c6b0b07…:path`／`git diff <ancestor>..tip`；未 checkout 脏树）。
- 祖先全部 `merge-base --is-ancestor`＝YES：`6c6efb1`／`b45b6ad`／`4229fb4`／`55acb81`。
- 文档索引：`/workspace/billiards-playability/phase1-pc-wave7-w{2,12,21,19}-*-{merge-gate,product-accept}-*.md`；盘点裁 `phase1-wave7-three-ends-te-min-align-inventory-cut-20261104.md` §TE-01/02/04/05（已标 PC 现行头缺专证）。
- **未**跑 smoke；**未**改码；**未**把祖先有条件关升为现行头 PASS。

## TE-E3 · design↔physics 同构形态

| 项 | 内容 |
|---|---|
| 对照安卓 | tip `f63154f` · `phase1-android-wave7-w7-design-physics-merge-gate-f63154f.md` L11–22 · `BilliardsDesignPhysicsResidualTest` Residual 锁测6／felt 同比 2.0（**非** PC tip 祖先） |
| 对照 iOS | tip `d9fe02b` · `phase1-ios-wave7-w7-design-physics-merge-gate-d9fe02b.md` L11–22 · `feltRect` 强制物理 2:1＋球径残差锁（**非** PC tip 祖先） |
| PC 厨区（≠本项） | tip `d6f6269` · `phase1-pc-wave7-w7-soft-kitchen-highlight-merge-gate-d6f6269.md` L11–21 · KitchenMax／DrawKitchen **≠** residual／felt 锁测 |
| PC tip 检索 | `git ls-tree`／`git grep`＠`6c6b0b0`：**无** `*Residual*`／`DisplayGeom`／`feltRect`／design-physics 探针路径 |
| WIN-P2 | `Program.cs` L389–407 cloth aspect＝布局拟合，**≠** 安卓／iOS Residual 同构 |
| soft-reg | `phase1-billiards-v12-4021539-soft-reg-w1-refresh-20261028.md` L15「W7 三端有条件并关」**不可**替代 PC 对等残差锁测形态 |
| **结论** | **缺** |
| 缺口 | 无同构 design↔physics residual／felt 锁测；不签视觉；不编造 PASS |

## 分列表（汇总）

详见同包 `phase1-wave7-three-ends-te-e0-e3-readonly-observe-6c6b0b0-fenliebiao.md`（5 行全列）。

| ID | 结论一行 |
|---|---|
| TE-E0-1 W2 | 旁证有（码继承）／≠ PASS／缺 tip 专证 |
| TE-E0-2 W12 | 旁证有（常量继承）／≠ PASS／缺 tip 专证 |
| TE-E0-3 W21 | 旁证有（相位继承）／≠ PASS／缺 tip 专证 |
| TE-E0-4 W19 | 旁证部分有（harness+fixture；G2 锁已漂）／≠ PASS／缺 tip 专包 |
| TE-E3 | **缺**（无同构 residual／felt 锁测） |

## 包级判定

| 候选 | 是否采纳 | 理由 |
|---|---|---|
| COMPLETE／全 PASS | **否** | TE-E3 缺；TE-E0 均为旁证≠现行头 PASS；W19 G2 锁相对闸 tip 已改 |
| **PARTIAL** | **是** | BIND＋Auth MATCH；TE-E0 四项可定位旁证／缺口；TE-E3 明确缺证收口 |
| BLOCKED | 否 | 只读探针成功；无触机失败 |

## 禁项回声（本轮遵守）

- **禁** T1／T4 烟测 · **禁** 改码／造烟测当 PASS · **禁** 合 main／真服／黑八胜／换皮／升头
- **禁** 重开 A17／物理续测／扩大安卓／iOS 执行 · **禁** 把厨区高亮当 TE-E3
- **交证后停手等产品裁**；勿自扩／勿自开烟测／勿自续轮

## 产物

| 文件 | 路径 |
|---|---|
| win-verify（本文件） | `_te-e0-e3-readonly-6c6b0b0/phase1-wave7-three-ends-te-e0-e3-readonly-observe-6c6b0b0-win-verify.md` |
| 分列表 | `_te-e0-e3-readonly-6c6b0b0/phase1-wave7-three-ends-te-e0-e3-readonly-observe-6c6b0b0-fenliebiao.md` |
| exe-bind stamp | `_te-e0-e3-readonly-6c6b0b0/exe-bind-6c6b0b0-te-e0-e3-readonly.txt` |
| SHA 清单 | `_te-e0-e3-readonly-6c6b0b0/DELIVERABLE-SHA256.txt` |

### win-verify SHA256 (final · of body above this heading)
`d11cecfa942ebf43065ebd482435fbaf61fb2ff70e3e9ce78d9ecfad8734abe3`
