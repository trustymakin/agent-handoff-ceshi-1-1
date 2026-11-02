# 产品整理 · G-ROLL tip `6c6b0b0` · 合格证 ＋ 最小补测结果 · 2026-11-03 Asia/Shanghai

| 项 | 内容 |
|---|---|
| 角色 | **产品侧核验整理**（只读证包／写本裁稿）；**未改码／未派 Codex／未合 main** |
| Tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（短 `6c6b0b0`） |
| 父 tip | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| exe BIND | size **272384** · SHA256 **`7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E`** · mtime `2026-11-03T02:48:30+08:00` · **BIND_MATCH=True** · **未重编** |
| 清单 | `phase1-pc-wave7-batch1-g-roll-6c6b0b0-evidence-gap-min-retest-20261103.md` |
| 本包 win-verify | `phase1-pc-wave7-batch1-g-roll-min-retest-6c6b0b0-win-verify.md` |
| 本包 zip | `g-roll-min-retest-6c6b0b0-evidence.zip` · size **19158406** · SHA256 **`ED035A3397380694449C1E49BEC961AE59E30A59DAA30C4A1F1C5DEF84378B53`** ✓ 本机 `sha256sum`（原宣称 `823B142E…5077` 字节副本误删无法同 SHA 复原；Win 同次跑包＋HL v2 重交；**未重测／未重编**；裁结论不变） |
| 旧合格证引用 | `g-roll-remediation-6c6b0b0-evidence.zip` SHA `47316F42…AD5F440` |
| 用户口径 | 保留本版；**维持不关 G-ROLL**；不派 Codex／不改码；只用现有证目视、不重录已有合格证据；点缺项后再定；不合 main／μγ／真服／黑八胜／下一批 |

---

## 产品结论

**最小补测证面＝有限通过（证据补齐）**。  
PC「MIN-RETEST VERIFY-COMPLETE」≠ 产品完整 PASS ≠ 授权关闸。

相对清单 M1–M4：**证据缺口已按最小范围补齐**（旧失败选段已作废并重采；pose 含下一杆实击出；检查表已交；HL-FALLBACK＝N/A）。  
**G-ROLL-01／02 仍暂不关** — 须**用户目视**三轴 v2 录屏／pose nextfire／高光近距后再议关闸。

演示≠PASS。禁合 main／μγ／真服／黑八胜／下一批／Codex。

---

## zip／BIND 核验

| 项 | 结果 |
|---|---|
| zip SHA256 | 现主包 `ED035A33…84378B53` ✓；原 `823B142E…0E5077` 不可同字节复原（RESTORE） |
| zip size | 19158406 ✓ |
| tip／parent／exe | 与钉死一致；`BIND_MATCH=True`；≠`DD02432A…`／≠`ADAEB7F8…` ✓ |
| 环境 | mock＋HOTSEAT；1650×1080／dpi144 ✓ |
| mp4 SHA（抽核） | rh／rv／rd-axes-v2 与 win-verify 表一致 ✓；nextfire SHA `A3F3E684…` ✓ |
| 时长 | 三轴 v2 与 nextfire 均为 ~14s（ffprobe） |

---

## ① 已有合格证（继续保留，不必重采）

| 类 | 依据 |
|---|---|
| BIND／INIT／BALL-TYPES／SHADOW | 旧 remediation 证包＋本包 BIND 复核 |
| 三项代码路径 | `RasterizeSpherePrint`／`SampleBallAlbedo`＋`MakeLightingOverlay`／`_poseCache`（探针仍在；`MatrixTransform=False`；`ImageFailedHits=0`） |
| 旧 HL 抽样旁证 | 旧 zip 可引用（不作全覆盖主证） |

---

## ② 本补测结果（对照清单 M1–M4）

| ID | PC 标签 | 产品裁 | 证据强度 | 说明 |
|---|---|---|---|---|
| **BIND** | 通过 | **通过** | **有** | 钉死 tip／exe SHA；未重编 |
| **M1-AUDIT-OLD** | 失败 | **失败（作废）** | — | 旧 rh／rd-axes＝空杆／取消／无出杆后运动；**不可再当滚动主证** |
| **M1** | 通过 | **有限通过** | **有（静帧强／mp4 交用户目视）** | 三轴 v2 均 `fired=True` 且 maxWbDist≫30；`rd-motion1` 目视：散架＋条纹／全色＋相位 rolling；近距／半近距 crop 齐。**完整侧面→遮挡→转回**终判交用户看三支 mp4（产品未逐帧播放） |
| **M2** | 通过（主测 next hold 失败＋补测通过） | **有限通过** | **有** | 停球→换手→刷新静帧齐；补测 **next fired=True**（pct=55）＋`pose-chain-nextfire.mp4`；post-stop／handoff／refresh **SHA 互异**（非同字节空对照）。连续观感交用户看分段 mp4 |
| **M3** | 通过 | **有限通过** | **有／母球专用近距素材不足** | 检查表 cue＋1–15 均 visible；4／14＝partial（遮挡）。条纹／混聚近距 v2 可读。**`hl-cue-close-v2` ~6KB 近空＝未框到球面（专用近距素材不足）**；**≠已观察到实际渲染异常**。旁证可用 `hl-cue-close` v1／混聚／scatter，**不足以单独裁定解耦 PASS／FAIL** |
| **M4** | N/A | **N/A** | **不适用** | 台面无 `ImageFailed`／无资产失败分支；V4 仅 MiniBall。**不**作未测阻塞；**不**写成通过；不加回旧路径 |

### 关键 mp4（本包）

| 文件 | SHA256（短） | 用途 |
|---|---|---|
| `…-rh-axes-v2.mp4` | `E358AF74…A6A73C9` | 横轴实运动 |
| `…-rv-axes-v2.mp4` | `287D2DEB…C3AA2D` | 纵轴实运动 |
| `…-rd-axes-v2.mp4` | `3AEC5C42…E2741C1` | 斜轴实运动 |
| `…-pose-seed-fire.mp4` | `CCAEE0CE…` | M2 种子杆 |
| `…-pose-chain-handoff.mp4` | `4B4A06CD…` | 换手窗 |
| `…-pose-chain-nextfire.mp4` | `A3F3E684…C6238D` | **下一杆实击出** |
| `…-pose-chain-v2.mp4` | `0D7235A8…` | 主测换手／刷新（next 曾失败，旁证） |

---

## ③ 仍闸／不停手边界

| 项 | 状态 |
|---|---|
| 关 G-ROLL-01／02 | **维持不关**（用户目视站立；点缺项前勿自派） |
| 合 main／μγ／真服／黑八胜／下一批 | **否** |
| Codex／改码 | **否** |
| 重录已有合格证据 | **否** |
| PC 本项 | **停手**（无新硬派前勿自跑） |

---

## ④ 建议用户目视重点

1. **三轴 v2**：条纹＋全色是否真实滚动；号码／条纹侧面→遮挡→转回（背向可不强制见号）。  
2. **pose-chain-nextfire**：停球姿态是否带到换手／刷新后，且下一杆实击出而非空杆。  
3. **高光**：条纹／全色近距解耦观感；母球＝**专用近距素材不足**（`hl-cue-close-v2` 近空未框球面），**不是**已观察到渲染异常；旁证看混聚／scatter／v1，勿单独据此裁定解耦。  
4. 目视后**仅点剩余缺项**再定补证或修复；维持不关／不派 Codex（站立令 2026-11-03 ~04:37）。

---

## 变更

| 时（Asia/Shanghai） | 内容 |
|---|---|
| 2026-11-03 ~04:10 | 产品核 zip SHA／BIND／M1–M4；落本整理稿＝**证据补齐有限通过**；G-ROLL **仍不关**；交 PM 转用户目视；PC 停手；未改码／未派 Codex |
| 2026-11-03 ~04:37 | 对齐用户目视站立令：维持不关／不派 Codex／不重录合格证；母球高光改准＝**专用近距素材不足≠渲染异常**；主包 SHA 改记 `ED035A33…84378B53`（原 `823B142E…` 不可同字节复原）；裁结论不变 |
