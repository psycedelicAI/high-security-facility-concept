# Incident Coordinate Wrist Display Model – High-Security Facility Concept

> A low-signature, incident-only tasking model in which authorized patrol personnel receive operational coordinates, routes, task states, and controlled passage instructions through authenticated wrist-worn or patrol-equipment displays during defined security incidents.

---

## Document Information

| Field | Value |
|---|---|
| Document | Incident Coordinate Wrist Display Model |
| Subject | Silent incident tasking, coordinate delivery, and patrol execution |
| Type | Supporting Operations Model |
| Status | Conceptual |
| Scope | Patrol guards, silent-security incidents, coordinate delivery, route tasking, passage support, task states, and radio reduction |
| Related Areas | Facility Chessboard Coordinate Layer, Master Watcher Operations, Incident Response, Incident Maneuver and Door Control, Context-Dependent Directional Coding, Degraded Operations, Human Factors |
| Parent Concept | High-Security Facility Concept |

---

## Purpose

This document defines a low-signature tasking layer for patrol guards during selected security incidents.

The model allows authorized personnel to receive:

- operational coordinates
- local grid sectors
- movement routes
- task states
- assignment updates
- passage instructions
- cancellation or return instructions
- arrival and observation states

through a controlled display rather than relying primarily on spoken radio communication.

Possible display endpoints include:

- wrist-worn e-paper displays
- wrist-worn low-power displays
- flashlight-mounted LED displays
- narrow patrol-equipment displays
- authenticated handheld displays
- haptic tasking devices

The purpose is to reduce unnecessary radio exposure while preserving:

- task clarity
- operator control
- acknowledgement
- movement verification
- arrival confirmation
- auditability
- emergency fallback
- life-safety compatibility

---

## Core Principle

> **During a defined silent-security incident, patrol personnel should receive the minimum actionable task information through the least observable suitable channel.**

The display should provide enough information for the guard to act correctly without exposing the full incident context.

A guard may need to know:

- who they are operationally
- where they are assigned
- which route to use
- what task state applies
- whether a passage condition is relevant

They do not necessarily need to know:

- the complete incident narrative
- all affected zones
- the identity of other personnel
- the location of other guards
- the reason for the alarm
- the entire facility map
- sensitive technical details
- the full door-control sequence
- other response priorities

---

## Operational Problem

Open radio communication during a covert security incident may reveal:

- the approximate incident location
- the responding guard
- the guard’s destination
- the route being used
- the existence of a security response
- the structure of the facility
- the movement of security personnel
- the current operational priority
- the use of specific passage routes

A low-signature display can reduce the need to communicate this information verbally.

Without a display, a task might be spoken as:

```text
Control to Guard 8:
Proceed to Beta-F6, northeast sector, via the stairs and observe.
```

With the display, the guard may receive:

```text
THETA:VIII ][ BETA-F6-NE
STAIRS
OBSERVE
```

The display does not eliminate communication.

It reduces unnecessary exposure of task details over shared audio channels.

---

## Scope

The model applies to defined operational states such as:

- silent security alarm
- covert, non-life-threatening security incident
- suspected communications monitoring
- suspected radio compromise
- discreet observation task
- controlled patrol reassignment
- low-signature response
- movement requiring limited disclosure
- temporary passage coordination
- controlled route support

The model does not replace normal communication during:

- fire
- smoke
- medical emergency
- immediate violence
- evacuation
- rescue
- structural danger
- hazardous release
- emergency responder coordination
- any situation where clear speech is required for safety

---

## Relationship to the Wider Architecture

The Incident Coordinate Wrist Display Model connects:

```text
Silent Security Alarm
        ↓
Master Watcher Operator
        ↓
Watcher Operator Assignment
        ↓
Guard Call Sign
        ↓
Operational Coordinate
        ↓
Route and Task State
        ↓
Optional Passage Support
        ↓
Silent Task Execution
        ↓
Movement Verification
        ↓
Arrival or Escalation
        ↓
Audit and Review
```

It uses the following existing layers:

- the Facility Chessboard Coordinate Layer for position and local sector
- the Fixed Security-Center Orientation model for spatial consistency
- the Master Watcher Operations Model for assignment and oversight
- Context-Dependent Directional Coding for selected communications states
- Incident Response for incident classification and task lifecycle
- Incident Maneuver and Door Control for passage support
- Degraded Operations for fallback
- Recovery for closure and reconciliation
- Audit and Review for reconstructability

---

## Display Assignment Format

A standard guard assignment is expressed as:

```text
[Call Sign] ][ [Operational Coordinate]
```

Example:

```text
THETA:VIII ][ BETA-F6-NE
```

This is interpreted as:

```text
Call Sign: THETA:VIII
Assigned Coordinate: BETA-F6-NE
```

The separator has a deliberate visual function:

```text
THETA:VIII ][ BETA-F6-NE
```

The `][` delimiter separates:

- guard identity
- assigned operational position

The display may show additional task information below the primary assignment.

---

## Call-Sign Structure

A guard call sign uses:

```text
[Greek Designation]:[Roman Guard Number]
```

Example:

```text
THETA:VIII
```

The call sign contains:

- a Greek operational designation
- a colon
- a Roman-numbered guard identifier

The Greek designation may identify:

- assigned floor group
- patrol group
- operational sector
- shift group
- temporary assignment group

The Roman number identifies the guard within that operational group.

The call sign should be understood as an operational identity, not as the guard’s permanent personal identity.

---

## Call-Sign Examples

```text
ALPHA:I
BETA:IV
GAMMA:VII
THETA:VIII
```

The call sign does not necessarily mean that the guard is currently located on the named floor.

For example:

```text
THETA:VIII ][ BETA-F6-NE
```

means that the guard assigned to the Theta group, number VIII, has been tasked to Beta floor, grid square F6, local sector NE.

The guard’s assigned group and current task location are separate fields.

---

## Coordinate Structure

The operational coordinate uses:

```text
[Operational Floor]-[Grid Square]-[Local Sector]
```

Example:

```text
BETA-F6-NE
```

This represents:

- `BETA` — operational floor designation
- `F6` — facility grid square
- `NE` — local sector within the square

The coordinate is defined by the Facility Chessboard Coordinate Layer.

---

## Local Sector Precision

Each grid square may use a controlled 3×3 local structure:

```text
NW | N  | NE
---+----+---
W  | C  | E
---+----+---
SW | S  | SE
```

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

The sector boundaries must be defined in the facility’s controlled coordinate reference.

The guard should not be expected to interpret a sector subjectively during a live event.

If the local sector cannot be determined reliably:

- use the main grid coordinate
- mark the sector as unresolved
- request clarification
- use a controlled room, camera, or door reference
- do not guess

---

## Information Hierarchy

The display should present information in the following order:

1. guard call sign
2. assigned coordinate
3. route instruction
4. task state
5. passage note where required
6. update or acknowledgement state

Example:

```text
THETA:VIII
BETA-F6-NE
STAIRS
MOVE
```

The device should avoid displaying unnecessary context.

The guard should receive:

> **The correct task, not the entire incident.**

---

## Route Instructions

A route instruction may identify the intended movement method or path.

Examples:

```text
STAIRS
ELEVATOR
ROUTE-A
ROUTE-B
SERVICE-PATH
NORTH-STAIR
```

Route instructions should be defined within the facility’s operational procedures.

A route instruction must not conflict with:

- life-safety requirements
- active evacuation
- emergency responder movement
- current physical hazards
- access restrictions
- updated control-room instructions
- current door or passage state

The route may be changed while the task is active.

---

## Passage Support

The control room may manage passage conditions in the background through the Incident Maneuver Panel.

The guard-facing display should normally remain minimal:

```text
THETA:VIII
BETA-F6-NE
STAIRS
MOVE
```

If a specific passage instruction is necessary, it may be shown separately:

```text
PASSAGE: D-12
```

The display should not expose the full door sequence unless required by procedure.

The control room may retain:

- door identifiers
- passage sequence
- lock and unlock state
- camera coverage
- occupancy information
- timeout
- owner
- safety conditions

The guard should receive only the information needed to move safely and correctly.

---

## Task States

Task states describe what the guard should currently do.

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

The facility should define a controlled vocabulary and avoid synonyms that may create confusion.

### `MOVE`

Proceed toward the assigned coordinate using the displayed route.

### `OBSERVE`

Remain at or near the assigned coordinate and observe according to procedure.

### `HOLD`

Remain in a controlled position and await further instruction.

### `WAIT`

Do not continue until the assignment is updated or confirmed.

### `RETURN`

Return through the defined route or to the assigned safe position.

### `CANCEL`

The current assignment is no longer active.

### `ESCALATE`

Contact the appropriate control function or transition to the defined escalation procedure.

Task states should be displayed in a clear, stable format.

---

## Assignment Lifecycle

A silent task should have a defined lifecycle.

### 1. Created

A Watcher Operator or authorized control-room operator creates the assignment.

### 2. Issued

The assignment is sent to the authenticated guard device.

### 3. Received

The device confirms that the assignment was delivered.

### 4. Acknowledged

The guard confirms receipt through an approved discreet interaction.

### 5. En Route

The guard begins movement toward the assigned coordinate.

### 6. Arrived

The system or Watcher Operator confirms that the guard has reached the relevant area.

### 7. Active Task

The guard performs the assigned task, such as observation or hold.

### 8. Updated

The assignment may receive a new coordinate, route, passage note, or task state.

### 9. Completed

The task is completed and closed.

### 10. Cancelled

The task is withdrawn before completion.

### 11. Escalated

The task requires additional response, communication, or control.

---

## Assignment State Examples

```text
ASSIGNED
ACKNOWLEDGED
EN ROUTE
ARRIVED
OBSERVING
HOLDING
UPDATED
COMPLETED
CANCELLED
ESCALATED
UNRESOLVED
```

These states may be displayed on control-room systems even if only a smaller subset is shown to the guard.

The guard display should remain minimal.

---

## Silent Tasking Workflow

A typical workflow may be:

1. A silent security alarm is activated.
2. The Master Watcher Operator identifies the affected coordinate or zone.
3. A Watcher Operator reviews the camera and incident context.
4. Available patrol guards are assessed.
5. The nearest suitable guard is selected, unless already occupied.
6. The assignment is created.
7. The assignment is sent to the guard’s authenticated device.
8. The guard acknowledges discreetly.
9. The guard receives the coordinate and route.
10. Optional passage support is activated where authorized.
11. The guard moves without unnecessary radio transmission.
12. Cameras and sensors support movement verification.
13. The Watcher Operator confirms arrival or identifies a delay.
14. The guard performs the task.
15. The assignment is completed, updated, cancelled, or escalated.
16. The event is preserved for audit and recovery.

---

## Example: Reassignment from Another Floor

A guard assigned to Theta may be required to respond to a Beta-floor incident because closer guards are already occupied.

The display may show:

```text
THETA:VIII ][ BETA-F6-NE
STAIRS
MOVE
```

The interpretation is:

- operational call sign: `THETA:VIII`
- destination: `BETA-F6-NE`
- route: stairs
- current task: move

The display does not need to explain why the guard was selected.

That decision remains visible to:

- the Watcher Operator
- the Master Watcher Operator
- the assignment system
- the audit record

---

## Radio-Silent Tasking

During Silent Security Mode, the display may reduce the need for spoken radio traffic.

The guard may receive:

```text
THETA:VIII ][ BETA-F6-NE
```

without a voice transmission stating:

- the incident location
- the guard’s identity
- the destination
- the route
- the response priority
- the passage sequence

This reduces the information value of intercepted radio traffic.

Radio remains available for:

- life-safety events
- unexpected contact
- medical emergencies
- unclear instructions
- escalation
- display failure
- communication failure
- emergency responder coordination

> **Radio silence is a defined operating mode, not a prohibition on speaking when clarity or safety requires it.**

---

## Acknowledgement

Silent tasking must not mean unconfirmed tasking.

The system should support acknowledgement through:

- physical button
- discreet touch action
- short gesture
- haptic confirmation
- authenticated device signal
- controlled movement confirmation

The acknowledgement should confirm that:

- the assignment was delivered
- the intended device received it
- the guard accepted or recognized it
- the task state is known

If acknowledgement is not received within a defined period:

1. the Watcher Operator is notified
2. the Master Watcher displays the unresolved assignment
3. another guard may be selected
4. a controlled radio fallback may be used
5. the incident may be escalated if required

---

## Movement Verification

The control room should be able to determine whether the guard is:

- stationary
- moving
- delayed
- following the expected route
- approaching the coordinate
- at the assigned coordinate
- no longer responding
- deviating from the expected path
- blocked by a passage condition

Verification may use:

- cameras
- access events
- controlled location signals
- device state
- Watcher Operator confirmation
- direct observation
- facility sensors
- door and passage events

Movement verification should support the task, not become an unjustified source of continuous personal surveillance outside the defined operational purpose.

---

## Arrival Confirmation

Arrival may be confirmed through:

- camera observation
- access event
- controlled device signal
- local acknowledgement
- Watcher Operator confirmation
- direct operator confirmation
- passage completion

The system should distinguish between:

```text
Estimated arrival
```

and:

```text
Confirmed arrival
```

An assignment should not automatically be marked complete merely because a device appears near the coordinate.

---

## Master Watcher Integration

The Master Watcher Operator should provide the wider operational picture.

It may show:

- guard call sign
- assigned coordinate
- local sector
- current observed coordinate
- route
- passage condition
- task state
- acknowledgement state
- movement state
- arrival state
- assigned Watcher Operator
- camera coverage
- incident reference
- communication mode
- device status
- door or passage status
- life-safety status

The Master Watcher Operator should be able to:

- create assignments
- approve or coordinate assignments
- update coordinates
- change routes
- change task states
- cancel assignments
- reassign guards
- review acknowledgement
- monitor arrival
- record task notes
- coordinate with the Incident Maneuver Panel

The Master Watcher should not expose more information to the guard than is necessary for the assigned task.

---

## Watcher Operator Integration

The assigned Watcher Operator should manage the task within the relevant incident or zone context.

The Watcher Operator may:

- select the guard
- review guard availability
- assign the coordinate
- define the route
- define the task state
- request passage support
- observe movement
- confirm arrival
- update the assignment
- request acknowledgement
- cancel the task
- escalate the event
- document the outcome

The Watcher Operator should understand why the guard was assigned, even if the guard display shows only the task.

---

## Guard Availability

The system should maintain an operational availability state for guards.

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

A guard should not receive a new silent task without considering:

- current assignment
- current location
- task state
- physical condition
- communication state
- equipment status
- access permissions
- current incident priority
- route availability

A guard who is already engaged may be reassigned only through an authorized process.

---

## Display Endpoints

### Wrist-Worn Display

A wrist-worn display may provide:

- low-signature tasking
- persistent short messages
- haptic notification
- discreet acknowledgement
- hands-free access
- e-paper or low-power visual output

It should be readable while:

- standing
- moving
- wearing gloves
- operating in low-light conditions
- carrying patrol equipment

### Flashlight-Mounted Display

A flashlight-mounted display may provide:

- short coordinate output
- route indication
- task-state display
- quick-glance interaction
- integration with existing patrol equipment

Example:

```text
THETA:VIII ][ BETA-F6-NE
```

or:

```text
BETA-F6-NE
OBSERVE
```

The flashlight display should not become a full operational terminal.

### Other Controlled Endpoints

The model may support:

- secured handheld displays
- protected patrol tablets
- haptic devices
- authenticated wearable displays
- other low-signature operational endpoints

The endpoint may change, but the tasking logic should remain consistent.

---

## Display Design

The display should prioritize:

- high contrast
- minimal content
- readable typography
- stable coordinate visibility
- clear task state
- low cognitive load
- visible update state
- low power consumption
- glove-compatible interaction
- clear cancellation
- clear stale-state indication

A static coordinate is generally preferable to continuously scrolling text during movement.

The display should not show unnecessary:

- incident details
- personal information
- sensitive zone descriptions
- other guard locations
- facility-wide maps
- technical system information
- complete door-control sequences
- unrelated task assignments

---

## Device Authentication and Assignment

Each display endpoint should be associated with:

- a specific device identity
- an assigned guard
- an operational call sign
- a current shift
- a current assignment
- a trusted communication relationship

The system should know:

```text
Which guard received the assignment?
Which device received it?
When was it delivered?
Was it acknowledged?
Was the device reassigned?
Did the guard arrive?
Was the task completed?
Was the task cancelled?
```

If a device is:

- lost
- stolen
- handed to another person
- damaged
- disconnected
- tampered with

the active assignment should be reviewed, cleared, or reassigned.

A displayed call sign must not be treated as proof of identity by itself.

---

## Call-Sign and Coordinate Syntax

The standard display syntax is:

```text
[Greek Designation]:[Roman Guard Number] ][ [Floor]-[Grid]-[Local Sector]
```

Example:

```text
THETA:VIII ][ BETA-F6-NE
```

The syntax is interpreted as:

```text
Call Sign: THETA:VIII
Floor: BETA
Grid Square: F6
Local Sector: NE
```

The notation uses:

- `:` between Greek designation and Roman guard number
- `][` between guard identity and assigned coordinate
- `-` between coordinate components

The display may use spacing for readability:

```text
THETA:VIII ][ BETA-F6-NE
```

An internal machine representation may use a structured format, but the human-facing display should remain consistent.

---

## Separation from Directional Coding

The coordinate system remains fixed.

Context-Dependent Directional Coding may alter the meaning of spoken directional terms during a defined covert security state.

These are separate layers:

```text
Fixed coordinate:
BETA-F6-NE

Contextual spoken direction:
May be remapped during Silent Security Mode
```

The guard display should normally show the trusted coordinate and local sector.

It should not silently change the meaning of `BETA-F6-NE`.

If a route requires additional directional information, that information should be delivered through a separately defined and clearly marked field.

---

## Radio Fallback

The device reduces radio exposure but does not eliminate radio capability.

Radio fallback should be available when:

- the display is unreadable
- the coordinate is unclear
- the route is blocked
- a passage is unavailable
- the guard encounters a hazard
- the incident changes
- the task becomes life-threatening
- the guard requires medical assistance
- the device fails
- the control room loses confidence
- emergency responders need direct coordination

The guard should be trained that safety and clarity override radio-silence requirements.

---

## Life-Safety Override

If the event becomes life-threatening, the silent-security tasking layer is subordinate to life safety.

Triggers may include:

- fire
- smoke
- medical emergency
- immediate violence
- structural danger
- evacuation
- rescue
- hazardous release
- emergency responder direction

In such conditions:

- explicit emergency communication takes priority
- standard floor and room references remain available
- actual physical directions may be used
- radio silence may be broken immediately
- emergency instructions override task states
- the guard may abandon or change the silent task
- door and passage instructions follow approved emergency behavior
- the event is logged and reviewed afterward

> **No silent tasking protocol should prevent a guard from communicating a life-safety emergency.**

---

## Failure and Degraded Operations

The facility should define fallback behavior for:

- display failure
- unreadable display
- device loss
- battery failure
- wireless communication failure
- assignment synchronization failure
- coordinate metadata failure
- incorrect coordinate
- route obstruction
- passage obstruction
- guard unavailability
- Master Watcher failure
- Watcher station failure
- camera verification failure
- door-state uncertainty
- life-safety override

Possible fallback actions include:

- controlled radio communication
- direct Watcher Operator guidance
- manual coordinate reference
- approved printed facility plan
- fixed physical reference
- temporary hold
- task cancellation
- guard reassignment
- escalation

The system should not silently continue an outdated assignment when confidence in the task state is lost.

---

## Audit and Review

The system should record:

- assignment creation
- assigning operator
- receiving guard
- device identity
- call sign
- coordinate
- local sector
- route
- passage reference where used
- task state
- delivery time
- acknowledgement time
- movement state
- arrival state
- task updates
- reassignment
- cancellation
- escalation
- radio fallback
- device failure
- passage obstruction
- life-safety override
- task completion
- incident association

The record should preserve the original assignment and subsequent changes.

Review should examine:

- delayed acknowledgement
- repeated reassignment
- route deviations
- device failures
- unclear coordinates
- unnecessary radio exposure
- missed arrivals
- operator workload
- guard workload
- task conflicts
- passage-related delays
- false or stale assignments
- life-safety interruptions

---

## Example Operational Sequences

### Silent Assignment

```text
Silent alarm
    ↓
Master Watcher Operator selects BETA-F6-NE
    ↓
Watcher Operator selects available THETA:VIII
    ↓
Display receives:

THETA:VIII ][ BETA-F6-NE
STAIRS
MOVE
    ↓
Guard acknowledges
    ↓
Optional passage support is activated
    ↓
Guard moves silently
```

### Arrival and Observation

```text
THETA:VIII
BETA-F6-NE
OBSERVE
```

The Watcher Operator confirms arrival through:

- camera
- local event
- device state
- direct observation
- passage completion

### Assignment Update

```text
THETA:VIII
BETA-F6-SE
HOLD
```

The guard remains in or moves to the updated sector according to procedure.

### Cancellation

```text
THETA:VIII
CANCEL
```

The control system records the cancellation and provides the next defined instruction.

### Return

```text
THETA:VIII
RETURN
```

The guard follows the approved return procedure.

### Passage Obstruction

```text
THETA:VIII
BETA-F6-NE
ROUTE BLOCKED
HOLD
```

The Watcher Operator reviews the route and provides an update or fallback.

---

## Design Requirements

The Incident Coordinate Wrist Display Model should satisfy the following requirements:

- display activation is limited to defined operational states
- silent tasking is authorized and auditable
- every task includes a call sign and operational coordinate
- coordinate syntax remains consistent
- local-sector precision is supported
- route and task state are distinguishable
- passage support is optional, controlled, and life-safety compatible
- acknowledgement is available
- movement and arrival can be verified
- device identity is controlled
- assignments are visible to the Watcher Operator and Master Watcher Operator
- stale assignments can be cancelled or replaced
- device loss triggers review
- radio remains available as fallback
- life-safety communication overrides silent tasking
- display content follows minimum-necessary disclosure
- guard availability is tracked
- handoffs and reassignments are logged
- degraded-mode procedures exist
- operator and guard workload are reviewed
- the system does not rely solely on the display for safety
- passage obstruction has defined handling

---

## Limitations

This model does not by itself provide:

- complete communications security
- guaranteed radio silence
- accurate location at all times
- reliable identity assurance
- complete situational awareness
- protection against device compromise
- protection against insider misuse
- certified passage-control engineering
- life-safety compliance
- guaranteed task completion
- replacement for trained patrol procedures
- replacement for professional human-factors validation

Its effectiveness depends on:

- reliable task distribution
- authenticated devices
- accurate facility coordinates
- trained guards
- functioning Watcher Operators
- reliable camera and sensor context
- clear fallback procedures
- engineered passage systems
- regular exercises
- disciplined assignment management

---

## Relationship to the Wider Architecture

### Facility Chessboard Coordinate Layer

Provides the floor, grid, local-sector, door, and route references used by the display.

### Master Watcher Operations Model

Defines assignment, oversight, guard availability, movement verification, and operational control.

### Incident Response

Defines when silent tasking is activated and how assignments support containment and escalation.

### Incident Maneuver and Door Control

Provides optional passage support and controlled door-state coordination.

### Context-Dependent Directional Coding

Provides a separate communications-security layer during selected covert incidents.

### Degraded Operations

Defines behavior when displays, devices, communications, routes, or passage systems are degraded.

### Passive Fire Resilience

Defines life-safety behavior, emergency access, and evacuation compatibility.

### Recovery Model

Defines task closure, device accountability, assignment reconciliation, and restoration.

### Audit and Review

Preserves the history of tasking, movement, passage support, fallback, and closure.

---

## Summary

The Incident Coordinate Wrist Display Model provides a low-signature way to assign and update patrol tasks during selected security incidents.

It combines:

- silent-security tasking
- wrist-worn or flashlight-mounted displays
- Greek and Roman guard call signs
- fixed operational coordinates
- local grid sectors
- route instructions
- optional passage support
- task states
- discreet acknowledgement
- movement verification
- arrival confirmation
- Master Watcher oversight
- Watcher Operator control
- radio fallback
- life-safety override
- audit and review

The human-facing assignment format is:

```text
THETA:VIII ][ BETA-F6-NE
```

The notation separates:

```text
Guard identity ][ Operational position
```

The guard receives the minimum actionable instruction while the control room retains the wider incident context.

> **The guard does not need the whole incident. The guard needs the correct task.**

---

## Final Design Principle

> **During a silent security incident, deliver the minimum actionable coordinate through a controlled low-signature channel, support safe passage where authorized, verify the guard’s movement, and preserve radio communication for safety, clarity, and escalation.**
