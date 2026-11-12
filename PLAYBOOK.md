> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value.
>
> **This is the playbook for pre-run 12.** It is not Wednesday. It is not Tuesday. It is not pre-run 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, or 11. It does not start a machine and it does not arm one.

# Playbook

Who does what, and the gates before each machine may start. The plan is [plan/PLAN.md](plan/PLAN.md), the locks are [locks/LOCKED.md](locks/LOCKED.md), and the go files are the three GO pages. This page does not override them.

## Oversight

TN10 ops oversees this rehearsal end to end: Mini, the desk (Build), and the bot. TN10 only. Never mainnet. Do not edit the Tuesday repo, the Wednesday repo, or pre-run 1's to 11's go files. Do not write `REVIEW_CLOSED`.

For pre-run 12 the operator does not paste. On 2026-11-12 he asked TN10 ops for covenant pre-runs under congestion and competition, pre-run 11 and then 12, 13 or more as needed (voice, 09:06 and 09:09 Brussels time), and at 10:04 in chat said "Keep exploring". That is the arm. The agents start their runners once the gates are facts.

## Start gates

1. **Mini node synced.** Existing TN10 kaspad, existing data, no wipe. `isSynced` true, DAA moving.
2. **Desk node synced.** Existing private TN10 kaspad, existing data, loopback only, started with `pwsh`. No wipe. Synced, DAA moving.
3. **No other runner.** No earlier runner, waiter, or counter on any machine. Lane above the abort line. The desk's private candidate list is present and not empty (`HELD candidates-missing` otherwise).
4. **Hashes.** `hashes/SIXTEEN.md` with sixteen rows and an On origin line, from [tools/sixteen](tools/sixteen/README.md).
5. **Open.** The desk pushes `logs/PRE-RUN-OPEN.md`. Mini then pushes `logs/MINI-ARMED.md`.
6. **Counter, families, senders.** The desk runner starts the counter on its private node and waits for its start line (`HELD counter-down` otherwise). Then the genesis from the bundle that wrote `hashes/SIXTEEN.md`, the families, and the payment steps.

## Who does what

| Who | Role | What not to do |
|---|---|---|
| **Desk (Build)** | Sends the sixteen families (five fee tiers, one path, one build). No payments. Its private TN10 node counts what the chain accepted (lock line (iv)) and its probe reads the mempool (xii). Publishes `hashes/SIXTEEN.md`, `logs/PRE-RUN-OPEN.md`, `counts/desk/` per step, `counts/chain/TIMELINE.md` and `MEMPOOL.md` after the tail, and `logs/METHOD.md`. | Do not stop or wipe the desk node. No Windows PowerShell 5.1, no `KaspaPublicNode`, no miner, no devnet. No 8- or 32-family publisher. No second runner. Never restart the runner mid-run. No payment sender, no heavy lane. |
| **Mini** | Second chain read on its own node. Does not send, mine, or hold a key. Publishes `logs/MINI-ARMED.md`, then `counts/mini/` when the matching desk file is on origin. | Do not wipe. Do not repeat the desk's head as Mini's. |
| **Bot (TN10 ops)** | Sends payments in the HOLD-4 minute only, on a synced public kaspad that is not one the desk kept, or publishes a legal `NO SEND`. | Do not send in any other step. One waiter. No local node. |

## Status when this repo was opened

Not a gate. Read on 2026-11-12 between 09:55Z and 10:10Z. This is our own TN10 testing; status lines are what we read on our own machines.

- Mini: existing TN10 kaspad 2.1.0 up, no wipe. Pre-run 11's Mini runner ended at 2026-11-12T09:56:38Z.
- Desk: existing private TN10 kaspad 2.1.0 up with `pwsh`, no wipe. It is not stopped for this pre-run. No pre-run 11 runner or child is running.
- Box: no local TN10 node. No bot waiter running.
- Lane: keys 1–15 got a fresh genesis coin from the lane at 2026-11-12T10:06:32Z (15 transactions, none rejected; amounts and ids in private notes). Lane before that: 5,510 coins, 215,651 usable tKAS, above the abort line. The payment key's 8,400 coins are not used in pre-run 12.
- Known risks, not fixed mid-run:
  - The outside fee-100 stream may be there or not. The probe records it either way; if it is absent, the run is the control.
  - With no payments of ours, the ready mass may stay under one block for long stretches; then the selector takes everything and the tiers are not expected to separate.
  - Each family is a chain of hops, so a hop waits for its parent whatever its fee.
  - The probe reads the desk node's mempool and template, not a miner's.
  - Only two unique public kaspads answered in every check so far, and the desk keeps both, so the bot is expected to file `NO SEND no-free-node`.

## Offline rehearsal, recorded before `PRE-RUN-OPEN`

Rehearsal A (p12-a), 2026-11-12 10:13:03Z to 10:35:25Z (desk, Brussels 11:13 to 11:35). The real pre-run 12 desk runner, counter and read-only mempool probe ran with the rehearsal family sender, the stand-in genesis submit (it writes state files and submits nothing) and pre-run 9's stand-in node, against a local bare origin. Short times: BASE, OBS-1..3 and RETURN 2 minutes each, a 2-minute tail.

- FEE_SPLIT verified on the submit rows: floor 100, r110 110, r126 126, r150 150, r200 200, every tier on the desk path. No payment sender was started (`senders=0`).
- BASE, HOLD-1, HOLD-2, HOLD-3 (OBS-1..3), the pinned HOLD-4 minute (10:29Z) and RETURN published as `OBSERVATION`; each step file carried the new per-minute tier table, the chain table and the probe table. `counts/chain/TIMELINE.md`, `counts/chain/MEMPOOL.md` and `logs/METHOD.md` were published and the runner exited 0. No rehearsal process was left running.
- The probe read the real desk node (read-only), so its columns show the outside fee-100 heavy stream present at that time (10 to 16 entries, nearly all ready, ready mass 5 to 8 blocks) and none of our rehearsal hops (they went to the stand-in). The stand-in lands hops by its own rule, so its tier numbers are not a network result.
- Before the rehearsal, `fee-check.mjs --builder` built hops offline in one builder process from the check bundle: mass 13,046 in every tier, fee 1,304,600 / 1,435,060 / 1,643,796 / 1,956,900 / 2,609,200 sompi (mass times 100 / 110 / 126 / 150 / 200). Nothing was submitted.
- A setup slip of mine, recorded: a PowerShell loop variable overwrote the rehearsal folder variable, so the first copy of the rehearsal tools landed in the desk's private sixteen folder. I removed those three copied folders and rebuilt the rehearsal folder before it ran. No node was touched and the published bundle was not changed.

## Status after the live run

AFTER_PLACEHOLDER

## When something breaks

Append a worked fix to [locks/LOCKED.md](locks/LOCKED.md) in the form that page shows, and a repair line to `logs/FIXES.md`. If the run dies before RETURN, write `logs/FAILED.md`, stop every runner, waiter, and counter, and do not resume. The next attempt is a new repo that starts from this repo's lock file.
