# ROADMAP

This roadmap defines the implementation sequence for the Cloud-Native Event Processing Platform.

## 1) Bootstrap

### Goal
Establish a clean project baseline with repository standards, branch workflow, and build-ready structure.

### Deliverables
- Repository structure: `services/`, `infra/`, `docs/`, `.github/`
- Branching and contribution rules documented
- Initial CI baseline for pull requests

### Done criteria
- Team can create feature branches and open PRs into `develop`
- CI runs on PRs and reports status
- Project structure is stable and documented in README

---

## 2) Auth

### Goal
Provide secure authentication and token lifecycle management for platform access.

### Deliverables
- Auth service skeleton and API contracts
- Registration and login endpoints
- JWT access token and refresh token rotation flow

### Done criteria
- Valid users can register and log in
- Access tokens are issued and validated
- Refresh token rotation works and old refresh tokens are invalidated

---

## 3) Event Ingest

### Goal
Accept incoming events reliably and publish them to Kafka in an idempotent way.

### Deliverables
- Event ingest API endpoint
- Idempotency key handling and deduplication logic
- Kafka producer integration for accepted events

### Done criteria
- Duplicate requests with same idempotency key are safely handled
- Accepted events are published to the target Kafka topic
- Error handling is consistent and observable

---

## 4) Event Processing

### Goal
Process ingested events asynchronously with fault tolerance.

### Deliverables
- Kafka consumer for event processing service
- Retry policy for transient failures
- Dead Letter Queue (DLQ) handling for non-recoverable errors

### Done criteria
- Events are consumed and processed successfully under normal conditions
- Retriable failures are retried with configured policy
- Non-retriable failures are routed to DLQ with traceable metadata

---

## 5) Notification

### Goal
Deliver processed events to external systems through reliable webhook notifications.

### Deliverables
- Notification service skeleton
- Webhook delivery mechanism
- Retry/backoff strategy for failed deliveries

### Done criteria
- Successful events trigger webhook delivery
- Failed deliveries are retried according to policy
- Permanent failures are recorded and visible for operations

---

## 6) Observability

### Goal
Make platform behavior measurable and debuggable in production-like environments.

### Deliverables
- Metrics integration (Micrometer)
- Prometheus scraping and Grafana dashboards
- Structured JSON logging with correlation metadata

### Done criteria
- Core service metrics are exposed and scraped
- Dashboards show traffic, errors, and latency
- Logs support request/event tracing across services

---

## 7) Kubernetes

### Goal
Prepare the platform for cloud-native deployment and scaling.

### Deliverables
- Dockerfiles for all services
- Kubernetes manifests or Helm charts
- Baseline autoscaling and resource configuration

### Done criteria
- Services deploy successfully to a Kubernetes cluster
- Core workflows run end-to-end in cluster environment
- Basic scaling and health checks operate as expected
