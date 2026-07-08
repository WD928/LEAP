# Human Baseline

This folder contains anonymized closed-book human-expert scoring tables for the mechanism-consistency benchmark.

The evaluators were human experts with perovskite research experience who were not involved in benchmark question generation or answer-key assignment. They answered the same 32 multiple-choice questions without access to model outputs, answer keys, web search, or the source papers. Responses were scored using the fixed benchmark answer key.

Files:

- `human_expert_responses.csv`: one row per benchmark question, with each human expert's answer, correctness label, and the three-expert majority vote.
- `human_baseline_scored_answers.csv`: per-question human answers and correctness labels for each anonymized evaluator.
- `human_baseline_summary.csv`: per-evaluator accuracy summary.
- `human_baseline_group_summary.csv`: group-level mean and standard deviation across the three human evaluators.
