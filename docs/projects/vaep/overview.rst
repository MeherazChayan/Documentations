Method and interpretation
=========================

ReliableVAEP does not replace the underlying VAEP value model. It examines
how strongly the available match sample supports the resulting player order.
It works with VAEP per 90 minutes and repeatedly resamples each player's
matches with replacement.

Four outputs are highlighted by the source repository:

- Bootstrap rank uncertainty, expressed using rank intervals.
- Pairwise support, expressing how frequently one player ranks above another.
- Pairwise Consensus Score (PCS), aggregated from pairwise comparisons.
- Reliability-Adjusted Rank (RAR), the ranking obtained by sorting PCS.

The project's reported final experiments use **3,500 bootstrap draws**. The
repository explains that this count was selected to support an approximately
0.01 Monte Carlo margin at the 0.90 pairwise threshold.

Reproducibility is evaluated on independent, non-overlapping match samples
using Spearman rank correlation. The declared stability criterion requires a
median correlation of at least 0.80 across three consecutive tested sample
sizes. These are research-defined criteria, not universal football ranking
standards.

Interpretation
--------------

The repository reports different stable match thresholds for two Barcelona
periods (44 and 27 matches per player), indicating that a single match-count
rule is inappropriate. The Premier League 2015/16 stress test includes 423
players. The repository reports improvements from RAR in 77.2% of 600
independent comparisons, with a small pooled median Spearman increase.

These are reported outcomes of the source analyses, not independently
reproduced findings of this documentation build.

Source: `ReliableVAEP README <https://github.com/MeherazChayan/ReliableVAEP#readme>`_.
