Dataset and output reference
============================

Documented dataset coverage
---------------------------

- Premier League, 2015/16.
- Barcelona in La Liga, 2015/16–2019/20.
- Barcelona in La Liga, 2008/09–2012/13.
- Bayer Leverkusen in the Bundesliga, 2023/24.
- FA Women's Super League, 2018/19–2020/21.
- Real Madrid players using 2015/16 La Liga events for an external
  comparison with the 2016 Ballon d'Or.

Reported measurements
---------------------

``95% rank interval``
   Interval summarizing bootstrap variation in estimated player rank.

``Pairwise support``
   Proportion of bootstrap comparisons in which one player outranks another.

``PCS``
   Pairwise Consensus Score used by the source analysis to construct the
   reliability-adjusted order.

``RAR``
   Reliability-Adjusted Rank derived from PCS ordering.

``Spearman correlation``
   Rank association measure used for reproducibility on independent samples.

The exact code-level PCS calculation is defined by the notebooks; readers
should rely on those implementations rather than on an invented formula.

Output organization
-------------------

``Results/premier_league/``, ``Results/barcelona/``,
``Results/leverkusen/``, ``Results/wsl/``, ``Results/ballon_dor/``
and ``Results/bootstrap_selection/`` organize the final artifacts.

StatsBomb Open Data remains the source of the match and event data.
