# A17 min-accept problems · tip `6c6b0b0` · 2026-11-03

## 仍 FAIL

### G3 · ≥3 目标球入槽 · 无漏／无重／无重叠（A17-03）

| 项 | 内容 |
|---|---|
| 现象 | 收球槽内未能稳定出现 ≥3 颗互异目标球芯片；终态为空槽或仅单号 |
| 主测 | `verdict-a17-min-accept.txt`：`G3=FAIL :: fewer than 3 object balls pocketed; have=[3]` → **球号 3 一颗**（count=1），非三颗 |
| g3supp | 06:35–06:52；未达 ≥3（stdout 过程 `have=0`） |
| g3retry | 06:53–07:43；`verdict-a17-g3-retry.txt`：`G3_RETRY_PASS=False` count=0；终帧 `a17-g3-slot-ge3.png` 收球槽空。跨 round 日志曾记单球 10／9，但 rematch 后未累积到 ≥3 |
| 复现 | BIND tip `6c6b0b0` mock HOTSEAT → 登录匹配 → 手操／harness 拉杆入袋；主测＋supp＋retry 均未在同一连续局内把 ≥3 互异目标球留在收球槽 |
| 期望 | 槽内 ≥3 互异目标球；球号与入袋集合一致；停球／换手后不重复追加；有 `a17-g3-slot-ge3.png` + `a17-g3-slot-after-rest-or-handoff.png` |
| 实际 | 未达 ≥3；缺 after-rest／handoff 帧；G3=**FAIL** |
| 影响 | G3 FAIL；**不挡**本批已 PASS 的 G1／G2／G4／G5 标签，但本批整体不可宣称 A17 最小验收全绿 |
| 证据 | 主 mp4 SHA `0F558035…`；g3retry mp4 SHA `A06D7A97…`；`a17-g3-slot-ge3.png`；`pocket-order-log.md`；`pocket-order-log-g3retry.md`；`logs/launch-console-a17-g3-retry.txt` |

## 口径提醒（非缺陷）

- 同杆多球：**无；覆盖缺口保留**（G4 已写明）。
- A17-05 回置：**未测**。A17-07 重连：后置。
- ≠ product PASS；≠ A17 全量关闭；G-ROLL 关闭；未改码／未派 Codex。

*问题清单 · 失败先交证 · 2026-11-03 07:45 Asia/Shanghai*
