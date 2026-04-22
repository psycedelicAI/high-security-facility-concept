# Governance Model – High-Security Facility Concept

> Konceptuell styrmodell för ansvar, ägarskap, godkännanden, undantag, revision och recertifiering inom en högsäker teknisk anläggning.

---

## Document Information

| Field | Value |
|---|---|
| Document | Governance Model |
| Subject | High-Security Facility Concept |
| Type | Security Governance / Operating Model Concept |
| Status | Draft |
| Scope | Ownership, approval, exceptions, review, recertification, control structure |
| Audience | Security architects, facility planners, governance leads, IT security leads, decision-makers |

---

## Purpose

Detta dokument beskriver en konceptuell **governance-modell** för High-Security Facility Concept.

Målet är att säkerställa att säkerhetsmodellen inte enbart består av tekniska och fysiska kontroller, utan även av tydlig styrning kring:

- vem som äger vad
- vem som godkänner vad
- hur undantag hanteras
- hur åtkomst granskas
- hur avvikelser följs upp
- hur ansvar fördelas mellan roller och funktioner

---

## Why Governance Matters

En högsäker modell kan vara tekniskt stark men ändå svag i praktiken om följande saknas:

- tydliga ägare
- definierade beslutspunkter
- ansvarsmatris
- undantagshantering
- recertifiering
- revisionsbarhet
- uppföljning av policyavvikelser

Governance behövs för att göra modellen:

- repeterbar
- beslutsbar
- mindre personberoende
- revisionsbar
- hållbar över tid

---

# Governance Objectives

Governance-modellen ska säkerställa att:

- varje säkerhetskontroll har en tydlig ägare
- varje zon, identitetstyp och tillgångskategori omfattas av ansvar
- tillträde inte ges utan tydlig beslutskedja
- undantag är kontrollerade, tidsbundna och spårbara
- privilegier recertifieras regelbundet
- incidenter och avvikelser följs upp
- modellen kan utvecklas utan att tappa kontroll

---

# Core Governance Principles

## 1. Ownership Must Be Explicit
Varje säkerhetsrelevant objekt eller kontroll ska ha en tydlig ägare.

Exempel:
- zoner
- badge-policy
- privileged access
- tokens
- adminenheter
- maintenance-processer
- exception workflows

---

## 2. Approval Must Be Role-Based
Godkännanden ska inte vara informella eller personberoende.

De ska vara:
- rollbaserade
- dokumenterade
- situationsanpassade
- kopplade till tydligt scope

---

## 3. Access Must Be Reviewable
Fysisk och logisk åtkomst ska gå att granska regelbundet.

Det gäller bland annat:
- zonbehörigheter
- adminprivilegier
- tillfälliga undantag
- konsult- och besökstillgång
- break-glass-tillgångar

---

## 4. Exceptions Must Be Controlled
Undantag är ibland nödvändiga, men de får inte bli dolda permanenta genvägar.

Undantag ska därför vara:
- motiverade
- tidsbegränsade
- godkända
- loggade
- eftergranskade

---

## 5. Governance Must Cover Both Physical and Logical Security
Styrningen ska omfatta både:
- fysisk access
- systemåtkomst
- asset custody
- tekniska zoner
- maintenance
- privileged access

---

# Governance Domains

## 1. Zone Governance
Styrning av:
- zonklassning
- tillträdesnivåer
- passersekvenser
- escortkrav
- avvikelsehantering i fysisk rörelse

### Governance Needs
- zonägare
- godkännandeflöden för fysisk access
- översyn av zonbehörigheter
- policy för sekvensavvikelse
- undantagshantering för tillfälliga passager

---

## 2. Identity & Credential Governance
Styrning av:
- badges
- tokens
- smartcards
- identitetsbindning
- credential lifecycle
- spärr och återtag

### Governance Needs
- credential ownership
- process för tilldelning
- process för återtag
- förlusthantering
- recertifiering av privilegierade credentials

---

## 3. Privileged Access Governance
Styrning av:
- adminroller
- adminidentiteter
- adminenheter
- förhöjd åtkomst
- break-glass

### Governance Needs
- tydlig rollkatalog
- ansvar för privilegietilldelning
- regelbunden översyn
- spårbarhet av användning
- särskild kontroll över högsta privilegier

---

## 4. Asset Governance
Styrning av:
- laptops
- tillgångsklasser
- enhetsrörelse
- RFID-relaterad policy
- lockers
- flyttbara media

### Governance Needs
- definierade asset owners
- policy för rörelse och förvaring
- inventering och avvikelseuppföljning
- recertifiering av känsliga tillgångar

---

## 5. Maintenance & Change Governance
Styrning av:
- serviceaktiviteter
- change approval
- tillträde till teknikzoner
- återgång till drift
- tekniska undantag

### Governance Needs
- change ownership
- godkännandekedja
- kontroll av deltagare
- verifiering efter arbete
- eftergranskning vid avvikelse

---

## 6. Incident & Recovery Governance
Styrning av:
- incidentmode
- recovery
- break-glass-användning
- avvikelsehantering
- återställningsbeslut

### Governance Needs
- definierade incidentroller
- beslutsrätt för undantag i kris
- eftergranskning av akuta avsteg
- tydlig väg tillbaka till normal drift

---

# Governance Roles

Nedan följer en konceptuell rollmodell. Exakta titlar kan anpassas till organisationens struktur.

---

## Security Governance Owner
Övergripande ägare av styrmodell och säkerhetsprinciper.

### Responsibilities
- äger säkerhetsramverket
- godkänner centrala policyer
- säkerställer att kontroller har utsedda ägare
- ansvarar för övergripande översyn och förbättring

---

## Facility Security Owner
Ägare av fysisk säkerhetsmodell.

### Responsibilities
- zonklassning
- fysisk accesspolicy
- reception / passersystem
- escortpolicy
- fysisk avvikelsehantering

---

## Identity & Credential Owner
Ägare av identitets- och credentialmodellen.

### Responsibilities
- badge lifecycle
- token lifecycle
- smartcards
- credential issuance
- credential revocation
- credential custody policy

---

## Privileged Access Owner
Ägare av privileged access-modellen.

### Responsibilities
- adminrollskatalog
- tilldelning av privilegier
- adminpolicy
- översyn av privilegierad åtkomst
- break-glass-modell

---

## Asset Owner / Endpoint Owner
Ansvarig för säkerhetskritiska klienter och tillgångar.

### Responsibilities
- laptopklasser
- device policy
- asset tracking
- förflyttningspolicy
- tekniska avvikelser kopplade till enheter

---

## Change Authority
Ansvarig för godkännande av större tekniskt arbete.

### Responsibilities
- change approval
- riskbedömning av större ingrepp
- kontroll av deltagare och scope
- verifiering av återgång till normal drift

---

## Audit / Review Function
Ansvarig för oberoende eller halvoberoende uppföljning.

### Responsibilities
- access review
- privilege review
- exception review
- policy compliance review
- avvikelseuppföljning

---

# Approval Model

## Principle
Godkännanden ska ske enligt tydliga nivåer beroende på:

- tillgångens känslighet
- zonens klassning
- privilegienivå
- tillfälligt eller permanent behov
- standardfall eller undantag

---

## Example Approval Categories

### Standard Access Approval
Gäller:
- normal tilldelning av låg- eller medelkänslig access
- standardzoner
- etablerade roller

### Elevated Access Approval
Gäller:
- högklassade zoner
- känsliga tekniska utrymmen
- privilegierade roller
- högre risk än normalt

### Exception Approval
Gäller:
- tillfälliga avsteg
- ovanliga accessvägar
- tillfällig device movement
- extra känsliga arbetsuppgifter

### Emergency Approval
Gäller:
- incident
- recovery
- break-glass
- brådskande återställning

---

# Access Review & Recertification

## Purpose
Tilldelad åtkomst får inte betraktas som permanent korrekt bara för att den en gång godkänts.

### Review Should Cover
- fysisk zonåtkomst
- privilegierade roller
- badges och credentials
- adminenheter
- tillfälliga undantag
- konsulter och externa roller
- break-glass-beredskap

---

## Review Principles
Recertifiering bör vara:
- regelbunden
- riskbaserad
- rollbaserad
- dokumenterad
- åtgärdsbar

---

## Example Review Questions
- behöver personen fortfarande denna tillgång?
- är rollen fortfarande relevant?
- används privilegiet faktiskt?
- finns tillfälliga undantag som blivit permanenta?
- finns credentials som borde spärras eller återtas?
- är tilldelad zonåtkomst fortfarande motiverad?

---

# Exception Handling Model

## Principle
Undantag ska vara synliga, inte informella.

### Every Exception Should Have
- tydlig motivering
- tydlig ägare
- tydlig giltighetstid
- tydligt scope
- tydligt godkännande
- tydlig eftergranskning

---

## Examples of Exceptions
- tillfällig passage utanför normal sekvens
- extern maintenance i högklassad zon
- tillfällig användning av särskild adminväg
- kontrollerad device movement utanför standardpolicy
- tillfällig access för recovery eller incidentarbete

---

## Expiry Principle
Undantag ska som huvudregel:
- upphöra automatiskt
- eller kräva aktiv omprövning

De ska inte glida över till permanent praxis.

---

# Auditability & Oversight

## Governance Requires Visibility
Styrning utan synlighet är inte verklig styrning.

### Oversight Should Include
- accessloggar
- change approvals
- privileged use review
- badge / credential anomalies
- device movement anomalies
- sequence deviation handling
- undantagshistorik

---

## Minimum Expectations
Det ska gå att svara på:
- vem beslutade?
- vem fick åtkomst?
- till vad?
- varför?
- under hur lång tid?
- enligt vilken process?
- med vilket undantag, om något?

---

# Offboarding Governance

Governance-modellen ska stödja snabb och kontrollerad offboarding.

## Minimum Requirements
- fysisk access spärras
- logisk access spärras
- badges återtas eller spärras
- tokens återtas eller spärras
- adminenheter återkallas
- tillfälliga undantag avslutas
- privilegierad åtkomst verifieras borttagen

---

## Governance Value
En stark governance-modell minskar risken för:
- kvarstående access efter avslutad roll
- glömda credentials
- informella restprivilegier
- personberoende offboarding

---

# Governance Metrics

För att styrningen ska kunna förbättras över tid bör vissa nyckeltal följas.

## Example Metrics
- antal aktiva privilegierade identiteter
- antal öppna undantag
- antal försenade recertifieringar
- antal badge-/credentialavvikelser
- antal sekvensavvikelser i zonmodell
- antal incidentrelaterade accessavsteg
- tid till revocation vid offboarding
- antal tillgångar utan tydlig owner

---

# Recommended Policy Statements

## Example Policy 1
Varje säkerhetsrelevant zon, identitet, credential och tillgång ska ha en tydligt utsedd ägare.

## Example Policy 2
Tilldelning av fysisk eller logisk åtkomst ska ske enligt definierade godkännandeflöden och vara spårbar till roll, syfte och beslut.

## Example Policy 3
Undantag från ordinarie säkerhetsmodell ska vara tidsbegränsade, godkända, loggade och obligatoriskt eftergranskade.

## Example Policy 4
Privilegierad åtkomst och högklassad fysisk åtkomst ska recertifieras regelbundet enligt riskbaserad modell.

## Example Policy 5
Offboarding ska omfatta både fysisk, logisk och asset-relaterad åtkomst och vara verifierad innan processen anses slutförd.

---

# Common Governance Failures

Om governance saknas eller är svag uppstår ofta:

- otydligt ägarskap
- permanenta undantag
- access som aldrig recertifieras
- privilegier utan verkligt behov
- bristande offboarding
- för stark personberoende drift
- bristande revisionsbarhet
- stark teknik men svag kontrollkedja

---

# Recommended Next Steps

## 1. Create Ownership Matrix
Dokumentera:
- vilka objekt som finns
- vem som äger dem
- vem som godkänner förändringar
- vem som granskar dem

## 2. Define Review Cycles
Bestäm:
- vad som ska recertifieras
- hur ofta
- av vem
- hur åtgärder följs upp

## 3. Build Exception Workflow
Skapa process för:
- begäran
- godkännande
- tidsgräns
- loggning
- eftergranskning

## 4. Link Governance to Other Models
Knyt denna modell till:
- zone model
- privileged access model
- asset custody model
- maintenance model
- incident / recovery model

## 5. Add Governance Reporting
Definiera:
- nyckeltal
- uppföljningsformat
- rapporteringsintervall
- ansvar för uppföljning

---

# Final Note

I en högsäker miljö är governance det som förvandlar starka kontroller till ett verkligt styrt system.

Den centrala principen i denna modell är:

> **Säkerhet ska inte bara vara stark — den ska också vara ägd, godkänd, granskningsbar och styrbar över tid.**
