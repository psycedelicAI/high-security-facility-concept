# Policy Baseline – High-Security Facility Concept

> Grundläggande policyprinciper för fysisk säkerhet, zonstyrning, credentials, privilegierad åtkomst, enhetskontroll, tekniska zoner, incidenthantering, recovery och governance i en högsäker teknisk anläggning.

---

## Document Information

| Field | Value |
|---|---|
| Document | Policy Baseline |
| Subject | High-Security Facility Concept |
| Type | Security Policy Baseline / Concept Governance Foundation |
| Status | Draft |
| Scope | Baseline policy principles for physical, logical and operational security |
| Audience | Security architects, governance owners, facility planners, IT security leads, reviewers |

---

## Purpose

Detta dokument definierar en **policy baseline** för High-Security Facility Concept.

Syftet är att formulera de grundläggande policykrav som ska gälla för hela modellen, så att konceptet inte bara består av designidéer och arkitekturprinciper, utan också av tydliga styrande utgångspunkter.

Denna baseline anger vad som ska betraktas som:

- standardförväntan
- miniminivå
- obligatorisk säkerhetsriktning
- grund för vidare detaljpolicy

---

## Scope

Policy-baselinen omfattar följande områden:

- fysisk säkerhet
- zonindelning och rörelselogik
- identiteter och credentials
- badges och tokens
- privilegierad åtkomst
- klienter och devices
- asset custody
- skyddade tekniska zoner
- maintenance och change
- incidenthantering
- recovery
- governance, review och undantag

---

# Baseline Security Principles

## 1. Security Shall Be Layered
Säkerheten ska byggas i flera lager och inte vila på en enskild kontroll.

Det innebär att fysisk access, identitet, zonlogik, devices, privilegier och recovery ska samverka i en sammanhängande modell.

---

## 2. Trust Shall Be Contextual
Tillit ska inte enbart baseras på att en credential existerar eller att ett konto kan autentiseras.

Tillit ska även påverkas av:
- zon
- rörelsemönster
- device context
- roll
- syfte
- tidsfönster
- säkerhetsstatus

---

## 3. High-Risk Actions Shall Require Higher Control
Ju högre risk en aktivitet innebär, desto högre kontrollnivå ska krävas.

Det gäller särskilt:
- privilegierad administration
- högklassad fysisk access
- tekniskt arbete i skyddade zoner
- undantag från normal policy
- recovery och emergency access

---

## 4. Security-Relevant Assets Shall Be Under Active Control
Badges, tokens, adminenheter, känsliga laptops och andra säkerhetsrelevanta tillgångar ska hållas under aktiv kontroll, inte bara antagen kontroll.

---

## 5. Exceptions Shall Be Temporary and Controlled
Undantag från ordinarie säkerhetsmodell ska vara:
- motiverade
- godkända
- tidsbegränsade
- loggade
- eftergranskade

---

## 6. Recovery Shall Preserve Security Intent
Recovery och fallback får inte innebära att ordinarie säkerhetskrav överges permanent eller informellt.

---

## 7. Governance Shall Be Explicit
Alla centrala säkerhetskontroller ska ha tydligt ägarskap, godkännandeflöde och granskningsbarhet.

---

# Physical Security Baseline

## Policy Statement
Facilityn ska använda flera lager av fysisk säkerhet för att styra, begränsa och övervaka fysisk tillgång till anläggningens olika zoner.

## Baseline Requirements
- fysisk tillgång ska vara behovsstyrd
- reception eller motsvarande kontrollpunkt ska finnas
- övergång mellan zoner ska vara kontrollerad
- högklassade zoner ska ha striktare fysisk accessmodell än öppna eller interna standardzoner
- fysisk säkerhet ska stödja både prevention, detektion och containment

---

# Zone and Movement Baseline

## Policy Statement
Fysisk rörelse inom facilityn ska betraktas som en säkerhetsparameter och omfattas av definierad policy.

## Baseline Requirements
- zoner ska klassificeras efter känslighet
- varje zon ska ha definierat syfte och tillåten rollbaserad access
- övergång mellan högre klassade zoner ska kunna loggas och granskas
- sekventiell zonvalidering ska användas där skyddsvärdet motiverar det
- avvikande rörelsemönster ska kunna flaggas och hanteras

---

# Identity and Credential Baseline

## Policy Statement
Fysisk och logisk identitet ska hanteras som säkerhetskritiska funktioner med tydlig koppling till roll, tillgång och ansvar.

## Baseline Requirements
- credentials ska vara personbundna eller spårbart tilldelade
- credential lifecycle ska vara definierad
- förlust, spärr och återutgivning ska hanteras genom kontrollerad process
- credentials med högre risk ska ha högre skyddsnivå
- identitetskontroller ska kunna stödja både normal access och recovery

---

# Badge and Token Baseline

## Policy Statement
Badges, autentiseringstokens och liknande säkerhetsobjekt ska hanteras under tydlig chain of custody.

## Baseline Requirements
- badges ska som huvudregel inte lämna facilityn utan uttryckligt behov
- återlämning och utebliven återlämning ska kunna följas upp
- högprivilegierade tokens ska omfattas av starkare kontroll än standardobjekt
- credential exposure utanför kontrollerad miljö ska ses som säkerhetsrelevant händelse
- tillfälliga credentials ska vara tidsbegränsade och särskilt markerade

---

# Privileged Access Baseline

## Policy Statement
Privilegerad åtkomst ska vara separerad från vanlig användning, starkt autentiserad, spårbar och begränsad till definierad kontext.

## Baseline Requirements
- adminidentiteter ska vara separata från standardanvändaridentiteter
- privilegierad åtkomst ska endast tillåtas från godkända adminenheter eller definierad säker kontext
- högprivilegierade funktioner ska skyddas starkare än standardfunktioner
- bredast möjliga privilegier ska betraktas som undantag
- break-glass ska vara särskilt definierat, skyddat och eftergranskat

---

# Device and Endpoint Baseline

## Policy Statement
Devices ska behandlas som säkerhetsbärare och omfattas av policy för roll, rörelse, användning och skyddsnivå.

## Baseline Requirements
- olika deviceklasser ska kunna ha olika policy
- högre tillitsnivå ska kräva högre kontroll
- känsliga enheter ska inte användas i odefinierad eller blandad kontext
- avvikande device movement ska kunna loggas och hanteras
- devices med känslig funktion ska kunna isoleras eller återkallas enligt policy

---

# Asset Custody Baseline

## Policy Statement
Säkerhetskritiska tillgångar ska ha tydlig ägare, definierad förvaring och spårbar användning.

## Baseline Requirements
- tillgångar ska vara klassificerade efter känslighet
- custody-flöden ska finnas för utlämning, återlämning och avvikelse
- RFID eller liknande stödmekanismer kan användas för synlighet och policytrigger
- förlust eller ologisk förflyttning av känsliga tillgångar ska behandlas som säkerhetsrelevant händelse
- flyttbara media ska omfattas av särskilt restriktiv policy

---

# Technical Zone Baseline

## Policy Statement
Skyddade tekniska zoner ska behandlas som särskilda miljöer med begränsad mänsklig närvaro och högre krav på syftesbunden åtkomst.

## Baseline Requirements
- teknikzoner ska inte betraktas som vanliga arbetsytor
- mänsklig vistelse ska vara motiverad, tidsbunden och spårbar
- service, change, incident och recovery ska hanteras enligt olika processlägen
- större tekniskt arbete ska kräva tydlig change- eller recoverykontext
- återgång till normal drift ska vara verifierad och dokumenterad

---

# Maintenance and Change Baseline

## Policy Statement
Tekniskt arbete i skyddade zoner ska ske enligt definierad process och får inte bygga på informell eller otydlig åtkomst.

## Baseline Requirements
- arbete ska vara kopplat till arbetsorder, incident eller change
- deltagare ska vara identifierade och godkända
- tillträde ska vara tidsbundet och syftesbundet
- change ska ha tydligt ansvar och godkännande
- rollback eller återställningsväg ska finnas där relevant

---

# Incident Response Baseline

## Policy Statement
Alla säkerhetsrelevanta avvikelser ska kunna klassificeras, begränsas, dokumenteras och följas upp genom definierad incidentprocess.

## Baseline Requirements
- incidentkategorier ska vara definierade
- fysisk och logisk kontext ska kunna korreleras
- containment ska kunna prioriteras framför bekvämlighet
- incidenter ska ha tydlig closure och eftergranskning
- lärdomar ska kunna återföras till policy, styrning och design

---

# Recovery Baseline

## Policy Statement
Recovery ska vara definierad, kontrollerad och säkerhetsbevarande.

## Baseline Requirements
- fallback-processer ska finnas för kritiska beroenden
- credential recovery ska ske under kontroll
- recovery ska inte skapa permanenta bypasser
- återgång till normal drift ska vara explicit, verifierad och loggad
- recoveryhändelser ska kunna granskas i efterhand

---

# Governance Baseline

## Policy Statement
Säkerhetsmodellen ska ha tydligt ägarskap, tydliga godkännandeflöden och regelbunden uppföljning.

## Baseline Requirements
- alla centrala kontrollområden ska ha utsedd owner
- godkännanden ska vara rollbaserade och dokumenterade
- access och privilegier ska recertifieras regelbundet
- undantag ska ha egen styrmodell
- governance ska täcka både fysisk, logisk och operativ säkerhet

---

# Review and Recertification Baseline

## Policy Statement
Tilldelad åtkomst, tillgångar och privilegier ska granskas regelbundet för att säkerställa fortsatt relevans.

## Baseline Requirements
- fysisk access ska recertifieras
- privilegierad åtkomst ska recertifieras med högre prioritet
- temporära undantag ska följas upp innan eller vid utgång
- tillgångar och credentials ska kunna inventeras och verifieras
- reviewprocesser ska dokumenteras och vara åtgärdsbara

---

# Exception Baseline

## Policy Statement
Undantag från säkerhetsmodellen ska vara synliga, tidsbundna och styrda.

## Baseline Requirements
- varje undantag ska ha motivering
- varje undantag ska ha owner
- varje undantag ska ha godkännande
- varje undantag ska ha utgångstid eller aktiv omprövning
- undantag ska eftergranskas när risknivån motiverar det

---

# Compliance and Enforcement Baseline

## Policy Statement
Policyer inom denna baseline ska vara styrande för design, drift och uppföljning i facilityn.

## Baseline Requirements
- policybrott ska kunna upptäckas och hanteras
- återkommande avvikelser ska kunna leda till styrningsåtgärd
- revision och kontroll ska kunna verifiera efterlevnad
- informella arbetssätt får inte ersätta definierad policy i känsliga områden

---

# Minimum Documentation Expectations

För att policy-baselinen ska vara operativt användbar bör följande kompletterande dokument finnas eller tas fram:

- zonmodell
- privileged access-modell
- asset custody-modell
- maintenance-modell
- recovery-modell
- incident response-modell
- governance-modell
- roadmap
- eventuella playbooks och undantagsrutiner

---

# Recommended Policy Statements

## Example Policy 1
All fysisk, logisk och privilegierad åtkomst inom facilityn ska vara behovsstyrd, spårbar och knuten till definierad roll och kontext.

## Example Policy 2
Högklassade zoner, credentials och tillgångar ska omfattas av starkare kontrollnivå än standardmiljöer och standardroller.

## Example Policy 3
Undantag, recovery och emergency access ska vara uttryckligt definierade och får inte ersätta ordinarie styrmodell.

## Example Policy 4
Säkerhetskritiska tillgångar ska hållas under aktiv custody och får inte lämna kontrollerad miljö utan tydligt godkänt syfte.

## Example Policy 5
Governance, review och recertifiering ska vara en permanent del av säkerhetsmodellen och inte en separat efterhandsaktivitet.

---

# Common Policy Failures

Om policy-baselinen saknas eller är svag uppstår ofta:

- god design utan styrning
- otydliga minimikrav
- osäker tolkning mellan team
- tillfälliga undantag som blir standard
- låg konsekvens mellan fysisk och logisk säkerhet
- svårt att granska efterlevnad
- hög personberoende drift

---

# Recommended Next Steps

## 1. Create Domain-Specific Policy Documents
Bryt ut detaljerade policyer för:
- zoner
- privileged access
- credentials
- assets
- maintenance
- recovery
- incident response

## 2. Define Mandatory vs Recommended Controls
Markera vilka delar som är:
- obligatoriska
- rekommenderade
- situationsberoende

## 3. Align Baseline With Governance
Säkerställ att varje policyområde har:
- owner
- approval chain
- review cycle
- exception path

## 4. Add Review Triggers
Definiera när policy ska omprövas, exempelvis vid:
- incident
- större change
- ny zonklassning
- ny credentialtyp
- förändrad riskbild

## 5. Link Baseline to Implementation Planning
Använd denna baseline som grund för:
- kravarbete
- arkitekturdetaljering
- operativ modell
- kontrollkartläggning
- framtida design review

---

# Final Note

Policy-baselinen är till för att säkerställa att konceptets kärnidéer inte bara blir inspirerande, utan även styrande.

Den centrala principen i detta dokument är:

> **Hög säkerhet kräver inte bara stark design, utan också tydliga grundregler som gör modellen konsekvent, granskningsbar och hållbar över tid.**
