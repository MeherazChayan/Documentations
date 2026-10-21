Reproduce the notebook analyses
===============================

Data source
-----------

The notebooks obtain `StatsBomb Open Data <https://github.com/statsbomb/open-data>`_
directly rather than redistributing raw event files inside the project.

Notebook workflow
-----------------

The original README documents Kaggle as the intended execution environment.
For each notebook:

1. Open the selected notebook in Kaggle.
2. Enable Internet access for the notebook session.
3. Run cells from top to bottom.
4. Allow the notebook to retrieve its required StatsBomb data.
5. Inspect generated tables, graphics and summaries under ``/kaggle/working/``.

The notebooks use fixed random seeds and pinned package versions according to
the project README. The analyses were not executed again for this collection.

Notebook selection
------------------

``01_premier_league_rar_stress_test.ipynb``
   Premier League 2015/16 cohort stress test.

``02_barcelona_stability_and_rar.ipynb``
   Two Barcelona historical periods and ranking stability.

``03_bayer_leverkusen_rar.ipynb``
   Bayer Leverkusen 2023/24.

``04_wsl_longitudinal_rar.ipynb``
   Three-season Women's Super League analysis.

``05_real_madrid_ballondor_external_check.ipynb``
   Comparison with six Real Madrid players in the 2016 Ballon d'Or ranking.

``06_bootstrap_size_selection.ipynb``
   Bootstrap sample-count precision justification.

The ``Results/`` directory holds final study tables and graphics; it does not
contain all exploratory runs.
