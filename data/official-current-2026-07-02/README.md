# official-current-2026-07-02 Results

Public structured data for the completed SCOPE-Bench `official-current-2026-07-02` Claude Fable 5 run.

## Run Summary

| Field | Value |
|---|---:|
| Run ID | `d2446122-f670-47d1-82fa-890b875c5cc5` |
| Status | `completed` |
| Model | `anthropic/claude-fable-5` |
| Benchmark items | 21 |
| Saved responses | 21 |
| Pass rate | 57.1% |
| Official combo score | 84.669465 |
| Duration | 5m 31s |
| Item score formula | `scope-score-v0.8.2` |
| Aggregate formula | `scope-combo-v0.8.4` |

## Model Result

| Model | Combo | Soph. | Obj. | Corr. | Pass/Items |
|---|---:|---:|---:|---:|---:|
| `anthropic/claude-fable-5` | 84.669 | 82.43 | 84.07 | 87.51 | 12/21 |

## Files

| File | Purpose |
|---|---|
| `run-summary.json` | Run-level metadata, aggregate summary, formula versions, totals, and source-table notes. |
| `model-results.csv` | Spreadsheet-friendly model result and diagnostics. |
| `model-results.json` | JSON form of the model result. |
| `item-scores.csv` | Public item-level score ledger. |
| `item-scores.jsonl` | JSON Lines form of the item-level score ledger. |
| `efficiency-rankings.csv` | Spreadsheet-friendly relative efficiency diagnostics. |
| `efficiency-rankings.json` | JSON form of relative efficiency diagnostics. |
| `data-dictionary.md` | Field definitions and interpretation notes. |

## Scoring Interpretation

`combo_score` is the official ranking metric. Token use, duration, latency, cost, reliability, SCOPE Base, and efficiency fields are diagnostics only and do not modify official scores.

## Public Data Boundary

This folder excludes raw provider responses, hidden verifier details, answer keys, private seeds, private item bodies, service credentials, and internal runner/scoring implementation code.
