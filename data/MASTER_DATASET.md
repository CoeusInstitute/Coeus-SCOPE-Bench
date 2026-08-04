# Master Model Results Dataset

The canonical all-model download is:

- [`SCOPE-Bench_All_Model_Scores.xlsx`](SCOPE-Bench_All_Model_Scores.xlsx) — organized Excel workbook with all four scores, estimated cost, and run traceability
- [`all-model-results.csv`](all-model-results.csv) — spreadsheet/data-tool format
- [`all-model-results.json`](all-model-results.json) — agent/programmatic format

## Row Identity

Each row represents one `(run_id, model_id)` result. This preserves historical traceability when the same model is evaluated in more than one run instead of silently replacing an earlier result.

## Update Contract

Whenever a new public model score package is added:

1. Create or update `data/<run-name>/model-results.csv` and its matching run package.
2. Regenerate `data/all-model-results.csv` and `data/all-model-results.json` from every published run folder.
3. Verify the master row count equals the sum of rows in all run-level `model-results.csv` files.
4. Update the root README's current package and package index.

## Included Packages

- `official-current-2026-07-31` — 8 model rows
- `official-current-2026-06-30` — 28 model rows
- `official-current-2026-07-02` — 1 model row (`anthropic/claude-fable-5`)
- `official-current-2026-07-13` — 5 model rows

Current total: **42 model-result rows across 4 runs**.

## Important Interpretation

`combo_score` is the official model ranking metric within a run. Run metadata and formula-version columns must be used when comparing results across packages.

Token, cost, duration, and relative-efficiency fields are diagnostics and do not modify official scores.
