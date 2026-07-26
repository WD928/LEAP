# Candidate-Selection Data

`top50_validation_shortlists_mechanism_scores.csv` contains the 50 released
validation-shortlist entries for each of the three experimental rounds (150
rows in total). The molecule identities and round-specific shortlist positions
are the actual round-specific records used in the manuscript. The tested
additives occupy shortlist positions 25, 1, and 10 in rounds 1, 2, and 3,
respectively.

## Column Definitions

| Column | Description |
|---|---|
| `round` | Experimental validation round (1-3). |
| `top50_rank` | Actual position in the released round-specific validation shortlist. |
| `name_en`, `cas`, `SMILES` | Molecule identifiers. |
| `binding_mode_score` | Mean Perovskite-RL binding-mode descriptor score. |
| `interfacial_shielding_score` | Mean interfacial-shielding descriptor score. |
| `hydrophobic_protection_score` | Mean hydrophobic-protection descriptor score. |
| `ion_interaction_score` | Mean ion-interaction descriptor score. |
| `electronic_modulation_score` | Mean electronic-modulation descriptor score. |
| `predicted_effect_score` | Mean overall predicted-effect score. |
| `experimental_validation_status` | Whether the entry was tested experimentally. |
| `tested_additive` | Manuscript abbreviation for a tested entry; blank otherwise. |
| `expert_review_boundary` | General study-level feasibility criteria; this is not a molecule-specific rejection record. |
| `experimental_advancement_status` | Whether the entry advanced in this campaign; `not_advanced_in_this_campaign` does not mean that the molecule was individually reviewed and rejected. |

The three experimentally tested entries are Boc-DCPy (round 1, shortlist
position 25), 6-CDQ (round 2, position 1), and 2-CNA (round 3, position 10).
