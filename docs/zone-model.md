# Zone Model – High-Security Facility Concept

> Zonstruktur, passersekvenser, rörelselogik och avvikelsehantering för en högsäker teknisk anläggning.

---

## Document Information

| Field | Value |
|---|---|
| Document | Zone Model |
| Subject | High-Security Facility Concept |
| Type | Concept Design / Security Zoning Model |
| Status | Draft |
| Scope | Physical zones, movement rules, access progression, anomaly handling |
| Audience | Security architects, facility planners, physical security teams, IT security leads |

---

## Purpose

Detta dokument beskriver en konceptuell **zonmodell** för en högsäker teknisk anläggning där fysisk rörelse betraktas som en del av den övergripande trust-modellen.

Målet är att definiera:

- olika zonklassningar
- syftet med respektive zon
- vem som får tillträde
- hur passage mellan zoner ska ske
- när sekventiell zonvalidering ska användas
- hur avvikelser ska upptäckas och hanteras

---

## Design Principles

Zonmodellen bygger på följande principer:

- **Defense in Depth**  
  Flera lager av fysisk kontroll används, inte en enda barriär.

- **Progressive Trust**  
  Högre känslighet kräver högre tillit och striktare kontroll.

- **Sequential Validation**  
  I högklassade zoner kontrolleras inte bara *om* någon har tillträde, utan även *hur* personen tog sig dit.

- **Role-Based Access**  
  Tillträde styrs av roll, ansvar och behov.

- **Anomaly Detection**  
  Avvikelser i rörelsemönster ska kunna upptäckas tidigt.

- **Controlled Exceptions**  
  Undantag får endast ske via dokumenterad och godkänd process.

- **Emergency Overrides**  
  Nödlägen ska kunna överstyra ordinarie zonlogik på ett säkert sätt.

---

# Zone Structure

## Zone A – Public Entry Zone

### Purpose
Första mottagningspunkt för:
- entré
- besökare
- reception
- initial identitetskontroll
- yttre screening

### Typical Characteristics
- lägsta skyddsnivå inom facilityn
- kan innehålla gästytor
- alltid kontrollerad övergång till nästa zon
- ingen tillgång till interna resurser eller känsliga system

### Typical Allowed Roles
- reception staff
- security staff
- escorted visitors
- internal staff under inpassering

### Security Controls
- reception desk
- initial ID check
- visitor handling
- badge issue / badge retrieval
- CCTV / monitoring
- controlled transition to next zone

---

## Zone B – Controlled Reception / Guest Transition Zone

### Purpose
Övergångszon mellan offentlig entré och intern miljö.

Kan användas för:
- gästväntan
- säkerhetsbriefing
- uthämtning/återlämning av badges
- första man-trap eller kontrollerad passage

### Typical Characteristics
- fortfarande relativt låg klassning
- mer kontrollerad än Zone A
- inga känsliga verksamheter ska exponeras här

### Typical Allowed Roles
- internal staff
- reception/security staff
- escorted visitors
- approved contractors under escort

### Security Controls
- badge validation
- man-trap / controlled door sequencing
- escort assignment
- visitor registration
- optional biometric or secondary identity control

---

## Zone C – Internal Office Zone

### Purpose
Intern arbetszon för normal verksamhet.

Exempel:
- kontorsytor
- mötesrum för intern personal
- administrativa funktioner
- låg till medelhög intern känslighet

### Typical Characteristics
- endast för intern personal och godkända besök under kontroll
- ingen direkt åtkomst till högklassade teknik- eller säkerhetszoner utan vidare kontroll

### Typical Allowed Roles
- internal staff
- selected support functions
- escorted visitors in limited scope

### Security Controls
- badge-controlled access
- movement logging
- CCTV in key corridors
- restricted access to higher zones
- optional anti-tailgating controls in transitions

---

## Zone D – Restricted Administrative / Leadership Zone

### Purpose
Känsligare administrativ zon.

Exempel:
- ledningsytor
- känsligare mötesrum
- säkerhetsadministration
- beslutstunga eller förtroendekänsliga funktioner

### Typical Characteristics
- högre klassning än normal intern arbetszon
- övergången hit markerar skiftet från normal intern access till striktare skyddsmodell
- sekventiell zonvalidering kan börja här eller från nästa nivå beroende på facility policy

### Typical Allowed Roles
- leadership
- approved administrators
- selected security-cleared personnel
- escort-controlled visitors only when justified

### Security Controls
- stricter badge access
- access logging
- stronger escort policy
- possible biometric factor
- transition control toward high-security operational zones

---

## Zone E – High-Security Technical / Administrative Operations Zone

### Purpose
Skyddad zon för tekniska eller privilegierade funktioner.

Exempel:
- IT support
- admin operations
- systems administration
- privileged technical work
- säkerhetsnära supportfunktioner

### Typical Characteristics
- högklassad intern zon
- endast för personal med legitimt behov
- sekventiell zonvalidering bör gälla från denna nivå om den inte redan aktiveras i Zone D
- avvikelse från normal passageordning ska betraktas som säkerhetshändelse

### Typical Allowed Roles
- IT admins
- security-cleared technical staff
- authorized support personnel
- escorted maintenance personnel under approved work order

### Security Controls
- badge + stronger identity validation
- full movement logging
- anti-tailgating controls
- escort enforcement where applicable
- anomaly detection on sequence deviation
- restricted onward transition to Zone F

---

## Zone F – Critical Security / OPSEC / Protected Technical Zone

### Purpose
Facilityns högst skyddade zon(er).

Exempel:
- säkerhetsfunktioner
- OPSEC-relaterade verksamheter
- känslig administration
- kritisk nätverks- eller serverinfrastruktur
- skyddad teknisk utrustning

### Typical Characteristics
- högsta interna skyddsnivå
- minimal mänsklig närvaro
- strikt tillträdeskontroll
- avvikelsehantering ska vara omedelbar
- endast högsta trust-nivåer får tillträde

### Typical Allowed Roles
- highly trusted technical staff
- security team
- specifically authorized admins
- approved maintenance staff under strict supervision and work order

### Security Controls
- strongest badge validation
- multi-factor identity assurance
- strict sequence enforcement
- full logging and alerting
- escort requirement where applicable
- highly restricted dwell time depending on purpose
- service / maintenance activity under controlled process

---

# Sequential Zone Validation

## Concept

Sequential zone validation innebär att tillträde till en högre klassad zon inte endast avgörs av användarens behörighet, utan även av att användaren har passerat tidigare relevanta zoner i korrekt ordning.

Exempel på avsedd sekvens:

`A -> B -> C -> D -> E -> F`

En användare med tillgång till Zone F ska alltså inte kunna "hoppa in" i Zone F utan att passersystemet också kan verifiera korrekt rörelse genom nödvändiga föregående zoner.

---

## Purpose of Sequential Validation

Syftet är att:

- förhindra informella genvägar
- synliggöra avvikande rörelsemönster
- höja säkerhetsvärdet i accessloggar
- minska risken för otillåten transit mellan känsliga zoner
- stödja anomalidetektion och eskortkrav

---

## Where It Should Apply

Sekventiell validering bör **inte nödvändigtvis** användas i hela facilityn.

Rekommenderad tillämpning:
- **Zone A / B:** normal accesskontroll
- **Zone C:** intern kontroll men begränsad sekvenslogik
- **Zone D:** övergångspunkt där sekventiell validering kan börja
- **Zone E / F:** full sekventiell validering

Detta minskar onödig friktion i öppnare eller mer vardagliga zoner, samtidigt som högklassade områden får starkare kontroll.

---

# Example Access Paths

## Standard Internal Staff
Allowed path:
`A -> B -> C`

Not allowed:
- direct access to E or F
- unapproved transition into D without role-based authorization

---

## Leadership / Executive Staff
Allowed path:
`A -> B -> C -> D`

May not automatically access:
- E
- F

Unless separately authorized.

---

## IT Admin Staff
Allowed path:
`A -> B -> C -> D -> E`

Additional approval required for:
`F`

---

## Security / OPSEC Personnel
Allowed path:
`A -> B -> C -> D -> E -> F`

With strict logging and stronger anomaly handling.

---

## Maintenance / Contractor Personnel
Allowed path:
- must be explicitly defined by work order
- typically escorted
- limited to exact required zones
- no standing right to free movement

Example:
`A -> B -> C -> E`

Only when:
- approved
- logged
- escorted where required
- tied to maintenance/change activity

---

# Deviation Handling

## What Counts as a Deviation

Exempel på avvikelse:

- användare försöker nå Zone E utan korrekt tidigare passage
- användare syns i Zone F utan registrerad sekvens genom D/E
- användare försöker använda genväg eller odefinierad transitzon
- badge används i ologisk ordning
- rörelsemönster avviker från tillåten rollprofil

---

## Recommended Response Model

Vid sekvensavvikelse bör systemet kunna:

1. **Flagga händelsen**
2. **Begränsa vidare passage**
3. **Skicka larm till säkerhet**
4. **Kräva manuell verifiering**
5. **Eskortera eller följa upp användaren enligt policy**

Detta bör vara standardmodell i högklassade zoner, särskilt i E/F.

---

## Escalation Levels

### Low Severity
Exempel:
- missad passage p.g.a. tekniskt fel
- oklar logik i lågklassad zon

Åtgärd:
- logga
- verifiera
- återställ vid behov

### Medium Severity
Exempel:
- användare försöker passera utan korrekt sekvens i högre zon
- oplanerat rörelsemönster

Åtgärd:
- blockera vidare passage
- larma säkerhet
- manuell kontroll

### High Severity
Exempel:
- användare registreras i högklassad zon utan giltig trust path
- tydlig misstanke om policybrott, tailgating eller credential misuse

Åtgärd:
- omedelbart larm
- säkerhetseskort
- incidenthantering
- åtkomstbegränsning tills utredning är klar

---

# Role-Based Pathing

Sekventiell zonvalidering ska inte bygga på att **alla** måste röra sig exakt likadant.

I stället bör systemet definiera:

- godkända vägar per roll
- godkända vägar per arbetsuppgift
- särskilda regler för gäster, konsulter och maintenance
- vilka zonövergångar som är normala respektive onormala

Detta minskar falsklarm och gör avvikelsehantering mer meningsfull.

---

# Escort Model

Escortkrav bör användas i följande situationer:

- besökare i interna eller högre klassade zoner
- maintenance personnel utan ordinarie fri rörelse
- konsulter i känsliga teknikzoner
- avvikelse från passersekvens
- tillfälliga undantag från ordinarie policy

Escort innebär att:
- ansvarig person är utsedd
- rörelse är begränsad till godkänd yta
- vistelsetid är kontrollerad
- aktiviteten är kopplad till syfte eller arbetsorder

---

# Technical Zone Considerations

I högklassade tekniska zoner gäller ytterligare principer:

- minimal mänsklig närvaro
- kort vistelsetid
- arbete ska vara syftesbundet
- större förändringar ska ske under change control
- serviceinsatser ska vara planerade, loggade och verifierbara

Detta gäller särskilt i zoner som motsvarar serverhallar, skyddad nätinfrastruktur eller annan kritisk teknisk miljö.

---

# Emergency Mode

## Principle
Nödläge ska alltid kunna överstyra ordinarie zonlogik där människors säkerhet kräver det.

## Requirements
- utpassage får inte blockeras av sekvenslogik i nödläge
- evacuation mode ska kunna aktiveras centralt
- avvikande rörelsemönster under nödläge ska markeras som nödlägeshändelse, inte som ordinarie policybrott
- systemet måste kunna återställas kontrollerat efter nödläge

---

# Audit & Logging Requirements

För att zonmodellen ska ge verkligt säkerhetsvärde bör följande loggas:

- inpassering per zon
- utpassering per zon
- misslyckade passageförsök
- sekvensfel
- escort events
- maintenance-related access
- emergency overrides
- manuella återställningar och säkerhetsingripanden

Loggar bör vara:
- tidsstämplade
- kopplade till identitet
- kopplade till zon
- korrelerbara med CCTV, incidentlogg och access approval

---

# Recommended Policy Statements

## Example Policy 1
Tillträde till högklassade zoner ska inte endast baseras på behörighet, utan även på verifierad passage genom föregående godkända zoner enligt användarens roll och syfte.

## Example Policy 2
Avvikelse från tillåten passersekvens i zoner klassade som D och högre ska utlösa säkerhetshändelse, begränsa fortsatt passage och kräva manuell verifiering enligt fastställd rutin.

## Example Policy 3
Besökare, konsulter och underhållspersonal ska endast få tillträde till definierade zoner enligt arbetsorder, eskortkrav och tidsbegränsad behörighet.

## Example Policy 4
Nödläge ska kunna överstyra normal sekventiell zonlogik för att säkerställa säker utpassage, utan att förlora revisionsbarhet.

---

# Key Risks if Poorly Implemented

Om zonmodellen implementeras dåligt finns risk för:

- för många falsklarm
- otydliga undantag
- osäker resetlogik
- överdriven friktion i lågklassade zoner
- personal som skapar informella bypasser
- låg tillit till systemet
- svårhanterad nödlägesfunktion

Därför bör modellen:
- börja enkelt
- införas där skyddsvärdet är högst
- stödjas av tydlig policy och utbildning
- revideras utifrån faktiskt beteende och incidenter

---

# Recommended Next Documents

För att vidareutveckla zonmodellen rekommenderas:

- `privileged-access.md`
- `asset-custody.md`
- `maintenance-model.md`
- `incident-response.md`
- `roadmap.md`

---

# Final Note

Zonmodellen är en av de starkaste delarna i detta koncept. Rätt implementerad ger den inte bara bättre fysisk säkerhet, utan också bättre spårbarhet, bättre anomalidetektion och starkare koppling mellan fysisk rörelse och trust-nivå.

Det centrala värdet ligger i att facilityn inte endast kontrollerar **vem** som får tillträde, utan även **hur** personer, credentials och enheter rör sig genom den skyddade miljön.
