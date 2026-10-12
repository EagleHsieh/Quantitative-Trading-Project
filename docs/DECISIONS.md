# Decision Log

Status values: **Decided** (confirmed by the project owner) or **Proposed** (suggested, awaiting confirmation).

| # | Date | Decision | Status | Notes |
|---|---|---|---|---|
| 1 | 2026-10-12 | Target market: US equities | Decided | Stated by owner |
| 2 | 2026-10-12 | Use a GitHub **repository** (not only a GitHub Project board); `main` plus topic branches; changes via pull requests | Decided | Project board may be added later for task tracking |
| 3 | 2026-10-12 | Keep handoff documents (`AGENTS.md`, `STATUS.md`, `DECISIONS.md`, `references.md`) so other AI agents can continue the work | Decided | Stated by owner |
| 4 | 2026-10-12 | Interactive visualization is a core feature | Decided | Stated by owner |
| 5 | 2026-10-12 | Support users from small individual accounts to large firms, via layered tiers | Decided | See README tiers |
| 6 | 2026-10-12 | Use multiple agents in parallel, each owning a module and branch | Decided | Interfaces fixed first |
| 7 | 2026-10-12 | Start with short- to medium-term strategies on daily data; make holding period a strategy parameter so intraday can be added later | Proposed | Rationale: smaller data, lower infrastructure and execution complexity |
| 8 | 2026-10-12 | Store data as partitioned Parquet files (source of truth) and use DuckDB as the query engine; move to a database server only if needed | Proposed | Avoids DuckDB's single-writer limit when several agents work at once (see docs/references.md). Size estimates, assuming ~8,000 symbols: daily bars ~40M rows over 20 years; 1-minute bars up to ~7.9B rows over 10 years (upper bound). Not benchmarked. |
| 9 | 2026-10-12 | Visualization: Python dashboard prototype first (Plotly Dash or Streamlit), React front end later | Proposed | |
| 10 | 2026-10-12 | Python as the core language | Proposed | |
| 11 | 2026-10-12 | Quantum computing: optional research module only, benchmarked against classical baselines | Proposed | No verified practical advantage assumed |
| 12 | 2026-10-12 | Cloud: later; containerize (Docker) from the start | Proposed | |
| 13 | 2026-10-12 | Hedge-fund methods (long/short, market-neutral, risk limits) as design inspiration; running an actual fund deferred | Proposed | Needs securities counsel if pursued |
| 14 | 2026-10-12 | All data access goes through one module in `src/`, so the storage backend can be swapped | Proposed | Migration path: copy Parquet to cloud storage, load into the target system, run old and new in parallel and compare results, then switch |
| 15 | 2026-10-12 | Before every merge, check for conflicts in contents and code and report the result | Decided | Stated by owner |
| 16 | 2026-10-12 | Project name is **TalonQuant** (GitHub repo `EagleHsieh/TalonQuant`, renamed from `Quantitative-Trading-Project`); the README title stays "Quantitative Trading Project" because it summarizes the project at a glance | Decided | Stated by owner. Name is for now and may change. Exact-name checks on PyPI, npm, and GitHub found no conflicts on 2026-10-12; trademark and domain checks not done |

## Open decisions
- License (none chosen yet; a public repository without a license is not open for reuse by default).
- Repository visibility (currently public).
- Data source and budget.
- Whether Claude may merge pull requests directly in chat. Technically possible with a token that has Contents and Pull requests write access. Proposed rule: only on an explicit instruction naming the pull request, after a conflict check and test run.
