OBSERVATION

Not scored. No payment of ours in pre-run 12: families only, on the desk's private node.

# HOLD-3, desk, pre-run 12

> Our own TN10 testing: what we observed in this run, on our own desk node. Counts only. Included is what the desk's private TN10 node accepted on chain, read by the desk counter, by accepting chain block time. Mini's files are a second read.

HOLD-3 is OBS-3: a long observation stretch, families only, 12 whole minutes. Pre-run 12 keeps the HOLD file names so the bot's and Mini's gates read as in earlier pre-runs; nothing is offered. Not scored.

Families offer 1.2 hop/s, 16 families live, one family-sender process and one builder: floor (families 1–4) 100 sompi/gram on the desk's private node, r110 (families 5–7) 110 sompi/gram on the desk's private node, r126 (families 8–10) 126 sompi/gram on the desk's private node, r150 (families 11–13) 150 sompi/gram on the desk's private node, r200 (families 14–16) 200 sompi/gram on the desk's private node. No payment sender was started.

## Tiers against the mempool, per minute

| Minute (UTC) | floor (100) | r110 (110) | r126 (126) | r150 (150) | r200 (200) | Ready mass, blocks | Outside at 100, n | Outside at 100, heavy (>200k mass) / ready | Mempool | Fee estimate priority |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 2026-11-12T11:15 | 129 | 97 | 104 | 119 | 130 | 4.94 | 6 | 6 / 6 | 19 | 106.2 |
| 2026-11-12T11:16 | 160 | 126 | 126 | 130 | 140 | 4.06 | 9 | 9 / 9 | 22 | 100.0 |
| 2026-11-12T11:17 | 170 | 127 | 133 | 143 | 155 | 3.99 | 5 | 5 / 5 | 21 | 100.0 |
| 2026-11-12T11:18 | 103 | 82 | 96 | 97 | 119 | 9.89 | 15 | 15 / 14 | 23 | 122.4 |
| 2026-11-12T11:19 | 118 | 99 | 102 | 117 | 132 | 7.59 | 11 | 11 / 11 | 29 | 114.8 |
| 2026-11-12T11:20 | 150 | 118 | 124 | 134 | 139 | 5.30 | 7 | 7 / 7 | 21 | 100.8 |
| 2026-11-12T11:21 | 120 | 95 | 112 | 115 | 129 | 7.01 | 9 | 9 / 9 | 24 | 109.0 |
| 2026-11-12T11:22 | 158 | 122 | 130 | 137 | 142 | 5.82 | 9 | 9 / 9 | 22 | 106.5 |
| 2026-11-12T11:23 | 167 | 133 | 134 | 138 | 146 | 4.00 | 5 | 5 / 5 | 21 | 100.0 |
| 2026-11-12T11:24 | 130 | 104 | 106 | 112 | 129 | 4.74 | 7 | 7 / 7 | 24 | 105.0 |
| 2026-11-12T11:25 | 99 | 78 | 89 | 97 | 119 | 10.09 | 15 | 15 / 14 | 35 | 125.8 |
| 2026-11-12T11:26 | 137 | 102 | 112 | 120 | 130 | 5.96 | 8 | 8 / 8 | 23 | 105.5 |

Hops are what the desk counter read as accepted on chain in that minute, per tier. Ready mass, blocks, is the median of the probe's samples in the minute (block limit 500,000). Outside at 100 is the median count of mempool entries not in our logs paying 100 sompi/gram, and heavy is how many of those had a mass over 200,000 (median of samples). The outside stream is not attributed to anyone.

## Chain, desk counter

| Minute (UTC) | Included, all non-coinbase | Our payments included | Floor hops (100) | R110 hops (110) | R126 hops (126) | R150 hops (150) | R200 hops (200) | Other traffic | Chain blocks | DAA gap max | Sink age max, ms | Final after, s | Counter |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 2026-11-12T11:15 | 4,108 | 0 | 129 | 97 | 104 | 119 | 130 | 3,534 | 382 | 1 | 442 | 20 | kept pace |
| 2026-11-12T11:16 | 4,255 | 0 | 160 | 126 | 126 | 130 | 140 | 3,580 | 384 | 1 | 745 | 20 | kept pace |
| 2026-11-12T11:17 | 4,394 | 0 | 170 | 127 | 133 | 143 | 155 | 3,669 | 392 | 1 | 321 | 20 | kept pace |
| 2026-11-12T11:18 | 4,039 | 0 | 103 | 82 | 96 | 97 | 119 | 3,547 | 356 | 1 | 646 | 20 | kept pace |
| 2026-11-12T11:19 | 4,105 | 0 | 118 | 99 | 102 | 117 | 132 | 3,541 | 379 | 1 | 613 | 19 | kept pace |
| 2026-11-12T11:20 | 4,173 | 0 | 150 | 118 | 124 | 134 | 139 | 3,512 | 380 | 0 | 339 | 20 | kept pace |
| 2026-11-12T11:21 | 3,984 | 0 | 120 | 95 | 112 | 115 | 129 | 3,419 | 344 | 1 | 468 | 20 | kept pace |
| 2026-11-12T11:22 | 4,242 | 0 | 158 | 122 | 130 | 137 | 142 | 3,557 | 381 | 1 | 740 | 20 | kept pace |
| 2026-11-12T11:23 | 4,138 | 0 | 167 | 133 | 134 | 138 | 146 | 3,427 | 390 | 1 | 330 | 20 | kept pace |
| 2026-11-12T11:24 | 4,101 | 0 | 130 | 104 | 106 | 112 | 129 | 3,522 | 366 | 0 | 343 | 20 | kept pace |
| 2026-11-12T11:25 | 3,964 | 0 | 99 | 78 | 89 | 97 | 119 | 3,486 | 345 | 0 | 714 | 20 | kept pace |
| 2026-11-12T11:26 | 4,104 | 0 | 137 | 102 | 112 | 120 | 130 | 3,511 | 410 | 1 | 363 | 21 | kept pace |

Coinbase is taken out as one per merged blue block (on this node a chain block's accepted list carries the coinbase of each blue block it merges). Other traffic is the rest: other users' load, the genesis, and anything not in our logs.

## Hop rate per cohort, as built

Floor (families 1–4, desk private node): 100 sompi/gram per hop. R110 (families 5–7, desk private node): 110 sompi/gram per hop. R126 (families 8–10, desk private node): 126 sompi/gram per hop. R150 (families 11–13, desk private node): 150 sompi/gram per hop. R200 (families 14–16, desk private node): 200 sompi/gram per hop. The rate rides on each hop line to the one builder. Payments pay 150.

## Funding coins, as read from the desk node

The funding coins were not one size. Sizes seen, whole tKAS (coins): 18 (474), 17 (458), 19 (440), 16 (431), 15 (403), 20 (397), 21 (357), 22 (320), 14 (305), 13 (247), 12 (214), 23 (206), and 70 more sizes. The fee is not called the whole cause.

## Minutes

| Minute (UTC) | Pay submit-OK | Attempts | Rejects, rate | Rejects, full | Other | Floor OK / att / rate rej / full rej / waiting | R110 OK / att / rate rej / full rej / waiting | R126 OK / att / rate rej / full rej / waiting | R150 OK / att / rate rej / full rej / waiting | R200 OK / att / rate rej / full rej / waiting | Family stalls logged | Family node mempool-high marks | Clean |
|---|---:|---:|---:|---:|---:|---|---|---|---|---|---:|---:|---|
| 2026-11-12T11:15 | 0 | 0 | 0 | 0 | 0 | 131 / 343 / 0 / 0 / 4 | 97 / 254 / 0 / 0 / 3 | 105 / 255 / 0 / 0 / 3 | 121 / 274 / 0 / 0 / 3 | 131 / 274 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T11:16 | 0 | 0 | 0 | 0 | 0 | 157 / 360 / 0 / 0 / 1 | 125 / 272 / 0 / 0 / 2 | 125 / 268 / 0 / 0 / 2 | 128 / 266 / 0 / 0 / 1 | 140 / 269 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T11:17 | 0 | 0 | 0 | 0 | 0 | 173 / 354 / 0 / 0 / 4 | 127 / 269 / 0 / 0 / 2 | 134 / 274 / 0 / 0 / 3 | 145 / 271 / 0 / 0 / 3 | 155 / 274 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T11:18 | 0 | 0 | 0 | 0 | 0 | 103 / 326 / 0 / 0 / 4 | 83 / 252 / 0 / 0 / 3 | 96 / 254 / 0 / 0 / 3 | 97 / 261 / 0 / 0 / 3 | 119 / 268 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T11:19 | 0 | 0 | 0 | 0 | 0 | 117 / 340 / 0 / 0 / 3 | 96 / 256 / 0 / 0 / 0 | 100 / 258 / 0 / 0 / 1 | 117 / 265 / 0 / 0 / 3 | 129 / 272 / 0 / 0 / 0 | 0 | 0 | yes |
| 2026-11-12T11:20 | 0 | 0 | 0 | 0 | 0 | 151 / 346 / 0 / 0 / 4 | 121 / 267 / 0 / 0 / 3 | 126 / 266 / 0 / 0 / 3 | 134 / 266 / 0 / 0 / 3 | 142 / 269 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T11:21 | 0 | 0 | 0 | 0 | 0 | 120 / 332 / 0 / 0 / 4 | 95 / 250 / 0 / 0 / 3 | 112 / 265 / 0 / 0 / 3 | 115 / 260 / 0 / 0 / 3 | 129 / 272 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T11:22 | 0 | 0 | 0 | 0 | 0 | 157 / 355 / 0 / 0 / 3 | 120 / 265 / 0 / 0 / 1 | 130 / 273 / 0 / 0 / 3 | 136 / 269 / 0 / 0 / 2 | 142 / 273 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T11:23 | 0 | 0 | 0 | 0 | 0 | 168 / 356 / 0 / 0 / 4 | 136 / 280 / 0 / 0 / 3 | 134 / 272 / 0 / 0 / 3 | 139 / 282 / 0 / 0 / 3 | 146 / 285 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T11:24 | 0 | 0 | 0 | 0 | 0 | 128 / 334 / 0 / 0 / 2 | 102 / 258 / 0 / 0 / 2 | 104 / 249 / 0 / 0 / 1 | 111 / 256 / 0 / 0 / 2 | 128 / 269 / 0 / 0 / 2 | 0 | 0 | yes |
| 2026-11-12T11:25 | 0 | 0 | 0 | 0 | 0 | 100 / 330 / 0 / 0 / 3 | 78 / 246 / 0 / 0 / 2 | 91 / 253 / 0 / 0 / 3 | 97 / 254 / 0 / 0 / 2 | 120 / 267 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T11:26 | 0 | 0 | 0 | 0 | 0 | 138 / 346 / 0 / 0 / 4 | 103 / 262 / 0 / 0 / 3 | 112 / 261 / 0 / 0 / 3 | 121 / 272 / 0 / 0 / 3 | 130 / 266 / 0 / 0 / 3 | 0 | 0 | yes |

A family stall is a coordinator mark: no hop of that family landed for a while. The family was still attempting. It is logged, and it does not make the minute dirty.

A mempool-high mark means the family node read a mempool at or over 90,000. In pre-run 12 that does not stop the families: the skip does not apply to them. A skip, if one were set, is dirt with its reason (node-skip-fam) for every minute it covers, and it clears when the mempool falls back under the line.

Within 10 percent means 0 to 0 submit-OK in the minute.

## Public nodes (local numbers)

Kept: 1, 5. The family sender reads and submits every tier on the desk's private node, which the desk counter reads. The kept public kaspads are read for sync and DAA only; no payment of ours went to them.

Kept nodes are unique kaspads: each answered with its own node id at the preflight. 3 candidate endpoints passed the check and were 2 kaspads (node 4 is node 1; the second hostname was not used). 3 payment senders per kaspad.

| Node | Synced every sample | Last DAA | Pay submit-OK | Pay rejects | Dropped sockets | Answer ms, median |
|---:|---|---:|---:|---:|---:|---:|
| 1 | yes | 621466268 | 0 | 0 | 0 | 32 |
| 5 | yes | 621466268 | 0 | 0 | 0 | 40 |

## Hop submit to landing, per cohort

| Cohort | Landed of OK | Median ms | Slow tail (p95) ms |
|---|---:|---:|---:|
| floor | 1643 of 1643 | 1243 | 3676 |
| r110 | 1283 of 1283 | 1216 | 3488 |
| r126 | 1369 of 1369 | 1198 | 2786 |
| r150 | 1461 of 1461 | 1161 | 2460 |
| r200 | 1611 of 1611 | 1099 | 1969 |

Landing is the accepting block header time the desk's coordinator read. Waiting is submitted-OK not yet landed at the minute's end. Every tier has the same hop shape and the same node; only the rate differs.

## Mempool and template, desk node (probe)

| Minute (UTC) | Samples | Mempool | Ready (no parent in mempool) | Ready mass, blocks of 500k | Other traffic in mempool | Other ready | Other at 100, n | Other at 100, mean mass | Our payments in mempool | Floor in mempool / ready | R110 in mempool / ready | R126 in mempool / ready | R150 in mempool / ready | R200 in mempool / ready | Template txs | Template storage mass | Template txs over 100k storage mass | Template: payments | Template: floor | Template: r110 | Template: r126 | Template: r150 | Template: r200 | Template: other | Fee estimate priority / normal / low | Public 1 mempool | Public 5 mempool |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|
| 2026-11-12T11:15 | 3 | 19 | 25 | 4.94 | 13 | 13 | 6 | 266,618 | 0 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 7 | 473,874 | 1 | 0 | 0 | 0 | 0 | 2 | 2 | 2 | 106.2 / 104.5 / 101.5 | 25 | 25 |
| 2026-11-12T11:16 | 3 | 22 | 22 | 4.06 | 6 | 6 | 9 | 266,618 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 472,731 | 1 | 0 | 0 | 1 | 0 | 2 | 3 | 1 | 100.0 / 100.0 / 100.0 | 15 | 22 |
| 2026-11-12T11:17 | 3 | 21 | 21 | 3.99 | 5 | 5 | 5 | 266,618 | 0 | 4 / 4 | 3 / 3 | 2 / 2 | 3 / 3 | 3 / 3 | 6 | 474,325 | 1 | 0 | 2 | 0 | 0 | 0 | 1 | 1 | 100.0 / 100.0 / 100.0 | 20 | 10 |
| 2026-11-12T11:18 | 3 | 23 | 32 | 9.89 | 17 | 17 | 15 | 266,616 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 2 / 2 | 3 / 3 | 2 | 308,105 | 1 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 122.4 / 115.3 / 104.4 | 22 | 27 |
| 2026-11-12T11:19 | 3 | 29 | 29 | 7.59 | 14 | 14 | 11 | 266,616 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 3 | 349,054 | 1 | 0 | 0 | 0 | 0 | 0 | 1 | 1 | 114.8 / 110.4 / 103.2 | 19 | 24 |
| 2026-11-12T11:20 | 3 | 21 | 26 | 5.30 | 10 | 10 | 7 | 266,613 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 5 | 461,955 | 1 | 0 | 0 | 0 | 0 | 1 | 1 | 2 | 100.8 / 100.6 / 100.2 | 10 | 16 |
| 2026-11-12T11:21 | 3 | 24 | 28 | 7.01 | 12 | 12 | 9 | 266,613 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 5 | 432,179 | 1 | 0 | 1 | 0 | 0 | 0 | 2 | 1 | 109.0 / 106.5 / 102.0 | 21 | 24 |
| 2026-11-12T11:22 | 3 | 22 | 22 | 5.82 | 11 | 11 | 9 | 266,613 | 0 | 4 / 4 | 2 / 2 | 2 / 2 | 2 / 2 | 2 / 2 | 6 | 349,163 | 1 | 0 | 0 | 0 | 1 | 0 | 1 | 1 | 106.5 / 104.7 / 101.5 | 22 | 22 |
| 2026-11-12T11:23 | 3 | 21 | 22 | 4.00 | 6 | 6 | 5 | 266,610 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 472,653 | 1 | 0 | 1 | 0 | 1 | 1 | 2 | 1 | 100.0 / 100.0 / 100.0 | 6 | 7 |
| 2026-11-12T11:24 | 3 | 24 | 19 | 4.74 | 7 | 7 | 7 | 266,610 | 0 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 474,344 | 1 | 0 | 0 | 1 | 1 | 0 | 1 | 1 | 105.0 / 103.6 / 101.2 | 22 | 27 |
| 2026-11-12T11:25 | 3 | 35 | 35 | 10.09 | 21 | 20 | 15 | 266,608 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 2 | 307,818 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 125.8 / 117.3 / 104.9 | 24 | 30 |
| 2026-11-12T11:26 | 3 | 23 | 23 | 5.96 | 9 | 9 | 8 | 266,608 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 472,558 | 1 | 0 | 0 | 0 | 0 | 1 | 1 | 1 | 105.5 / 104.0 / 101.3 | 15 | 23 |

Read by the probe on the desk's private TN10 node every 20 s, read-only; each cell is the median of that minute's samples. Ready means no parent in the mempool: in rusty-kaspa v2.1.0 only those are in the selector's frontier. Ready mass is compared with one block's mass limit (500,000): at or under 1 the selector takes all ready transactions best-first; over 1 it samples at random weighted by (fee/mass)^3 (over 4, sample_inplace). Mass is the larger of compute and storage mass, as the v2.1.0 selector normalises it (transient mass is not in the RPC). Other traffic is every mempool entry not in our sender logs; its fee rate is the node's fee over that mass. Template transactions carry no id in the RPC, so each is matched to a mempool entry by its first input. The template is the desk node's own getBlockTemplate (never submitted): what this node would put in a block at that moment, not a miner's template. The fee estimate is the node's getFeeEstimate, read only; no sender reads it. Public mempool is getInfo's mempool size on each kept public kaspad.
