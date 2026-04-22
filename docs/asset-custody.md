# Asset Custody Model – High-Security Facility Concept

> Konceptuell modell för kontroll, förvaring, rörelse och spårbarhet av badges, tokens, laptops och andra säkerhetskritiska tillgångar i en högsäker teknisk anläggning.

---

## Document Information

| Field | Value |
|---|---|
| Document | Asset Custody Model |
| Subject | High-Security Facility Concept |
| Type | Security Architecture / Asset Control Concept |
| Status | Draft |
| Scope | Badges, tokens, laptops, lockers, RFID tracking, chain of custody |
| Audience | Security architects, facility planners, IT security leads, physical security teams |

---

## Purpose

Detta dokument beskriver en konceptuell modell för **asset custody** i en högsäker miljö.

Målet är att säkerställa att känsliga tillgångar:

- förvaras på rätt plats
- används av rätt person
- inte lämnar tillåtet område utan kontroll
- kan spåras och granskas
- omfattas av tydlig chain of custody
- skyddas både mot förlust och mot missbruk

---

## Scope

Följande typer av tillgångar omfattas av modellen:

- access badges / passagekort
- YubiKeys / FIDO2-tokens
- smartcards / säkerhetskort
- admin laptops
- user laptops
- power user laptops
- konsultenheter
- externa krypterade lagringsmedier
- lockers och tillhörande förvaringsobjekt
- övriga säkerhetskritiska identifierings- eller åtkomstobjekt

---

# Core Principles

## 1. Assets Are Security Objects
Tillgångar som badges, tokens och laptops ska inte behandlas som vanliga arbetsverktyg, utan som **säkerhetsobjekt**.

Det innebär att:
- de omfattas av policy
- deras rörelse ska kontrolleras
- deras förvaring ska vara definierad
- deras användning ska kunna knytas till person, plats och syfte

---

## 2. Custody Must Be Explicit
För varje säkerhetsrelevant tillgång ska det vara tydligt:

- vem som har den
- var den befinner sig
- när den hämtades ut
- när den lämnades tillbaka
- om den har lämnat tillåtet område
- om den avvikit från policy

---

## 3. Sensitive Assets Should Not Drift Into Private Life
Säkerhetskritiska tillgångar bör inte följa med in i privatlivet om det inte finns ett uttryckligt och kontrollerat behov.

Det gäller särskilt:
- badges
- högt skyddade tokens
- adminenheter
- särskilda säkerhetskort

---

## 4. Movement Is a Security Event
När en tillgång flyttas mellan zoner, lämnar facilityn eller separeras från avsedd kontext ska detta betraktas som en säkerhetshändelse eller minst en policyrelevant händelse.

---

## 5. Asset Type Determines Control Level
Olika tillgångar ska ha olika kontrollnivå beroende på:

- känslighet
- privilegienivå
- koppling till identitet
- koppling till systemsäkerhet
- exfiltrationsrisk
- återställningssvårighet

---

# Asset Categories

## 1. Access Credentials
Exempel:
- badge
- passagekort
- RFID-baserad identifiering
- smartcards för fysisk tillgång

### Security Relevance
Dessa tillgångar styr fysisk rörelse och ska därför omfattas av stark custody-kontroll.

---

## 2. Authentication Tokens
Exempel:
- YubiKey
- FIDO2-token
- smartcard för systeminloggning
- andra hårdvarubundna autentiseringsobjekt

### Security Relevance
Dessa tillgångar kan ge logisk åtkomst till känsliga system och ska därför skyddas minst lika starkt som fysiska accessobjekt.

---

## 3. Managed Endpoints
Exempel:
- admin laptops
- power user laptops
- user laptops
- konsultenheter under facilitykontroll

### Security Relevance
Dessa tillgångar bär både data, identitet och trust-nivå och ska därför kontrolleras utifrån både säkerhet och drift.

---

## 4. Portable Storage
Exempel:
- externa krypterade SSD-enheter
- särskilda flyttbara media

### Security Relevance
Flyttbara media utgör hög exfiltrationsrisk och ska omfattas av striktare policy än vanliga klientenheter.

---

# Badge Custody Model

## Principle
Badges ska som huvudregel **stanna i facilityn** och inte följa med användaren hem eller ut i privat miljö.

---

## Purpose
Denna modell stärker:

- OPSEC
- skydd mot social engineering
- minskad extern exponering
- snabb avaktivering vid offboarding
- mindre risk för glömda eller tappade badges
- bättre kontroll över credential lifecycle

---

## Expected Operational Flow
1. användaren anländer till facilityn
2. badge hämtas ut eller aktiveras enligt fastställd process
3. badge används för tillåten rörelse under arbetspass
4. badge återlämnas till reception eller definierad säker förvaring vid arbetspassets slut

---

## Security Benefits
- användaren kan inte glömma badge hemma
- badge exponeras inte i bil, bostad eller offentlig miljö
- avslutad anställning eller ändrad behörighet blir enklare att hantera
- credentialn befinner sig redan i kontrollerad miljö för spärr eller återtag

---

## Recommended Controls
- utlämning och återlämning loggas
- badge ska vara personligt kopplad eller spårbart tilldelad
- utebliven återlämning ska generera uppföljning
- tillfälliga badges ska ha särskild policy
- besöksbadges och konsultbadges ska vara tydligt separerade från ordinarie badges

---

# Token Custody Model

## Principle
Autentiseringstokens ska hanteras utifrån deras risknivå.

### Example Distinction
- standard user tokens kan i vissa miljöer vara personburna
- högprivilegierade tokens bör omfattas av starkare custody
- break-glass eller särskilt känsliga tokens bör hållas under strikt kontrollerad förvaring

---

## Security Considerations
Token custody bör ta hänsyn till:
- vilken åtkomst token möjliggör
- om token används för privilegierad administration
- om token används för BIOS, lokal admin eller globalt känsliga funktioner
- hur återställning ska ske om token försvinner

---

## Recommended Controls
- personbunden tilldelning där möjligt
- separata regler för standardtoken och högkänslig token
- tydlig spärrprocess
- återutgivning under kontroll
- stark koppling mellan token, identitet och roll

---

# Laptop Custody Model

## Principle
Laptops ska behandlas som både arbetsverktyg och säkerhetsobjekt.

Det innebär att:
- varje laptop ska ha definierad rollklass
- tillåten rörelse ska vara tydlig
- förflyttning utanför policy ska kunna upptäckas
- känsligare laptops ska omfattas av högre kontrollnivå

---

## Device Classes
Exempel på laptopklasser:

- admin laptop
- power user laptop
- standard laptop
- consultant laptop

Varje klass bör ha:
- egen policy
- egen tillitsnivå
- egen tillåten zonmodell
- egen åtkomstprofil

---

## Facility Movement Control
Laptops ska endast få röra sig inom godkända zoner och under definierade villkor.

### Example Principles
- vissa laptops får aldrig lämna facilityn
- vissa laptops får inte tas in i särskilda zoner
- vissa laptops får endast användas i definierade arbetsområden
- vissa laptops kan kräva särskild övervakning eller eskort vid förflyttning

---

## RFID-Based Tracking
RFID ska användas som stöd för:

- realtidspositionering
- zonkontroll
- asset visibility
- policytrigger
- larm om enhet lämnar tillåtet område

Det ska **inte** ses som enda säkerhetsmekanism, men som ett starkt komplement till annan kontroll.

---

## Recommended Responses to Device Deviation
När en laptop lämnar tillåtet område eller avviker från policy bör systemet kunna:

1. logga händelsen
2. generera larm
3. låsa enheten
4. begränsa fortsatt systemåtkomst
5. kräva manuell säkerhetsverifiering

Remote wipe bör normalt vara en senare åtgärd efter bekräftad incident, inte första respons.

---

# Pairing and Context Validation

Vissa tillgångar kan med fördel kopplas ihop kontextuellt, exempelvis:

- användare + badge
- användare + laptop
- adminidentitet + adminenhet
- zon + tillåten enhetsklass

Syftet är inte att skapa skör överautomation, utan att höja möjligheten att upptäcka:

- otillåten separation
- felaktig enhetsanvändning
- policybrott
- avvikande rörelsemönster

---

# Lockers and Controlled Storage

## Purpose
Lockers fungerar som kontrollerad övergång mellan privat och skyddad miljö.

De kan användas för:
- förvaring av privata mobiltelefoner
- förvaring av personliga föremål
- förvaring av säkerhetsobjekt mellan arbetspass
- utlämning och återtag av godkända tillgångar

---

## Security Value
Lockers stärker modellen genom att:
- separera privatliv från skyddad miljö
- minska risken att förbjudna objekt tas in
- skapa tydlig chain of custody för vissa tillgångar
- stödja kontroll av vad som förs in och ut

---

## Recommended Controls
- tilldelning ska vara spårbar
- tillgång till locker ska vara kontrollerad
- vissa lockers kan omfattas av särskild säkerhetspolicy
- säkerhetsteam ska kunna låsa eller säkra lockers vid incident eller policybrott

---

# Portable Media Control

## Principle
Flyttbara lagringsmedier ska behandlas som hög risk om de används i facilityn.

### Security Concerns
- dataexfiltration
- okontrollerad import av data
- förlust eller stöld
- svår revisionsbarhet

---

## Recommended Controls
- endast godkända krypterade media
- tydlig registrering
- begränsad användning till definierade roller och situationer
- loggning av utlämning och återlämning
- policy för destruktion, förvaring och återkallelse

---

# Offboarding & Revocation

En stark custody-modell ska underlätta snabb och säker offboarding.

## Expected Benefits
- badge finns redan inom facilityn
- tokens kan återtas eller spärras direkt
- laptops kan låsas, återtas eller isoleras
- tillgångar behöver inte eftersökas i privat miljö i samma omfattning

---

## Minimum Requirements
- omedelbar spärr av logiska och fysiska credentials
- tydlig checklista för återtag av tillgångar
- verifiering att privilegierade objekt återlämnats
- avvikelseflöde om något saknas

---

# Logging & Audit Requirements

Följande bör loggas där det är relevant:

- utlämning av badge
- återlämning av badge
- tilldelning av token
- spärr av token
- tilldelning av laptop
- policyavvikelse för laptoprörelse
- larm vid otillåten förflyttning
- utlämning och återtag av flyttbara media
- låsning, isolering eller återkallelse av enhet
- avvikelse vid offboarding

Loggning bör vara:
- tidsstämplad
- personkopplad där möjligt
- kopplad till zon eller plats
- tillgänglig för revision

---

# Recommended Policy Statements

## Example Policy 1
Säkerhetskritiska tillgångar ska omfattas av tydlig chain of custody och får endast användas, förvaras eller förflyttas enligt fastställd policy.

## Example Policy 2
Access badges ska som huvudregel stanna i facilityn och återlämnas till definierad kontrollpunkt vid arbetspassets slut.

## Example Policy 3
Privilegerade autentiseringstokens och adminenheter ska omfattas av högre kontrollnivå än standardanvändarens tillgångar.

## Example Policy 4
Otillåten förflyttning av laptop eller annan säkerhetskritisk utrustning ska generera säkerhetshändelse, loggning och policyenlig respons.

## Example Policy 5
Flyttbara media ska endast tillåtas när de är godkända, krypterade, registrerade och motiverade av definierad arbetsuppgift.

---

# Common Risks If Poorly Managed

Om asset custody hanteras svagt uppstår ofta:

- badges som tappas eller exponeras externt
- glömda credentials i privat miljö
- svår offboarding
- oklar ansvarskedja
- laptops som lämnar facilityn utan kontroll
- tokens utan tydlig ägare
- dålig spårbarhet vid incident
- ökad exfiltrationsrisk

---

# Recommended Next Steps

## 1. Create Asset Classification
Dela in tillgångar i tydliga klasser, exempelvis:
- standard credential
- privileged credential
- managed endpoint
- restricted endpoint
- removable media

## 2. Build Custody Workflows
Definiera processer för:
- utlämning
- återlämning
- avvikelse
- spärr
- återtag
- förlust
- offboarding

## 3. Map Controls to Asset Type
Bestäm vilka kontroller som gäller för:
- badges
- tokens
- adminlaptops
- userlaptops
- flyttbara media

## 4. Define Response Levels
Skapa tydliga nivåer för:
- avvikande rörelse
- utebliven återlämning
- misstänkt credential misuse
- otillåten device separation

## 5. Add Audit & Review
Bestäm:
- vem som granskar custody-händelser
- hur ofta tillgångar recertifieras
- hur avvikelser ska följas upp
- hur inventering ska göras

---

# Final Note

En stark asset custody-modell minskar inte bara risken för förlust, utan höjer även säkerhetsnivån genom att göra tillgångars rörelse, användning och ägarskap synliga och kontrollerbara.

Den centrala principen i denna modell är:

> **Säkerhetskritiska tillgångar ska vara under aktiv kontroll, inte bara under antagen kontroll.**
