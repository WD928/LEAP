# LEAP Data Release

<p align="center">
  <img src="https://img.shields.io/badge/project-LEAP%20%2F%20Perovskite--RL-2f6f9f" alt="Project">
  <img src="https://img.shields.io/badge/release-data%20tables-4b8bbe" alt="Data release">
  <img src="https://img.shields.io/badge/domain-perovskite%20photovoltaics-6a994e" alt="Domain">
  <img src="https://img.shields.io/badge/status-manuscript%20support-lightgrey" alt="Status">
</p>

This repository contains data tables supporting the LEAP / Perovskite-RL manuscript. It is a data-release repository: model weights, Hugging Face training datasets, raw PDFs, logs, procurement tables, and the full internally curated candidate pool are not stored here.

## Resource Links

| Resource | Link | Notes |
|---|---|---|
| Model weights | [JH976/Perovskite-RL](https://huggingface.co/JH976/Perovskite-RL) | Perovskite-RL model repository. Update this link if the public model repository uses a different name. |
| Training datasets | [datasets/JH976/Perovskite-RL](https://huggingface.co/datasets/JH976/Perovskite-RL) | SFT and GRPO datasets for the language-model training stages. |
| Data-release repository | [WD928/LEAP](https://github.com/WD928/LEAP) | Tables and source data used for benchmark, ablation, and candidate-selection reporting. |

## Repository Map

| Module | Path | Contents |
|---|---|---|
| Hot-start additive data | `data/` | 36 experimentally characterized additives, hard descriptors, soft mechanistic descriptor statistics, and relative PCE changes. |
| Mechanism benchmark | `benchmark/questions.csv` | 32 multiple-choice questions from held-out literature sources. |
| Model benchmark results | `benchmark/model_results/` | Per-question answers for Perovskite-RL and baseline models. |
| Benchmark statistics | `benchmark/statistics/` | Accuracy summaries, exact McNemar-test tables, and Holm-Bonferroni-adjusted pairwise comparisons. |
| Representation ablation | `ablation/representation/` | Hard/soft/hybrid representation ablation source data and bootstrap confidence intervals for Figure 3 metrics. |
| Reasoning-source ablation | `ablation/reasoning_source/` | Perovskite-RL versus backbone soft-descriptor ablation tables and top-k diagnostics. |
| Decision-policy ablation | `ablation/decision_policy/` | Expected-improvement, predicted-mean, uncertainty, and random-policy comparison data. |
| Candidate selection | `candidate_selection/` | Round-specific top-50 validation shortlists with molecule identifiers and mechanism-score summaries. |

## Key Files

| File | Description |
|---|---|
| `data/hot_start_additives.csv` | Main 36-additive hot-start table with measured PCE values and descriptors. |
| `benchmark/statistics/model_summary_with_ci.csv` | Benchmark accuracy summary with confidence intervals. |
| `benchmark/statistics/mcnemar_vs_reference_holm.csv` | Exact McNemar comparisons against Perovskite-RL with Holm-Bonferroni adjustment. |
| `ablation/representation/figure3_bootstrap_ci_table.csv` | Bootstrap confidence intervals for the Figure 3 representation-ablation metrics. |
| `candidate_selection/top50_validation_shortlists_mechanism_scores.csv` | Cleaned round-specific top-50 validation shortlist table. |

## License

This repository is released under the Apache License 2.0. See the `LICENSE` file for details.

## Citation

If you use this repository, please cite the associated arXiv preprint:

```bibtex
@misc{wang2026leap,
  title         = {LEAP: A Closed-Loop Framework for Perovskite Precursor Additive Discovery},
  author        = {Wang, Xin-De and Chen, Zhi-Rui and Gao, Ze-Feng and Guo, Peng-Jie and Mu, Cheng and Lu, Zhong-Yi},
  year          = {2026},
  eprint        = {2605.20242},
  archivePrefix = {arXiv},
  url           = {https://arxiv.org/abs/2605.20242}
}
