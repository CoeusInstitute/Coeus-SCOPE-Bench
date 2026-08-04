# Publication Notes

This repository publishes public SCOPE-Bench materials for external reference and analysis.

## What Is Public Here

- Public white paper PDF.
- Structured public result data for completed public calibration runs.
- Model-level, item-level, and efficiency diagnostic tables intended for analysts and agents.

## What Is Not Published Here

- Private benchmark harness code.
- Hidden verifier mechanics, answer keys, thresholds, private seeds, or private/generated official items.
- Raw provider responses or private operational traces.
- Supabase service-role keys, OpenRouter keys, or any provider credentials.

## Current Result Set

The current public data package is `data/official-current-2026-07-31/`, generated from the completed live SCOPE-Bench database run `76b10bcc-b876-48ae-9252-e9e19c0e4d87`.

That package covers eight models:

- `moonshotai/kimi-k3`
- `anthropic/claude-opus-5`
- `openai/gpt-5.4-nano`
- `openai/gpt-5.6-luna-pro`
- `google/gemini-3.5-flash-lite`
- `nvidia/nemotron-3-super-120b-a12b`
- `google/gemini-3.6-flash`
- `tencent/hy3`

The earlier five-model package remains available at `data/official-current-2026-07-13/`.
The earlier 28-model package remains available at `data/official-current-2026-06-30/`.

The July 2 Claude Fable 5 package is available at `data/official-current-2026-07-02/`.

## Canonical All-Model Dataset

Use `data/all-model-results.csv` as the single spreadsheet-friendly source for every published model result. The matching JSON file is `data/all-model-results.json`.

For human review, `data/SCOPE-Bench_All_Model_Scores.xlsx` presents the same 42-model collection with the four scores, estimated cost, filters, formatting, and run traceability.

Each master row is identified by `(run_id, model_id)`. The files must be regenerated whenever a run package or model score is added or corrected.

The official ranking metric is `combo_score`. Efficiency metrics are diagnostic and should not be treated as capability scores.