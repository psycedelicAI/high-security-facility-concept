# Zone Model – High-Security Facility Concept

> A model for how security zones, sequential passage, movement logic, spatial threat understanding, and controlled transitions between environments can be used in a high-security facility.

---

## Document Information

| Field | Value |
|---|---|
| Document | Zone Model |
| Subject | High-Security Facility Concept |
| Type | Core Architecture Document |
| Status | Draft |
| Scope | Zone structure, passage, movement logic, deviation handling, roof-aware zoning, protected transitions |
| Audience | Security architects, facility planners, physical security specialists, technical leads, reviewers |

---

## Purpose

This document describes how the facility is divided into security zones and how movement between these zones can be controlled within the **High-Security Facility Concept**.

Its purpose is to define a model in which:

- zones represent different protection values
- passage takes place sequentially and under control
- movement patterns are themselves security-relevant
- some transitions require stronger control or containment
- deviations can be detected and handled
- the threat model is understood spatially and not only in two dimensions

The zone model is a central part of the concept’s trust architecture because physical presence, permitted movement, and location-bound context influence how trust is assessed.

---

# Why a Zone Model Exists

In a high-security environment, it is not enough to know that someone “has access.”

It is also important to understand:

- which zone the person is in
- how the person reached the zone
- whether the movement follows the expected sequence
- whether the presence is normal in the current environment
- whether the right activity is taking place in the right location
- whether someone has reached a sensitive surface through an unusual or unexpected path

Without zone logic, the facility risks being reduced to a collection of individual doors and authorizations without a clear physical trust model.

---

# Design Philosophy

## Zones Represent Trust Context

A zone is not only an area within the building, but a security context with its own rules, expectations, and protection requirements.

## Movement Has Security Meaning

How someone moves through the facility is security-relevant, not only where the person ultimately ends up.

## Access Should Be Progressive

Access to more sensitive areas should normally require passage through prior control points and should not be possible through illogical shortcuts.

## Some Transitions Need Stronger Control

Transitions between certain zones require a higher security level, stronger verification, containment, or special purpose validation.

## Zones Must Reflect Real Risk, Not Just Floor Plans

The zone structure must be based on protection value, function, movement risk, and attack surface — not only on the building’s physical floor plan.

## Spatial Threat Thinking Matters

Threats to the facility must not be understood as only ground-level or two-dimensional. The zone model must therefore account for spatial attack paths, including roofs, height-related surfaces, and structurally overlooked access points.

---

# 3D Threat Thinking in the Zone Model

The zone model in this concept is based on **3D Threat Thinking**.

This means that the facility is not divided only according to rooms, corridors, and entrances at ground level, but that other spatial surfaces and access paths may also need to be treated as security-relevant zones or zone-adjacent risk surfaces.

This includes, for example:

- roofs
- roof access points
- height-related service paths
- internal vertical connections
- unusual bypass routes between external and internal environments

The practical point is that protection must not assume that attackers always move according to the building’s intended use pattern.

The zone model must therefore be able to support a threat understanding in which intrusion may occur:

- from the side
- from above
- through structurally weak transitions
- via unusual but high-impact access paths

---

# Core Zone Types

The following zone categories are examples of how the facility can be structured.

## 1. External Perimeter Zone

External area around the building where presence, approach, and perimeter behavior can be observed.

Typical characteristics:

- first detection surface
- support for CCTV and FLIR
- vehicle and person movement near the building
- early indication of anomalous activity

## 2. Entry Control Zone

Area where initial access is verified.

Typical characteristics:

- reception or guarded entrance
- first identity check
- visitor control
- ability for early rejection or escalation

## 3. Controlled Transition Zone

Transition zone between lower-controlled and higher-controlled environments.

Typical characteristics:

- man-trap or equivalent passage control
- sequential verification
- containment capability
- clear boundary between a more open and a more protected area

## 4. Internal Controlled Zone

Internal zone with limited but normal operational movement.

Typical characteristics:

- work areas or internal passages
- controlled presence
- not fully unrestricted movement
- expected but not unlimited activity

## 5. High-Security Zone

Zone with higher protection value where presence should be more restrictive, more justified, and more clearly traceable.

Typical characteristics:

- stronger passage requirements
- lower tolerance for deviations
- stronger purpose-bound access
- higher requirements for escorting, logging, or control

## 6. Protected Technical Zone

Protected technical environment where human presence should normally be limited, justified, and especially controlled.

Typical characteristics:

- critical infrastructure
- higher requirements for technical, physical, and operational control
- limited service access
- clear linkage to maintenance, privileged access, and incident handling

## 7. Roof and Elevated Access Zone

Roof surface or other height-related surface that, in a high-security environment, should be treated as a security-relevant access surface rather than as a neutral building component.

Typical characteristics:

- low expected normal presence
- strong deviation character in case of unplanned activity
- need for sensors, surveillance, and reinforced access points
- linkage to 3D Threat Thinking and unusual intrusion paths

---

# Sequential Zone Access

A central principle in the model is that higher-protection zones should normally be reached through the correct sequence.

This means that a person or activity should be understandable in relation to prior passage through relevant control points.

Examples:

- external perimeter → entry control
- entry control → controlled transition
- controlled transition → internal controlled zone
- internal controlled zone → high-security zone
- high-security zone → protected technical zone

This strengthens:

- traceability
- trust assessment
- detection of illogical presence
- containment in case of deviation

Sequential passage does not mean that all movement must be identical, but that the security model should be able to distinguish between:

- normal expected path
- approved exception
- illogical or suspicious path

---

# Zone Transitions

The transition between zones is often more important than the zone surface itself.

Some transitions must therefore be treated as security controls in their own right.

## Low-to-Medium Control Transition

Transitions from a more open area to a more controlled area require basic verification and clear passage control.

## Medium-to-High Security Transition

Transitions into a high-security zone should require stronger control, higher security tolerance, and a clearer link to purpose.

## High-to-Technical Transition

Transition into a protected technical zone must be especially strict because presence there may have high consequence.

## Roof-to-Interior Transition

Transitions between the roof and the internal environment must, in a high-security facility, be treated as especially sensitive because they may form unusual bypass paths for intrusion.

Such transitions should:

- be structurally reinforced
- be instrumented with sensors
- be monitored
- generate alarms on unplanned activity
- not allow direct and uncontrolled onward passage

---

# Movement Logic

Movement within the facility must be understood as a security signal.

This means that the system should be able to distinguish between:

- normal movement
- unusual but legitimate movement
- anomalous movement
- potentially hostile or unauthorized movement

## Normal Movement

Movement that follows the expected path, role, and purpose.

## Unusual but Legitimate Movement

Movement that deviates from everyday patterns but is planned, approved, or explainable.

## Suspicious Movement

Movement that lacks a clear explanation, breaks sequence, or reaches the wrong zone at the wrong time.

## High-Risk Movement

Movement that indicates an attempt to bypass control, reach a protected surface via the wrong path, or combine physical presence with suspicious intent.

---

# Roof-Aware Movement Logic

In a model based on 3D Threat Thinking, movement must also be understood in relation to height and unusual access paths.

This means that:

- rooftop activity should normally have a very low baseline
- unplanned rooftop presence should be treated as a strong deviation
- movement from the roof zone toward the internal structure should be treated as a high-risk event
- roof-related access should be distinguishable from normal ground-level traffic

This makes the threat model less dependent on two-dimensional perimeter logic.

---

# Containment and Verification

When movement, passage, or zone presence deviates from the expected model, the facility must be able to respond.

This may involve:

- verification
- temporary containment
- manual control
- alarm escalation
- redirection
- incident classification

Containment does not always need to be dramatic physical lockdown, but the model must be able to slow or mark uncertain passage so that trust is not granted automatically.

---

# Zone-Based Surveillance Integration

The zone model must work together with the surveillance model.

This means that camera and sensor logic should support:

- zone transitions
- sequential passage
- detection of anomalous movement
- roof-related incidents
- rapid visual verification of zone events

Examples of especially important camera support points:

- entrance
- reception
- man-trap
- transition into the high-security zone
- transition into the protected technical zone
- roof access points
- roof-adjacent surfaces and height-related access points

---

# Zone Integrity

Zone integrity means that a zone actually behaves like the security level it claims to be.

This means that zone integrity depends not only on doors or locks, but also on:

- passage control
- movement logic
- surveillance
- sensing
- deviation handling
- discipline in exception handling
- protection against unusual bypass paths

If illogical paths into a zone are tolerated, the zone loses part of its protection value even if formal access control exists.

---

# Exception Handling

All real facility environments have exceptions.

This may apply, for example, to:

- service
- maintenance
- emergency response
- temporary rerouting
- specially approved roof access
- recovery mode

These exceptions must, however, be treated as exceptions and must not become informal normality.

Exceptions should therefore:

- be documented
- be approved
- be time- or purpose-limited
- be traceable
- be reviewable afterward

---

# Governance Implications

The zone model requires governance to retain its strength over time.

This includes, among other things:

- clear ownership of the zone structure
- defined rules for passage between zones
- recurring review of zone segmentation
- review of exceptions and bypass patterns
- confirmation that roof-related risk surfaces continue to be handled
- coordination between physical security, surveillance, operations, and governance functions

---

# Design Boundaries

This document does not describe:

- full building-engineering design
- exact door or lock specifications
- complete fire or evacuation logic
- legal requirements per jurisdiction
- full implementation of sensor systems
- detailed staffing model

These aspects require separate design work, specialist input, and environment-specific adaptation.

---

# Summary

The zone model in the **High-Security Facility Concept** is not only about dividing a building into different areas.

It is about creating a security architecture in which:

- location matters
- movement matters
- transitions matter
- deviations can be detected
- higher protection value requires clearer sequence
- roofs and height-related surfaces are also treated as relevant parts of the threat model

The central idea is:

> A high-security facility becomes stronger when zones are not defined only geographically, but function as active trust contexts in which movement, transition, deviation, and spatial threat understanding are connected.
