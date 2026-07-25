# Candidate-Selection Data

`top50_validation_shortlists_mechanism_scores.csv` contains the 50 released
validation-shortlist entries for each of the three experimental rounds (150
rows in total). The molecule identities and round-specific shortlist positions
are preserved from the manuscript release table.

## GP and EI Fields

The three GP fields were calculated for all 150 entries with one frozen LEAP GP
scoring snapshot and the corresponding candidate-feature snapshot. The hybrid
input contains deterministic molecular descriptors and Perovskite-RL soft
descriptors. The GP posterior mean and standard deviation were combined using
expected improvement with the following fixed settings:

- `y_best`: 0.0140540540540541 (80th percentile of the scoring snapshot's
  hot-start responses)
- `xi`: 0.05
- fitted kernel: constant-scaled Matern kernel (`nu = 1.5`) plus a white-noise
  kernel

`top50_rank` is the released round-specific validation-shortlist position. It
is retained independently of the unified release-snapshot rescoring reported
in the three GP fields.

## Column Definitions

| Column | Description |
|---|---|
| `round` | Experimental validation round (1-3). |
| `top50_rank` | Position in the released round-specific validation shortlist. |
| `name_en`, `cas`, `SMILES` | Molecule identifiers. |
| `predicted_mean_response` | GP posterior mean for the target response. |
| `predictive_uncertainty` | GP posterior predictive standard deviation. |
| `expected_improvement_score` | Expected-improvement acquisition score. |
| `binding_mode_score` | Mean Perovskite-RL binding-mode descriptor score. |
| `interfacial_shielding_score` | Mean interfacial-shielding descriptor score. |
| `hydrophobic_protection_score` | Mean hydrophobic-protection descriptor score. |
| `ion_interaction_score` | Mean ion-interaction descriptor score. |
| `electronic_modulation_score` | Mean electronic-modulation descriptor score. |
| `predicted_effect_score` | Mean overall predicted-effect score. |
| `experimental_validation_status` | Whether the entry was tested experimentally. |
| `tested_additive` | Manuscript abbreviation for a tested entry; blank otherwise. |
| `expert_review_boundary` | General feasibility criteria used during expert review. |
| `expert_review_outcome` | Whether the entry advanced to device validation. |

The three experimentally tested entries are Boc-DCPy (round 1, shortlist
position 25), 6-CDQ (round 2, position 1), and 2-CNA (round 3, position 10).
