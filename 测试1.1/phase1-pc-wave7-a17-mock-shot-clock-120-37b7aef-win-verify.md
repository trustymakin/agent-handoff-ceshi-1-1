# A17 · B mock 延钟隔离核验 · tip `37b7aef` · win-verify · 2026-11-04 Asia/Shanghai

| 项 | 内容 |
|---|---|
| OUTCOME | **PASS** |
| 测机 | `DESKTOP-OQUR45J` / `a8697f40-d1d2-4f9b-a183-5f06c4944b2b` |
| 执行 | 客户端PC · 隔离核验（编译／BIND／关=30／开=120／HOTSEAT=0） |
| tip FULL | `37b7aefd25ec67e289097a801e95289b02a39eee` |
| tip HEAD（worktree） | `37b7aefd25ec67e289097a801e95289b02a39eee` |
| 分支（远端） | `codex/mock-shot-clock-120-6c6b0b0`（**未**合 main／本地 worktree detached） |
| 父 tip | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（`hayo-pc-6c6b0b0-win-runtime` HEAD 保持不动） |
| 工作树 | `...\work\hayo-pc-37b7aef-win-runtime`（`git worktree add --detach`） |
| 编译 | `dotnet build ... -c Release -p:Platform=x64 -p:RuntimeIdentifier=win-x64` → **exit 0**（14 warning / 0 error） |
| exe | `...\clients\pc\src\FindTeammates.App\bin\x64\Release\net8.0-windows10.0.19041.0\win-x64\FindTeammates.App.exe` |
| exe SHA256 | `C274B9747C957D16DAD21538DB16846EA4F836CC5371ADE7C9E9BA9D112E8600` |
| exe size | `272384` |
| BIND | 已记；与父 tip `6c6b0b0` 旧 BIND `7B6B6B1B…DB2E` **不同**（新 tip 重建，符合预期） |
| auth | `phase1-pc-wave7-a17-mock-shot-clock-120-37b7aef-verify-auth-20261104.md` OPEN |
| handoff | `phase1-pc-wave7-a17-mock-shot-clock-120-37b7aef-handoff-20261104.md` |

## 明文禁令遵守

未重跑H／未空清／未合main／未升头／未改码

（本核验未启动 Plan H 观察／未空清席循环／未叫人打／未 merge main／未把默认 tip 升到 37b7aef／未改任何源码；G-ROLL 关；物理 C 停。）

## UI 钟面 AutomationId 说明

产品钟面控件为 `ClockText`（XAML `x:Name="ClockText"`，文案形如 `行动钟 N 秒`）。`ActionClockText` AutomationId **不存在**（读数 `<none>`）。本核验以 `ClockText`＝行动钟同源显示为准（与既有 A17/H 脚本一致）。

## 基线（MOCK_SHOT_CLOCK=0）

| 项 | 值 |
|---|---|
| env | `API_MODE=mock` · `HOTSEAT=0` · `MOCK_SHOT_CLOCK=0` |
| 入局 | mock OTP → 休闲小游戏 → 匹配开局 |
| ClockText 首读 | `行动钟 27 秒` @ **2026-11-04 04:00:40 +08:00**（入局后已过约 3s，贴近 30） |
| 倒计时采样 | 27→25→23→20→18→16→14（约 14s 墙钟，递减） |
| dai_da | **false**（全程未见「本机代打」） |
| 帧 | `frame-baseline30-t0-040040.png` / `frame-baseline30-tend-040054.png` |

## MOCK 开（MOCK_SHOT_CLOCK=1）

| 项 | 值 |
|---|---|
| env | `API_MODE=mock` · `HOTSEAT=0` · `MOCK_SHOT_CLOCK=1` |
| 入局 | 同 pattern；**未**空清席 |
| ClockText 首读 | `行动钟 117 秒` @ **2026-11-04 04:01:09 +08:00**（入局后已过约 3s，贴近 **120**） |
| 倒计时采样 | 117→115→113→110→108→106→104（约 13s 墙钟，递减；与 DurationSec/Remaining 同源显示） |
| 超时到 0 | **未**等满 120s 触发（硬令短观察／不等人打）；倒计时同源已由连续递减证明 |
| HOTSEAT=0 | 短观察 **未**自动翻「本机代打」充数：`dai_da=false`；TurnPill=`轮到你击球` |
| 帧 | `frame-mock120-t0-040109.png`（可见「行动钟 117 秒」）／`frame-mock120-tend-040123.png` |

## 证据路径

### box pack
`/workspace/billiards-playability/_a17-mock-shot-clock-120-37b7aef/`

- `phase1-pc-wave7-a17-mock-shot-clock-120-37b7aef-win-verify.md`（本文件）
- `exe-bind-37b7aef-mock-shot-clock.txt`
- `phase-baseline30-readings.txt` / `phase-mock120-readings.txt`
- `verdict-mock-shot-clock-120.txt`
- `launch-console-mock-shot-clock-120.txt`
- frames：`frame-baseline30-*.png` / `frame-mock120-*.png`
- `a17-mock-shot-clock-120-37b7aef-evidence.zip` SHA256 `757270E07774B11D0203F977BC81B7D7ED128EC42F9B9CE611823A994DB74D9A`

### Win shots
`C:\Users\ZYDN\Documents\Codex\2026-10-26\windows-hayo-pc-https-github-com\work\hayo-pc-37b7aef-win-runtime\shots-a17-mock-shot-clock-120-37b7aef\`

## OUTCOME

**PASS** — Release 编译 exit 0；BIND 新 SHA；关开关 ClockText≈30 递减；开开关 ClockText≈120 递减；HOTSEAT=0 未见本机代打；未重跑 H／未空清／未合 main／未升头／未改码。

产品／PM：核验 PASS → 可维持 tip 候选 `37b7aef`；**再开 H 须另令**。本代理不自行抄产品／PM。
