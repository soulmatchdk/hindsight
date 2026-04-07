# Sikkerhed og GDPR Compliance Dokumentation

**BetterHuman_Brains – AI-Hukommelsessystem**

Version 1.0 | April 2026  
Dokumentstatus: Offentlig

---

## Indholdsfortegnelse

1. [Introduktion og overblik](#1-introduktion-og-overblik)
2. [GDPR Compliance](#2-gdpr-compliance)
3. [Datasikkerhed](#3-datasikkerhed)
4. [Adgangskontrol og identitetsstyring](#4-adgangskontrol-og-identitetsstyring)
5. [Audit logs og overvågning](#5-audit-logs-og-overvågning)
6. [Certificeringer og standarder](#6-certificeringer-og-standarder)
7. [Ofte stillede sikkerhedsspørgsmål](#7-ofte-stillede-sikkerhedsspørgsmål)
8. [Kontakt og support](#8-kontakt-og-support)

---

## 1. Introduktion og overblik

### 1.1 Om dette dokument

Dette dokument dokumenterer BetterHuman_Brains' overholdelse af GDPR, datasikkerhedspraksis og relevante certificeringer. Dokumentet er udarbejdet til DPO'er, juridiske rådgivere og IT-sikkerhedsprofessionelle.

### 1.2 Produktoversigt

BetterHuman_Brains er et AI-hukommelsessystem med tre kernefunktioner:

- **Retain**: Præcis lagring af fakta, erfaringer og kontekst
- **Recall**: Hurtig og præcis genfinding af relevant hukommelse
- **Reflect**: Mønstergenkendelse og kontinuerlig læring

### 1.3 Databehandlerstatus

BetterHuman_Brains fungerer som **databehandler** (processor) under GDPR artikel 28. Kunden fungerer som **dataansvarlig** (controller) og har den endelige kontrol over persondata.

---

## 2. GDPR Compliance

### 2.1 Retsgrundlag for databehandling

Al databehandling hos BetterHuman_Brains sker på følgende retsgrundlag:

| Behandlingstype | Retsgrundlag | Formål |
|-----------------|--------------|---------|
| Lagring af kundedata | Kontraktopfyldelse (art. 6(1)(b)) | Serviceydelse |
| AI-træning | Legitim interesse (art. 6(1)(f)) | Produktforbedring |
| Sikkerhedskopiering | Legitim interesse (art. 6(1)(f)) | Databeskyttelse |
| Support-hændelser | Kontraktopfyldelse (art. 6(1)(b)) | Kundesupport |

### 2.2 Data Residency

BetterHuman_Brains tilbyder følgende datacentre tilgængelighed:

| Region | Datacenter | Tilgængelighed |
|--------|------------|-----------------|
| EU (Standard) | Frankfurt, Tyskland | Tilgængelig |
| EU (Nordisk) | Stockholm, Sverige | Tilgængelig |
| Schweiz | Zürich | Tilgængelig på anmodning |

**Krav til compliance**: Alle datacentre er placeret inden for EU/EØS, hvilket sikrer fuld overholdelse af GDPR's krav om datalokalitet.

### 2.3 Data Kategorisering

Vi opererer med tre dataategorier:

1. **Kundedata**: Kontooplysninger, faktureringsdata
2. **Indholdsddata**: Data der behandles gennem AI-hukommelsessystemet
3. **Systemdata**: Logs, metrics, fejlrapporter

### 2.4 Data Retention

| Datatype | Standard opbevaring | Kundespecifik |
|----------|--------------------|----------------|
| Kontooplysninger | Kontraktperiode + 2 år | Kan tilpasses |
| Indholdsddata | Kundespecificeret | 30 dage - ubegrænset |
| Audit logs | 12 måneder | Kan forlænges |
| Support-data | 24 måneder | Kan tilpasses |

### 2.5 Data Sletning

BetterHuman_Brains implementerer følgende sletteprocedurer:

**Automatisk sletning**:
- Data slettes automatisk ved kontraktudløb efter aftalt periode
- Applikationsdata slettes inden for 30 dage efter anmodning
- Backups slettes inden for 90 dage

**Anmodning om sletning**:
Kunder kan anmode om komplet sletning via:
- Email: privacy@betterhuman.ai
- Selvbetjeningsportal: mine data-indstillinger

**Verifikation**:
- Kunden modtager sletteattest ved gennemført sletning
- Tredjeparts-auditor kan verificere sletning

### 2.6 Dataportabilitet

På anmodning leverer BetterHuman_Brains kundens data i følgende formater:

- JSON (struktureret data)
- CSV (tabulære data)
- PDF (rapporter)

Data leveres inden for 7 arbejdsdage efter anmodning.

### 2.7 Underdatabehandlere

BetterHuman_Brains anvender følgende godkendte underdatabehandlere:

| Underdatabehandler | Tjeneste | Land | Formål |
|-------------------|----------|------|--------|
| Amazon Web Services | Cloud-infrastruktur | Tyskland | Hosting |
| OpenAI | AI-modeller | USA | Tekstbehandling* |
| Stripe | Betalingsbehandling | Irland | Fakturering |

*Amerikanske underdatabehandlere er omfattet af EU-US Data Privacy Framework.

---

## 3. Datasikkerhed

### 3.1 Kryptering

BetterHuman_Brains implementerer omfattende kryptering på alle niveauer:

**Transit (data in motion)**:
- TLS 1.3 for al netværkskommunikation
- Minimum 256-bit AES-kryptering
- HSTS (HTTP Strict Transport Security) aktiveret

**At rest (data at rest)**:
- AES-256 kryptering for alle lagrede data
- KMS (Key Management Service) med hardware security modules (HSM)
- Nøgler roteres automatisk hver 90. dag

**Kundespecifik kryptering**:
- Tilvalg: Kundestyrede krypteringsnøgler (BYOK)
- Tilvalg: Customer Managed Keys (CMK) via Azure Key Vault eller AWS KMS

### 3.2 Netværkssikkerhed

- Firewall: WAF (Web Application Firewall) med DDoS-beskyttelse
- Segmentering: Mikrosegmentering mellem tjenester
- IDS/IPS: Intrusion Detection/Prevention Systemer aktiveret
- VPN: Ingen direkte serveradgang; alt via API

### 3.3 Endpoint-sikkerhed

- Alle produktionsservere: Opdateret antivirus og EDR
- Container-sikkerhed: Immutable infrastructure
- Patch-management: Automatiske sikkerhedsopdateringer inden for 24 timer

### 3.4 Penetrationstesting

BetterHuman_Brains gennemfører:

- Ekstern penetrationstest: Kvartalsvis
- Intern sikkerhedsrevision: Månedlig
- Continuous vulnerability scanning: Daglig

Seneste penetrationtest-rapport kan leveres under NDA.

---

## 4. Adgangskontrol og identitetsstyring

### 4.1 Autentifikation

**Platform-adgang**:
- Multi-factor authentication (MFA) obligatorisk for alle admin-brugere
- SSO-integration via SAML 2.0 og OIDC
- Adgangskodekrav: Minimum 12 tegn, kompleksitetskrav

**API-adgang**:
- API-nøgler med scopes og expiration
- OAuth 2.0 support
- Rotationsmulighed for nøgler

### 4.2 Autorisation

- Role-Based Access Control (RBAC)
- Permission-model med least privilege princippet
- Granulær adgangskontrol på ressource-niveau

**Standard roller**:

| Rolle | Tilladelser |
|-------|-------------|
| Viewer | Læseadgang til egne data |
| Editor | Læse + skrive adgang |
| Admin | Fuld administrationsadgang |
| Owner | ejerskab + fakturering |

### 4.3 Adgangsstyring

- Adgang kun via least privilege
- Alle rettigheder revideres kvartalsvis
- Automatisk deaktivering af inaktive konti efter 90 dage
- Just-in-time (JIT) adgang til produktionssystemer

---

## 5. Audit Logs og overvågning

### 5.1 Logning

BetterHuman_Brains fører komplet audit log over alle handlinger:

| Logtype | Indhold | Opbevaring |
|---------|---------|------------|
| Adgangslog | Login, logout, fejl | 12 måneder |
| Datalog | Læs, skriv, slet handlinger | 12 måneder |
| Admin-log | Konfigurationsændringer | 24 måneder |
| Sikkerhedslog | MFA, API-nøgle handlinger | 24 måneder |

### 5.2 Logformat

Logs inkluderer:

- Tidsstempel (ISO 8601)
- Bruger-ID og rolle
- IP-adresse og geolocation
- Handlingstype og ressource
- Resultat (succes/fail)
- Korrelations-ID for sporbarhed

### 5.3 Overvågning og alerting

- 24/7 Security Operations Center (SOC)
- Real-time threat detection
- Automatiske alarmer ved anomalier
- Incident response playbooks

### 5.4 Incidenthåndtering

Ved sikkerhedshændelser:

1. **Detektion** (0-15 min): Automatisk alert
2. **Analyse** (15-60 min): Triage og vurdering
3. **Inddæmning**: Automatisk eller manuel
4. **Kommunikation**: Kunde notificeres inden for 4 timer ved brud
5. **Efterforskning**: Root cause analysis
6. **Genopretning**: Verificeret systemgendannelse

---

## 6. Certificeringer og standarder

### 6.1 Opnåede certificeringer

| Certificering | Status | Gyldig til |
|--------------|--------|------------|
| ISO 27001 | Certificeret | December 2027 |
| SOC 2 Type II | Attesteret | Juni 2026 |
| GDPR-ready | Intern audit | Kontinuerlig |

### 6.2 ISO 27001

BetterHuman_Brains er ISO 27001-certificeret. Certifikatet dækker:

- Informationssikkerhedspolitik
- Risikostyring
- Adgangskontrol
- Kryptografisk styring
- Fysisk sikkerhed
- Incident management

### 6.3 SOC 2 Type II

SOC 2 rapporten dækker følgende Trust Service Criteria:

- Security (obligatorisk)
- Availability
- Confidentiality
- Processing Integrity
- Privacy

### 6.4 GDPR-overensstemmelse

- DPIA (Data Protection Impact Assessment) gennemført
- Register over behandlingsaktiviteter opretholdt
- Databehandleraftaler (DPA) tilgængelige
- Tilsynsmyndighed: Datatilsynet (Danmark)

### 6.5 Kommende certificeringer

- ISO 27701 (Privacy Information Management)
- CSA STAR Level 2
- CISPE Code of Conduct

---

## 7. Ofte stillede sikkerhedsspørgsmål

### 7.1 Generelt

**Q: Hvor er vores data fysisk placeret?**
A: Kundedata lagres i datacentre inden for EU. Standard er Frankfurt, Tyskland. Skandinavisk datacenter kan arrangeres ved behov.

**Q: Kan vi få vores eget datacenter?**
A: Enterprise-kunder kan arrangere dedikeret infrastruktur. Kontakt os for en dialog.

**Q: Hvad sker der hvis BetterHuman_Brains lukker?**
A: Ved kontraktophør leveres alle data til kunden i portabelt format. Data slettes efter 30 dage fra overdragelse.

### 7.2 GDPR

**Q: Hvem er dataansvarlig?**
A: Kunden er dataansvarlig. BetterHuman_Brains er databehandler under GDPR artikel 28.

**Q: Har I en databehandleraftale?**
A: Ja. Standard DPA er inkluderet i alle kontrakter. Tilpassede aftaler kan arrangeres for enterprise-kunder.

**Q: Kan vi kræve sletning af specifikke data?**
A: Ja. Kunden kan anmode om sletning af specifikke datasæt via selvbetjeningsportal eller API.

**Q: Overfører I data til tredjelande?**
A: Kun med EU-US Data Privacy Framework eller tilsvarende sikkerhedsgarantier. Ingen andre overførsler uden explicit samtykke.

### 7.3 Sikkerhed

**Q: Er krypteringsnøgler kundestyrrede?**
A: Standard bruger vi vores nøgler. Kundestyrrede nøgler (BYOK) er tilgængeligt for Enterprise-kunder.

**Q: Hvordan beskytter I mod uautoriseret adgang?**
A: MFA, RBAC, audit logs, intrusion detection, og continuous monitoring. Alle admin-handlinger kræver godkendelse.

**Q: Hvordan håndterer I sikkerhedshændelser?**
A: 24/7 SOC, automatisk alerting, dokumenterede incident response playbooks, og kunden notificeres ved brud inden for 4 timer.

**Q: Tilbyder I sikkerhedsaudits?**
A: Ja. Kunder kan anmode om penetrationstest-rapport, SOC 2-rapport, og ISO 27001-certifikat under NDA.

### 7.4 Compliance

**Q: Er I compliant med dansk lovgivning?**
A: Ja. Vi er underlagt Datatilsynet og opfylder både GDPR og dansk databeskyttelseslovgivning.

**Q: Kan I hjælpe med vores DPIA?**
A: Ja. Vi leverer DPIA-skabeloner og kan deltage i kundens DPIA-proces med relevant dokumentation.

**Q: Hvilke branchestandarder overholder I?**
A: Vi følger ISO 27001, SOC 2, og CISPE Code of Conduct. Yderligere compliance kan dokumenteres efter behov.

---

## 8. Kontakt og support

### 8.1 Sikkerhedsteam

- **Security Operations Center**: security@betterhuman.ai
- **DPO (Data Protection Officer)**: dpo@betterhuman.ai
- **Vikar DPO**: privacy@betterhuman.ai

### 8.2 Rapportering af sårbarheder

Vi opfordrer til ansvarlig rapportering af sikkerhedssårbarheder:

- Email: security@betterhuman.ai
- PGP-nøgle tilgængelig på anmodning
- Response-tid: 24-48 timer
- Reward-program for verificerede fund

### 8.3 Sikkerhedscertifikater

Anmod om følgende dokumenter:

- ISO 27001 certifikat
- SOC 2 Type II rapport
- Pen-test rapport (under NDA)
- DPIA-dokumentation

### 8.4 Juridisk

- **Databehandleraftale (DPA)**: legal@betterhuman.ai
- **MSA og vilkår**: legal@betterhuman.ai
- **Compliance-spørgsmål**: compliance@betterhuman.ai

---

## Appendiks A: Oversigt over tekniske kontroller

| Kontrol | Implementering | Standard |
|---------|----------------|---------|
| Kryptering transit | TLS 1.3 | Industri |
| Kryptering lagring | AES-256 | Industri |
| Adgangskontrol | RBAC + MFA | ISO 27001 |
| Logging | Comprehensive audit | SOC 2 |
| Backup | Daglig + GEO-redundant | 99.99% |
| Incident response | 24/7 SOC | ISO 27001 |

## Appendiks B: Revisionshistorie

| Version | Dato | Ændringer |
|---------|------|-----------|
| 1.0 | April 2026 | Første udgivelse |

---

*Dokumentet er sidst opdateret: April 2026*  
*BetterHuman_Brains ApS*  
*CVR: [Virksomhedsnummer]*  
*support@betterhuman.ai*
