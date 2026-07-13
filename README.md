# Coeus SCOPE-Bench

Public white paper and structured result data for SCOPE-Bench, a Coeus Institute benchmark for evaluating operational intelligence in large language models.

SCOPE-Bench focuses on three under-measured capabilities:

- **Sophistication** - calibrated reasoning depth and cognitive economy.
- **Objective Inference** - recovering and serving the user's real objective from incomplete or mis-specified requests.
- **Correlation Reasoning** - finding true relationships and rejecting false relationships across heterogeneous evidence.

## Repository Boundary

This is the public-facing publication and results repository. It is intentionally separate from the private benchmark operations repository, which contains the harness, scoring implementation, operational pipeline, and private methodology assets.

This repository is for:

- public white papers and explanatory docs;
- structured public benchmark result data;
- stable references for analysts, researchers, and agents.

It does not contain hidden verifier mechanics, private seeds, service credentials, internal runner code, or private benchmark source material.

## White Paper

- [SCOPE-Bench Public White Paper](docs/SCOPE-Bench_Public_White_Paper_Coeus_Institute.pdf)

## Current Public Result Data

The current published result set is:

- [official-current-2026-07-13](data/official-current-2026-07-13/README.md)

### Canonical all-model dataset

- [Download all published model results as CSV](data/all-model-results.csv)
- [Download all published model results as JSON](data/all-model-results.json)
- [Master dataset documentation](data/MASTER_DATASET.md)

The master dataset is regenerated whenever new public model scores are added. Each row represents one `(run_id, model_id)` result so historical evaluations remain traceable.

Key files:

- [Run summary JSON](data/official-current-2026-07-13/run-summary.json)
- [Model results CSV](data/official-current-2026-07-13/model-results.csv)
- [Model results JSON](data/official-current-2026-07-13/model-results.json)
- [Item scores CSV](data/official-current-2026-07-13/item-scores.csv)
- [Item scores JSONL](data/official-current-2026-07-13/item-scores.jsonl)
- [Efficiency rankings CSV](data/official-current-2026-07-13/efficiency-rankings.csv)
- [Efficiency rankings JSON](data/official-current-2026-07-13/efficiency-rankings.json)
- [Data dictionary](data/official-current-2026-07-13/data-dictionary.md)

### Models in the current package

| Rank | Model | Combo |
|---:|---|---:|
| 1 | `openai/gpt-5.6-terra` | 86.805 |
| 2 | `x-ai/grok-4.5` | 86.294 |
| 3 | `openai/gpt-5.6-luna` | 84.195 |
| 4 | `openai/gpt-5.6-sol` | 84.186 |
| 5 | `anthropic/claude-sonnet-5` | 83.929 |

### Earlier public packages

- [official-current-2026-07-02](data/official-current-2026-07-02/README.md) — Claude Fable 5 public calibration package
- [official-current-2026-06-30](data/official-current-2026-06-30/README.md) — 28-model public calibration package

## Scoring Note

The official ranking value is `combo_score`, a bounded 0-100 score computed as the arithmetic mean of normalized Sophistication, Objective Inference, and Correlation pillar scores.

Token use, duration, latency, cost, reliability, SCOPE Base, and relative efficiency fields are diagnostic. They do not modify official item scores, pillar scores, or `combo_score`.
