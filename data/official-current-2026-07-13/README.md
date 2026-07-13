# official-current-2026-07-13 Results

Public structured data for the completed SCOPE-Bench `official-current-2026-07-13` run.

## Run Summary

| Field | Value |
|---|---:|
| Run ID | `c1ad6939-5850-4dbd-92d2-f707ec67c49c` |
| Status | `completed` |
| Models | 5 |
| Benchmark items per model | 21 |
| Saved responses | 105 |
| Pass rate | 68.6% |
| Official combo score | 85.081955 |
| Duration | 9m 11s |
| Item score formula | `scope-score-v0.8.2` |
| Aggregate formula | `scope-combo-v0.8.4` |

## Models

| Rank | Model | Combo | Soph. | Obj. | Corr. | Pass/Items |
|---:|---|---:|---:|---:|---:|---:|
| 1 | `openai/gpt-5.6-terra` | 86.805 | 77.43 | 86.60 | 96.39 | 15/21 |
| 2 | `x-ai/grok-4.5` | 86.294 | 78.82 | 83.67 | 96.39 | 15/21 |
| 3 | `openai/gpt-5.6-luna` | 84.195 | 79.31 | 81.66 | 91.62 | 14/21 |
| 4 | `openai/gpt-5.6-sol` | 84.186 | 74.72 | 81.45 | 96.39 | 14/21 |
| 5 | `anthropic/claude-sonnet-5` | 83.929 | 77.78 | 77.62 | 96.39 | 14/21 |

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
