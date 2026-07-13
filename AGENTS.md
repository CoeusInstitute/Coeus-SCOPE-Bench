# AGENTS.md - Coeus SCOPE-Bench Public Results Repo

## Scope

This repository is the public-facing SCOPE-Bench publication and results surface for Coeus Institute.
It is separate from the private benchmark operations repository `CoeusInstitute/SCOPE-Benchmark`.

## Purpose

- Publish the public white paper and other public methodology documents.
- Publish structured public result data for completed SCOPE-Bench runs.
- Keep each completed public run under its own `data/<run-name>/` folder and update the root README when a newer package becomes current.
- Provide data analysts, researchers, and agents with stable files they can cite, inspect, and load.

## Boundary Rules

- Do not add private benchmark source code, scorer implementation, hidden verifier mechanics, private seeds, Supabase service-role keys, OpenRouter keys, raw private provider responses, or internal operations notes.
- Public data should be aggregate or score-ledger data intended for external analysis.
- Preserve run IDs, formula versions, model IDs, item IDs, pillar scores, failure categories, token/cost diagnostics, and timestamps needed for traceability.
- Do not publish answer keys, hidden ground truth, private item bodies, or private/generated official measurement sets unless the repository owner explicitly approves that storage model.

## Data Guidance

- Store each run under `data/<run-name-or-id>/`.
- Include a `README.md` for each run explaining source, formulas, files, and diagnostic fields.
- Treat `data/all-model-results.csv` and `data/all-model-results.json` as the canonical all-model datasets. Regenerate both from every published run-level `model-results.csv` whenever any model score is added or corrected.
- Keep one master row per `(run_id, model_id)`; never overwrite historical rows solely because a model ID appears in a newer run.
- Verify the master row count equals the sum of model rows across all published run packages.
- Prefer CSV for spreadsheet use and JSON for agents/programmatic loading.
- State clearly that `combo_score` is the official ranking metric and token/cost efficiency fields are diagnostics only.

## Public Artifact Guidance

- Store public papers under `docs/`.
- Keep file names stable and descriptive.
- If a paper is regenerated after new run data, update the matching structured data files in the same change.