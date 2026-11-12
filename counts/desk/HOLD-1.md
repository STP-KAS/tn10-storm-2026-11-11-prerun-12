OBSERVATION

Not scored. No payment of ours in pre-run 12: families only, on the desk's private node.

# HOLD-1, desk, pre-run 12

> Our own TN10 testing: what we observed in this run, on our own desk node. Counts only. Included is what the desk's private TN10 node accepted on chain, read by the desk counter, by accepting chain block time. Mini's files are a second read.

HOLD-1 is OBS-1: a long observation stretch, families only, 12 whole minutes. Pre-run 12 keeps the HOLD file names so the bot's and Mini's gates read as in earlier pre-runs; nothing is offered. Not scored.

Families offer 1.2 hop/s, 16 families live, one family-sender process and one builder: floor (families 1–4) 100 sompi/gram on the desk's private node, r110 (families 5–7) 110 sompi/gram on the desk's private node, r126 (families 8–10) 126 sompi/gram on the desk's private node, r150 (families 11–13) 150 sompi/gram on the desk's private node, r200 (families 14–16) 200 sompi/gram on the desk's private node. No payment sender was started.

## Tiers against the mempool, per minute

| Minute (UTC) | floor (100) | r110 (110) | r126 (126) | r150 (150) | r200 (200) | Ready mass, blocks | Outside at 100, n | Outside at 100, heavy (>200k mass) / ready | Mempool | Fee estimate priority |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 2026-11-12T10:49 | 184 | 138 | 142 | 142 | 152 | 4.01 | 5 | 5 / 5 | 17 | 100.0 |
| 2026-11-12T10:50 | 181 | 132 | 140 | 146 | 157 | 4.57 | 7 | 7 / 7 | 17 | 100.0 |
| 2026-11-12T10:51 | 157 | 118 | 130 | 137 | 149 | 5.07 | 7 | 7 / 7 | 23 | 100.8 |
| 2026-11-12T10:52 | 176 | 137 | 138 | 143 | 163 | 4.09 | 5 | 5 / 5 | 18 | 100.0 |
| 2026-11-12T10:53 | 183 | 137 | 146 | 154 | 163 | 5.60 | 8 | 8 / 8 | 24 | 108.8 |
| 2026-11-12T10:54 | 157 | 121 | 126 | 130 | 149 | 5.85 | 9 | 9 / 9 | 19 | 107.1 |
| 2026-11-12T10:55 | 116 | 89 | 103 | 110 | 129 | 7.55 | 12 | 12 / 12 | 26 | 118.2 |
| 2026-11-12T10:56 | 150 | 116 | 117 | 130 | 140 | 7.69 | 13 | 13 / 13 | 32 | 119.0 |
| 2026-11-12T10:57 | 126 | 99 | 101 | 114 | 130 | 4.49 | 6 | 6 / 5 | 21 | 100.0 |
| 2026-11-12T10:58 | 140 | 112 | 121 | 123 | 134 | 5.74 | 8 | 8 / 8 | 22 | 104.4 |
| 2026-11-12T10:59 | 149 | 111 | 122 | 127 | 135 | 8.26 | 13 | 13 / 13 | 27 | 122.7 |
| 2026-11-12T11:00 | 143 | 111 | 117 | 126 | 136 | 6.86 | 10 | 10 / 10 | 23 | 123.9 |

Hops are what the desk counter read as accepted on chain in that minute, per tier. Ready mass, blocks, is the median of the probe's samples in the minute (block limit 500,000). Outside at 100 is the median count of mempool entries not in our logs paying 100 sompi/gram, and heavy is how many of those had a mass over 200,000 (median of samples). The outside stream is not attributed to anyone.

## Chain, desk counter

| Minute (UTC) | Included, all non-coinbase | Our payments included | Floor hops (100) | R110 hops (110) | R126 hops (126) | R150 hops (150) | R200 hops (200) | Other traffic | Chain blocks | DAA gap max | Sink age max, ms | Final after, s | Counter |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 2026-11-12T10:49 | 4,240 | 0 | 184 | 138 | 142 | 142 | 152 | 3,491 | 421 | 0 | 502 | 20 | kept pace |
| 2026-11-12T10:50 | 4,232 | 0 | 181 | 132 | 140 | 146 | 157 | 3,488 | 394 | 0 | 520 | 20 | kept pace |
| 2026-11-12T10:51 | 4,170 | 0 | 157 | 118 | 130 | 137 | 149 | 3,490 | 429 | 0 | 418 | 20 | kept pace |
| 2026-11-12T10:52 | 4,200 | 0 | 176 | 137 | 138 | 143 | 163 | 3,455 | 390 | 0 | 697 | 20 | kept pace |
| 2026-11-12T10:53 | 4,463 | 0 | 183 | 137 | 146 | 154 | 163 | 3,694 | 397 | 0 | 348 | 20 | kept pace |
| 2026-11-12T10:54 | 4,200 | 0 | 157 | 121 | 126 | 130 | 149 | 3,524 | 390 | 0 | 371 | 19 | kept pace |
| 2026-11-12T10:55 | 4,084 | 0 | 116 | 89 | 103 | 110 | 129 | 3,544 | 376 | 0 | 501 | 20 | kept pace |
| 2026-11-12T10:56 | 4,147 | 0 | 150 | 116 | 117 | 130 | 140 | 3,497 | 367 | 0 | 579 | 20 | kept pace |
| 2026-11-12T10:57 | 4,075 | 0 | 126 | 99 | 101 | 114 | 130 | 3,507 | 377 | 0 | 543 | 20 | kept pace |
| 2026-11-12T10:58 | 4,136 | 0 | 140 | 112 | 121 | 123 | 134 | 3,510 | 369 | 0 | 397 | 20 | kept pace |
| 2026-11-12T10:59 | 4,148 | 0 | 149 | 111 | 122 | 127 | 135 | 3,506 | 374 | 0 | 745 | 20 | kept pace |
| 2026-11-12T11:00 | 4,107 | 0 | 143 | 111 | 117 | 126 | 136 | 3,480 | 374 | 1 | 283 | 20 | kept pace |

Coinbase is taken out as one per merged blue block (on this node a chain block's accepted list carries the coinbase of each blue block it merges). Other traffic is the rest: other users' load, the genesis, and anything not in our logs.

## Hop rate per cohort, as built

Floor (families 1–4, desk private node): 100 sompi/gram per hop. R110 (families 5–7, desk private node): 110 sompi/gram per hop. R126 (families 8–10, desk private node): 126 sompi/gram per hop. R150 (families 11–13, desk private node): 150 sompi/gram per hop. R200 (families 14–16, desk private node): 200 sompi/gram per hop. The rate rides on each hop line to the one builder. Payments pay 150.

## Funding coins, as read from the desk node

The funding coins were not one size. Sizes seen, whole tKAS (coins): 20 (538), 22 (522), 21 (513), 19 (449), 23 (405), 18 (371), 24 (363), 17 (338), 25 (296), 26 (250), 16 (229), 27 (184), and 72 more sizes. The fee is not called the whole cause.

## Minutes

| Minute (UTC) | Pay submit-OK | Attempts | Rejects, rate | Rejects, full | Other | Floor OK / att / rate rej / full rej / waiting | R110 OK / att / rate rej / full rej / waiting | R126 OK / att / rate rej / full rej / waiting | R150 OK / att / rate rej / full rej / waiting | R200 OK / att / rate rej / full rej / waiting | Family stalls logged | Family node mempool-high marks | Clean |
|---|---:|---:|---:|---:|---:|---|---|---|---|---|---:|---:|---|
| 2026-11-12T10:49 | 0 | 0 | 0 | 0 | 0 | 185 / 365 / 0 / 0 / 4 | 138 / 276 / 0 / 0 / 3 | 142 / 278 / 0 / 0 / 3 | 141 / 273 / 0 / 0 / 2 | 152 / 281 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T10:50 | 0 | 0 | 0 | 0 | 0 | 183 / 366 / 0 / 0 / 6 | 133 / 272 / 0 / 0 / 4 | 140 / 273 / 0 / 0 / 3 | 147 / 276 / 0 / 0 / 3 | 158 / 279 / 0 / 0 / 4 | 0 | 0 | yes |
| 2026-11-12T10:51 | 0 | 0 | 0 | 0 | 0 | 152 / 351 / 0 / 0 / 1 | 114 / 269 / 0 / 0 / 0 | 127 / 271 / 0 / 0 / 0 | 134 / 273 / 0 / 0 / 0 | 145 / 275 / 0 / 0 / 0 | 0 | 0 | yes |
| 2026-11-12T10:52 | 0 | 0 | 0 | 0 | 0 | 178 / 364 / 0 / 0 / 3 | 139 / 274 / 0 / 0 / 2 | 139 / 274 / 0 / 0 / 1 | 146 / 276 / 0 / 0 / 3 | 163 / 285 / 0 / 0 / 0 | 0 | 0 | yes |
| 2026-11-12T10:53 | 0 | 0 | 0 | 0 | 0 | 184 / 361 / 0 / 0 / 4 | 138 / 270 / 0 / 0 / 3 | 148 / 278 / 0 / 0 / 3 | 154 / 277 / 0 / 0 / 3 | 166 / 283 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T10:54 | 0 | 0 | 0 | 0 | 0 | 157 / 348 / 0 / 0 / 4 | 121 / 268 / 0 / 0 / 3 | 126 / 270 / 0 / 0 / 3 | 130 / 274 / 0 / 0 / 3 | 149 / 285 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T10:55 | 0 | 0 | 0 | 0 | 0 | 115 / 337 / 0 / 0 / 3 | 88 / 250 / 0 / 0 / 2 | 101 / 253 / 0 / 0 / 1 | 109 / 260 / 0 / 0 / 2 | 129 / 268 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T10:56 | 0 | 0 | 0 | 0 | 0 | 151 / 358 / 0 / 0 / 4 | 117 / 265 / 0 / 0 / 3 | 119 / 268 / 0 / 0 / 3 | 131 / 275 / 0 / 0 / 3 | 140 / 283 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T10:57 | 0 | 0 | 0 | 0 | 0 | 126 / 340 / 0 / 0 / 4 | 99 / 258 / 0 / 0 / 3 | 101 / 258 / 0 / 0 / 3 | 114 / 269 / 0 / 0 / 3 | 130 / 277 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T10:58 | 0 | 0 | 0 | 0 | 0 | 139 / 344 / 0 / 0 / 3 | 111 / 263 / 0 / 0 / 2 | 121 / 266 / 0 / 0 / 3 | 123 / 271 / 0 / 0 / 3 | 132 / 276 / 0 / 0 / 1 | 0 | 0 | yes |
| 2026-11-12T10:59 | 0 | 0 | 0 | 0 | 0 | 150 / 348 / 0 / 0 / 4 | 112 / 262 / 0 / 0 / 3 | 120 / 272 / 0 / 0 / 1 | 125 / 266 / 0 / 0 / 1 | 136 / 280 / 0 / 0 / 2 | 0 | 0 | yes |
| 2026-11-12T11:00 | 0 | 0 | 0 | 0 | 0 | 143 / 342 / 0 / 0 / 4 | 111 / 260 / 0 / 0 / 3 | 119 / 269 / 0 / 0 / 3 | 128 / 266 / 0 / 0 / 3 | 136 / 277 / 0 / 0 / 2 | 0 | 0 | yes |

A family stall is a coordinator mark: no hop of that family landed for a while. The family was still attempting. It is logged, and it does not make the minute dirty.

A mempool-high mark means the family node read a mempool at or over 90,000. In pre-run 12 that does not stop the families: the skip does not apply to them. A skip, if one were set, is dirt with its reason (node-skip-fam) for every minute it covers, and it clears when the mempool falls back under the line.

Within 10 percent means 0 to 0 submit-OK in the minute.

## Public nodes (local numbers)

Kept: 1, 5. The family sender reads and submits every tier on the desk's private node, which the desk counter reads. The kept public kaspads are read for sync and DAA only; no payment of ours went to them.

Kept nodes are unique kaspads: each answered with its own node id at the preflight. 3 candidate endpoints passed the check and were 2 kaspads (node 4 is node 1; the second hostname was not used). 3 payment senders per kaspad.

| Node | Synced every sample | Last DAA | Pay submit-OK | Pay rejects | Dropped sockets | Answer ms, median |
|---:|---|---:|---:|---:|---:|---:|
| 1 | yes | 621450481 | 0 | 0 | 0 | 34 |
| 5 | yes | 621450481 | 0 | 0 | 0 | 40 |

## Hop submit to landing, per cohort

| Cohort | Landed of OK | Median ms | Slow tail (p95) ms |
|---|---:|---:|---:|
| floor | 1863 of 1863 | 1177 | 2701 |
| r110 | 1421 of 1421 | 1150 | 2649 |
| r126 | 1503 of 1503 | 1122 | 2268 |
| r150 | 1582 of 1582 | 1099 | 2182 |
| r200 | 1736 of 1736 | 1019 | 1783 |

Landing is the accepting block header time the desk's coordinator read. Waiting is submitted-OK not yet landed at the minute's end. Every tier has the same hop shape and the same node; only the rate differs.

## Mempool and template, desk node (probe)

| Minute (UTC) | Samples | Mempool | Ready (no parent in mempool) | Ready mass, blocks of 500k | Other traffic in mempool | Other ready | Other at 100, n | Other at 100, mean mass | Our payments in mempool | Floor in mempool / ready | R110 in mempool / ready | R126 in mempool / ready | R150 in mempool / ready | R200 in mempool / ready | Template txs | Template storage mass | Template txs over 100k storage mass | Template: payments | Template: floor | Template: r110 | Template: r126 | Template: r150 | Template: r200 | Template: other | Fee estimate priority / normal / low | Public 1 mempool | Public 5 mempool |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|
| 2026-11-12T10:49 | 3 | 17 | 22 | 4.01 | 6 | 6 | 5 | 266,486 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 474,469 | 1 | 0 | 1 | 0 | 0 | 1 | 3 | 1 | 100.0 / 100.0 / 100.0 | 5 | 21 |
| 2026-11-12T10:50 | 3 | 17 | 17 | 4.57 | 7 | 7 | 7 | 266,472 | 0 | 3 / 3 | 3 / 3 | 2 / 2 | 2 / 2 | 3 / 3 | 6 | 474,895 | 1 | 0 | 0 | 0 | 1 | 0 | 1 | 1 | 100.0 / 100.0 / 100.0 | 33 | 31 |
| 2026-11-12T10:51 | 3 | 23 | 23 | 5.07 | 7 | 7 | 7 | 266,456 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 473,875 | 1 | 0 | 1 | 0 | 0 | 0 | 1 | 1 | 100.8 / 100.6 / 100.2 | 17 | 22 |
| 2026-11-12T10:52 | 3 | 18 | 19 | 4.09 | 7 | 7 | 5 | 266,429 | 0 | 4 / 4 | 3 / 3 | 2 / 2 | 3 / 3 | 3 / 3 | 7 | 476,263 | 1 | 0 | 2 | 0 | 1 | 1 | 2 | 2 | 100.0 / 100.0 / 100.0 | 17 | 16 |
| 2026-11-12T10:53 | 3 | 24 | 24 | 5.60 | 9 | 9 | 8 | 266,413 | 0 | 4 / 4 | 2 / 2 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 473,451 | 1 | 0 | 1 | 0 | 1 | 0 | 1 | 1 | 108.8 / 106.3 / 102.0 | 18 | 17 |
| 2026-11-12T10:54 | 3 | 19 | 23 | 5.85 | 10 | 10 | 9 | 266,385 | 0 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 4 | 391,569 | 1 | 0 | 0 | 1 | 0 | 0 | 2 | 1 | 107.1 / 105.2 / 101.6 | 20 | 20 |
| 2026-11-12T10:55 | 3 | 26 | 26 | 7.55 | 12 | 12 | 12 | 266,351 | 0 | 4 / 4 | 3 / 3 | 2 / 2 | 3 / 3 | 2 / 2 | 6 | 394,135 | 1 | 0 | 1 | 0 | 0 | 1 | 1 | 1 | 118.2 / 112.6 / 103.8 | 43 | 46 |
| 2026-11-12T10:56 | 3 | 32 | 35 | 7.69 | 19 | 19 | 13 | 266,307 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 9 | 379,099 | 1 | 0 | 0 | 1 | 1 | 1 | 1 | 5 | 119.0 / 113.2 / 103.9 | 30 | 32 |
| 2026-11-12T10:57 | 3 | 21 | 22 | 4.49 | 7 | 6 | 6 | 266,248 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 473,746 | 1 | 0 | 1 | 1 | 1 | 1 | 1 | 1 | 100.0 / 100.0 / 100.0 | 13 | 12 |
| 2026-11-12T10:58 | 3 | 22 | 22 | 5.74 | 9 | 9 | 8 | 266,171 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 474,159 | 1 | 0 | 1 | 0 | 0 | 2 | 2 | 1 | 104.4 / 103.2 / 101.0 | 15 | 21 |
| 2026-11-12T10:59 | 2 | 27 | 29 | 8.26 | 13 | 13 | 13 | 266,035 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 11 | 462,145 | 1 | 0 | 2 | 1 | 2 | 3 | 3 | 1 | 122.7 / 115.5 / 104.5 | 50 | 34 |
| 2026-11-12T11:00 | 3 | 23 | 36 | 6.86 | 21 | 20 | 10 | 265,917 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 7 | 430,612 | 1 | 0 | 0 | 0 | 1 | 1 | 1 | 3 | 123.9 / 116.2 / 104.7 | 19 | 23 |

Read by the probe on the desk's private TN10 node every 20 s, read-only; each cell is the median of that minute's samples. Ready means no parent in the mempool: in rusty-kaspa v2.1.0 only those are in the selector's frontier. Ready mass is compared with one block's mass limit (500,000): at or under 1 the selector takes all ready transactions best-first; over 1 it samples at random weighted by (fee/mass)^3 (over 4, sample_inplace). Mass is the larger of compute and storage mass, as the v2.1.0 selector normalises it (transient mass is not in the RPC). Other traffic is every mempool entry not in our sender logs; its fee rate is the node's fee over that mass. Template transactions carry no id in the RPC, so each is matched to a mempool entry by its first input. The template is the desk node's own getBlockTemplate (never submitted): what this node would put in a block at that moment, not a miner's template. The fee estimate is the node's getFeeEstimate, read only; no sender reads it. Public mempool is getInfo's mempool size on each kept public kaspad.
