# Facility Chessboard Coordinate Layer – High-Security Facility Concept

> A facility-wide spatial reference system for describing observation, movement, camera coverage, zone context, incident locations, and patrol tasking through fixed floor-specific coordinates.

---

## Document Information

| Field | Value |
|---|---|
| Document | Facility Chessboard Coordinate Layer |
| Subject | Spatial coordination and operational location reference |
| Type | Supporting Operations Model |
| Status | Conceptual |
| Scope | Facility-wide observation, movement tracking, camera coordination, incident response, and patrol tasking |
| Related Areas | Surveillance, Incident Response, Zone Model, Master Watcher, Watcher Operations, Human Factors |
| Parent Concept | High-Security Facility Concept |

---

## Purpose

This document defines a facility-wide chessboard coordinate layer for use in:

- observation
- incident coordination
- movement tracking
- camera selection
- last-known-position reporting
- zone reference
- operational logging
- Watcher coordination
- Master Watcher control
- patrol tasking
- low-signature incident communication

The coordinate layer provides a shared and precise way to describe physical positions without relying primarily on:

- informal landmarks
- descriptive room names
- corridor names
- public-facing area names
- ambiguous expressions
- inconsistent local orientation

The system is intended to create a common operating picture for authorized personnel.

---

## Core Principle

> **Every operationally relevant area of the facility should be capable of being referenced through a shared, precise, stable, and visually consistent coordinate system.**

A coordinate should be usable whether a position is identified through:

- fixed cameras
- PTZ cameras
- the video wall
- the Master Watcher
- an individual Watcher station
- a floor plan
- direct observation
- access-control events
- asset-tracking events
- an incident log
- a patrol tasking display
- a wrist-worn or flashlight-mounted display

---

## Coordinate Architecture

The facility uses a layered spatial reference:

```text
Operational Floor
        ↓
Grid Square
        ↓
Local Sector
```

A complete operational coordinate is expressed as:

```text
[Operational Floor]-[Grid Square]-[Local Sector]
```

Example:

```text
BETA-F6-NE
```

This represents:

- `BETA` — operational floor designation
- `F6` — chessboard-style grid square
- `NE` — local sector within that square

The coordinate is a spatial reference, not an identity or task by itself.

---

## Facility Chessboard Grid

The facility is divided into a fixed grid resembling a chessboard.

Each grid position is identified by:

- a letter
- a number

Examples:

```text
A1
F6
C4
H8
```

Combined with an operational floor:

```text
ALPHA-A1
BETA-F6
GAMMA-C4
THETA-H8
```

The grid may be expanded for larger facilities:

```text
BETA-M12
GAMMA-P16
```

The exact grid size should be based on:

- required precision
- facility dimensions
- camera coverage
- zone boundaries
- operational density
- incident complexity
- expected movement
- required handoff accuracy

The grid should optimize:

```text
Precision + speed + interpretability
```

rather than maximum detail alone.

---

## Operational Floor Designations

The coordinate layer may use Greek operational floor designations.

Example:

| Physical floor | Operational designation |
|---|---|
| Floor 1 | Alpha |
| Floor 2 | Beta |
| Floor 3 | Gamma |
| Floor 4 | Delta |
| Floor 5 | Epsilon |
| Floor 6 | Zeta |
| Floor 7 | Eta |
| Floor 8 | Theta |

The mapping between operational and physical floor references must be maintained in a trusted facility reference system.

The mapping must not rely solely on operator memory during an active incident.

> **A grid coordinate without a floor designation is incomplete.**

Greek floor designations must not replace official emergency floor references during life-safety incidents.

---

## Fixed Spatial Orientation

Every floor grid must follow a fixed orientation relative to the facility.

The following systems should use the same orientation:

- physical floor plans
- security control-room displays
- video wall layouts
- Master Watcher interface
- Watcher station interfaces
- camera maps
- zone overlays
- incident markers
- movement trails
- patrol displays
- coordinate references

The grid must not rotate according to:

- selected camera
- operator position
- subject direction
- current incident
- temporary display layout
- camera viewing direction

The facility entrance should remain a stable shared reference.

> **One facility, one spatial orientation, one shared operating picture.**

---

## Coordinate Meaning

A coordinate may represent:

- a room
- a corridor section
- a technical area
- a transition point
- a controlled access area
- a camera field
- a temporary incident location
- a zone boundary
- a patrol destination
- a last-known position
- an observation point

The coordinate does not independently determine:

- identity
- intent
- authorization
- threat level
- task state
- response priority

Those attributes must be interpreted through the wider trust architecture.

> **Location is a security signal, not a complete interpretation of behavior.**

---

## Local Sector Precision

Each grid square may be divided into a local 3×3 sector structure:

```text
NW | N  | NE
---+----+---
W  | C  | E
---+----+---
SW | S  | SE
```

The local sector provides greater precision without requiring an excessively dense main grid.

Examples:

```text
BETA-F6-NW
BETA-F6-N
BETA-F6-NE
BETA-F6-W
BETA-F6-C
BETA-F6-E
BETA-F6-SW
BETA-F6-S
BETA-F6-SE
```

The sector boundaries must be defined in the controlled facility coordinate reference.

Operators and guards should not be expected to divide a square subjectively during a live incident.

If a space does not fit the 3×3 model, the facility may use:

- a controlled sub-coordinate
- a room reference
- a camera identifier
- an access-point identifier
- a zone identifier

The main coordinate system should remain simple while supporting greater precision where required.

---

## Coordinate Syntax

The standard coordinate syntax is:

```text
[Floor]-[Grid Square]-[Local Sector]
```

Example:

```text
BETA-F6-NE
```

The notation uses hyphens to separate:

```text
Floor - Grid Square - Local Sector
```

The coordinate should use a consistent uppercase format for operational displays and machine-readable records.

---

## Guard Assignment Syntax

A patrol assignment combines a guard call sign with an operational coordinate.

The human-facing format is:

```text
[Greek Designation]:[Roman Guard Number] ][ [Floor]-[Grid]-[Local Sector]
```

Example:

```text
THETA:VIII ][ BETA-F6-NE
```

This is interpreted as:

```text
Guard Call Sign: THETA:VIII
Assigned Coordinate: BETA-F6-NE
```

The notation uses:

- `:` between Greek designation and Roman guard number
- `][` between guard identity and assigned coordinate
- `-` between coordinate components

The call sign identifies the assigned operational guard. The coordinate identifies the task location.

A guard’s call-sign group and current task location may be different.

Example:

```text
THETA:VIII ][ BETA-F6-NE
```

A guard assigned to Theta may be sent to Beta because other guards are occupied.

---

## Route and Task Information

Route and task information should be displayed separately from the coordinate.

Example:

```text
THETA:VIII
BETA-F6-NE
ROUTE: STAIRS
TASK: MOVE
```

After arrival:

```text
THETA:VIII
BETA-F6-NE
TASK: OBSERVE
```

The coordinate identifies the location.

The route describes how the guard should move.

The task state describes what the guard should do.

Possible route values include:

```text
STAIRS
ELEVATOR
ROUTE-A
ROUTE-B
SERVICE-PATH
NORTH-STAIR
```

Possible task states include:

```text
MOVE
OBSERVE
HOLD
WAIT
RETURN
CANCEL
ESCALATE
```

These fields should not be merged into the coordinate itself.

---

## Observation States

The system should distinguish between different coordinate states.

### Static Coordinate

A fixed physical position.

```text
BETA-F6-NE
```

### Observed Coordinate

The latest position identified by a trusted source.

```text
Last observed: BETA-F6-NE
```

### Confirmed Coordinate

A position verified by more than one trusted source.

```text
Confirmed: BETA-F6-NE
```

### Estimated Coordinate

A position inferred from incomplete or indirect information.

```text
Estimated: BETA-F6-NE
```

### Predicted Coordinate

A projected future position based on movement, route, access, or facility constraints.

```text
Predicted next position: BETA-G6-W
```

A predicted position must never be presented as confirmed.

### Unresolved Position

Used when a reliable position cannot be established.

```text
Position unresolved
```

The interface should clearly distinguish:

- observed
- confirmed
- estimated
- predicted
- unresolved

---

## Confidence and Source Attribution

Each observation should carry a confidence state where practical.

Possible confidence values include:

```text
CONFIRMED
HIGH
MODERATE
LOW
UNVERIFIED
UNRESOLVED
```

The source should also be identified where possible:

- camera
- Watcher
- access-control event
- asset sensor
- radio report
- direct observation
- device signal
- system inference

Example:

```text
SUBJECT-01
CONFIRMED
BETA-F6-NE
CAMERA-12 + WATCHER-02
14:32
```

A coordinate without source or time context may be insufficient for incident response.

---

## Standard Observation Format

A standardized format should be used:

```text
[Subject or Event] – [Status] – [Coordinate] – [Time] – [Source]
```

Examples:

```text
SUBJECT-01 – LAST OBSERVED – BETA-F6-NE – 14:32 – CAMERA-12
```

```text
UNAUTHORIZED MOVEMENT – CONFIRMED – GAMMA-C4-S – 14:35 – CAMERA-08 + WATCHER-02
```

```text
RADIO-03 – ESTIMATED – ALPHA-B2-W – 14:38 – ASSET SYSTEM
```

A shorter spoken form may be used when speed is required:

> “Subject last observed, Beta-F6-NE.”

---

## Movement Tracking

The coordinate layer can record movement over time.

Example:

```text
ALPHA-C3-E → ALPHA-D3-W → ALPHA-D4-S → ALPHA-E4-N
```

A movement trail may show:

- direction of travel
- local sector changes
- time between positions
- pauses
- reversals
- zone transitions
- deviations from an authorized route
- movement after access denial
- movement after a silent alarm
- movement inconsistent with role or purpose

Movement should be interpreted together with:

- identity
- actor type
- role
- credential
- device
- zone
- time
- purpose
- escort state
- operational mode
- trust state
- access history
- observation confidence

---

## Camera Integration

Each camera should be associated with one or more grid coordinates.

Camera metadata may include:

- camera identifier
- operational floor
- camera coordinate
- viewing direction
- field of view
- covered zone
- adjacent coordinates
- PTZ capability
- current control owner
- health status
- recording status
- tamper state
- availability state

A camera’s physical location must be distinguished from:

- its field of view
- the subject’s position
- the subject’s direction of movement
- adjacent visible coordinates

Selecting a camera must not rotate the facility map.

---

## Camera and Zone Overview

When a camera or coordinate is selected, the system may display:

- all cameras covering the coordinate
- adjacent cameras
- neighboring coordinates
- the relevant zone
- neighboring zones
- active access points
- nearby movement
- current trust indicators
- active alarms
- connected assets
- assigned Watchers

This supports:

> **A selected point should reveal the surrounding operational context, not only one isolated camera view.**

---

## Master Watcher Integration

The Master Watcher provides the facility-aligned visual representation of the coordinate layer.

It should allow authorized operators to:

- select an operational floor
- select a grid square
- select a local sector
- view associated cameras
- display the surrounding zone
- highlight active incidents
- show movement trails
- identify assigned Watchers
- identify assigned guards
- display task states
- mark observations
- initiate temporary camera overviews
- transfer detailed control
- update or cancel patrol assignments

The Master Watcher may display the full facility context.

Patrol guards should receive only the information necessary for their assigned task.

---

## Watcher Integration

Individual Watchers should be able to:

- accept an observation task
- assign a guard
- select a coordinate
- define a local sector
- define a route
- set a task state
- control relevant cameras
- follow movement
- verify or reject an observation
- confirm arrival
- request additional coverage
- update a task
- cancel or escalate an assignment
- hand off responsibility
- record notes

The Watcher should see the wider incident context even when the guard sees only:

```text
THETA:VIII ][ BETA-F6-NE
```

---

## Incident Coordinate Wrist and Flashlight Displays

The coordinate layer may be delivered to patrol personnel through:

- wrist-worn e-paper displays
- low-power wrist displays
- flashlight-mounted LED displays
- secured handheld displays
- authenticated patrol equipment
- haptic tasking devices

A display may show:

```text
THETA:VIII ][ BETA-F6-NE
STAIRS
OBSERVE
```

The coordinate display supports:

- silent tasking
- low-signature communication
- reduced radio exposure
- route guidance
- arrival confirmation
- task-state updates
- auditability

The display should not become a full facility terminal.

It should show only the minimum actionable information.

---

## Radio-Silent Tasking

During a defined Silent Security Mode, the coordinate system may reduce the need to speak task information over shared radio channels.

Without a display:

```text
Proceed to Beta-F6, northeast sector, via the stairs and observe.
```

With a controlled display:

```text
THETA:VIII ][ BETA-F6-NE
STAIRS
OBSERVE
```

This reduces exposure of:

- incident location
- guard identity
- destination
- route
- response activity
- facility structure

Radio remains available for:

- life-safety events
- unexpected contact
- medical emergencies
- unclear instructions
- display failure
- communication failure
- escalation
- emergency responder coordination

Radio silence is a defined operating mode, not a prohibition on speaking when safety or clarity requires it.

---

## Coordinate and Directional Coding

The coordinate system remains spatially fixed.

Context-Dependent Directional Coding may alter the meaning of spoken directional terms during a defined covert security state.

These are separate layers:

```text
Fixed coordinate:
BETA-F6-NE

Context-dependent spoken direction:
May be remapped during Silent Security Mode
```

The coordinate must not silently change meaning for authorized personnel.

The coordinate layer should be used for stable spatial reference, while directional coding protects selected spoken communication.

---

## Security and Information Exposure

The coordinate system may reduce the intelligence value of radio communication by avoiding:

- descriptive room names
- informal landmarks
- public-facing area names
- direct references to sensitive zones
- unnecessary architectural details
- casual explanations of facility structure

However:

```text
Coordinate abstraction ≠ encryption
```

An adversary may reconstruct the grid through:

- repeated observations
- facility diagrams
- insider knowledge
- access events
- movement patterns
- repeated coordinate references
- compromised systems
- correlations with camera activity

The coordinate layer should therefore be combined with:

- authenticated communications
- credential custody
- device control
- access control
- surveillance
- incident verification
- audit and review
- communications-compromise procedures

---

## Human Factors

The system must be easy for authorized personnel to interpret under:

- stress
- low light
- fatigue
- noise
- time pressure
- gloves
- movement
- incomplete information

Design requirements include:

- fixed orientation
- consistent naming
- clear floor designations
- unambiguous pronunciation
- visible coordinate selection
- clear confidence states
- readable touch targets
- stable display syntax
- synchronized interfaces
- visible task ownership
- simple local-sector logic
- fallback procedures
- regular training and exercises

The system should avoid:

- unclear grid boundaries
- similar-sounding identifiers
- overloaded squares
- hidden coordinate transformations
- conflicting map orientations
- excessive task states
- long scrolling instructions
- reliance on memory
- silent device failure

> **The operational grid may abstract the facility for outsiders, but it must clarify the facility for authorized operators.**

---

## Life-Safety Compatibility

The coordinate layer may support life-safety response but must not introduce ambiguity.

During life-safety incidents:

- actual floor and room references remain available
- emergency responders are not required to know the internal coordinate system
- evacuation routes use approved signage
- emergency communications remain explicit
- physical directions remain clear
- coded communication is overridden
- silent tasking may be cancelled or replaced
- guards may use radio immediately

The system should support:

```text
Operational Coordinate
→ Actual Building Reference
→ Emergency Response Reference
```

No coordinate abstraction may delay rescue, evacuation, medical response, or emergency communication.

---

## Audit and Review

Coordinate-related actions should be recorded where appropriate.

The audit trail may include:

- floor selected
- grid square selected
- local sector selected
- coordinate selected
- user or Watcher
- guard call sign
- device identity
- camera sources viewed
- observation created
- confidence level
- movement trail
- task assignment
- route
- task state
- acknowledgement
- arrival confirmation
- camera-control handoff
- incident association
- time of action
- correction or closure
- system or metadata failure
- radio fallback
- life-safety override

Corrections should preserve the original event rather than silently rewriting history.

---

## Failure and Degraded Operations

The facility should define fallback behavior if the coordinate layer or tasking system is unavailable.

Possible failures include:

- Master Watcher unavailable
- floor-plan display unavailable
- coordinate database unavailable
- camera metadata unavailable
- display synchronization failure
- wrist display failure
- flashlight-display failure
- device loss
- battery failure
- route obstruction
- incorrect coordinate
- communication degradation
- conflicting location reports

Fallback procedures may include:

- approved printed floor plans
- controlled coordinate reference cards
- direct camera identifiers
- standard facility references
- manual event logging
- direct Watcher confirmation
- controlled radio communication
- guard reassignment
- temporary hold
- task cancellation
- explicit confidence statements

The system should not silently continue an outdated assignment when confidence in the task state is lost.

> **Reduced system confidence must not produce undefined behavior.**

---

## Example Operational Sequence

1. A silent, non-life-threatening security alarm is activated.
2. The Master Watcher identifies the affected operational floor and grid square.
3. The local sector is refined to `BETA-F6-NE`.
4. The Watcher reviews cameras and surrounding zone context.
5. Available guards are assessed.
6. Guards already engaged remain occupied unless reassigned through an authorized process.
7. `THETA:VIII` is selected because other guards are unavailable.
8. The assignment is sent to the authenticated patrol display.
9. The guard receives:

   ```text
   THETA:VIII ][ BETA-F6-NE
   STAIRS
   MOVE
   ```

10. The guard acknowledges discreetly.
11. Cameras and sensors support movement verification.
12. The guard arrives at the assigned sector.
13. The display updates to:

   ```text
   THETA:VIII
   BETA-F6-NE
   OBSERVE
   ```

14. The Watcher confirms arrival and observation.
15. The task is completed, updated, cancelled, or escalated.
16. The complete event history remains available for review.

---

## Design Requirements

The coordinate layer should satisfy the following requirements:

- every operational coordinate includes a floor designation
- every floor has fixed spatial orientation
- the facility entrance remains a stable reference
- grid squares have controlled boundaries
- local-sector boundaries are defined
- coordinates map to controlled metadata
- cameras are linked to relevant grid positions
- camera location is distinguished from field of view
- observations include time, source, and confidence
- predicted positions are never presented as confirmed
- Master Watcher and Watcher stations share orientation
- selected coordinates expose surrounding camera coverage
- guard call signs are separate from assigned coordinates
- route and task state are separate from position
- patrol displays show minimum necessary information
- silent tasking is authorized and auditable
- acknowledgement is available
- movement and arrival can be verified
- control ownership is visible
- handoffs are auditable
- coordinate history is preserved
- radio fallback exists
- device failure has defined handling
- life-safety references remain clear
- the coordinate system is treated as an abstraction layer, not encryption

---

## Relationship to the Wider Architecture

### Zone Model

Coordinates provide a spatial reference for zone boundaries, transitions, and access conditions.

### Surveillance Model

Cameras become spatial observation points linked to coordinates, fields of view, and confidence.

### Identity and Actor Model

A subject’s location is interpreted together with identity, role, actor type, and legitimacy.

### Trust-State Model

Movement through coordinates may contribute to changes in contextual trust.

### Context-Bound Authorization

A ticket’s permitted zones, route, and purpose may be compared with observed coordinates.

### Offline OPSEC Verification

High-risk ticket verification may use coordinate and camera context during human review.

### Post-Access Trust Control

Incorrect or unjustified movement can be detected after initial access.

### Incident Response

Coordinates support incident localization, guard tasking, observation, handoff, and containment.

### Degraded Operations

The coordinate layer provides fallback behavior when systems or assumptions are weakened.

### Master Watcher Operations

The Master Watcher provides the central spatial interface, while Watchers and patrol displays support detailed execution.

### Incident Coordinate Wrist Display Model

The wrist or flashlight display uses the coordinate layer to deliver low-signature patrol assignments.

---

## Limitations

The coordinate layer does not by itself provide:

- physical protection
- access authorization
- identity assurance
- communications encryption
- camera authenticity
- intent determination
- complete situational awareness
- guaranteed subject tracking
- life-safety compliance
- guaranteed radio silence

It is a coordination and abstraction layer.

Its effectiveness depends on:

- accurate facility mapping
- trusted metadata
- functioning surveillance
- authenticated devices
- trained operators
- trained guards
- clear procedures
- reliable communication
- regular testing
- disciplined review

---

## Summary

The Facility Chessboard Coordinate Layer provides a shared spatial language for:

- location
- observation
- movement
- camera coverage
- zone context
- incident response
- patrol tasking
- low-signature communication
- operational logging
- Watcher coordination
- Master Watcher control

It combines:

- Greek operational floor designations
- fixed facility orientation
- entrance-aligned spatial reference
- chessboard-style grid coordinates
- local 3×3 sector precision
- camera and zone metadata
- confidence-aware observation
- auditable movement tracking
- guard call signs
- route and task states
- wrist and flashlight display integration
- radio-silent tasking
- Master Watcher coordination
- Watcher-level control
- controlled camera handoff
- life-safety translation and override

The primary coordinate format is:

```text
BETA-F6-NE
```

The patrol assignment format is:

```text
THETA:VIII ][ BETA-F6-NE
```

This separates:

```text
Guard identity ][ Operational position
```

> **A precise shared coordinate system allows authorized personnel to understand the facility quickly, coordinate movement discreetly, and reduce the need to expose descriptive architectural information over shared communication channels.**

---

## Final Design Principles

> **The chessboard square identifies the area; the local sector identifies the position within it.**

> **The coordinate identifies the position; the task state identifies what should happen there.**

> **The control room sees the whole facility; the guard receives the minimum actionable task.**

> **The coordinate layer must make the facility easier to understand for authorized operators, harder to interpret from isolated communications, and never more ambiguous during life-safety operations.**
