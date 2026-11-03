# Handoff · mock 行动钟 120s 开关 · tip `37b7aef` · 2026-11-04

| 项 | 内容 |
|---|---|
| 角色 | Codex工具人 · 本机 CLI 写码交付 |
| 模型 | **gpt-6.1-sol · Ultra**（session `01a1a2f2-c7b0-7962-aa19-08d4559c12e7`） |
| 父 tip | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` |
| 新 tip | **`37b7aefd25ec67e289097a801e95289b02a39eee`**（短 `37b7aef`） |
| 分支 | `codex/mock-shot-clock-120-6c6b0b0` @ trustymakin/hayo- |
| 对照 advice | SHA `6b9a5fef…9edc`／handoff `63f5b4e` |
| 禁 | **未**合 main／未升默认 tip／未真服／未黑八胜／未换皮 |

## Diff 摘要（3 files, +46/−5）

- `ApiClientSettings.cs`：`FINDTEAMMATES_BILLIARDS_MOCK_SHOT_CLOCK` + `BilliardsMockShotClockEnabled`（Live 恒 false；1/true/on/120→开）
- `BilliardsActionClock.cs`：`MockShotClockEnabledProvider`；开则 `DurationSec=120`；Remaining／Deadline／超时同源
- `BilliardsMatchPage.xaml.cs`：绑定 provider；文案／ShotClockSec 在开关开时对齐 120

## 如何开 mock 开关（PowerShell，同环境启客户端）

```powershell
$env:FINDTEAMMATES_API_MODE = "mock"
$env:FINDTEAMMATES_BILLIARDS_HOTSEAT = "0"
$env:FINDTEAMMATES_BILLIARDS_MOCK_SHOT_CLOCK = "1"
```

关延钟：未设或 `0`／`false`／`off` → 原 30s。

## 请产品

出核验包（编译／BIND／开关开时倒计时＝120 且超时同源；HOTSEAT=0）。**本交付不重跑 H**；再开 H 另令。

*本机 Codex CLI gpt-6.1-sol · Ultra · 2026-11-04 Asia/Shanghai*
