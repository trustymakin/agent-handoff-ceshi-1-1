# A17 pocket-rail min-accept · win-verify · tip `6c6b0b0`

| 字段 | 值 |
|---|---|
| Tag | `phase1-pc-wave7-a17-pocket-rail-min-accept-6c6b0b0` |
| Machine | DESKTOP-OQUR45J (`a8697f40-d1d2-4f9b-a183-5f06c4944b2b`) |
| Recorded (Asia/Shanghai) | 2026-11-03 06:04 → 07:43:24（主测 06:04–06:32；g3supp 06:35–06:52；g3retry 06:53–07:43） |
| tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` |
| tip short | `6c6b0b0` |
| parent | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| exe SHA256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` |
| exe size | 272384 |
| BIND_MATCH | **True**（启动核＋本交付 closing 复核均匹配；mock + HOTSEAT） |
| API mode | mock |
| Product 全量关闭 | **否**（本批 ≠ A17 全量关闭；≠ product PASS） |
| Code change / Codex | 无／未派 |
| G-ROLL | 保持关闭（未重测） |

## G1–G5 结论（仅 PASS／FAIL／未测）

| 项 | 标签 | 摘要 |
|---|---|---|
| G1 | **PASS** | 合法目标球入袋事件成立；主测 pocket-order `#3` mp4t=06:59 ball=`3`；帧 `a17-g1-pocket-in.png` / `a17-g1-slot-fill.png` |
| G2 | **PASS** | 实际发生母球入袋（cue_scratch mp4t=02:12 与 06:00）；槽无白球芯片；帧 `a17-g2-cue-pocket-event.png` / `a17-g2-slot-no-cue.png` |
| G3 | **FAIL** | 全程未能在收球槽内稳定呈现 ≥3 颗**互异**目标球。主测 `have=[3]`＝球号 3（count=1），**不是**三颗球。g3supp 未达。g3retry 结束 `G3_RETRY_PASS=False` count=0；终帧 `a17-g3-slot-ge3.png`（=`a17g3r-g3-ge3-fail.png`）收球槽空。缺 `a17-g3-slot-after-rest-or-handoff.png`（未达 ≥3 故未拍）。详见 problems.md |
| G4 | **PASS** | 主测事件序 ↔ 槽序逐项一致（cum=`[3]`）；**同杆多球＝无；覆盖缺口保留**；不宣称全部顺序场景通过 |
| G5 | **PASS** | 路径=exit+new（Exit-And-Rematch）；旧局有球帧 → 进新局 → 新局空槽；`a17-g5-old-slot-occupied.png` / `a17-g5-enter-new-match.png` / `a17-g5-new-empty-slot.png` |
| A17-05 回置 | **未测** | 本批未触达 |
| A17-07 重连 | （后置，本批不测） | — |

## 同杆多球覆盖

**无；覆盖缺口保留。** 不宣称全部顺序场景通过。

## G3 奇义澄清（主测 FAIL 文案）

主测 verdict：`G3=FAIL :: fewer than 3 object balls pocketed; have=[3]`  
解读：`have=[3]` 为球号列表（仅球 **#3** 一颗），**不是**「已有 3 颗」。与 pocket-order-log 行 `#3 object_pocket balls=3` 一致。g3retry verdict 亦注明此点。

## G3 补测是否新开

- **本 executor 未新开** G3 全量／supp／retry。
- 到岗时 g3retry（`a17-g3-retry-6c6b0b0.ps1` + App pid 223276）仍在跑；**未杀**（非卡死），待其于 **07:43:24 Asia/Shanghai** 自行结束 → `G3_RETRY_PASS=False`。
- 此前已有 g3supp（06:35–06:52）。按「ONE focused then stop」：收获既有证＋该在途 retry，**不再第三轮**。

## 主测 pocket-order（嵌入）

见 `phase1-pc-wave7-a17-min-accept-6c6b0b0-pocket-order-log.md`：

| # | mp4t | event | balls | same-shot | rail L->R | chipEst | consistent |
|---|---|---|---|---|---|---|---|
| 1 | 02:12 | cue_scratch | 0 | 否 |  | 0 | Y(no-white) |
| 2 | 06:00 | cue_scratch | 0 | 否 |  | 0 | Y(no-white) |
| 3 | 06:59 | object_pocket | 3 | 否 | 3 | 0 | Y |

## g3retry pocket-order（旁证，不抬 G3）

见 `phase1-pc-wave7-a17-min-accept-6c6b0b0-pocket-order-log-g3retry.md`：跨 round 曾记 ball 10／9 单球入袋，但 rematch 清空后槽内从未同时 ≥3；终态 count=0 → 仍 FAIL。

## 证据路径与 SHA256

| 产物 | 路径 | SHA256 | size |
|---|---|---|---|
| win-verify | `/workspace/billiards-playability/phase1-pc-wave7-a17-pocket-rail-min-accept-6c6b0b0-win-verify.md` | （本文） | — |
| BIND | `/workspace/billiards-playability/exe-bind-6c6b0b0-a17.txt` | `159791DB8318D8BF4A37AFF8FA0B90A6D9732198612077C180DE58FE143F19C3` | 640 |
| 主 mp4 | `/workspace/billiards-playability/phase1-pc-wave7-a17-min-accept-6c6b0b0.mp4` | `0F55803582D99B215EE90C352803B55479AEAEF5DBD1DA5F60971C60DD2A7310` | 6349102 |
| g3supp mp4 | `_a17-min-accept-6c6b0b0/phase1-pc-wave7-a17-min-accept-6c6b0b0-g3supp.mp4` | `6CB2D0FA183851CC7B6EC8BE0BD93598C2B9A89FDB2314EF262A7EB8833A2CFF` | 6243531 |
| g3retry mp4 | `_a17-min-accept-6c6b0b0/phase1-pc-wave7-a17-min-accept-6c6b0b0-g3retry.mp4` | `A06D7A97FFCA95FEFD1F61772AC02F0EAC72D757E5CED5DBE5A29DEFDB8E736A` | 8491361 |
| evidence zip | `/workspace/billiards-playability/phase1-pc-wave7-a17-min-accept-6c6b0b0-evidence.zip` | `35854813189AF91E55C90BA6D4E4FEB2E2B6393B088E8601D755328768841AAD` | 21949312 |
| pocket-order | `phase1-pc-wave7-a17-min-accept-6c6b0b0-pocket-order-log.md` | — | — |
| problems | `phase1-pc-wave7-a17-min-accept-6c6b0b0-problems.md` | — | — |
| 帧目录 | `_a17-min-accept-6c6b0b0/frames/` | — | — |
| Win 原目录 | `...\shots-a17-pocket-rail-min-accept-6c6b0b0\` | — | — |

注：g3retry ffmpeg 约 780s 上限，mp4 落盘 ~07:08，脚本继续至 07:43；mp4 不覆盖 retry 全程后段。

## 页脚

本批＝G1–G5 最小验收 @ tip `6c6b0b0` mock Release。  
结束 ≠ A17 全量关闭；≠ 合 main；≠ product PASS。G-ROLL 关闭。未派 Codex、未改码。  
Labels only: PASS／FAIL／未测。

*交付 closing · 2026-11-03 07:45 Asia/Shanghai*
