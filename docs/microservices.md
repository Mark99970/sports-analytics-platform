# Microservices Description

## Ingestor-Service
**Purpose**
- Receives NBA game data.
- Validates and stores data in Postgres.

**Key Endpoints**
- `POST /games`
- `GET /games`
- `GET /health`

---

## Analytics-Service
**Purpose**
- Reads data and generates statistics.

**Key Endpoints**
- `GET /stats/basic`
- `GET /stats/team/{team}`
- `GET /health`

---

## API Gateway
**Purpose**
- Single external entrypoint.
- Forwards requests to the correct microservice.

**Public Endpoints**
- `/api/games` → Ingestor
- `/api/stats/*` → Analytics
