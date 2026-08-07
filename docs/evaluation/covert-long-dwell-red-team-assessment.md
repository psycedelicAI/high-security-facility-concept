# Covert Long-Dwell Red-Team Assessment

> A patient-adversary validation model for testing whether the High-Security Facility Concept remains coherent under long-term reconnaissance, adaptive attack attempts, contextual anomalies, and controlled adversarial pressure.

## Document Information

| Field | Value |
|---|---|
| Document | Covert Long-Dwell Red-Team Assessment |
| Subject | High-Security Facility Concept |
| Type | Evaluation and adversarial validation model |
| Status | Conceptual |
| Assessment style | Covert, long-duration, multi-domain red team |
| Proposed duration | Up to twelve months |
| Primary owner | Facility owner or designated security authority |
| Normal personnel awareness | Not informed in advance |
| Exercise authority | Authorized white team |
| Safety principle | Realistic testing without uncontrolled harm |

---

## 1. Purpose

A conventional penetration test usually evaluates a limited set of technical or physical controls during a defined test window.

A high-security facility must also be evaluated against a patient and adaptive adversary that has time to:

- observe normal routines;
- study movement patterns;
- identify procedural weaknesses;
- test access transitions;
- identify inconsistencies between security systems;
- attempt social or operational manipulation;
- wait for favorable conditions; and
- adapt after unsuccessful attempts.

This assessment models a long-dwell adversary that may conduct reconnaissance and controlled attack attempts over an extended period.

The purpose is to determine whether the facility can maintain a coherent security state when an attacker has time to learn, plan, test, and adapt.

The assessment does not attempt to prove that the facility is impossible to penetrate.

It evaluates whether:

1. unauthorized access is prevented or delayed;
2. contradictions are detected across security layers;
3. sensitive equipment remains accountable;
4. normal procedures remain resistant to manipulation;
5. operators receive actionable information;
6. the Master Watcher Operator can coordinate an appropriate response;
7. life-safety functions remain protected;
8. successful attempts create a clear and reviewable failure record; and
9. discovered weaknesses can be corrected and retested.

---

## 2. Core Assessment Principle

The facility should not be evaluated only by asking whether a badge opens a door.

The relevant question is whether the complete security context remains coherent:

- Is the correct person present?
- Is the correct badge being used?
- Is the ticket valid for this person and purpose?
- Is the encrypted QR valid in the current context?
- Is the person entering the correct zone?
- Is the movement following the approved route?
- Is the required escort present?
- Is the assigned laptop or equipment in the expected location?
- Did human validation actually occur?
- Was the action properly acknowledged?
- Does the operator still own the next decision?

The assessment therefore evaluates the relationship between:

```text
Person
↔ identity
↔ badge
↔ ticket
↔ encrypted QR
↔ human validation
↔ route
↔ escort
↔ zone
↔ equipment
↔ RFID location
↔ time
↔ operator authorization
```

A single valid credential must not be treated as proof that the entire access state is legitimate.

---

## 3. Assessment Philosophy

The red team represents a patient, adaptive adversary rather than a tester performing one short, predictable exercise.

The red team may be allowed to:

- observe normal activity;
- study routines;
- identify repeated patterns;
- test different times and conditions;
- learn from unsuccessful attempts;
- identify procedural inconsistencies;
- test human and organizational behavior;
- test physical and contextual controls;
- and attempt to create contradictions between security layers.

The assessment should preserve the normal operating environment as far as legally and safely possible.

Normal personnel should continue performing their ordinary work and should not be informed of the assessment in advance unless disclosure is required by law, policy, employment requirements, or a specific safety condition.

---

## 4. No Legitimate Starting Advantage

At the beginning of the assessment, the red team should not be handed legitimate facility assets.

Unless a later scenario explicitly introduces a controlled test identity or asset, the red team begins without:

- a facility badge;
- an access card;
- a laptop;
- a facility-issued ticket;
- an encrypted QR credential;
- an escort;
- a walkie-talkie;
- or other facility-owned equipment.

This prevents the assessment from giving the red team an artificial advantage.

The initial question is:

> Can an external adversary make meaningful progress without being given access, credentials, equipment, or internal assistance?

Later scenarios may simulate:

- insider access;
- contractor access;
- credential misuse;
- escort separation;
- asset movement;
- operator manipulation; or
- cyber-physical coordination.

Such scenarios must be explicitly authorized and documented.

---

## 5. White Team

The white team is the trusted exercise authority.

The white team may be small, but it must have sufficient authority to control the assessment and terminate it immediately when necessary.

### 5.1 White-team responsibilities

The white team is responsible for:

- written authorization;
- legal and contractual approval;
- scope definition;
- rules of engagement;
- protected personnel and areas;
- safety boundaries;
- emergency stop authority;
- coordination with emergency services;
- exercise communications;
- evidence handling;
- secure records;
- exercise termination;
- acceptance of findings; and
- remediation oversight.

### 5.2 Restricted awareness

Normal personnel should not be briefed about the assessment in advance.

Their normal behavior is part of what is being evaluated.

The white team must therefore maintain:

- a secure exercise contact channel;
- a covert termination mechanism;
- a list of protected personnel and areas;
- a process for distinguishing test activity from a real incident;
- and a recovery process that does not expose unnecessary information.

The red team must not create an uncontrolled emergency merely because personnel are unaware of the exercise.

---

## 6. Red-Team Operating Model

The red team may conduct activity over a period of up to twelve months.

The duration exists to model a planned attack in which an adversary has time to:

- conduct reconnaissance;
- observe staff routines;
- study access patterns;
- identify shift changes;
- observe contractor behavior;
- identify equipment movements;
- test response timing;
- look for procedural gaps;
- wait for favorable conditions;
- and adapt after failed attempts.

The red team does not need to maintain constant visible activity.

Long-dwell testing may include periods of observation, analysis, inactivity, and controlled attempts.

Patience is part of the adversary model.

The one-year period does not mean unlimited authority. All activity remains bound by the written rules of engagement.

---

## 7. Assessment Phases

| Phase | Purpose |
|---|---|
| Preparation | Define authorization, scope, threats, safety controls, and success conditions |
| Baseline | Understand normal facility behavior and expected security states |
| Reconnaissance | Conduct authorized observation and pattern analysis |
| Access testing | Test perimeter, entrances, mantraps, person-counting, and invalid credentials |
| Context testing | Test ticket, QR, human validation, route, escort, and zone logic |
| Asset testing | Test RFID visibility, equipment accountability, and device protection |
| Operator testing | Test handshakes, escalation, workload, and Master Watcher response |
| Insider simulation | Test controlled insider, contractor, and credential-misuse scenarios |
| Coordinated exercise | Test multiple simultaneous or time-separated anomalies |
| Reporting | Document results, evidence, timelines, and residual risk |
| Remediation | Correct weaknesses and perform controlled retesting |

The exact timing and sequencing should be known only to the authorized white team and the red-team leadership.

---

## 8. Threat Model

### 8.1 External Intruder

An external intruder attempts to approach and enter without valid authorization.

Expected facility behavior:

- invalid credentials do not permit progression;
- mantraps allow only the intended number of people;
- person-count mismatches generate alerts;
- unusual behavior is detected;
- alternate or forced-entry attempts are recorded;
- and the intruder is denied, delayed, contained, or escalated.

The facility should not rely on a single door reader to identify or stop an external intruder.

The assessment should evaluate the complete transition:

```text
Approach
→ observation
→ credential attempt
→ person count
→ mantrap state
→ human interpretation
→ operator response
→ containment or escalation
```

---

### 8.2 Tailgating and Piggybacking

A mantrap should allow only the intended number of people to pass during each controlled transition.

A single valid badge scan followed by detection of two people should produce a person-count contradiction:

```text
One valid badge scan
+ two detected persons
= unauthorized passage state
```

Expected response:

- passage rejected, held, or placed into a supervised state;
- operator alert generated;
- event logged;
- associated identity and camera records preserved;
- and further progression prevented until the condition is resolved.

The assessment should also test:

- close-following behavior;
- attempts to exploit door timing;
- unusual body positioning;
- mobility aids;
- legitimate exceptions;
- uncertain person counts; and
- emergency behavior.

The facility must distinguish security response from life-safety response.

---

### 8.3 Credential, Ticket, or Encrypted QR Misuse

The assessment may evaluate whether a credential, ticket, or encrypted QR payload can be:

- replayed;
- copied;
- presented at the wrong location;
- used outside its approved time;
- used by another person;
- associated with the wrong task;
- or combined with an incorrect route, zone, or escort state.

The badge itself is a blank card containing an encrypted QR code. The QR code is intended for specific use cases and should not expose unnecessary identity information.

The QR code should not independently grant access.

Expected high-risk authorization state:

```text
Identity
+ valid ticket
+ encrypted QR
+ correct zone
+ correct time
+ human validation
+ required escort
+ coherent route
+ compatible equipment context
= permitted transition
```

If any required context is contradictory, the transition should enter an exception, hold, or investigation state.

Encryption may protect the QR contents, but the system must also consider:

- authenticity;
- integrity;
- expiry;
- replay resistance;
- context binding;
- and revocation.

---

### 8.4 Malicious Insider Simulation

The malicious insider is one of the more difficult threat models because the person may possess legitimate access and knowledge of normal procedures.

The assessment may simulate:

- unauthorized movement;
- zone deviation;
- unusual timing;
- unexpected device interaction;
- access outside assigned duties;
- attempts to bypass handshakes;
- attempts to use another person’s authority;
- attempts to manipulate records;
- attempts to exploit operator trust; and
- attempts to create a false but coherent security state.

The facility should use:

- zone control;
- movement control;
- device control;
- RFID asset correlation;
- camera observation;
- ticket and route validation;
- human verification;
- and operator escalation.

The facility does not need to solve every cyber or identity-provider threat itself.

A defined handoff should exist:

```text
Facility security
→ detects physical and contextual contradiction
→ preserves evidence
→ escalates to IT and identity security
```

IT security remains responsible for investigation and response involving:

- accounts;
- passwords;
- tokens;
- endpoints;
- identity providers;
- and cyber activity.

---

### 8.5 Compromised Contractor

The assessment may test whether a contractor can:

- leave a planned route;
- separate from an escort;
- approach an unauthorized zone;
- continue after route deviation;
- present an invalid or incomplete ticket;
- or create an exception that an operator incorrectly approves.

Expected facility behavior:

- route deviation becomes visible;
- escort separation is detected;
- further progression is paused or restricted;
- the contractor is directed to a controlled state;
- the escort or supervisor is notified;
- and the event is escalated for investigation.

A route deviation should create a controlled exception, not an automatic assumption of malicious intent.

Emergency, accessibility, maintenance, and life-safety exceptions must remain possible and reviewable.

---

### 8.6 Coordinated Group

The assessment may simulate multiple actors attempting to:

- create simultaneous anomalies;
- exploit operator workload;
- use distraction;
- approach from multiple paths;
- create conflicting instructions;
- test pathway restrictions;
- or overwhelm the Master Watcher Operator.

The facility should test whether cameras, zone controls, OPSEC correlation, and the Master Watcher Operator can:

- identify coordinated movement;
- correlate events across zones;
- segment or restrict pathways;
- preserve escape and emergency routes;
- maintain operator awareness;
- prevent uncontrolled spread;
- and coordinate an appropriate response.

The operator should control pathways without creating uncontrolled entrapment.

---

### 8.7 Accidental Operator

The assessment should test whether an operator can unintentionally:

- leave an action incomplete;
- approve the wrong person;
- approve the wrong zone;
- fail to transfer responsibility;
- create an incorrect door state;
- or treat an unresolved exception as complete.

A handshake should provide a visible state transition:

```text
Initiated
→ Acknowledged
→ Executed
→ Confirmed
```

Failure should create:

```text
Timeout
→ Escalation
→ Handoff or recovery
```

A handshake reduces silent or unowned error. It does not eliminate the possibility that multiple people share the same incorrect assumption.

---

## 9. Core Asset-Accountability Model

Sensitive equipment is part of the facility’s security context.

RFID readers distributed throughout the facility may monitor tagged:

- laptops;
- walkie-talkies;
- tools;
- containers;
- access-related equipment;
- and other designated assets.

The purpose is not merely inventory management.

RFID asset visibility is a primary OPSEC and security-correlation layer.

It helps answer:

- Where is the sensitive equipment?
- Who is responsible for it?
- Is the equipment in an authorized zone?
- Is the assigned person nearby?
- Is the equipment following the approved route?
- Has the equipment been left unattended?
- Has an asset entered a zone without a matching task?
- Does equipment location contradict a badge or ticket event?

---

## 10. Identity and Asset Continuity

The facility should continuously evaluate the relationship between:

```text
Person
↔ badge
↔ ticket
↔ encrypted QR
↔ human validation
↔ assigned laptop
↔ RFID location
↔ route
↔ escort
↔ zone
↔ time
↔ operator authorization
```

A valid badge, ticket, QR code, or human approval alone does not establish a coherent high-risk access state.

The system should look for contradictions such as:

- a person entering a high-risk zone while their assigned laptop remains elsewhere;
- a laptop entering a zone without its assigned person;
- a ticket being used outside its approved route;
- an escort disappearing before the contractor reaches the next transition;
- equipment appearing in a zone without an assigned task;
- a person-count mismatch at a single-person mantrap;
- a valid ticket associated with the wrong person;
- or an operator approval that lacks the required handshake or ownership transfer.

---

## 11. RFID Asset-Location Model

RFID presence is evidence that an asset was detected near a reader.

It does not independently prove:

- identity;
- authorization;
- intent;
- exact position;
- or continuous possession.

Every RFID event should ideally include:

- tag identity;
- equipment identity;
- reader identity;
- timestamp;
- last confirmed location;
- detection confidence;
- movement or stationary state;
- assigned person;
- assigned task;
- and relevant zone state.

A location record should distinguish between:

- **confirmed**;
- **probable**;
- **stale**;
- **uncertain**; and
- **not detected**.

A missed read should not automatically be interpreted as proof that an asset has moved.

However, a confirmed contradiction between equipment location and a high-risk access event should receive a serious response.

---

## 12. Example: High-Risk Context Contradiction

Example event:

```text
Employee: AAXX11
Badge event: Door 97
Zone: 3 / High Risk
Ticket: Present
Encrypted QR: Valid
Human validation: Recorded
Escort: Missing
Assigned laptop: Laptop X
Laptop location: Main entrance
```

Sensitive laptops must not be left unattended.

Therefore, “the employee left the laptop temporarily” is not an accepted normal explanation.

This event should be classified as:

> **High-severity identity, escort, and asset-continuity contradiction.**

Expected response:

1. stop further high-risk progression;
2. freeze or protect Laptop X;
3. invalidate or suspend the relevant authorization state;
4. revoke or restrict active sessions where appropriate;
5. verify the human-validation event;
6. correlate cameras, RFID readers, badge events, tickets, and logs;
7. notify the OPSEC authority and Master Watcher Operator;
8. preserve evidence; and
9. begin a controlled investigation.

Possible causes may include:

- badge misuse;
- ticket misuse;
- human-validation error;
- escort failure;
- RFID association error;
- system-integrity failure; or
- an intentionally created false security state.

The system should identify the contradiction without prematurely deciding which explanation is correct.

---

## 13. Unattended Sensitive Laptop Response

An unattended sensitive laptop is a security violation.

Expected response:

```text
Laptop detected without assigned employee
→ laptop enters protected state
→ active session is locked
→ sensitive operations are restricted
→ OPSEC alert is generated
→ identity and asset context are investigated
```

Possible additional actions include:

- device freeze;
- network restriction;
- revocation of active sessions;
- invalidation of active tokens;
- forced reauthentication;
- credential rotation;
- forensic preservation;
- and security approval before returning the device to normal operation.

The response may be divided into levels.

### Level 1 — Immediate Containment

- lock the session;
- block sensitive actions;
- alert OPSEC;
- preserve the initial event state.

### Level 2 — Identity Protection

- revoke active sessions and tokens;
- require reauthentication;
- invalidate the associated ticket or QR authorization;
- restrict network access where appropriate.

### Level 3 — Credential Reset

- rotate passwords or credentials;
- investigate possible compromise;
- review relevant logs;
- reissue authorization only after review.

---

## 14. Optional Personnel Safety Tags

Some high-value employees may voluntarily carry a wearable RFID or safety tag for emergency protection.

The tag may assist with:

- emergency location;
- evacuation accounting;
- distress response;
- medical or security assistance;
- and location confirmation during a facility incident.

The wearable should not be the sole source of truth.

The facility should also use:

- badge events;
- cameras;
- other equipment tags;
- manual reports;
- communications;
- and last-known-location records.

Personnel-location data must be:

- purpose-limited;
- access-controlled;
- auditable;
- minimized outside declared safety or security use;
- and protected against operator misuse.

The facility should define:

- who can view individual locations;
- when tracking is active;
- how long location history is retained;
- whether employees can access their own data;
- who can activate emergency monitoring; and
- how misuse is investigated.

---

## 15. Operator and Master Watcher Evaluation

The Master Watcher Operator should be evaluated on:

- situational awareness;
- interpretation of cross-system contradictions;
- decision quality;
- response speed;
- communication;
- delegation;
- handoff;
- use of pathway restrictions;
- preservation of life-safety access;
- and ability to recover from incomplete information.

The operator should receive enough information to act, but not an unstructured flood of unrelated events.

Example event:

```text
HIGH-RISK CONTEXT MISMATCH

Subject: AAXX11
Badge: Valid
Door: 97
Zone: 3 / High Risk
Ticket: Present
Encrypted QR: Valid
Human validation: Recorded
Escort: Missing
Assigned device: Laptop X
Device location: Main entrance
Status: Contradictory authorization state
Action: Hold progression and initiate OPSEC investigation
```

The interface should distinguish:

- what happened;
- what is known;
- what is uncertain;
- what action is recommended;
- what action has already occurred;
- and who currently owns the next decision.

---

## 16. Rules of Engagement

The red team may be authorized to use realistic but controlled methods, including:

- physical access attempts;
- observation from lawful locations;
- social-engineering simulations;
- route and escort testing;
- credential-context testing;
- asset-accountability testing;
- operator-deception scenarios;
- and cyber-physical simulations.

The following are prohibited unless separately and explicitly authorized in a safe test environment:

- physical harm or threats;
- weapons;
- coercion, blackmail, or harassment;
- disabling life-safety systems;
- interference with emergency communications;
- destructive activity;
- uncontrolled malware;
- irreversible alteration of production data;
- disruption of medical, fire, or evacuation functions;
- and actions likely to cause uncontrolled panic.

A realistic test must not become an uncontrolled real incident.

The red team must not escalate an encounter merely because normal personnel discover or challenge them.

The red team must not use discovered information to create unnecessary risk to uninvolved people.

---

## 17. Legal and Safety Authorization

Before the assessment begins, the facility owner must establish:

- written authorization;
- ownership of the facility and systems in scope;
- permitted locations and hours;
- authorized test methods;
- prohibited actions;
- emergency stop authority;
- evidence-handling requirements;
- privacy and data-protection requirements;
- emergency-service coordination;
- and post-exercise disclosure procedures.

The assessment should be performed by appropriately qualified professionals with:

- suitable contracts;
- appropriate insurance;
- legal review;
- professional competence;
- and clearly defined responsibility.

---

## 18. Success Criteria

The red team succeeds when it creates an unauthorized or unsafe security state that the facility fails to prevent, detect, contain, or correctly escalate.

Examples include:

- entering a protected zone without the required authorization state;
- bypassing a mantrap or person-counting control;
- causing two people to pass as one;
- using a ticket or QR payload outside its intended context;
- moving sensitive equipment without detection;
- separating an employee from an assigned laptop without a response;
- creating contradictory badge, RFID, camera, and operator records;
- bypassing an escort requirement;
- manipulating an operator into approving an unsafe action;
- remaining in an unauthorized zone without detection;
- or causing the Master Watcher response to fail.

A test should also record partial success, such as:

- detection without containment;
- containment without correct escalation;
- alert generation without operator comprehension;
- correct detection but incorrect response;
- delayed response;
- or response that compromises life safety.

A successful red-team finding is not limited to physical entry.

A finding may be successful if the red team can create a contradictory or unauthorized state that remains undetected or uncontrolled.

---

## 19. Detection and Response Measures

Each event should be evaluated using:

- time to detection;
- time to operator awareness;
- time to containment;
- time to escalation;
- correctness of the decision;
- preservation of evidence;
- life-safety impact;
- and ability to recover normal operation.

The assessment should distinguish between:

| Outcome | Meaning |
|---|---|
| Prevented | The attempt could not progress |
| Detected | The attempt was observed |
| Delayed | Progress was slowed |
| Contained | The threat was restricted |
| Escalated | The correct authority was notified |
| Recovered | Normal safe operation was restored |
| Successful breach | The red team reached the defined objective |

A control should not be considered fully successful merely because it generated an alert.

The alert must:

- reach the correct operator;
- contain enough context to support a decision;
- identify uncertainty;
- preserve the event timeline;
- and lead to an appropriate response.

---

## 20. Handshake and Handoff Evaluation

The assessment should test whether operators can safely transfer responsibility.

A complete handoff should establish:

- who initiated the action;
- who acknowledged it;
- who executed it;
- who confirmed the result;
- who owns the next decision; and
- what happens if the responsible person becomes unavailable.

Expected handoff sequence:

```text
Operator A initiates
→ Operator B acknowledges
→ Operator B accepts ownership
→ action is executed
→ result is confirmed
→ responsibility is recorded
```

Failed handoff:

```text
Handoff requested
→ no acknowledgement
→ timeout
→ escalation
→ alternate operator or supervisor assigned
```

The system should prevent an unresolved action from silently appearing complete.

---

## 21. Stop Conditions

The red team must stop immediately when:

- an agreed objective is achieved;
- a real safety risk emerges;
- a person may be harmed;
- emergency services become involved;
- life-safety systems are affected;
- the white team issues a termination order;
- continued activity could create irreversible consequences; or
- the exercise can no longer be reliably distinguished from a real uncontrolled incident.

After stopping, the red team must:

1. cease further activity;
2. preserve evidence;
3. notify the authorized white-team contact;
4. identify the achieved objective;
5. document the current state;
6. support safe restoration of normal operation; and
7. avoid further exploitation until explicitly reauthorized.

---

## 22. Immediate Success Reporting

If the red team achieves a defined objective, it must stop and report rather than continue expanding the compromise.

The reporting sequence should be:

```text
Objective achieved
→ red team stops
→ evidence preserved
→ white team notified
→ current state documented
→ risk contained
→ initial finding delivered
→ full report prepared
→ remediation planned
→ controlled retest performed
```

The red team should not continue searching for additional weaknesses after a significant objective has been achieved unless the white team explicitly authorizes continuation.

---

## 23. Reporting Requirements

The final report should include:

- executive summary;
- assessment dates and duration;
- objectives and assumptions;
- reconnaissance narrative;
- attempted methods;
- successful and unsuccessful paths;
- relevant badge, ticket, QR, RFID, camera, and operator events;
- detection and response timelines;
- affected zones and assets;
- root cause;
- contributing conditions;
- residual risk;
- recommended remediation;
- and retest requirements.

Reports should distinguish between:

- observed facts;
- red-team assumptions;
- system decisions;
- operator decisions;
- and conclusions.

A timeline should be provided for each important event:

```text
T+00:00 — Initial approach or observation
T+00:05 — Security control engaged
T+00:08 — Contradiction or anomaly created
T+00:10 — OPSEC detection
T+00:12 — Operator awareness
T+00:15 — Containment
T+00:20 — Escalation
T+00:30 — Exercise termination
```

The report should include the facility’s state at each point:

- person location;
- credential state;
- ticket state;
- QR state;
- equipment location;
- escort state;
- door state;
- operator ownership;
- and confidence or uncertainty.

---

## 24. Remediation and Retesting

A finding is not closed merely because it has been documented.

For each finding, the owner should define:

- corrective action;
- responsible authority;
- target date;
- validation method;
- residual risk;
- and retest condition.

Remediation should be retested without revealing unnecessary details to normal personnel.

The retest should determine whether:

- the original attack path remains possible;
- the original contradiction is detected;
- the response is faster or more accurate;
- the correct authority is notified;
- the affected asset is protected;
- evidence remains reviewable;
- and life safety remains protected.

The final outcome should state whether the facility:

- prevented the attempt;
- detected it;
- delayed it;
- contained it;
- escalated it;
- recovered safely; or
- failed to maintain a coherent security state.

---

## 25. Evaluation Matrix

| Threat or condition | Primary controls | Expected detection | Expected response |
|---|---|---|---|
| External intruder | Perimeter, invalid-credential denial, mantrap | Failed entry, forced-entry attempt, abnormal movement | Deny, alert, delay, contain |
| Tailgating | Person counting, single-person mantrap, camera correlation | One scan with multiple persons | Hold passage, alert operator, investigate |
| Ticket or QR misuse | Context-bound ticket, encrypted QR, human validation | Identity, zone, time, route, or context mismatch | Reject, suspend, escalate |
| Malicious insider | Zone, movement, device, RFID, privilege controls | Unauthorized movement or device interaction | Restrict, investigate, preserve evidence |
| Compromised contractor | Escort, route plan, ticket, zone transitions | Route deviation or escort separation | Pause progression, controlled return, escalate |
| Coordinated group | Cameras, correlation, pathway control, Master Watcher | Multi-point or coordinated movement | Segment, delay, contain, coordinate response |
| Unattended laptop | RFID, device policy, endpoint protection | Device/person separation | Freeze device, protect credentials, investigate |
| Accidental operator | Handshake, confirmation, timeout, handoff | Missing acknowledgement or inconsistent state | Escalate, transfer ownership, recover |
| System contradiction | Cross-layer correlation | Conflicting badge, RFID, camera, ticket, or escort data | Hold progression, investigate, preserve evidence |
| Degraded operation | Local policy, safe fallback, manual procedures | Sensor, network, or control degradation | Enter approved degraded mode and maintain safety |

---

## 26. Design Principles

This assessment is based on the following principles:

1. **No legitimate starting advantage**  
   The red team begins without a badge, laptop, ticket, escort, or facility equipment unless a later scenario explicitly introduces one.

2. **Patient-adversary realism**  
   The red team may observe, wait, adapt, and try different approaches over time.

3. **Normal personnel remain normal**  
   Ordinary personnel should continue their expected work without being briefed in advance, subject to legal and safety requirements.

4. **White-team control**  
   A trusted white team authorizes, governs, monitors, and can terminate the assessment.

5. **Cross-layer validation**  
   Physical, human, digital, RFID, route, escort, and operator signals must be evaluated together.

6. **Contradictions matter**  
   A valid credential does not establish valid access when surrounding context is inconsistent.

7. **RFID is a primary OPSEC layer**  
   Sensitive equipment location is part of the facility’s security state, not merely an inventory concern.

8. **Sensitive equipment remains accountable**  
   Unattended or misplaced equipment enters a protected state and triggers investigation.

9. **Human control remains accountable**  
   Handshakes, ownership, confirmation, and escalation prevent silent actions.

10. **Stop after proof**  
    Once an agreed objective is achieved, the red team stops and reports.

11. **Evidence over assumption**  
    Every conclusion should be supported by logs, timestamps, observation, or reproducible test evidence.

12. **Life safety overrides security restrictions**  
    Security response must never obstruct required emergency action.

13. **Security must be reviewable**  
    The facility should be able to reconstruct what happened, what it believed, what it did, and why.

14. **A failed control must produce learning**  
    Findings should lead to remediation, ownership, validation, and retesting.

---

## 27. Expected Outcome

A successful assessment does not mean that no attack was ever attempted.

A successful assessment means the facility demonstrates that:

- unauthorized activity is difficult to perform silently;
- access decisions depend on coherent context;
- invalid credentials do not permit normal progression;
- mantraps detect and prevent person-count contradictions;
- sensitive assets remain accountable;
- an unattended laptop enters a protected state;
- suspicious contradictions reach the correct operator;
- the Master Watcher can coordinate an appropriate response;
- operators can hand off responsibility safely;
- route and escort deviations become visible;
- life-safety functions remain available;
- failures can be corrected and retested; and
- the facility can explain its security decisions after the event.

The purpose of the red team is not to validate a feeling of security.

It is to reveal where the trust architecture breaks under a patient, adaptive, realistic adversary.
