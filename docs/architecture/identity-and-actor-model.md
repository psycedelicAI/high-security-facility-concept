# Identity and Actor Model – High-Security Facility Concept

> A conceptual model describing how identities, actor types, roles, and contextual trust should be understood within the High-Security Facility Concept.

---

## Document Information

| Field | Value |
|---|---|
| Document | Identity and Actor Model |
| Subject | High-Security Facility Concept |
| Type | Supporting Trust Architecture Document |
| Status | Draft |
| Scope | Identity, actor types, role-based trust, contextual legitimacy, movement interpretation, trust differentiation |
| Audience | Security architects, facility planners, governance owners, access designers, operations leads, concept reviewers |

---

## Purpose

This document defines how identities and actor types should be understood within the **High-Security Facility Concept**.

Its purpose is to clarify that a high-security facility should not treat all authorized presence as equivalent.

A person may be:
- known
- registered
- issued a credential
- allowed to enter certain zones
- expected at certain times

and still not be equally trusted in every context.

For that reason, this concept distinguishes between **identity**, **role**, **presence**, **movement**, and **contextual trust**.

---

# Core Principle

The concept assumes that identity alone is not enough.

A secure environment should not ask only:

> Who is this?

It should also ask:

- What type of actor is this?
- Why are they here?
- Where are they allowed to be?
- How did they arrive there?
- What is normal for this role?
- What level of trust should apply in this context?
- What kind of scrutiny or limitation should apply to this actor type?

The result is a more meaningful trust model.

---

# Identity Is Not the Same as Trust

Identity answers whether someone can be recognized, registered, or authenticated.

Trust answers whether their presence, movement, access, and behavior remain legitimate in context.

This means a person may have:
- verified identity
- valid credentials
- approved entry

while still requiring:
- constrained movement
- additional oversight
- time restrictions
- escort requirements
- zone limitations
- stronger anomaly sensitivity

This distinction is central to the concept.

---

# Actor Categories

The concept assumes that different actor categories should be treated differently.

These categories do not necessarily define legal status or HR classification.  
They define **trust-relevant operational meaning**.

## 1. Resident Internal Actor

An actor whose normal function is embedded in the facility’s recurring operations.

Examples may include:
- core employees
- embedded technical staff
- regular control room staff
- long-term operational personnel

### Trust implications
These actors may have higher familiarity and more predictable patterns, but also greater opportunity for normalized misuse.

### Security meaning
They should not automatically receive the least scrutiny just because they are common.

---

## 2. Privileged Internal Actor

An actor with elevated operational authority, technical override capability, administrative reach, or high-impact access.

Examples may include:
- senior administrators
- privileged technicians
- infrastructure operators
- maintenance leads with override capability
- security administrators

### Trust implications
These actors require stronger governance, stronger reviewability, and greater separation from ordinary access logic.

### Security meaning
Their legitimacy must remain constrained by context, not by status alone.

---

## 3. Temporary Authorized Actor

An actor who is authorized for a limited task, period, scope, or zone.

Examples may include:
- contractors
- service technicians
- short-term consultants
- project visitors with operational purpose
- temporary support staff

### Trust implications
These actors may be legitimate without being deeply trusted.

### Security meaning
Temporary legitimacy should remain narrow, explicit, time-bound, and reviewable.

---

## 4. Escorted Actor

An actor whose presence may be acceptable only under supervision or guided movement conditions.

Examples may include:
- visitors
- external assessors
- delivery-related personnel
- auditors
- observers
- non-embedded specialists

### Trust implications
Their presence is conditionally legitimate rather than independently trusted.

### Security meaning
Escort logic is not only a courtesy measure.  
It is a trust-limiting mechanism.

---

## 5. Emergency or Exceptional Actor

An actor whose presence becomes legitimate under emergency, incident, or exceptional conditions rather than ordinary operating logic.

Examples may include:
- firefighters
- emergency medical personnel
- urgent repair personnel
- incident-response specialists
- law enforcement under authorized conditions

### Trust implications
These actors may require rapid conditional access, but their movement still needs control, clarity, and review.

### Security meaning
Emergency legitimacy must not dissolve all architectural discipline.

---

## 6. Unknown or Unverified Actor

An actor whose identity, intent, or legitimacy cannot be confidently established.

Examples may include:
- unidentified persons
- unexplained movement
- possible intruders
- unverified presence in controlled zones

### Trust implications
These actors should be treated as high-uncertainty conditions.

### Security meaning
The system should support visibility, interpretation, containment, and escalation.

---

# Role Does Not Override Context

A critical principle of the concept is that role should not automatically override context.

For example:
- a technician may be legitimate in one zone and anomalous in another
- an employee may be expected during the day and unusual at night
- an administrator may be trusted for system oversight but not for unreviewed physical access everywhere
- a contractor may be approved for a task but not for broad autonomous movement

This means the concept does not ask only:

> What is this person allowed to do in principle?

It also asks:

> Is this behavior legitimate here, now, and in this sequence?

---

# Contextual Trust Dimensions

Contextual trust within the concept may be influenced by several dimensions.

## Identity confidence
How strongly the actor’s identity is established.

## Role legitimacy
Whether the actor’s declared or assigned role matches the environment and task.

## Zone appropriateness
Whether the actor is present in a zone that fits their expected purpose.

## Movement sequence
Whether the actor arrived through a meaningful and expected path.

## Time appropriateness
Whether the timing of presence matches expected activity.

## Asset association
Whether the actor carries or uses credentials, devices, tools, or assets that fit their role.

## Oversight state
Whether the actor is independently trusted, monitored, escorted, or under restricted logic.

## Operational condition
Whether the facility is in normal mode, incident mode, maintenance mode, degraded state, or recovery.

These dimensions help determine trust in context.

---

# Trust Is Gradient, Not Binary

The concept assumes that trust is often graduated rather than absolute.

An actor may be:
- highly trusted in one context
- conditionally trusted in another
- tolerated only with controls in another
- anomalous in another
- unacceptable in another

This is important because binary thinking such as “authorized” versus “unauthorized” is often too simplistic for real high-security environments.

---

# Identity and Movement Relationship

Identity should be interpreted together with movement.

A valid identity does not erase the meaning of:
- unusual sequence
- unexplained route choice
- presence in low-baseline areas
- repeated zone transitions without clear purpose
- boundary behavior inconsistent with role

This reflects one of the broader truths of the concept:

> The meaning of a person in a facility is partly revealed by how they move through it.

---

# Identity and Asset Relationship

The concept also treats trust-bearing assets as extensions of identity context.

This may include:
- credentials
- issued devices
- administrative tools
- maintenance tools
- access tokens
- controlled keys or equivalent trust objects

This matters because:
- a trusted person with the wrong asset may be anomalous
- an expected asset in the wrong custody may indicate misuse
- asset legitimacy and actor legitimacy should reinforce each other

The concept therefore treats identity and asset custody as related but distinct trust questions.

---

# Identity and Privilege Relationship

Privilege is not simply a stronger form of identity.  
It is a separate risk amplifier.

A privileged actor may be:
- highly necessary
- fully legitimate
- strongly authenticated

and still require:
- more constraints
- more logging
- more scrutiny
- stronger review
- narrower context handling

This reflects the principle that privileged legitimacy should remain disciplined.

---

# Human Interpretation and Operational Use

The identity and actor model is not meant only for access control systems.

It is also intended to support:
- facility design
- surveillance interpretation
- incident review
- movement assessment
- zone policy decisions
- maintenance planning
- response logic

This means the model should help humans reason about trust, not only help systems classify people.

---

# What This Model Rejects

This concept rejects several overly simplistic assumptions.

## Rejected assumption 1:
If identity is known, trust is solved.

## Rejected assumption 2:
If access is approved, context no longer matters.

## Rejected assumption 3:
If a person works here, their movement is self-justifying.

## Rejected assumption 4:
If someone is privileged, they should face fewer constraints.

## Rejected assumption 5:
If a person is legitimate, they cannot still be anomalous.

These assumptions are treated as dangerous simplifications in a high-security environment.

---

# Design Implications

Because of this model, the concept favors:

- actor-aware trust logic
- role-sensitive access interpretation
- contextual movement review
- stronger differentiation between actor types
- time-bounded and scope-bounded legitimacy
- oversight-aware presence models
- privilege-specific governance
- stronger alignment between identity, movement, and zone meaning

---

# Adaptation Principle

If the concept is adapted to other controlled environments, actor categories may change in name or operational detail.

However, the deeper principle should remain:

> Not all legitimate identities are equally trustworthy in all contexts.

That principle is central to the concept’s trust architecture.

---

# Summary

Within the **High-Security Facility Concept**, identity is necessary but not sufficient.

A secure environment must understand not only who a person is, but what kind of actor they are, what role they hold, how they move, what context applies, and what degree of trust is justified at that moment.

The central idea is:

> Identity establishes recognition, but contextual trust determines legitimacy.

This distinction helps the concept treat presence, movement, privilege, and oversight as meaningful parts of security rather than secondary details.
