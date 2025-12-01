# Project Overview – Sports Analytics Microservices Platform

This project is a cloud-native training platform designed to simulate a real microservices architecture for DevOps and Cloud Engineering learning.

## 🎯 Goals
- Learn how microservices communicate.
- Train on Docker and containerization.
- Deploy services on Kubernetes (k3d).
- Manage API Gateway routing.
- Integrate a Postgres database.
- Set up monitoring (Grafana / Prometheus).
- Prepare for AWS migration (EKS, RDS, ECR).

## 🧱 Architecture Summary
- **ingestor-service** → receives NBA game data, writes to Postgres.
- **analytics-service** → reads data and computes statistics.
- **api-gateway** → single public entrypoint for all clients.
- **Postgres** → persistent database.
- **Grafana** → visualization layer (later).

## 🏗 Deployment
- Phase 1 → Local deployment with Docker & Docker Compose.
- Phase 2 → Kubernetes deployment using k3d.
- Phase 3 → Migration to AWS using EKS + RDS (future).

## 📌 Project Status
**Phase 1: In progress**
- Repository structure prepared
- Microservices documentation
- Deployment planning

**Next step:** Week 1 – Local environment setup on CentOS VM.
