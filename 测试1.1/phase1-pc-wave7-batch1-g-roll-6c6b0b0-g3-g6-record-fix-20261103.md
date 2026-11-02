# G3–G6 文档记录修正 · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

**并行于 G1／G2 开闸；不派 PC；G-ROLL 仍不关。**

| 钉 | 内容 |
|---|---|
| 范围 | **仅文档记录修正**（G3–G6）；**不派 PC**；**不改业务代码**；**不合 main**；不重录已有合格段 |
| Tip | 保持 `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（短 `6c6b0b0`） |
| 依据 | `phase1-pc-wave7-batch1-g-roll-6c6b0b0-remaining-gaps-20261103.md` |
| 补测包 | `/workspace/billiards-playability/_cut-min-retest-6c6b0b0/` |
| G1／G2 | 并行开闸（另文）；本文**不**覆盖 G1／G2 补证执行 |
| G-ROLL | **仍暂不关** |

---

## G3 刷新后姿态保持 · 记录对齐（不重录）

| 项 | 内容 |
|---|---|
| 对齐主帧 | `_cut-min-retest-6c6b0b0/phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-m2-pose-after-refresh.png` |
| 同会话对照 | `…-m2-pose-after-handoff.png`；`…-m2-pose-post-stop.png` |
| 旧包旁证 | `_cut-6c6b0b0/…-pose-after-refresh.png`＋`_diff_pose-after-handoff_vs_pose-after-refresh.png` |
| 记录句 | 「刷新后姿态保持」**已用** `m2-pose-after-refresh` 与 handoff／post-stop 对照匹配；win-verify soft refresh 保持、SHA 互异＝非空对照 |
| 动作 | **仅记录修正**；**不重录** |

---

## G4 新局重置 · 记录对齐（不重录）

| 项 | 内容 |
|---|---|
| 对齐主帧 | `_cut-min-retest-6c6b0b0/phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-m2-pose-newmatch-initial.png` |
| 旧包旁证 | `_cut-6c6b0b0/…-pose-newmatch-initial.png`／`…-initial2.png`＋`_diff_pose-newmatch-initial_vs_init-orientation.png` |
| 记录句 | 「新局重置」对齐到 `m2-pose-newmatch-initial*`（满架初始姿态可核对）；**≠** nextfire 无缝链证明 |
| 动作 | **仅记录修正**；**不重录** |

---

## G5 checklist partial · 纠正为用户目视 4／6／7／10／14

| 项 | 内容 |
|---|---|
| 用户目视（准） | partial 球号＝**4／6／7／10／14** |
| 旧说法（纠） | 仅写「4／14」 |
| checklist 原文 | `m3-ball-coverage-checklist-6c6b0b0.txt`：行上仅 **4、14** 标 `HL_readable=partial`；**6／7／10** 行曾标 `yes` → **产品旁注以用户目视为准**，不把「行上 yes」写成产品已关闭遮挡关注 |
| SUMMARY 保留 | `partial＝occlusion/angle not missing asset`（遮挡／角度，非缺素材） |
| 对齐帧 | `…-m3-checklist-fulltable.png`；混聚 `…-hl-cluster-close-v2.png`／`…-hl-rd-solid-stripe-close-v2.png`；运动旁证 `…-rh-motion1.png`／rd-motion* |
| 动作 | **仅记录修正**／产品文档旁注；**不重录**合格段；**不改** checklist 原文文件字节 |

---

## G6 纠正旧说法 · `hl-cue-close-v2` 未补齐；PC M3 ≠ 产品 M3 PASS

| 旧说法（勿再写／勿再当关闸） | 产品纠正 |
|---|---|
| 「母球近距 v2 已补齐」／「母球＋…近距（v2 补齐）」 | **`hl-cue-close-v2` 裁空（~6KB／近空未框球面）＝未补齐**；勿再写「母球近距 v2 已补齐」 |
| 「M3 = 通过」暗示产品 M3 PASS | **PC M3 通过／VERIFY-COMPLETE ≠ 产品 M3 PASS**；产品裁＝有限通过／母球专用近距素材不足 |
| 条纹／全色／混聚 v2 可读 ⇒ 母球专用近距合格 | **否**；旁证可读 ≠ 母球解耦主证合格 |

来源钉：`…-win-verify.md` M3 行旧写「v2 补齐」「M3 = 通过」——**不得**再作产品关闸依据。  
动作：**仅文档修正**；**无**补测；**无**改码；**不派 PC**。

---

## 同步轻量修补（本轮）

| 文件 | 修补点 |
|---|---|
| `phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-product-cut-20261103.md` | M3 说明「仅 4／14」→用户目视 **4／6／7／10／14**；钉 PC M3≠产品 M3 PASS／cue-close-v2 未补齐；变更日志一行 |
| `phase1-pc-wave7-batch1-g-roll-6c6b0b0-visual-audit-pack-20261103.md` | 检查记录「4／14 partial」→**4／6／7／10／14**；钉勿写母球 v2 已补齐；变更日志一行 |

---

## 禁项（再钉）

- 不派 PC；不改业务代码；不合 main；不下一批  
- 不重录已有合格段；不派 Codex；勿改高光亮度／球皮路径  
- G-ROLL **仍不关**

---

*产品经理助手 · 只写文件 · 2026-11-03 ~05:11 Asia/Shanghai · tip `6c6b0b0` · 并行 G1／G2 · 不派 PC · G-ROLL 仍不关*
