> **Experimental. We are just trying this.** [Disclaimer](DISCLAIMER.md) · Kaspa Testnet-10 only; tKAS has no value.
>
> **This is a pre-run. Pre-run 42.** It is not the Wednesday run. It is not the Tuesday run. It is not pre-run 1 to 41, and it does not edit their repos. A read does not start a runner.

# tn10-storm-2026-11-11-prerun-42

**Pre-run 42: one heavy lane of ours, one hundred chains, no ready cap, fee cap 6,000 tKAS, on the desk node, with the lane off at both ends.** The neuron stays [tn10-storm-2026-11-11](https://github.com/STP-KAS/tn10-storm-2026-11-11). This repo does not edit that repo.

> **Our own testing.** This is our own Kaspa Testnet-10 testing, run on our own machines and nodes. What these pages report is what we observed in this run; it is not a claim of how TN10 or Kaspa behave in general.

| Field | Value |
|---|---|
| Target | A table of the desk template and the desk fee estimate with our lane off, then at one hundred chains and no ready cap under a 6,000 tKAS fee cap, then off again. The lane returns to zero |
| The change | One knob: the fee cap, 3,000 to 6,000 tKAS. One hundred chains stay. The ready cap stays off. The rate stays 460 sompi per gram. No payment ladder. No second lane |
| Met or not met | **met** on the table and on the lane returning to zero. BASE 18:09–18:11Z: fee estimate 100 / 100 / 100, lane submit 0. HOLD: the lane log shows pending 100, 100, 100, 99, 100 and 100, and submit-OK 643, 566, 552, 645, 574 and 596. In the eighteen samples from 18:12:16Z through 18:18:01Z the template's heavy count is 1, template storage mass 266,676–295,231, our heavy class 84–99 at fee rate 460, and 756–3,025 other transactions sit in the 101–149 fee band. Ready mass in those samples is 54.24–78.48 blocks. The fee cap of 6,000 tKAS did not trip. Fees 4,388.53 tKAS. The 80-block pause did not trip. No sample has a template heavy count above 1, and every sample is under 400,000. RETURN fee estimate 100 / 100 / 100, pending 0 from 18:18. 3,576 submit-OK, 0 rejects |
| Retry count | 0. The next attempt is a new repo. This one is not resumed |
| Core tags | — |
| Status | done. Closed from the lane log and the probe |

Plan, lock, and the prediction are in [plan/PLAN.md](plan/PLAN.md), [locks/LOCKED.md](locks/LOCKED.md), and [plan/PREDICTIONS.md](plan/PREDICTIONS.md). Written before any submit.

While the lane is on, it slows other users' low-fee transactions on our node. We say so here.
