# Zone Model – High-Security Facility Concept

> En modell för hur säkerhetszoner, sekventiell passage, rörelselogik, spatial hotförståelse och kontrollerad övergång mellan miljöer kan användas i en högsäker facility.

---

## Document Information

| Field | Value |
|---|---|
| Document | Zone Model |
| Subject | High-Security Facility Concept |
| Type | Core Architecture Document |
| Status | Draft |
| Scope | Zonstruktur, passage, movement logic, avvikelsehantering, roof-aware zoning, skyddade övergångar |
| Audience | Security architects, facility planners, physical security specialists, technical leads, reviewers |

---

## Purpose

Detta dokument beskriver hur facilityn delas in i säkerhetszoner och hur rörelse mellan dessa zoner kan kontrolleras inom **High-Security Facility Concept**.

Syftet är att definiera en modell där:

- zoner representerar olika skyddsvärden
- passage sker sekventiellt och kontrollerat
- rörelsemönster i sig är säkerhetsrelevanta
- vissa övergångar kräver särskild kontroll eller containment
- avvikelser kan upptäckas och hanteras
- hotmodellen förstås rumsligt och inte bara i två dimensioner

Zonmodellen är en central del av konceptets trust architecture eftersom fysisk närvaro, tillåten rörelse och platsbunden kontext påverkar hur tillit bedöms.

---

# Why a Zone Model Exists

I högsäker miljö räcker det inte att veta att någon “har access”.

Det är också viktigt att förstå:

- vilken zon personen befinner sig i
- hur personen nådde zonen
- om rörelsen följer förväntad sekvens
- om närvaron är normal i den aktuella miljön
- om rätt aktivitet sker på rätt plats
- om någon har nått en känslig yta via en ovanlig eller icke-förväntad väg

Utan zonlogik riskerar facilityn att reduceras till en samling enskilda dörrar och behörigheter utan tydlig fysisk tillitsmodell.

---

# Design Philosophy

## Zones Represent Trust Context
En zon är inte bara ett område i byggnaden, utan en säkerhetskontext med egna regler, förväntningar och skyddskrav.

## Movement Has Security Meaning
Hur någon rör sig genom facilityn är säkerhetsrelevant, inte bara var personen slutligen befinner sig.

## Access Should Be Progressive
Tillgång till mer känsliga områden ska normalt kräva passage genom tidigare kontrollpunkter och inte kunna ske genom ologiska genvägar.

## Some Transitions Need Stronger Control
Övergångar mellan vissa zoner kräver högre säkerhetsnivå, starkare verifiering, containment eller särskild syftesprövning.

## Zones Must Reflect Real Risk, Not Just Floor Plans
Zonstrukturen ska bygga på skyddsvärde, funktion, rörelserisk och angreppsyta — inte bara på byggnadens fysiska ritning.

## Spatial Threat Thinking Matters
Hot mot facilityn ska inte förstås som enbart marknära eller tvådimensionella. Zonmodellen ska därför ta höjd för rumsliga angreppsvägar, inklusive tak, höjdrelaterade ytor och strukturellt förbisedda accesspunkter.

---

# 3D Threat Thinking in the Zone Model

Zonmodellen i detta koncept bygger på **3D Threat Thinking**.

Det innebär att facilityn inte enbart delas in efter rum, korridorer och entréer på marknivå, utan att även andra rumsliga ytor och åtkomstvägar kan behöva behandlas som säkerhetsrelevanta zoner eller zonnära riskytor.

Detta inkluderar exempelvis:

- tak
- takaccesspunkter
- höjdrelaterade servicevägar
- interna vertikala förbindelser
- ovanliga bypass-vägar mellan yttre och inre miljö

Den praktiska poängen är att skyddet inte får utgå från att angripare alltid rör sig enligt byggnadens avsedda användningsmönster.

Zonmodellen ska därför kunna stödja en hotförståelse där intrång kan ske:

- från sidan
- ovanifrån
- genom strukturellt svaga övergångar
- via ovanliga men högpåverkande accessvägar

---

# Core Zone Types

Följande zonkategorier är exempel på hur facilityn kan struktureras.

## 1. External Perimeter Zone
Yttre område runt byggnaden där närvaro, approach och perimeterbeteende kan observeras.

Typiska egenskaper:
- första upptäcktsyta
- stöd för CCTV och FLIR
- fordon- och personrörelse nära byggnad
- tidig indikation på avvikande aktivitet

## 2. Entry Control Zone
Område där initial access verifieras.

Typiska egenskaper:
- reception eller bevakad entré
- första identitetskontroll
- besöksstyrning
- möjlighet till tidig avvisning eller eskalering

## 3. Controlled Transition Zone
Övergångszon mellan lägre och högre kontrollerad miljö.

Typiska egenskaper:
- man-trap eller motsvarande passagekontroll
- sekventiell verifiering
- containment-möjlighet
- tydlig gräns mellan mer öppen och mer skyddad yta

## 4. Internal Controlled Zone
Intern zon med begränsad men normal verksamhetsrörelse.

Typiska egenskaper:
- arbetsytor eller interna passager
- kontrollerad närvaro
- inte full fri rörelse
- förväntad men inte obegränsad aktivitet

## 5. High-Security Zone
Zon med högre skyddsvärde där närvaro ska vara mer restriktiv, mer motiverad och tydligare spårbar.

Typiska egenskaper:
- starkare passagekrav
- lägre tolerans för avvikelser
- starkare syftesbundenhet
- högre krav på eskort, loggning eller kontroll

## 6. Protected Technical Zone
Skyddad teknisk miljö där mänsklig närvaro normalt ska vara begränsad, motiverad och särskilt kontrollerad.

Typiska egenskaper:
- kritisk infrastruktur
- högre krav på teknisk, fysisk och operativ kontroll
- begränsad serviceaccess
- tydlig koppling till maintenance, privileged access och incidenthantering

## 7. Roof and Elevated Access Zone
Takyta eller annan höjdrelaterad yta som i högsäker miljö ska behandlas som en säkerhetsrelevant accessyta, inte som en neutral byggnadskomponent.

Typiska egenskaper:
- låg förväntad normalnärvaro
- stark avvikelsekaraktär vid oplanerad aktivitet
- behov av sensorer, övervakning och förstärkta accesspunkter
- koppling till 3D Threat Thinking och ovanliga intrångsvägar

---

# Sequential Zone Access

En central princip i modellen är att högre skyddszoner normalt ska nås genom korrekt sekvens.

Det betyder att en person eller aktivitet bör kunna förstås i relation till tidigare passage genom relevanta kontrollpunkter.

Exempel:

- external perimeter → entry control
- entry control → controlled transition
- controlled transition → internal controlled zone
- internal controlled zone → high-security zone
- high-security zone → protected technical zone

Detta stärker:

- spårbarhet
- tillitsbedömning
- upptäckt av ologisk närvaro
- containment vid avvikelse

Sekventiell passage betyder inte att alla rörelser måste vara identiska, men att säkerhetsmodellen ska kunna skilja mellan:

- normal förväntad väg
- godkänt undantag
- ologisk eller misstänkt väg

---

# Zone Transitions

Övergången mellan zoner är ofta viktigare än själva zonytan.

Därför ska vissa övergångar ses som egna säkerhetskontroller.

## Low-to-Medium Control Transition
Övergångar från mer öppen till mer kontrollerad yta kräver grundläggande verifiering och tydlig passagekontroll.

## Medium-to-High Security Transition
Övergångar till högsäker zon bör kräva starkare kontroll, högre säkerhetstolerans och tydligare koppling till syfte.

## High-to-Technical Transition
Övergång till skyddad teknikzon ska vara särskilt strikt eftersom närvaro där kan ha hög konsekvens.

## Roof-to-Interior Transition
Övergångar mellan tak och inre miljö ska i högsäker facility behandlas som särskilt känsliga, eftersom de kan utgöra ovanliga bypass-vägar för intrång.

Sådana övergångar bör:

- förstärkas strukturellt
- sensoreras
- övervakas
- ge larm vid oplanerad aktivitet
- inte möjliggöra direkt och okontrollerad vidarepassage

---

# Movement Logic

Rörelse i facilityn ska förstås som en säkerhetssignal.

Det innebär att systemet bör kunna skilja mellan:

- normal rörelse
- ovanlig men legitim rörelse
- avvikande rörelse
- potentiellt fientlig eller otillåten rörelse

## Normal Movement
Rörelse som följer förväntad väg, roll och syfte.

## Unusual but Legitimate Movement
Rörelse som avviker från vardagsmönster men är planerad, godkänd eller förklarbar.

## Suspicious Movement
Rörelse som saknar tydlig förklaring, bryter sekvens eller når fel zon vid fel tid.

## High-Risk Movement
Rörelse som indikerar försök att bypassa kontroll, nå skyddad yta via fel väg eller kombinera fysisk närvaro med misstänkt syfte.

---

# Roof-Aware Movement Logic

I en modell som bygger på 3D Threat Thinking måste rörelse även kunna förstås i relation till höjd och ovanliga accessvägar.

Det innebär att:

- aktivitet på tak normalt ska ha mycket låg baslinje
- oplanerad närvaro på tak bör betraktas som stark avvikelse
- rörelse från roof zone mot inre struktur ska behandlas som högriskhändelse
- roof-related access ska kunna särskiljas från marknära normaltrafik

Detta gör att hotmodellen blir mindre beroende av tvådimensionell perimeterlogik.

---

# Containment and Verification

När rörelse, passage eller zonnärvaro avviker från förväntad modell måste facilityn kunna reagera.

Det kan innebära:

- verifiering
- tillfällig containment
- manuell kontroll
- larmeskalering
- omdirigering
- incidentklassning

Containment behöver inte alltid vara dramatisk fysisk låsning, men modellen ska kunna bromsa eller markera osäker passage så att tillit inte ges automatiskt.

---

# Zone-Based Surveillance Integration

Zonmodellen ska samverka med surveillance-modellen.

Det innebär att kamera- och sensorlogik bör stödja:

- zonövergångar
- sekventiell passage
- upptäckt av avvikande rörelse
- roof-related incidenter
- snabb visuell verifiering av zonhändelser

Exempel på särskilt viktiga kamerastödjepunkter:

- entré
- reception
- man-trap
- övergång till high-security zone
- övergång till protected technical zone
- roof access points
- taknära ytor och höjdrelaterade åtkomstpunkter

---

# Zone Integrity

Zonintegritet betyder att en zon faktiskt beter sig som den säkerhetsnivå den påstår sig vara.

Det innebär att zonintegritet inte bara beror på dörrar eller lås, utan också på:

- passagekontroll
- rörelselogik
- surveillance
- sensorering
- avvikelsehantering
- disciplin i undantagshantering
- skydd mot ovanliga bypass-vägar

Om ologiska vägar in i en zon tolereras förlorar zonen en del av sitt skyddsvärde även om formell accesskontroll finns.

---

# Exception Handling

Alla verkliga facilitymiljöer har undantag.

Det kan exempelvis gälla:

- service
- maintenance
- räddningsinsats
- tillfällig omledning
- särskilt godkänd takaccess
- recovery-läge

Dessa undantag måste dock behandlas som just undantag och inte bli informell normalitet.

Undantag bör därför:

- vara dokumenterade
- vara godkända
- vara tids- eller syftesbegränsade
- vara spårbara
- kunna granskas i efterhand

---

# Governance Implications

Zonmodellen kräver governance för att behålla sin styrka över tid.

Detta innefattar bland annat:

- tydligt ägarskap för zonstruktur
- definierade regler för passage mellan zoner
- återkommande review av zonindelning
- review av undantag och bypass-mönster
- kontroll av att roof-related riskytor fortsatt hanteras
- samordning mellan fysisk säkerhet, surveillance, drift och governancefunktioner

---

# Design Boundaries

Detta dokument beskriver inte:

- full byggnadsteknisk projektering
- exakta dörr- eller låsspecifikationer
- fullständig brand- eller utrymningslogik
- juridiska krav per jurisdiktion
- full implementation av sensorsystem
- detaljerad bemanningsmodell

Dessa delar kräver separat projektering, specialistarbete och miljöspecifik anpassning.

---

# Summary

Zonmodellen i **High-Security Facility Concept** handlar inte bara om att dela in en byggnad i olika områden.

Den handlar om att skapa en säkerhetsarkitektur där:

- plats har betydelse
- rörelse har betydelse
- övergångar har betydelse
- avvikelser kan upptäckas
- högre skyddsvärde kräver tydligare sekvens
- även tak och höjdrelaterade ytor behandlas som relevanta delar av hotmodellen

Den centrala idén är:

> En högsäker facility blir starkare när zoner inte bara definieras geografiskt, utan fungerar som aktiva tillitskontexter där rörelse, övergång, avvikelse och rumslig hotförståelse hänger ihop.
