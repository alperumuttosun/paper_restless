# Replication code

R code that reproduces all results, tables and figures.

## Data

ReSTLess Open Database, version 2 (France and United Kingdom), Zenodo: https://doi.org/10.5281/zenodo.21993591.
The script downloads the data in step00 (version 1 is also downloaded for comparison).

## Requirements

R with the packages `jsonlite`, `curl`, `data.table`, `haven`, `readxl`, `xml2`, `poLCA` (installed automatically if missing; `ggplot2` is used for figures if available).

## Use

Run `paper_restless_step00-13.R` from top to bottom. Each step is skipped if its output files already exist, so the script can be resumed after an interruption.

## Code flow and outputs

| Step | Content | Outputs |
|---|---|---|
| step00 | Download of the data from Zenodo | `v2_*`, `v1_*` |
| step01 | Data audit | `audit_*.csv` |
| step02 | Merged vs conditional coding; one-dimensional latent class models | `step02_*.csv` |
| step03 | Robustness of one-dimensional models | `step03_*.csv` |
| step04 | Two-dimensional latent class model; first Monte Carlo | `step04_*.csv` |
| step05 | Model scan, bootstrap, subgroups | `step05_*.csv` |
| step06 | Gradient under two group definitions; tables | `step06_*.csv`, `table*.csv` |
| step07 | Occupation, larger models, item deletion, Monte Carlo S5–S9 | `step07_*.csv` |
| step09 | Measurement assumption, random starts, threshold c = 4, Monte Carlo S10–S12 | `step09_*.csv` |
| step10 | Model selection, model-free measure, simulation S13 | `step10_*.csv` |
| step11 | Selected 6 × 5 model: profiles, bootstrap, subgroups, sensitivity, S13 | `step11_*.csv` |
| step12 | Agreement (ARI) of one-dimensional typologies | `step12_*.csv` |
| step13 | Partial measurement invariance | `step13_*.csv` |
| figures | Figures (1600 dpi PNG and PDF) | `fig1_*`, `fig2_*`, `fig3_*` |

Figure files: `fig2_need_by_compensation` = Figure 1, `fig3_gradient_across_models` = Figure 2, `fig1_montecarlo_bias` = Figure 3.
