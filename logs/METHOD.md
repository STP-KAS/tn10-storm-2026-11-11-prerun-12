# Method, pre-run 12

> This is our own Kaspa Testnet-10 testing. What follows is what we observed in this run, on our own nodes; it is not a claim of how TN10 or Kaspa behave in general.

> Counts only. Desk side. Submit-OK is the desk sender log; included is the desk counter's read of what the desk's private TN10 node accepted on chain. Mini's files are a second read.

Steps: BASE 8 min, HOLD-1..3 = OBS-1..3 12 min each, the HOLD-4 minute, RETURN 8 min, then a 5-minute counter tail.

Accepted hops per cohort, as the desk's coordinator read them: floor 9,233, r110 7,125, r126 7,512, r150 7,911, r200 8,637.

Per step (all OBSERVATION, families only, no payment of ours):

- BASE: OBSERVATION, submit-OK 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; our payments included 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; hops included floor/r110/r126/r150/r200 1317/1007/1046/1081/1147; counter minutes not kept-pace 0 of 8.
- HOLD-1: OBSERVATION, submit-OK 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; our payments included 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; hops included floor/r110/r126/r150/r200 1862/1421/1503/1582/1737; counter minutes not kept-pace 0 of 12.
- HOLD-2: OBSERVATION, submit-OK 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; our payments included 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; hops included floor/r110/r126/r150/r200 2126/1625/1640/1682/1733; counter minutes not kept-pace 0 of 12.
- HOLD-3: OBSERVATION, submit-OK 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; our payments included 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; hops included floor/r110/r126/r150/r200 1641/1283/1368/1459/1610; counter minutes not kept-pace 0 of 12.
- HOLD-4: OBSERVATION, submit-OK 0; our payments included 0; hops included floor/r110/r126/r150/r200 128/96/110/121/133; counter minutes not kept-pace 0 of 1.
- RETURN: OBSERVATION, submit-OK 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; our payments included 0 / 0 / 0 / 0 / 0 / 0 / 0 / 0; hops included floor/r110/r126/r150/r200 976/779/854/920/1055; counter minutes not kept-pace 0 of 8.

Decent on the desk side: every step file reached origin.

## Selection rule, read before the run

The desk node and the kept public kaspads answered serverVersion 2.1.0 at the preflight. In rusty-kaspa tag v2.1.0 (commit 01b532e8b553523216471682649693af92f0fd16), `mining/src/mempool/model/frontier.rs` `build_selector` takes every ready transaction best-first while the ready set's mass fits one block, and otherwise samples at random with weight (fee/mass)^3 (`ALPHA = 3` in `mining/src/mempool/model/frontier/selectors.rs`, weight in `mining/src/mempool/model/frontier/feerate_key.rs`): `sample_inplace` above four blocks' mass, `MutatingTreeSelector` between one and four. Only a transaction with no parent in the mempool is in the ready set (`mining/src/mempool/model/transactions_pool.rs`), so a chained hop is not a candidate until its parent is out of the mempool. Against an outside stream at 100, the weights are 1.00 (100), 1.33 (110), 2.00 (126), 3.38 (150) and 8.00 (200), per unit of mass. A higher fee raises the odds; it does not buy a place in a queue. This is the source's rule, read from the code; the run does not see a miner's template.

Hop rates per hop, one builder: floor (families 1–4) 100 sompi/gram on the desk's private node, r110 (families 5–7) 110 sompi/gram on the desk's private node, r126 (families 8–10) 126 sompi/gram on the desk's private node, r150 (families 11–13) 150 sompi/gram on the desk's private node, r200 (families 14–16) 200 sompi/gram on the desk's private node. Payments 150. The funding coins were not one size, so the fee is not called the whole cause. Every tier was read and submitted on the desk's private TN10 node, which also ran the counter. No payment sender was started; 2 unique public kaspads were read for sync only.

## Misses

- none

## Fixes

- none

## On origin

- counts/desk/BASE.md: 2026-11-12T10:48:22Z
- counts/desk/HOLD-1.md: 2026-11-12T11:01:22Z
- counts/desk/HOLD-2.md: 2026-11-12T11:14:22Z
- counts/desk/HOLD-3.md: 2026-11-12T11:27:22Z
- counts/desk/HOLD-4.md: 2026-11-12T11:32:23Z
- counts/desk/RETURN.md: 2026-11-12T11:41:21Z
- counts/chain/TIMELINE.md: 2026-11-12T11:46:33Z
- counts/chain/MEMPOOL.md: 2026-11-12T11:46:36Z
