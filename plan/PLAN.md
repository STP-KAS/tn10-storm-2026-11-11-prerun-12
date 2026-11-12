> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This page does not start a machine. Pre-run 12. Not Wednesday. Not Tuesday. Not pre-run 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, or 11.

# Targets

There is no T0. There is no public clock. There is no latest minute. Nothing in pre-run 12 is scored: every step is an observation of whole minutes.

The hash file comes first and does not wait for the open. Nothing else in this page starts until the gates are true: Mini's TN10 node is synced with DAA moving; the desk's private TN10 node is up from its own data (PowerShell 7, no wipe) and synced; no Tuesday, Wednesday, or pre-run 1 to 11 runner is up; the operator has armed (no paste; see the README); and this repo's `logs/PRE-RUN-OPEN.md` is on origin.

## Order

1. **Nodes live.** Both TN10 nodes synced, DAA moving. No wipe.
2. **Hashes first.** [hashes/SIXTEEN.md](../hashes/README.md): sixteen rows, family label, tier, sha256 of the lowercase hex covenant id, and an On origin line.
3. **Families.** The sixteen covenant families start on the desk's private node, 1.2 hop/s offered.
4. **Observation steps, families only.** No payment sender of ours is started.

| Order | File | What it is | Length |
|---:|---|---|---|
| 1 | BASE | families only | 8 whole minutes |
| 2 | HOLD-1 | OBS-1, families only | 12 whole minutes |
| 3 | HOLD-2 | OBS-2, families only | 12 whole minutes |
| 4 | HOLD-3 | OBS-3, families only | 12 whole minutes |
| 5 | HOLD-4 | the pinned minute; the bot sends only on a free third public kaspad, or files `NO SEND` | 1 minute |
| 6 | RETURN | families only | 8 whole minutes |
| 7 | tail | families stopped, the counter reads on | 5 minutes |

The HOLD file names are kept on purpose: the bot pins HOLD-4 from HOLD-3's On origin time, and Mini publishes its second read when the matching desk file is on origin. In pre-run 12 they are names, not payment offers.

## Fee tiers

| Tier | Families | Rate, sompi/gram | Weight against an outside transaction at 100, per unit of mass |
|---|---|---:|---:|
| floor | 1–4 | 100 | 1.00 |
| r110 | 5–7 | 110 | 1.33 |
| r126 | 8–10 | 126 | 2.00 |
| r150 | 11–13 | 150 | 3.38 |
| r200 | 14–16 | 200 | 8.00 |

One build, one hop shape (13,046 mass per hop in pre-runs 6–11), one builder process, every tier on the desk's private node. The rate rides on each hop line; a hop's fee is its mass times its rate. Genesis 200.

## Why this shape

- Pre-run 11 tied the floor's speed to the ready mass and to an outside fee-100 heavy stream, not to our payments. The next question is the price of staying ahead of that stream, so the tiers sit between 100 and 200 rather than at 100 / 200 / 300 / 1000.
- No payments: our payments at 150 were themselves part of the ready mass in pre-run 11 and pushed the outside stream back. Leaving them out keeps the only competitor outside our control, and keeps us from crowding other users.
- Long stretches: the outside stream comes and goes over minutes; longer stretches give more minutes with it and without it in the same run.
- No heavy lane of our own: building our own heavy competitor would also delay other users' transactions. That needs the operator's explicit OK first.

## What we read

For each minute: hops per tier (desk counter, accepted on chain), the probe's median ready mass in blocks of 500,000, the median count of outside mempool entries at 100 sompi/gram and how many of those are heavy (over 200,000 mass), the mempool size and the fee estimate. Mini is a second read of the hops.

The answer we look for: the lowest tier whose hops per minute stay near its own rate in minutes without the outside stream, in minutes with it. If the outside stream is absent through the run, that is the control, and we report whether the tiers separate without it.

## Selection rule

The desk node and the public kaspads answered serverVersion 2.1.0. In rusty-kaspa tag v2.1.0 (commit 01b532e8b553523216471682649693af92f0fd16), `mining/src/mempool/model/frontier.rs` takes every ready transaction best-first while the ready set's mass fits one block, and otherwise samples at random with weight (fee/mass)^3 (`ALPHA = 3`). Only a transaction with no parent in the mempool is ready, so a chained hop is not a candidate until its parent is out of the mempool. A higher fee raises the odds of being drawn; it does not buy a place in a queue. This is the source's rule, read from the code; the run reads the desk node's own template, not a miner's.

Abort line **2,500 coins** and **18,000 usable tKAS**. Do not lower it.
