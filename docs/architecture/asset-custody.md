# Asset Custody Model – High-Security Facility Concept

> Conceptual model for the control, storage, movement, and traceability of badges, tokens, laptops, and other security-critical assets in a high-security technical facility.

---

## Document Information

| Field | Value |
|---|---|
| Document | Asset Custody Model |
| Subject | High-Security Facility Concept |
| Type | Security Architecture / Asset Control Concept |
| Status | Draft |
| Scope | Badges, tokens, laptops, lockers, RFID tracking, chain of custody |
| Audience | Security architects, facility planners, IT security leads, physical security teams |

---

## Purpose

This document describes a conceptual model for **asset custody** in a high-security environment.

The goal is to ensure that sensitive assets:

- are stored in the correct location
- are used by the correct person
- do not leave the permitted area without control
- can be tracked and reviewed
- are covered by a clear chain of custody
- are protected against both loss and misuse

---

## Scope

The following types of assets are covered by the model:

- access badges / entry cards
- YubiKeys / FIDO2 tokens
- smartcards / security cards
- admin laptops
- user laptops
- power user laptops
- consultant devices
- external encrypted storage media
- lockers and related storage objects
- other security-critical identification or access objects

---

# Core Principles

## 1. Assets Are Security Objects

Assets such as badges, tokens, and laptops must not be treated as ordinary work tools, but as **security objects**.

This means that:

- they are subject to policy
- their movement must be controlled
- their storage must be defined
- their use must be attributable to person, place, and purpose

---

## 2. Custody Must Be Explicit

For every security-relevant asset, it must be clear:

- who has it
- where it is located
- when it was issued
- when it was returned
- whether it has left the permitted area
- whether it has deviated from policy

---

## 3. Sensitive Assets Should Not Drift Into Private Life

Security-critical assets should not follow users into private life unless there is an explicit and controlled need.

This applies especially to:

- badges
- highly protected tokens
- admin devices
- special security cards

---

## 4. Movement Is a Security Event

When an asset moves between zones, leaves the facility, or becomes separated from its intended context, this should be treated as a security event, or at minimum as a policy-relevant event.

---

## 5. Asset Type Determines Control Level

Different assets should have different levels of control depending on:

- sensitivity
- privilege level
- linkage to identity
- linkage to system security
- exfiltration risk
- recovery difficulty

---

# Asset Categories

## 1. Access Credentials

Examples:

- badge
- entry card
- RFID-based identification
- smartcards for physical access

### Security Relevance

These assets control physical movement and should therefore be subject to strong custody control.

---

## 2. Authentication Tokens

Examples:

- YubiKey
- FIDO2 token
- smartcard for system login
- other hardware-bound authentication objects

### Security Relevance

These assets can provide logical access to sensitive systems and should therefore be protected at least as strongly as physical access objects.

---

## 3. Managed Endpoints

Examples:

- admin laptops
- power user laptops
- user laptops
- consultant devices under facility control

### Security Relevance

These assets carry data, identity, and trust level, and must therefore be controlled from both a security and operational perspective.

---

## 4. Portable Storage

Examples:

- external encrypted SSD devices
- special removable media

### Security Relevance

Removable media present a high exfiltration risk and should be subject to stricter policy than ordinary client devices.

---

# Badge Custody Model

## Principle

As a general rule, badges should **remain inside the facility** and not follow the user home or into private environments.

---

## Purpose

This model strengthens:

- OPSEC
- protection against social engineering
- reduced external exposure
- rapid deactivation during offboarding
- lower risk of forgotten or lost badges
- better control over the credential lifecycle

---

## Expected Operational Flow

1. the user arrives at the facility
2. the badge is issued or activated according to the established process
3. the badge is used for permitted movement during the work session
4. the badge is returned to reception or a defined secure storage point at the end of the work session

---

## Security Benefits

- the user cannot forget the badge at home
- the badge is not exposed in a car, residence, or public environment
- termination of employment or changes in authorization become easier to manage
- the credential is already in a controlled environment for revocation or retrieval

---

## Recommended Controls

- issuance and return must be logged
- the badge should be personally linked or traceably assigned
- failure to return a badge should trigger follow-up
- temporary badges should have a separate policy
- visitor badges and consultant badges should be clearly separated from standard badges

---

# Token Custody Model

## Principle

Authentication tokens should be handled according to their risk level.

### Example Distinction

- standard user tokens may, in some environments, be user-carried
- highly privileged tokens should be subject to stronger custody
- break-glass or especially sensitive tokens should be kept under strictly controlled storage

---

## Security Considerations

Token custody should take into account:

- what access the token enables
- whether the token is used for privileged administration
- whether the token is used for BIOS, local admin, or globally sensitive functions
- how recovery should take place if the token is lost

---

## Recommended Controls

- personally assigned issuance where possible
- separate rules for standard tokens and highly sensitive tokens
- clear revocation process
- controlled reissuance
- strong linkage between token, identity, and role

---

# Laptop Custody Model

## Principle

Laptops should be treated as both work tools and security objects.

This means that:

- every laptop must have a defined role class
- permitted movement must be clear
- movement outside policy must be detectable
- more sensitive laptops must be subject to a higher level of control

---

## Device Classes

Examples of laptop classes:

- admin laptop
- power user laptop
- standard laptop
- consultant laptop

Each class should have:

- its own policy
- its own trust level
- its own permitted zone model
- its own access profile

---

## Facility Movement Control

Laptops should only be allowed to move within approved zones and under defined conditions.

### Example Principles

- some laptops must never leave the facility
- some laptops must not be brought into specific zones
- some laptops may only be used in defined work areas
- some laptops may require special monitoring or escort when moved

---

## RFID-Based Tracking

RFID should be used to support:

- real-time positioning
- zone control
- asset visibility
- policy triggers
- alerts when a device leaves the permitted area

It should **not** be seen as the only security mechanism, but as a strong complement to other controls.

---

## Recommended Responses to Device Deviation

When a laptop leaves the permitted area or deviates from policy, the system should be able to:

1. log the event
2. generate an alert
3. lock the device
4. restrict continued system access
5. require manual security verification

Remote wipe should normally be a later action after a confirmed incident, not the first response.

---

# Pairing and Context Validation

Some assets can advantageously be linked together contextually, for example:

- user + badge
- user + laptop
- admin identity + admin device
- zone + permitted device class

The purpose is not to create fragile over-automation, but to improve the ability to detect:

- unauthorized separation
- incorrect device usage
- policy violations
- anomalous movement patterns

---

# Lockers and Controlled Storage

## Purpose

Lockers act as a controlled transition point between private life and the protected environment.

They can be used for:

- storage of personal mobile phones
- storage of personal belongings
- storage of security objects between work sessions
- issuance and return of approved assets

---

## Security Value

Lockers strengthen the model by:

- separating private life from the protected environment
- reducing the risk that prohibited objects are brought inside
- creating a clear chain of custody for certain assets
- supporting control over what enters and leaves the environment

---

## Recommended Controls

- assignment must be traceable
- locker access must be controlled
- some lockers may be subject to special security policy
- security teams must be able to lock or secure lockers during an incident or policy violation

---

# Portable Media Control

## Principle

Removable storage media must be treated as high risk when used in the facility.

### Security Concerns

- data exfiltration
- uncontrolled data import
- loss or theft
- poor auditability

---

## Recommended Controls

- only approved encrypted media
- clear registration
- restricted use to defined roles and situations
- logging of issuance and return
- policy for destruction, storage, and revocation

---

# Offboarding & Revocation

A strong custody model should enable rapid and secure offboarding.

## Expected Benefits

- the badge is already inside the facility
- tokens can be retrieved or revoked immediately
- laptops can be locked, recovered, or isolated
- assets do not need to be searched for in private environments to the same extent

---

## Minimum Requirements

- immediate revocation of logical and physical credentials
- clear asset recovery checklist
- verification that privileged objects have been returned
- deviation flow if anything is missing

---

# Logging & Audit Requirements

The following should be logged where relevant:

- badge issuance
- badge return
- token assignment
- token revocation
- laptop assignment
- laptop movement policy deviation
- alert on unauthorized movement
- issuance and return of removable media
- locking, isolation, or revocation of a device
- deviation during offboarding

Logging should be:

- timestamped
- linked to a person where possible
- linked to a zone or location
- available for audit

---

# Recommended Policy Statements

## Example Policy 1

Security-critical assets must be covered by a clear chain of custody and may only be used, stored, or moved in accordance with established policy.

## Example Policy 2

As a general rule, access badges must remain inside the facility and be returned to a defined control point at the end of the work session.

## Example Policy 3

Privileged authentication tokens and admin devices must be subject to a higher level of control than standard user assets.

## Example Policy 4

Unauthorized movement of a laptop or other security-critical equipment must generate a security event, logging, and a policy-defined response.

## Example Policy 5

Removable media should only be permitted when approved, encrypted, registered, and justified by a defined work task.

---

# Common Risks If Poorly Managed

If asset custody is managed weakly, the following often occurs:

- badges are lost or exposed externally
- credentials are forgotten in private environments
- offboarding becomes difficult
- the responsibility chain becomes unclear
- laptops leave the facility without control
- tokens lack a clear owner
- traceability is poor during incidents
- exfiltration risk increases

---

# Recommended Next Steps

## 1. Create Asset Classification

Divide assets into clear classes, for example:

- standard credential
- privileged credential
- managed endpoint
- restricted endpoint
- removable media

## 2. Build Custody Workflows

Define processes for:

- issuance
- return
- deviation
- revocation
- recovery
- loss
- offboarding

## 3. Map Controls to Asset Type

Determine which controls apply to:

- badges
- tokens
- admin laptops
- user laptops
- removable media

## 4. Define Response Levels

Create clear levels for:

- anomalous movement
- failure to return
- suspected credential misuse
- unauthorized device separation

## 5. Add Audit & Review

Decide:

- who reviews custody events
- how often assets are recertified
- how deviations should be followed up
- how inventory should be performed

---

# Final Note

A strong asset custody model not only reduces the risk of loss, but also raises the security level by making asset movement, use, and ownership visible and controllable.

The central principle in this model is:

> **Security-critical assets must be under active control, not merely assumed control.**
