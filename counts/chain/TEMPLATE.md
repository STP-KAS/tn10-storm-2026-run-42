> **Experimental. We are just trying this.** [Disclaimer](../../DISCLAIMER.md) · Kaspa Testnet-10 only. tKAS has no value. Counts only.

# Template, pre-run 42

The desk probe, every 20 s, on our own desk node. A cell is the median of that minute's samples. An odd count takes the middle sample. An even count takes the average of the two middle samples. Template storage mass is the mass the template's transactions carry. "Under 400k" is how many of those samples had template storage mass under 400,000. The lane log is a different clock: its pending count is the lane's own in-flight count at the minute line. "Our heavy" is the probe's class for ids this lane had already written, at fee rate 460.

The lane was off in BASE (18:09–18:11Z) and RETURN (18:18–18:20Z). HOLD on the clock was 18:12–18:17Z, one hundred chains, no ready cap, rate 460, fee cap 6,000 tKAS. The fee cap did not stop the sends. The six minutes completed. The 18:15 row has two samples, so that cell is the average of the two.

| Minute (UTC) | Step | Samples | Mempool | Ready count | Ready mass, blocks of 500k | Template txs | Template storage mass | Samples under 400k | Fee estimate priority / normal / low | Our heavy in mempool | Lane pending | Lane submit-OK |
|---|---|---:|---:|---:|---:|---:|---:|---:|---|---:|---:|---:|
| 2026-11-14T18:09 | BASE | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T18:10 | BASE | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T18:11 | BASE | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T18:12 | HOLD | 3 | 1,477 | 1,476 | 54.59 | 3 | 266,684 | 3 of 3 | 760.76 / 193.21 / 115.14 | 92 | 100 | 643 |
| 2026-11-14T18:13 | HOLD | 3 | 2,837 | 2,836 | 66.62 | 4 | 266,718 | 3 of 3 | 833.23 / 193.99 / 115.19 | 91 | 100 | 566 |
| 2026-11-14T18:14 | HOLD | 3 | 3,429 | 3,428 | 73.08 | 6 | 266,716 | 3 of 3 | 864.94 / 194.27 / 115.21 | 96 | 100 | 552 |
| 2026-11-14T18:15 | HOLD | 2 | 3,322 | 3,321 | 72.58 | 7.5 | 270,837 | 2 of 2 | 856.47 / 194.20 / 115.21 | 90 | 99 | 645 |
| 2026-11-14T18:16 | HOLD | 3 | 3,493 | 3,492 | 77.84 | 3 | 266,685 | 3 of 3 | 888.08 / 194.46 / 115.23 | 96 | 100 | 574 |
| 2026-11-14T18:17 | HOLD | 3 | 3,503 | 3,502 | 77.38 | 5 | 269,423 | 3 of 3 | 886.66 / 194.45 / 115.23 | 93 | 100 | 596 |
| 2026-11-14T18:18 | RETURN | 3 | 2 | 2 | 0.70 | 2 | 270,252 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T18:19 | RETURN | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | 0 | 0 |
| 2026-11-14T18:20 | RETURN | 3 | 0 | 0 | 0 | 0 | 0 | 3 of 3 | 100 / 100 / 100 | 0 | — | — |

The 18:15 priority fee, 856.47, is the average of 844.04 and 868.89, rounded to the cent. Normal 194.20 is the average of 194.09 and 194.31. Low 115.21 is the average of 115.2 and 115.22.

The 18:17 median hides the high sample. At 18:17:00Z the mempool size is 3,499, the ready count is 3,498, ready mass is 78.48 blocks, the template has 7 transactions and storage mass 295,231, the template's heavy count is 1 and that one is classed as ours, our heavy class is 97, the 101–149 band holds 2,858, and the priority fee estimate is 890.43. The other two samples of that minute are lower, so the median storage mass is 269,423 and the median ready mass is 77.38. 295,231 is still one heavy transaction of our shape plus other template mass. It is not two of our shape.

The 18:18 median is a trap if it is read alone. The sample at 18:18:01Z, one second after RETURN was written, still has our class: mempool size 3,633, ready count 3,632, ready mass 72.60 blocks, template storage mass 270,252, template heavy count 1 classed as ours, our heavy class 84, 3,025 other transactions in the 101–149 band, priority fee 876.39. The sample at 18:18:22Z has our class gone: size 2, ready count 2, ready mass 0.70, template storage mass 342,997, template heavy count 1 classed other, fee estimate 100. The sample at 18:18:42Z is empty, fee estimate 100. The minute median takes the middle of those three. It is not our lane still filling the template, and the minute is not empty. The lane submitted 0 in that minute.

Across the eighteen samples from 18:12:16Z through 18:18:01Z, while our heavy class was present, template storage mass runs from 266,676 to 295,231. All eighteen are under 400,000. The template's heavy count is 1 in each, and that one template transaction is classed as ours. Our heavy class in those samples is 84 to 99 transactions, all ready, fee rate 460 on the class. The probe did not see exactly 100. The same eighteen samples hold 756 to 3,025 other transactions in the 101–149 fee band, and in these samples that band's ready count equals its count. Mempool size in those samples is 867 to 3,633. Ready mass in those samples runs from 54.24 to 78.48 blocks. The highest is 78.48, at 18:17:00Z, which is under 80. Later samples in that present set are 77.38, 75.30 and 72.60. In these samples the ready count is one below the mempool size field. We report both as the probe wrote them.

No sample in this run has a template heavy count above 1. No sample has template storage mass at or above 400,000. The highest template storage mass in the run is 342,997, at 18:18:22Z, and that one is classed other.

The lane's own minute lines say pending 100, 100, 100, 99, 100 and 100, and submit-OK 643, 566, 552, 645, 574 and 596. One hundred chains were available, the ready cap was off, and pending on five of those six lines is 100. The 18:15 row stamps pending 99 on the first tick of 18:16, and that minute has 645 submits. The submit count is the minute. The 18:20 lane minute was not flushed. The probe covers it, and the end line says pending 0.

The lane's end line at 18:21:00Z: 3,576 submit-OK, 0 rejects, 0 lost, fees 4,388.53 tKAS, parked 134.10 tKAS, 179 coins taken, pending 0. Node rate on the lane's own HOLD entries, and on the 18:18 line, was 460. Storage mass did not drift. The second lane submitted 0. The lane's pause lines stay 0. There is no fee-cap line.

BASE was not an empty mempool. At 18:09:12Z the mempool size is 7, the ready count is 7, ready mass is 0.03 blocks, the template has 7 transactions and storage mass 7,277, heavy count 0, and 7 other transactions sit in the 101–149 band. The fee estimate is 100 / 100 / 100, and the lane submitted 0. The other two 18:09 samples are empty, so the median is 0. 18:10 is empty in all three samples. At 18:11:36Z one sample has mempool size 1, ready count 1, template storage mass 20,671, heavy count 0, classed other. The other two 18:11 samples are empty, so the median mass is 0. The fee estimate is 100 / 100 / 100.

RETURN is a fee estimate of 100 / 100 / 100 and pending 0 on the lane. 18:19 is empty in all three samples. The 18:20 median is empty, and it hides one sample. At 18:20:24Z the mempool size field is 0, the ready count is 9, ready mass is 0.04 blocks, the template has 9 transactions and storage mass 0, and 9 other transactions sit in the 101–149 band. The fee estimate is 100. Our heavy class is 0.
