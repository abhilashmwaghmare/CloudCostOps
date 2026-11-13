# CloudCostOps

Enterprise AWS Cloud Cost Optimization & FinOps Platform starter.

This repository is an initial scaffold. It includes a FastAPI backend with a health endpoint and starter Cost Explorer / EC2 inventory APIs, a React dashboard, Docker Compose, a GitHub Actions CI workflow, and a minimal Terraform S3 example.

## Important scope note
This is not a production-ready FinOps platform yet. CloudWatch collection, durable persistence, full inventory, optimization rules, recommendation approvals, safe execution, savings validation, and production hardening remain on the implementation roadmap.

## Quick start

```bash
cp .env.example .env
docker compose up --build
```

Backend health: `http://localhost:8000/health`

Frontend: `http://localhost:5173`

Do not expose application or database ports publicly. Use an EC2 instance profile with least-privilege read-only AWS permissions for AWS API access; do not commit AWS credentials.

## Project structure

- `backend/` — FastAPI application and tests
- `frontend/` — React dashboard
- `terraform/` — starter infrastructure configuration
- `.github/workflows/` — CI workflow
- `docs/` — implementation roadmap

See `docs/IMPLEMENTATION-ROADMAP.md` and `terraform/README.md` for next steps.
