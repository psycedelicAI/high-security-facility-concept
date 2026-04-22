# One-Pager – High-Security Facility Concept

> Ett koncept för högsäker teknisk anläggning där fysisk säkerhet, zonlogik, credential custody, device control, privilegierad åtkomst och recovery samverkar som ett sammanhängande system.

---

## What It Is

**High-Security Facility Concept** är en konceptuell modell för hur en högsäker teknisk miljö kan designas för att ge starkare kontroll över:

- fysisk access
- rörelse mellan zoner
- badges och credentials
- devices och tillgångar
- privilegierad administration
- tekniska skyddszoner
- incidenter och recovery

I stället för att behandla dessa områden som separata säkerhetsproblem utgår konceptet från att de måste fungera tillsammans som en gemensam **trust model**.

---

## The Core Idea

Hög säkerhet uppstår inte bara genom att veta **vem** som har access, utan genom att förstå:

- vilken roll personen har
- vilken zon personen befinner sig i
- hur personen tog sig dit
- vilken credential som används
- vilken device som används
- om aktiviteten är normal eller avvikande
- hur undantag, incidenter och återställning hanteras

Kort sagt:

> **Identitet, rörelse, devices, credentials, privilegier och recovery måste hänga ihop för att skapa verklig hög säkerhet.**

---

## The Problem It Solves

Många säkerhetsmiljöer har starka punktkontroller, men svag koppling mellan:

- fysisk säkerhet och IT-säkerhet
- access och rörelsemönster
- credentials och custody
- adminpolicy och faktisk adminkontext
- drift, incidenthantering och recovery

Det skapar luckor där:
- credentials exponeras
- genvägar uppstår
- devices rör sig fel
- avvikelser missas
- högriskåtkomst sker i fel kontext
- recovery bygger på improvisation

---

## Key Differentiators

### Sequential Zone Access
Högre zoner kräver korrekt passage genom tidigare zoner, vilket förbättrar spårbarhet och avvikelsedetektering.

### Credential Custody
Badges och andra känsliga credentials hålls under aktiv kontroll, exempelvis genom att badges stannar i facilityn.

### Device Trust
Devices behandlas som säkerhetsbärare, inte bara arbetsverktyg.

### Privileged Access Separation
Adminåtkomst sker med separata identiteter, separata enheter och starkare kontrollnivå.

### Protected Technical Zones
Serverhallar och andra teknikzoner behandlas som särskilda miljöer med begränsad närvaro och tydlig change/recovery-logik.

### Recovery by Design
Recovery och fallback är inbyggda i modellen och inte beroende av informella nödlösningar.

---

## Intended Environments

Konceptet är främst relevant för:

- skyddade serverhallar
- säkerhetsklassade driftmiljöer
- tekniska säkerhetszoner
- miljöer med höga krav på OPSEC
- verksamheter där insiderhot och avvikande rörelsemönster är relevanta risker

Det är inte i första hand utformat för:
- vanliga kontorsmiljöer
- lågfriktionsmiljöer
- generell standard-enterprise IT

---

## Why It Matters

Konceptet skapar värde genom att:

- koppla ihop fysisk och logisk säkerhet
- minska informella säkerhetsglapp
- stärka kontrollen över credentials och assets
- höja spårbarhet i högklassade miljöer
- separera högriskfunktioner tydligare
- stödja mogen drift, recovery och incidenthantering

---

## Current Status

Konceptet är idag att betrakta som:

- en stark konceptmodell
- ett dokumenterat designunderlag
- en möjlig grund för vidare säkerhetsarkitektur, rådgivning eller paketering

### Assessment Reference
**88 / 100**

---

## Bottom Line

**High-Security Facility Concept** är ett försök att beskriva högsäker teknisk miljö som ett sammanhängande system där människor, credentials, devices, privilegier, zoner och drift inte hanteras separat — utan som delar av samma säkerhetsarkitektur.

> **Hög säkerhet blir starkare när tillit inte bara handlar om access, utan om sambandet mellan identitet, rörelse, enheter, kontroll och återställning.**
