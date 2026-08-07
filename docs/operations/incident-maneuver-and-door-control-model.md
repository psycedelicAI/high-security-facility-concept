# Incident Maneuver and Door Control Model – High-Security Facility Concept

> A controlled movement-management layer in which authorized operators temporarily shape passage conditions during defined security incidents while preserving life-safety access, accountability, and human verification.

---

## Document Information

| Field | Value |
|---|---|
| Document | Incident Maneuver and Door Control Model |
| Subject | Incident-based passage control and movement shaping |
| Type | Supporting Operations Model |
| Status | Conceptual |
| Scope | Temporary door control, guard-route support, passage management, containment, and recovery |
| Related Areas | Master Watcher, Incident Response, Facility Coordinates, Surveillance, Degraded Operations, Passive Fire Resilience, Recovery |
| Parent Concept | High-Security Facility Concept |

---

## Purpose

This document defines a controlled maneuver and door-control layer for use during selected security incidents.

The model allows authorized operators to coordinate:

- guard movement
- controlled passage routes
- temporary door states
- access-point sequencing
- movement restriction
- camera coverage
- subject separation
- verification time
- containment
- controlled release
- restoration of normal door operation

The purpose is not to allow unrestricted remote control of every door.

The purpose is to provide a controlled way to shape movement when:

- a silent security alarm is active
- a high-risk incident requires rapid response
- a guard needs an approved passage route
- uncontrolled movement must be temporarily restricted
- multiple zones must be coordinated
- additional time is needed for observation and verification

---

## Core Principle

> **During a defined incident, authorized operators may temporarily shape movement corridors and passage conditions to support response, verification, and containment.**

Door control must remain:

- authorized
- visible
- attributable
- time-limited
- condition-aware
- auditable
- subordinate to life safety

The system should create controlled time and separation for decision-making rather than automatically treating every detected person as hostile.

---

## Operational Problem

During a security incident, normal door behavior may create problems such as:

- delays for responding guards
- uncontrolled movement between zones
- open routes toward protected areas
- blocked routes for authorized responders
- conflicting access decisions
- unnecessary radio traffic
- unclear responsibility for temporary door states
- loss of containment after an observation

A coordinated maneuver layer can help the control room manage these conditions through a shared relationship between:

```text
Incident
→ Coordinate
→ Zone
→ Camera Coverage
→ Door and Passage State
→ Guard Route
→ Verification
→ Containment or Release
```

---

## Scope

The maneuver layer may be activated during:

- silent security alarms
- high-risk non-life-threatening incidents
- suspected unauthorized movement
- suspected insider activity
- communications compromise
- credential or ticket mismatch
- controlled guard response
- temporary zone isolation
- coordinated movement restriction
- incident-based passage management

It must not be used as a substitute for:

- emergency planning
- fire protection
- evacuation design
- access-control engineering
- life-safety systems
- professional security operations
- qualified incident command

---

## Relationship to the Wider Architecture

The maneuver layer connects:

```text
Detection
    ↓
Interpretation
    ↓
Coordinate and Zone
    ↓
Maneuver Panel
    ↓
Door and Passage State
    ↓
Guard Route Support
    ↓
Movement Verification
    ↓
Containment, Release, or Escalation
    ↓
Recovery and Audit
```

It uses:

- the Facility Chessboard Coordinate Layer for spatial reference
- the Master Watcher for facility-wide coordination
- Watcher Operators for detailed incident control
- surveillance for verification
- Incident Response for classification and escalation
- Degraded Operations for fallback
- Passive Fire Resilience for life-safety compatibility
- Recovery for restoration of normal states
- Audit and Review for reconstructability

---

## Incident Maneuver Panel

The Incident Maneuver Panel is a restricted control function within the Master Watcher environment.

It may provide authorized operators with:

- door status
- access-point status
- passage direction
- nearby camera coverage
- occupancy or presence indicators
- active route
- guard assignment
- incident state
- life-safety state
- temporary control ownership
- timeout information
- control history

The panel should not be a collection of unlabeled open, close, lock, and unlock buttons.

Each action should show:

- affected door or passage
- current state
- requested state
- responsible operator
- incident reference
- active duration
- timeout
- safety conditions
- resulting route effect
- whether acknowledgement is required

---

## Panel Availability

The maneuver panel should be unavailable or restricted during normal operations unless a specific administrative function requires access.

Possible activation states include:

```text
NORMAL
SILENT SECURITY MODE
HIGH-RISK INCIDENT MODE
COMPROMISED ACCESS MODE
EMERGENCY COORDINATION MODE
```

Activation should require:

- an authorized operator
- a defined incident or approved operational reason
- appropriate role permissions
- visible mode status
- audit logging

The panel must not become available merely because a person clicks a hidden interface element.

---

## Operational Roles

### Master Watcher Operator

The Master Watcher Operator maintains the facility-wide operational picture and may:

- authorize or approve incident-level maneuver actions
- review competing incidents
- prioritize routes
- approve door sequences
- monitor temporary door states
- resolve control conflicts
- authorize exceptional containment
- coordinate with the Incident Commander
- ensure restoration and review

### Watcher Operator

The Watcher Operator manages the assigned incident or zone and may:

- request a maneuver action
- select relevant doors
- define a guard route
- verify camera and coordinate context
- monitor door status
- confirm passage
- request a hold or release
- report unexpected conditions
- escalate when local control is insufficient

### Incident Commander

Where a separate Incident Commander exists, that role may determine:

- response posture
- zone closure
- escalation
- full-control transition
- emergency coordination
- return to normal operations

### Patrol Guard

The patrol guard:

- follows the assigned route where safe
- uses authorized passages
- reports hazards or blocked paths
- confirms arrival
- escalates uncertainty
- may override silent tasking when safety requires it

---

## Door and Passage States

The facility should define a controlled vocabulary for door states.

Possible states include:

```text
LOCKED
UNLOCKED
OPEN
CLOSED
HOLD OPEN
HOLD CLOSED
ACCESS RESTRICTED
ISOLATED
FAULT
UNKNOWN
EMERGENCY RELEASE
```

The meaning of each state must be defined operationally.

A displayed state should distinguish between:

- commanded state
- sensor-reported state
- verified physical state
- uncertain state

For example:

```text
Commanded: LOCKED
Sensor: CLOSED
Verification: CONFIRMED
```

or:

```text
Commanded: LOCKED
Sensor: UNKNOWN
Verification: UNRESOLVED
```

An unknown door state must not be presented as secure.

---

## Door Actions

Possible controlled actions include:

```text
LOCK
UNLOCK
OPEN
CLOSE
HOLD OPEN
HOLD CLOSED
ISOLATE
RELEASE
RETURN TO NORMAL
```

The actual available actions depend on:

- door type
- zone
- access classification
- life-safety function
- hardware capability
- current incident state
- operator permissions

A command should not be accepted if the requested state conflicts with:

- fire or smoke conditions
- evacuation
- emergency responder access
- anti-entrapment logic
- mechanical limitations
- current authorized passage
- known occupancy hazards

---

## Controlled Movement Corridors

The maneuver layer may define temporary movement corridors.

A corridor may consist of:

- starting coordinate
- destination coordinate
- allowed direction
- approved doors
- restricted side routes
- camera coverage
- guard assignment
- time window
- incident reference
- termination condition

Example:

```text
Guard: THETA:VIII
Origin: THETA-C2
Destination: BETA-F6-NE
Route: STAIRS
Passage: D-12 → D-14
Status: ACTIVE
```

The corridor should be treated as an operational route, not as a permanent change to facility architecture.

---

## Guard Route Support

The maneuver layer may support guard movement by:

- identifying an approved route
- opening an authorized passage when safe
- holding unnecessary side passages closed
- displaying route status
- confirming door sequence
- monitoring guard movement
- detecting blocked or unavailable passages
- updating the route when conditions change

The guard-facing display may remain minimal:

```text
THETA:VIII ][ BETA-F6-NE
STAIRS
MOVE
```

The Master Watcher and Watcher interfaces may show the complete door and route sequence.

---

## Door Sequence

A door sequence should be explicit and controlled.

Example:

```text
1. Verify life-safety state.
2. Confirm guard identity and assignment.
3. Confirm route and destination.
4. Verify door D-12 availability.
5. Permit authorized passage.
6. Confirm guard movement.
7. Restore D-12 to defined state.
8. Continue to D-13 only if conditions remain valid.
9. Terminate sequence on arrival, cancellation, fault, or escalation.
```

Each step should have:

- owner
- status
- timestamp
- condition
- confirmation
- failure behavior

A sequence should not continue automatically when a required condition becomes uncertain.

---

## Temporary Door-State Ownership

Every temporary door state must have an owner.

The system should record:

- operator identity
- station
- door or passage
- requested state
- reason
- incident
- start time
- expiry time
- extension authority
- current verification
- restoration state

Example:

```text
Door: D-12
State: UNLOCKED
Reason: Authorized guard passage
Incident: Silent Security Event-07
Owner: Master Watcher Operator
Started: 14:32
Expires: 14:36
Verification: Confirmed
```

A temporary state without an owner must be treated as unresolved.

---

## Timeout and Automatic Restoration

Temporary door actions should have defined time limits.

A temporary state should include:

- start time
- expiration time
- responsible operator
- extension authority
- restoration state
- alarm if the state remains active
- behavior if confirmation is lost

Example:

```text
Door D-12
State: UNLOCKED
Reason: Guard passage
Expires: 14:36
Owner: Master Watcher Operator
```

The system may return a door to its approved normal state after timeout only if doing so does not create a safety hazard or interrupt an authorized passage.

Automatic restoration must not be assumed to mean physical restoration.

The system should verify the resulting state.

---

## Movement Restriction and Containment

The maneuver layer may temporarily restrict uncontrolled movement by:

- securing selected side routes
- limiting passage between zones
- closing controlled access points
- maintaining safe responder corridors
- preventing movement toward protected areas
- separating incident areas
- preserving observation opportunities
- creating time for verification

The objective is controlled movement shaping.

It is not an automatic determination of guilt.

The system should account for:

- authorized persons
- uninvolved personnel
- guards
- escorts
- emergency responders
- maintenance personnel
- people needing assistance
- unknown occupants

---

## Containment Conditions

Before applying movement restrictions, the system should evaluate:

- life-safety state
- fire and smoke status
- occupancy
- emergency routes
- known guard locations
- active tickets
- current authorized passages
- camera coverage
- door status
- anti-entrapment conditions
- availability of manual override
- incident confidence

Containment should be proportionate to:

- confidence
- consequence
- affected zone
- threat
- current operational mode
- risk to innocent or authorized persons

---

## Anti-Entrapment and Safety Controls

The maneuver layer must include safeguards against unsafe closure or isolation.

Possible safeguards include:

- occupancy detection
- door-zone sensors
- emergency release
- manual override
- fire-system integration
- smoke-state awareness
- route validation
- guard location verification
- responder access
- door interlock monitoring
- physical egress preservation
- fault indication

A door should not be closed merely because a map shows that closing it would be convenient.

The system must account for people who may be:

- inside the door zone
- between controlled doors
- injured
- unable to respond
- authorized but not visible
- responding to an emergency

---

## Life-Safety Override

Life safety has priority over security containment.

During:

- fire
- smoke
- evacuation
- rescue
- medical emergency
- structural danger
- hazardous release
- emergency responder entry

the maneuver layer must follow approved life-safety behavior.

This may require:

- emergency release
- clear egress
- responder access
- explicit communication
- cancellation of security containment
- restoration of standard emergency door behavior
- use of actual floor and room references

> **Security containment must never prevent evacuation, rescue, medical response, or emergency access.**

Any life-safety override should be logged and reviewed afterward.

---

## High-Risk Actions and Dual Control

Certain actions may require elevated authorization or dual control.

Examples include:

- isolating a critical zone
- closing multiple routes
- changing access conditions around a protected technical zone
- overriding a normal door policy
- extending a temporary lock state
- acting during an active communications compromise
- controlling doors during uncertain occupancy
- applying facility-wide movement restrictions

Possible authority levels:

```text
Watcher Operator:
Request or control assigned low-consequence passages.

Master Watcher Operator:
Authorize incident-level maneuver sequences.

Dual Control:
Required for critical isolation or exceptional containment.

Emergency Authority:
Override ordinary security control for life safety.
```

The exact authority model must be defined by facility risk and governance requirements.

---

## Master Watcher Integration

The Incident Maneuver Panel should be integrated into the Master Watcher environment while remaining visually distinct from ordinary map navigation.

The Master Watcher Operator should be able to see:

```text
Coordinate: BETA-F6-NE
Incident State: SILENT SECURITY
Guard: THETA:VIII
Route: STAIRS
Door Sequence: ACTIVE
Camera Coverage: CONFIRMED
Life-Safety State: CLEAR
Door D-12: UNLOCKED FOR PASSAGE
Door D-13: SECURED
```

The interface should show:

- current state
- commanded state
- verified state
- owner
- timeout
- route effect
- camera relationship
- occupancy condition
- safety condition
- next action
- failure state

---

## Watcher Integration

Watcher Operators may manage maneuver actions within their assigned incident or zone.

They may:

- request route creation
- select relevant passage points
- review door states
- monitor guard progress
- confirm camera coverage
- request temporary unlock
- request route restriction
- report faults
- confirm arrival
- request release
- escalate conflicting conditions

A Watcher Operator should not silently inherit control of a door sequence.

Control transfer must be explicit and acknowledged.

---

## Relationship to the Coordinate Layer

Doors and passage points should be linked to facility coordinates.

Metadata may include:

- door identifier
- physical coordinate
- adjacent coordinates
- zone boundary
- direction of passage
- access classification
- camera coverage
- life-safety relevance
- emergency behavior
- current controller
- current state
- normal state
- applicable procedures

Example:

```text
Door D-12
Coordinate: BETA-F5-E
Connects: BETA-F5 ↔ BETA-F6
Zone Boundary: Service / Restricted
Camera Coverage: Camera-12
Life-Safety Relevance: Controlled
```

The coordinate layer identifies where the door is.

The maneuver layer defines how it may be used during an incident.

---

## Relationship to Patrol Displays

Patrol guards should normally receive only the minimum actionable route information.

Example:

```text
THETA:VIII ][ BETA-F6-NE
STAIRS
MOVE
```

The control room may manage door details in the background.

If a specific passage instruction is required, it may be shown separately:

```text
PASSAGE: D-12
```

The guard display should not expose unnecessary:

- door topology
- containment logic
- other guard locations
- incident causes
- sensitive zone names
- full maneuver sequences

---

## Door Control and Unauthorized Presence

The maneuver layer may be used when a subject’s presence or movement is inconsistent with:

- ticket scope
- credential state
- role
- expected route
- current zone
- device context
- escort state
- facility operational mode

The response should proceed through:

```text
Observe
→ Verify
→ Assess
→ Shape movement if authorized
→ Maintain separation
→ Contain or release
→ Escalate if required
```

Door control should provide time for human verification.

It should not independently determine:

- guilt
- intent
- identity
- threat level
- final disposition

---

## Communications

During Silent Security Mode, maneuver actions may be coordinated through:

- Master Watcher interface
- Watcher stations
- controlled tasking displays
- authenticated operator communications
- defined status indicators

Radio should be used when:

- safety requires it
- door status is uncertain
- a route is blocked
- a guard reports a hazard
- life safety is affected
- the maneuver state is unclear
- emergency responders require coordination

The maneuver panel must not create an assumption that silent operation is always preferable.

---

## Failure and Degraded Operations

The facility should define fallback behavior for:

- panel failure
- door-state sensor failure
- lock failure
- power failure
- communication loss
- incorrect door mapping
- unknown occupancy
- route obstruction
- camera failure
- Master Watcher failure
- Watcher Operator unavailability
- loss of authority
- emergency override
- synchronization failure

Possible fallback actions include:

- hold the current safe state
- use manual control
- restore standard access behavior
- suspend the maneuver sequence
- assign another operator
- use controlled radio
- use direct physical verification
- cancel guard routing
- escalate
- activate life-safety procedures

If door state cannot be verified:

> **The system must not assume that the door is secure, open, closed, or safe.**

An unresolved door state should be visible to all relevant operators.

---

## Degraded Door States

Possible states include:

```text
COMMAND UNKNOWN
SENSOR UNKNOWN
PHYSICAL STATE UNVERIFIED
CONTROL LOST
ROUTE UNCERTAIN
OCCUPANCY UNKNOWN
LIFE-SAFETY STATUS UNKNOWN
```

These states should trigger controlled review.

A maneuver sequence should pause or change when a required door, route, or safety condition becomes unknown.

---

## Recovery and Return to Normal

Recovery should include:

1. confirmation that the incident is contained or otherwise resolved
2. confirmation that active guard routes are complete or cancelled
3. confirmation that occupants are accounted for
4. review of temporary door states
5. verification of actual door conditions
6. restoration of approved normal states
7. confirmation that no temporary override remains active
8. reconciliation of camera, access, and door records
9. termination of maneuver mode
10. post-incident review

A door returning to its normal command state does not prove that the physical state is correct.

Physical verification remains necessary where risk requires it.

---

## Audit and Review

Every maneuver action should be auditable.

The audit record may include:

- incident reference
- operator identity
- station
- door or passage
- coordinate
- requested state
- commanded state
- sensor-reported state
- verified physical state
- reason
- route
- guard assignment
- time
- timeout
- extension
- control handoff
- dual approval
- life-safety override
- fault
- manual intervention
- restoration
- closure

Review should examine:

- whether door control was necessary
- whether the selected route was appropriate
- whether the guard was delayed or assisted
- whether containment created unnecessary risk
- whether any door remained in a temporary state
- whether operator workload affected control
- whether life-safety behavior worked
- whether the system produced false confidence
- whether the maneuver improved response

---

## Example Operational Sequence

1. A silent security alarm is detected at `BETA-F6-NE`.
2. The Watcher verifies the event through camera and access data.
3. The Master Watcher Operator confirms that life safety is clear.
4. The Incident Maneuver Panel becomes available.
5. Guard `THETA:VIII` is selected because closer guards are occupied.
6. The approved route is defined as `STAIRS`.
7. The guard receives:

   ```text
   THETA:VIII ][ BETA-F6-NE
   STAIRS
   MOVE
   ```

8. Door D-12 is temporarily unlocked for the authorized guard passage.
9. Door D-13 remains secured to restrict an unnecessary side route.
10. Camera coverage confirms the guard’s movement.
11. Door D-12 returns to its approved state after passage.
12. The guard arrives at `BETA-F6-NE`.
13. The display updates:

   ```text
   THETA:VIII
   BETA-F6-NE
   OBSERVE
   ```

14. The Watcher maintains observation.
15. The maneuver state is released, extended, or escalated according to incident conditions.
16. All door actions and task states are preserved for audit.

---

## Example: Uncertain Door State

1. A door command is issued for D-12.
2. The system reports that the sensor state is unknown.
3. The maneuver sequence pauses.
4. The Watcher is notified.
5. Camera coverage is checked.
6. A guard or authorized person may verify the door physically if safe.
7. The route is continued, changed, or cancelled.
8. The event is recorded as an unresolved door-state condition.

The system must not display D-12 as secure merely because a lock command was sent.

---

## Design Requirements

The Incident Maneuver and Door Control Model should satisfy the following requirements:

- maneuver controls are restricted to defined operational states
- all door actions require authorization
- current and requested states are visible
- commanded and verified states are distinguished
- every temporary state has an owner
- every temporary state has a timeout
- control handoffs require acknowledgement
- door and passage points map to coordinates
- routes consider life safety and occupancy
- anti-entrapment controls exist
- emergency release behavior is defined
- high-risk actions may require dual control
- guard routes and door sequences are auditable
- patrol displays expose minimum necessary information
- unknown door states are visible
- failure does not create false security
- life safety overrides containment
- normal operation is restored through verification
- temporary overrides are reviewed after incidents

---

## Relationship to the Wider Architecture

### Master Watcher Operations Model

Provides the central interface, operator roles, assignments, door visibility, and maneuver coordination.

### Incident Response

Defines when maneuver control may be activated and how it supports containment, escalation, and closure.

### Facility Chessboard Coordinate Layer

Provides coordinates for doors, routes, zones, guards, and incident locations.

### Incident Coordinate Wrist Display Model

Delivers the minimum route and task information to patrol guards.

### Context-Dependent Directional Coding

May reduce radio exposure while maneuver actions are coordinated.

### Surveillance Model

Provides camera verification of movement, passage, occupancy, and incident context.

### Degraded Operations

Defines fallback when doors, sensors, interfaces, communications, or authority are degraded.

### Passive Fire Resilience

Defines life-safety compatibility, fire behavior, egress, and emergency access.

### Alarm and Signaling Model

Defines the relationship between silent security alarms, maneuver activation, and life-safety signals.

### Recovery Model

Defines restoration of normal door states, routes, permissions, and operational legitimacy.

### Audit and Review

Preserves the history of door commands, routes, handoffs, overrides, and restoration.

---

## Limitations

This model does not by itself provide:

- certified access-control engineering
- fire and life-safety compliance
- complete anti-entrapment protection
- reliable occupancy detection
- accurate door-state sensing
- complete situational awareness
- identity assurance
- intent determination
- physical protection
- guaranteed containment
- replacement for qualified facility engineering
- replacement for emergency planning

Its effectiveness depends on:

- correctly engineered door systems
- reliable sensors
- accurate facility metadata
- trained operators
- clear authority
- tested procedures
- reliable emergency behavior
- life-safety integration
- disciplined maintenance
- regular exercises
- independent professional review

---

## Summary

The Incident Maneuver and Door Control Model adds a controlled passage-management layer to the High-Security Facility Concept.

It connects:

```text
Incident
→ Coordinate
→ Zone
→ Camera Context
→ Maneuver Panel
→ Door Sequence
→ Guard Route
→ Movement Constraint
→ Verification
→ Containment or Release
→ Recovery
→ Audit
```

The model allows authorized operators to:

- support guard movement
- temporarily shape passage corridors
- restrict uncontrolled routes
- coordinate doors with cameras and coordinates
- preserve time for verification
- maintain visible ownership
- restore normal operation after the incident

It does not authorize unrestricted remote locking or automatic judgment of people.

> **The maneuver layer shapes authorized passage conditions to support response and verification while preserving life-safety access and accountable human control.**

---

## Final Design Principles

> **Every door action is authorized, visible, time-limited, and auditable.**

> **Unknown door state must never be presented as secure.**

> **Containment creates time for verification; it does not determine guilt.**

> **The guard receives the route required for the task, while the control room retains the full maneuver context.**

> **Life safety overrides security containment.**

> **Every temporary door state must end in a verified and reviewable final state.**
