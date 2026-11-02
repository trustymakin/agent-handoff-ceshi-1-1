# PC 桌台换皮 · 文档齐全度缺口盘点 · tip `6c6b0b0` · 2026-11-03

| 项 | 内容 |
|---|---|
| 角色 | **产品侧只读盘点**（文档齐全度优先）；≠开闸；≠授权派美术／Codex |
| 代码锚 | `/workspace/wt-pc-ui7a01-7a96b27` · HEAD **`6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`**（短 tip `6c6b0b0`）· 父 `9fb9c5b` · 日志：`fix(pc): G-ROLL remediation sphere UV + unlit print + pose persist (Wave7 batch1)` |
| 资料锚（确认基线） | `phase1-pc-wave7-pr76-gap-draft-acceptance-boundary-93bfe45-20261102.md` · `phase1-pc-wave7-pr76-gap-confirm-body-93bfe45-20261102.md`（同文；资料 PR#76@`2c84497` × 代码曾记 tip `93bfe45`；**本盘点代码层升到 `6c6b0b0`，文档基线未随升改写**） |
| 本轮用户改令 | **换桌／杆前先核产品文档**；勿盲开工；**确认前不派美术／Codex** |
| 明确不是 | ≠合 main；≠改 μ／γ；≠真服；≠合法黑八胜；≠关掉 G-ROLL；≠立刻硬派 UI美术·氛围出图或 Codex 接线 |

---

## 结论摘要（≤5 行）

1. **文档尚未齐全到可开「整套桌台 UI 换皮」**：PR#76／gap 确认基线把 **G-UI-01 袋口／库边**标成「已有但未验证／叠图验收」，**不是**「换一套新桌／杆资产」的开闸条目；多皮肤在 backlog 明确 **本轮单皮肤、后排**。
2. 已有的是：**尺寸映射（BV12-E01）**、**赛博蓝黑石墨＋青边方向句**、**木质球杆素材锚点**、**V5 袋口轮廓保留**、**ui7a 人测色样／结构 PASS 旁证**——多为「现行冻结／对照」，**缺换皮 brief（风格拍板、资产清单、替换边界、验收截图矩阵）**。
3. **桌布／台框／袋口／灯光氛围**在运行时多为 **代码绘制（Geometry／Brush）**；产品文档几乎无「可换 PNG 壳层」规格 → 主态多落 **B 或缺文档的 C**。
4. **球杆**文档相对最齐（木杆外观＋锚点）；仍缺「是否允许换新杆图／尺寸是否锁 1168×64」的换皮确认。
5. **建议下一步：先交用户确认风格与范围（是否换皮、换到哪一稿、桌／杆优先边界）并补文档；确认前不派美术／Codex。**

---

## 文档齐全度主表（三态）

**三态定义**

| 态 | 含义 |
|---|---|
| **A. 文档已有** | 产品／美术／验收文档能指到出处＋要点，足以说明「现行目标／冻结」或「明确后排」 |
| **B. 文档缺项** | 换皮／出图／接线**应有**的规格，在已查产品／美术文档中找不到 |
| **C. 仅代码有、文档无** | `6c6b0b0` XAML／cs／Assets 可指到实现，但无对应产品描述（或文档口径与代码已分叉） |

| 项 | 三态 | 文档出处与要点（A）／缺什么（B）／代码锚（C） | 对「可开换皮」的含义 |
|---|---|---|---|
| **桌布（台呢／felt）** | **A（方向）＋B（换皮 brief）＋C（现行绘制）** | **A**：`billiards-spec/…experience-physics…` BV12-E01「台呢…必须共享映射」；`UI_…README`「赛博外观采用蓝黑石墨、青色边线」；`ui7a03-product-accept-582d303` 毡采样 ≈RGB(24,70,104)／对齐 PC-01；`backlog-skins` **本轮单皮肤**、多皮肤后排；gap **G-UI-01** 只谈袋口／库边叠图，不谈换呢。**B**：无换皮色板／材质类型（纯色 vs 纹理 PNG vs SVG）、无目标对照帧清单、无「允许偏离 ui7a 冻结」批注。**C**：`DrawFeltGrid` 用 `Rectangle`+`LinearGradientBrush`（约 `#1A4A6A→#0E2A42`）＋淡网格 `Line`；`FeltHost` XAML `#FF0E2A42`；**无** felt PNG 资源。 | 不能把「有赛博色方向」当成「可立刻出新桌布图」；须先补换皮 brief |
| **台框／库边（rail／cushion 外观）** | **A（尺寸／方向）＋B（外观资产）＋C（绘制）** | **A**：E01 外框「不将外框当物理内台」；UI README 赛博青边；ui7a「库边青线克制」；gap **G-UI-01**「袋口／库边｜E01；UI｜已有但未验证｜叠图；球径比」。**B**：无木纹／金属／赛博板材选型；无 rail 宽度视觉 token 与 `RailFraction=0.08` 是否可改的产品句；无独立 rail 贴图交付物。**C**：`DrawFeltGrid` 外圈 `Rectangle`+纵向 `LinearGradientBrush`（`#1A2A34→#0C1820`）；外层 `TableFrame`／内边 XAML Border（`#08121A`／`#0B1A22`＋青／深边）；注释写明 U1 cyber、**not wooden-only**。 | G-UI-01＝验收叠图，≠换框开闸；缺资产规格 |
| **球杆（cue）** | **A（较齐）＋B（换皮确认）＋C（接线）** | **A**：`UI/billiards/README`「真实木质球杆…maple／深把／接牙／皮头」；锚点 SVG 292×16 皮头(286,7)、PNG 1168×64 锚点(1144,28)；`HUD-INTERACTION-SPEC`「杆外观是真实木杆，不能用加粗杆体代替命中区域」；cue-controls「拉动桌面球杆松手出杆」。**B**：无「本波是否换新杆图／是否锁现锚点与长宽比」的产品确认；无换杆验收截图矩阵。**C**：`EnsureCue` → `ms-appx:///Assets/billiards/wooden-cue.png`；`UpdateAimAndCue` 旋转／后拉；Assets 仅此一张杆图（另有源 SVG 在 UI pack，PC 运行时用 PNG）。 | 相对最接近可换资产，但仍须用户确认风格与是否动锚点；**确认前不派** |
| **袋口（pocket 视觉）** | **A（保留 V5／验叠图）＋B（换皮／新美术）＋C（代码几何）** | **A**：UI README／HUD「**V5 袋口轮廓不变**」；「不用发光掩盖洞口」；E01「袋口开口／袋角／袋唇几何仍须与物理调校一并冻结」；gap **G-UI-01**；ui7a「V5 袋口…分层洞口可见」。**B**：无「允许重绘袋口 path／换 PNG 袋口」的换皮许可；无 jaw 美术层 vs 物理 mouth 对照表（产品只强调勿用美术代替物理）。**C**：`DrawPockets`：`PathGeometry`（Bezier／Line）填充灰蓝＋`Border` 黑洞口；尺寸绑 `CornerMouth`／`SideMouthHalf`×scale；**无** pocket PNG。 | 文档倾向 **冻结轮廓**；换皮若动袋口＝高冲突，须显式产品开闸句 |
| **灯光氛围（对局台面／球桌环境光）** | **B 为主＋C** | **A（弱／旁证）**：球体侧「高光遵循场景灯光、不随印刷转」（E02／gap G-ROLL-02）——谈的是**球**，不是台面灯槽／环境 HDR。语音房 `Assets/atmosphere/*` 属壳层氛围，**不是**对局桌灯光规范。**B**：**无**对局页台面灯光／灯槽／环境遮罩的美术 brief；无「赛博霓虹强度」token；无换氛围出图清单。**C**：台面无独立灯光层；球体 `MakeLightingOverlay`＝屏固定 `RadialGradientBrush`；桌壳靠 XAML／代码色。 | 不可派「氛围出图」——缺标的物定义 |
| **球体贴图（台面球）** | **A（V4／解耦口径）＋C（代码已偏文档）＋B（换皮未开）** | **A**：E01／UI README「V4 球面＋A 阴影」；「高光不随印刷转」；gap **G-ROLL-01／02**；`V4-provenance.json`；skins「不新增皮肤商城」。**B**：无「换球皮材质包」产品条目；G-ROLL 目视包仍要求补证而非换资产。**C（分叉）**：`6c6b0b0` 台面球＝**程序 unlit albedo**（`RasterizeSpherePrint`／`SampleBallAlbedo`）＋独立高光 overlay；注释写明 **table sphere never samples V4 PNGs**；`ball-*.png` 仍在 Assets，主要用于 **MiniBall／收球槽 HUD**（`TryGetBallSprite`）。 | **换桌／杆开闸若碰到球皮＝踩 G-ROLL**；文档仍写 V4，代码台面已 unlit——换皮文档须先声明边界 |
| **收球槽外观（附）** | **A（行为＋结构旁证）＋B（换壳 brief）＋C** | **A**：BV12-E04／HUD 15 目标球、无白球、权威序；gap **G-UI-02**「已有部分实现，A17 未完整验收」；ui7a「弯接连续槽／凹井槽壳」。**B**：无换槽壳材质／色的出图规格。**C**：XAML `PocketTray` 容器＋`LinearGradientBrush` 槽壳；球芯片走 MiniBall／V4 PNG。 | 非本波桌／杆优先项；文档未授权换壳 |

---

## 对照 PR#76 确认基线：换皮是否在闸内？

| 来源 | 与「整套桌台换皮」关系 |
|---|---|
| gap-draft／confirm-body §2③ **G-UI-01** | 目标＝袋口／库边 **叠图／球径比验证**；状态「已有但未验证」；动作「统一世界坐标落地」——**验收／对齐，不是换资产开闸** |
| 同稿 §3 **P2** | 三端视觉分列＋收球槽验收；**无**「换桌布／换杆图」期项 |
| 同稿 **OUT／暂停钉** | 合 main／真服／黑八胜／改 μγ／demo＝PASS 等 **禁**；未写允许换皮 |
| `backlog-skins-20261025` | **本轮单皮肤**；可切换台面皮肤＝**后排、不挡本轮** |
| `ui7a-p2-product-call`（历史） | 曾要美术出「绿网格 vs 蓝黑石墨／V5／收球槽」差异页再批——指向 **向冻结稿收敛**，不是新皮肤战役 |
| `spec-gap-vs-pr76` **GAP-UI-01** | 「禁盲改桌体」；等用户指屏——与本轮「先核文档」一致 |

**结论句（钉死）**：**以现有确认基线，文档不足以把「换掉台球桌子、球杆等整套桌台 UI」标成已批准工作项；确认前不派美术／Codex。**

---

## 必须先补的文档（开换皮前最低集）

在用户确认「要做换皮」之后，产品／美术文档至少补齐下列（缺一则仍不宜硬派）：

1. **风格拍板一页**：保持赛博蓝黑石墨／回到设计包某一帧／新木质／其它；附 **1～2 张对照目标**（PR#76 UI 帧或新稿）与「明确不采用」反例。
2. **范围边界**：Phase A 仅桌呢＋杆？是否含台框、袋口、收球槽、灯光？**袋口默认冻结 V5** 是否写入？
3. **资产清单**：每项交付物格式（PNG／SVG）、尺寸、锚点、命名、是否替换代码 Brush／Path；球杆是否锁 1168×64 与皮头锚点。
4. **与 G-ROLL／球皮边界声明**：台面球继续 unlit 程序皮＋解耦高光；**本开闸不改** `RasterizeSpherePrint`／`MakeLightingOverlay`／姿态；V4 PNG 仅 HUD／槽则写清。
5. **验收截图矩阵**：全桌、角袋近景、中袋近景、杆 idle／拉杆、（可选）槽壳；对比 tip `6c6b0b0` 基线帧。
6. **冲突声明回写 gap 基线**：本项是否升为正式缺口 ID；仍钉不合 main／μγ／真服／黑八胜；**G-ROLL 维持不关并行**。

---

## 最小范围 Phase A（桌／杆）——仅作「文档未批前的结构建议」

> 下列不是开工授权，只标「若用户确认换皮后，文档应如何切 Phase」。

| 切片 | 文档条件 | 实现倾向（附录，供写 brief 用） |
|---|---|---|
| **Phase A1 球杆图** | 确认新杆或保留木杆；锁锚点 | 相对最接近「换 PNG」；仍可能微调 `UpdateAimAndCue` 比例 |
| **Phase A2 台呢色／纹理** | 色板或纹理图＋是否消灭网格线 | 今为代码 Gradient；换纹理＝须 Codex 改 `DrawFeltGrid` 接 ImageBrush（**非**零改逻辑） |
| **Phase A3 台框** | 外框／库边是否进 Phase A | 今为 XAML＋代码 Rectangle；换皮多半要改色或接图 |
| **不做进 Phase A（除非另批）** | 袋口 V5、收球槽壳、球体、灯光氛围大图、多皮肤切换 | 与冻结句／G-ROLL／后排皮肤冲突风险高 |

**可立刻做（无派工）**：补齐上文「必须先补的文档」草稿交用户确认。  
**须先出图再接线**：仅在 brief 批准且资产清单齐全后。  
**须改代码**：台呢／框／袋口今日均非「纯换文件」壳层（见附录）。

---

## 验收点（文档批准后方可测；可截图）

| ID | 截图／观察 | 通过直觉（须写入批准 brief） |
|---|---|---|
| R-01 | 对局全桌 | 台呢／框风格＝批准对照；比例仍满足 E01 球径／短边比观感 |
| R-02 | 角袋＋中袋近景 | 若 brief 冻结 V5：轮廓不漂移；洞口不被发光糊死 |
| R-03 | 杆 idle | 皮头朝向／锚点贴母球后方；完整杆身可见 |
| R-04 | 杆后拉峰值 | 杆沿瞄准轴后退；松手规则不变（D-G11） |
| R-05 | 与 `6c6b0b0` 球皮对照 | 号码／条纹滚动与屏固定高光路径**无回归**（G-ROLL 不关） |
| R-06 | HUD／收球槽小球 | 若未批换球皮：槽内仍可读球号；无白球入槽规则不变 |

---

## 与 G-ROLL／球体贴图边界（冲突声明）

| 钉 | 内容 |
|---|---|
| **G-ROLL** | **维持不关并行**（目视包 `phase1-pc-wave7-batch1-g-roll-6c6b0b0-visual-audit-pack-20261103.md`：不派 Codex／不改码；补母球近距高等） |
| **本开闸若盲换桌／杆** | 球杆 Image 层与球皮分离，**杆 PNG 替换原则上不碰** `RasterizeSpherePrint`；但同页 `BilliardsMatchPage.xaml.cs` 大文件并改易误伤 |
| **会碰到球皮／高光路径吗？** | **台呢／框／袋口代码绘制**与球皮同在 FeltCanvas 重建路径；改 `DrawFeltGrid`／`DrawPockets` 顺序或清画布逻辑有碰撞风险。**换球皮／改 overlay＝直接踩 G-ROLL**，文档未授权 |
| **文档 vs 代码分叉** | 产品仍常写 V4 台面球；`6c6b0b0` 台面已是 unlit 程序皮——换皮 brief **必须**写清以代码现状为准，避免美术按 V4 台面球重出图 |
| **OUT** | **不合 main／不改 μγ／不真服／不做黑八胜**（对齐 gap 确认基线 OUT） |

---

## 建议下一步（派工闸）

1. **先交用户确认**：是否真要「换皮」还是只要「对冻结赛博稿做缺口验收（G-UI-01）」；桌／杆风格选哪一档。  
2. **确认前：不派 UI美术·氛围出图；不派 Codex 接线。**  
3. 用户确认后：产品补「必须先补的文档」→ 再决定是否硬派美术出图 → 最后才 Codex（且与 G-ROLL 错峰／声明文件边界）。

---

## 附录 A · 代码实现快照（`6c6b0b0`，供写 brief，非主结论）

| 项 | 现状实现 | 可换资产？ | 需 Codex？ |
|---|---|---|---|
| 桌布 | 代码 `Rectangle` + `LinearGradientBrush` + 网格 `Line` | 否（无 PNG）；接图须改绘制 | 是（若换纹理／去掉网格） |
| 台框／库边 | XAML `TableFrame` Border 色＋代码 rail `Rectangle` Gradient | 改色可小改 XAML／常量；贴图须改代码 | 多半是 |
| 球杆 | `Image` + `wooden-cue.png`（1168×64） | **是（换 PNG，锚点慎动）** | 锚点／比例变则要改 |
| 袋口 | 代码 `PathGeometry` + `Border` | 否；V5 文档倾向冻结 | 动轮廓必须 Codex＋产品开闸 |
| 灯光氛围 | 无台面灯图层；球用 `RadialGradientBrush` overlay | 无氛围资产可换 | 新灯层＝Codex |
| 台面球皮 | 程序 `WriteableBitmap` unlit + 高光 overlay | 台面不读 `ball-*.png` | **禁随换皮改**（G-ROLL） |
| HUD／槽小球 | `ball-0..15.png` V4 | HUD 可换图但属球皮战役 | 与 G-ROLL／E01 口径交叉，另批 |

**重点文件**

- `clients/pc/…/Views/BilliardsMatchPage.xaml`（TableFrame／FeltHost／PocketTray）
- `clients/pc/…/Views/BilliardsMatchPage.xaml.cs`（`DrawFeltGrid`／`DrawPockets`／`EnsureCue`／`MakeBall`／`MakeLightingOverlay`／`RasterizeSpherePrint`）
- `clients/pc/…/Services/Billiards/BilliardsTableDisplay.cs`（`RailFraction`）
- `clients/pc/…/Assets/billiards/`（`wooden-cue.png`、`ball-*.png`、`V4-provenance.json`）

---

## 附录 B · 已查文档索引

| 路径 | 用途 |
|---|---|
| `/workspace/billiards-playability/phase1-pc-wave7-pr76-gap-draft-acceptance-boundary-93bfe45-20261102.md` | 确认基线／G-UI-01／OUT |
| `/workspace/billiards-playability/phase1-pc-wave7-pr76-gap-confirm-body-93bfe45-20261102.md` | 同上正文 |
| `/workspace/billiards-spec/docs_product_v1.2-billiards_billiards-v1.2-experience-physics-20261027.md` | BV12-E01～E05 |
| `/workspace/billiards-spec/UI_billiards_v1.2-20261027_README.md` | 赛博基准／V5／木杆／V4 |
| `/workspace/billiards-spec/UI_billiards_v1.2-20261027_HUD-INTERACTION-SPEC.md` | 木杆命中／袋口／收球槽 |
| `/workspace/wt-pc-ui7a01-7a96b27/UI/billiards/README.md` | 球杆锚点与木质描述 |
| `/workspace/wt-pc-ui7a01-7a96b27/docs/product/v1.2-billiards/phase1-hayo-v1.2-billiards-backlog-skins-20261025.md` | 单皮肤／多皮肤后排 |
| `/workspace/billiards-playability/phase1-pc-wave7-ui7a03-product-accept-582d303-20261029.md` | 台呢色样／V5 旁证 |
| `/workspace/billiards-playability/phase1-pc-wave7-ui7a-p2-product-call-20261029.md` | 向冻结稿收敛流程 |
| `/workspace/billiards-playability/phase1-wave7-spec-gap-vs-pr76-4021539-20261029.md` | 禁盲改桌体 |
| `/workspace/billiards-playability/phase1-pc-wave7-batch1-g-roll-6c6b0b0-visual-audit-pack-20261103.md` | G-ROLL 不关／不派 Codex |

---

*产品侧调研助手 · 只读 · 2026-11-03 Asia/Shanghai · tip `6c6b0b0`*
