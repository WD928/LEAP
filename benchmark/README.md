# Mechanism-Consistency Benchmark

`questions.csv` contains 32 multiple-choice mechanism-consistency questions. `model_results/` contains per-question model answers, and `statistics/` contains aggregate accuracy and exact McNemar-test tables. `mcnemar_vs_reference_holm.csv` reports Holm-Bonferroni-adjusted pairwise comparisons against Perovskite-RL.

The source papers in `benchmark_sources.csv` were excluded from the SFT and GRPO training corpora.
