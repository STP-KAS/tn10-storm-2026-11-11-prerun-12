> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Kaspa Testnet-10 only. No id, key, address, host, or port in this folder.

# Desk runner, pre-run 12

The private config, key file, node addresses and kit stay on the desk. Nothing here starts a machine.

- `desk-runner.mjs`: pre-run 11's runner plus (xiv) five fee tiers on the desk's private node (floor 100, r110, r126, r150, r200; kit20 is kit19 with this repo's `family-fees.mjs`) and (xv) no payment sender: BASE 8 minutes, HOLD-1..3 as observation stretches OBS-1..3 (12 minutes each), the pinned HOLD-4 minute, RETURN 8 minutes, a 5-minute counter tail. Each step file carries a per-minute tier table against the probe's ready mass and the outside fee-100 stream. `STORM_NO_PAY=0` puts pre-run 11's payment path back (not used here).
- `mempool-probe.mjs`: pre-run 11's read-only probe plus a heavy count (mass over 200,000) and a heavy-and-ready count per outside fee bucket. It submits nothing.
- `counter.mjs`, `pay2.mjs`, `paypool.mjs`, `preflight.mjs`: pre-run 11's, unchanged (the counter takes the tiers from `family-fees.mjs`; the payment senders are not started in pre-run 12).
