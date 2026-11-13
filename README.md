# MTTF and MTTR Settings for the Four LOLP Cases

The four experiments use Case 9 (load multiplier 0.9), Case 14 (1.0), Case 30 (0.8), and Case 39 (0.8). The modeled components are the generators in the MATPOWER `gen` table. `G1`, `G2`, etc. refer to row positions in that table, not bus numbers. Both MTTF and MTTR are measured in hours.

| Case | Number of generators | MTTF (G1 through Gn, h) | MTTR (G1 through Gn, h) |
| --- | ---: | --- | --- |
| Case 9 | 3 | 450, 450, 1960 | 50, 50, 40 |
| Case 14 | 5 | 450, 450, 1960, 1960, 450 | 50, 50, 40, 40, 50 |
| Case 30 | 6 | 450, 450, 1960, 1960, 450, 450 | 50, 50, 40, 40, 50, 50 |
| Case 39 | 10 | 450, 450, 1960, 1960, 450, 450, 1960, 1960, 1200, 1200 | 50, 50, 40, 40, 50, 50, 40, 40, 50, 50 |

All four cases use the same ordered parameter arrays, truncated to the first `n` entries for the case's `n` generators. The stationary unavailability used in the independent-generator outage model is

\[
q_m=\frac{\mathrm{MTTR}_m}{\mathrm{MTTF}_m+\mathrm{MTTR}_m}.
\]
