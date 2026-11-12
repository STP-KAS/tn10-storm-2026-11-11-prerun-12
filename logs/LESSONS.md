> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value. Pre-run 12.
>
> **Our own testing.** This is our own Kaspa Testnet-10 testing, run on our own machines and nodes. What this page reports is what we observed in this run; it is not a claim of how TN10 or Kaspa behave in general.

# Lessons, pre-run 12

> Written by the operator after RETURN closed and the counter's tail was read. [METHOD.md](METHOD.md) is the desk runner's own summary; its last section, the reading against the selection rule and the label fix, was added by the operator afterwards. Hops are the desk counter's read of the desk's private TN10 node ([counts/chain/TIMELINE.md](../counts/chain/TIMELINE.md)), checked against a kept public kaspad every 10 s. Mempool, ready-set and template figures are the read-only probe on the same node ([counts/chain/MEMPOOL.md](../counts/chain/MEMPOOL.md)), every 20 s, one median per minute. They are one node's view, not a network-wide figure. The probe's template is the desk node's own `getBlockTemplate`, never submitted.

## The question

What fee keeps a covenant chain moving when it competes with heavy same-fee outside transactions in the mempool? Pre-run 11 had tied the floor's slowdown to another TN10 sender's chained stream of heavy transactions (about 267,000 storage mass each, exactly 100 sompi/gram). Pre-run 12 put the sixteen families on five rates near the floor, all on the desk's private node, one build, one builder: floor (families 1–4) 100, r110 (5–7) 110, r126 (8–10) 126, r150 (11–13) 150, r200 (14–16) 200 sompi/gram. No payment load of ours. We did not attribute the outside stream to anyone.

## What happened

Every step was an `OBSERVATION`; nothing was scored. Every minute was clean, no repair, the runner was not restarted, nothing was killed, no `FAILED` file was written, and the desk node was not stopped. Every desk count file, the timeline, the mempool timeline and the method file reached origin on the first try.

| Step | Whole minutes | Desk file on origin (UTC), commit | Mini file, commit |
|---|---:|---|---|
| BASE | 8 (10:40–10:47Z) | 10:48:22Z, aaaddd5 | d2baff3 |
| HOLD-1 = OBS-1 | 12 (10:49–11:00Z) | 11:01:22Z, e98467e | 19c165f |
| HOLD-2 = OBS-2 | 12 (11:02–11:13Z) | 11:14:22Z, 16d6188 | d5e247b |
| HOLD-3 = OBS-3 | 12 (11:15–11:26Z) | 11:27:22Z, ac9a627 | 95c0bdb |
| HOLD-4 (pinned 11:31Z) | 1 | 11:32:23Z, 608d98b | b7875c5 |
| RETURN | 8 (11:33–11:40Z) | 11:41:21Z, 6c0c3df | 1fb4bf2 |

The bot filed `NO SEND no-free-node` for HOLD-4 (d5b4fe8, on origin 11:32:04Z): its free-node check at 11:30:31Z found only the desk's two kept kaspads. The families stopped at 11:41:24Z. After the 5-minute tail the runner published the timeline (bfbd30a, 11:46:33Z), the mempool timeline (d432d12, 11:46:36Z) and its method file (3d7477a, 11:46:38Z) and ended at 11:46:41Z.

Family hops landed over the whole run (desk counter totals, start to tail): floor 9,239, r110 7,130, r126 7,516, r150 7,915, r200 8,640; 40,440 in all. Every OK hop landed in every step. No payment of ours was offered.

**The control came on its own.** The outside heavy stream was in the desk mempool in every minute of the run except 11:02–11:11Z (ten whole minutes inside OBS-2): 0 outside fee-100 entries, ready mass 0.58–1.54 blocks, and the node's own template held no heavy transaction. It came back at 11:12Z (35 entries) and stayed to the end. Outside of that window it was lighter than in pre-run 11: 3–35 entries at fee 100, median 8, all of them heavy (mean mass about 266,000–266,600), ready mass 1.3–12.1 blocks.

## Hops per family, per step

Floor has four families, the others three, so every figure below is **per family**: sum of the step's minutes divided by the family count, then per minute (sum per cohort in brackets).

| Step (minutes) | Floor 100 | R110 | R126 | R150 | R200 | Ready mass, blocks | Outside heavy at 100 |
|---|---:|---:|---:|---:|---:|---|---|
| BASE (8) | 41.2 (1,317) | 42.0 (1,007) | 43.6 (1,046) | 45.0 (1,081) | 47.8 (1,147) | 2.4–6.0 | 3–12 |
| OBS-1 (12) | 38.8 (1,862) | 39.5 (1,421) | 41.8 (1,503) | 43.9 (1,582) | 48.2 (1,737) | 4.0–8.3 | 5–13 |
| OBS-2 (12) | 44.3 (2,126) | 45.1 (1,625) | 45.6 (1,640) | 46.7 (1,682) | 48.1 (1,733) | 0.6–12.1 | 0 for 10 minutes, then 35, 17 |
| OBS-2, the ten stream-absent minutes | 48.6 | 48.7 | 48.9 | 49.3 | 50.1 | 0.6–1.5 | 0 |
| OBS-3 (12) | 34.2 (1,641) | 35.6 (1,283) | 38.0 (1,368) | 40.5 (1,459) | 44.7 (1,610) | 4.0–10.1 | 5–15 |
| HOLD-4 (1) | 32.0 (128) | 32.0 (96) | 36.7 (110) | 40.3 (121) | 44.3 (133) | 9.3 | 15 |
| RETURN (8) | 30.5 (976) | 32.5 (779) | 35.6 (854) | 38.3 (920) | 44.0 (1,055) | 3.5–8.7 | 4–12 |

Median submit-to-landing per hop, ms (p95 in brackets), from the step files:

| Step | Floor | R110 | R126 | R150 | R200 |
|---|---|---|---|---|---|
| BASE | 1,164 (2,191) | 1,145 (2,136) | 1,115 (1,985) | 1,080 (1,884) | 1,040 (1,635) |
| OBS-1 | 1,177 (2,701) | 1,150 (2,649) | 1,122 (2,268) | 1,099 (2,182) | 1,019 (1,783) |
| OBS-2 | 1,063 (1,656) | 1,071 (1,665) | 1,057 (1,650) | 1,057 (1,651) | 1,031 (1,622) |
| OBS-3 | 1,243 (3,676) | 1,216 (3,488) | 1,198 (2,786) | 1,161 (2,460) | 1,099 (1,969) |
| HOLD-4 | 1,207 (4,324) | 1,209 (5,355) | 1,204 (3,803) | 1,119 (2,458) | 1,090 (2,220) |
| RETURN | 1,366 (4,273) | 1,318 (3,782) | 1,281 (3,260) | 1,218 (2,894) | 1,123 (1,970) |

## Tiers against the ready mass and the outside stream

Per-family hops a minute, median over the minutes in each row, and in brackets as a share of the same tier's rate in the stream-absent control (11:02–11:11Z). The control is the reference rate here: this run's BASE already had the stream in it, so BASE is not a clean reference.

| Minutes | n | Floor 100 | R110 | R126 | R150 | R200 |
|---|---:|---:|---:|---:|---:|---:|
| Stream absent, 11:02–11:11Z (control) | 10 | 48.9 (100%) | 48.7 (100%) | 48.5 (100%) | 48.8 (100%) | 49.5 (100%) |
| Stream present, all | 43 | 37.2 (76%) | 37.3 (77%) | 40.0 (82%) | 42.3 (87%) | 45.7 (92%) |
| Stream present, ready mass ≤ 3 blocks | 4 | 41.0 (84%) | 42.3 (87%) | 42.8 (88%) | 44.8 (92%) | 46.3 (94%) |
| Stream present, 3–6 blocks | 24 | 39.2 (80%) | 40.5 (83%) | 42.3 (87%) | 44.3 (91%) | 47.0 (95%) |
| Stream present, 6–9 blocks | 11 | 29.5 (60%) | 31.7 (65%) | 35.7 (74%) | 38.3 (78%) | 44.0 (89%) |
| Stream present, over 9 blocks | 4 | 25.2 (52%) | 26.7 (55%) | 30.8 (64%) | 32.3 (66%) | 39.7 (80%) |
| Stream present, ≤ 6 heavy entries | 11 | 41.8 (85%) | 42.0 (86%) | 44.0 (91%) | 45.0 (92%) | 47.3 (96%) |
| Stream present, 7–10 heavy | 20 | 36.6 (75%) | 38.3 (79%) | 40.8 (84%) | 42.7 (87%) | 46.2 (93%) |
| Stream present, 11 or more heavy | 12 | 28.8 (59%) | 31.0 (64%) | 33.8 (70%) | 37.5 (77%) | 43.0 (87%) |

Minutes with the stream present in which a tier reached at least 90 percent of its control rate: floor 4 of 43, r110 7, r126 11, r150 16, r200 27. Lowest minute with the stream present, as a share of control: floor 35%, r110 42%, r126 49%, r150 60%, r200 71% (all at 11:13Z, ready mass 12.1 blocks).

## Every minute: hops per family, and the probe

Hops per family: desk counter, by accepting chain block time, divided by 4 for floor and 3 for the others. Probe columns: medians of that minute's samples on the desk node. "Ready mass" is the mass of mempool transactions with no parent in the mempool, in blocks of 500,000. "Outside at 100" is mempool entries not in our logs at 100 sompi/gram; "heavy" is how many of those had mass over 200,000. The fee estimate is the desk node's `getFeeEstimate` priority bucket, read only; no sender read it. Only scored-step whole minutes are listed; the transition minutes are in [TIMELINE.md](../counts/chain/TIMELINE.md).

| Minute (UTC) | Step | Floor 100 | R110 | R126 | R150 | R200 | Ready mass, blocks | Outside at 100, n | Outside heavy (>200k) | Fee estimate, priority |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 10:40 | BASE | 43.2 | 44.7 | 45.3 | 48.3 | 48.3 | 5.51 | 8 | 8 | 101.9 |
| 10:41 | BASE | 42.2 | 42.0 | 45.3 | 45.0 | 47.3 | 4.56 | 5 | 5 | 100.0 |
| 10:42 | BASE | 39.8 | 41.3 | 41.7 | 44.3 | 45.0 | 2.43 | 3 | 3 | 100.0 |
| 10:43 | BASE | 42.2 | 43.3 | 44.0 | 46.7 | 47.7 | 2.41 | 12 | 12 | 100.0 |
| 10:44 | BASE | 43.5 | 44.7 | 47.0 | 46.7 | 51.0 | 5.97 | 9 | 9 | 104.7 |
| 10:45 | BASE | 35.5 | 36.3 | 39.3 | 40.0 | 45.7 | 3.95 | 8 | 8 | 100.0 |
| 10:46 | BASE | 43.5 | 43.3 | 44.0 | 45.3 | 50.7 | 2.97 | 4 | 4 | 100.0 |
| 10:47 | BASE | 39.2 | 40.0 | 42.0 | 44.0 | 46.7 | 5.19 | 8 | 8 | 101.4 |
| 10:49 | OBS-1 | 46.0 | 46.0 | 47.3 | 47.3 | 50.7 | 4.01 | 5 | 5 | 100.0 |
| 10:50 | OBS-1 | 45.2 | 44.0 | 46.7 | 48.7 | 52.3 | 4.57 | 7 | 7 | 100.0 |
| 10:51 | OBS-1 | 39.2 | 39.3 | 43.3 | 45.7 | 49.7 | 5.07 | 7 | 7 | 100.8 |
| 10:52 | OBS-1 | 44.0 | 45.7 | 46.0 | 47.7 | 54.3 | 4.09 | 5 | 5 | 100.0 |
| 10:53 | OBS-1 | 45.8 | 45.7 | 48.7 | 51.3 | 54.3 | 5.60 | 8 | 8 | 108.8 |
| 10:54 | OBS-1 | 39.2 | 40.3 | 42.0 | 43.3 | 49.7 | 5.85 | 9 | 9 | 107.1 |
| 10:55 | OBS-1 | 29.0 | 29.7 | 34.3 | 36.7 | 43.0 | 7.55 | 12 | 12 | 118.2 |
| 10:56 | OBS-1 | 37.5 | 38.7 | 39.0 | 43.3 | 46.7 | 7.69 | 13 | 13 | 119.0 |
| 10:57 | OBS-1 | 31.5 | 33.0 | 33.7 | 38.0 | 43.3 | 4.49 | 6 | 6 | 100.0 |
| 10:58 | OBS-1 | 35.0 | 37.3 | 40.3 | 41.0 | 44.7 | 5.74 | 8 | 8 | 104.4 |
| 10:59 | OBS-1 | 37.2 | 37.0 | 40.7 | 42.3 | 45.0 | 8.26 | 13 | 13 | 122.7 |
| 11:00 | OBS-1 | 35.8 | 37.0 | 39.0 | 42.0 | 45.3 | 6.86 | 10 | 10 | 123.9 |
| 11:02 | OBS-2 (control: stream absent) | 50.5 | 51.0 | 52.3 | 52.7 | 53.7 | 1.54 | 0 | 0 | 100.0 |
| 11:03 | OBS-2 (control: stream absent) | 49.0 | 49.0 | 49.0 | 49.0 | 49.7 | 1.34 | 0 | 0 | 100.0 |
| 11:04 | OBS-2 (control: stream absent) | 48.8 | 48.3 | 48.0 | 48.3 | 49.0 | 1.33 | 0 | 0 | 100.0 |
| 11:05 | OBS-2 (control: stream absent) | 50.8 | 50.7 | 49.3 | 50.0 | 50.3 | 1.33 | 0 | 0 | 100.0 |
| 11:06 | OBS-2 (control: stream absent) | 48.0 | 48.0 | 48.0 | 48.7 | 49.0 | 1.33 | 0 | 0 | 100.0 |
| 11:07 | OBS-2 (control: stream absent) | 46.5 | 46.7 | 47.3 | 48.0 | 49.3 | 1.33 | 0 | 0 | 100.0 |
| 11:08 | OBS-2 (control: stream absent) | 50.2 | 50.7 | 51.7 | 50.7 | 51.7 | 0.58 | 0 | 0 | 100.0 |
| 11:09 | OBS-2 (control: stream absent) | 43.8 | 43.3 | 44.7 | 45.3 | 45.7 | 1.51 | 0 | 0 | 100.0 |
| 11:10 | OBS-2 (control: stream absent) | 49.8 | 51.7 | 51.3 | 51.7 | 53.0 | 1.33 | 0 | 0 | 100.0 |
| 11:11 | OBS-2 (control: stream absent) | 48.8 | 47.7 | 47.7 | 48.7 | 49.3 | 1.00 | 0 | 0 | 100.0 |
| 11:12 | OBS-2 | 28.5 | 34.3 | 33.7 | 38.3 | 41.7 | 1.33 | 35 | 35 | 100.0 |
| 11:13 | OBS-2 | 17.0 | 20.3 | 23.7 | 29.3 | 35.3 | 12.11 | 17 | 17 | 128.2 |
| 11:15 | OBS-3 | 32.2 | 32.3 | 34.7 | 39.7 | 43.3 | 4.94 | 6 | 6 | 106.2 |
| 11:16 | OBS-3 | 40.0 | 42.0 | 42.0 | 43.3 | 46.7 | 4.06 | 9 | 9 | 100.0 |
| 11:17 | OBS-3 | 42.5 | 42.3 | 44.3 | 47.7 | 51.7 | 3.99 | 5 | 5 | 100.0 |
| 11:18 | OBS-3 | 25.8 | 27.3 | 32.0 | 32.3 | 39.7 | 9.89 | 15 | 15 | 122.4 |
| 11:19 | OBS-3 | 29.5 | 33.0 | 34.0 | 39.0 | 44.0 | 7.59 | 11 | 11 | 114.8 |
| 11:20 | OBS-3 | 37.5 | 39.3 | 41.3 | 44.7 | 46.3 | 5.30 | 7 | 7 | 100.8 |
| 11:21 | OBS-3 | 30.0 | 31.7 | 37.3 | 38.3 | 43.0 | 7.01 | 9 | 9 | 109.0 |
| 11:22 | OBS-3 | 39.5 | 40.7 | 43.3 | 45.7 | 47.3 | 5.82 | 9 | 9 | 106.5 |
| 11:23 | OBS-3 | 41.8 | 44.3 | 44.7 | 46.0 | 48.7 | 4.00 | 5 | 5 | 100.0 |
| 11:24 | OBS-3 | 32.5 | 34.7 | 35.3 | 37.3 | 43.0 | 4.74 | 7 | 7 | 105.0 |
| 11:25 | OBS-3 | 24.8 | 26.0 | 29.7 | 32.3 | 39.7 | 10.09 | 15 | 15 | 125.8 |
| 11:26 | OBS-3 | 34.2 | 34.0 | 37.3 | 40.0 | 43.3 | 5.96 | 8 | 8 | 105.5 |
| 11:31 | HOLD-4 | 32.0 | 32.0 | 36.7 | 40.3 | 44.3 | 9.26 | 15 | 15 | 123.8 |
| 11:33 | RETURN | 38.5 | 38.3 | 40.0 | 43.3 | 45.7 | 3.53 | 4 | 4 | 100.0 |
| 11:34 | RETURN | 27.0 | 29.7 | 32.0 | 35.0 | 41.0 | 6.78 | 11 | 11 | 115.7 |
| 11:35 | RETURN | 32.2 | 30.7 | 35.7 | 38.3 | 44.7 | 6.24 | 8 | 8 | 120.8 |
| 11:36 | RETURN | 21.5 | 25.0 | 29.3 | 34.7 | 42.3 | 6.81 | 9 | 9 | 113.1 |
| 11:37 | RETURN | 29.2 | 32.0 | 36.7 | 39.3 | 46.0 | 7.75 | 10 | 10 | 114.3 |
| 11:38 | RETURN | 38.5 | 41.3 | 42.7 | 43.3 | 46.0 | 4.02 | 5 | 5 | 100.0 |
| 11:39 | RETURN | 26.8 | 30.0 | 32.7 | 36.0 | 43.0 | 8.70 | 12 | 12 | 121.5 |
| 11:40 | RETURN | 30.2 | 32.7 | 35.7 | 36.7 | 43.0 | 5.90 | 7 | 7 | 103.2 |

## What this seems to show

- **With the stream absent, fee made no difference.** In the ten control minutes every tier landed 48.5–49.5 hops per family a minute, within about 2 percent of each other, and the ready mass stayed at 0.6–1.5 blocks. That is about one hop per 1.2 s per family, which matches the median submit-to-landing of about 1.06 s in OBS-2: with little ready mass, a chain's speed is set by how fast its own hops land and are rebuilt, not by its fee. Per the v2.1.0 selector, at or under one block of ready mass every ready transaction is taken best-first; we observed the tiers flat at 1.0–1.5 blocks too.
- **With the stream present, the tiers separated in fee order, and the gap grew with the ready mass and the heavy count.** Over all 43 stream-present minutes the per-family medians were floor 76, r110 77, r126 82, r150 87, r200 92 percent of control. In 32 of those 43 minutes the five tiers were in strict fee order; r200 was ahead of floor in all 43. Over 9 blocks of ready mass, floor fell to 52 percent and r200 held 80. The rank correlation (Spearman, 53 scored minutes) of hops per family with ready mass was −0.76 for floor, −0.78 r110, −0.71 r126, −0.70 r150 and −0.58 r200; with the outside fee-100 count −0.78, −0.75, −0.73, −0.70, −0.61. The cheaper the tier, the more it followed the stream.
- **Which fee held near its reference rate.** No tier held its control rate in every minute with the stream present. r200 came closest (median 92 percent; at least 90 percent in 27 of 43 minutes; never under 71). r150 held 91–92 percent (medians) while the ready mass stayed under 6 blocks and fell to 66–78 percent above that. r126 and r110 sat between floor and r150. r110 was barely different from floor (77 against 76 percent): a 10 percent premium bought almost nothing here. We read this as: in this run, against this light stream, 200 kept a chain within about 10 percent of its free-running rate most of the time, and nothing near 100 did when the ready mass went over 6 blocks. That is one run on one node.
- **The separation was much smaller than the selection weights.** The v2.1.0 weight (fee/mass)^3 gives 1.00, 1.33, 2.00, 3.38 and 8.00 for our five tiers against a same-mass competitor at 100, but over the stream-present minutes r200's per-family rate was a median of about 1.27 times floor's (at most 2.08). Our reading: a hop that is not picked in one block is a candidate again in the next, about 0.1 s later at TN10's block rate, so the weight changes how long a hop waits, not whether it lands; every OK hop landed, and the p95 landing time grew from about 1.6–2.2 s (r200) to 3.7–5.4 s (floor and r110) in OBS-3, HOLD-4 and RETURN. The chain's speed is the inverse of that wait. This is a reading, not a measurement of the selector.
- **One heavy transaction per template.** In 50 of the 51 stream-present probe minutes the desk node's own template held exactly one transaction over 100,000 storage mass; in the ten control minutes it held none. Other traffic landed on this node was a median of about 3,510 a minute with the stream and 3,139 without it. Each heavy transaction takes a little over half of one block's 500,000 mass limit, so the rest of the block is what our hops and everyone else's compete for.
- **The node's fee estimate tracked the same thing, modestly.** The priority estimate read 100.0 in every control minute and 100–128 with the stream present; it went over 115 only in minutes with ready mass over 6 blocks. A developer following it would have paid about 100–128, which in this run's heavier minutes bought 55–74 percent of the free-running rate. We did not test a sender that follows the estimate.
- **The counter kept pace.** Every whole minute from 10:39Z to the end of the tail was marked kept pace (DAA gap at most 2 against the kept public kaspad, sink age at most about 1.15 s). The start minute (10:38Z) was partial and the last tail minute (11:46Z) not final, as marked.
- **Mini matched the desk in 259 of 265 cohort cells** over the 53 scored minutes. All six mismatches were in the last two OBS-3 minutes (11:25Z and 11:26Z: floor, r126 and r150 each one hop lower on Mini). Mini published HOLD-3 at 11:27:29Z, about 30 s after 11:26Z closed; its log shows 19 late removals in the minute after that publish (0 before), and its duplicate-skip count rose in the same two minutes. We did not establish the mechanism. Mini's file does not rewrite a closed minute, by design. The desk counter stays the inclusion figure.

## Source check: our SDK's storage mass vs the node's

Read on the desk with our client SDK and the desk node's read-only RPC at about 10:20Z, and from rusty-kaspa tag v2.1.0 (commit 01b532e). Nothing was submitted; pre-run 12 ran no heavy lane.

- The outside stream's shape (2 inputs; four 0.60 tKAS outputs plus change; no payload) is about 267,000 storage mass as the desk node reports it, and about 15,300 compute mass. Our SDK's `calculateStorageMass` gives 66,650 for the same shape, about a quarter.
- Our reading of the source: the wasm `calculateStorageMass` builds `UtxoCell::new(1, value)` for every input and output (`wallet/core/src/wasm/tx/mass.rs`, lines 112–114), so it always counts a plurality of 1. Consensus counts a UTXO's plurality as ceil((63 + script length, + 32 if the output carries a covenant id) / 100) (`utxo_plurality` in `consensus/core/src/mass/mod.rs`; 63 is the fixed UTXO bytes, and the source comment says every standard script fits one 100-byte unit), and its storage term is C·p²/amount with C = 10^12. An output with p = 2 costs four times what the SDK says. 10^12 × 2² / 60,000,000 ≈ 66,667 per 0.60 tKAS output, four of them about 266,667, which matches what the node reports. So the outside outputs most likely have plurality 2 (a covenant id or a long script); that is an inference from the formula and the numbers, not a reading of their scripts.
- With plain p = 1 outputs the same storage mass needs about a quarter of the value per output: our SDK gives 266,650–266,855 for four 0.15 tKAS outputs plus change (one built and signed offline, not submitted: 266,855, fee 0.267 tKAS at 100 sompi/gram).
- The node's per-transaction mass caps are the block mass limits (`mempool_block_mass_limits` in `mining/src/mempool/check_transaction_limits.rs`: compute and transient checked in isolation, storage in context; 500,000 for compute and storage). The SDK's `MAXIMUM_STANDARD_TRANSACTION_MASS` of 100,000 (`wallet/core/src/tx/mass.rs`, line 25) is a wallet-side guard, not the node's rule: the desk node held 267,000-mass transactions.
- In v2.1.0 the relay minimum fee is checked on the larger of compute mass and normalized transient mass, not on storage mass (`mining/src/mempool/check_transaction_standard.rs`, lines 67–76). The selector's fee rate uses the node's mass including storage, per METHOD's selection section.
- What a developer could take from this, in our wording: an SDK-only mass estimate can be about four times low for outputs that carry a covenant id, so a fee taken from it would be about four times low on the rate the selector sees. Read the mass back from the node (or count plurality yourself) before choosing a fee.

## Spend

- Family re-funding, before hashes: `fund12.mjs` at 10:06:32Z sent 15 transactions, none rejected, one fresh genesis coin of about 15.0–15.35 tKAS to each of keys 1–15 (about 227 tKAS in all). The lane read 5,510 coins and 215,651 usable tKAS before that funding (pre-run 11's end), and 5,480 coins and 174,299 usable tKAS when status.mjs was read after the run (2026-11-12, about 11:53Z, read-only). That is 41,352 usable tKAS over the run including the re-funding, about 1.02 tKAS per family hop landed (40,440), close to pre-runs 10 and 11 (about 1.06–1.09). It is not split further here.
- No payment of ours: the payment key still holds 8,400 coins, as before.
- The lane stays above the abort line (2,500 coins and 18,000 usable tKAS), with about 156,000 usable tKAS of headroom: about three to four more family runs of this length, not an open-ended series. Keys 1–15 have no genesis coin left; a next repo funds them again.

## Fixes

- The desk runner's auto-written METHOD commit message said `Pre-run 11 method.` (3d7477a), and its FAILED path still carries `Pre-run 11 failed before RETURN.`: labels left over from pre-run 11's runner. No gate or count reads them. Small fix for the next repo's runner: take the pre-run number from the config. The METHOD file's own content is pre-run 12's.

## What a next attempt could try (pre-run 13, designed, not opened)

1. Our own heavy lane, so the competitor can be set and switched off rather than waited for: N parallel chains at about 267,000 storage mass and 100 sompi/gram, stepped by ready count (0 → 10 → 20 → 40 → 60 → 40 → 20 → 0), with the same five tiers, plus one step with the lane at 126. stp approved it for pre-run 13 and said it need not be short. The design, caps and wording are in the pre-run 13 repo when it opens.
2. Calibrate the lane on the node's mass, not the SDK's: use plain p = 1 outputs and read the first transaction's storage mass back from the desk mempool before the second goes out.
3. Keep the stream-absent window as the reference (or make one with the lane at N = 0), since this run's BASE was not clean.
4. Keep the probe and Mini's count. The bot stays a `NO SEND` until a third unique kaspad answers.
