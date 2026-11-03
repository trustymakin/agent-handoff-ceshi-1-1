# Wave7「三端对齐」· TE-MIN v2 缺项表 · 2026-11-04

| 项 | 内容 |
|---|---|
| 配套裁 | `phase1-wave7-three-ends-te-min-align-inventory-cut-20261104.md` |
| 范围 | TE-MIN v2 只读盘点（PM 拍板 A；scope SHA `97ac5d67…c8eb`／handoff `4ef729a`） |
| 口径 | 祖先／未见 diff＝旁证 ≠ 现行头 PASS；盘点完成 ≠ 全量／现行头通过 |
| 时区 | 2026-11-04 Asia/Shanghai |

---

## 缺项清单

| 缺项ID | 缺什么 | 为何不能直接用旧证 | 本轮记录 | 建议（须另授权才执行） |
|---|---|---|---|---|
| **TE-E0** | PC `6c6b0b0` 对 W2 freeBall／W12 table-v0／W21 相位／W19 rest 的**现行头专证或可核继承** | 关闸均在更旧 tip：`6c6efb1`／`b45b6ad`／`4229fb4`／`55acb81`；祖先／未见相关 diff 仅旁证 | **关键缺证 → 核验 PARTIAL** | 只读 diff／证据索引已做；烟测须另列用例＋tip／产物绑定后确认；禁改码 |
| **TE-E1** | 远端 PR head 是否仍＝箱内 tip | 远端可能前推；箱内 S6「维持」 | 本轮按箱内文档钉 `16a7c3b`／`6c6b0b0`／`79b4f3b`／`e10d02f`；**未见**更新于上述的 Wave7 正式 tip 升迁 | 另授权开测前再 rg／merge-gate；不符则停 |
| **TE-E2** | 跨端 rest **bit-identical** | soft-reg #9／W19 明确不宣称；remarks 锁微差 | **OUT** | 维持 remarks；禁 μ／DT 追 bit |
| **TE-E3** | PC design↔physics **对等残差锁测**形态（同构于安卓 `f63154f`／iOS `d9fe02b`） | soft-reg 写「三端齐」；箱内 PC 仅见厨区高亮 `d6f6269`≠本项 | **缺／待核 → 计入 PARTIAL 旁支** | 分列「待核」；不编造 PASS；不签视觉 |
| **TE-E4** | 真机手感／视觉终签 | 各关闸均不签 | **OUT／后置** | — |
| **TE-E5** | cm 正式冻／厨区校准表 | soft-reg #4 仍闸 | **OUT** | — |
| **TE-E6** | G-UI 安卓／iOS「未查」实查（G-UI-01～05／击点／HUD28） | pr76-gap §③／P2 钉未查；禁 PC 填三端 | **索引保留**；不入 TE-MIN 可执行 | 另包／换皮后置 |
| **TE-E7** | A17 移动端实体槽接入（G-UI-02） | A17 仍开（PC G3 FAIL）；移动未查 | **前序依赖**；本包不重测 A17 | 不冒充已通过 |
| **TE-E8** | 物理角袋 STRICT 正入等 PG 缺口 | PG-MIN PARTIAL／到限归档停观察 | **前序依赖**；本包不重开物理观察 | — |
| **TE-ENV** | 各端 BIND／APK／探针与 tip MATCH（开测时） | 历史宣称须重核 | 范围确认**不**自动开测；PC exe BIND＠`6c6b0b0` 已在 T0 索引 | 若另授权开测：分列重核 tip／产物 SHA |

---

## 关键缺证 vs 已证实背离

| 类 | 本轮 |
|---|---|
| **关键契约缺证 → PARTIAL** | TE-E0（主）；TE-E3（PC 残差形态） |
| **已证实背离 → FAIL** | **无**（freeBall 清时机／table-v0 常量未见与 BE 已证实背离） |
| **OUT／索引／前序** | TE-E2／E4／E5 OUT；TE-E6 索引；TE-E7／E8 前序；TE-E1／ENV 开测前再核 |

---

## 分端缺证速查

| 端 | 现行 tip | 关键缺／待核 | 现行头已有可定位证 |
|---|---|---|---|
| BE | `16a7c3b` | W2／W12／W21 为祖先旁证（归档头≠专复跑） | S6／W19-S2 归档＝现行头 |
| PC | `6c6b0b0` | **W2／W12／W21／W19 现行头专证缺**；design↔physics 对等残差缺 | tip／exe BIND；A17／PG／G-ROLL 本头包（非 TE 关项） |
| 安卓 | `79b4f3b` | W2／W12／W7／W21＝祖先旁证 | W19 tip⑦ G0–G5／remarks＝现行头；S6 维持 |
| iOS | `e10d02f` | W2／W12／W7／W21＝祖先旁证 | W19 G0–G5／remarks／Δsteps＝现行头；S6 维持 |

---

*TE-MIN v2 缺项表 · 配套只读盘点裁 · 2026-11-04 Asia/Shanghai*
