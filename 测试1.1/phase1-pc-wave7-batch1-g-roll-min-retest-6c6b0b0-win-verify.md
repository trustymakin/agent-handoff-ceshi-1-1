# Phase1 PC · Wave7 Batch1 G-ROLL **最小补测 M1–M4** · tip `6c6b0b0` · Win verify

| 项 | 内容 |
|---|---|
| 角色 | **客户端PC**（证据缺口补测；**不**产品裁定；demo≠PASS） |
| Tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（短 `6c6b0b0`；禁 `5d6987f`） |
| 父 tip | `9fb9c5b3d2b9890677df549c3f15083452356dda`（短 `9fb9c5b`）✓ |
| 机 | DESKTOP-OQUR45J · machineId `a8697f40-d1d2-4f9b-a183-5f06c4944b2b` |
| 工作树 | `...\work\hayo-pc-6c6b0b0-win-runtime`（detached @ tip） |
| 批时 | 2026-11-03 03:40–04:04 Asia/Shanghai（BIND 复核 → M1 三轴 → M2 主测失败补测 → M3/M4；测完 Kill；无 idle HOLD） |
| 清单 | `phase1-pc-wave7-batch1-g-roll-6c6b0b0-evidence-gap-min-retest-20261103.md` |
| 模式 | Release win-x64 · `FINDTEAMMATES_API_MODE=mock` · `FINDTEAMMATES_BILLIARDS_HOTSEAT=1` · OTP `13800000001`/`123456` |
| 探针 | `g-roll-min-retest-6c6b0b0.ps1`＋`g-roll-m2-supp-6c6b0b0.ps1`（UTF-8 BOM；`$N_CONTINUE`=继续对局）；**录屏在 hold 就绪后、Inj-Up 前启动**（修复旧选段窗口） |
| 边界 | **PC 不产品裁定**；标签仅 通过／失败／未测／阻塞／N/A；演示≠PASS；VERIFY-COMPLETE（本最小包）≠ 产品 PASS；**G-ROLL 仍未关闭**；未改码／未 Codex／不合 main；真服未测；合法黑八胜未测；未改 μ／γ／power-map |

## 包级结论

**MIN-RETEST M1–M4 VERIFY-COMPLETE** — BIND 复核匹配；M1 三轴新 mp4 有实击出后条纹＋全色运动；M2 经补测达到停球→换手→实际击出下一杆＋刷新／新局；M3 近距＋1–15＋母球检查表；M4＝N/A（不适用）＋代码依据。证交产品裁；**本包完成 ≠ 产品 PASS**；**G-ROLL 仍不关闭**。

可引用旧证包合格静帧：`g-roll-remediation-6c6b0b0-evidence.zip` SHA `47316F42B8542C6C66A2CD4D54B936694806D91080122A52C35E06640AD5F440`（INIT／SHADOW／部分 HL 抽样／pose-newmatch 等旁证）。

---

## BIND tip／exe 复核

| 项 | 实测 |
|---|---|
| HEAD | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` |
| 父 | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| Release exe | `...\win-x64\FindTeammates.App.exe` |
| size | **272384** |
| mtime | **2026-11-03T02:48:30+08:00**（Asia/Shanghai） |
| SHA256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` |
| BIND_MATCH | **True**（与清单钉死 SHA／size 一致；**未**重编） |
| BAN `9fb9c5b` exe | ≠ `DD02432A…` ✓ |
| BAN `93bfe45` exe | ≠ `ADAEB7F8…` ✓ |
| 窗口 | 客户区 **1650×1080** · dpiWin=**144** · mock + HOTSEAT=1 |
| 代码探针 | `ImageFailedHits=0` · `SampleBallAlbedo=True` · `RasterizeSpherePrint=True` · `_poseCache=True` · `MakeLightingOverlay=True` · `MatrixTransform=False` · `TryGetBallSpriteHits=2` · `MiniBallHits=4` |

**BIND = 通过**

重录：`exe-bind-6c6b0b0-min-retest.txt`（`recorded_at=2026-11-03T04:03:10+08:00` Asia/Shanghai）。

---

## 结果总表（仅 M1–M4）

| ID | 标签 | 关键事实 | 证据 |
|---|---|---|---|
| **BIND** | **通过** | tip／父链／SHA／size 与钉死 BIND 一致；禁冒充否；mock+HOTSEAT | exe-bind-min-retest；verdict |
| **M1-AUDIT-OLD** | **失败** | 旧 `rh-axes`／`rd-axes` 不可作滚动主证（见下自核） | 帧差审计＋用户核实 |
| **M1** | **通过** | 横／纵／斜三支 **v2** 新录屏：均 `fired=True` 且 maxWbDist≫30；sliding→rolling；条纹＋全色在运动静帧可见；近距／半近距 crop×8／轴 | `…-rh/rv/rd-axes-v2.mp4`＋`*-motion*`＋`*-near*` |
| **M2** | **通过** | 主测换手／刷新／新局仍在；**下一杆**主测 hold 失败后 **M2 补测**成功：seed fired→post-stop／handoff／refresh→**next fired=True**（pct=55）＋分段 mp4 | `m2-pose-*`＋`pose-seed-fire`／`pose-chain-handoff`／`pose-chain-nextfire`＋既有 `pose-*` |
| **M3** | **通过** | 母球＋条纹＋全色可辨近距（v2 补齐）；1–15＋母球检查表；全台／运动旁证 | `hl-*-close`／`hl-*-close-v2`／checklist／`rh-motion1` |
| **M4** | **N/A** | 不适用（台面路径）；**勿写成通过** | 见 §M4 |

### 包级

| 包级 | 判定 |
|---|---|
| **MIN-RETEST VERIFY-COMPLETE** | M1–M4 行齐；demo≠PASS；≠产品 PASS；G-ROLL 仍不关闭 |

---

## M1 · 三轴实运动滚动录屏

### 旧轴自核

| 介质 | 结论 |
|---|---|
| `g-roll-remediation-6c6b0b0-rd-axes.mp4` | **失败**。用户密集帧核实＝无有效出杆后球体运动；本机复审：duration=16s bitrate≈121kbps；P/B skip≈99%；帧差 max≈0.85；画面为瞄准／取消（「已取消，未出杆」）满架未散。选段／窗口失败。 |
| `g-roll-remediation-6c6b0b0-rh-axes.mp4` | **失败（不可作 M1 主证）**。帧差早期近静；尖峰对应 UI 换手／自由球；抽帧见犯规自由球态且 **三角架仍完整**（无出杆后目标球散架滚动）。空杆／窗口／未击出类失败。 |
| 根因 | 旧脚本 **先 Start-GdiGrab 再 Calibrate-Pull**，校准耗时长，录屏窗口落在瞄准／取消／空窗，未盖住出杆后运动。 |
| 本包修复 | **hold 就绪（松手出杆）后才 gdigrab**，随即 Inj-Up；大力开球 75–90%；轴间 rematch。 |

### 新交 v2

| 轴 | pct | aim | fired | maxWbDist | 相位摘要 | mp4 | size | SHA256 |
|---|---|---|---|---|---|---|---|---|
| **R-H** | 87 | 358° | True | 643 | sliding→sliding→rolling→rolling | `g-roll-min-retest-6c6b0b0-rh-axes-v2.mp4` | 252776 | `E358AF74FCDFB46949FA5ABC5497B2F87FFAC9C2703484029BD58E9F3A6A73C9` |
| **R-V** | 80 | 318° | True | 529 | sliding→rolling→rolling | `g-roll-min-retest-6c6b0b0-rv-axes-v2.mp4` | 245743 | `287D2DEBED1455F1F4916017C35D4122E6A83916DE79E66D1665B3DCB2C3AA2D` |
| **R-D** | 86 | 332° | True | 647 | sliding→rolling→rest | `g-roll-min-retest-6c6b0b0-rd-axes-v2.mp4` | 270894 | `3AEC5C421F2FFC531CD1C507DB735D2B0FE98D3FC0977541DB4184FD4E2741C1` |

本机 v2 帧差抽检（fps=5）：rh max≈11.4／rv max≈4.6／rd max≈11.1（对比旧 rd max≈0.85）。`rh-motion1` 等静帧可见散架后 **条纹（9/10/11/12/13/15…）＋全色（1/2/3/5/6/7/8…）**；号码／条纹随姿态转侧面遮挡可观察（不强制背面号码）。每轴 near／halfnear crop×8。

**M1 = 通过**（PC 事实标签；demo≠PASS）

---

## M2 · pose-chain 连续

### 主测（同会话）

- `pose-post-stop`／`pose-after-handoff`（handed=True，`轮到 对手B1 · 本机代打`）／`pose-after-refresh`／`pose-before-next`／`pose-newmatch-initial*` 已采。
- `pose-chain-v2.mp4`（SHA `0D7235A8…`）覆盖换手／刷新窗；**下一杆**在散架桌短拉杆未进「松手出杆」→ `posenext hold_fail` → 主测曾标失败。

### 补测 `g-roll-m2-supp`（同 BIND／同 tip／同 exe；Asia/Shanghai ~03:57–04:01）

| 步 | 事实 |
|---|---|
| seed | pct=74 aim=357 fired=True maxWb=806；`pose-seed-fire.mp4` SHA `CCAEE0CE…` |
| post-stop | turn 已换手 `轮到 对手B1 · 本机代打`；`m2-pose-post-stop` |
| handoff | handed=True；`m2-pose-after-handoff`；`pose-chain-handoff.mp4` SHA `4B4A06CD…` |
| soft refresh | `m2-pose-after-refresh` |
| before-next | turn=`轮到你击球` |
| **next fired** | pct=**55** fired=**True** maxWbDist=262 phases=sliding→rest；`pose-chain-nextfire.mp4` SHA `A3F3E6840782528CA7859B0843CE839BC155EFF3021D4DF92B2496B8D4C6238D`；stills `m2next-motion*`／`m2-pose-next-fired-motion` |
| newmatch | `m2-pose-newmatch-initial*` 满架 |

对照说明（PC 观察事实，非产品 PASS）：换手前后号码朝向无「11／13／15 一并回正」类群体跳变旁证；soft refresh 保持；下一杆运动首帧非满架集体重置。连续链以 **timestamped 分段 mp4**（seed-fire → handoff → nextfire）＋静帧交代。

**M2 = 通过**（主测换手／刷新／新局＋补测 next-fired；demo≠PASS）

---

## M3 · 高光近距＋全覆盖检查表

| 项 | 事实 |
|---|---|
| 近距 | `hl-cue-close`（母球）；`hl-stripe-close`／`hl-stripe-close-v2`（条纹 13 等）；`hl-solid-close-v2`／`hl-cluster-close-v2`／`hl-rd-solid-stripe-close-v2`（全色＋条纹混聚；印刷朝向各异时高光斑相对球冠／屏幕方位可观察） |
| 注 | 初裁 `hl-solid-close`（init 坐标）近空 → **已用 motion 帧 v2 补齐**；不以空 crop 充数 |
| 检查表 | `m3-ball-coverage-checklist-6c6b0b0.txt`：cue＋1–15 逐号 visible／HL_readable／notes；partial＝遮挡／角度非缺素材 |
| 全台旁证 | `m3-checklist-fulltable`／`pose-newmatch-initial`／`rh-motion1`／`scatter-table` |
| 禁 | 未造 HL-FALLBACK 缺图；未测 MiniBall／HUD 芯片 |

**M3 = 通过**（PC 事实；demo≠PASS）

---

## M4 · HL-FALLBACK

| 项 | 内容 |
|---|---|
| 标签 | **N/A（不适用）** — **不要**写成「通过」 |
| 代码依据摘要（pack §② · tip `6c6b0b0` · `BilliardsMatchPage.xaml.cs`） | ① 全文件 **`ImageFailed` 命中＝0**（旧 `ImageFailed`→`MakeBallPrint` 回退已移除）。② `SampleBallAlbedo`：台面球 **0–15＋母球** unlit 程序化材质，**no V4 PNGs, baked highlights, … or asset-failure branch**。③ `MakeBall`：可见 albedo 全在球面盘；MiniBall HUD 可仍用 V4，**台面球面从不采样那些 PNG**。④ `TryGetBallSprite`／V4 `ball-{id}.png` **仅** `MiniBall`（HUD／收球槽芯片）调用（探针 TryGetBallSpriteHits=2／MiniBallHits=4）。 |
| 范围 | HUD／收球槽用图另属范围（本补证不测、不挡）。 |
| 禁 | 未加回旧回退代码；未派 Codex；未把 N/A 写成通过。 |

**M4 = N/A**

---

## 证据包

| 项 | 内容 |
|---|---|
| zip | `/workspace/billiards-playability/g-roll-min-retest-6c6b0b0-evidence.zip` |
| size | **19174446** |
| SHA256 | `823B142ED17773D003F08F8A7BFF238B60A0680B8DE7F28BC0DD1DB3770E5077` |
| 内含 | 新 mp4（rh/rv/rd-axes-v2＋pose-seed-fire／handoff／nextfire／pose-chain-v2）＋运动／近距／HL v2＋checklist＋exe-bind 重录＋verdict／launch-console／脚本 |
| 旧证引用 | `g-roll-remediation-6c6b0b0-evidence.zip` SHA `47316F42…AD5F440`（合格静帧可复用，不必整包重打） |

### 录屏 SHA（本包）

| 文件 | size | SHA256 |
|---|---|---|
| `g-roll-min-retest-6c6b0b0-rh-axes-v2.mp4` | 252776 | `E358AF74FCDFB46949FA5ABC5497B2F87FFAC9C2703484029BD58E9F3A6A73C9` |
| `g-roll-min-retest-6c6b0b0-rv-axes-v2.mp4` | 245743 | `287D2DEBED1455F1F4916017C35D4122E6A83916DE79E66D1665B3DCB2C3AA2D` |
| `g-roll-min-retest-6c6b0b0-rd-axes-v2.mp4` | 270894 | `3AEC5C421F2FFC531CD1C507DB735D2B0FE98D3FC0977541DB4184FD4E2741C1` |
| `g-roll-min-retest-6c6b0b0-pose-seed-fire.mp4` | 235855 | `CCAEE0CEFB65895CFB738A63CAFBF11CC1A2E472ECAD381A718F88520E9DDE1F` |
| `g-roll-min-retest-6c6b0b0-pose-chain-handoff.mp4` | 618147 | `4B4A06CDD7872351C9B27359C917132C627E89E7D84BBDB4481CCAEA1922A0DD` |
| `g-roll-min-retest-6c6b0b0-pose-chain-nextfire.mp4` | 229567 | `A3F3E6840782528CA7859B0843CE839BC155EFF3021D4DF92B2496B8D4C6238D` |
| `g-roll-min-retest-6c6b0b0-pose-chain-v2.mp4` | 1007937 | `0D7235A8C93754E0DDBA330E2C47826CD6B22BE4503A24E81B89245B848C438D` |

---

## 禁项自检

| 项 | 状态 |
|---|---|
| 合 main | 否 |
| 写产品代码／Codex | 否 |
| 真服 | 否（mock） |
| 合法黑八胜终测 | 否 |
| 改 μ／γ／power-map／停稳 | 否 |
| 旧 `9fb9c5b`／`93bfe45` exe SHA 冒充 | 否 |
| tip `5d6987f` | 否 |
| SHA 漂移后假重编冒充 | 否（SHA 匹配；未重编） |
| demo＝PASS／产品 PASS | 否；仅最小包 VERIFY-COMPLETE；**G-ROLL 仍不关闭** |
| HL-FALLBACK 假通过 | 否（N/A） |
| idle HOLD | 否（Kill-App） |

---

## 变更

| 时（Asia/Shanghai） | 内容 |
|---|---|
| 2026-11-03 ~03:40–03:50 | BIND 复核匹配；M1 三轴 v2 实运动；M2 主测换手／刷新／新局；下一杆 hold 失败；M3／M4 |
| 2026-11-03 ~03:57–04:01 | M2 补测：seed→handoff→refresh→next fired；Kill |
| 2026-11-03 ~04:03–04:04 | exe-bind 重录；HL v2 近距补齐；evidence zip＋本 win-verify |
