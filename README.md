# Quantitative Trading Project

An open, research-grade toolkit for quantitative trading research on **US equities**, built to be useful from an individual trader with a small account to a professional or institutional team, with interactive visualization as a core feature.

> **Status:** early setup. No strategy or data code yet. See [`docs/STATUS.md`](docs/STATUS.md) for the current state.

## Goals
- Be useful to every kind of trader, from individuals with few assets to large firms.
- Be a rigorous resource for competitive traders, including aspiring quant traders.
- Provide excellent, interactive visualization that users can explore.
- Keep every claim, formula, and reference **verifiable**. Nothing is made up. See [`docs/references.md`](docs/references.md).

## Design principles
1. **Correctness first.** Sourced facts only; unverified items are labeled as such.
2. **Reproducible.** Any result can be rerun from code, data manifest, and parameters.
3. **Realistic backtests.** Transaction costs, slippage, no look-ahead, no survivorship bias.
4. **Holding period is a parameter.** The same engine should serve short- and long-term strategies.
5. **Layered by user tier.** A core library with no UI dependency, with tiers on top (see below).

## Planned tiers
| Tier | Audience | Approach |
|---|---|---|
| Individual | Small accounts | Local-first, free data sources, simple dashboard |
| Pro | Serious independent traders | Parallel backtests, walk-forward validation, richer interactive explorer |
| Institutional | Teams and firms | Cloud deployment, database server, audit logs, access control (later) |

## Repository layout
```
docs/        Project documents (status, decisions, references)
data/        Local data (git-ignored; see data/README.md)
src/         Source code
tests/       Automated tests
notebooks/   Research notebooks
viz/         Visualization / dashboard code
AGENTS.md    Rules and context for any AI agent or contributor
```

## Contributing (humans and AI agents)
Read [`AGENTS.md`](AGENTS.md) first. Work on a branch and open a pull request; `main` is changed only through reviewed pull requests.

## Disclaimer
This project is for research and education. It is **not financial advice**. Backtested results do not guarantee future performance, and trading involves risk of loss.
