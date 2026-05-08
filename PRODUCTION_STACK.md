# Production Stack Reference

**Last updated:** 2026-05-08

## Component Catalogue

- **Prediction Engine Core**: `src/prediction/engine.py` (PredictionEngine composing components)
- **Team DNA**: `src/team_dna/` (v4 quantile embeddings, archetype clustering)
- **Player DNA**: `src/player_dna/` (in flight, kNN + GBT)
- **Context Engines**: `src/context_engines/` (P3 anomaly smoothing)
- **Bet Builder**: `src/bet_builder/` (tiered slip construction, compounding)
- **Data Pipeline**: `scripts/data_pull_sofascore.py` (Sofascore API ingestion)
- **Backtesting**: `scripts/bb_0_5_run_backtest.py` (blind walk-forward)
- **Feature Manifest**: `configs/feature_manifest.yaml`

## Entry Points

- Backtest: `python -m scripts.bb_0_5_run_backtest backtest --fast`
- Tests: `python -m pytest tests/bet_builder -q`

## Configs

- `bet_builder_config.yaml` (risk bands, thresholds per league)
- `configs/bet365_markets.yaml`

## Artefacts

- `artifacts/features.parquet`, `player_history.parquet`
- Model pickles in `artifacts/models/`

## Known Inconsistencies

- Initial setup phase; full V3 migration pending detailed planning.

**Read this first for any task.**