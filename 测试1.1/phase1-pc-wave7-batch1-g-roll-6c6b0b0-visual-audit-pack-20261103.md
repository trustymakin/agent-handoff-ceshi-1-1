# 目视审核包 · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

## 站立口径（用户）
- **G-ROLL 维持不关**；保留 tip `6c6b0b0`
- **不派 Codex／不改码**
- 只用现有三轴 v2／nextfire／近距高光＋检查记录做目视；**不重复录制已有合格证据**
- 审核后**仅针对剩余缺项**再定补证或修复
- **HL-FALLBACK＝N/A**；不合 main／μγ／真服／黑八胜／下一批 仍闸

## 母球高光：不足 vs 异常（明确裁）

| 判定 | **素材不足以判断（专用近距）** |
|---|---|
| 不是 | 已观察到实际渲染异常（无烘焙高光残留／球皮缺失／明显坏斑等结论） |
| 依据 | `hl-cue-close-v2`（~6KB，936×636）目视＝台面近空＋细点，**未框到可用母球面**，不能当高光主证 |
| 旁证 | `hl-cue-close`（v1）可见母球本体＋球杆尖＋柔和明暗，可证「球在」；但帧内高光斑／解耦对比仍偏淡，**不足以单独裁定解耦高光 PASS／FAIL** |
| `hl-scatter-cue-close` | 近空台面，**不可用** |
| `hl-rd-solid-stripe-close-v2` | 混聚可读；母球在角且偏小／带瞄准圈，仅作旁证 |
| 检查表 | checklist 将 cue 标 `HL_readable=yes`＝全台／运动旁证口径，**≠** 专用 cue-close-v2 已合格 |

→ 母球高光当前缺项＝**缺一张可用的母球专用近距高光帧**；在补到之前，不据此宣称「已见异常需改码」。

## 现有素材清单（不重录）

### M1 三轴 v2
- `g-roll-min-retest-6c6b0b0-rh-axes-v2.mp4`
- `g-roll-min-retest-6c6b0b0-rv-axes-v2.mp4`
- `g-roll-min-retest-6c6b0b0-rd-axes-v2.mp4`
- 静帧旁证：`…-rd-motion1.png` 等

### M2 nextfire
- `g-roll-min-retest-6c6b0b0-pose-chain-nextfire.mp4`

### M3 近距高光
- 条纹：`…-hl-stripe-close-v2.png`
- 全色：`…-hl-solid-close-v2.png`（边角裁，球面占比小）
- 混聚：`…-hl-cluster-close-v2.png`／`…-hl-rd-solid-stripe-close-v2.png`
- 母球：`…-hl-cue-close.png`（旁证）／`…-hl-cue-close-v2.png`（不足）

### 检查记录
- `m3-ball-coverage-checklist-6c6b0b0.txt`（cue＋1–15；4／14 partial＝遮挡）
- `phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-win-verify.md`
- `phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-product-cut-20261103.md`
- 证包主 SHA `ED035A33…84378B53`（已分卷）

## 目视后建议动作（仅剩缺项）
1. 若三轴／nextfire／条纹·全色高光你目视 OK → **仅补母球专用近距一帧**（可选），仍不关闸前不派 Codex。
2. 若某条你判失败 → 点名缺项后再定补证或改码。
3. 在你点名前：**不派 Codex、不重录已合格段、不关 G-ROLL**。
