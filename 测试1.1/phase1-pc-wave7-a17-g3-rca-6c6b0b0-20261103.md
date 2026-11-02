# A17 G3 FAIL · Root-cause analysis · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 字段 | 值 |
|---|---|
| Role | **只读根因分析**（existing evidence only）；**未重测 G3**；**未改码／未派 Codex／未合 main** |
| Tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（短 `6c6b0b0`） |
| parent | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| exe SHA256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` · size 272384 |
| BIND | True · mock · HOTSEAT=1 · `exe-bind-6c6b0b0-a17.txt` SHA `159791DB…19C3` |
| 证据根 | `/workspace/billiards-playability/_a17-min-accept-6c6b0b0/` |
| Win shots | `...\shots-a17-pocket-rail-min-accept-6c6b0b0\`（machine `a8697f40-…`） |
| 主 mp4 SHA | `0F55803582D99B215EE90C352803B55479AEAEF5DBD1DA5F60971C60DD2A7310` |
| g3supp mp4 SHA | `6CB2D0FA183851CC7B6EC8BE0BD93598C2B9A89FDB2314EF262A7EB8833A2CFF` |
| g3retry mp4 SHA | `A06D7A97FFCA95FEFD1F61772AC02F0EAC72D757E5CED5DBE5A29DEFDB8E736A` |
| evidence zip SHA | `35854813189AF91E55C90BA6D4E4FEB2E2B6393B088E8601D755328768841AAD` |
| G1／G2／G4／G5 | **保持已标 PASS**（本 RCA 不改标签） |
| G3 | **FAIL 维持**；本 RCA 判定为 **覆盖缺口（②）**，非已证展示轨实现缺陷 |
| A17 最小包 | **仍开／未关**（G3 阻断） |
| G-ROLL | **保持关闭** |
| PC 裁定 | **不**冒充 product PASS；本文件＝产品卷宗根因分析 only |

**Primary classification: ② Scenario coverage gap（B）** — harness never achieved ≥3 distinct object balls remaining in the pocket rail within one continuous match. Display of a single chip (#3) was observed and is consistent with G1/G5 frames; multi-chip miss/overwrite is **not proven**.

---

## 1) Actual pocket events（ball # · time · rail）

> Sources: `pocket-order-log.md`／`pocket-order-log-g3retry.md`／`logs/harness-stdout.txt`／`logs/g3supp-stdout.txt`／`logs/g3retry-stdout.txt`／frames.  
> **Caveat on “rail L→R” column in pocket-order tables:** harness writes `railAfter = Join(eventBalls)` (cumulative HintText-parsed pocket IDs), **not** a live UIA enumeration of tray sprites. Visual confirmation uses frames + `chipEst` (often undercounts — see §2 nuance).

### 1.1 Main run（`a17-pocket-rail-min-accept-6c6b0b0.ps1`）

FFMPEG_START wall **06:05:09 Asia/Shanghai** · mp4 `phase1-pc-wave7-a17-min-accept-6c6b0b0.mp4`.

| # | mp4t | wall (Asia/Shanghai) | event | ball(s) | same-shot | rail L→R (event cum) | chipEst (UIA/bmp) | frame / log cite |
|---|---|---|---|---|---|---|---|---|
| 1 | 02:12 | ~06:07:21 | cue_scratch | — | 否 | *(empty)* | 0 | `harness-stdout` L110 `s03-dn CUE_SCRATCH … mp4=02:12`; frames `a17-g2-cue-pocket-event.png`／`a17-g2-slot-no-cue.png` |
| 2 | 06:00 | ~06:11:09 | cue_scratch | — | 否 | *(empty)* | 0 | L379 `s06-mid CUE_SCRATCH … mp4=06:00` |
| 3 | 06:59 | ~06:12:09 | **object_pocket** | **#3** | 否 | **`3`** | 0† | L405 `s07-top OBJECT_POCKET balls=3 cum=3 … mp4=06:59`; Hint `入袋[3]`; frames `a17-g1-pocket-in.png`／`a17-g1-slot-fill.png`／later `a17-g5-old-slot-occupied.png` |

† `chipEst=0` at observe time, but **visual** G1/G5 frames show exactly one chip **#3** in bottom「收球」tray — UIA/bmp estimator undercount (script itself allows “chipEst may undercount sprites”).

**Object balls pocketed in this continuous match: 1（only #3）.**  
No further `OBJECT_POCKET` after 06:12 through hunt end → G3 FAIL at **06:32:01** (`have=[3]`). Then G5 rematch (Exit-And-Rematch) wiped tray (expected for G5).

`pocket-order-log.md` SHA `C99E48B9CB3566464DC491F24F10FCDE8210D14102C77E55C6D4428F3B10D6D7`.

### 1.2 g3supp（`a17-g3-supp-6c6b0b0.ps1` · 06:35–06:52）

| # | mp4t | wall | event | ball(s) | rail L→R | notes |
|---|---|---|---|---|---|---|
| 1 | 01:26 | ~06:37:37 | cue_scratch | — | — | `g3supp-stdout` `s02 CUE_SCRATCH` |
| 2 | 05:07 | ~06:41:19 | cue_scratch | — | — | `s08 CUE_SCRATCH` |

**Zero `OBJECT_POCKET` lines.** Every shot header logged `have=0`. Run degraded near end (`SHOT_NO_PROC`／Automation `nullToObjectInvalidCast` in stderr) without ever pocketing an object ball. No supplemental pocket-order table was produced with object events.

mp4 SHA `6CB2D0FA…2CFF`.

### 1.3 g3retry（`a17-g3-retry-6c6b0b0.ps1` · 06:53–07:43）

FFMPEG_START wall **06:55:12** · secs=**780** (mp4 truncates ~07:08; script continued to 07:43 — post-cap events have mp4t but may be past file end).

| # | mp4t | wall | round | event | ball(s) | rail L→R (within-round cum) | cite |
|---|---|---|---|---|---|---|---|
| 1 | 05:11 | ~07:00:23 | **1** | object_pocket | **#10** | **`10`** | `g3retry-stdout` L366 `OBJECT_POCKET balls=10 cum=10 count=1` |
| — | — | ~07:10:51 | 1→2 | **NOFIRE_STREAK rematch** | — | **eventBalls RESET** (tray cleared by Exit-And-Rematch) | L1145; script lines 368–370 |
| 2 | 16:36 | ~07:11:48 | **2** | cue_scratch | — | *(empty after reset)* | L1175 |
| 3 | 17:51 | ~07:13:03 | **2** | cue_scratch | — | — | L1228 |
| 4 | 18:48 | ~07:14:00 | **2** | object_pocket | **#9** | **`9`** | L1258 `balls=9 cum=9 count=1` |
| — | — | ~07:32:37 | 2→3 | **NOFIRE_STREAK rematch** | — | **eventBalls RESET** | L2605 |
| 5 | 37:56 | ~07:33:08 | **3** | cue_scratch | — | — | L2635 |
| end | — | 07:43:22 | 3 | — | — | **`EVENT_BALLS=` count=0** | L3241–3246 `G3_RETRY_FAIL have=[] count=0` |

`pocket-order-log-g3retry.md` SHA `1EA87A5C0ED0E9BCE8DB104B37EF47AB72500DC49EC12DBC71074F8C37A577DE`.  
终帧 `a17-g3-slot-ge3.png` ≡ `a17g3r-g3-ge3-fail.png` SHA `2543995E…F8D7`：**收球槽空**（新局／未分彩 rack 在台，槽无芯片）.

**Max distinct object balls resident in rail in any single continuous match across all three runs: 1.**  
Cross-round union {10, 9, 3} is **not** valid G3 evidence — rematch intentionally clears tray (script comment: “Rematch clears tray, so RESET eventBalls on rematch”).

---

## 2) Meaning of `have=[3]` — nailed

**`have=[3]` means: the harness list `eventBalls` contains ball number 3 only (count = 1). It does NOT mean “three balls.”**

Proof chain:

1. **Verdict text** (`verdict-a17-min-accept.txt`):  
   `G3=FAIL :: fewer than 3 object balls pocketed; have=[3]`  
   simultaneously with `event_balls=3` (scalar = the single ID, not a count of three).

2. **Harness source** (`a17-pocket-rail-min-accept-6c6b0b0.ps1` ~L463–465):  
   ```
   else { Set-Result "G3" "FAIL" ("fewer than 3 object balls pocketed; have=[$([string]::Join(',', $eventBalls))]") }
   ```  
   Gate is `$eventBalls.Count -ge 3`. Bracket contents = **joined ball IDs**.

3. **Pocket parse** (`Parse-PocketedFromHint`): regex on HintText `…[([0-9,\s]+)]` → for Hint `入袋[3]` yields list `[3]` → one element.

4. **g3retry verdict NOTE** (`verdict-a17-g3-retry.txt` L7):  
   `NOTE=have=[3] in main verdict meant ball number 3 (count=1), not three balls`

5. **Visual**: `a17-g1-slot-fill.png`／`a17-g5-old-slot-occupied.png` show **one** chip labeled **3** in「收球」.

Ambiguity is **closed**. Any prior reading of “already have three” is incorrect.

---

## 3) Classification judgment

### Primary: **② Scenario coverage gap（B）**

G3 requires（acceptance-scope A17-03／ACE）: **≥3 distinct object balls in the pocket rail in one continuous match**, ball IDs checked, no miss/dup/overlap, then re-check after rest/handoff.

Across main + g3supp + g3retry:

| Run | Max object pockets in one continuous match | Rail ≥3 simultaneous? |
|---|---|---|
| Main | 1 (#3) | **No** — visual rail shows only #3 |
| g3supp | 0 | **No** |
| g3retry round1 | 1 (#10) | **No** — rematch wipe before 2nd object |
| g3retry round2 | 1 (#9) | **No** — rematch wipe |
| g3retry round3 | 0 | **No** — empty end frame |

Therefore: **coverage incomplete — not yet proven as a rail display/impl bug.**  
G3 remains **未完成／阻塞** pending a targeted continuous-match hunt that actually leaves ≥3 chips in「收球」before exit.

### Secondary nuance（does **not** flip primary to ①）

- `chipEst` stayed 0 even when frame shows chip #3 → harness tray estimator unreliable; script already documents undercount. **Not** evidence the UI failed to show the one pocketed ball.
- pocket-order “rail L→R” is event-cum, not sprite order read — G4 PASS on cum=`[3]` is consistent with single-event coverage, **not** multi-chip UI proof.
- g3retry rematch-on-`NOFIRE_STREAK≥8` / settlement **clears** tray by design → destroys accumulation needed for G3; this is a **harness strategy** issue relative to the G3 acceptance criterion, not a product rail overwrite bug (overwrite would require ≥3 chips first, then loss — never observed).

### Rejected as primary: **① Display/impl defect（A）**

No evidence that ≥3 object balls were pocketed in one continuous match while the rail failed to show/keep them (miss／overwrite／dup／clear). Single-chip display for #3 **worked** (G1/G5 frames). Multi-chip behavior is **untested**, not failed.

---

## 4) If impl（①）— N/A this cut

**Not applicable.** No read-only code localization, minimal fix, or impact scope proposed.  
**Do not edit** `clients/pc`／do not dispatch Codex／do not merge main — awaiting user auth only if a future continuous-match run proves ①.

(Optional future locus *if* ① is later proven: search Win worktree `...\hayo-pc-6c6b0b0-win-runtime\clients\pc\` for pocket-rail／tray／chip UI — deferred.)

---

## 5) Coverage（②）— 未完成／阻塞 + targeted retest plan

### Status mark

| 项 | 状态 |
|---|---|
| G3／A17-03 | **未完成／FAIL 维持** |
| 阻塞原因 | 三轮既有证均未在**同一连续对局**内把 ≥3 互异目标球留在收球槽；g3retry 用 rematch 清槽打断累积；瞄准／HOTSEAT 代打／nofire rematch 限制了覆盖 |
| A17 最小包关闭 | **否** |
| 改码／Codex | **未授权**（本 RCA 不请求） |
| 第三轮盲测 G3 | **禁止**（本 RCA 亦不执行） |

### Targeted retest plan（≠ blind G3 rerun）

Must **differ** from prior main／supp／retry:

1. **Stay in one match** until ≥3 distinct object pockets are logged **and** visually confirmed in「收球」.  
   - **Disable** (or raise far above 8) `NOFIRE_STREAK → Exit-And-Rematch` while `eventBalls.Count < 3`.  
   - On settlement mid-hunt: **do not rematch** for G3; prefer leave-settlement / continue same table if rules allow; if match truly ended, abort G3 as coverage miss rather than fake-accumulate across rematches.
2. **Force ≥3 object pockets before any exit/G5 path.** Do not start G5 rematch until G3 frames are banked.
3. **HOTSEAT seat control:** keep shooting seat that can legally pocket (avoid long proxy-only stretches); after suit split, aim only legal suit balls to raise pocket rate.
4. **Evidence gates before PASS:**  
   - pocket-order with ≥3 object rows, **same round**, rail cum length ≥3;  
   - frames: `a17-g3-slot-ge3.png` showing ≥3 chips with readable IDs;  
   - `a17-g3-slot-after-rest-or-handoff.png` after rest/hand-change with **same** set (no dup append);  
   - optional: human assist / longer aim catalog / lower power near pockets — still real physics, no force-pocket.
5. **Do not** claim ① from another failed hunt that never reaches ≥3 events. Only after ≥3 continuous-match pockets + mismatch vs tray may flip class to A and open read-only code locus.
6. Keep G1/G2/G4/G5 labels; G-ROLL closed; BIND tip `6c6b0b0` mock HOTSEAT; no main merge.

### Out of scope for retest opener

- Blind clone of `a17-g3-retry-6c6b0b0.ps1` with same rematch-on-nofire policy.  
- Code change to rail／tray.  
- Product PASS adjudication by PC.

---

## Evidence inventory (this RCA)

| Artifact | Path / SHA |
|---|---|
| Main verdict | `_a17-min-accept-6c6b0b0/verdict-a17-min-accept.txt` SHA `F96FC0B9…7C81` |
| g3retry verdict | `verdict-a17-g3-retry.txt` SHA `75C6E046…381D` |
| pocket-order main／retry | `pocket-order-log.md`／`pocket-order-log-g3retry.md`（SHAs above） |
| Logs | `logs/harness-stdout.txt`／`g3supp-stdout.txt`／`g3retry-stdout.txt` + launch-console twins |
| Frames | `frames/a17-g1-slot-fill.png`／`a17-g5-old-slot-occupied.png`／`a17-g3-slot-ge3.png` |
| win-verify／problems／product-cut | `phase1-pc-wave7-a17-pocket-rail-min-accept-6c6b0b0-win-verify.md`；`…-problems.md`；`…-product-cut-20261103.md` |
| Scripts | `a17-pocket-rail-min-accept-6c6b0b0.ps1`；`a17-g3-supp-6c6b0b0.ps1`；`a17-g3-retry-6c6b0b0.ps1` |

---

## One-paragraph cause（rollup）

G3 FAIL on tip `6c6b0b0` is a **scenario coverage gap**, not a proven pocket-rail display bug: `have=[3]` is ball **#3** with **count=1**; main＋g3supp＋g3retry never left ≥3 distinct object chips in「收球」inside one continuous match (retry’s #10 and #9 were wiped by harness rematch); single-chip UI for #3 is visually confirmed, so multi-chip miss/overwrite remains untested — mark G3 未完成／阻塞，targeted same-match ≥3 hunt only，no blind third run，no code edit.

*RCA · 2026-11-03 Asia/Shanghai · analysis only · A17 open · G-ROLL closed*
