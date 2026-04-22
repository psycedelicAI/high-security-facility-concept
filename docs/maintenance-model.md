# Maintenance Model – High-Security Facility Concept

> Konceptuell modell för service, underhåll, change-hantering och teknisk vistelse i skyddade tekniska zoner inom en högsäker anläggning.

---

## Document Information

| Field | Value |
|---|---|
| Document | Maintenance Model |
| Subject | High-Security Facility Concept |
| Type | Operations / Security Architecture Concept |
| Status | Draft |
| Scope | Service access, technical work, maintenance windows, change mode, protected technical zones |
| Audience | Security architects, infrastructure leads, facility planners, operations teams, physical security teams |

---

## Purpose

Detta dokument beskriver en konceptuell modell för hur **service, underhåll och förändringsarbete** ska hanteras i skyddade tekniska zoner inom en högsäker anläggning.

Målet är att säkerställa att:

- tekniskt arbete sker under kontrollerade former
- mänsklig närvaro i känsliga zoner begränsas
- skillnaden mellan normaldrift, service och större change är tydlig
- åtkomst till skyddad utrustning är behovsstyrd och spårbar
- tekniska miljöer skyddas utan att förlora drift- och återställningsförmåga

---

## Scope

Detta dokument omfattar:

- serverhallar
- nätverksrum
- skyddade tekniska utrymmen
- kritisk server- och nätverksutrustning
- fysisk teknisk åtkomst för service och underhåll
- maintenance windows
- change mode
- återgång till normaldrift

---

# Core Principles

## 1. Protected Technical Zones Are Not Normal Workspaces
Tekniska skyddszoner ska inte betraktas som vanliga arbetsmiljöer där människor vistas kontinuerligt.

De ska i stället ses som:
- kontrollerade driftmiljöer
- zoner för kortvarig teknisk åtkomst
- utrymmen där närvaro ska vara motiverad, tidsbegränsad och spårbar

---

## 2. Minimize Human Presence
Mänsklig närvaro i känsliga tekniska zoner ska hållas till ett minimum.

Det innebär att:
- onödiga fysiska besök ska undvikas
- fjärradministration föredras när säkerhet och drift tillåter det
- fysisk åtkomst ska kräva tydligt syfte
- längre arbeten ska ske under kontrollerade driftlägen

---

## 3. Separate Routine Service From Planned Change
Konceptet ska tydligt skilja mellan:

- **normaldrift**
- **kort serviceinsats**
- **planerad change**
- **incidentåtgärd**
- **recovery / återställning**

Varje typ av aktivitet ska ha egen kontrollnivå, egen logik och egna godkännandekrav.

---

## 4. Access Must Be Purpose-Bound
Teknisk åtkomst ska vara kopplad till:

- syfte
- arbetsorder
- change-begäran
- incident
- tidsfönster
- godkänd roll

Ingen fri eller otydlig rörelse i tekniska zoner ska accepteras.

---

## 5. Maintenance Is a Security Event
Fysiskt arbete i skyddad teknisk miljö ska betraktas som en säkerhetsrelevant aktivitet.

Det innebär att:
- aktivitet ska loggas
- identitet ska verifieras
- syfte ska dokumenteras
- avvikelse ska kunna upptäckas
- återgång till normaldrift ska vara kontrollerad

---

# Operating States

## 1. Normal Operations Mode

### Description
Facilityn kör i ordinarie driftläge.

### Characteristics
- minimal mänsklig närvaro i skyddade teknikzoner
- endast mycket begränsade serviceinsatser tillåtna
- inga större förändringar utan formell övergång till annat läge
- högsta skyddsnivå gäller för utrustning och access

### Typical Allowed Activities
- övervakad inspektion
- kort fysisk kontroll
- begränsade byten av enklare komponenter om policy tillåter
- incidentverifiering under strikt kontroll

---

## 2. Limited Service Mode

### Description
Avsett för korta, avgränsade tekniska uppgifter med låg förändringsgrad.

### Example Activities
- byte av SFP
- kontrollerat kabelbyte
- verifiering av fysisk anslutning
- enklare hårdvarukontroll
- begränsad supportinsats

### Characteristics
- kort vistelsetid
- tydligt definierat syfte
- endast godkända roller
- ingen bred systemförändring
- återgång till normaldrift utan full change-process om policy tillåter

### Security Requirements
- arbetsuppgift ska vara registrerad
- identitet ska verifieras
- åtkomst ska vara tidsbunden
- aktivitet ska loggas
- avvikelse ska kunna generera säkerhetshändelse

---

## 3. Planned Change Mode

### Description
Används när större tekniska förändringar ska utföras.

### Example Activities
- större kabelomläggning
- förändring av rackstruktur
- utbyte av kritisk utrustning
- planerat arbete som påverkar drift eller skyddsnivå
- förändringar som kräver avstängning eller kontrollerad påverkan på system

### Characteristics
- formell change-begäran
- tydligt godkännande
- definierat tidsfönster
- tydlig ansvarig person
- fördefinierad rollback eller återställningsstrategi

### Security Requirements
- change måste vara godkänd innan arbete påbörjas
- tillträde ska vara kopplat till change-id eller arbetsorder
- endast godkända personer får delta
- aktivitet ska loggas och kunna revideras
- återgång till normaldrift ska kräva verifiering

---

## 4. Incident Response Mode

### Description
Används vid säkerhetsincident, driftstörning eller annan händelse som kräver snabb teknisk åtkomst.

### Characteristics
- hög prioritet
- tillträde kan behöva beviljas snabbare än vid planerad change
- avsteg från normal process kan tillåtas under strikt dokumentation
- eftergranskning är obligatorisk

### Security Requirements
- incident ska registreras
- ansvarig funktion ska vara utsedd
- all avvikande åtkomst ska loggas
- eftergranskning ska ske
- eventuellt break-glass-flöde ska kunna användas enligt separat policy

---

## 5. Recovery Mode

### Description
Används när system, accessvägar eller facilityfunktioner måste återställas efter fel, incident eller planerad avstängning.

### Characteristics
- fokus på säker återställning
- vissa ordinarie begränsningar kan behöva justeras kontrollerat
- ska vara tydligt separerad från vanlig drift
- all aktivitet bör vara extra starkt dokumenterad

---

# Technical Zone Access Model

## General Rule
Tillträde till skyddade tekniska zoner ska endast ges när följande är uppfyllt:

- legitimt behov finns
- korrekt roll eller arbetsorder finns
- identitet har verifierats
- tidsfönster är definierat
- zon- och rörelsepolicy följs
- avsedd aktivitet är dokumenterad

---

## Access Preconditions
Före tillträde till känslig teknikzon bör följande vara tydligt:

- vem som går in
- varför personen går in
- vilken utrustning som berörs
- vilken zon som ska nås
- hur länge vistelsen förväntas pågå
- vem som ansvarar för aktiviteten

---

## Escort Considerations
Escort kan krävas när:
- besökare eller tredje part ska in i teknikzon
- maintenance utförs av extern part
- tillträde sker utanför normala mönster
- känslighetsnivån motiverar extra kontroll

---

# Human Presence Controls

## Short-Duration Principle
I känsliga tekniska zoner bör mänsklig vistelse vara:

- kort
- motiverad
- planerad
- övervakad eller spårbar
- begränsad till uppgiften

---

## Dwell Time Awareness
Längre vistelsetid än förväntat kan utgöra:
- operativ avvikelse
- säkerhetsavvikelse
- tecken på felaktig arbetsplanering
- potentiellt incidentunderlag

Därför bör modellen kunna stödja:
- registrerad starttid
- förväntad sluttid
- avvikelseflagga vid överskriden vistelsetid

---

# Maintenance Workflow

## Example High-Level Flow
1. behov identifieras
2. aktivitet klassas som service, change, incident eller recovery
3. rätt arbetsorder eller change skapas
4. roller och deltagare verifieras
5. tillträde beviljas inom definierat fönster
6. arbete utförs
7. aktivitet loggas
8. resultat verifieras
9. zon eller system återgår till normaldrift enligt process
10. eftergranskning sker där det krävs

---

# Logging & Audit Requirements

Följande bör loggas för tekniskt arbete i skyddade zoner:

- identitet på deltagare
- tid för inpassering
- tid för utpassering
- berörd zon
- typ av aktivitet
- change-id, incident-id eller arbetsorder
- godkännande
- avvikelser
- återgång till drift
- eventuella säkerhetseskorter
- manuella overrides

Loggar bör kunna korreleras med:
- accessloggar
- CCTV
- change management-system
- incidentregister
- asset records

---

# Safety & Environmental Considerations

## Principle
Skydd av teknik får aldrig ske utan tydlig modell för människors säkerhet.

I tekniska skyddszoner med särskilda miljöförutsättningar måste följande vara definierat:

- vem som får vistas där
- under vilka förutsättningar
- hur länge
- när normal drift måste avbrytas inför större arbete
- hur säkert inträde och utträde sker
- hur nödläge hanteras

---

## Operational Interpretation
För vissa skyddade teknikzoner kan det vara rimligt att:
- endast kortvarig vistelse tillåts under normal drift
- större arbeten kräver att system ställs i annat driftläge eller stängs av
- all teknisk åtkomst sker under strikt process och ansvar

---

# Change Approval Expectations

Planerat förändringsarbete bör tydligt ange:

- vad som ska göras
- varför det ska göras
- vilka system eller zoner som påverkas
- vilka personer som deltar
- när arbetet ska ske
- vilka risker som finns
- hur rollback eller återställning ska ske
- vem som godkänt arbetet

---

# Return to Service / Return to Normal Operations

Efter underhåll eller change bör återgång till normal drift inte vara implicit.

Den bör kräva:
- verifiering att arbete är slutfört
- bekräftelse att zonen åter är i rätt säkert läge
- verifiering att system fungerar som avsett
- stängning av eventuella tillfälliga undantag
- dokumentation av avvikelser eller restpunkter

---

# Recommended Policy Statements

## Example Policy 1
Skyddade tekniska zoner ska inte användas som ordinarie arbetsytor och fysisk vistelse ska begränsas till godkända, syftesbundna aktiviteter.

## Example Policy 2
Tekniskt arbete i högsäker zon ska klassificeras som service, change, incident eller recovery och hanteras enligt respektive processmodell.

## Example Policy 3
Större förändringar i skyddade tekniska miljöer ska endast utföras under godkänt change-fönster och med definierad ansvarig funktion.

## Example Policy 4
Återgång till normal drift efter tekniskt arbete ska vara verifierad, dokumenterad och revisionsbar.

## Example Policy 5
Tillträde till skyddad teknikzon ska vara tidsbundet, behovsstyrt och kopplat till arbetsorder, incident eller change.

---

# Common Risks If Poorly Managed

Om maintenance-modellen är svag uppstår ofta:

- oplanerad eller otydlig fysisk närvaro i teknikzon
- arbete utan tydligt syfte eller godkännande
- osäker skillnad mellan snabb service och större change
- dålig återgång till normaldrift
- låg revisionsbarhet
- säkerhetskontroller som kringgås under tekniskt arbete
- personberoende drift i stället för styrd process

---

# Recommended Next Steps

## 1. Define Activity Classes
Skapa tydlig klassning för:
- normal inspection
- limited service
- planned change
- incident response
- recovery activity

## 2. Build Technical Access Workflow
Dokumentera:
- hur tillträde begärs
- hur det godkänns
- hur det loggas
- hur vistelsetid hanteras
- hur avvikelser eskaleras

## 3. Formalize Change Model
Definiera:
- change ownership
- approval chain
- rollback expectations
- technical verification
- return-to-service criteria

## 4. Add Safety Layer
Beskriv:
- tillåten mänsklig närvaro
- nödlägeslogik
- inträdes- och utträdesregler
- hur skyddad teknikzon säkras inför större arbete

## 5. Link With Other Models
Koppla maintenance-modellen till:
- zonmodell
- privileged access-modell
- asset custody-modell
- incident response
- governance och revision

---

# Final Note

I en högsäker teknisk anläggning är maintenance och change inte bara driftfrågor — de är säkerhetsfrågor.

Den centrala principen i denna modell är därför:

> **Tekniskt arbete i skyddad miljö ska vara syftesbundet, tidsbundet, kontrollerat och fullt revisionsbart.**
