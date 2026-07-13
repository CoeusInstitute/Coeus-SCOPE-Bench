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

The current public data package is `data/official-current-2026-07-13/`, generated from the completed live SCOPE-Bench database run `c1ad6939-5850-4dbd-92d2-f707ec67c49c`.

That package covers five models:

- `openai/gpt-5.6-terra`
- `x-ai/grok-4.5`
- `openai/gpt-5.6-luna`
- `openai/gpt-5.6-sol`
- `anthropic/claude-sonnet-5`

The earlier 28-model package remains available at `data/official-current-2026-06-30/`.

The July 2 Claude Fable 5 package is available at `data/official-current-2026-07-02/`.

## Canonical All-Model Dataset

Use `data/all-model-results.csv` as the single spreadsheet-friendly source for every published model result. The matching JSON file is `data/all-model-results.json`.

Each master row is identified by `(run_id, model_id)`. The files must be regenerated whenever a run package or model score is added or corrected.

The official ranking metric is `combo_score`. Efficiency metrics are diagnostic and should not be treated as capability scores.