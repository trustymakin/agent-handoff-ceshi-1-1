# G3 本地定向 · 用户目视齐证清单 · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 项 | 内容 |
|---|---|
| 目的 | 用户定 A 后目视齐证；**未重开 G3 猎／未改码／未拼假单卷** |
| 产品催 | 补齐交清逐球＋录像＋槽帧＋zip |
| 本机更长连续原片 | **无**（Win `shots-a17-g3-targeted-local-6c6b0b0` 仅 primary／cont2／cont3 三卷，与已交一致） |
| DOC-SOFT | 主卷 `-t 1200` **未盖** #5＠19:29:10／#2＠20:00:24 墙钟；入袋以逐球表＋Hint＋槽帧为主证 |

---

## 1 · 逐球表终稿（无修订）

| 字段 | 值 |
|---|---|
| 路径 | `/workspace/billiards-playability/pocket-order-log-g3-targeted-local-6c6b0b0.md` |
| SHA256 | `29E1EEBE62D8916693AF937DD3F9835C9CC3139F97AE0B039054068D8AEB6616` |
| 修订 | **无**（与产品已核字节一致） |

| # | 墙钟 Asia/Shanghai | event | 球号 | 槽累计 | 落在哪段录像 |
|---|---|---|---|---|---|
| 1 | **19:29:10** | object_pocket | **#5** | `5` | **间隙**：primary 结束～cont2 开始（无该瞬间视频；有槽帧 after-1＋日志 Hint `进袋[5]`） |
| 2 | **20:00:24** | object_pocket | **#2** | `5,2` | **cont3** 墙钟窗内 |
| 3 | **20:19:28** | cue_scratch | — | `5,2` | 三段录屏皆已结束；有 end 槽帧 ge3＋日志 |

最终数组：`[5,2]` · count=2 · rematch=否 · inject=否 · shots=70 · rounds=1

---

## 2 · 录像路径＋SHA＋墙钟覆盖

| 段 | 路径 | SHA256 | size | 墙钟覆盖（约） |
|---|---|---|---|---|
| **primary（主）** | `/workspace/billiards-playability/phase1-pc-wave7-a17-g3-targeted-local-6c6b0b0.mp4` | `1896E52AFC019ACB89FA11B614A6919B1B769AE1DE2A17C9C76191D280508367` | 11795838 | **19:07:45–~19:27:45** |
| **cont2** | `/workspace/billiards-playability/phase1-pc-wave7-a17-g3-targeted-local-6c6b0b0-cont2.mp4`（同字节亦在 `_a17-g3-targeted-local-6c6b0b0/`） | `B81F25BB5841C4DF1D04B5B342BAE4AA2AF38F879D87F82AAC0FF6B18FAD6CD6` | 2359344 | **19:32:45–19:43:37** |
| **cont3** | `/workspace/billiards-playability/phase1-pc-wave7-a17-g3-targeted-local-6c6b0b0-cont3.mp4` | `470505EC5D535FC08DF2B7393890EAE24E9694C4E672B312061D2FA5E7E8607D` | 7309903 | **19:44:35–~20:09:35** |

入袋落段钉死：

- **#5＠19:29:10** → 不在 primary／cont2／cont3 任一连续文件内（DOC-SOFT 间隙）；主证＝槽帧 after-1＋pocket-order＋stdout `OBJECT_POCKET balls=5`
- **#2＠20:00:24** → **cont3**
- 三卷为同局**分段连续**录制，**未**拼接成假单卷

Win 原片同目录：`C:\Users\ZYDN\Documents\Codex\2026-10-26\windows-hayo-pc-https-github-com\work\hayo-pc-6c6b0b0-win-runtime\shots-a17-g3-targeted-local-6c6b0b0\`

---

## 3 · 槽帧

| 逻辑名 | 路径 | SHA256 | 墙钟（帧 mtime 约） |
|---|---|---|---|
| after-1（#5 入槽） | `/workspace/billiards-playability/_a17-g3-targeted-local-6c6b0b0/frames/a17-g3-slot-after-1.png` | `F0DA3CACFAB001BB85BA534F090EC8747E42FDB9ED899E02D091D0B4ADD10352` | ~19:29:13 |
| after-2（#5+#2） | `…/frames/a17-g3-slot-after-2.png` | `4C48A0E9096B02CFB730A21201AAAB2A62E9FF907CEC864F8EBAF1A3B8E23AED` | ~20:00:26 |
| ge3 终帧（仍仅 2 芯片／FAIL） | `…/frames/a17-g3-slot-ge3.png` | `22D29C3E38615A4EA8F2ADF03260B550D6C1E9EAD400A1BA6998BB28A8FDB322` | ~20:19:31 |

---

## 4 · evidence zip 终 SHA

| 字段 | 值 |
|---|---|
| 路径 | `/workspace/billiards-playability/phase1-pc-wave7-a17-g3-targeted-local-6c6b0b0-evidence.zip` |
| SHA256 | `092A335BF73545C792A6DB268D76D0ACDB22EB4220EBB94628BF93A14DFA15BF` |
| 修订 | **无**（与产品已核一致） |

旁证：win-verify SHA `B8A6212361B5C2BBA9646EAA574D329910CFCD76975EE507ED9FA6D4AF6F0B64`；原因索引 SHA `970728D6DAC8752FB67E2D8E87AA0E7D07AD9D2E2435356D83246DCD924AA743`

---

## 5 · 状态

齐证补交完毕。G3 FAIL 维持；A17 开；不改码；不开下一轮；等用户确认产品稳方案。
