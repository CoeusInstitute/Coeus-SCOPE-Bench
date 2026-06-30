# Data Dictionary

Field definitions for the `official-current-2026-06-30` public result files.

## Ranking And Score Fields

| Field | Definition |
|---|---|
| `combo_score` | Official 0-100 model ranking score for the run. It is the arithmetic mean of normalized pillar scores. |
| `sophistication_score` | 0-100 pillar score for calibrated reasoning depth and cognitive economy. |
| `objective_inference_score` | 0-100 pillar score for recovering and serving the user's real objective. |
| `correlation_score` | 0-100 pillar score for finding true relationships and rejecting false relationships across evidence. |
| `test_score` | Public item-level score on a 0-100 scale. |
| `passed` | Strict deterministic pass/fail result for the item. A failed item may still receive partial `test_score` credit. |
| `failure_category` | Stable public failure category such as `incorrect` or `provider_error`. |

## Run And Model Fields

| Field | Definition |
|---|---|
| `run_id` | Supabase benchmark run identifier. |
| `run_name` | Human-readable run name. |
| `model_id` | Provider/model identifier. |
| `provider` | Provider segment of `model_id`. |
| `model` | Model segment of `model_id`. |
| `item_count` | Intended scored item count for a model. |
| `invocation_count` | Saved response count represented in the model projection. |
| `pass_count` | Number of strict item passes. |
| `failure_count` | Number of non-passing item rows. |
| `pass_rate` | `pass_count / item_count`. |

## Token, Cost, And Duration Diagnostics

| Field | Definition |
|---|---|
| `total_scored_tokens` | Scorer-owned token total used for diagnostic efficiency calculations. |
| `total_tokens` | Provider total token count where available. |
| `total_estimated_cost_usd` | Estimated provider cost for the model in this run. |
| `total_duration_ms` | Total persisted model invocation duration in milliseconds. |
| `scored_tokens` | Item-level scored-token diagnostic. |
| `token_efficiency` | Item-level diagnostic ratio from token budget to scored tokens. It does not modify official score. |
| `estimated_cost_usd` | Item-level estimated cost where available. |
| `duration_ms` | Item-level invocation duration. |

## Relative Efficiency Fields

| Field | Definition |
|---|---|
| `ranking_type` | `token` or `cost`. |
| `relative_efficiency_score` | 0-100 value normalized to the best model in this run for the selected efficiency type. |
| `scope_efficiency_index` | `combo_score` per 1k scored tokens. Present for token-efficiency rows. |
| `cost_adjusted_scope_score` | `combo_score` per estimated US dollar. Present for cost-efficiency rows. |
| `scored_tokens_per_1k` | Scored tokens divided by 1,000. |
| `estimated_run_cost_usd` | Estimated model run cost used for cost efficiency. |

## Public Safety Notes

The public export includes enough information for reproducible result analysis, but it intentionally excludes raw model responses, answer keys, hidden verifier rules, private item seeds, and source code for the private scorer/harness.