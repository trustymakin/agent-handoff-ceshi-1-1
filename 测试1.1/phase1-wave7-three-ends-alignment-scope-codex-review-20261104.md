# Codex 只读审稿 · 三端对齐范围／TE-MIN · 2026-11-04

| 项 | 内容 |
|---|---|
| 角色 | Codex工具人 · **只读**；未改码／未派执行／未合 main |
| 审稿对象 | `phase1-wave7-three-ends-alignment-acceptance-scope-20261104.md` |
| 稿 SHA256 | `C444EADBB2328BB9DED80733FBA6D86B48D0ECE7072E98D089328461295EEA84`（与产品报 `c444eadb…` 一致；以该路径为准） |
| handoff | `a53194c`（产品报） |
| 本机 CLI | `/home/box/.local/bin/codex` 0.165.0 · ChatGPT device login |
| 实际 model＋effort | **gpt-6.1-sol · Ultra**；session `01a1a236-75be-7e32-8542-c0cf6bd6caa3` |
| 日志 | `/workspace/billiards-playability/phase1-wave7-three-ends-alignment-scope-codex-review-20261104.log` |
| 本建议 SHA | 见同目录 `.sha256`（以 `sha256sum` 本 md 为准） |

## 四问

1. **TE-MIN 基本够小，但需收紧。** 索引／静态核对可零改码完成；T1／T4 可选烟测混入盘点导致授权边界不清；证据须落到具体文件、位置与 tip。
2. **未见直接越界。** 换皮／bit-identical 终追／重开 A17／物理均已 OUT；但「前序依赖」易被误读为须重开前项；G-UI 不宜整体归为换皮视觉。
3. **A／B／C 分流够用，A 需改。** 「确认后开测授权」未钉用例；「盘点完成可含不足」与「关键契约缺证＝PARTIAL」须分开定义。
4. **改稿要点见下**（可直接粘贴）。

## 收紧结论

**建议改稿**：保留 TE-MIN，只收紧证据、完成判据和授权边界，再进确认。≠ 原样直接开测授权。

## 改稿要点（可粘贴）

- **IN／授权：**「TE-MIN 本轮为 T0–T6 只读盘点；T1／T4 烟测不随范围确认自动获准，须另列固定用例、各端 tip／产物绑定及预期证据后确认；确认前不派测。」
- **证据要求：**「每项按适用端记录具体文件路径及章节／行号、证据 tip、现行 tip、结论与缺口。BE／PC／安卓／iOS 均核历史证据至现行头的继承依据；祖先关系或未见相关 diff 仅作旁证，不自动记现行头 PASS。」
- **包级判据：**「ALIGN-INVENTORY-COMPLETE 仅表示 T0–T5 各适用端均有可定位证据或明确缺证记录。另列核验结论：关键契约缺证为 PARTIAL，已证实背离为 FAIL；盘点完成不代表全量或现行头通过。」
- **前序／OUT：**「A17 开／G3 FAIL、H 停、G-ROLL 关、物理 C 停观察原状维持，仅作背景与缺口旁证，不构成本包复测或重开授权。T3 仅索引残差锁测，T5 仅盘点既有 G0–G5／remarks。G-UI 本轮仅索引；交互项不等同换皮，换皮仍 last。」
- **文末 A 替换：**「A · 确认 TE-MIN 范围及只读盘点；不自动授权烟测、复跑、改码或重开既有闸。B／C 保留。」

## 是否立刻硬派测／端

**否。** 先改稿再进确认；确认前不派测。

*≠ 改码。交产品。*
