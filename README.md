# portfolio

Portfolio personnel — NestJS backend (PostgreSQL) + Next.js/React frontend.

## Structure

```
portfolio/
├── my-portfolio-backend/    # API NestJS + PostgreSQL
├── my-portfolio-frontend/   # Next.js / React
├── minio-on-fly/            # MinIO déployé sur Fly.io
├── docker-compose.yml       # Dev local (backend + frontend + postgres)
└── .github/
    └── workflows/
        └── ci-cd.yml        # CI backend + frontend + security scan
```

## Démarrage rapide

```bash
docker compose up -d
```

## CI/CD

Le workflow `ci-cd.yml` exécute :
- Tests backend (NestJS + PostgreSQL service)
- Type checking + build frontend
- Security scan (Trivy)
- Deploy staging (develop) / production (main)

## Licence

MIT — voir [LICENSE](LICENSE)
