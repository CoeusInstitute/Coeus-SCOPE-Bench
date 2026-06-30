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

- [official-current-2026-06-30](data/official-current-2026-06-30/README.md)

Key files:

- [Run summary JSON](data/official-current-2026-06-30/run-summary.json)
- [Model results CSV](data/official-current-2026-06-30/model-results.csv)
- [Model results JSON](data/official-current-2026-06-30/model-results.json)
- [Item scores CSV](data/official-current-2026-06-30/item-scores.csv)
- [Item scores JSONL](data/official-current-2026-06-30/item-scores.jsonl)
- [Efficiency rankings CSV](data/official-current-2026-06-30/efficiency-rankings.csv)
- [Efficiency rankings JSON](data/official-current-2026-06-30/efficiency-rankings.json)
- [Data dictionary](data/official-current-2026-06-30/data-dictionary.md)

## Scoring Note

The official ranking value is `combo_score`, a bounded 0-100 score computed as the arithmetic mean of normalized Sophistication, Objective Inference, and Correlation pillar scores.

Token use, duration, latency, cost, reliability, SCOPE Base, and relative efficiency fields are diagnostic. They do not modify official item scores, pillar scores, or `combo_score`.
