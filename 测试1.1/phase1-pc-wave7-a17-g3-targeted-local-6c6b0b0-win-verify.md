# A17 G3 targeted-local retest · win-verify · tip `6c6b0b0` · 2026-11-03 Asia/Shanghai

| 字段 | 值 |
|---|---|
| Role | PC executor G3-only continuous-match hunt on **authorized local Win**；**不**冒充 product PASS |
| Auth nail | `/workspace/billiards-playability/phase1-pc-wave7-a17-g3-targeted-retest-auth-local-desktop-6c6b0b0-20261103.md` SHA256 `42feab5b175296c25ea8060cb691d7c2894846c740a0604a680c288ce1bd5f6b` |
| Machine | **DESKTOP-OQUR45J** · machineId `a8697f40-d1d2-4f9b-a183-5f06c4944b2b` · authorized occupy |
| Tip FULL | `6c6b0b07d6e2a4febbff4b4e6430df11b52ebc65`（短 `6c6b0b0`） |
| parent | `9fb9c5b3d2b9890677df549c3f15083452356dda` |
| exe | `...\hayo-pc-6c6b0b0-win-runtime\...\win-x64\FindTeammates.App.exe` |
| BIND sha256 | `7B6B6B1B3E36F7BFC19E91AD77E30204C2AAE281976ED75D088E3EDB3E6BDB2E` |
| BIND size | **272384** |
| BIND_MATCH | **True**（launch-time recheck + preflight） |
| API_MODE / HOTSEAT | mock / 1 |
| Ban check | DD02432A／ADAEB7F8／tip `5d6987f` **not used** |
| Client | ~1650×1080 dpi 144 |
| Pack | `a17-g3-targeted-local` · RCA §5 policy (nofire rematch threshold=999; settlement→abort; no G5) |
| Win shots | `C:\Users\ZYDN\Documents\Codex\2026-10-26\windows-hayo-pc-https-github-com\work\hayo-pc-6c6b0b0-win-runtime\shots-a17-g3-targeted-local-6c6b0b0\` |
| Box staging | `/workspace/billiards-playability/_a17-g3-targeted-local-6c6b0b0/` |
| Wall window | FFMPEG_START **2026-11-03 19:07:45 +08:00** → harness DONE **2026-11-03 20:19:32 +08:00** Asia/Shanghai |

## Verdict

| Gate | Result |
|---|---|
| **G3** | **FAIL** — max distinct object balls in **one continuous match** = **2** (`5,2`); need ≥3 |
| Rematch used | **No** (`rematch_used=False`, `rounds=1`, nofire threshold 999 / ALLOW_REMATCH=False) |
| Inject / force-pocket / preset | **No**（见下方 inject 单列） |
| Settlement mid-hunt abort | No（match stayed live through 70 shots） |
| G1／G2／G4／G5 | **Not retested** this pack；prior labels retained |
| A17 | **Still open**（G3 blocks） |
| G-ROLL | **Closed**（untouched） |
| PC product PASS | **Does not adjudicate** — evidence pack only |

## Pocket-order summary（same continuous match, round=1）

| # | wall (Asia/Shanghai) | mp4t (harness clock) | event | balls | rail L→R (event cum) |
|---|---|---|---|---|---|
| 1 | 2026-11-03 19:29:10 +08:00 | 21:25 | object_pocket | **5** | `5` |
| 2 | 2026-11-03 20:00:24 +08:00 | 52:39 | object_pocket | **2** | `5,2` |
| 3 | 2026-11-03 20:19:28 +08:00 | 71:43 | cue_scratch | 0 | `5,2` |

- Final `eventBalls` = `[5,2]` · count=2  
- Frames: `a17-g3-slot-after-1.png`／`a17-g3-slot-after-2.png`／fail end `a17-g3-slot-ge3.png`  
- Rest/handoff ≥3 check: **N/A** (never reached ≥3)

## Capture notes（continuous, unstitched segments）

Primary harness gdigrab (`-t 1200`) covered **19:07:45–~19:27:45**. Object pocket #5 at **19:29:10** and #2 at **20:00:24** fall **after** primary `-t` end; harness mp4t clock continued. Follow-on **cont2** (19:32:45–19:43:37, undersized Soft-Refresh rect) and **cont3** (19:44:35–~20:09:35) are **separate continuous** segments for the same match — **not** spliced into one file and **not** claimed as a single unstitched full-window reel. Pocket #5 sits in a short gap between primary end and cont2 start; still evidenced by frame `a17-g3-slot-after-1.png` + HintText log. Pocket #2 is inside cont3 wall window.

## Artifacts / SHA256

| Artifact | Path | SHA256 | size |
|---|---|---|---|
| win-verify | `/workspace/billiards-playability/phase1-pc-wave7-a17-g3-targeted-local-6c6b0b0-win-verify.md` | *(this file; see SHASUMS)* | — |
| pocket-order | `/workspace/billiards-playability/pocket-order-log-g3-targeted-local-6c6b0b0.md` | `29E1EEBE62D8916693AF937DD3F9835C9CC3139F97AE0B039054068D8AEB6616` | 618 |
| bind (Win launch) | `/workspace/billiards-playability/exe-bind-6c6b0b0-g3-targeted-local.txt` | `7D0909DE7CC45921FF3215C0485750ED5C35A7B02C4237DA9B63104FAB10FCCE` | 655 |
| primary mp4 | `/workspace/billiards-playability/phase1-pc-wave7-a17-g3-targeted-local-6c6b0b0.mp4` | `1896E52AFC019ACB89FA11B614A6919B1B769AE1DE2A17C9C76191D280508367` | 11795838 |
| cont2 mp4 | `_a17-g3-targeted-local-6c6b0b0/…-cont2.mp4` | `B81F25BB5841C4DF1D04B5B342BAE4AA2AF38F879D87F82AAC0FF6B18FAD6CD6` | 2359344 |
| cont3 mp4 | `_a17-g3-targeted-local-6c6b0b0/…-cont3.mp4` | `470505EC5D535FC08DF2B7393890EAE24E9694C4E672B312061D2FA5E7E8607D` | 7309903 |
| evidence zip | `/workspace/billiards-playability/phase1-pc-wave7-a17-g3-targeted-local-6c6b0b0-evidence.zip` | `092A335BF73545C792A6DB268D76D0ACDB22EB4220EBB94628BF93A14DFA15BF` | 20014529 |
| verdict | `_a17-g3-targeted-local-6c6b0b0/verdict-a17-g3-targeted-local.txt` | `60ED19A6327DB76612BDD3C59B4A5779AE078C991FF54D7AE134CD9C7B75D243` | 589 |
| slot-after-1 | `…/frames/a17-g3-slot-after-1.png` | `F0DA3CACFAB001BB85BA534F090EC8747E42FDB9ED899E02D091D0B4ADD10352` | 199348 |
| slot-after-2 | `…/frames/a17-g3-slot-after-2.png` | `4C48A0E9096B02CFB730A21201AAAB2A62E9FF907CEC864F8EBAF1A3B8E23AED` | 199645 |
| slot-ge3 (fail) | `…/frames/a17-g3-slot-ge3.png` | `22D29C3E38615A4EA8F2ADF03260B550D6C1E9EAD400A1BA6998BB28A8FDB322` | 174312 |
| launch-console | `…/logs/launch-console-a17-g3-targeted-local.txt` | `DBFFD24A12998602ABA112A85221E9C8ABE30E5C9EDD1B958E28CEB746046C15` | 443271 |

## Inject / preset / force section（required separate）

**Inject used: NO.**  
No force-pocket, no ball preset, no memory poke, no mock event injection. All pockets from normal physics + HOTSEAT UI automation pulls. Mock OTP login only (`13800000001` / `123456`) for app entry — not pocket inject.

## Cause（one paragraph）

G3 remains FAIL as a **coverage gap after an honest same-match hunt**: rematch/exit+new accumulation was disabled (nofire streak climbed past 8 without rematch; rounds stayed 1); 70 continuous shots over ~72 wall minutes pocketed only **two** distinct object balls (#5 then #2) into the rail; never reached ≥3 chips in「收球」, so multi-chip miss/overwrite remains **untested** and A17 stays open — no code change / no tip upgrade / no G5 / PC does not claim product PASS.

*Written 2026-11-03 Asia/Shanghai · executor G3 targeted-local*
