# FAQ – High-Security Facility Concept

> Vanliga frågor och korta svar om High-Security Facility Concept, dess syfte, avgränsning, relation till Zero Trust och praktiska användning.

---

## What is this?

High-Security Facility Concept är en konceptuell modell för högsäker teknisk miljö där fysisk säkerhet, zonlogik, credentials, devices, privilegierad åtkomst, incidenthantering, recovery och governance behandlas som delar av samma säkerhetssystem.

---

## Is this a product?

Nej.

Detta är inte en färdig produkt utan ett koncept, ett designunderlag och ett ramverk för vidare säkerhetsarkitektur, diskussion och förädling.

---

## Is this an implementation guide?

Nej.

Dokumentationen beskriver principer, modeller och riktning, men är inte en färdig implementationsspecifikation.

Verklig implementation skulle kräva:

- miljöspecifika krav
- specialistgranskning
- teknisk detaljering
- policyarbete
- operativ anpassning
- juridisk och regulatorisk anpassning där relevant

---

## What is the core idea?

Kärnidén är att hög säkerhet inte bara beror på vem som har access, utan också på:

- var personen befinner sig
- hur personen kom dit
- vilken zon som nås
- vilken enhet som används
- vilken credential som används
- om aktiviteten sker i rätt kontext
- hur avvikelser, incidenter och recovery hanteras

---

## What makes this concept different?

Några av de mest särskiljande delarna är:

- sekventiell zonaccess
- credential custody som säkerhetskontroll
- device location som säkerhetsparameter
- tydlig separation mellan normalyta och skyddad teknikzon
- separering mellan vanlig användning och privilegierad åtkomst
- recovery och governance som del av konceptets kärna

---

## Is this a Zero Trust model?

Inte i klassisk eller snäv IT-bemärkelse.

Konceptet bygger primärt på:

- fysisk närvaro
- zonkontext
- rörelselogik
- enheters lokation
- credential custody i fysisk miljö

Det är därför mer korrekt att säga att modellen är **kompatibel med Zero Trust-principer**, snarare än att den enbart är en Zero Trust-modell.

---

## How does it relate to Zero Trust?

Zero Trust kan integreras i konceptet, men är inte dess enda eller primära utgångspunkt.

Konceptet utgår från fysisk och operativ kontext och tillför därför ett lager som ofta är svagare representerat i traditionella Zero Trust-implementationer.

Detta gäller särskilt:

- fysisk rörelse
- sekventiell zonvalidering
- credential custody i facilitymiljö
- device location som säkerhetsparameter
- skyddade tekniska zoner

Kort uttryckt:

- konceptet försöker inte ersätta Zero Trust
- konceptet förutsätter inte att Zero Trust är okänt
- konceptet tillför en starkare fysisk och operativ dimension till tillitsmodellen

---

## Does the concept assume organizations already know Zero Trust?

Ja, i praktiken.

Konceptet är inte byggt på antagandet att organisationer saknar kännedom om Zero Trust. I stället utgår modellen från att många redan känner till eller använder Zero Trust-principer i någon form.

Det unika här är inte att introducera Zero Trust som idé, utan att tillföra en facility-centrerad modell där fysisk närvaro, rörelselogik och enheters lokation får större betydelse.

---

## Why is physical presence so central?

Därför att i högsäker facilitymiljö är fysisk närvaro inte bara ett resultat av access, utan en del av tillitsbedömningen.

Det spelar roll:

- var personen är
- hur personen tog sig dit
- om närvaron är normal eller avvikande
- om rätt aktivitet sker i rätt zon

Detta gör fysisk kontext till en säkerhetsparameter, inte bara till bakgrundsinformation.

---

## Why is movement logic so important?

Därför att säkerhet inte bara handlar om att en dörr kan öppnas, utan också om hur någon rör sig genom miljön.

Sekventiell passage och rörelselogik gör det lättare att:

- förstå hur någon nådde en viss zon
- upptäcka avvikande rörelsemönster
- begränsa informella genvägar
- stärka spårbarhet i högklassade miljöer

---

## Why are badges and tokens treated so strictly?

Därför att badges, tokens och liknande objekt inte bara är praktiska verktyg, utan säkerhetsobjekt.

Om de lämnar kontrollerad miljö eller hanteras slarvigt ökar risken för:

- förlust
- exponering
- social engineering
- credential misuse
- svår offboarding
- oklar custody

Därför bygger konceptet på tydlig kontroll och aktiv custody.

---

## Why are devices treated as security objects?

Därför att devices bär:

- data
- identitet
- tillit
- åtkomstmöjlighet
- operativ risk

I högsäker miljö räcker det därför inte att bara se devices som arbetsverktyg. Deras placering, rörelse och användningskontext blir också säkerhetsrelevanta.

---

## Why is device location important?

Därför att en enhets säkerhetsbetydelse inte bara avgörs av dess konfiguration, utan också av var den befinner sig och i vilken kontext den används.

En enhet som används i fel zon, lämnar kontrollerad miljö eller rör sig på ett ologiskt sätt kan vara ett tecken på:

- policyavvikelse
- credential misuse
- otillåten dataexponering
- svag asset control
- förhöjd insider-risk

---

## Does the concept assume insider risk?

Ja.

Konceptet utgår från att risk inte bara finns utanför facilityn, utan även kan uppstå genom:

- misstag
- policyavvikelser
- genvägar
- credential misuse
- avvikande intern rörelse
- felaktig hantering av devices eller privilegier

Det gör insiderresistens till en viktig del av modellen.

---

## Why is privileged access separated so clearly?

Därför att administrativ åtkomst innebär högre risk än vanlig användning.

Konceptet behandlar därför admin som en egen trust class, med krav på:

- separata identiteter
- separata enheter
- stark autentisering
- tydligare loggning
- högre kontrollnivå
- governance review

---

## What is break-glass in this context?

Break-glass syftar på särskilt definierad emergency access när ordinarie åtkomstmodell inte räcker, till exempel vid allvarlig incident eller kritisk återställning.

I konceptet ska break-glass vara:

- uttryckligt definierad
- begränsad
- starkt skyddad
- loggad
- eftergranskad
- tydligt separerad från normal administration

---

## Why are technical zones treated differently from normal workspaces?

För att skyddade tekniska zoner inte är vanliga arbetsmiljöer.

De innehåller ofta kritisk infrastruktur, känsliga system eller funktioner där:

- mänsklig närvaro bör minimeras
- service måste vara syftesbunden
- maintenance och change måste styras
- incidenter måste hanteras kontrollerat
- recovery behöver vara planerad

---

## Is recovery really part of security here?

Ja.

I högsäker miljö räcker det inte att bygga stark kontroll för normal drift. Man måste också ha en säker modell för:

- credential loss
- systemfel
- adminproblem
- incidentläge
- break-glass
- återgång till normal drift

Recovery är därför en integrerad del av säkerheten, inte ett separat sidospår.

---

## Why is governance included in the core concept?

Därför att stark design utan tydligt ägarskap, review och undantagshantering sällan förblir stark över tid.

Governance behövs för att:

- tydliggöra ansvar
- hantera undantag
- recertifiera access och privilegier
- koppla incidentlärdomar tillbaka till modellen
- säkerställa att säkerhetsnivån inte urholkas gradvis

---

## Is this meant for all organizations?

Nej.

Konceptet är främst relevant för miljöer med höga skyddskrav, till exempel:

- skyddade serverhallar
- säkerhetsklassade driftmiljöer
- tekniska säkerhetszoner
- verksamheter med höga krav på OPSEC
- miljöer där insiderhot och avvikande rörelsemönster är realistiska risker

Det är inte primärt tänkt för:

- vanliga kontorsmiljöer
- lågfriktionsmiljöer
- generell standard-enterprise IT
- miljöer där stark governance inte kan upprätthållas

---

## Why is friction part of the concept?

I högsäker miljö är låg friktion inte alltid målet.

I vissa fall är det önskvärt att:

- access kräver flera steg
- credentials inte lämnar facilityn
- rörelse är kontrollerad
- adminvägar är separata
- högre risk kräver tydligt högre kontroll

Friktion används därför som en avsiktlig säkerhetsmekanism där skyddsvärdet motiverar det.

---

## Is the concept complete?

Nej, inte i betydelsen färdig slutmodell eller implementation.

Det är däremot en relativt mogen konceptskiss med dokumenterad struktur, tydlig riktning och flera kompletterande dokument inom arkitektur, policy, governance, recovery, use cases och diagram.

---

## What stage is the concept in?

Konceptet befinner sig i ett tidigt men strukturerat stadium.

Det finns nu bland annat:

- executive summary
- one-pager
- concept description
- FAQ
- diagrams
- assessment
- roadmap
- zone model
- privileged access model
- asset custody model
- maintenance model
- governance model
- policy baseline
- recovery model
- incident response model
- use cases

Det gör att konceptet är väl positionerat för vidare förädling.

---

## Can this be extended further?

Ja.

Naturliga nästa steg kan vara:

- fler diagram
- access review model
- exception handling model
- break-glass model
- visitor / contractor model
- policy refinement
- implementation-oriented design layers

---

## What is the shortest way to describe the concept?

Ett möjligt kort svar är:

> Ett facility-centrerat säkerhetskoncept där identitet, fysisk närvaro, rörelse, enheter, credentials, privilegier och recovery behandlas som delar av samma tillitsmodell.
