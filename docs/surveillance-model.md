# Surveillance Model – High-Security Facility Concept

> En modell för hur CCTV, termisk övervakning, anti-tamper-placering, roof security, 3D Threat Thinking och operativa incidentvyer kan integreras i en högsäker facilitymiljö.

---

## Document Information

| Field | Value |
|---|---|
| Document | Surveillance Model |
| Subject | High-Security Facility Concept |
| Type | Supporting Security Architecture Document |
| Status | Draft |
| Scope | CCTV, thermal surveillance, camera placement principles, anti-tamper logic, roof surveillance, incident focus views |
| Audience | Security architects, physical security planners, surveillance operators, facility planners, reviewers |

---

## Purpose

Detta dokument beskriver hur övervakning kan utformas som en integrerad del av **High-Security Facility Concept**.

Syftet är att formulera principer för:

- yttre CCTV-placering
- termisk övervakning / FLIR
- ömsesidig kameratäckning
- tamper-resistant och tamper-evident design
- roof security och taksensorering
- zonbaserade incidentvyer
- operativ användbarhet vid larm och incident

Målet är att övervakningssystemet inte bara ska “finnas”, utan vara utformat för att:

- upptäcka
- verifiera
- övervaka egna kontrollpunkter
- stödja snabb operatörsrespons
- bidra till spårbarhet, containment och recovery

---

# Surveillance Philosophy

Övervakning i en högsäker facility ska inte ses som en passiv inspelningsfunktion.

I denna modell är surveillance i stället:

- en aktiv säkerhetskontroll
- en del av facilityns trust architecture
- ett stöd för incidentdetektion och verifiering
- ett skydd även för andra skyddskontroller
- ett verktyg för snabb situationsförståelse under press

Det innebär att kameror inte bara ska ge generell täckning, utan också placeras och grupperas så att de:

- minskar blinda vinklar
- gör sabotage svårare
- övervakar egna kamerapositioner
- ger redundans
- stödjer snabb operativ fokus vid incident
- stödjer en rumslig hotmodell där intrång inte bara antas ske på marknivå

---

# 3D Threat Thinking in Surveillance

I denna modell utformas surveillance utifrån **3D Threat Thinking**.

Det innebär att hotbilden inte förstås som en platt eller tvådimensionell perimeterfråga, utan som en rumslig säkerhetsutmaning där intrång, närvaro och påverkan kan ske från flera riktningar och nivåer.

För surveillance innebär detta att kameralogik och sensorer inte bara ska täcka:

- entréer
- fasader
- marknära rörelsevägar

utan också ta höjd för:

- takaccess
- höjdrelaterade angreppsvägar
- ovanliga eller icke-linjära approach paths
- strukturellt förbisedda ytor
- sabotage mot själva övervakningssystemet

Detta gör att övervakningsmodellen blir bättre anpassad för högsäker miljö där angripare inte förväntas följa normala accessvägar.

---

# Core Principles

## 1. Surveillance Is Part of Security Control, Not Just Observation
Kamerasystemet ska behandlas som en aktiv del av säkerhetsmodellen, inte enbart som ett efterhandsstöd.

## 2. Cameras Should Help Protect Cameras
Kritiska kamerapositioner bör övervakas av andra kameror för att göra manipulation, täckning eller skadegörelse svårare att genomföra obemärkt.

## 3. Different Camera Types Have Different Roles
Standard CCTV och termiska sensorer / FLIR bör användas med olika men kompletterande syften.

## 4. External Coverage Should Be Designed for Tamper Resistance
Yttre kameror bör placeras så att sabotageförsök mot en enskild kamera kan observeras av andra sensorer eller kameror.

## 5. Roof Areas Are Security-Relevant Surfaces
Tak och takrelaterade accesspunkter ska behandlas som säkerhetsrelevanta ytor och inte som byggnadstekniska sidofrågor.

## 6. Operator Speed Matters
Övervakning måste kunna användas effektivt i incidentläge. Rätt information ska snabbt kunna visas utan tung manuell navigering.

## 7. Surveillance Should Follow Zone Logic
Kamerastruktur och kameravyer bör spegla facilityns säkerhetszoner och kritiska accesspunkter.

---

# Surveillance Layers

## Layer 1 – Standard CCTV
Standard CCTV används främst för:

- visuell bekräftelse
- identifikation
- händelseförlopp
- övervakning av monteringspunkter
- detektion av sabotage mot andra kameror
- uppföljning av rörelse runt fasad, entré och accesspunkter

## Layer 2 – Thermal / FLIR
FLIR eller annan termisk övervakning används främst för:

- perimeterdetektion
- mörkerkapacitet
- upptäckt vid låg sikt
- upptäckt av personer nära fasad eller yttre skyddslinje
- komplement till vanlig visuell övervakning
- detektion i ytor där traditionell visuell övervakning är svagare

## Layer 3 – Overwatch / Elevated Control
Högre placerade kameror används för:

- övergripande överblick
- övervakning av kritiska lägre kameror
- nedåtriktad kontroll av kameraområden
- extra vinkel vid sabotage, incident eller rörelse nära byggnad
- stöd för roof security och övervakning av höjdrelaterade ytor

---

# External CCTV Placement Model

## Design Intent

Yttre kameror ska inte enbart placeras för att “täcka hörn” eller ge generell perimeterbild.

I denna modell ska externa kameror även bidra till att övervaka:

- varandra
- sina monteringspunkter
- närliggande approach paths
- försök till fysisk manipulation eller skadegörelse

## Mutual Oversight Pairing

Ett rekommenderat mönster är att använda sidoplacerade kameror som visuellt korsövervakar varandra.

### Side Camera A
- placeras på ena sidan av byggnaden eller fasadytan
- riktas mot motsatt sida
- ska täcka fasadyta, rörelseväg och den andra kamerans position

### Side Camera B
- placeras på motsatt sida
- riktas tillbaka mot första sidan
- ska täcka fasadyta, rörelseväg och den första kamerans position

Detta skapar:

- ömsesidig övervakning
- bättre redundans
- högre motståndskraft mot sabotage mot enskild kamera
- bättre sannolikhet att fånga manipulation, täckning eller approach

## Elevated Overwatch Camera

En tredje kamera bör i kritiska lägen placeras högre upp, exempelvis nära takkant eller annan skyddad höjdposition.

Denna kamera ska:

- se ned mot de sidoplacerade kamerorna
- övervaka området där sabotage eller manipulation kan ske
- ge ytterligare vinkel för verifiering
- minska beroendet av endast två sidovyer

Detta skapar ett enklare men starkt anti-tamper-arrangemang där kameror inte lämnas oövervakade.

## Practical Interpretation

Målet är inte att varje byggnad alltid måste använda exakt samma geometri.

Målet är att kameraplacering ska följa principen:

- ömsesidig täckning
- övervakning av kamerapositioner
- minimering av enkelpunktsförlust
- förbättrad sabotageupptäckt

Detta bör därför ses som en designprincip, inte som en absolut layoutregel.

---

# FLIR / Thermal Camera Positioning

## Role of FLIR

Termiska kameror bör användas som ett kompletterande lager snarare än som ersättning för vanliga CCTV-kameror.

De är särskilt användbara för:

- perimeterövervakning i mörker
- upptäckt av rörelse vid låg eller varierande belysning
- övervakning av skuggade eller svårbelysta ytor
- tidig indikation på närvaro nära fasad eller yttre skyddslinje
- stöd för upptäckt i rumsliga angreppsvägar där visuell kamera inte alltid räcker

## Corner Placement

I denna modell kan termiska kameror med fördel placeras i byggnadens hörn, där de kan bidra med:

- bred perimeteröversikt
- värmebaserad detektion från flera riktningar
- stöd till vanlig CCTV
- förbättrad upptäckt i ytterområden

Till skillnad från standard-CCTV, som i vissa fall bör placeras för ömsesidig anti-tamper-övervakning, kan FLIR i högre grad användas för att förstärka perimeterdetektion från hörnpositioner.

## Sensor Complementarity

Standard CCTV och FLIR ska ses som kompletterande:

- CCTV ger bättre visuell verifiering och detalj
- FLIR ger bättre upptäckt i vissa ljus- och väderförhållanden

Tillsammans ger de:

- bättre upptäckt
- bättre verifiering
- bättre robusthet i varierande förhållanden

---

# Roof Security and Elevated Access Surveillance

## Roof as a Security-Relevant Surface

Taket ska i högsäker miljö behandlas som en säkerhetsrelevant yta, inte som en neutral byggnadskomponent.

Det betyder att taket ska förstås som en möjlig:

- intrångsväg
- sabotageyta
- observationspunkt
- åtkomstväg till skyddade strukturer
- bypass av traditionell marknära perimeterlogik

## Why Roof Security Matters

I vissa högriskmiljöer kan angripare använda ovanliga eller asymmetriska intrångsvägar, inklusive takaccess.

Därför ska säkerhetsmodellen inte utgå från att hot enbart kommer via:

- huvudentréer
- marknivå
- förväntade accesspunkter

I stället måste även höjdrelaterade och strukturellt förbisedda vägar behandlas som realistiska riskytor.

## Roof Access Hardening

Takrelaterade öppningar och accesspunkter bör utformas med starkt skydd.

Det kan inkludera:

- förstärkta takluckor eller servicetillträden
- tamper-resistant accesspunkter
- fördröjande barriärer
- kontrollerade övergångspunkter mellan tak och inre ytor
- strukturell förstärkning där hotbilden motiverar det

Principen är att även om någon når taket ska detta inte innebära enkel eller direkt vidareaccess till skyddad inre miljö.

## Roof Sensors

Takytor och kritiska takaccesspunkter bör kunna sensoreras.

Exempel på relevanta kontrollmekanismer:

- rörelsedetektion
- närvarodetektion
- tamper-sensorer på luckor eller accesspunkter
- vibrationsindikering där det är relevant
- larmkoppling för oplanerad aktivitet på tak

Det viktiga är att taket får:

- detektion
- larmbarhet
- verifieringsmöjlighet
- operativ responskoppling

## Roof Surveillance

Övervakningen av tak bör stödjas genom:

- höjdplacerade kameror
- relevanta siktlinjer mot takkant och åtkomstvägar
- termiska sensorer där det förbättrar upptäcktsförmågan
- kameravinklar som kan verifiera aktivitet på eller mot tak

Oplanerad närvaro på tak i högsäker miljö bör som huvudregel behandlas som stark avvikelse tills motsatsen verifierats.

---

# Tamper-Resistant and Tamper-Evident Surveillance

Full tamper-proof övervakning är sällan realistisk.

Därför bör modellen i första hand sträva efter att vara:

- tamper-resistant
- tamper-evident

Det betyder att kamerasystemet ska utformas så att manipulation blir:

- svårare att genomföra
- lättare att upptäcka
- lättare att verifiera i efterhand

## Tamper-Resistant Measures
Exempel på principer:

- korsövervakning mellan kameror
- högt placerade overwatch-kameror
- skyddade monteringspunkter där möjligt
- flera vinklar mot kritiska angreppspunkter
- kombination av visuell och termisk detektion
- övervakning av roof access och höjdrelaterade ytor

## Tamper-Evident Measures
Exempel på principer:

- sabotageförsök fångas av annan kamera
- plötslig kameraförlust kopplas till larm eller operatörsindikering
- händelseförlopp kan rekonstrueras från fler än en kameravinkel
- aktivitet mot takrelaterade kontrollpunkter blir synlig i logik och övervakning

---

# Surveillance by Zone and Function

Övervakning bör organiseras utifrån facilityns zoner och kritiska funktioner, inte enbart utifrån tekniska kameranamn.

Det innebär att kameror bör kopplas till områden som exempelvis:

- entré
- reception
- man-trap
- perimeter north / south / east / west
- roof
- loading / service access
- technical access
- internal control zone
- protected technical zone

Detta förbättrar:

- operativ användbarhet
- incidentfokus
- utbildning av operatörer
- gemensam begreppsanvändning mellan säkerhet, drift och ledning

---

# Rapid Incident Focus Presets

## Purpose

Vid incident ska operatör inte behöva bygga sin situationsbild manuellt från grunden.

Systemet bör därför stödja fördefinierade kameravyer eller presets kopplade till särskilda områden och funktioner.

## Example: Entrance Focus

Om en incident upptäcks vid entrén ska operatören snabbt kunna aktivera en förkonfigurerad vy som visar:

- alla relevanta entrékameror
- närliggande fasadkameror
- eventuell termisk täckning
- approach paths mot entrén
- övergripande vy över närliggande zon

Detta bör kunna ske genom en mycket snabb operativ handling, exempelvis en dedikerad knapp eller preset-aktivering.

## Example: Roof Focus

Om aktivitet eller larm uppstår på taket ska operatören snabbt kunna växla till en roof preset som visar:

- relevanta takkameror
- närliggande övervakningskameror
- taknära FLIR- eller termiska feeds där sådana finns
- närliggande fasadvyer som kan fånga approach eller flyktväg
- åtkomstpunkter mellan tak och inre struktur

## Benefits

Fördefinierade incidentvyer förbättrar:

- responstid
- fokus
- situationsförståelse
- förmåga att samordna åtgärder
- minskad kognitiv belastning vid stress

## Recommended Preset Examples

Följande typer av zon- eller funktionspresets bör övervägas:

- Entrance
- Reception
- Man-Trap
- Perimeter North
- Perimeter South
- Roof
- Loading / Service Access
- Technical Access
- Internal Security Corridor
- Protected Technical Zone
- Emergency Evacuation View

---

# Operator Usability Under Pressure

Övervakningssystem i högsäker miljö måste fungera under stress, inte bara i normaldrift.

Det innebär att designen bör stödja:

- snabb växling mellan relevanta vyer
- logiska kameragrupper
- tydliga namn och zonetiketter
- enkel eskalering från generell vy till fokusvy
- minimerad tid för att hitta rätt kameror

En övervakningslösning som tekniskt sett har många kameror men som är långsam att använda under incident ger lägre operativt värde.

---

# Incident Integration

Surveillance ska vara integrerad med incidentarbetet och inte leva som ett isolerat sidospår.

Kameradata och kameravyer bör kunna stödja:

- snabb verifiering av larm
- bedömning av rörelse eller närvaro
- containment-beslut
- operatörsstöd till väktare eller responsfunktion
- efteranalys och rekonstruktion
- recovery och återgång till normal drift

---

# Governance Considerations

Surveillance-modellen bör också styras genom tydlig governance.

Detta bör inkludera:

- definierat ägarskap för kameralogik och placering
- återkommande review av kameratäckning
- review av blinda zoner och sabotageexponering
- kontroll av att presets fortfarande motsvarar verklig layout
- dokumenterade principer för ändringar i kamerastruktur
- samordning mellan fysisk säkerhet, IT, facility och incidentansvariga

---

# Design Boundaries

Detta dokument beskriver inte:

- exakta kameramodeller
- specifik linstyp eller sensorval
- inspelningspolicy i detalj
- lagringstid / retention i detalj
- juridiska eller regulatoriska krav för kameraövervakning
- fullständig installationsritning
- fullständig byggteknisk projektering av takskydd

Dessa delar kräver separat projektering, juridisk bedömning och miljöspecifik anpassning.

---

# Summary

Surveillance i denna modell handlar inte bara om att spela in vad som händer.

Det handlar om att bygga en övervakningsarkitektur som:

- stöder facilityns trust model
- skyddar även sina egna kontrollpunkter
- använder både visuell och termisk detektion
- minskar sabotageexponering
- tar höjd för hot i flera rumsliga dimensioner
- inkluderar tak och höjdrelaterade accessvägar i hotmodellen
- ger operatörer snabb fokus vid incident
- stärker detektion, verifiering och spårbarhet

Den centrala idén är:

> Övervakning ska inte bara se vad som händer runt byggnaden, utan också bidra till att skydda själva övervakningssystemet, täcka hot i 3D och ge snabb, användbar situationsförståelse när något faktiskt händer.
