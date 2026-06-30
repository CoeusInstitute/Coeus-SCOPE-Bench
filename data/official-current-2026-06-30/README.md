# official-current-2026-06-30 Results

Public structured data for the completed SCOPE-Bench `official-current-2026-06-30` run.

## Run Summary

| Field | Value |
|---|---:|
| Run ID | `9ff7a720-826a-4d34-9fbf-ca21b7a70b39` |
| Status | `completed` |
| Models | 28 |
| Benchmark items per model | 21 |
| Saved responses | 588 |
| Pass rate | 62.4% |
| Official combo score | 77.965071 |
| Duration | 93m 8s |
| Item score formula | `scope-score-v0.8.2` |
| Aggregate formula | `scope-combo-v0.8.4` |

## Files

| File | Purpose |
|---|---|
| `run-summary.json` | Run-level metadata, aggregate summary, formula versions, totals, and source-table notes. |
| `model-results.csv` | Spreadsheet-friendly model ranking and model-level diagnostic fields. |
| `model-results.json` | JSON form of the model ranking data. |
| `item-scores.csv` | Public item-level score ledger for each model x item pair. |
| `item-scores.jsonl` | JSON Lines form of the public item-level score ledger. |
| `efficiency-rankings.csv` | Spreadsheet-friendly relative token/cost efficiency rankings. |
| `efficiency-rankings.json` | JSON form of relative token/cost efficiency rankings. |
| `data-dictionary.md` | Field definitions and interpretation notes. |

## Scoring Interpretation

`combo_score` is the official ranking metric. It is a bounded 0-100 arithmetic mean of normalized Sophistication, Objective Inference, and Correlation pillar scores.

Token use, duration, latency, cost, reliability, SCOPE Base, and relative efficiency fields are diagnostics only. They do not modify official item scores, pillar scores, or `combo_score`.

Relative token/cost efficiency scores are normalized within this selected run. A value of `100` means best-in-run score-per-token or score-per-dollar, not perfect benchmark quality.

## Public Data Boundary

This folder intentionally excludes raw provider responses, hidden verifier details, answer keys, private seeds, private item bodies, service credentials, and internal runner/scoring implementation code.