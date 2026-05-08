# LEAP Data Release

This repository contains data tables supporting the LEAP / Perovskite-RL manuscript. It is a data release only: model weights, Hugging Face training datasets, raw PDFs, logs, procurement tables, and the full internally curated candidate pool are not included here.

## Contents

- `data/hot_start_additives.csv`: 36 experimentally characterized hot-start additives with hard molecular descriptors, soft mechanistic descriptor statistics, and relative PCE changes.
- `benchmark/questions.csv`: mechanism-consistency benchmark questions, answer options, ground-truth choices, source file names, and explanation/evidence notes.
- `benchmark/model_results/`: per-question results for Perovskite-RL and baseline models.
- `benchmark/statistics/`: accuracy summaries and McNemar-test tables.
- `ablation/representation/`: source data for hard/soft/hybrid representation ablations.
- `ablation/reasoning_source/`: source data for reasoning-source ablations.
- `ablation/decision_policy/`: source data for decision-policy ablations.

## Non-Released Data

The full candidate pool is not released because it contains internally curated commercially actionable candidates and procurement-related filtering information. To support reproducibility, this repository releases the hot-start additive dataset, mechanism-consistency benchmark, baseline result tables, and ablation source data.

## Benchmark Holdout Note

The benchmark source papers listed in `benchmark/benchmark_sources.csv` were held out from the Perovskite-RL SFT and GRPO training corpora. The `excluded_from_training` column records this status for each source file.

## License

License and citation metadata should be finalized when the manuscript is public.
