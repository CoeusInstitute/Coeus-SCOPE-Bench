# official-current-2026-07-31 Results

Public structured data for completed SCOPE-Bench run `official-current-2026-07-31`.

## Run Summary

| Field | Value |
|---|---:|
| Run ID | `76b10bcc-b876-48ae-9252-e9e19c0e4d87` |
| Status | `completed` |
| Models | 8 |
| Benchmark items per model | 21 |
| Saved responses | 168 |
| Pass rate | 65.5% |
| Official combo score | 81.378714 |
| Duration | 24m 15s |
| Item score formula | `scope-score-v0.8.2` |
| Aggregate formula | `scope-combo-v0.8.4` |

## Model Results

| Rank | Model | Combo | Soph. | Obj. | Corr. | Pass/Items |
|---:|---|---:|---:|---:|---:|---:|
| 1 | `moonshotai/kimi-k3` | 92.739 | 91.11 | 95.90 | 91.20 | 18/21 |
| 2 | `anthropic/claude-opus-5` | 89.348 | 88.19 | 86.05 | 93.80 | 16/21 |
| 3 | `openai/gpt-5.4-nano` | 82.430 | 66.11 | 86.60 | 94.58 | 13/21 |
| 4 | `openai/gpt-5.6-luna-pro` | 82.140 | 70.00 | 80.03 | 96.39 | 14/21 |
| 5 | `google/gemini-3.5-flash-lite` | 78.306 | 67.50 | 77.05 | 90.37 | 12/21 |
| 6 | `nvidia/nemotron-3-super-120b-a12b` | 76.843 | 54.38 | 81.66 | 94.50 | 12/21 |
| 7 | `google/gemini-3.6-flash` | 76.809 | 82.50 | 76.66 | 71.27 | 12/21 |
| 8 | `tencent/hy3` | 72.414 | 70.21 | 88.77 | 58.27 | 13/21 |

## Files

- `run-summary.json`
- `model-results.csv` / `model-results.json`
- `item-scores.csv` / `item-scores.jsonl`
- `efficiency-rankings.csv` / `efficiency-rankings.json`

## Public Data Boundary

This package excludes raw provider responses, hidden verifier details, answer keys, private seeds, private item bodies, service credentials, and internal runner/scoring implementation code.
