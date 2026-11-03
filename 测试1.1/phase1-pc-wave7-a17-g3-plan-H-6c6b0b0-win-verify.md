# A17 G3 · Plan H win-verify · tip `6c6b0b0` · Asia/Shanghai

| 项 | 值 |
|---|---|
| tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65` (short `6c6b0b0`) |
| BIND exe SHA256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` |
| BIND size | **272384** |
| BIND_MATCH | **true** |
| machine | DESKTOP-OQUR45J |
| machineId | `a8697f40-d1d2-4f9b-a183-5f06c4944b2b` |
| API_MODE / HOTSEAT | mock / 1 |
| player present | **yes** |
| REC_START | **2026-11-03 20:47:15 +08:00** (Asia/Shanghai) |
| REC_END | **2026-11-03 20:48:36 +08:00** (Asia/Shanghai) |
| rematch | **no** (PC did not click; Rematch UI seen=false) |
| inject | **no** |
| auto-scan / auto-cue / auto-fire | **no** |
| G3 result | **PASS_EVIDENCE** (PC does **not** claim product PASS) |
| G3 count | **3** |
| G3 have | `[15,13,12]` same continuous match |
| wall span | ~81 s (well under 60 min limit) |

## Inject section
**NO.** No force-pocket, preset, memory poke, or mock event injection. Mock OTP login only (`13800000001` / `123456`) for app entry. Observation = UIAutomation TextOf / PrintWindow screenshots only.

## Pocket order (same match)
1. `20:47:27` mp4t `00:13` → **15** (进袋[15] · 分彩 stripe · 连击)
2. `20:47:50` mp4t `00:36` → **13** (进袋[13] · 连击) · cum `15,13`
3. `20:48:31` mp4t `01:16` → **12** (进袋[12] · 连击) · cum `15,13,12`

After 3rd: tray-1/2/3 + rest-verify + handoff-verify frames captured.

## Continuous gdigrab primary — FAILED (honest)
- Intended: `plan-H-primary.mp4` continuous full-window gdigrab (`-t 3600`, no `-t 1200` truncate).
- Actual: file is **48-byte empty mdat** container (SHA256 `64D52708F594E8A1A3A4F76DEEF7275C8AD5184480C9473D8F60A0C9B6F4628B`).
- Root cause: ffmpeg launched via `ProcessStartInfo` with `RedirectStandardError/Output=true` **without a consumer** → encode stalled; stop left empty container.
- **Do not treat empty primary as play video.**

## Published video artifact
- `phase1-pc-wave7-a17-g3-plan-H-6c6b0b0.mp4` = **stills timeline** from ordered PNG frames (1 fps slideshow), SHA256 `89F10BB792D802F6CD70E2287677CBCC7A9D29842FB851972BE9772ECA4D5294`.
- Label: **NOT continuous play reel** — supplemental review only after gdigrab failure.
- Frame evidence (PNG) remains authoritative for tray/slot visuals.

## Frame SHAs
- `a17-g3-planH-slot-after-1.png` SHA256 `313647C1FDBA9BAF2E8B05B6B139F92F7FD2E8393066A25DAFB2A382305D79C2` size=325947
- `a17-g3-planH-slot-after-2.png` SHA256 `4A2F3F7F8CDFF0AE80BF7C8AC1E671D3988005741288E6DDD609724837153A7D` size=308856
- `a17-g3-planH-slot-after-3.png` SHA256 `64F28324B72B336EC1FCEB58578437DC42821D528EAA42F8AF38CE4BBFC5C1CA` size=314669
- `a17-g3-planH-tray-1.png` SHA256 `B1877601A0415BF17457E0F64FE605F1F87C81ABF9417B96A2E6F14D112C5022` size=312975
- `a17-g3-planH-tray-2.png` SHA256 `FAD6DAD7E092BE1F4E0316C5CB9F8A469AE157346ECD14FDA6864A7333737A7C` size=312980
- `a17-g3-planH-tray-3.png` SHA256 `94BDEFCB1DDB8E8AE61DBD6BF958216CD5A9308D47C6224C8A94086CBBD0F3AB` size=312987
- `a17-g3-planH-rest-verify.png` SHA256 `D1AEFAB8BEAF93942255617E0FEFDF67568838D59D0377BA5AE4A787CBD657CF` size=312900
- `a17-g3-planH-handoff-verify.png` SHA256 `3C849B5FE5DF02EE20900BA7DC0CA9D0FF2201F1E34A6D3AD42EFDBFFC7CCDF7` size=312964

## Other artifact SHAs
- bind `exe-bind-6c6b0b0-plan-H.txt`: `7CAF15FF8E1CA25B4E9D1795AE2CBDC927952DE71EDA5D2AFAA66979DF8793B7`
- pocket log `pocket-order-log-g3-plan-H-6c6b0b0.md`: `4580BF27656209EAA51776B990DD2A7D2B5E8F87A0FF10A39591E790A422B86D`
- stills mp4: `89F10BB792D802F6CD70E2287677CBCC7A9D29842FB851972BE9772ECA4D5294`
- empty primary container: `64D52708F594E8A1A3A4F76DEEF7275C8AD5184480C9473D8F60A0C9B6F4628B`

## Retention
G1/G2/G4/G5 not retested · A17 still open · G-ROLL closed · PC does not adjudicate product PASS.

## PC 收证复核（交裁前补钉 · 不冒充产品 PASS）

| 项 | PC 说明 |
|---|---|
| 连续全窗 gdigrab | **FAILED**（48B empty mdat）；见 `logs/mp4-primary-failure.txt` |
| 已发布 `.mp4` | **11s 静帧 slideshow**（`duration=11`），**不是**连续实况卷；勿当入袋窗录像 |
| 入袋号来源 | Observer 解析 **HintText** `进袋[15]/[13]/[12]` → have=`[15,13,12]` count=3 |
| 槽帧目视（人工） | `slot-after-3`／`tray-3` 底部收球与余球图标与 Hint 号 **不完全同构**（目视更像收球含 1／6／10／11／13 等；桌上仍可见花色球）。**以帧为准请产品目视裁定**，PC 不改 have 数组、不宣称 PASS |
| 打手／代打 | 入袋时刻 TurnPill 多为 **「轮到 对手B1 · 本机代打」**；PC **未**点力度／拉杆／出杆，但 mock HOTSEAT 对手座 **本机代打**＝游戏侧自动出杆。方案 H 口径是熟练**真人**打——此点请产品裁是否采信为人打证 |
| rematch／inject／PC 自动扫杆 | **no**（日志 `NO_AUTO_INPUT`；Rematch UI 未见） |
| REC | `20:47:15`→`20:48:36`（达 3 即停）；用户经 PM 报打完约 `20:51`（停录后） |
| A17／G-ROLL | A17 **未关**（待产品裁）；G-ROLL **关**；不合 main |

**PC 结论标签：** `EVIDENCE_HANDED` · internal observer `PASS_EVIDENCE` **仅表示** Hint 累计达 3，**不等于**产品 G3 PASS。连续录像缺口＋代打／槽目视分歧须产品裁。

