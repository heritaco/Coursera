# Compact glossary

## Planning & strategy

* **Wardley mapping:** Map components by user visibility vs. evolutionary maturity to spot strategic plays.
* **Opportunity–Solution Tree:** Outcomes → opportunities → experiments → solutions; trace why a feature exists.
* **JTBD (Jobs-to-Be-Done):** Describe user “jobs” independent of current solutions to avoid feature bias.
* **RICE:** Prioritize by Reach × Impact × Confidence ÷ Effort.
* **WSJF:** Weighted shortest job first; cost of delay ÷ job size.
* **MoSCoW:** Must, Should, Could, Won’t; requirement criticality tags.
* **Kano model:** Classify features as basic, performance, or delight based on satisfaction curves.
* **OKRs:** Objectives and Key Results; align goals and measurable outcomes.
* **North Star Metric:** Single metric capturing product value creation.
* **PR/FAQ:** Press-release plus FAQ spec that forces clarity before building.
* **RACI / DACI:** Responsibility and decision-making matrices for who does/decides/consults/informs.

## Discovery & architecture

* **Event storming:** Workshop to surface domain events and process flow.
* **DDD:** Bounded contexts, ubiquitous language, and context maps to tame complexity.
* **ADR:** Architectural Decision Record; lightweight, versioned rationale for choices.
* **Conway’s Law:** System design mirrors org communication structure.

## Delivery & DevOps

* **Trunk-based development:** Small, frequent merges to main; favors CI/CD.
* **GitFlow:** Branching model with long-lived develop/release branches.
* **Monorepo / Polyrepo:** Single vs multiple repos; centralization vs autonomy trade-offs.
* **Blue-green deploy:** Two prod stacks; swap traffic to reduce downtime.
* **Canary release:** Gradual rollout to a subset of users to de-risk.
* **Dark launch:** Ship latent code paths without exposing features.
* **Feature flags:** Toggle behavior at runtime; enable A/B and safe rollback.
* **Shadow traffic:** Replay real traffic to a new service without user impact.

## Reliability & performance

* **SLA / SLO / SLI:** Contracted target, internal objective, and measured indicator of reliability.
* **Error budget:** Allowed unreliability to balance velocity vs stability.
* **MTTR / MTBF:** Mean time to recovery / between failures; incident health signals.
* **Circuit breaker:** Fail fast on unhealthy dependencies to avoid cascades.
* **Bulkhead:** Isolate resources so one failure doesn’t sink all.
* **Idempotency key:** Ensure safe retries without duplicate effects.

## Data consistency & integration

* **Saga pattern:** Split distributed transaction into compensable local steps.
* **Outbox pattern:** Persist events atomically with state to avoid dual-write loss.
* **CAP theorem:** In partition, choose consistency or availability.
* **PACELC:** Even without partition, trade latency vs consistency.

## Data, ML, and AI

* **RAG:** Retrieval-augmented generation; ground LLM with external knowledge.
* **Vector database:** Index embeddings for semantic search and similarity.
* **Embedding drift:** Representation shift that degrades retrieval quality.
* **Zero-/few-shot:** Inference with no or few examples in the prompt.
* **Guardrails:** Policies and checks that constrain model behavior.
* **Prompt leakage:** Unintended exposure of hidden/system prompts.
* **Tool use / agents:** Models invoking tools or sub-policies to act.
* **Self-consistency:** Sample multiple reasonings and aggregate for robustness.
* **Multi-armed bandit:** Online allocation to best option under uncertainty.
* **CUPED:** Variance reduction using pre-experiment covariates.
* **Uplift modeling:** Predict causal lift, not just response.
* **Power analysis:** Estimate sample size to detect an effect.
* **Data flywheel:** Usage → data → better model → better product → more usage.

## Security, risk, and safety

* **STRIDE:** Spoofing, Tampering, Repudiation, Information disclosure, DoS, Elevation of privilege.
* **PASTA:** Risk-centric threat modeling methodology across stages.
* **STPA:** Systems-theoretic process analysis for hazards in complex systems.
* **Chaos engineering:** Intentionally inject failure to validate resilience.
* **Game day:** Rehearsed incident scenario to train and harden.
* **Runbook:** Stepwise operational playbook for common events.

## Quality & process improvement

* **Blameless postmortem:** Fact-focused learning after incidents.
* **Five whys / fishbone:** Root-cause analysis techniques.
* **Value-stream mapping:** Visualize flow to remove waste.
* **DORA metrics:** Deploy frequency, lead time, change-fail rate, MTTR.
