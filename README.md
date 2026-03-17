# GitOps Repository

This repository is the **single source of truth** for all Kubernetes deployments managed by ArgoCD.

## How It Works

```
Push to this repo → ArgoCD detects change → Deploys to Kubernetes
```

No manual `kubectl apply` needed. Everything is controlled by Git.

## Structure

```
apps/
├── nginx/
│   ├── deployment.yaml
│   └── service.yaml
└── <future-apps>/
```

## Managed By

- **ArgoCD** watches this repository
- **Auto-sync** is enabled — any Git push triggers deployment
- Part of the [GitOps Multi-Tenant SaaS Deployment Platform](https://github.com/imperfect0007/GitOps-Multi-Tenant-SaaS-Deployment-Platform)
