> **Experimental. We are just trying this.** [Disclaimer](../DISCLAIMER.md) · This page does not start a machine. Pre-run 42. Not Wednesday. Not Tuesday. Not pre-run 1 to 41.

# Targets

Pre-run 41 held one hundred chains with the ready cap off and a fee cap of 3,000 tKAS. Pending reached 100. Submit-OK was 558–658 a minute. In the twelve samples while our heavy class was 88–100, the template's heavy count stayed 1, and ready mass was 54.96–76.80 blocks. The fee cap stopped new submits at 17:56:03Z. The pause at 80 blocks did not trip. One hundred is this lane's own clamp, so the chain count cannot be the next knob. The next single knob is the fee cap, 3,000 to 6,000 tKAS.

**Question.** On our desk node, with one hundred chains, the rate held, and no ready cap, what happens to ready mass and to the lane's pause when the fee cap is 6,000 tKAS instead of 3,000? We do not expect the template's heavy count to rise. Finding 33 already says a second transaction of about 267,000 storage mass does not fit a 500,000-mass block.

**Target.** The lane runs only in the middle step and is at zero at the end. A table, written after the tail from this run's own files, shows template storage mass, template transaction count, ready mass, and the fee estimate, for the baseline minutes, the hold minutes, and the return minutes. **Met means the table exists and the lane is at zero, not that a particular theory won.** If the fee cap or the pause stops new submits before the six minutes are up, the table still counts.

## Why the twelve families are not in this run

At 2026-11-14T18:02:39Z the funding key's usable balance (coins over 3 tKAS, above that line) was 17,905 tKAS. That is the same figure as the 17:41:49Z read. Pre-runs 36 through 41 did not spend that key. A family window aborts under 18,000 tKAS. This run does not start the families, the mint line, or the guest. The two keys this series leaves unused stay unused.

## The pile, read before the arm

The lane takes a coin only when that coin is at or above 10 tKAS. At 2026-11-14T18:02:39Z the payment pile had 195 such coins, together 3,828 tKAS, and 3,794 coins between 2 and 10 tKAS, together 29,369 tKAS. 3,828 tKAS does not cover a 6,000 tKAS fee cap.

After this plan is on origin, and before the lane process starts, this run joins the pile's own coins that are between 2 and 10 tKAS into coins of 40 tKAS on the same pile, and stops at 120 of those coins or sooner if a submit is rejected. It does not spend a coin already at or above 10 tKAS. It does not touch the funding key or the two unused keys. Value stays on the pile. Nothing moves onto the funding key. The lane starts only after a fresh read can see the new coins.

## The one change, written before the arm

**Fee cap 6,000 tKAS. One hundred chains stay. The ready cap stays off.** Our heavy lane (the same shape as pre-run 41: one input, two outputs, storage mass about 266,666, submitted only to the desk's private node). The rate is 460 sompi per gram, held. No second lane. No climb toward 1,405 or 2,000. The moved cap is 7,000 tKAS, so it sits above the fee cap and is not the knob. The pile floor stays 200 tKAS. The lane's existing pause, at mempool size 90,000 or ready mass over 80 blocks, stays in the code. That pause is what this run is here to observe. It is not a second knob. The join above is setup. It is not the knob.

**While it runs it slows other users' low-fee transactions on our node. We say so here, in public.**

| Order | Step | Lane | Length |
|---:|---|---|---:|
| 1 | BASE | off (N=0, ready cap 0) | 3 whole minutes |
| 2 | HOLD | N=100, ready cap off, rate 460, fee cap 6,000 tKAS | 6 whole minutes |
| 3 | RETURN | off | 3 whole minutes |

The desk node is not restarted. One counter: the desk. The Mini is not reachable. No payment flood. No heavy submit to a public node.

Disk line: abort if the desk is under 150 GB free.
