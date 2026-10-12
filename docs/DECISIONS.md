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
| 8 | 2026-10-12 | Start with Parquet files + DuckDB; move to a database server only if needed | Proposed | |
| 9 | 2026-10-12 | Visualization: Python dashboard prototype first (Plotly Dash or Streamlit), React front end later | Proposed | |
| 10 | 2026-10-12 | Python as the core language | Proposed | |
| 11 | 2026-10-12 | Quantum computing: optional research module only, benchmarked against classical baselines | Proposed | No verified practical advantage assumed |
| 12 | 2026-10-12 | Cloud: later; containerize (Docker) from the start | Proposed | |
| 13 | 2026-10-12 | Hedge-fund methods (long/short, market-neutral, risk limits) as design inspiration; running an actual fund deferred | Proposed | Needs securities counsel if pursued |

## Open decisions
- License (none chosen yet; a public repository without a license is not open for reuse by default).
- Repository visibility (currently public).
- Data source and budget.
