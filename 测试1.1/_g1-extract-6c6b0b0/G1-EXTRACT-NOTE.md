# G1 最小补证 · 母球近距提取 · tip `6c6b0b0`

| 项 | 内容 |
|---|---|
| 时 | 2026-11-03 05:14 Asia/Shanghai（CST） |
| Tip | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（短 `6c6b0b0`） |
| 方式 | **只读提取**已有证包；**未**改码／**未**派 Codex／**未**重录／**未**合 main |
| 结论 | **EXTRACT_OK** |
| 范围 | `_cut-min-retest-6c6b0b0/`、`_cut-6c6b0b0/`、`g-roll-min-retest-6c6b0b0-evidence.zip` 内相关 png |

> 本提取仅交付「完整母球近距＋对应全台原帧」素材对。**≠ 产品 PASS**；**≠ G-ROLL 关闭**；不重录其他已合格项。

---

## 合格对（选用）

### 近距帧

| 项 | 值 |
|---|---|
| 文件 | `phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-hl-cue-close.png` |
| 本目录 | `/workspace/billiards-playability/_g1-extract-6c6b0b0/phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-hl-cue-close.png` |
| 源路径 | `/workspace/billiards-playability/_cut-min-retest-6c6b0b0/phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-hl-cue-close.png`（同 zip 内副本） |
| size | 22376 |
| 像素 | 1204×816 |
| SHA256 | `2f28a5984af26da3838e7b3d53ad8fce14318c6394d732595dc9f3dd31c0bdc4` |
| 合格？ | **是** — 框到**完整白母球球面**；球冠／侧向有可辨明暗梯度（近距内球盘半径≈60px；象限亮度差 NW−SE≈6.4；Read 可见高光＋软影） |
| 成因 | 探针 `Crop-Zoom`：`pose-newmatch-initial` → `cxFrac=0.30 cyFrac=0.52 frac=0.18 scale=4`；launch-console：`rect=352,489 301x204 x4`（2026-11-03 03:50:34 Asia/Shanghai） |
| 像素核 | 用该 rect＋NearestNeighbor 复现 crop：**MSE=0 / 像素全等** → 近距确为其源全台之放大裁切 |

### 对应全台原帧（裁切源，主配）

| 项 | 值 |
|---|---|
| 文件 | `phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-pose-newmatch-initial.png` |
| 本目录 | `/workspace/billiards-playability/_g1-extract-6c6b0b0/phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-pose-newmatch-initial.png` |
| 源路径 | `g-roll-min-retest-6c6b0b0-evidence.zip` 内同名（`_cut-min-retest-6c6b0b0/` 原先未放此主测帧，仅有 M2 补测 `m2-pose-newmatch-initial`） |
| size | 172571 |
| 像素 | 1672×1136 |
| SHA256 | `fdc5100a94a63d466882ed5dbd4ea4d738c239a746564ba8739be8bf6303d4d3` |
| 场景 | 同会话 M3：新局满架＋厨房母球＋球杆瞄准开球；母球在厨房线右侧完整可见 |

### 同会话全台旁证（检查表帧，非裁切源但同局同态）

| 项 | 值 |
|---|---|
| 文件 | `phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-m3-checklist-fulltable.png` |
| 本目录 | `/workspace/billiards-playability/_g1-extract-6c6b0b0/phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-m3-checklist-fulltable.png` |
| 源路径 | `/workspace/billiards-playability/_cut-min-retest-6c6b0b0/…-m3-checklist-fulltable.png` |
| size | 172576 |
| SHA256 | `face8b95c6842b566ffda05e27bec58f3a267ea8be9fa9f8bd25d8188fca9307` |
| 说明 | M3 checklist 全台快照（03:50:34，紧随 crop）；满架＋母球；**非** `hl-cue-close` 的像素源，作同场景全台旁证 |

### 为何选它

1. 用户原令：`hl-cue-close` v1 若可见完整母球＋明暗可辨 → 可标候选；须配全台原帧。  
2. Read 实看：完整白母球＋球杆头近贴；球面有高光／软影，明暗可辨（非近空）。  
3. launch-console 钉死源＝`pose-newmatch-initial`；本机像素复现全等。  
4. 拒绝把 `cue-close-v2`／`scatter-cue-close`／remediation `hl-cue-close` 等近空／错裁当合格。

---

## 已扫＋否决（母球相关／近距候选）

### `_cut-min-retest-6c6b0b0/`

| 文件 | size | 裁决 |
|---|---:|---|
| `…-hl-cue-close.png` | 22376 | **选用**（见上） |
| `…-hl-cue-close-v2.png` | 6427 | **否决** — 近空／极小点状，无完整母球球面与可辨明暗（用户明示勿当合格） |
| `…-hl-scatter-cue-close.png` | 16076 | **否决** — 空台＋网格／虚线，无母球（用户明示勿当合格） |
| `…-hl-solid-close-v2.png` | 6605 | **否决** — 非母球近距；体量近空级 |
| `…-hl-stripe-close-v2.png` | 21794 | **否决** — 条纹球近距，非母球 |
| `…-hl-cluster-close-v2.png` | 29779 | **否决** — 球堆近距，非「完整母球」专用帧 |
| `…-hl-rd-solid-stripe-close-v2.png` | 28222 | **否决** — 全色／条纹混聚，非母球专用 |
| `…-m3-checklist-fulltable.png` | 172576 | **全台旁证**（已拷）；非近距 |

### zip 内另解压核对（`_g1-scan-tmp-6c6b0b0/`）

| 文件 | 裁决 |
|---|---|
| `…-pose-newmatch-initial.png` | **全台源帧**（已拷） |
| `…-scatter-table.png` | 散架全台；其 cue crop＝`hl-scatter-cue-close` 已否决为近空 |
| `…-hl-rack-mid-close.png` / `…-hl-from-*-rd-motion*-close.png` | 球架／运动区近距，目标非完整母球专用 |
| `…-*-halfnear-*.png` / `…-*-near-stripe-solid-*.png` | M1 条纹／全色近距旁证，非 G1 母球专用近距 |

### `_cut-6c6b0b0/`（旧 remediation）

| 文件 | size | 裁决 |
|---|---:|---|
| `…-hl-cue-close.png` | 16596 | **否决** — Read：近空（仅台布网格／虚线），无母球 |
| `…-hl-left/top-close.png` | 13–16KB | **否决** — 近空／错位 crop |
| `…-hl-mid-close.png` | 35322 | **否决** — 目标为 1 号球且球面被裁切不完整 |
| `…-hl-bot/apex/right-close.png` | 33–48KB | **否决** — 对象球近距，非母球 |
| `…-hlmain-motion2-close.png` | 40483 | **否决** — 画面为带号球体（非白母球专用） |
| `…-hl-from-*-rd-motion*-close.png` | 39–41KB | **否决** — 运动区对象球近距 |
| `…-scatter-table.png` | 187093 | 散架全台旁证；无合格配套 cue-close |

### 其他目录

- `_min-retest-6c6b0b0/hl-fix/`：与 cut 中 v2 近距重复（含近空 cue-close-v2）。  
- `_github-handoff-ceshi-1-1/测试1.1/`：同 tip 拷贝，无更优母球近距。  
- `_g-roll-key-frames/`／`_g-roll-key2/`：属 tip `9fb9c5b` 旧键帧，**不**作 `6c6b0b0` G1 主证。

---

## 禁项自检

| 项 | 状态 |
|---|---|
| 改业务／高光代码 | 否 |
| 派 Codex／合 main | 否 |
| 重录视频／其他已合格项 | 否 |
| 声称产品 PASS／G-ROLL 关闭 | 否 |
| 以 cue-close-v2／scatter 近空充数 | 否 |

---

## 回报摘要

- **结论：EXTRACT_OK**
- **近距：** `…-hl-cue-close.png` · SHA256 `2f28a5984af26da3838e7b3d53ad8fce14318c6394d732595dc9f3dd31c0bdc4`
- **全台（裁切源）：** `…-pose-newmatch-initial.png` · SHA256 `fdc5100a94a63d466882ed5dbd4ea4d738c239a746564ba8739be8bf6303d4d3`
- **全台旁证：** `…-m3-checklist-fulltable.png` · SHA256 `face8b95c6842b566ffda05e27bec58f3a267ea8be9fa9f8bd25d8188fca9307`
- **NOTE：** `/workspace/billiards-playability/_g1-extract-6c6b0b0/G1-EXTRACT-NOTE.md`
