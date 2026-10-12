# References

Rule: only list sources that were actually opened and checked. Unverified items go in the second section until verified. Access date for all items below: 2026-10-12.

## Verified (opened and read)
| Topic | Source | What it supports |
|---|---|---|
| Long-term vs short-term holding period | IRS Topic 409, https://www.irs.gov/taxtopics/tc409 | Held more than one year = long-term; one year or less = short-term |
| Pattern day trader (PDT) rule change | King & Spalding, https://www.kslaw.com/insights/articles/finra-adopts-sweeping-changes-to-margin-requirements-for-day-trading ; E*TRADE, https://us.etrade.com/knowledge/library/margin/pattern-day-trading-rule-change | FINRA Rule 4210 amended; PDT designation and $25,000 minimum replaced by an intraday margin model; $2,000 minimum margin equity remains |
| Hedge fund exemptions (US) | Proskauer via National Law Review, https://natlawreview.com/article/hedge-start-what-key-exemptions-apply-hedge-funds | Reg D private placements; accredited investor and qualified purchaser concepts; Investment Company Act 3(c)(7) |
| GS Quant | https://github.com/goldmansachs/gs-quant | Python toolkit for quantitative finance by Goldman Sachs quants; API access requires institutional client credentials |
| Perspective | https://github.com/finos/perspective/blob/asan-expr/README.md | Interactive visualization component for large and streaming data; originally developed at J.P. Morgan; open-sourced via FINOS |
| Capitalize Analytics | https://capitalizeconsulting.com/ | Data/analytics/AI consulting firm; lists partners including Alteryx, UiPath, Workday Adaptive Planning, Databricks, Power BI, Snowflake, Tableau |
| Claude Code | https://code.claude.com/docs/en/quickstart.md | Coding tool that works with git; supports terminal, IDE, desktop, and web |
| DuckDB memory and larger-than-memory processing | https://duckdb.org/docs/stable/guides/performance/environment | Can process larger-than-memory workloads by spilling to disk; rule of thumb 1-2 GB per thread (aggregation-heavy) and 3-4 GB per thread (join-heavy); fast disks matter |
| DuckDB workload tuning limits | https://duckdb.org/docs/current/guides/performance/how_to_tune_workloads | Out-of-core support has limits: some complex aggregate states cannot yet be offloaded to disk and may cause out-of-memory errors |
| DuckDB concurrency | https://duckdb.org/docs/stable/connect/concurrency.html ; https://duckdb.org/docs/current/connect/concurrency | Native database file: one process reads and writes, or many processes read-only; multi-process writing is not automatic. Newer docs mention other options (see Unverified) |
| DuckDB FAQ: Parquet pattern for multiple writers | Mirror of the DuckDB web repo, https://github.com/pmm-motif/duckdb-web/blob/master/faq.md (not the official site; confirm on duckdb.org) | Suggests writing Parquet files and reading many of them with DuckDB when multiple processes must write |

## Known discrepancies to resolve
- SEC approval date of the FINRA Rule 4210 amendments: some sources say April 14, 2026, one says April 15, 2026. The effective date reported is June 4, 2026. Check the primary SEC order and FINRA Regulatory Notice 26-10.

## Unverified (do not rely on until checked)
- Lopez de Prado, *Advances in Financial Machine Learning* (2018) - recalled from memory
- Bailey, Borwein, Lopez de Prado, Zhu - work on the probability of backtest overfitting - recalled from memory
- Bailey and Lopez de Prado - Deflated Sharpe Ratio - recalled from memory
- Egger et al., "Quantum Computing for Finance: State-of-the-art and future prospects", IEEE Transactions on Quantum Engineering, 2020 - recalled from memory
- Qualified purchaser threshold of about $5 million in investments - seen only in a vendor glossary; verify against SEC text
- Perspective license terms
- Jane Street's use of OCaml - recalled from memory
- Suitability of Ray or Dask for parallel backtests
- Current state of practical quantum advantage in finance
- DuckDB version we will use, and whether newer multi-process write options (Quack remote protocol; DuckLake with a PostgreSQL catalog) are stable - mentioned in current DuckDB docs, not studied
- DuckDB S3 Parquet import/export pages - listed in the docs navigation, not yet read
- Parquet loading support and procedures for PostgreSQL/TimescaleDB, Snowflake, and Databricks - not yet checked
- Row-count estimates in docs/DECISIONS.md assume a universe of about 8,000 symbols (assumption, not sourced)
