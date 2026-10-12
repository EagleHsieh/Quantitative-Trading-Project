# Project Status

_Last updated: 2026-10-12_

## Done
- GitHub repository created (`EagleHsieh/Quantitative-Trading-Project`, branch `main`).
- Repository skeleton and handoff documents added (this pull request).

## In progress
- Confirming scope decisions listed as "Proposed" in `docs/DECISIONS.md`.
- Storage decision (partitioned Parquet + DuckDB) and merge-conflict rule documented in a follow-up pull request.

## Next
1. Confirm scope: asset universe, holding-period tiers, success metrics.
2. Choose and verify a data source (survivorship bias, split/dividend adjustment, point-in-time data).
3. Build the data layer (ingestion, cleaning, validation checks).
4. Build the backtest engine (costs, slippage, no look-ahead).
5. Build validation (out-of-sample, walk-forward, overfitting controls).
6. Build the first interactive visualization prototype.

## Blockers / open questions
- Intended use: personal trading, research/portfolio, or managing outside money (affects compliance planning).
- Data budget: free sources only, or paid data.
