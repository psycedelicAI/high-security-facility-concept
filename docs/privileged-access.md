# Privileged Access Model – High-Security Facility Concept

> Conceptual model for privileged access in a high-security technical facility, with a focus on role separation, dedicated admin paths, strong authentication, control of admin sessions, and auditability.

---

## Document Information

| Field | Value |
|---|---|
| Document | Privileged Access Model |
| Subject | High-Security Facility Concept |
| Type | Security Architecture / Access Control Concept |
| Status | Draft |
| Scope | Privileged identities, admin workflows, admin devices, access elevation, auditability |
| Audience | Security architects, identity leads, infrastructure leads, facility security planners |

---

## Purpose

This document describes a conceptual model for **privileged access** in a high-security technical environment.

The goal is to define principles for:

- what types of privileged roles exist
- how privileged access should take place
- which devices and environments may be used
- how strong authentication should be applied
- how elevated rights should be controlled
- how traceability and audit should be ensured
- how emergency access should be handled

---

## Design Goals

The privileged access model should achieve the following:

- protect high-risk functions better than normal user access
- clearly separate administrative activity from everyday use
- make privileged activity person-bound, traceable, and auditable
- reduce the risk of credential misuse
- make lateral movement between roles and environments more difficult
- ensure that administration takes place from the correct environment, with the correct identity, under the correct conditions
- enable strict control without losing recovery capability

---

# Core Principles

## 1. Admin Is a Separate Trust Class

Administrative access must be treated as a **separate risk class**, not as an extension of normal user access.

This means that:

- admin identities must be separate from user identities
- administrative actions must have a higher level of control
- admin sessions must take place in a specially defined environment

---

## 2. No Privileged Access From Standard User Devices

Standard user devices must not be used for highly privileged administration.

Privileged access must be allowed only from:

- dedicated admin devices
- approved technical zones or defined admin paths
- environments with the correct level of protection, logging, and control

---

## 3. Strong Authentication Is Mandatory

Privileged access must require strong authentication.

Examples:

- password or passphrase
- FIDO2 / YubiKey
- potentially an additional factor in especially sensitive environments
- role- and context-bound control

---

## 4. Privileges Should Be Specific, Not Broad by Default

The main principle should be:

- least possible privilege
- time-limited access where possible
- role-bound administrative authorization
- as few permanent highly privileged rights as possible

---

## 5. Admin Activity Must Be Traceable

Every privileged action should, as far as possible, be attributable to:

- person
- device
- point in time
- purpose
- approval or change / reference
- affected system or zone

---

## 6. Emergency Access Must Exist, But Be Exceptional

Emergency access must exist, but it must:

- be strongly protected
- be used rarely
- be clearly defined
- generate immediate audit and follow-up

---

# Role Model

## Standard User

Standard user identity for daily use.

### Characteristics

- used for normal work tasks
- must not have privileged administrative rights
- must not be used for sensitive administrative functions

---

## Power User

Expanded but limited function for certain work tasks.

### Characteristics

- may have some elevated rights within a narrow scope
- must not replace a real admin role
- must not have broad infrastructure or security administration

### Example Use Cases

- application-adjacent operational tasks
- limited local system management
- approved technical specialist tasks

---

## Admin

Dedicated administrative role for technical or system-adjacent administration.

### Characteristics

- separate identity from normal user identity
- used only from a dedicated admin device
- strong authentication is mandatory
- access is restricted by responsibility and scope

### Example Areas

- server administration
- identity administration
- network administration
- system support in a high-security environment

---

## Security Admin

Especially sensitive admin role for security functions.

### Characteristics

- higher protection level than normal admin
- stricter access requirements
- only from defined secure environments
- enhanced audit and monitoring

### Example Areas

- security systems
- OPSEC-relevant functions
- access control systems
- logging and audit platforms

---

## Break-Glass / Emergency Role

Special emergency role used only when the standard model is insufficient.

### Characteristics

- used during incidents, serious disruption, or recovery need
- must be strongly protected
- must be separate from standard admin flows
- use must trigger immediate follow-up

---

# Privileged Device Model

## Dedicated Admin Devices

Privileged administration must only be performed from **dedicated admin devices**.

### Principles

- the admin device must not be an ordinary workstation
- the device must be used for administration, not everyday work
- separate roles should have separate device profiles where justified
- the device must be subject to a higher level of protection than normal clients

### Expected Controls

- strong login
- high hardening level
- clear logging
- limited software surface
- controlled network access
- clear linkage between user, device, and administrative function

---

## No Mixed-Use Principle

The same device should not be used for both:

- everyday communication
- normal web usage
- document handling
- privileged administration

This reduces the risk that a compromised everyday environment affects sensitive administrative flows.

---

# Authentication Model

## Standard Requirements for Privileged Access

Privileged access should require at minimum:

- personal administrative identity
- strong secret or passphrase
- FIDO2 / YubiKey or equivalent hardware-based factor
- approved admin device
- permitted network and zone context

---

## Contextual Requirements

For especially sensitive functions, additional requirements may apply, such as:

- special zone
- special admin path
- documented change ID or case reference
- additional approval
- monitored session

---

# Access Elevation Model

## Preferred Principle

Elevated rights should be granted according to the principle of:

- the right person
- the right role
- the right device
- the right time window
- the right purpose

---

## Permanent vs Temporary Privilege

### Permanent Privilege

Must be kept to a minimum and exist only where clearly justified.

### Temporary Privilege

Preferred where possible and should be:

- time-limited
- tied to a task or change
- clearly logged
- quickly revocable

---

## Scope Control

Privileges should, as far as possible, be limited by:

- system
- zone
- function
- time
- role
- responsibility

The goal is to avoid giving an account or role more power than the task requires.

---

# Session Control & Oversight

## Logging Expectations

Privileged activity should be correlatable with:

- user identity
- admin identity
- device
- login time
- action or task
- change ticket / approval
- affected system

---

## Oversight Principles

For especially sensitive actions, the model should support:

- clear session start and session end
- additional logging
- manual oversight where justified
- post-review of high-risk activities

---

## Administrative Intent

Before sensitive privileged actions are performed, it should be clear:

- what will be done
- why it will be done
- in which environment
- under which change or request
- by whom

This strengthens both traceability and accountability.

---

# Global Admin / Highest Privilege Considerations

## Design Position

The broadest possible privileges must be treated as **exceptions**, not as the normal way of working.

### Recommended Principles

- as few such identities as possible
- the strongest possible protection
- use only when there is a genuine need
- the highest level of logging and follow-up
- not used for routine administration if a lower level is sufficient

---

## Shared vs Personal Privileged Identity

A shared highly privileged identity may seem easy to control if it is used only in a monitored environment, but personally assigned privileged identities normally provide better:

- accountability
- audit trail
- attribution
- least privilege

The main principle should therefore be:

- personal admin identities in everyday use
- special emergency or break-glass identities as exceptions

---

# Break-Glass Model

## Purpose

Break-glass should be used when:

- the normal administrative path does not work
- an incident requires rapid restoration
- standard privileged identities are not sufficient
- critical access to systems must be regained

---

## Design Requirements

Break-glass must:

- be strongly protected
- be documented
- be separate from everyday administration
- be reviewed after every use
- be revocable, restorable, and recertifiable

---

## Governance Expectations

Every use of break-glass should be:

- justified
- logged
- reviewed
- reported to the relevant responsible function

---

# Administrative Zone Considerations

Privileged administration should be tied to defined zones and/or approved access paths.

Examples:

- a normal user zone must not provide direct admin capability
- sensitive administrative functions should require a higher-classified zone
- some functions should only be possible from a protected technical or administrative environment

This strengthens the relationship between:

- identity
- device
- physical context
- permitted action

---

# Auditability Requirements

For the model to be strong in practice, it should be possible to review:

- who requested privileged access
- who was granted privileged access
- from which device
- from which zone or admin path
- with which authentication level
- during which time period
- to which system
- for which purpose or change basis
- which deviations occurred

---

# Recovery & Fallback Considerations

The privileged access model must handle situations such as:

- lost YubiKey
- broken admin device
- unavailable standard admin path
- credential compromise
- need for rapid restoration during an incident

This requires clear playbooks and approved exception procedures.

---

# Recommended Policy Statements

## Example Policy 1

Privileged access must take place with a separate administrative identity and must not be performed from standard user devices.

## Example Policy 2

Administrative actions in a high-security environment must only be allowed from approved admin devices and within a defined physical and logical context.

## Example Policy 3

Strongly authenticated, person-bound, and auditable access must be the primary model for privileged administration.

## Example Policy 4

The broadest possible privileges must be treated as exceptions and used only when a lower privilege level is not sufficient.

## Example Policy 5

Break-glass access must be separately defined, strongly protected, and subject to mandatory post-review after every use.

---

# Common Risks If Poorly Designed

If the privileged access model is poorly implemented, the following often occur:

- shared admin accounts without clear accountability
- overly broad permanent rights
- admin activity from the wrong devices
- weak recovery capability
- low traceability
- overdependence on informal routines
- unclear boundary between user and admin activity

---

# Recommended Next Steps

## 1. Define Admin Role Catalog

Create a clear role catalog for:

- user
- power user
- admin
- security admin
- emergency / break-glass

## 2. Map Privileges to Scope

Describe:

- which systems belong to which role
- which roles require which device
- which privileges may be permanent versus temporary

## 3. Formalize Admin Device Classes

Document:

- which admin devices exist
- who may use them
- which protection levels apply
- how they differ from standard clients

## 4. Create Recovery Playbooks

Define processes for:

- lost token
- broken admin device
- blocked admin identity
- emergency access
- credential compromise

## 5. Establish Audit & Review Model

Determine:

- what must be logged
- how admin activity is reviewed
- how deviations are handled
- how privileges are recertified

---

# Final Note

Privileged access is one of the areas where the facility’s real security level is determined in practice. A strong physical environment can quickly be weakened if privileged access is not person-bound, controlled, and auditable.

The central principle of this model is therefore:

> **Privileged access must be separate, strongly protected, context-bound, and fully traceable.**
