# BetterHuman_Brains
## Live Demo Præsentation

---

# Oversigt

**Produkt:** BetterHuman_Brains – AI-hukommelsessystem  
**Målgruppe:** Beslutningstagere og brugere ved salgsmøder  
**Varighed:** 15-20 minutter  
**Format:** Live demo med 6 hovedscenarier

---

# Forberedelse før demoen

## Checklist
- [ ] Laptop med internetforbindelse
- [ ] API-nøgle konfigureret
- [ ] Demo-miljø kører
- [ ] Skærmdeling testet
- [ ] Backup slides klar (PDF-format)

## Demo-konto
- API Endpoint: `https://api.betterhumanbrains.ai/v1`
- Demo API-nøgle: `[DEMO-KEY-VISES-FOR-KUNDE]`

---

# SCENARIE 1: Første samtale – "Hvem er jeg?"

**Formål:** Vis systemets evne til at lagre og genkende basale fakta

## Screendump 1.1: Tom agent-samtale

```
┌─────────────────────────────────────────────────────────┐
│  BetterHuman_Brains – Agent Demo                       │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │ Bruger: Hej, jeg hedder Maria Jensen og jeg    │   │
│  │         arbejder som salgschef hos NovoTech A/S │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │ Agent: Hej Maria! Velkommen. Jeg er din nye    │   │
│  │        AI-assistent. Hvordan kan jeg hjælpe     │   │
│  │        dig i dag?                               │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  [Send besked...]                         [Retain ON]  │
└─────────────────────────────────────────────────────────┘
```

**Beskrivelse:** Tom chat-grænseflade med velkomstboks. I bunden ses "Retain ON" indikator som viser at hukommelsessystemet er aktivt.

## Screendump 1.2: Agenten gemmer informationen

```
┌─────────────────────────────────────────────────────────┐
│  BetterHuman_Brains – Agent Demo                       │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │ 💾 Hukommelse opdateret:                        │   │
│  │    • Navn: Maria Jensen                         │   │
│  │    • Titel: Salgschef                          │   │
│  │    • Virksomhed: NovoTech A/S                   │   │
│  │    • Lagret i: Langtidshukommelse ✓             │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │ Agent: Forstået, Maria. Jeg husker det frem-    │   │
│  │        over. Hvad kan jeg hjælpe dig med?       │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Beskrivelse:** Popup-boks viser hvad systemet har registreret og gemt. Grøn bekræftelse på succesfuld lagring.

## Demo-script:

```
SALGSPERSON: "Lad os starte med noget simpelt. Jeg fortæller agenten 
hvem jeg er..."

[SKRIV]: "Hej, jeg hedder Maria Jensen og jeg arbejder som 
salgchef hos NovoTech A/S"

SALGSPERSON: "Som I kan se, svarer agenten høfligt. Men vigtigere 
er det, hvad I IKKE ser endnu. Lad mig vise jer hukommelses-panelet..."

[KLIK PÅ hukommelsesikon]

SALGSPERSON: "Systemet har automatisk udtrukket og gemt:
- Navn: Maria Jensen
- Titel: Salgschef  
- Virksomhed: NovoTech A/S

Dette sker uden at jeg har bedt om det. Systemet forstår konteksten 
af sig selv."
```

---

# SCENARIE 2: Anden samtale – "Kender du mig?"

**Formål:** Vis systemets evne til at huske på tværs af samtaler

## Screendump 2.1: Ny samtale, samme agent

```
┌─────────────────────────────────────────────────────────┐
│  BetterHuman_Brains – Agent Demo                    🔄 │
│  ┌─────────────────────────────────────────────────┐   │
│  │ 💬 Ny samtale startet                           │   │
│  │    Sidste samtale: for 2 timer siden            │   │
│  └─────────────────────────────────────────────────┘   │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │ Bruger: Hej, kan du huske hvad jeg hedder?      │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │ Agent: Hej igen, Maria Jensen. Du er salgschef   │   │
│  │        hos NovoTech A/S. Hvad kan jeg hjælpe    │   │
│  │        dig med i dag?                           │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  ⚡ Recall: 3 fakta fundet | 0.2ms responstid          │
└─────────────────────────────────────────────────────────┘
```

**Beskrivelse:** Chat-grænseflade der viser en ny samtale, men agenten husker allerede brugeren. I bunden vises "Recall" statistik.

## Demo-script:

```
SALGSPERSON: "Nu slutter jeg samtalen og starter en HELT NY samtale..."

[AFSLUT samtale, START ny samtale]

SALGSPERSON: "Dette er en ny samtale. Agenten har ingen kontekst fra 
den forrige. Lad mig spørge..."

[SKRIV]: "Hej, kan du huske hvad jeg hedder?"

SALGSPERSON: "AGENTER UDEN HUKOMMELSE ville svare: 'Jeg kender dig 
ikke, kan du fortælle mig mere om dig selv?'

Lad mig vise jer hvad BetterHuman_Brains gør..."

[VENT på svar]

SALGSPERSON: "Agenten husker:
- Dit navn: Maria Jensen
- Din rolle: Salgschef
- Din virksomhed: NovoTech A/S

Dette er ikke muligt med traditionelle AI-løsninger."
```

---

# SCENARIE 3: Forretningskontekst – "Hvad ved du om mit firma?"

**Formål:** Vis dybde i hukommelsen og forretningsforståelse

## Screendump 3.1: Firma-hukommelse

```
┌─────────────────────────────────────────────────────────┐
│  Hukommelses-panel                    🔍 Søg: "NovoTech" │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │ VIRKSOMHED: NovoTech A/S                        │   │
│  ├─────────────────────────────────────────────────┤   │
│  │  📅 Grundlagt: 2015                             │   │
│  │  👥 Ansatte: 45                                │   │
│  │  📍 Lokation: Aarhus, Danmark                   │   │
│  │  💼 Branche: SaaS / B2B teknologi              │   │
│  │  🎯 Fokus: salgsoptimering                     │   │
│  ├─────────────────────────────────────────────────┤   │
│  │  📝 SAMTALER: 12                                │   │
│  │  🔗 RELATERET: Maria Jensen (salgschef)         │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  [Detaljer]  [Historik]  [Indsigt]                     │
└─────────────────────────────────────────────────────────┘
```

**Beskrivelse:** Detaljeret hukommelsesvisning med firmaoplysninger, relationsdata og samtalehistorik.

## Screendump 3.2: Samtale om forretning

```
┌─────────────────────────────────────────────────────────┐
│  BetterHuman_Brains – Agent Demo                       │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │ Bruger: Vi overvejer at implementere AI i vores │   │
│  │         salgsafdeling. Hvad kan du foreslå?     │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │ Agent: Med jeres fokus på salgsoptimering hos   │   │
│  │        NovoTech, vil jeg anbefale at starte med │   │
│  │        kundesupport. Baseret på 45 medarbejdere │   │
│  │        kan I potentielt spare 12 timer ugentlig │   │
│  │        på gentagne henvendelser. Vil du høre   │   │
│  │        mere om vores ROI-beregning?             │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  🧠 Reflect: Mønster fundet • salg + AI                │
└─────────────────────────────────────────────────────────┘
```

**Beskrivelse:** Agenten trækker på både brugerens kontekst (salgschef) og virksomhedens kontekst (45 ansatte, salgsoptimering).

## Demo-script:

```
SALGSPERSON: "Nu går vi dybere. Lad mig fortælle systemet mere 
om Marias situation..."

[SKRIV]: "Jeg arbejder som salgschef hos NovoTech i Aarhus. 
Vi er 45 medarbejdere og fokuserer på salgsoptimering."

SALGSPERSON: "Systemet har gemt:
- Virksomhedsnavn og lokation
- Antal medarbejdere
- Forretningsfokus

Lad mig stille et spørgsmål..."

[SKRIV]: "Hvad kan du foreslå til vores salgsafdeling?"

SALGSPERSON: "Igen – UDEN hukommelse ville agenten svare generisk.
MED BetterHuman_Brains giver den personligt, relevant rådgivning 
baseret på den faktiske situation hos NovoTech.

Bemærk også 'Reflect' i bunden – systemet har identificeret et 
mønster: salg + AI-optimering = anbefaling om kundesupport first."
```

---

# SCENARIE 4: Historisk kontekst – "Hvad talte vi om sidst?"

**Formål:** Vis evnen til at hente specifik historik

## Screendump 4.1: Samtalehistorik

```
┌─────────────────────────────────────────────────────────┐
│  Hukommelses-panel                    📅 Historik        │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  SAMTALE #12 – I dag kl. 14:32                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │ Emne: AI-implementering i salgsafdeling        │   │
│  │ Nøglepunkter:                                   │   │
│  │ • Interesseret i kundesupport først            │   │
│  │ • Budget: ikke diskuteret                      │   │
│  │ • Beslutningstager: Maria + CTO (nævnt)        │   │
│  │ • Næste skridt: sende case-studies             │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  SAMTALE #11 – I går kl. 10:15                        │
│  ┌─────────────────────────────────────────────────┐   │
│  │ Emne: Introduktion og behovsafdækning          │   │
│  │ Nøglepunkter:                                   │   │
│  │ • 45 medarbejdere                               │   │
│  │ • NovoTech A/S, Aarhus                         │   │
│  │ • Fokus på salg                                │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Beskrivelse:** Tidslinje-visning af alle tidligere samtaler med opsummerede nøglepunkter.

## Screendump 4.2: "Hvad talte vi om sidst?"

```
┌─────────────────────────────────────────────────────────┐
│  BetterHuman_Brains – Agent Demo                       │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │ Bruger: Hvad talte vi om sidst?                │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │ Agent: Sidst talte vi om at implementere AI i   │   │
│  │        salgsafdelingen hos NovoTech. Du var     │   │
│  │        interesseret i at starte med kunde-      │   │
│  │        support. Vi aftalte at jeg skulle sende │   │
│  │        case-studies til dig. Vil du have mig   │   │
│  │        til at sende dem nu?                     │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  📚 Recall: "sidst" → 1 samtale fundet | 98% relevans  │
└─────────────────────────────────────────────────────────┘
```

**Beskrivelse:** Agenten giver præcis, sammenfattet information fra den seneste samtale.

## Demo-script:

```
SALGSPERSON: "Lad mig springe tilbage til tidligere samtaler..."

[VIS hukommelses-panel med samtalehistorik]

SALGSPERSON: "Her kan I se ALLE samtaler Maria har haft med systemet. 
Hver samtale er opsummeret med nøglepunkter. Lad mig spørge..."

[SKRIV]: "Hvad talte vi om sidst?"

SALGSPERSON: "Perfekt! Agenten kan:
1. Forstå hvad 'sidst' betyder
2. Finde den relevante samtale
3. Opsummere nøglepunkterne
4. Tilbyde opfølgning ('Vil du have mig til at sende dem nu?')

Ingen manual indtastning. Ingen tagging. Ingen strukturerede 
skemaer. Systemet forstår naturligt sprog."
```

---

# SCENARIE 5: Mødeforberedelse – "Forbered mig til mødet"

**Formål:** Vis praktisk forretningsværdi

## Screendump 5.1: Mødeforberedelse-anmodning

```
┌─────────────────────────────────────────────────────────┐
│  BetterHuman_Brains – Agent Demo                       │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │ Bruger: Forbered mig til mødet med NovoTech     │   │
│  │        i morgen kl. 10.                        │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  ┌─────────────────────────────────────────────────┐   │
│  │ Agent: Her er din mødeforberedelse til NovoTech│   │
│  │        (Maria Jensen, Salgschef):              │   │
│  │                                                 │   │
│  │  KONTAKT:                                      │   │
│  │  • Maria Jensen, Salgschef                     │   │
│  │  • Omtalte også CTO som beslutning-            │   │
│  │    tager                                       │   │
│  │                                                 │   │
│  │  BEHOV:                                        │   │
│  │  • Ønsker AI til salgsafdeling                 │   │
│  │  • Vil starte med kundesupport                 │   │
│  │                                                 │   │
│  │  FREMTIDIGE SKRIDT:                           │   │
│  │  • Sendte mine case-studies                    │   │
│  │  • Hun lovede at læse dem                      │   │
│  │                                                 │   │
│  │  ANBEFALING:                                   │   │
│  │  • Hav ROI-beregning klar                      │   │
│  │  • Forbered CTO-speakerafcis                  │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

**Beskrivelse:** Genereret mødeforberedelse med kontaktinfo, identificerede behov, aftaler og anbefalinger.

## Demo-script:

```
SALGSPERSON: "Nu til noget VIRKELIGT værdifuldt. Forestil jer 
at sælgeren har talt med Maria i dag, og i morgen skal 
til møde med hende..."

[SKRIV]: "Forbered mig til mødet med NovoTech i morgen kl. 10"

SALGSPERSON: "Systemet genererer øjeblikkeligt en komplet 
mødeforberedelse med:
- Kontaktinfo og nøglepersoner
- Identifierede behov fra samtalerne
- Aftaler og løfter givet
- Specifikke anbefalinger

SALGSPERSONENS KOMMENTAR: 
'Hav ROI-beregning klar – forbered CTO-speakerafcis'

Dette ville tidligere kræve at sælgeren:
1. Gennemgik alle sine noter
2. Huskede hvad der blev sagt
3. Skrev en forberedelse fra bunden

NU: 2 sekunder. Alt er der."
```

---

# SCENARIE 6: Integration – "Kun 2 linjer kode"

**Formål:** Vis hvor let det er at implementere

## Screendump 6.1: Integration eksempel

```
┌─────────────────────────────────────────────────────────┐
│  BetterHuman_Brains – Integration                     │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  INSTALLATION (1 minut):                               │
│  ┌─────────────────────────────────────────────────┐   │
│  │ $ pip install betterhumanbrains                 │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  IMPORTERING:                                          │
│  ┌─────────────────────────────────────────────────┐   │
│  │ from betterhumanbrains import MemoryAgent       │   │
│  │                                                │   │
│  │ agent = MemoryAgent(                           │   │
│  │     api_key="din-api-nøgle"                    │   │
│  │ )                                              │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  BRUG:                                                 │
│  ┌─────────────────────────────────────────────────┐   │
│  │ response = agent.chat("Besked fra bruger")      │   │
│  │ # Hukommelse aktiveres automatisk              │   │
│  └─────────────────────────────────────────────────┘   │
│                                                         │
│  ✅ Færdig! Ingen konfiguration. Ingen training.        │
└─────────────────────────────────────────────────────────┘
```

**Beskrivelse:** Kodetvæ med tre enkle trin: installation, import, brug.

## Demo-script:

```
SALGSPERSON: "Lad mig vise hvor simpelt det er at implementere..."

[VIS integration-panel]

SALGSPERSON: "Trin 1: Installation med pip – ét kommandolinje
Trin 2: Importer biblioteket
Trin 3: Instantier agenten med din API-nøgle

Det ER literalt 2 linjers kode for at tilføje 
langtidshukommelse til ENHVER eksisterende AI-agent.

Ingen:
- Arkitekturændringer
- Omskrivning af eksisterende kode
- Training eller fine-tuning
- Dataindtastning

Vi siger 'under en dag' – men de fleste kunder er i gang 
på under en time."
```

---

# Bonus: Teknisk live-visning

## Screendump: Hukommelses-visualisering (valgfrit)

```
┌─────────────────────────────────────────────────────────┐
│  🧠 BetterHuman_Brains – Internt panel                 │
├─────────────────────────────────────────────────────────┤
│                                                         │
│  RETAIN          RECALL         REFLECT               │
│    ████           ██             █                    │
│    ████           ████           ██                   │
│    █████          ████           ███                  │
│                                                         │
│  ═══════════════════════════════════════════════════  │
│  Seneste lagret: "Maria Jensen, Salgschef, NovoTech"   │
│  Forespørgsler i cache: 3 | Gennemsnitlig recall: 0.2ms│
│  Mønstre identificeret: 1 | Indsigt genereret: 0      │
│  ═══════════════════════════════════════════════════  │
│                                                         │
│  ⚡ Live: Bruger skriver...                            │
└─────────────────────────────────────────────────────────┘
```

**Beskrivelse:** Teknisk dashboard der viser systemets tre kernefunktioner i aktion.

---

# Afslutning

## Tidsforbrug
- Scenarie 1 (Første samtale): 2 min
- Scenarie 2 (Anden samtale): 2 min
- Scenarie 3 (Forretningskontekst): 3 min
- Scenarie 4 (Historik): 3 min
- Scenarie 5 (Mødeforberedelse): 3 min
- Scenarie 6 (Integration): 2 min
- Buffer/spørgsmål: 5 min

**Total: ~20 minutter**

## Nøglebudskaber til afslutning

1. **Ingen kontekst-tab:** Hver samtale bygger videre på den forrige
2. **Automatisk læring:** Systemet forstår og gemmer uden manual indtastning
3. **Forretningsværdi:** Konkrete use-cases der sparer tid og forbedrer kundeservice
4. **Enkel integration:** 2 linjer kode – ingen barrierer for implementering

## Call to Action

"Ønsker I en gratis pilot-periode så I kan se systemet i jeres eget miljø?"

---

# Backup slides (PDF-format)

Hvis live-demo fejler:

1. **Slide 1:** Problem – AI starter fra nul hver gang
2. **Slide 2:** Løsning – BetterHuman_Brains Retain/Recall/Reflect
3. **Slide 3:** Screendumps fra hvert scenarie (for-optaget)
4. **Slide 4:** Integration – 2 linjer kode
5. **Slide 5:** ROI og case-studies
6. **Slide 6:** Kontakt og næste skridt

---

*Dokumentversion: 1.0*  
*Sidst opdateret: April 2026*  
*BedreHuman_Brains – AI-hukommelse der virker*
