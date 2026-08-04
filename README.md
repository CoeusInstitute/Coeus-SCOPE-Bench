# SCOPE-Bench

**A deterministic benchmark for measuring how well language models reason at the right depth, recover the user's real objective, and distinguish meaningful relationships from misleading correlations.**

SCOPE-Bench is a Coeus Institute research benchmark for evaluating operational intelligence in large language models. It is designed to complement benchmarks centered on knowledge recall, coding, or mathematics by testing three capabilities that strongly affect whether a model is useful in real decisions:

1. **Sophistication** — Does the model use the right amount of reasoning for the problem, avoiding both shallow answers and unnecessary complexity?
2. **Objective Inference** — Can the model recover and serve the user's actual goal when the request is incomplete, indirect, or mis-specified?
3. **Correlation Reasoning** — Can the model identify genuine relationships, reject spurious ones, and reason across mixed qualitative, quantitative, and code-like evidence?

This repository is the public publication and results surface for SCOPE-Bench. It contains the public white paper, completed public-calibration result packages, and analysis-ready datasets. The private benchmark operations repository—containing the execution harness, hidden verifier mechanics, private seeds, and operational infrastructure—is intentionally separate.

## Start here

- **[Download the Excel workbook](data/SCOPE-Bench_All_Model_Scores.xlsx)** — organized scores, costs, filters, formatting, and run traceability for all 42 models
- **[Download the canonical CSV](data/all-model-results.csv)** — one row per published model result
- **[Download the canonical JSON](data/all-model-results.json)** — the same data for agents and applications
- **[Read the public white paper](docs/SCOPE-Bench_Public_White_Paper_Coeus_Institute.pdf)**
- **[Open the latest result package](data/official-current-2026-07-31/README.md)**

## How scoring works

Every model answers the same 21-item public calibration suite. Model outputs are scored by deterministic verifiers; a model never grades another model.

Each item receives a bounded `test_score`, and the item results are aggregated into three normalized pillar scores from 0 to 100. The official ranking value is:

```text
Combo score = (Sophistication + Objective Inference + Correlation) / 3
```

`combo_score` is the only capability-ranking metric presented below. Token use, latency, duration, cost, reliability, and relative efficiency remain available in the downloadable datasets as diagnostics, but they do not alter item scores, pillar scores, or Combo.

The public results use item formula `scope-score-v0.8.2` and aggregate formula `scope-combo-v0.8.4`. These are public calibration results, not the benchmark's private contamination-resistant official measurement set.

## All published model results

The table combines 42 unique models from four completed public calibration runs and sorts them by Combo score. Run IDs, timestamps, formula versions, and source-package paths remain in the canonical datasets for full provenance.

| Rank | Model | Combo score |
|---:|---|---:|
| 1 | `minimax/minimax-m3` | 93.412 |
| 2 | `moonshotai/kimi-k3` | 92.739 |
| 3 | `anthropic/claude-opus-5` | 89.348 |
| 4 | `anthropic/claude-opus-4.8` | 88.370 |
| 5 | `anthropic/claude-opus-4.7` | 87.768 |
| 6 | `qwen/qwen3.6-flash` | 87.165 |
| 7 | `openai/gpt-5.6-terra` | 86.805 |
| 8 | `google/gemini-3.1-flash-lite` | 86.801 |
| 9 | `openai/gpt-5.5` | 86.384 |
| 10 | `x-ai/grok-4.5` | 86.294 |
| 11 | `google/gemma-4-31b-it` | 84.944 |
| 12 | `google/gemini-3.5-flash` | 84.912 |
| 13 | `anthropic/claude-fable-5` | 84.669 |
| 14 | `openai/gpt-5.6-luna` | 84.195 |
| 15 | `openai/gpt-5.6-sol` | 84.186 |
| 16 | `anthropic/claude-sonnet-5` | 83.929 |
| 17 | `meta-llama/llama-4-maverick` | 83.876 |
| 18 | `openai/gpt-5.4-mini` | 83.286 |
| 19 | `x-ai/grok-build-0.1` | 83.022 |
| 20 | `deepseek/deepseek-v4-flash` | 82.880 |
| 21 | `openai/gpt-5.4-nano` | 82.430 |
| 22 | `qwen/qwen3.7-plus` | 82.349 |
| 23 | `openai/gpt-5.6-luna-pro` | 82.140 |
| 24 | `x-ai/grok-4.20-multi-agent` | 81.128 |
| 25 | `moonshotai/kimi-k2.7-code` | 80.943 |
| 26 | `nvidia/nemotron-3-ultra-550b-a55b` | 80.567 |
| 27 | `deepseek/deepseek-v4-pro` | 79.841 |
| 28 | `x-ai/grok-4.3` | 79.509 |
| 29 | `mistralai/mistral-small-2603` | 78.666 |
| 30 | `google/gemini-3.5-flash-lite` | 78.306 |
| 31 | `nvidia/nemotron-3-super-120b-a12b` | 76.843 |
| 32 | `google/gemini-3.6-flash` | 76.809 |
| 33 | `z-ai/glm-5.2` | 76.083 |
| 34 | `xiaomi/mimo-v2.5-pro` | 74.394 |
| 35 | `minimax/minimax-m2.7` | 74.008 |
| 36 | `tencent/hy3` | 72.414 |
| 37 | `meta-llama/llama-4-scout` | 70.083 |
| 38 | `openai/gpt-oss-120b` | 67.965 |
| 39 | `mistralai/mistral-medium-3-5` | 66.888 |
| 40 | `moonshotai/kimi-k2.6` | 64.077 |
| 41 | `tencent/hy3-preview` | 50.257 |
| 42 | `qwen/qwen3.7-max` | 43.442 |

## What is in the data

The canonical CSV, JSON, and Excel files merge every published run while preserving historical identity with `(run_id, model_id)`.

Each run also has a self-contained package under `data/<run-name>/`:

- `run-summary.json` — run identity, status, timing, formulas, coverage, and aggregate statistics
- `model-results.csv` / `.json` — model-level Combo, pillar, pass-rate, token, cost, and duration fields
- `item-scores.csv` / `.jsonl` — the public deterministic score ledger for every model × item pair
- `efficiency-rankings.csv` / `.json` — relative token and cost diagnostics
- `README.md` — a human-readable run summary

See [the master dataset documentation](data/MASTER_DATASET.md) for the row-identity and update contract.

## Published run packages

- [official-current-2026-07-31](data/official-current-2026-07-31/README.md) — 8 models
- [official-current-2026-07-13](data/official-current-2026-07-13/README.md) — 5 models
- [official-current-2026-07-02](data/official-current-2026-07-02/README.md) — 1 model
- [official-current-2026-06-30](data/official-current-2026-06-30/README.md) — 28 models

## Reproducibility and public-data boundary

Public artifacts retain the identifiers and formula metadata needed to trace every score back to a completed run. This repository intentionally excludes:

- raw provider responses and private operational traces;
- answer keys, hidden ground truth, verifier thresholds, and private seeds;
- private benchmark item bodies and contamination-resistant official measurement sets;
- service credentials, provider keys, and internal runner code.

This boundary keeps the public results useful for analysis without exposing material that would compromise benchmark integrity.

## About Coeus Institute

SCOPE-Bench is developed by [Coeus Institute](https://coeus.institute/) as part of its work on rigorous, decision-relevant evaluation of artificial intelligence.
