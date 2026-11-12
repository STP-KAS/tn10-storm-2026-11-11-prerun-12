> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value.
>
> **This is a pre-run. Pre-run 12.** It is not the Wednesday run. It is not the Tuesday run. It is not pre-run 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, or 11. A read does not start a runner.

# tn10-storm-2026-11-11-prerun-12

**Pre-run 12 of the Wednesday neuron.** The neuron stays [tn10-storm-2026-11-11](https://github.com/STP-KAS/tn10-storm-2026-11-11). This repo does not edit that repo, does not write `REVIEW_CLOSED`, and does not set or move a clock for it. [tn10-storm-2026-11-10](https://github.com/STP-KAS/tn10-storm-2026-11-10) (Tuesday) is not edited from here either.

> **Our own testing.** This is our own Kaspa Testnet-10 testing, run on our own machines and nodes. What these pages report is what we observed in this run; it is not a claim of how TN10 or Kaspa behave in general.

**Where this starts.** Pre-runs 1 to 4 failed and are closed. Pre-runs 5 to 11 finished through RETURN and are closed. The index of all of them is the [pre-run 2 README](https://github.com/STP-KAS/tn10-storm-2026-11-11-prerun-2#pre-runs-in-this-rehearsal); the cumulative findings are in [tn-master](https://github.com/STP-KAS/tn-master). This repo starts from [pre-run 11's locks/LOCKED.md](https://github.com/STP-KAS/tn10-storm-2026-11-11-prerun-11/blob/e185e5b/locks/LOCKED.md) at commit e185e5b, copied here as [locks/LOCKED.md](locks/LOCKED.md), with a pre-run 12 section added at the end.

## What pre-run 11 left open

In [pre-run 11](https://github.com/STP-KAS/tn10-storm-2026-11-11-prerun-11) the floor tier (100 sompi/gram) followed the ready mass in the desk node's mempool, not our payment offer. Much of that ready mass was another TN10 sender's chained stream of heavy transactions (about 267,000 storage mass each) paying exactly 100 sompi/gram, the floor's own rate. In RETURN, with no payments of ours and that stream's backlog draining, the tiers separated by fee: floor about 12–26 hops a minute, double (200) about 65–100, triple (300) about 113–131, against about 113–175 for floor in BASE. We did not attribute the stream to anyone.

## What pre-run 12 tries

The question: **what fee keeps a covenant chain moving when it competes with heavy same-fee outside transactions in the mempool?**

- **Five fee tiers just above the floor**, all on the desk's private node, one build, one builder: floor (families 1–4) 100, r110 (5–7) 110, r126 (8–10) 126, r150 (11–13) 150, r200 (14–16) 200 sompi/gram. 126 is the priority rate the desk node's fee estimate read before pre-run 11; 150 is the rate our payments paid in pre-runs 7–11. Sixteen families allow 4 + 3 + 3 + 3 + 3, so the shape fits as asked.
- **No payment load of ours.** No payment sender is started. The only competition is whatever other TN10 traffic is there.
- **Long observation stretches.** BASE (8 whole minutes), then three 12-minute stretches OBS-1, OBS-2, OBS-3, published under the file names HOLD-1, HOLD-2 and HOLD-3 so the bot's and Mini's gates read as before, the pinned HOLD-4 minute, RETURN (8 minutes), and the counter's 5-minute tail. All are `OBSERVATION`; nothing is scored.
- **Read against the probe.** Each step file carries a per-minute table: hops per tier (desk counter) next to the ready mass and the count of outside fee-100 entries (and how many are heavy, over 200,000 mass) in the desk node's mempool.
- **If the outside stream is absent, the run goes on and says so.** That is the control: whether the tiers separate without it.
- **No heavy lane of our own.** We do not build or submit our own heavy-mass competitor in this repo. That needs the operator's explicit OK. A note on how one would reach about 267,000 storage mass, measured offline with nothing submitted, is in [logs/LESSONS.md](logs/LESSONS.md) after the run.

All locked lines from earlier pre-runs stay, except where the pre-run 12 block in [locks/LOCKED.md](locks/LOCKED.md) says what changes and why.

## Machines

| Machine | Go file | First sentence |
|---|---|---|
| Desk | [GO-DESK.md](GO-DESK.md) | DESK. I send and count on pre-run 12. This is not Wednesday. |
| Mini | [GO-MINI.md](GO-MINI.md) | MINI. I count pre-run 12 as the second read. I do not send. This is not Wednesday. |
| Bot | [GO-BOT.md](GO-BOT.md) | GROKBOT. I send payments on the pre-run 12 HOLD-4 only. I do not count. This is not Wednesday. |

The operator does not paste. On 2026-11-12 he asked TN10 ops for covenant pre-runs under congestion and competition, pre-run 11 and then 12, 13 or more as needed (voice, 09:06 and 09:09 Brussels time), and at 10:04 in chat said "Keep exploring". That is the arm for pre-run 12. The agents start the runners once the gates are facts. [GO.md](GO.md) is the map, [PLAYBOOK.md](PLAYBOOK.md) has the roles and gates, and [plan/PLAN.md](plan/PLAN.md) has the targets and the reasons.

## Gates, in order

No clock. Each gate is a fact read from a node or from origin.

1. Mini's TN10 node is up from its own data, synced, DAA moving.
2. The desk's private TN10 node is up from its own data (PowerShell 7), synced, DAA moving.
3. No other runner or waiter is up. The lane is above the abort line (2,500 coins, 18,000 usable tKAS). The desk's private candidate list is present.
4. `hashes/SIXTEEN.md` is on origin: sixteen rows and an On origin line, from the sixteen-family path.
5. The desk pushes `logs/PRE-RUN-OPEN.md`; Mini pushes `logs/MINI-ARMED.md`.
6. The probe and the desk counter are up. Then the families and the observation steps.

## What a decent result is

- `hashes/SIXTEEN.md` on origin before the first family submit.
- Every step file on origin, each with hops per minute for all five tiers and the probe's table for the same minutes.
- `counts/chain/TIMELINE.md` and `counts/chain/MEMPOOL.md` after the tail.
- An answer to the question, or an honest "not answered" with the reason (for example, the outside stream was not there).
- A HOLD-4 desk file, a bot file or a legal `NO SEND`, and a Mini file.
- No id, txid, key, address, host, or port in this repo.

A miss stays in this repo. A next attempt is a new repo and starts from this repo's lock file.

**Part of [tn-master](https://github.com/STP-KAS/tn-master).** The rule is [docs/NEURON.md](https://github.com/STP-KAS/tn-master/blob/main/docs/NEURON.md). This pre-run is its own row. It is not row 47.
