# Surveillance Model – High-Security Facility Concept

> A model for how CCTV, thermal surveillance, anti-tamper placement, roof security, 3D Threat Thinking, and operational incident views can be integrated into a high-security facility environment.

---

## Document Information

| Field | Value |
|---|---|
| Document | Surveillance Model |
| Subject | High-Security Facility Concept |
| Type | Supporting Security Architecture Document |
| Status | Draft |
| Scope | CCTV, thermal surveillance, camera placement principles, anti-tamper logic, roof surveillance, incident focus views |
| Audience | Security architects, physical security planners, surveillance operators, facility planners, reviewers |

---

## Purpose

This document describes how surveillance can be designed as an integrated part of the **High-Security Facility Concept**.

Its purpose is to formulate principles for:

- external CCTV placement
- thermal surveillance / FLIR
- mutual camera coverage
- tamper-resistant and tamper-evident design
- roof security and rooftop sensing
- zone-based incident views
- operational usability during alarms and incidents

The goal is for the surveillance system not merely to “exist,” but to be designed to:

- detect
- verify
- monitor its own control points
- support rapid operator response
- contribute to traceability, containment, and recovery

---

# Surveillance Philosophy

Surveillance in a high-security facility must not be seen as a passive recording function.

In this model, surveillance is instead:

- an active security control
- part of the facility’s trust architecture
- support for incident detection and verification
- protection even for other security controls
- a tool for rapid situational understanding under pressure

This means that cameras should not only provide general coverage, but should also be placed and grouped so that they:

- reduce blind spots
- make sabotage more difficult
- monitor their own camera positions
- provide redundancy
- support rapid operational focus during incidents
- support a spatial threat model in which intrusion is not assumed to occur only at ground level

---

# 3D Threat Thinking in Surveillance

In this model, surveillance is designed according to **3D Threat Thinking**.

This means that the threat model is not understood as a flat or two-dimensional perimeter problem, but as a spatial security challenge in which intrusion, presence, and impact can occur from multiple directions and levels.

For surveillance, this means that camera logic and sensors should not only cover:

- entrances
- facades
- ground-level movement paths

but must also account for:

- roof access
- height-related attack paths
- unusual or non-linear approach paths
- structurally overlooked surfaces
- sabotage against the surveillance system itself

This makes the surveillance model better suited to high-security environments where attackers are not expected to follow normal access routes.

---

# Core Principles

## 1. Surveillance Is Part of Security Control, Not Just Observation

The camera system must be treated as an active part of the security model, not only as a retrospective support function.

## 2. Cameras Should Help Protect Cameras

Critical camera positions should be monitored by other cameras to make manipulation, covering, or damage more difficult to perform unnoticed.

## 3. Different Camera Types Have Different Roles

Standard CCTV and thermal sensors / FLIR should be used for different but complementary purposes.

## 4. External Coverage Should Be Designed for Tamper Resistance

External cameras should be placed so that sabotage attempts against one individual camera can be observed by other sensors or cameras.

## 5. Roof Areas Are Security-Relevant Surfaces

Roofs and roof-related access points must be treated as security-relevant surfaces, not as side issues of building engineering.

## 6. Operator Speed Matters

Surveillance must be usable effectively in incident conditions. The right information must be quickly available without heavy manual navigation.

## 7. Surveillance Should Follow Zone Logic

Camera structure and camera views should reflect the facility’s security zones and critical access points.

---

# Surveillance Layers

## Layer 1 – Standard CCTV

Standard CCTV is used primarily for:

- visual confirmation
- identification
- event reconstruction
- monitoring of mounting points
- detection of sabotage against other cameras
- follow-up of movement around facades, entrances, and access points

## Layer 2 – Thermal / FLIR

FLIR or other thermal surveillance is used primarily for:

- perimeter detection
- nighttime capability
- detection in low visibility
- detection of persons near the facade or outer protective line
- complementing normal visual surveillance
- detection in areas where traditional visual surveillance is weaker

## Layer 3 – Overwatch / Elevated Control

Higher-mounted cameras are used for:

- overall overview
- monitoring of critical lower-mounted cameras
- downward oversight of camera areas
- additional angle during sabotage, incident, or movement near the building
- support for roof security and monitoring of height-related surfaces

---

# External CCTV Placement Model

## Design Intent

External cameras should not be placed only to “cover corners” or provide a general perimeter image.

In this model, external cameras should also help monitor:

- each other
- their mounting points
- nearby approach paths
- attempts at physical manipulation or damage

## Mutual Oversight Pairing

A recommended pattern is to use side-mounted cameras that visually cross-monitor each other.

### Side Camera A

- placed on one side of the building or facade surface
- directed toward the opposite side
- should cover the facade surface, movement path, and the position of the other camera

### Side Camera B

- placed on the opposite side
- directed back toward the first side
- should cover the facade surface, movement path, and the position of the first camera

This creates:

- mutual surveillance
- better redundancy
- greater resistance to sabotage against a single camera
- better probability of capturing manipulation, covering, or approach

## Elevated Overwatch Camera

A third camera should, in critical cases, be placed higher up, for example near the roof edge or another protected elevated position.

This camera should:

- look down toward the side-mounted cameras
- monitor the area where sabotage or manipulation may occur
- provide an additional angle for verification
- reduce dependence on only two side views

This creates a simple but strong anti-tamper arrangement in which cameras are not left unmonitored.

## Practical Interpretation

The goal is not that every building must always use exactly the same geometry.

The goal is that camera placement should follow the principle of:

- mutual coverage
- monitoring of camera positions
- minimization of single points of failure
- improved sabotage detection

This should therefore be seen as a design principle, not an absolute layout rule.

---

# FLIR / Thermal Camera Positioning

## Role of FLIR

Thermal cameras should be used as a complementary layer rather than as a replacement for standard CCTV cameras.

They are particularly useful for:

- perimeter monitoring in darkness
- movement detection in low or varying lighting
- monitoring of shadowed or difficult-to-illuminate areas
- early indication of presence near the facade or outer protective line
- support for detection along spatial attack paths where visual cameras are not always sufficient

## Corner Placement

In this model, thermal cameras may advantageously be placed at building corners, where they can contribute:

- broad perimeter overview
- heat-based detection from multiple directions
- support to standard CCTV
- improved detection in outer areas

Unlike standard CCTV, which in some cases should be placed for mutual anti-tamper surveillance, FLIR can to a greater extent be used to strengthen perimeter detection from corner positions.

## Sensor Complementarity

Standard CCTV and FLIR should be seen as complementary:

- CCTV provides better visual verification and detail
- FLIR provides better detection in certain lighting and weather conditions

Together they provide:

- better detection
- better verification
- better robustness in varying conditions

---

# Roof Security and Elevated Access Surveillance

## Roof as a Security-Relevant Surface

In a high-security environment, the roof must be treated as a security-relevant surface, not as a neutral building component.

This means that the roof must be understood as a possible:

- intrusion path
- sabotage surface
- observation point
- access route to protected structures
- bypass of traditional ground-level perimeter logic

## Why Roof Security Matters

In some high-risk environments, attackers may use unusual or asymmetric intrusion paths, including roof access.

The security model must therefore not assume that threats come only via:

- main entrances
- ground level
- expected access points

Instead, height-related and structurally overlooked paths must also be treated as realistic risk surfaces.

## Roof Access Hardening

Roof-related openings and access points should be designed with strong protection.

This may include:

- reinforced roof hatches or service entries
- tamper-resistant access points
- delaying barriers
- controlled transition points between the roof and interior spaces
- structural hardening where the threat model justifies it

The principle is that even if someone reaches the roof, this must not mean easy or direct further access into the protected internal environment.

## Roof Sensors

Roof surfaces and critical roof access points should be capable of being instrumented with sensors.

Examples of relevant control mechanisms:

- motion detection
- presence detection
- tamper sensors on hatches or access points
- vibration indication where relevant
- alarm linkage for unplanned rooftop activity

What matters is that the roof has:

- detection
- alarm capability
- ability to verify
- linkage to operational response

## Roof Surveillance

Roof monitoring should be supported through:

- elevated cameras
- relevant sightlines toward the roof edge and access paths
- thermal sensors where they improve detection capability
- camera angles that can verify activity on or toward the roof

As a general rule, unplanned rooftop presence in a high-security environment should be treated as a strong deviation until verified otherwise.

---

# Tamper-Resistant and Tamper-Evident Surveillance

Fully tamper-proof surveillance is rarely realistic.

The model should therefore primarily strive to be:

- tamper-resistant
- tamper-evident

This means that the camera system should be designed so that manipulation becomes:

- harder to perform
- easier to detect
- easier to verify afterward

## Tamper-Resistant Measures

Examples of principles:

- cross-monitoring between cameras
- elevated overwatch cameras
- protected mounting points where possible
- multiple angles toward critical attack points
- combination of visual and thermal detection
- monitoring of roof access and height-related surfaces

## Tamper-Evident Measures

Examples of principles:

- sabotage attempts are captured by another camera
- sudden camera loss is linked to an alarm or operator indication
- event sequence can be reconstructed from more than one camera angle
- activity against roof-related control points becomes visible in both surveillance and control logic

---

# Surveillance by Zone and Function

Surveillance should be organized according to the facility’s zones and critical functions, not only according to technical camera names.

This means that cameras should be tied to areas such as:

- entrance
- reception
- man-trap
- perimeter north / south / east / west
- roof
- loading / service access
- technical access
- internal control zone
- protected technical zone

This improves:

- operational usability
- incident focus
- operator training
- shared terminology between security, operations, and management

---

# Rapid Incident Focus Presets

## Purpose

During an incident, the operator should not need to build situational awareness manually from scratch.

The system should therefore support predefined camera views or presets tied to specific areas and functions.

## Example: Entrance Focus

If an incident is detected at the entrance, the operator should be able to quickly activate a preconfigured view showing:

- all relevant entrance cameras
- nearby facade cameras
- any thermal coverage
- approach paths toward the entrance
- an overall view of the nearby zone

This should be possible through a very fast operational action, for example a dedicated button or preset activation.

## Example: Roof Focus

If activity or an alarm occurs on the roof, the operator should be able to quickly switch to a roof preset showing:

- relevant roof cameras
- nearby surveillance cameras
- roof-adjacent FLIR or thermal feeds where available
- nearby facade views that can capture approach or escape path
- access points between the roof and the internal structure

## Benefits

Predefined incident views improve:

- response time
- focus
- situational understanding
- ability to coordinate actions
- reduced cognitive load under stress

## Recommended Preset Examples

The following types of zone or function presets should be considered:

- Entrance
- Reception
- Man-Trap
- Perimeter North
- Perimeter South
- Roof
- Loading / Service Access
- Technical Access
- Internal Security Corridor
- Protected Technical Zone
- Emergency Evacuation View

---

# Operator Usability Under Pressure

Surveillance systems in a high-security environment must work under stress, not only during normal operations.

This means that the design should support:

- rapid switching between relevant views
- logical camera groups
- clear names and zone labels
- simple escalation from general view to focus view
- minimized time to locate the correct cameras

A surveillance solution that technically has many cameras but is slow to use during an incident provides lower operational value.

---

# Incident Integration

Surveillance must be integrated with incident work and not live as an isolated side track.

Camera data and camera views should be able to support:

- rapid alarm verification
- assessment of movement or presence
- containment decisions
- operator support to guards or response functions
- post-analysis and reconstruction
- recovery and return to normal operations

---

# Governance Considerations

The surveillance model should also be governed through clear governance.

This should include:

- defined ownership of camera logic and placement
- recurring review of camera coverage
- review of blind zones and sabotage exposure
- confirmation that presets still reflect the real layout
- documented principles for changes to camera structure
- coordination between physical security, IT, facility, and incident-responsible functions

---

# Design Boundaries

This document does not describe:

- exact camera models
- specific lens type or sensor choice
- recording policy in detail
- storage time / retention in detail
- legal or regulatory requirements for camera surveillance
- complete installation drawings
- complete building-engineering design of roof protection

These aspects require separate design work, legal assessment, and environment-specific adaptation.

---

# Summary

Surveillance in this model is not only about recording what happens.

It is about building a surveillance architecture that:

- supports the facility’s trust model
- protects its own control points
- uses both visual and thermal detection
- reduces sabotage exposure
- accounts for threats across multiple spatial dimensions
- includes the roof and height-related access paths in the threat model
- gives operators rapid focus during incidents
- strengthens detection, verification, and traceability

The central idea is:

> Surveillance should not only see what happens around the building, but also help protect the surveillance system itself, cover threats in 3D, and provide rapid, usable situational understanding when something actually happens.
