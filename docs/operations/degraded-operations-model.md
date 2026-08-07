# Degraded Operations Model – High-Security Facility Concept

> A controlled-continuity model for maintaining governability, interpretability, and accountable action when systems, trust assumptions, communications, personnel, or operating conditions are weakened but not fully collapsed.

---

## Document Information

| Field | Value |
|---|---|
| Document | Degraded Operations Model |
| Subject | Controlled continuity under reduced confidence |
| Type | Operations Model |
| Status | Conceptual |
| Scope | Degraded systems, weakened trust, communications compromise, personnel constraints, door and passage uncertainty, fallback, recovery, and life-safety interaction |
| Related Areas | Trust-State Model, Incident Response, Master Watcher Operations, Facility Coordinates, Incident Maneuver and Door Control, Offline OPSEC Verification, Recovery, Audit and Review |
| Parent Concept | High-Security Facility Concept |

---

## Purpose

This document defines how the facility should remain governable when normal systems, assumptions, communication paths, personnel availability, or trust conditions are weakened.

Degraded operations do not necessarily mean total failure.

They may occur when:

- a system is partially unavailable
- a data source is stale
- communication confidence is reduced
- a device is suspected of compromise
- the Master Watcher is unavailable
- a Watcher Operator becomes unavailable
- camera coverage is incomplete
- the offline OPSEC server cannot be reached
- a patrol display fails
- a door state cannot be verified
- personnel are overloaded
- multiple incidents compete for attention
- a facility enters a restricted operating state
- trust in a person, asset, zone, or process is reduced

The objective is to preserve:

- control
- interpretation
- accountability
- safe continuity
- explicit uncertainty
- controlled fallback
- life-safety compatibility
- recovery readiness

---

## Core Principle

> **Reduced confidence must not produce undefined behavior.**

When normal systems or trust assumptions are weakened, the facility must not:

- silently continue as if nothing changed
- grant broader access because verification failed
- assume a commanded state is a verified state
- allow operators to invent inconsistent procedures
- hide uncertainty
- rely on unrecorded exceptions
- permit informal shortcuts to become normal operations
- continue an outdated patrol or maneuver assignment without confirmation

Instead, the facility should move into a defined degraded state with:

- known limitations
- assigned authority
- restricted actions
- fallback procedures
- explicit communication
- enhanced logging
- recovery conditions

---

## Degraded Operations as a Trust State

Degradation is not only a technical condition.

It may represent reduced trust in:

- a person
- a credential
- a ticket
- a device
- a radio
- a camera
- a sensor
- a door
- a route
- a database
- a coordinate
- a Watcher Operator
- a procedure
- a physical zone
- an operational assumption

Reduced trust does not automatically prove malicious intent.

It means that normal assumptions may no longer be sufficient.

The appropriate response may include:

- verification
- observation
- restriction
- suspension
- replacement
- isolation
- reassignment
- escalation
- recovery review

---

## Degraded-State Classification

The facility may classify degraded conditions according to severity.

### Level 0 — Normal Operations

Normal systems, trust assumptions, and procedures are available.

- standard verification
- standard access
- standard communication
- standard surveillance
- normal door and passage control
- routine audit

### Level 1 — Local Degradation

A limited system, device, zone, or process is weakened while wider operations remain stable.

Examples:

- one camera unavailable
- one scanner offline
- one patrol display fails
- one access reader requires manual verification
- one door sensor is unavailable

Possible controls:

- local fallback
- increased observation
- manual confirmation
- targeted logging
- temporary restriction
- controlled reassignment

### Level 2 — Operational Degradation

Multiple systems, personnel, or assumptions are weakened.

Examples:

- several cameras unavailable
- Master Watcher partially degraded
- offline verification delayed
- communication confidence reduced
- multiple guards occupied
- repeated ticket or credential mismatches
- several door states are uncertain

Possible controls:

- reduced access
- stronger human review
- reassignment
- restricted movement
- increased Watcher control
- temporary suspension of non-essential activity
- manual route or door verification

### Level 3 — Facility-Control Degradation

The facility’s ability to interpret or govern normal activity is substantially reduced.

Examples:

- major surveillance loss
- control-room systems unavailable
- widespread communications compromise
- inability to verify identity or authorization reliably
- multiple zones affected
- insufficient authorized staff
- significant door or passage uncertainty
- loss of Master Watcher Operator authority

Possible controls:

- full-control posture
- closure of selected zones
- suspension of routine access
- manual control points
- controlled accountability
- emergency staffing
- escalation to senior authority
- restriction of non-essential movement

### Level 4 — Life-Safety or Critical Emergency

Life safety or critical survivability is affected.

Examples:

- fire
- smoke
- medical emergency
- immediate violence
- structural danger
- hazardous release
- evacuation
- rescue

Possible controls:

- emergency procedures
- explicit communication
- evacuation or shelter
- rescue coordination
- emergency responder access
- life-safety override of ordinary security abstractions

Life safety takes priority.

---

## Degraded-State Transition

A degraded state should be activated when:

- a required system becomes unavailable
- trust in a system or communication path falls below an accepted level
- identity or authorization cannot be verified normally
- personnel capacity falls below operational requirements
- multiple anomalies create uncertainty
- a control-room function becomes unreliable
- door or passage status cannot be confirmed
- a life-safety condition emerges

A transition should record:

- state level
- trigger
- time
- affected area
- affected systems
- authority
- restrictions
- fallback
- review interval
- recovery conditions

The facility should avoid informal “temporary” degradation that remains undocumented.

---

## Authority and Responsibility

Every degraded state must have a defined authority.

The responsible authority should be able to:

- activate the degraded state
- define affected areas
- assign restrictions
- approve fallback
- assign resources
- escalate
- authorize exceptions
- terminate the degraded state
- require post-event review

The role relationship is:

```text
Master Watcher Operator
→ facility-wide coordination and continuity

Watcher Operators
→ local observation, interpretation, and task control

Incident Commander
→ broader response posture and escalation

Patrol Guards
→ physical execution and local reporting
```

If the Master Watcher Operator becomes unavailable, responsibility must transfer explicitly to:

- a designated alternate Master Watcher Operator
- an Incident Commander
- an authorized senior Watcher Operator
- a documented manual coordination process

Responsibility must not transfer merely because someone opens the same interface.

---

## Master Watcher Degradation

The Master Watcher should display degraded-state information such as:

- unavailable systems
- stale data
- missing camera coverage
- unavailable Watcher Operators
- unavailable guards
- uncertain coordinates
- failed assignments
- communication status
- door-state uncertainty
- current fallback procedure
- current authority
- recovery conditions

If the Master Watcher is unavailable, the facility should use:

- approved printed floor plans
- controlled coordinate cards
- direct camera identifiers
- standard facility references
- manual assignment boards
- controlled verbal procedures
- manual event logging
- Watcher-to-Watcher confirmation

The fallback interface must not silently present stale or unverified information as current.

---

## Watcher Operator Degradation

If a Watcher station or operator becomes unavailable:

- assigned cameras must be reviewed
- responsibility must be transferred explicitly
- affected zones must be identified
- gaps in observation must be visible
- another Watcher Operator may be assigned
- camera-control ownership must be updated
- unresolved events must remain open
- guard tasks must be reviewed
- maneuver sequences must be paused or transferred where required

A camera feed being visible at another station does not automatically mean that responsibility has transferred.

---

## Patrol Guard Degradation

The facility should track patrol guard availability.

Possible states include:

```text
AVAILABLE
ASSIGNED
EN ROUTE
ON TASK
HOLDING
UNAVAILABLE
COMMUNICATION DEGRADED
EMERGENCY ENGAGED
```

If a guard becomes unavailable or cannot acknowledge a task:

1. the Watcher Operator is notified
2. the assignment is marked unresolved
3. the guard’s last known state is recorded
4. another guard may be selected
5. radio fallback may be used
6. the incident may be escalated

A replacement guard should not receive an unclear or outdated task.

---

## Wrist and Flashlight Display Failure

If a patrol display fails:

- the assignment should be marked uncertain
- the guard should not be assumed to have received an update
- the Watcher Operator should be notified
- the current task should be reviewed
- radio fallback may be activated
- direct Watcher guidance may be used
- the guard may be reassigned
- life-safety communication remains available

Possible causes include:

- battery failure
- display damage
- communication loss
- device loss
- device reassignment
- stale assignment
- incorrect coordinate
- synchronization failure
- suspected compromise

The system must not continue to rely on an unseen or unacknowledged task.

---

## Coordinate-System Degradation

If coordinate information becomes unreliable:

- affected coordinates should be marked uncertain
- stale metadata should be identified
- camera-coordinate mismatches should be exposed
- direct physical references may be used
- standard facility terminology may be restored
- patrol tasking may be held
- Watcher Operators may provide direct confirmation
- life-safety references remain explicit

A coordinate should not be treated as authoritative if:

- its floor mapping is uncertain
- its grid boundaries are wrong
- its local sector is unresolved
- camera coverage is stale
- the display is out of synchronization
- operators disagree about its meaning

---

## Communications Degradation

Communication degradation may include:

- suspected radio monitoring
- stolen radio
- channel compromise
- lost device
- outdated directional code
- failed acknowledgement
- conflicting messages
- excessive interference
- loss of trusted communication path

Possible controls include:

- Silent Security Mode
- Context-Dependent Directional Coding
- low-signature patrol displays
- reduced radio content
- controlled radio fallback
- replacement devices
- alternative authorized channels
- direct Watcher confirmation
- explicit emergency communication

If the active code set is uncertain:

> **Stop relying on coded direction and restore clear communication.**

---

## Contextual Authorization Degradation

If a ticket or authorization cannot be fully verified:

- high-risk access should be held or denied
- manual verification may be used where approved
- a named escort may be required
- second-person approval may be required
- route and duration may be restricted
- additional observation may be assigned
- the event must be logged

Failure of the ticket system must not create broader access.

The fallback hierarchy may be:

```text
Normal verification
        ↓
Manual controlled verification
        ↓
Second-person approval
        ↓
Restricted access or escort
        ↓
Hold or deny
        ↓
Escalate
```

---

## Offline OPSEC Server Degradation

If the offline OPSEC server is unavailable:

- automatic high-risk verification is suspended
- QR presentation alone is insufficient
- identity must be checked through approved fallback
- paper or controlled reference may be used if authorized
- a named escort may be required
- second-person approval may be required
- access may be restricted in time and route
- enhanced logging is required
- normal verification must be restored and reconciled afterward

If fallback conditions cannot be met:

```text
Hold or deny
```

---

## Door and Passage Degradation

Door and passage states must distinguish between:

- commanded state
- sensor-reported state
- verified physical state
- unknown state

Examples:

```text
Commanded: LOCKED
Sensor: UNKNOWN
Verification: UNRESOLVED
```

or:

```text
Commanded: UNLOCKED
Sensor: CLOSED
Verification: CONFIRMED
```

If a door or passage state cannot be trusted:

- maneuver sequences should pause
- the affected route should be marked uncertain
- the Watcher Operator should be notified
- camera coverage should be checked
- physical verification may be required
- another route may be selected
- the door may be returned to an approved safe state where appropriate
- the incident may be escalated

The facility must not assume that a sent command equals a verified physical result.

> **Unknown door state must never be presented as secure.**

---

## Maneuver-Panel Degradation

If the Incident Maneuver Panel becomes unavailable:

- temporary door states must be reviewed
- active routes must be identified
- current owners must be confirmed
- guard tasking must be checked
- manual door procedures may be activated
- new maneuver sequences may be suspended
- life-safety behavior must remain available
- all manual actions must be logged

If the panel displays stale or conflicting information, operators should use:

- direct sensor confirmation
- camera verification
- physical confirmation
- controlled radio
- approved manual records

A failed maneuver interface must not create false confidence that doors remain under control.

---

## Data and Metadata Degradation

The facility should identify when data becomes:

- stale
- incomplete
- conflicting
- unavailable
- corrupted
- unauthenticated
- out of sequence
- unsynchronized

Affected data may include:

- identity references
- trusted photographs
- ticket records
- revocation data
- zone permissions
- camera metadata
- coordinate mappings
- door metadata
- device assignments
- asset records
- incident states
- guard availability

The system should expose data confidence rather than present uncertainty as certainty.

---

## Access and Movement Under Degradation

When normal trust or observation is reduced, the facility may:

- restrict new access
- pause non-essential movement
- close selected zones
- require escorts
- require two-person approval
- increase camera observation
- use manual checkpoints
- reduce permitted routes
- suspend tickets
- isolate devices
- increase logging
- shift to full-control posture
- restrict temporary door control
- require explicit passage authorization

Movement should remain purposeful and reviewable.

Informal shortcuts should not become accepted merely because systems are degraded.

---

## Control-Flow Principle

During degraded operations:

```text
Reduced confidence
        ↓
More explicit control
        ↓
Less discretionary movement
        ↓
Greater human verification
        ↓
More visible accountability
```

Degradation should not produce:

```text
Reduced confidence
        ↓
Less control
        ↓
More informal behavior
```

---

## Human Factors

Degraded operations increase cognitive and operational load.

The facility should account for:

- operator fatigue
- repeated manual checks
- queue formation
- alert overload
- communication pressure
- conflicting instructions
- staffing shortages
- shift changes
- unfamiliar fallback procedures
- pressure to restore normal operation too quickly
- repeated door-state uncertainty
- guard tasking conflicts

Controls may include:

- relief staffing
- task rotation
- simplified status vocabulary
- clearly assigned authority
- visible fallback state
- decision support
- mandatory handoffs
- shorter task instructions
- explicit uncertainty
- post-event review

Fallback procedures should be simpler than the normal system where possible.

---

## Communication During Degraded Operations

Communication should be:

- explicit
- short
- role-aware
- state-aware
- auditable
- consistent with life-safety requirements

The facility should identify:

- active communication mode
- available channels
- trusted channels
- compromised channels
- fallback channels
- emergency channels
- recipients who have acknowledged the state

If uncertainty exists about who received an instruction, the system should not assume delivery.

---

## Audit and Review

The degraded-state record should include:

- trigger
- state level
- authority
- affected systems
- affected zones
- affected people or assets
- restrictions
- fallback procedures
- manual decisions
- task assignments
- device failures
- communication mode
- access decisions
- door and passage actions
- maneuver-panel state
- overrides
- review intervals
- recovery conditions
- termination
- post-event findings

Review should examine:

- whether the state was activated early enough
- whether restrictions were proportionate
- whether fallback increased workload
- whether people improvised
- whether communications remained clear
- whether access control became too permissive or too restrictive
- whether temporary door states remained controlled
- whether life-safety compatibility was preserved
- whether recovery was declared too early
- whether the architecture should change

---

## Recovery Conditions

A degraded state should not end merely because a system appears to function again.

Recovery should require confirmation that:

- affected systems are trusted or replaced
- data is synchronized
- camera and coordinate mappings are verified
- door and passage states are verified
- communications are trusted
- ticket and revocation records are current
- patrol devices are accounted for
- assignments are reconciled
- temporary access restrictions are reviewed
- operators understand the restored state
- unresolved incidents remain assigned
- an authorized person approves return

Recovery may occur gradually:

```text
Degraded
→ Stabilizing
→ Validating
→ Controlled Restoration
→ Normal Operations
```

---

## Life-Safety Compatibility

Life safety takes priority over degraded security abstractions.

During:

- fire
- smoke
- medical emergency
- immediate violence
- evacuation
- rescue
- structural danger
- hazardous release

the facility should:

- use explicit communication
- use actual floor and room references
- preserve emergency access
- allow radio use
- override silent tasking where necessary
- override coded directional language
- follow approved emergency door behavior
- coordinate with responders
- log emergency overrides
- review security consequences afterward

A degraded security system must never delay rescue or evacuation.

---

## Example: Patrol Display Failure

1. A silent task is assigned to `THETA:VIII`.
2. The patrol display does not acknowledge delivery.
3. The Watcher Operator marks the assignment unresolved.
4. The Master Watcher displays the failed task state.
5. The Watcher checks camera coverage and guard location.
6. A controlled radio fallback is attempted.
7. If the guard cannot be reached, another guard is selected.
8. The original assignment is cancelled or marked uncertain.
9. The event is recorded for review.

---

## Example: Master Watcher Failure

1. The Master Watcher becomes unavailable.
2. The control room enters a defined degraded state.
3. Watcher Operators use approved fixed floor plans and coordinate references.
4. Camera assignments are confirmed manually.
5. Patrol tasking uses controlled displays or radio fallback.
6. New high-risk activity is restricted if spatial confidence is insufficient.
7. Temporary door actions are paused or manually verified.
8. A temporary manual assignment record is maintained.
9. System restoration is validated.
10. Records are reconciled.
11. Normal operations resume only after authorization.

---

## Example: Offline Verification Failure

1. A high-risk ticket is presented.
2. The offline OPSEC server is unavailable.
3. Automatic high-risk verification is suspended.
4. Identity and purpose are reviewed through the approved fallback.
5. Escort and second-person approval are required.
6. Access is restricted or held.
7. The event is manually logged.
8. The system is restored.
9. The fallback decision is reconciled and reviewed.

---

## Example: Door-State Uncertainty

1. A maneuver sequence requires Door D-12.
2. The system reports that the sensor state is unknown.
3. The route is marked uncertain.
4. The Watcher Operator is notified.
5. Camera coverage and occupancy are reviewed.
6. A qualified person may verify the door physically if safe.
7. The route is continued, changed, or cancelled.
8. The action and uncertainty are recorded.
9. Temporary states are reviewed during recovery.

---

## Design Requirements

The Degraded Operations Model should satisfy the following requirements:

- degraded states are defined before incidents occur
- state levels are understandable
- triggers are documented
- authority is assigned
- authority continuity is defined
- affected systems and zones are visible
- uncertainty is exposed
- failure does not increase trust automatically
- fallback procedures exist for critical systems
- patrol display failure has defined handling
- Master Watcher failure has defined handling
- Watcher Operator failure has defined handling
- offline verification failure has defined handling
- communication degradation has defined handling
- coordinate uncertainty is visible
- door-state uncertainty is visible
- maneuver-panel failure has defined handling
- high-risk access becomes more controlled, not less
- manual decisions are auditable
- human workload is monitored
- life safety overrides security abstractions
- recovery conditions are explicit
- restoration is validated before normal operation
- unresolved issues remain assigned

---

## Relationship to the Wider Architecture

### Trust-State Model

Defines how reduced confidence and changing trust affect operational state.

### Incident Response

Defines how degraded conditions are detected, classified, contained, escalated, and reviewed.

### Master Watcher Operations

Defines how control-room overview, Master Watcher Operators, Watcher Operators, patrol tasking, and camera coordination operate during degradation.

### Facility Chessboard Coordinate Layer

Provides stable spatial references and controlled fallback coordinates.

### Incident Coordinate Wrist Display

Defines how patrol tasking behaves when displays, devices, or communication paths are degraded.

### Incident Maneuver and Door Control

Defines fallback when doors, sensors, routes, or passage controls are weakened.

### Context-Dependent Directional Coding

Provides a controlled communication layer when radio trust is reduced.

### Context-Bound Facility Authorization Ticket

Defines authorization conditions that may be restricted or suspended during degraded operation.

### Offline OPSEC Verification

Defines high-risk ticket verification and fallback when the offline server is unavailable.

### Recovery Model

Defines the restoration of trust, control, and operational legitimacy after the degraded state.

### Audit and Review

Preserves the complete history of degraded decisions and fallback actions.

---

## Limitations

This model does not by itself provide:

- guaranteed continuity
- complete technical resilience
- reliable communications
- complete identity assurance
- automatic decision-making
- certified door-control behavior
- life-safety compliance
- protection against insider misuse
- replacement for professional continuity planning
- replacement for emergency planning
- a finished implementation procedure

Its effectiveness depends on:

- realistic fallback design
- trained operators
- adequate staffing
- reliable manual procedures
- tested communications
- accurate facility references
- disciplined authority
- engineered door and life-safety systems
- regular exercises
- independent review
- integration with life-safety planning

---

## Summary

The Degraded Operations Model ensures that weakened systems and reduced trust do not produce uncontrolled behavior.

It provides a structured response to:

- system failure
- communication compromise
- device loss
- stale data
- personnel shortage
- coordinate uncertainty
- offline verification failure
- Master Watcher failure
- Watcher Operator failure
- patrol display failure
- door-state uncertainty
- maneuver-panel failure
- identity or authorization uncertainty
- operational disruption
- life-safety interaction

The model follows:

```text
Degradation detected
        ↓
State classified
        ↓
Authority assigned
        ↓
Restrictions applied
        ↓
Fallback activated
        ↓
Actions logged
        ↓
Systems and trust validated
        ↓
Controlled restoration
        ↓
Review
```

The central principle is:

> **When normal trust, systems, or assumptions are weakened, the facility must become more explicit, more controlled, and more accountable—not more informal.**

---

## Final Design Principles

> **Reduced confidence must not produce undefined behavior.**

> **Failure of the trust system must not create an automatic increase in trust.**

> **Degraded operations should increase explicit control, not informal discretion.**

> **Unknown door state must never be presented as secure.**

> **Life safety overrides security abstractions.**

> **Normal operations resume only after trust, data, systems, authority, and temporary states have been validated.**
