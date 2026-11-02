# 产品裁 · G1／G2 最小补证 · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 项 | 内容 |
|---|---|
| 角色 | **产品侧核验整理**；未改码／未派 Codex／未合 main |
| Tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（短 `6c6b0b0`） |
| 父 tip | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| 实际构建 | exe SHA **`7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E`** · size **272384** · mtime `2026-11-03T02:48:30+08:00` · **BIND_MATCH=True** · **未重编** |
| 用户开闸 | 仅 G1／G2 最小补证；换皮挂起；不重录其他已合格项 |
| **G-ROLL** | **仍暂不关** — 本裁＝补证齐备度；关闸交用户审核 |

---

## 产品结论

**G1／G2 最小补证证面＝有限通过（证据齐）**。  
PC VERIFY-COMPLETE ≠ 产品完整 PASS ≠ 授权关闸。

| ID | 来源 | 产品裁 | 说明 |
|---|---|---|---|
| **G1** | 已有包 EXTRACT_OK（不派补拍） | **有限通过（素材齐）** | 近距框到完整母球、明暗可辨；配全台裁切源；**≠** 解耦高光单独终裁（终裁交你目视近距） |
| **G2** | PC 新采连续窗 | **有限通过（链证齐）** | 单路 gdigrab **140.000s／4192 帧／无拼接**；seed→停→换手→回我方→瞄准→实出杆；seed/next 均 fired；朝向衔接终裁交你看连续 mp4 |
| **G3–G6** | 记录修正已落 | **记录已对齐** | partial＝4／6／7／10／14；cue-close-v2 未补齐旧说已纠；不派 PC |
| **G7** | 先前目视 | **已关闭** | 三轴 v2／nextfire／FALLBACK＝N/A |

**请你审核 G1 近距＋G2 连续窗后说：关／不关 G-ROLL。**

---

## G1 核验

| 项 | 结果 |
|---|---|
| 近距 | `_g1-extract-6c6b0b0/…-hl-cue-close.png` · 1204×816 · SHA `2f28a598…0bdc4` · **完整白母球＋可辨明暗** |
| 全台源 | `…-pose-newmatch-initial.png` · SHA `fdc5100a…03d4d3` · Crop 源像素全等 |
| 否决 | cue-close-v2／scatter 近空等 |
| 改码 | **无** |
| NOTE | `_g1-extract-6c6b0b0/G1-EXTRACT-NOTE.md` |

---

## G2 核验

| 项 | 结果 |
|---|---|
| BIND | tip／parent／exe／size／mtime 全匹配；禁 tip／禁 exe SHA 未触 |
| 连续窗 | `g-roll-g2-pose-seamless-6c6b0b0.mp4` · SHA `5B1898F2…45135` · **140.000s** · 4192 帧 · 单流 · **无拼接** |
| 链事实（PC） | seed fired pct=74 → 停 → handed 对手B1 → 回我方 → next aim → next fired pct=55 |
| zip | `g-roll-g2-pose-seamless-6c6b0b0-evidence.zip` · SHA `1559382A…E2D2` · size 5893666 |
| win-verify | `phase1-pc-wave7-batch1-g-roll-g2-pose-seamless-6c6b0b0-win-verify.md` |
| 改码／重编 | **无**；未重录三轴／既有 nextfire |

---

## 仍闸

| 项 | 状态 |
|---|---|
| 关 G-ROLL | **暂不关**（等你审核） |
| 合 main／μγ／真服／黑八胜／下一批 | **否** |
| Codex／改码 | **否** |
| 换皮 | **本轮挂起** |
| PC 本项 | **停手**（G1 不补拍；G2 已交） |

---

## 交付索引

- G1 目录：`/workspace/billiards-playability/_g1-extract-6c6b0b0/`
- G2 mp4／zip／bind／win-verify：`/workspace/billiards-playability/g-roll-g2-pose-seamless-6c6b0b0*`
- G3–G6：`phase1-pc-wave7-batch1-g-roll-6c6b0b0-g3-g6-record-fix-20261103.md`

---

| 时（Asia/Shanghai） | 内容 |
|---|---|
| 2026-11-03 ~05:20 | 产品核 G1 EXTRACT_OK＋G2 BIND／连续窗；裁＝证据齐有限通过；G-ROLL **仍不关**；交 PM 转用户定关；PC 停手 |
