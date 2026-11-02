# G-ROLL 剩余缺口对齐表 · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 钉 | 内容 |
|---|---|
| **G-ROLL** | **仍暂不关**（补证有实质进展 ≠ 关闸） |
| **改码** | **无改码理由**；不派 Codex；勿改高光亮度／勿改球皮路径 |
| **Tip** | 保持 `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（短 `6c6b0b0`）；父 `9fb9c5b` |
| **合入／批次** | **不合 main**；**不下一批**；不重做整套；**不重录已有合格段**；**勿再上传沟通仓** |
| 角色 | 产品侧剩余缺口盘点（只写文件）；≠开工；≠派 PC／美术／Codex |
| 用户目视站立（已定） | 三轴 v2 实出杆＋遮挡转回 **OK**；nextfire 实击出且未集体回正 **OK**；混聚可补静帧 **OK**；FALLBACK＝N/A **保留** |

---

## 结论摘要

1. 补测包使 M1 三轴／M2 nextfire／混聚近距有实质进展；**产品仍不关 G-ROLL**；PC「VERIFY-COMPLETE／M3 通过」**≠** 产品 M3 PASS。
2. 须立刻纠正旧说法：**`hl-cue-close-v2` 裁空 ≠ 母球近距已补齐**；win-verify 写「母球＋…近距（v2 补齐）」／「M3 通过」**不能**当作产品关闸依据。
3. 检查表 partial 以用户目视对齐为 **4／6／7／10／14**（不止原文行上的 4／14）；混聚／fulltable 已有部分静帧 → **逐项对齐记录即可**，默认不重录。
4. 姿态链：nextfire **已确认**实击出 ≠ **无缝连续**证明；刷新／新局先匹配已有 `m2-pose-after-refresh`／`m2-pose-newmatch-initial*`，不重录合格段。
5. **无改码理由**；对「确实缺失」仅列可选最小补证句；默认不派 PC。

---

## 主表 · 剩余缺口

| 缺项ID | 用户关注点 | 现有材料能否补上 | 材料路径／记录句 | 状态 | 下一步 |
|---|---|---|---|---|---|
| **G1** | 母球高光专用近距：v1 未见渲染异常；**v2 裁空 ≠ 近距补齐**；**勿改亮／勿改码** | **否（专用近距主证）**；v1／混聚仅旁证 | `_cut-min-retest-6c6b0b0/…-hl-cue-close-v2.png`（~6KB／936×636，近空未框球面）＝**不可作主证**；`…-hl-cue-close.png`（v1）可见母球＋杆尖＋柔和明暗，**未见异常、不足以单独裁定解耦 PASS**；旁证：`…-hl-rd-solid-stripe-close-v2.png`／`…-hl-cluster-close-v2.png`／`…-hl-scatter-cue-close.png`（scatter 近空不可用）。visual-audit-pack：素材不足 ≠ 已观察渲染异常 | **确实缺失**（缺一张可用母球专用近距高光帧作解耦主证） | **可选最小补证**：仅补 1 帧母球专用近距（框住球面、可判高光相对球冠／屏方位）；注明可选、**不改码／不改亮**、不重录三轴／nextfire／混聚合格段；**默认不派 PC** |
| **G2** | 姿态无缝连续：nextfire 已确认实击出且未集体回正 ≠ 证明停球→换手→下一杆**无缝** | **部分旁证有；无缝主证无** | 已确认 OK：`…-pose-chain-nextfire.mp4`（fired=True，pct=55）＋`…-m2-pose-next-fired-motion.png`／`…-m2next-motion*`。链旁证：`…-m2-pose-post-stop.png`／`…-m2-pose-after-handoff.png`；旧 `_cut-6c6b0b0/…-pose-chain.mp4`／pose-motion* 可匹配对照。记录句：nextfire＝「下一杆实击出」证，**≠**「全时段无缝连续」证 | **确实缺失**（无缝连续专用证明） | **可选最小补证**：若用户仍要无缝主证，仅要一段覆盖停球→换手→下一杆的连续窗（或明确时间戳对齐说明）；**不重录**已合格 nextfire／三轴段；**默认不派 PC**。否则下一步＝**仅记录修正**（文档写清 nextfire≠无缝） |
| **G3** | 刷新后姿态保持（站立令：刷新未在「已确认 OK」明示） | **能（匹配已有静帧）** | `_cut-min-retest-6c6b0b0/…-m2-pose-after-refresh.png`；同会话对照 `…-m2-pose-after-handoff.png`／`…-m2-pose-post-stop.png`；旧 `_cut-6c6b0b0/…-pose-after-refresh.png`＋`_diff_pose-after-handoff_vs_pose-after-refresh.png`。win-verify：soft refresh 保持；SHA 互异非空对照 | **可用现有补齐记录** | **仅记录修正**：在产品裁／目视包写明「刷新后姿态保持」已用 `m2-pose-after-refresh` 匹配；**不重录** |
| **G4** | 新局重置（站立令：新局未在「已确认 OK」明示） | **能（匹配已有静帧）** | `_cut-min-retest-6c6b0b0/…-m2-pose-newmatch-initial.png`；旧 `_cut-6c6b0b0/…-pose-newmatch-initial.png`／`…-initial2.png`＋`_diff_pose-newmatch-initial_vs_init-orientation.png`。记录句：新局满架初始姿态可核对，≠ nextfire 无缝链 | **可用现有补齐记录** | **仅记录修正**：对齐「新局重置」到 `m2-pose-newmatch-initial*`；**不重录** |
| **G5** | 检查表 partial 实为 **4／6／7／10／14**（不止 4／14）；混聚已补部分 → 逐项对齐证据；SUMMARY「partial＝遮挡非缺素材」保留 | **能（逐项对齐记录）** | checklist 原文：`m3-ball-coverage-checklist-6c6b0b0.txt` 行上仅 **4、14** 标 `HL_readable=partial`；**6／7／10** 行写 `yes`——与用户目视 **4／6／7／10／14** 不一致，须产品侧改记。对齐材料：`…-m3-checklist-fulltable.png`；`…-hl-cluster-close-v2.png`；`…-hl-rd-solid-stripe-close-v2.png`；`…-rh-motion1.png`／rd-motion*。SUMMARY：partial＝occlusion/angle **not missing asset** | **可用现有补齐记录** | **仅记录修正**：产品文档／检查表旁注改记 partial＝**4／6／7／10／14**，并逐号点到 fulltable／混聚／motion 帧；**不重录合格段**；不把「行上 yes」误写成产品已关闭遮挡关注 |
| **G6** | 纠正旧说法：「母球近距 v2 已补齐」「产品 M3 通过」 | **能（文档修正）** | 须纠正来源：`…-win-verify.md` M3 行「母球＋条纹＋全色可辨近距（**v2 补齐**）」＋「**M3 = 通过**」；visual-audit／product-cut 已写 cue-close-v2 近空。正确产品句：**cue-close-v2 未补齐**；PC M3 事实标签 ≠ **产品 M3 PASS**；条纹／全色／混聚 v2 可读 ≠ 母球专用近距合格 | **可用现有补齐记录** | **仅记录修正**（本文＋后续裁稿引用本表）；**无**补测；**无**改码 |
| **G7** | FALLBACK＝N/A；三轴 v2；nextfire 实击出 — 用户已目视确认 | **已确认，无需再补** | M4：win-verify／checklist NOTE「Do NOT force HL-FALLBACK」；代码 `ImageFailedHits=0`、台面 unlit 无资产失败分支。M1：`…-rh/rv/rd-axes-v2.mp4` 实出杆＋遮挡转回 **OK**。M2：`…-pose-chain-nextfire.mp4` 实击出且未集体回正 **OK** | **已目视关闭** | **无** |

---

## 状态统计

| 状态 | 缺项ID | 条数 |
|---|---|---|
| 确实缺失 | G1、G2 | **2** |
| 可用现有补齐记录 | G3、G4、G5、G6 | 4 |
| 已目视关闭 | G7 | 1 |

---

## 与 win-verify／product-cut 的产品纠正钉

| 旧说法（勿再引用为产品关闸） | 产品纠正 |
|---|---|
| 「母球＋…近距（v2 补齐）」 | **`hl-cue-close-v2` 裁空，未补齐**；v1 旁证未见异常 ≠ 解耦主证合格 |
| 「M3 = 通过」／暗示产品 M3 PASS | PC 事实标签／VERIFY-COMPLETE **≠** 产品 M3 PASS；**G-ROLL 仍不关** |
| checklist partial＝仅 4／14 | 用户目视对齐 **4／6／7／10／14**；用混聚／fulltable 逐项记，不重录 |
| nextfire 通过 ⇒ 姿态链无缝 | nextfire＝实击出确认；**≠** 无缝连续证明 |

---

## 禁项（再钉）

- 不合 main；不下一批；不重做整套；不重录已有合格段  
- 无改码／不派 Codex；勿改高光亮度；勿动球皮／`RasterizeSpherePrint`／`MakeLightingOverlay`  
- 勿再上传沟通仓  
- 默认不派 PC；上表「可选最小补证」须用户点名后才议  

---

## 材料索引（box）

| 包 | 路径 |
|---|---|
| 补测包 | `/workspace/billiards-playability/_cut-min-retest-6c6b0b0/` |
| 旧 remediation | `/workspace/billiards-playability/_cut-6c6b0b0/` |
| 目视包 | `phase1-pc-wave7-batch1-g-roll-6c6b0b0-visual-audit-pack-20261103.md` |
| 产品裁 | `phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-product-cut-20261103.md` |
| win-verify | `_cut-min-retest-6c6b0b0/phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-win-verify.md` |

---

*产品经理助手 · 只写文件 · 2026-11-03 Asia/Shanghai · tip `6c6b0b0` · G-ROLL 仍不关*
