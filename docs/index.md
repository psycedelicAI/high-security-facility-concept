# Documentation Index

> A structured overview of the High-Security Facility Concept repository and its current document set.

---

## Purpose

This index provides a structured map of the repository’s documentation.

Its purpose is to make the document set easier to navigate by grouping the material according to its role in the concept. The repository is organized not as a flat collection of notes, but as a coherent body of work spanning foundational framing, architecture, operations, extensions, strategy, and evaluation.

The document set covers not only initial trust and access logic, but also how the environment should remain interpretable, governable, and controllable when access, movement, or presence no longer fit expected conditions.

---

## Repository Structure

The repository is organized under `docs/` using the following structure:

- `foundational/`
- `architecture/`
- `operations/`
- `extensions/`
- `strategy/`
- `evaluation/`

---

## Foundational

Core framing and conceptual grounding for the repository.

- [concept.md](foundational/concept.md) — The main concept description for the High-Security Facility Concept and its overall trust architecture framing.
- [executive-summary.md](foundational/executive-summary.md) — A concise high-level summary of the concept, its purpose, and its architectural direction.
- [one-pager.md](foundational/one-pager.md) — A short-form introduction intended for quick overview, briefing, or lightweight sharing.
- [design-principles.md](foundational/design-principles.md) — Core design principles that shape the logic, posture, and intent of the concept.
- [threat-model.md](foundational/threat-model.md) — The conceptual threat framing for the facility and the kinds of conditions the model is designed to resist, constrain, detect, interpret, or recover from.
- [FAQ.md](foundational/FAQ.md) — Clarifications, recurring questions, and concise conceptual answers.
- [diagrams.md](foundational/diagrams.md) — Visual overview material and diagram guidance supporting the concept’s structure and communication.

---

## Architecture

Core trust and security architecture models.

- [zone-model.md](architecture/zone-model.md) — Defines how the facility is divided into meaningful protection zones and how zones function as trust-relevant boundaries.
- [surveillance-model.md](architecture/surveillance-model.md) — Describes surveillance as an active visibility, interpretation, verification, and response-supporting function.
- [identity-and-actor-model.md](architecture/identity-and-actor-model.md) — Explains how actor type, role, legitimacy, and contextual trust affect how presence is interpreted.
- [trust-state-model.md](architecture/trust-state-model.md) — Models how trust can narrow, degrade, suspend, and recover rather than remain binary.
- [privileged-access.md](architecture/privileged-access.md) — Describes how privileged identities, devices, and actions are separated and governed as elevated-risk functions.
- [asset-custody.md](architecture/asset-custody.md) — Explains how credentials, devices, and other trust-bearing assets must remain under controlled custody.
- [governance-model.md](architecture/governance-model.md) — Defines the governance structure that keeps the concept durable, accountable, reviewable, and policy-anchored.
- [policy-baseline.md](architecture/policy-baseline.md) — Establishes baseline policy expectations across trust, access, review, exception handling, and control.
- [post-access-trust-control.md](architecture/post-access-trust-control.md) — Describes how the model detects, interprets, and controls incorrect or unjustified presence after initial access has failed, been bypassed, or been contextually misused.

---

## Operations

Operational resilience, controlled continuity, and reviewability.

- [incident-response.md](operations/incident-response.md) — Describes how the environment detects, classifies, contains, and responds to incidents.
- [degraded-operations-model.md](operations/degraded-operations-model.md) — Defines how the facility remains governable when trust, systems, or operating assumptions are weakened but not fully collapsed.
- [recovery-model.md](operations/recovery-model.md) — Explains how trust, control, and operational legitimacy are restored after disruption or incident.
- [maintenance-model.md](operations/maintenance-model.md) — Describes how maintenance and technical work should occur under controlled and reviewable conditions.
- [audit-and-review-model.md](operations/audit-and-review-model.md) — Defines how reconstructability, accountability, reviewability, and follow-up are maintained across the concept.

---

## Extensions

Supporting architecture extensions that strengthen realism, signaling, and survivability.

- [incident-lighting.md](extensions/incident-lighting.md) — Explores how lighting can support detection, interpretation, safety, and control during abnormal conditions.
- [alarm-and-signaling-model.md](extensions/alarm-and-signaling-model.md) — Describes how alarm semantics and signaling categories should remain meaningful and distinguishable.
- [passive-fire-resilience.md](extensions/passive-fire-resilience.md) — Explains how passive fire resilience supports survivability, containment, and architectural seriousness in high-security environments.

---

## Strategy

Use, positioning, interpretation, and future direction.

- [use-cases.md](strategy/use-cases.md) — Example use cases showing where and how the concept may be relevant.
- [value-proposition.md](strategy/value-proposition.md) — Explains the concept’s strategic value, differentiation, and public-facing relevance.
- [roadmap.md](strategy/roadmap.md) — Describes likely development directions, maturity progression, and future expansion areas.

---

## Evaluation

Independent assessment, reflection, and review material.

- [assessment.md](evaluation/assessment.md) — A broader evaluative document reviewing the concept’s strengths, structure, and development direction.
- [Concept-Evaluation-Scorecard.md](evaluation/Concept-Evaluation-Scorecard.md) — A structured category-based conceptual evaluation of the repository as an architecture project.
- [AI-Report-Review.md](evaluation/AI-Report-Review.md) — Review-oriented material reflecting on AI-generated assessment and interpretation of the concept.

---

## Reading Paths

Depending on the reader’s purpose, the repository can be approached through different paths.

### For a quick conceptual overview
Start with:

- [foundational/one-pager.md](foundational/one-pager.md)
- [foundational/executive-summary.md](foundational/executive-summary.md)
- [foundational/concept.md](foundational/concept.md)

### For core architecture understanding
Continue with:

- [architecture/zone-model.md](architecture/zone-model.md)
- [architecture/identity-and-actor-model.md](architecture/identity-and-actor-model.md)
- [architecture/trust-state-model.md](architecture/trust-state-model.md)
- [architecture/post-access-trust-control.md](architecture/post-access-trust-control.md)
- [architecture/privileged-access.md](architecture/privileged-access.md)
- [architecture/asset-custody.md](architecture/asset-custody.md)

### For operational control and resilience
Continue with:

- [operations/incident-response.md](operations/incident-response.md)
- [operations/degraded-operations-model.md](operations/degraded-operations-model.md)
- [operations/recovery-model.md](operations/recovery-model.md)
- [operations/audit-and-review-model.md](operations/audit-and-review-model.md)

### For signaling, survivability, and supporting extensions
See:

- [extensions/alarm-and-signaling-model.md](extensions/alarm-and-signaling-model.md)
- [extensions/incident-lighting.md](extensions/incident-lighting.md)
- [extensions/passive-fire-resilience.md](extensions/passive-fire-resilience.md)

### For strategic framing and external positioning
See:

- [strategy/value-proposition.md](strategy/value-proposition.md)
- [strategy/use-cases.md](strategy/use-cases.md)
- [strategy/roadmap.md](strategy/roadmap.md)

### For evaluation and concept review
See:

- [evaluation/assessment.md](evaluation/assessment.md)
- [evaluation/Concept-Evaluation-Scorecard.md](evaluation/Concept-Evaluation-Scorecard.md)
- [evaluation/AI-Report-Review.md](evaluation/AI-Report-Review.md)

---

## Current Documentation Direction

At this stage, the document set reflects a repository that is evolving from a strong conceptual archive into a more mature and coherent architecture body of work.

The structure increasingly supports:

- trust architecture framing
- contextual interpretation of access and presence
- movement- and zone-aware security logic
- post-access trust control
- controlled continuity under degraded conditions
- reviewability and governance discipline
- externally readable concept presentation

---

## Notes

This documentation set is conceptual in nature.

It is intended to support architectural thinking, structured discussion, review, and further development. It should not be interpreted as a finalized implementation blueprint, certified engineering specification, or jurisdiction-specific compliance design.
