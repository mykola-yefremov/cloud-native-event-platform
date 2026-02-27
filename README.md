# Cloud-Native Event Processing Platform

A production-like, cloud-native event-driven platform for ingesting, processing,
and delivering events at scale.

This project demonstrates how modern backend systems are built using asynchronous
messaging, microservices, Kubernetes and observability-first principles.

---

## Why This Project Exists

In real-world systems, synchronous communication between services leads to:
- tight coupling
- cascading failures
- poor scalability

This platform solves these problems using an **event-driven architecture** where
services communicate asynchronously via Kafka.

---

## High-Level Architecture

Clients → API Gateway → Services → Kafka → Consumers → External Webhooks

**Services**
- API Gateway
- Auth Service
- Event Ingest Service
- Event Processing Service
- Notification Service

---

## Tech Stack
- Java 17, Spring Boot, Security (JWT), Data JPA
- Apache Kafka
- PostgreSQL
- Docker (multi-stage builds) & Kubernetes
- Helm
- Prometheus & Grafana
- Micrometer & Structured JSON logging
- GitHub Actions

---

## Key Features
- Event-driven architecture
- JWT-based authentication with refresh token rotation
- Idempotent event ingestion
- Retry & Dead Letter Queue handling
- Horizontal pod autoscaling
- Observability (metrics, logs, tracing)

---

## How to Run Locally
(coming soon)

---

## Roadmap
- [ ] Auth service
- [ ] Event ingestion
- [ ] Kafka processing
- [ ] Kubernetes deployment
- [ ] Observability

## Development Flow

We use a `main` + `develop` branching model.

- `main` is release-only and must always stay stable.
- `develop` is the integration branch for completed feature work.
- `feature/*` branches are used for isolated implementation and merged into `develop` via Pull Request.

### Merge Rules

- No direct pushes to `main`.
- No direct pushes to `develop`.
- Every change must go through Pull Request review.
- Prefer squash merge for clean history.
- Use Conventional Commits for commit messages (`feat:`, `fix:`, `docs:`, `chore:`, `test:`, `ci:`).

## Project Structure

- `.github/` - GitHub workflows, PR templates, and repository automation.
- `docs/` - architecture notes, roadmap, and operational documentation.
- `infra/` - infrastructure manifests and deployment assets (Docker, Kubernetes, Helm).
- `services/` - backend services (Auth, Event Ingest, Event Processing, Notification).

