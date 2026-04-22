# High-Security Facility Concept

> Ett koncept för en högsäker teknisk anläggning med fokus på fysisk säkerhet, zonindelning, accesskontroll, OPSEC, privileged access, endpoint security och insiderresistens.

---

## Overview

**High-Security Facility Concept** är en konceptuell säkerhetsmodell för skyddade tekniska miljöer där hög friktion, strikt rörelsekontroll och stark credential custody är en del av designmålet.

Konceptet riktar sig främst mot miljöer som:

- skyddade serverhallar
- säkerhetsklassade driftmiljöer
- tekniska säkerhetszoner
- verksamheter med höga krav på OPSEC
- miljöer där fysisk och logisk säkerhet måste fungera som ett sammanhängande system

Det här projektet beskriver inte bara en samling kontroller, utan ett **samlat säkerhetskoncept** där:

- människor
- enheter
- zoner
- identiteter
- rörelsemönster
- privilegier
- drift och underhåll

behandlas som delar av samma trust model.

---

## Core Design Ideas

### 1. Layered Security
Konceptet bygger på **defense in depth** med flera skyddslager, till exempel:

- fysisk perimeter
- reception och kontrollpunkter
- man-traps
- zonklassning
- badge- och identitetskontroller
- FIDO2 / YubiKey
- segmenterade klienter
- dedikerade adminenheter
- nätsegmentering
- asset tracking

### 2. Sequential Zone Access
Högre klassade zoner kräver att användaren passerat tidigare zoner i korrekt ordning.

Detta gör att systemet inte bara kontrollerar **om** någon har access, utan även:

- **hur personen tog sig dit**
- **om korrekt passersekvens följts**
- **om rörelsemönstret avviker från policy**

### 3. Credential Custody
Credentials ska vara under kontroll, inte spridda i privatlivet.

Exempel:
- badges lämnas kvar i facility
- säkerhetskritiska tokens hanteras med tydlig custody
- adminåtkomst sker från rätt enhet och rätt miljö

### 4. Protected Technical Zones
Teknikzoner, såsom serverhallar och känsliga driftmiljöer, behandlas annorlunda än vanliga arbetsytor.

Det innebär bland annat:
- begränsad mänsklig närvaro
- kontrollerade serviceinsatser
- tydlig change-hantering
- högre fysisk och logisk skyddsnivå

### 5. Role-Based Device Separation
Olika roller använder olika typer av enheter, med olika nivåer av tillit och åtkomst.

Exempel:
- admin laptops
- power user laptops
- standard laptops
- consultant devices

### 6. Insider & Exfiltration Resistance
Konceptet tar särskild hänsyn till:

- insiderhot
- policyavvikelser
- informella genvägar
- social engineering
- informationsläckage
- otillåten förflyttning av enheter

---

## Example Security Principles

- Least privilege
- Defense in depth
- Role separation
- Device separation
- Sequential access validation
- Credential custody
- OPSEC by design
- Controlled maintenance
- Protected admin paths
- High-friction access for high-trust zones

---

## Example Zone Model

| Zone | Purpose | Example Access Level |
|---|---|---|
| A | Entrance / guest-facing area | Public / escorted |
| B | Open meeting / reception support area | Low sensitivity |
| C | Internal office zone | Internal staff |
| D | Restricted leadership / sensitive admin zone | Approved staff only |
| E | IT / support / privileged operations | High trust personnel |
| F | Security / OPSEC / critical technical zone | Highest trust personnel |

> Sekventiell zonvalidering kan tillämpas från högre zonklasser, exempelvis D/E/F, där korrekt passersekvens är en del av säkerhetsmodellen.

---

## Example Concept Components

### Physical Security
- reception-controlled access
- badge custody
- man-traps
- fenced perimeter
- secure lockers
- controlled escort handling
- high-security technical zones

### Identity & Access
- badge-based entry
- biometrics where justified
- password + FIDO2/YubiKey
- dedicated admin authentication paths
- strong privileged access requirements

### Endpoint Security
- dedicated admin laptops
- segmented user device classes
- restrictions based on role
- controlled device movement
- asset visibility and policy-triggered lock events

### Operations & Maintenance
- service windows
- restricted technical access
- maintenance vs change mode separation
- controlled re-entry to protected zones
- supervised privileged activity

---

## What Makes This Concept Different

Det som särskiljer konceptet är kombinationen av:

- **fysisk säkerhet**
- **rörelselogik**
- **credential custody**
- **device trust**
- **privileged access discipline**
- **OPSEC**
- **insider-resilience**

Målet är inte bara att stoppa obehöriga från att komma in, utan att skapa en miljö där:

- rätt personer rör sig rätt väg
- rätt enheter används i rätt sammanhang
- credentials hålls under kontroll
- avvikelser blir synliga
- känsliga zoner skyddas både fysiskt och logiskt

---

## Assessment Summary

Konceptet har granskats som en tidig säkerhetsmodell för högsäker teknisk miljö.

### Current Assessment Score
# **88 / 100**

### Strong Areas
- defense in depth
- zonlogik och sekventiell passage
- insider threat / exfiltration resistance
- asset tracking och credential custody
- separation mellan normalyta och skyddad teknikzon

### Main Improvement Areas
- governance och ägarskap
- recovery och fallback-processer
- formell privileged access-modell
- revisionsbarhet
- operativ policyformalisering

> Se gärna separat bedömningsdokument för full review.

---

## Project Status

**Status:** Concept / Early Design  
**Maturity:** Strong concept, not yet production architecture

Detta repo bör ses som underlag för:

- vidare arkitektur
- policyutveckling
- designreview
- säkerhetsdiskussioner
- konceptvalidering

Inte som färdig implementationsspecifikation.

---

## Suggested Repository Structure

```text
.
├── README.md
├── docs/
│   ├── assessment.md
│   ├── zone-model.md
│   ├── privileged-access.md
│   ├── asset-custody.md
│   ├── maintenance-model.md
│   └── roadmap.md
