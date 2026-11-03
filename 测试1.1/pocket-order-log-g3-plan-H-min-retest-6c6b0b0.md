# Pocket-order log · A17 G3 Plan H **最小补测** · tip `6c6b0b0`

**VERIFY ≠ product PASS.** Count rule: same-match · TurnPill=`轮到你*` · NOT `本机代打` · Hint contains `进袋[N]` · 槽=Hint.  
User self-report「进了8球」= **SELF-REPORT only**, **not** a cut basis — **do not** treat as verified count.

| 项 | 值 |
|---|---|
| seat_clear | **2026-11-04 02:25:22 +08:00** Asia/Shanghai · TurnPill=`轮到你击球` · Hint=`开球权随机 → A1` · has_proxy_dai_da=false |
| window parsed | seat-clear → REC_END (console + human-pocket-ledger + poll-only) |
| sources | `logs/launch-console-a17-g3-plan-H-min-retest.txt` · `logs/human-pocket-ledger.txt` · `logs/human-play-status.txt` |
| rematch / inject / Bump / PC cue | **none** |

## COUNTABLE (human A1) — countable_n=**1**

| # | wall (+08) | TurnPill | Hint (原文) | ball | 代打=false | decision |
|---|---|---|---|---|---|---|
| 1 | 2026-11-04 **02:27:08** | 轮到你击球 | 击球 进袋[14] · 连击 | **14** | yes | **COUNT** human A1 · slot=Hint (HUD text only; no slot-after-1 frame) |

**have list (verified):** `[14]`  
**countable_n:** **1** （＜产品门槛同局≥3可核）

## EXCLUDED 代打 / B1 window pockets

| wall (+08) | TurnPill | Hint (原文) | ball | reason |
|---|---|---|---|---|
| 02:26:18 | 轮到 对手B1 · 本机代打 | 击球 进袋[5] · 分彩 solid · 连击 | 5 | EXCLUDE B1/代打 |
| 02:26:52 | 轮到 对手B1 · 本机代打 | 击球 进袋[6] · 连击 | 6 | EXCLUDE B1/代打 |
| 02:28:16 | 轮到 对手B1 · 本机代打 | 击球 进袋[3] · 连击 | 3 | EXCLUDE B1/代打 |

## Other excluded (no pocket / proxy handoff)

- Multiple `轮到你击球` rows with Hint=`开球权随机 → A1` / `自由球已放置` / `击球 · 换手 → A1` / `超时仅换手 → A1` — **EXCLUDE no-pocket** or proxy handoff text (no `进袋[N]`).
- Multiple B1 `本机代打` rows with `已取消，未出杆` / `自由球已放置` / `超时仅换手 → B1` — **EXCLUDE** B1 window / 超时仅换手 proxy.

## Slot / tray isomorphism

- Auth requires `slot-after-N` + `tray-N` near-readable ball id matching Hint have order.
- This harvest: **no** in-play `slot-after-1` / `tray-1` captures. Post-hoc frames only (`frames/pocket14-approx-t2212s.png`, `final-hud-printwindow.png`, `primary-last-frame.png`).
- Ball **14** counted from **TurnPill+Hint console text only**; slot-frame visual isomorphism **not independently proven**.

## Honesty

- countable_n=**1** ＜ 3 → **does not meet** 同局≥3可核 product gate on facts.
- Self-claim 8 pockets ≠ verified.
