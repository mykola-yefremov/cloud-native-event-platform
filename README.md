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
