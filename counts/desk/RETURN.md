OBSERVATION

Not scored. No payment of ours in pre-run 12: families only, on the desk's private node.

# RETURN, desk, pre-run 12

> Our own TN10 testing: what we observed in this run, on our own desk node. Counts only. Included is what the desk's private TN10 node accepted on chain, read by the desk counter, by accepting chain block time. Mini's files are a second read.

RETURN is families only, 8 whole minutes, the last stretch before the families stop. Not scored.

Families offer 1.2 hop/s, 16 families live, one family-sender process and one builder: floor (families 1–4) 100 sompi/gram on the desk's private node, r110 (families 5–7) 110 sompi/gram on the desk's private node, r126 (families 8–10) 126 sompi/gram on the desk's private node, r150 (families 11–13) 150 sompi/gram on the desk's private node, r200 (families 14–16) 200 sompi/gram on the desk's private node. No payment sender was started.

## Tiers against the mempool, per minute

| Minute (UTC) | floor (100) | r110 (110) | r126 (126) | r150 (150) | r200 (200) | Ready mass, blocks | Outside at 100, n | Outside at 100, heavy (>200k mass) / ready | Mempool | Fee estimate priority |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|
| 2026-11-12T11:33 | 154 | 115 | 120 | 130 | 137 | 3.53 | 4 | 4 / 4 | 17 | 100.0 |
| 2026-11-12T11:34 | 108 | 89 | 96 | 105 | 123 | 6.78 | 11 | 11 / 11 | 20 | 115.7 |
| 2026-11-12T11:35 | 129 | 92 | 107 | 115 | 134 | 6.24 | 8 | 8 / 8 | 19 | 120.8 |
| 2026-11-12T11:36 | 86 | 75 | 88 | 104 | 127 | 6.81 | 9 | 9 / 9 | 26 | 113.1 |
| 2026-11-12T11:37 | 117 | 96 | 110 | 118 | 138 | 7.75 | 10 | 10 / 10 | 29 | 114.3 |
| 2026-11-12T11:38 | 154 | 124 | 128 | 130 | 138 | 4.02 | 5 | 5 / 5 | 19 | 100.0 |
| 2026-11-12T11:39 | 107 | 90 | 98 | 108 | 129 | 8.70 | 12 | 12 / 12 | 28 | 121.5 |
| 2026-11-12T11:40 | 121 | 98 | 107 | 110 | 129 | 5.90 | 7 | 7 / 7 | 25 | 103.2 |

Hops are what the desk counter read as accepted on chain in that minute, per tier. Ready mass, blocks, is the median of the probe's samples in the minute (block limit 500,000). Outside at 100 is the median count of mempool entries not in our logs paying 100 sompi/gram, and heavy is how many of those had a mass over 200,000 (median of samples). The outside stream is not attributed to anyone.

## Chain, desk counter

| Minute (UTC) | Included, all non-coinbase | Our payments included | Floor hops (100) | R110 hops (110) | R126 hops (126) | R150 hops (150) | R200 hops (200) | Other traffic | Chain blocks | DAA gap max | Sink age max, ms | Final after, s | Counter |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| 2026-11-12T11:33 | 4,092 | 0 | 154 | 115 | 120 | 130 | 137 | 3,450 | 367 | 1 | 637 | 20 | kept pace |
| 2026-11-12T11:34 | 4,023 | 0 | 108 | 89 | 96 | 105 | 123 | 3,502 | 358 | 0 | 317 | 20 | kept pace |
| 2026-11-12T11:35 | 4,062 | 0 | 129 | 92 | 107 | 115 | 134 | 3,486 | 370 | 1 | 452 | 20 | kept pace |
| 2026-11-12T11:36 | 4,005 | 0 | 86 | 75 | 88 | 104 | 127 | 3,527 | 346 | 0 | 399 | 20 | kept pace |
| 2026-11-12T11:37 | 4,055 | 0 | 117 | 96 | 110 | 118 | 138 | 3,477 | 357 | 1 | 406 | 19 | kept pace |
| 2026-11-12T11:38 | 4,111 | 0 | 154 | 124 | 128 | 130 | 138 | 3,444 | 357 | 1 | 327 | 20 | kept pace |
| 2026-11-12T11:39 | 4,257 | 0 | 107 | 90 | 98 | 108 | 129 | 3,726 | 356 | 1 | 347 | 20 | kept pace |
| 2026-11-12T11:40 | 4,129 | 0 | 121 | 98 | 107 | 110 | 129 | 3,565 | 392 | 1 | 331 | 19 | kept pace |

Coinbase is taken out as one per merged blue block (on this node a chain block's accepted list carries the coinbase of each blue block it merges). Other traffic is the rest: other users' load, the genesis, and anything not in our logs.

## Hop rate per cohort, as built

Floor (families 1–4, desk private node): 100 sompi/gram per hop. R110 (families 5–7, desk private node): 110 sompi/gram per hop. R126 (families 8–10, desk private node): 126 sompi/gram per hop. R150 (families 11–13, desk private node): 150 sompi/gram per hop. R200 (families 14–16, desk private node): 200 sompi/gram per hop. The rate rides on each hop line to the one builder. Payments pay 150.

## Funding coins, as read from the desk node

The funding coins were not one size. Sizes seen, whole tKAS (coins): 15 (443), 16 (440), 18 (425), 17 (425), 14 (399), 19 (372), 13 (327), 20 (321), 12 (297), 21 (271), 11 (226), 22 (225), and 69 more sizes. The fee is not called the whole cause.

## Minutes

| Minute (UTC) | Pay submit-OK | Attempts | Rejects, rate | Rejects, full | Other | Floor OK / att / rate rej / full rej / waiting | R110 OK / att / rate rej / full rej / waiting | R126 OK / att / rate rej / full rej / waiting | R150 OK / att / rate rej / full rej / waiting | R200 OK / att / rate rej / full rej / waiting | Family stalls logged | Family node mempool-high marks | Clean |
|---|---:|---:|---:|---:|---:|---|---|---|---|---|---:|---:|---|
| 2026-11-12T11:33 | 0 | 0 | 0 | 0 | 0 | 154 / 355 / 0 / 0 / 4 | 116 / 262 / 0 / 0 / 3 | 120 / 265 / 0 / 0 / 3 | 130 / 272 / 0 / 0 / 3 | 138 / 275 / 0 / 0 / 2 | 0 | 0 | yes |
| 2026-11-12T11:34 | 0 | 0 | 0 | 0 | 0 | 106 / 334 / 0 / 0 / 2 | 89 / 252 / 0 / 0 / 3 | 96 / 252 / 0 / 0 / 3 | 104 / 266 / 0 / 0 / 2 | 124 / 271 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T11:35 | 0 | 0 | 0 | 0 | 0 | 131 / 338 / 0 / 0 / 4 | 92 / 253 / 0 / 0 / 3 | 107 / 253 / 0 / 0 / 3 | 116 / 262 / 0 / 0 / 3 | 134 / 268 / 0 / 0 / 3 | 0 | 0 | yes |
| 2026-11-12T11:36 | 0 | 0 | 0 | 0 | 0 | 85 / 318 / 0 / 0 / 3 | 74 / 243 / 0 / 0 / 2 | 87 / 252 / 0 / 0 / 2 | 103 / 260 / 0 / 0 / 2 | 126 / 270 / 0 / 0 / 2 | 0 | 0 | yes |
| 2026-11-12T11:37 | 0 | 0 | 0 | 0 | 0 | 117 / 336 / 0 / 0 / 3 | 96 / 264 / 0 / 0 / 2 | 110 / 263 / 0 / 0 / 2 | 116 / 268 / 0 / 0 / 0 | 136 / 273 / 0 / 0 / 0 | 0 | 0 | yes |
| 2026-11-12T11:38 | 0 | 0 | 0 | 0 | 0 | 155 / 347 / 0 / 0 / 4 | 125 / 268 / 0 / 0 / 3 | 129 / 272 / 0 / 0 / 3 | 133 / 269 / 0 / 0 / 3 | 139 / 277 / 0 / 0 / 1 | 0 | 0 | yes |
| 2026-11-12T11:39 | 0 | 0 | 0 | 0 | 0 | 107 / 328 / 0 / 0 / 4 | 90 / 257 / 0 / 0 / 3 | 97 / 256 / 0 / 0 / 2 | 108 / 262 / 0 / 0 / 3 | 130 / 273 / 0 / 0 / 2 | 0 | 0 | yes |
| 2026-11-12T11:40 | 0 | 0 | 0 | 0 | 0 | 120 / 336 / 0 / 0 / 3 | 97 / 253 / 0 / 0 / 2 | 105 / 262 / 0 / 0 / 0 | 107 / 261 / 0 / 0 / 0 | 128 / 265 / 0 / 0 / 1 | 0 | 0 | yes |

A family stall is a coordinator mark: no hop of that family landed for a while. The family was still attempting. It is logged, and it does not make the minute dirty.

A mempool-high mark means the family node read a mempool at or over 90,000. In pre-run 12 that does not stop the families: the skip does not apply to them. A skip, if one were set, is dirt with its reason (node-skip-fam) for every minute it covers, and it clears when the mempool falls back under the line.

Within 10 percent means 0 to 0 submit-OK in the minute.

## Public nodes (local numbers)

Kept: 1, 5. The family sender reads and submits every tier on the desk's private node, which the desk counter reads. The kept public kaspads are read for sync and DAA only; no payment of ours went to them.

Kept nodes are unique kaspads: each answered with its own node id at the preflight. 3 candidate endpoints passed the check and were 2 kaspads (node 4 is node 1; the second hostname was not used). 3 payment senders per kaspad.

| Node | Synced every sample | Last DAA | Pay submit-OK | Pay rejects | Dropped sockets | Answer ms, median |
|---:|---|---:|---:|---:|---:|---:|
| 1 | yes | 621474711 | 0 | 0 | 0 | 32 |
| 5 | yes | 621474711 | 0 | 0 | 0 | 40 |

## Hop submit to landing, per cohort

| Cohort | Landed of OK | Median ms | Slow tail (p95) ms |
|---|---:|---:|---:|
| floor | 975 of 975 | 1366 | 4273 |
| r110 | 779 of 779 | 1318 | 3782 |
| r126 | 851 of 851 | 1281 | 3260 |
| r150 | 917 of 917 | 1218 | 2894 |
| r200 | 1055 of 1055 | 1123 | 1970 |

Landing is the accepting block header time the desk's coordinator read. Waiting is submitted-OK not yet landed at the minute's end. Every tier has the same hop shape and the same node; only the rate differs.

## Mempool and template, desk node (probe)

| Minute (UTC) | Samples | Mempool | Ready (no parent in mempool) | Ready mass, blocks of 500k | Other traffic in mempool | Other ready | Other at 100, n | Other at 100, mean mass | Our payments in mempool | Floor in mempool / ready | R110 in mempool / ready | R126 in mempool / ready | R150 in mempool / ready | R200 in mempool / ready | Template txs | Template storage mass | Template txs over 100k storage mass | Template: payments | Template: floor | Template: r110 | Template: r126 | Template: r150 | Template: r200 | Template: other | Fee estimate priority / normal / low | Public 1 mempool | Public 5 mempool |
|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|
| 2026-11-12T11:33 | 3 | 17 | 21 | 3.53 | 6 | 6 | 4 | 266,597 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 469,299 | 1 | 0 | 1 | 1 | 1 | 0 | 0 | 1 | 100.0 / 100.0 / 100.0 | 11 | 12 |
| 2026-11-12T11:34 | 3 | 20 | 23 | 6.78 | 12 | 12 | 11 | 266,594 | 0 | 4 / 4 | 3 / 3 | 2 / 2 | 3 / 3 | 2 / 2 | 4 | 349,174 | 1 | 0 | 0 | 0 | 0 | 0 | 1 | 3 | 115.7 / 111.0 / 103.3 | 11 | 14 |
| 2026-11-12T11:35 | 3 | 19 | 30 | 6.24 | 14 | 14 | 8 | 266,592 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 307,473 | 1 | 0 | 0 | 0 | 0 | 0 | 0 | 1 | 120.8 / 114.3 / 104.2 | 10 | 25 |
| 2026-11-12T11:36 | 3 | 26 | 26 | 6.81 | 11 | 11 | 9 | 266,589 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 8 | 390,927 | 1 | 0 | 1 | 0 | 0 | 0 | 2 | 3 | 113.1 / 109.3 / 102.8 | 25 | 26 |
| 2026-11-12T11:37 | 3 | 29 | 29 | 7.75 | 13 | 13 | 10 | 266,586 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 4 | 349,647 | 1 | 0 | 0 | 0 | 0 | 0 | 1 | 2 | 114.3 / 110.0 / 103.1 | 50 | 38 |
| 2026-11-12T11:38 | 3 | 19 | 23 | 4.02 | 7 | 7 | 5 | 266,586 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 8 | 472,470 | 1 | 0 | 1 | 0 | 0 | 0 | 3 | 3 | 100.0 / 100.0 / 100.0 | 11 | 13 |
| 2026-11-12T11:39 | 3 | 28 | 31 | 8.70 | 15 | 15 | 12 | 266,584 | 0 | 4 / 4 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 4 | 307,423 | 1 | 0 | 0 | 0 | 0 | 0 | 1 | 2 | 121.5 / 114.8 / 104.3 | 77 | 28 |
| 2026-11-12T11:40 | 3 | 25 | 24 | 5.90 | 12 | 11 | 7 | 266,581 | 0 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 3 / 3 | 6 | 474,380 | 1 | 0 | 1 | 0 | 0 | 1 | 2 | 2 | 103.2 / 102.3 / 100.8 | 20 | 22 |

Read by the probe on the desk's private TN10 node every 20 s, read-only; each cell is the median of that minute's samples. Ready means no parent in the mempool: in rusty-kaspa v2.1.0 only those are in the selector's frontier. Ready mass is compared with one block's mass limit (500,000): at or under 1 the selector takes all ready transactions best-first; over 1 it samples at random weighted by (fee/mass)^3 (over 4, sample_inplace). Mass is the larger of compute and storage mass, as the v2.1.0 selector normalises it (transient mass is not in the RPC). Other traffic is every mempool entry not in our sender logs; its fee rate is the node's fee over that mass. Template transactions carry no id in the RPC, so each is matched to a mempool entry by its first input. The template is the desk node's own getBlockTemplate (never submitted): what this node would put in a block at that moment, not a miner's template. The fee estimate is the node's getFeeEstimate, read only; no sender reads it. Public mempool is getInfo's mempool size on each kept public kaspad.
