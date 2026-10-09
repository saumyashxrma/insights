# OmniInsight

Analytics for small e-commerce and retail businesses. Upload sales and marketing data, check data readiness, run customer segmentation, sales forecasting, churn/inactivity risk, and Marketing Mix Modeling, and get results with uncertainty and limitations.

**Status:** Phase 0 — foundation. See `docs/` for the problem statement and ADRs.

## Repository layout

- `apps/api` — FastAPI service (HTTP only; no model logic).
- `apps/web` — Next.js frontend (UI only).
- `packages/core` — the single home for analytics logic. Imported by apps, workers, notebooks, and CI.
- `infra` — Docker Compose, Dockerfiles, observability config.
- `pipelines` — dbt models and Airflow DAGs (later phases).
- `notebooks` — thin Colab/Kaggle runners calling `packages/core`.
- `data`, `evals`, `benchmarks` — datasets, assistant eval set, and saved results.
- `docs` — product, architecture, ADRs.