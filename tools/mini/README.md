> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Kaspa Testnet-10 only. No id, key, address, host, or port in this folder.

# Mini's second read, pre-run 12

- `mini-runner.mjs`: pre-run 11's Mini counter, pointed at this repo, with pre-run 12's five tiers (floor 1–4, r110 5–7, r126 8–10, r150 11–13, r200 14–16) and the observation-only steps. One hop per transaction (lock line (xi)).
- `mini-classify-test.mjs`: offline check of the one-hop-per-transaction fix.
- `mini-dedupe-test.mjs`, `mini-dedupe.mjs`: pre-run 9's dedupe and its offline check, unchanged.
