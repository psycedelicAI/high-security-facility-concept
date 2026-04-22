# Recovery Model – High-Security Facility Concept

> Konceptuell modell för återställning, fallback, reservrutiner och kontrollerad återgång till normal drift i en högsäker teknisk anläggning.

---

## Document Information

| Field | Value |
|---|---|
| Document | Recovery Model |
| Subject | High-Security Facility Concept |
| Type | Security Operations / Recovery Architecture Concept |
| Status | Draft |
| Scope | Recovery flows, fallback logic, break-glass alignment, credential loss, system recovery, return to normal operations |
| Audience | Security architects, infrastructure leads, facility planners, operations teams, governance owners |

---

## Purpose

Detta dokument beskriver en konceptuell modell för **recovery** inom en högsäker teknisk anläggning.

Målet är att säkerställa att miljön inte bara är hårt skyddad, utan också kan:

- återställas på ett säkert sätt
- hantera avbrott och fel i kontrollsystem
- fortsätta fungera under avvikande förhållanden
- återgå till normal drift utan att säkerheten tappas
- stödja incidenthantering utan att skapa okontrollerade undantag

---

## Why Recovery Matters

Ju mer kontrollerad och restriktiv en miljö är, desto viktigare blir recovery.

Utan recovery riskerar en högsäker modell att bli:

- operativt skör
- beroende av informella nödlösningar
- svår att återställa efter incident
- sårbar för credential loss eller systemfel
- stark i normaldrift men svag i avvikelseläge

Recovery behövs därför för att säkerställa att:
- skyddsnivån kan bibehållas även under störning
- fallback inte blir permanent bypass
- återställning är styrd, dokumenterad och revisionsbar

---

# Recovery Objectives

Recovery-modellen ska säkerställa att:

- kritiska funktioner kan återställas under kontrollerade former
- förlorade eller otillgängliga credentials kan hanteras utan okontrollerad access
- fel i passersystem eller identitetssystem inte leder till kaos eller improvisation
- privilegierad återställning sker via definierade vägar
- återgång till normal drift är verifierad
- nödlägesåtkomst inte blir vardaglig genväg

---

# Core Principles

## 1. Strong Security Requires Strong Recovery
En hög skyddsnivå är bara hållbar om det finns en säker väg tillbaka från:

- tekniska fel
- förlorade credentials
- incidenter
- felaktiga spärrar
- operativa avvikelser

---

## 2. Recovery Must Be Defined Before It Is Needed
Recovery får inte bygga på improvisation.

Det ska finnas definierade modeller för:
- vem som får besluta
- vilka vägar som får användas
- hur åtkomst återställs
- hur undantag dokumenteras
- hur återgång till normal drift sker

---

## 3. Recovery Is Not the Same as Removing Controls
Återställning ska inte innebära att säkerheten överges.

Recovery ska i stället:
- ersätta normal kontroll med kontrollerad reservlogik
- vara tidsbegränsad
- vara starkt loggad
- vara kopplad till tydligt ansvar

---

## 4. Recovery Must Be Reviewable
Alla recovery-relaterade aktiviteter ska kunna granskas i efterhand.

Det gäller särskilt:
- break-glass-användning
- tillfälliga accessundantag
- credential reset
- återöppnade vägar
- manuell override i fysisk eller logisk säkerhet

---

## 5. Return to Normal Must Be Explicit
Återgång till normal drift eller ordinarie kontrollmodell ska aldrig vara implicit.

Den ska:
- beslutas
- verifieras
- loggas
- dokumenteras
- kunna granskas i efterhand

---

# Recovery Domains

## 1. Credential Recovery
Exempel:
- förlorad badge
- förlorad YubiKey
- skadad token
- otillgänglig smartcard-lösning
- blockerad adminidentitet

---

## 2. Access Path Recovery
Exempel:
- passersystem fungerar inte
- sekventiell zonlogik felar
- fysisk kontrollpunkt är otillgänglig
- användare fastnar i felaktigt accessläge
- adminväg är inte tillgänglig

---

## 3. Device Recovery
Exempel:
- trasig adminlaptop
- låst laptop
- device deviation har utlöst kontroll
- otillgänglig godkänd enhet
- behov av ersättningsenhet

---

## 4. Technical Operations Recovery
Exempel:
- change avbröts
- tekniskt arbete orsakade driftfel
- skyddad teknikzon måste återställas
- återgång från maintenance mode eller incident mode
- fysisk eller logisk kontroll måste återställas efter avvikelse

---

## 5. Governance Recovery
Exempel:
- otydlig ägare i pågående incident
- behov av snabb undantagsgodkännande
- tillfällig styrning under krisläge
- återgång från nödläge till ordinarie governance

---

# Recovery Scenarios

## Scenario 1 – Lost Badge

### Risk
Användare kan inte genomföra ordinarie fysisk access, eller badge kan utgöra risk om den tappats utanför kontroll.

### Recovery Expectations
- badge spärras omedelbart eller markeras som otillgänglig
- användaren får inte automatiskt fri ersättningsaccess utan kontroll
- tillfällig ersättningsprocess ska finnas
- incident eller avvikelse ska loggas
- ny credential ska utfärdas enligt definierad process

### Minimum Controls
- identitetsverifiering
- loggning
- tidsbegränsad ersättningsbehörighet
- återkallelse av temporär credential när ordinarie credential återställts

---

## Scenario 2 – Lost or Unavailable YubiKey / Token

### Risk
Ordinarie stark autentisering kan inte genomföras.

### Recovery Expectations
- token spärras eller markeras som komprometterad/otillgänglig
- alternativ recovery-väg ska kräva hög kontrollnivå
- privilegierad åtkomst ska inte “förenklas bort” för att lösa problemet
- tillfällig recovery-token eller reservmetod ska hanteras enligt strikt process

### Minimum Controls
- identitetsverifiering
- godkännande av relevant ansvarig
- stark loggning
- tidsbegränsad återställningsmetod
- eftergranskning vid privilegierad påverkan

---

## Scenario 3 – Failed Sequential Zone Validation

### Risk
Passersystemet anser att användaren saknar korrekt sekvens eller att zonlogiken blivit felaktig.

### Recovery Expectations
- vidare passage ska normalt begränsas
- säkerhetsfunktion ska kunna verifiera om det rör sig om:
  - systemfel
  - användarfel
  - faktisk avvikelse
- manuell reset eller kontrollerad återställning ska finnas

### Minimum Controls
- händelsen loggas
- säkerhetsverifiering krävs
- återställning ska vara spårbar
- fel får inte tysta framtida avvikelser

---

## Scenario 4 – Failed Admin Device

### Risk
Ordinarie privilegierad administration kan inte utföras eftersom godkänd adminenhet är otillgänglig.

### Recovery Expectations
- ersättningsenhet ska endast användas om den är godkänd för rollen
- improviserad admin från vanlig användarenhet ska inte vara standardlösning
- administrativ återställning ska ske via definierad reservväg

### Minimum Controls
- godkänd ersättningsenhet eller reservadminenhet
- identitetsverifiering
- loggad aktivering
- tids- eller sessionsbunden användning
- kontroll av att ersättningsvägen stängs efter användning

---

## Scenario 5 – Break-Glass Usage

### Risk
Ordinarie kontrollväg räcker inte för att återställa kritisk funktion eller hantera incident.

### Recovery Expectations
- break-glass ska användas endast vid legitimt och tydligt definierat behov
- användning ska vara strikt skyddad, loggad och eftergranskad
- break-glass får inte ersätta vardaglig adminmodell

### Minimum Controls
- tydlig aktiveringströskel
- loggning av vem, varför, när och hur
- begränsat scope där möjligt
- obligatorisk eftergranskning
- återställning till ordinarie modell snarast möjligt

---

## Scenario 6 – Passer/Identity System Failure

### Risk
Ett centralt kontrollsystem för fysisk access eller identitetsverifiering är delvis eller helt otillgängligt.

### Recovery Expectations
- fallback ska finnas för att möjliggöra kontrollerad fortsatt drift
- fallback får inte innebära fri access
- manuell kontrollkedja ska kunna ta över där nödvändigt

### Minimum Controls
- definierad manuell verifieringsprocess
- säkerhetspersonal eller annan ansvarig funktion deltar
- loggning av manuella beslut
- temporär drift i reducerat men kontrollerat läge
- kontrollerad återgång när systemet åter fungerar

---

## Scenario 7 – Device Locked Due to Policy Trigger

### Risk
En laptop har låsts på grund av avvikande rörelse, RFID-trigger eller annan policyhändelse.

### Recovery Expectations
- enheten ska inte återaktiveras automatiskt utan kontroll
- avvikelsen ska utredas innan full återställning
- återaktivering ska vara kopplad till identitet, enhet och bedömning

### Minimum Controls
- händelsen loggas
- säkerhets- eller IT-funktion verifierar kontext
- återställning godkänns enligt policy
- eventuell fortsatt övervakning kan krävas efter upplåsning

---

## Scenario 8 – Interrupted Change or Maintenance

### Risk
Ett planerat tekniskt arbete avbryts eller leder till ofullständig återgång till drift.

### Recovery Expectations
- zon eller system ska inte lämnas i oklart mellanläge
- rollback eller alternativ återställningsväg ska finnas
- tillfälliga undantag ska stängas när arbetet avslutas eller avbryts

### Minimum Controls
- change-id eller arbetsorder kopplas till recovery
- ansvarig funktion beslutar om rollback eller fortsatt recovery
- dokumenterad verifiering innan återgång till ordinarie läge

---

# Recovery Modes

## 1. Controlled Manual Recovery
Används när automatisk eller ordinarie väg inte fungerar, men där manuell process fortfarande kan ske under kontroll.

### Typical Use
- badge issue
- sekvensreset
- manuell accessverifiering
- manuell device release

---

## 2. Temporary Restricted Recovery
Används när funktion måste återställas snabbt men bara under reducerat och strikt kontrollerat läge.

### Typical Use
- tillfällig credential
- tillfällig adminväg
- fallback vid kontrollsystemfel
- tillfällig drift i begränsat läge

---

## 3. Emergency Recovery
Används vid kritisk incident eller allvarlig driftstörning där snabb återställning av kontroll eller funktion är nödvändig.

### Typical Use
- break-glass
- incidentrelaterad återtagning av kontroll
- allvarligt systemfel
- kritisk tillgänglighetsstörning

---

# Recovery Decision Model

## Principle
Recovery-beslut ska baseras på:
- risk
- påverkan
- känslighetsnivå
- vilken kontroll som fallerat
- möjlighet till säker verifiering
- behov av snabb återställning

---

## Suggested Decision Questions
- vad har gått fel?
- vilken kontroll är påverkad?
- kan normal process fortfarande användas?
- finns definierad fallback?
- krävs undantag eller emergency path?
- vem måste godkänna?
- hur återgår vi till normalmodell?

---

# Return to Normal Operations

## Purpose
Efter recovery måste facilityn eller systemet återgå till normal kontrollerad drift.

### This Should Include
- stängning av tillfälliga undantag
- återställning av ordinarie accessvägar
- verifiering att credentials och system åter är i rätt tillstånd
- kontroll av att reservrutiner inte ligger kvar
- dokumentation av vad som gjordes

---

## Verification Questions
- är ordinarie kontroll återställd?
- finns tillfälliga behörigheter kvar?
- finns tillfälliga devices eller tokens kvar i bruk?
- är incident- eller recovery-läge avslutat?
- är loggning komplett?
- krävs eftergranskning eller ytterligare åtgärd?

---

# Recovery Logging & Audit Requirements

Följande recovery-händelser bör loggas:

- credential recovery
- manuell accessåterställning
- sekvensreset
- tillfällig credential issuance
- admin device replacement
- break-glass usage
- fallback activation
- return to normal operations
- recovery-related approvals
- recovery-related exceptions

Loggning bör kunna korreleras mot:
- identitet
- enhet
- zon
- tid
- ansvarig funktion
- incident-id / change-id / exception-id

---

# Governance Alignment

Recovery-modellen ska vara direkt kopplad till governance-modellen.

Det innebär att följande ska vara definierat:
- vem som får besluta om recovery
- vem som får godkänna undantag
- vem som får aktivera break-glass
- vem som verifierar återgång till normal drift
- vem som granskar recovery-händelser i efterhand

---

# Recommended Policy Statements

## Example Policy 1
Alla recovery-relaterade åtgärder ska utföras enligt definierad reservprocess och får inte bygga på informell eller permanent bypass av ordinarie säkerhetskontroller.

## Example Policy 2
Förlorade eller otillgängliga credentials ska hanteras via kontrollerad recovery-process med identitetsverifiering, loggning och tidsbegränsad ersättningslogik där tillämpligt.

## Example Policy 3
Break-glass och andra nödlägesvägar ska vara starkt skyddade, sparsamt använda och obligatoriskt eftergranskade.

## Example Policy 4
Återgång till normal drift efter recovery ska vara explicit beslutad, verifierad och dokumenterad.

## Example Policy 5
Fallback-lösningar får endast användas under definierade förutsättningar och ska avvecklas så snart ordinarie kontrollmodell är återställd.

---

# Common Recovery Failures

Om recovery-modellen är svag uppstår ofta:

- improviserade reservlösningar
- informella undantag som blir permanenta
- svag spårbarhet i nödläge
- för stor beroende av enskilda personer
- förenklad access “bara för att få igång det”
- otydlig återgång till normal drift
- säkerhetsförsvagning efter incident

---

# Recommended Next Steps

## 1. Create Recovery Playbooks
Skapa konkreta playbooks för:
- lost badge
- lost token
- failed sequence
- failed admin device
- break-glass usage
- access control system failure
- locked endpoint due to policy event

## 2. Define Recovery Authorities
Bestäm:
- vem som får fatta vilka recovery-beslut
- vem som kan godkänna tillfälliga undantag
- vem som ansvarar för return to normal

## 3. Link Recovery to Other Models
Koppla recovery-modellen till:
- governance model
- privileged access model
- zone model
- maintenance model
- incident response model
- asset custody model

## 4. Define Return-to-Normal Criteria
Beskriv tydligt:
- vad som krävs för att lämna recovery-läge
- hur tillfälliga accesser stängs
- hur verifiering sker
- hur eftergranskning genomförs

## 5. Add Audit & Review Process
Bestäm:
- hur recovery-händelser granskas
- vilka som ska följas upp särskilt
- hur lärdomar förs tillbaka till modellen

---

# Final Note

I en högsäker miljö är recovery inte ett undantag från säkerhet — det är en del av säkerheten.

Den centrala principen i denna modell är därför:

> **Återställning ska vara kontrollerad, tidsbunden, spårbar och utformad för att återföra miljön till normal säker drift utan att skapa dolda bypasser.**
