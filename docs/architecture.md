
## Components
### 1. API Gateway
- Exposes all REST endpoints.
- Routes requests to internal services.
- No business logic, only forwarding.

### 2. Ingestor Service
- Accepts NBA game JSON input.
- Validates and writes data to Postgres.
- Provides `/games` endpoints.

### 3. Analytics Service
- Reads data from Postgres.
- Computes statistics (avg points, rebounds, win rate).
- Provides `/stats` endpoints.

### 4. Postgres
- Stores all game data.
- Queried by analytics and displayed via Grafana.

### 5. Grafana
- Connects directly to Postgres.
- Displays dashboards (not through API Gateway).

## Kubernetes Architecture
- Each microservice → Deployment + Service (ClusterIP).
- API Gateway → Ingress exposed.
- Postgres → StatefulSet (later), Deployment (initial).
- ConfigMaps for app config.
- Secrets for DB credentials.
