# Compact glossary (additions)

## Product & requirements

* **User story:** Short requirement from user view. *As a \[role], I want \[capability] so \[benefit].*
* **Acceptance criteria:** Verifiable conditions to mark a story done.
* **Epic:** Large objective split into stories.
* **Persona:** Archetypal user to anchor decisions.
* **Backlog grooming:** Prioritize and refine upcoming work.
* **DoR / DoD:** Definition of Ready / Done gates for flow quality.

## CI/CD & DevOps

* **CI (Continuous Integration):** Auto build+test on each change to detect breakage early.
* **CD (Delivery/Deployment):** Auto promote artifacts to staging/prod with approvals or fully automated.
* **Pipeline:** Orchestrated steps: checkout → build → test → scan → package → deploy.
* **Artifact:** Built output stored immutably (wheel, JAR, container).
* **IaC:** Infrastructure as Code (Terraform, CloudFormation).
* **Trunk-based:** Short-lived branches merged to main frequently.
* **Blue-green / canary / feature flags:** Safe-release strategies.
* **Test pyramid:** Many unit, fewer integration, few end-to-end.

## SaaS & cloud

* **SaaS:** Vendor-hosted app delivered over the internet.
* **PaaS / IaaS / FaaS:** Platform / infrastructure / function runtimes.
* **Multi-tenant / single-tenant:** Shared vs isolated customer runtime.
* **Tenant isolation:** Controls that prevent data cross-leakage.
* **Metering / billing:** Usage capture and invoicing logic.
* **Plan tiering:** Feature and quota segmentation by price.

## Security & compliance

* **SSO:** Single sign-on via identity provider.
* **OAuth2 / OIDC:** Delegated authN/authZ for APIs and user login.
* **RBAC / ABAC:** Role-based vs attribute-based access control.
* **Rate limiting / throttling:** Protect capacity and fairness.
* **Secrets management:** Secure storage/rotation of keys and tokens.
* **GDPR / HIPAA / SOC 2 / PCI DSS:** Major data and security regimes.
* **DPA / DPIA:** Data processing and impact assessments.

## APIs & integration

* **REST / gRPC / GraphQL:** Dominant API styles.
* **OpenAPI:** Machine-readable REST spec.
* **Webhooks:** Server-to-server callbacks on events.
* **Event-driven / pub-sub:** Async decoupled communication.
* **Idempotency key:** Safe retries without duplicates.
* **API versioning / semver:** Backwards-compatibility contracts.

## Data & scaling

* **Caching (client/edge/app/db):** Reduce latency and load.
* **Shard / partition:** Split data horizontally for scale.
* **CQRS:** Separate read and write models.
* **Event sourcing:** State = replay of events.
* **Saga:** Orchestrate distributed transactions with compensation.
* **SLO/SLI/SLA:** Reliability target, measure, and promise.
* **Autoscaling:** Adjust capacity to load.

## Observability & quality

* **Logs / metrics / traces:** Core telemetry pillars.
* **p50/p95/p99:** Latency percentiles.
* **MTTR / change-fail rate:** DORA outcomes.
* **TDD / BDD:** Test- or behavior-driven development.
* **Static analysis / SAST / DAST / SCA:** Code and dependency scans.
