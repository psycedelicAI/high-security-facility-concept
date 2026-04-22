# Privileged Access Model – High-Security Facility Concept

> Konceptuell modell för privilegierad åtkomst i en högsäker teknisk anläggning, med fokus på rollseparation, dedikerade adminvägar, stark autentisering, kontroll av adminsessioner och revisionsbarhet.

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

Detta dokument beskriver en konceptuell modell för **privilegerad åtkomst** i en högsäker teknisk miljö.

Målet är att definiera principer för:

- vilka typer av privilegierade roller som finns
- hur privilegierad åtkomst ska ske
- vilka enheter och miljöer som får användas
- hur stark autentisering ska tillämpas
- hur förhöjda rättigheter ska kontrolleras
- hur spårbarhet och revision ska säkerställas
- hur nödlägesåtkomst bör hanteras

---

## Design Goals

Den privilegierade åtkomstmodellen ska uppnå följande:

- skydda högriskfunktioner bättre än vanlig användaråtkomst
- tydligt separera administrativ aktivitet från vardagsanvändning
- göra privilegierad aktivitet personbunden, spårbar och revisionsbar
- minska risken för credential misuse
- försvåra lateral movement mellan roller och miljöer
- säkerställa att administration sker från rätt miljö, med rätt identitet, under rätt förutsättningar
- möjliggöra strikt kontroll utan att förlora recovery-förmåga

---

# Core Principles

## 1. Admin Is a Separate Trust Class
Administrativ åtkomst ska behandlas som en **egen riskklass**, inte som en förlängning av vanlig användaråtkomst.

Det innebär att:
- adminidentiteter ska vara separata från användaridentiteter
- administrativa åtgärder ska ha högre kontrollnivå
- adminsessioner ska ske i särskilt definierad miljö

---

## 2. No Privileged Access From Standard User Devices
Vanliga användarenheter ska inte användas för högprivilegierad administration.

Privilegerad åtkomst ska endast tillåtas från:
- dedikerade adminenheter
- godkända tekniska zoner eller definierade adminvägar
- miljöer med rätt skyddsnivå, loggning och kontroll

---

## 3. Strong Authentication Is Mandatory
Privilegerad åtkomst ska kräva stark autentisering.

Exempel:
- lösenord eller passphrase
- FIDO2 / YubiKey
- eventuellt ytterligare faktor i särskilt känsliga miljöer
- roll- och kontextbunden kontroll

---

## 4. Privileges Should Be Specific, Not Broad by Default
Huvudprincipen ska vara:
- minsta möjliga privilegium
- tidsbegränsad åtkomst när möjligt
- rollbunden administrativ behörighet
- så få permanenta högprivilegierade rättigheter som möjligt

---

## 5. Admin Activity Must Be Traceable
Varje privilegierad handling ska i möjligaste mån kunna kopplas till:

- person
- enhet
- tidpunkt
- syfte
- godkännande eller change/referens
- berört system eller zon

---

## 6. Emergency Access Must Exist, But Be Exceptional
Nödlägesåtkomst ska finnas, men:
- vara strikt skyddad
- användas sällan
- vara tydligt definierad
- generera omedelbar revision och uppföljning

---

# Role Model

## Standard User
Vanlig användaridentitet för daglig användning.

### Characteristics
- används för normala arbetsuppgifter
- ska inte ha privilegierade administrativa rättigheter
- får inte användas för känsliga administrativa funktioner

---

## Power User
Utökad men begränsad funktion för vissa arbetsuppgifter.

### Characteristics
- kan ha vissa förhöjda rättigheter inom snävt scope
- ska inte ersätta riktig adminroll
- ska inte ha bred infrastruktur- eller säkerhetsadministration

### Example Use Cases
- applikationsnära driftuppgifter
- begränsad lokal systemhantering
- godkända tekniska specialuppgifter

---

## Admin
Dedikerad administrativ roll för teknisk eller systemnära förvaltning.

### Characteristics
- separat identitet från vanlig användaridentitet
- används endast från dedikerad adminenhet
- stark autentisering obligatorisk
- åtkomst begränsas efter ansvar och scope

### Example Areas
- serveradministration
- identitetsadministration
- nätverksadministration
- systemsupport i högsäker miljö

---

## Security Admin
Särskilt känslig adminroll för säkerhetsfunktioner.

### Characteristics
- högre skyddsnivå än vanlig admin
- striktare åtkomstkrav
- endast från definierade säkra miljöer
- utökad revision och övervakning

### Example Areas
- säkerhetssystem
- OPSEC-relevanta funktioner
- accesskontrollsystem
- logg- och revisionsplattformar

---

## Break-Glass / Emergency Role
Särskild nödlägesroll som endast används när ordinarie modell inte räcker.

### Characteristics
- används vid incident, allvarlig störning eller recovery-behov
- ska vara hårt skyddad
- ska vara separat från ordinarie adminflöden
- användning ska utlösa omedelbar uppföljning

---

# Privileged Device Model

## Dedicated Admin Devices
Privilegerad administration ska endast få utföras från **dedikerade adminenheter**.

### Principles
- adminenheten ska inte vara en vanlig arbetsstation
- enheten ska användas för administration, inte vardaglig användning
- separata roller ska ha separata enhetsprofiler där motiverat
- enheten ska omfattas av högre skyddsnivå än vanliga klienter

### Expected Controls
- stark inloggning
- hög hårdningsnivå
- tydlig loggning
- begränsad programvaruyta
- kontrollerad nätverksåtkomst
- tydlig koppling mellan användare, enhet och administrativ funktion

---

## No Mixed-Use Principle
En och samma enhet bör inte användas för både:

- vardaglig kommunikation
- normal webbanvändning
- dokumenthantering
- privilegierad administration

Detta minskar risken att en komprometterad vardagsmiljö påverkar känsliga administrationsflöden.

---

# Authentication Model

## Standard Requirements for Privileged Access
Privilegerad åtkomst bör minst kräva:

- personlig administrativ identitet
- stark hemlighet eller passphrase
- FIDO2 / YubiKey eller likvärdig hårdvarubaserad faktor
- godkänd adminenhet
- tillåten nätverks- och zonkontext

---

## Contextual Requirements
För särskilt känsliga funktioner kan ytterligare krav gälla, exempelvis:

- särskild zon
- särskild adminväg
- dokumenterat change-id eller ärende
- ytterligare approval
- övervakad session

---

# Access Elevation Model

## Preferred Principle
Förhöjda rättigheter bör ges enligt principen:

- rätt person
- rätt roll
- rätt enhet
- rätt tidsfönster
- rätt ändamål

---

## Permanent vs Temporary Privilege
### Permanent Privilege
Ska hållas till ett minimum och endast finnas där det är tydligt motiverat.

### Temporary Privilege
Föredras där möjligt och bör:
- vara tidsbegränsad
- vara kopplad till uppgift eller change
- loggas tydligt
- kunna återkallas snabbt

---

## Scope Control
Privilegier bör så långt möjligt begränsas efter:

- system
- zon
- funktion
- tid
- roll
- ansvar

Målet är att undvika att ett konto eller en roll får mer makt än vad uppgiften kräver.

---

# Session Control & Oversight

## Logging Expectations
Privilegerad aktivitet bör kunna korreleras mot:

- användaridentitet
- adminidentitet
- enhet
- inloggningstid
- åtgärd eller uppgift
- change ticket / approval
- berört system

---

## Oversight Principles
För särskilt känsliga åtgärder bör modellen stödja:

- tydlig sessionstart och sessionslut
- extra loggning
- manuell uppsikt där motiverat
- eftergranskning av högriskaktiviteter

---

## Administrative Intent
Innan känsliga privilegierade åtgärder utförs bör det framgå:

- vad som ska göras
- varför det ska göras
- i vilken miljö
- under vilken change eller begäran
- av vem

Detta stärker både spårbarhet och ansvar.

---

# Global Admin / Highest Privilege Considerations

## Design Position
Bredast möjliga privilegier ska betraktas som **undantag**, inte normal arbetsmetod.

### Recommended Principles
- så få sådana identiteter som möjligt
- starkast möjliga skydd
- användning endast vid verkligt behov
- högsta nivå av loggning och uppföljning
- inte användas för rutinmässig administration om lägre nivå räcker

---

## Shared vs Personal Privileged Identity
En delad högprivilegierad identitet kan uppfattas som enkel att kontrollera om den bara används i övervakad miljö, men personbundna privilegierade identiteter ger normalt bättre:

- ansvar
- revisionsspår
- attributering
- least privilege

Därför bör huvudprincipen vara:
- personliga adminidentiteter i vardagen
- särskilda nödläges- eller break-glass-identiteter som undantag

---

# Break-Glass Model

## Purpose
Break-glass ska användas när:
- normal administrativ väg inte fungerar
- incident kräver snabb återställning
- ordinarie privilegierade identiteter inte räcker
- kritisk tillgång till system måste återtas

---

## Design Requirements
Break-glass ska:
- vara hårt skyddat
- vara dokumenterat
- vara separat från vardagsadministration
- granskas efter varje användning
- kunna spärras, återställas och recertifieras

---

## Governance Expectations
Varje användning av break-glass bör:
- motiveras
- loggas
- granskas
- rapporteras till relevant ansvarig funktion

---

# Administrative Zone Considerations

Privilegerad administration bör vara kopplad till definierade zoner och eller godkända accessvägar.

Exempel:
- vanlig användarzon ska inte ge direkt adminmöjlighet
- känsliga administrativa funktioner bör kräva högre klassad zon
- vissa funktioner bör bara vara möjliga från skyddad teknisk eller administrativ miljö

Detta stärker sambandet mellan:
- identitet
- enhet
- fysisk kontext
- tillåten handling

---

# Auditability Requirements

För att modellen ska vara stark i praktiken bör följande kunna granskas:

- vem som begärde privilegierad åtkomst
- vem som fick privilegierad åtkomst
- från vilken enhet
- från vilken zon eller adminväg
- med vilken autentiseringsnivå
- under vilken tidsperiod
- mot vilket system
- med vilket syfte eller changeunderlag
- vilka avvikelser som uppstod

---

# Recovery & Fallback Considerations

Privileged access-modellen måste hantera situationer som:

- förlorad YubiKey
- trasig adminenhet
- otillgänglig ordinarie adminväg
- credential compromise
- behov av snabb återställning under incident

Detta kräver tydliga playbooks och godkända undantagsrutiner.

---

# Recommended Policy Statements

## Example Policy 1
Privilegerad åtkomst ska ske med separat administrativ identitet och får inte utföras från standardanvändarenheter.

## Example Policy 2
Administrativa åtgärder i högsäker miljö ska endast tillåtas från godkända adminenheter och inom definierad fysisk och logisk kontext.

## Example Policy 3
Starkt autentiserad, personbunden och revisionsbar åtkomst ska vara huvudmodell för privilegierad administration.

## Example Policy 4
Bredast möjliga privilegier ska betraktas som undantag och användas endast när lägre privilegienivå inte är tillräcklig.

## Example Policy 5
Break-glass-åtkomst ska vara separat definierad, hårt skyddad och obligatoriskt eftergranskad efter varje användning.

---

# Common Risks If Poorly Designed

Om privileged access-modellen implementeras dåligt uppstår ofta:

- delade adminkonton utan tydligt ansvar
- för breda permanenta rättigheter
- admin från fel enheter
- svag återställningsförmåga
- låg spårbarhet
- överberoende av informella rutiner
- otydlig gräns mellan användar- och adminaktivitet

---

# Recommended Next Steps

## 1. Define Admin Role Catalog
Skapa tydlig rollkatalog för:
- user
- power user
- admin
- security admin
- emergency / break-glass

## 2. Map Privileges to Scope
Beskriv:
- vilka system som hör till vilken roll
- vilka roller som kräver vilken enhet
- vilka privilegier som får vara permanenta respektive tillfälliga

## 3. Formalize Admin Device Classes
Dokumentera:
- vilka adminenheter som finns
- vilka som får använda dem
- vilka skyddsnivåer som gäller
- hur de skiljer sig från vanliga klienter

## 4. Create Recovery Playbooks
Definiera processer för:
- förlorad token
- trasig adminenhet
- spärrad adminidentitet
- emergency access
- credential compromise

## 5. Establish Audit & Review Model
Bestäm:
- vad som ska loggas
- hur adminaktivitet granskas
- hur avvikelser hanteras
- hur privilegier recertifieras

---

# Final Note

Privileged access är ett av de områden där facilityns säkerhetsnivå i praktiken avgörs. En stark fysisk miljö kan snabbt försvagas om privilegierad åtkomst inte är personbunden, kontrollerad och revisionsbar.

Den centrala principen i denna modell är därför:

> **Privilegerad åtkomst ska vara separat, starkt skyddad, kontextbunden och fullt spårbar.**
