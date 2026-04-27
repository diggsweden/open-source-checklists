# Checklista – säkerhet i öppna programvaruprojekt

**Syfte:** Stöd för **OSS-specifikt** säkerhetsarbete. Allmänna säkerhetskrav (informationsklassning, riskanalys, hotmodellering, säker systemutveckling) hanteras i:

- **Riktlinje för it-säkerhet** (DIGG, intern)
- **Riktlinje för säker informationshantering** (DIGG, intern)

Den här checklistan kompletterar dessa med krav som är specifika för publicerad öppen programvara — SECURITY-policy, sårbarhetsrapportering enligt CVD, SBOM-leverans, beroendeanalys, signering, release-verifiering och liknande.

**Stilkonvention:** Punkter är krav (**SKA**) om inget annat anges. Punkter markerade **BÖR** är rekommendationer.

Den här checklistan är **kanonisk hemvist** för SECURITY-policy, sårbarhetsrapportering, SBOM och CI-säkerhetsverktyg. För branch protection, 2FA och code review se [checklista-plattform.md](checklista-plattform.md).

## A. Förutsättningar för publicering

- [ ] **SKA** — Allmänna säkerhetskrav (informationsklassning, riskanalys, säker systemutveckling) följer DIGG:s Riktlinje för it-säkerhet och Riktlinje för säker informationshantering.
- [ ] **SKA** — Källkoden är granskad utifrån informationsklassningen och bedömd som lämplig för publicering. *Källa: DIGG-riktlinje §Säkerhet genom hela livscykeln.*

## B. Beroenden och komponenter

- [ ] **SKA** — Verktyg för beroendeanalys (SCA) används i CI för att upptäcka sårbarheter och licensinkompatibiliteter.
- [ ] **SKA** — Det finns en rutin för att uppdatera beroenden (programfixar, nya versioner) snabbt vid kritiska sårbarheter.
- [ ] **SKA** — Automatiserad övervakning bevakar kritiska sårbarheter i beroenden (t.ex. Renovate, Dependabot).
- [ ] **SKA** — Tredjepartskomponenters licenser och säkerhetspraxis är kända och dokumenterade.
- [ ] **BÖR** — Hälsan hos varje nytt direkt beroende utvärderas innan det läggs till.
- [ ] **BÖR** — Pakethanterare används där möjligt för automatiska och konsekventa beroendeuppdateringar.

## C. Kodkvalitet och utvecklingsflöde

- [ ] **SKA** — Linter-verktyg används i CI för att upptäcka programfel och dålig utvecklingspraxis. Säkerhetsspecifika linters (Bandit, gosec etc.) komplementerar SAST/SCA.
- [ ] **SKA** — Statisk kodanalys (SAST) används i CI för att upptäcka potentiella sårbarheter.
- [ ] **SKA** — Verktyg för secret scanning används för att upptäcka oavsiktliga hemligheter (lösenord, tokens, API-nycklar).
- [ ] **SKA** — Code review krävs innan merge — se [checklista-plattform.md §C](checklista-plattform.md#c-branch-strategi-code-review-och-ändringsflöde).
- [ ] **SKA** — Branch protection är aktiverad — se [checklista-plattform.md §C](checklista-plattform.md#c-branch-strategi-code-review-och-ändringsflöde).
- [ ] **SKA** — Behörigheter följer least privilege — se [checklista-plattform.md §B](checklista-plattform.md#b-behörigheter-och-åtkomst).
- [ ] **SKA** — Automatiserad testning används, inklusive tester för negativa fall.
- [ ] **BÖR** — Läsbarhet och scope-krav säkerställer att nya ändringsförfrågningar inte är obfuskerade; ogenomskinliga binärer minimeras.
- [ ] **BÖR** — Projektets testmål och ambitioner är diskuterade och etablerade.

## D. Sårbarhetshantering

- [ ] **SKA** — Projektet har en publicerad `SECURITY.md` med rapporteringsväg och kontaktadress. *Källa: OSPS-VM-04.01 (L1).*
- [ ] **SKA** — En **privat** rapporteringskanal finns (t.ex. GitHub Private Vulnerability Reporting eller särskild mejl). *Källa: OSPS-VM-05.01 (L2).*
- [ ] **SKA** — `SECURITY.md` anger ett tidsfönster för bekräftelse och preliminär bedömning (rekommenderat: ≤ 5 arbetsdagar). *Källa: OSPS-VM-03.01 (L2).*
- [ ] **SKA** — Ansvarig funktion eller person för sårbarhetshantering är utsedd. *Källa: DIGG-riktlinje §Säkerhet genom hela livscykeln.*
- [ ] **SKA** — Identifiering, bedömning och åtgärd av sårbarheter dokumenteras spårbart.
- [ ] **SKA** — Rutiner finns för snabb hantering av allvarliga sårbarheter.
- [ ] **SKA** — SBOM (SPDX 2.3 eller CycloneDX 1.5) genereras i CI och **levereras med varje release**, så att slutanvändare kan verifiera sårbarheter och licenser. *Källa: OSPS-QA-02.02 (L3).*
- [ ] **BÖR** — Om projektet exponerar publika gränssnitt: säkerställ att resultaten av hotmodellering och attackytanalys (utförd enligt Riktlinje för it-säkerhet) är tillräckliga även för det öppet publicerade snittet. *Källa: OSPS-SA-03.02 (L3).*

## E. Data och konfiguration i publicerad kod

OSS-specifika krav. Generell informationshantering följer Riktlinje för säker informationshantering.

- [ ] **SKA** — Ingen intern eller känslig information ligger i öppna repos (personuppgifter, autentiseringsuppgifter, interna miljödetaljer, nycklar). *Källa: DIGG-riktlinje §Säkerhet genom hela livscykeln.*
- [ ] **SKA** — Källkod och data är tydligt separerade. Konfigurationsparametrar och driftsättning specifika för myndighetens miljöer ligger utanför det publicerade repot.
- [ ] **SKA** — Testdata är syntetisk, anonymiserad eller maskerad.

## F. Releaser och leveranskedja

- [ ] **SKA** — Releaser signeras (Sigstore/cosign rekommenderas; GPG accepteras). *Källa: OSPS-BR-06.01 (L2).*
- [ ] **SKA** — Releaser har publika instruktioner för verifiering av integritet och äkthet. *Källa: OSPS-DO-03.01 (L2).*
- [ ] **SKA** — CI hämtar dependencies över krypterade kanaler (HTTPS/TLS) och release-pipelinens externa tjänster nås krypterat. *Källa: OSPS-BR-07.02 (L2).*
- [ ] **SKA** — Genererade artefakter (build-output, kompilerade binärer) versionshanteras inte i `git`; `.gitignore` täcker språkets/byggsystemets default-output. *Källa: OSPS-QA-05.01 (L2).*
- [ ] **SKA** — Publiceringsrättigheter för artefakter är begränsade.
- [ ] **BÖR** — OpenSSF Scorecard används för att bedöma och förbättra projektets säkerhetshälsa.
- [ ] **BÖR** — Projektet siktar på en SLSA-nivå relevant för risken (minst Build L2).

## G. OSS-specifika ramverk

- [ ] **SKA** — Projektet har tagit del av relevanta OSS-rekommendationer från [OpenSSF](https://openssf.org/). *Refereras explicit i DIGG-riktlinje §Säkerhet genom hela livscykeln.*
- [ ] **BÖR** — [OpenSSF Concise Guide for Developing More Secure Software](https://best.openssf.org/Concise-Guide-for-Developing-More-Secure-Software) är genomgången.
- [ ] **BÖR** — Projektet ligger i linje med [ISO/IEC 18974](https://www.iso.org/standard/86529.html) (OpenChain Security Assurance) där det är rimligt.

---

## Källor

- **DIGG: Riktlinje för öppen programvara** (Dnr 2026-02797, beslutad 2026-04-07) — *Säkerhet genom hela livscykeln*. (OpenSSF och OWASP refereras explicit.)
- [OpenSSF OSPS Baseline](https://baseline.openssf.org/) — VM-03 till VM-06, BR-06, DO-03, QA-02, SA-03
- [OpenSSF Concise Guide for Developing More Secure Software](https://best.openssf.org/Concise-Guide-for-Developing-More-Secure-Software)
- [OpenSSF Scorecard](https://github.com/ossf/scorecard)
- [Sigstore](https://www.sigstore.dev/) — release-signering
- [SLSA – Supply-chain Levels for Software Artifacts](https://slsa.dev/)
- [SPDX (ISO/IEC 5962)](https://spdx.dev/) och [CycloneDX](https://cyclonedx.org/) — SBOM-format
- [OWASP Cheatsheets](https://cheatsheetseries.owasp.org/), [OWASP ASVS](https://owasp.org/www-project-application-security-verification-standard/)
- [ISO/IEC 27001/2](https://www.iso.org/standard/27001) — informationssäkerhet
- [ISO/IEC 18974](https://www.iso.org/standard/86529.html) — Security Assurance
- [CNCF Software Supply Chain Best Practices](https://github.com/cncf/tag-security/blob/main/supply-chain-security/supply-chain-security-paper/CNCF_SSCP_v1.pdf)

---

## Se även – alla checklistor

- [Checklista – anskaffning och val av öppen programvara](checklista-anskaffning.md)
- [Checklista – använda öppen programvara](checklista-anvandning.md)
- [Checklista – hantering av ärenden, frågor och externa bidrag](checklista-arenden-community.md)
- [Checklista – bidrag till tredjeparts-OSS](checklista-bidrag-uppstrom.md)
- [Checklista – diarieföring och arkivering](checklista-diarie-arkiv.md)
- [Checklista – licensval och licenskompatibilitet](checklista-licenser.md)
- [Checklista – arbete på kodsamverkansplattform](checklista-plattform.md)
- [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md)
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md)
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md) ← du är här
- [Översikt – standarder och specifikationer](checklista-standarder.md)
