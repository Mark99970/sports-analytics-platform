# Sports Analytics Microservices Platform

A cloud-native microservices project designed for DevOps and Cloud Engineering training.

## Overview
The platform collects NBA game data, stores it in a Postgres database, processes analytics, and exposes the results via an API Gateway and dashboards.

The project is designed to build practical skills in:
- Docker & containerization  
- Kubernetes (k3d)  
- API Gateway routing  
- Microservices communication  
- Postgres integration  
- Monitoring with Grafana & Prometheus  
- Cloud migration (AWS – future phase)  
- CI/CD pipelines  

## Architecture
Microservices:
1. **ingestor-service** — receives game data and writes to Postgres  
2. **analytics-service** — computes statistics  
3. **api-gateway** — single public entrypoint  

Additional components:
- **Postgres DB**  
- **Grafana Dashboard**  

## Local Deployment
The first phase runs locally using:
- Docker  
- docker-compose  
- k3d Kubernetes cluster  

## Next Steps
- Add CI/CD with GitHub Actions  
- Migrate Postgres → AWS RDS  
- Migrate microservices → AWS ECR + EKS  
- Add Terraform IaC  
- Add Cloud observability (CloudWatch, managed Grafana)  

## Status
**Phase 1 (Local DevOps)** — in progress  
