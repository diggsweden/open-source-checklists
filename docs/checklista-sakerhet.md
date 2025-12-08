

# Checklista – säkerhet i öppna programvaruprojekt

**Syfte:** Stöd för systematiskt säkerhetsarbete i öppna projekt.

## A. Grundläggande säkerhetsarbete

- [ ] Projektets informationsklassning är genomförd och dokumenterad.
- [ ] Säkerhetskrav är definierade utifrån riskanalys och regelverk.
- [ ] Projektet följer gällande riktlinje för it-säkerhet och säker systemutveckling.

## B. Beroenden och komponenter

- [ ] Verktyg för beroendeanalys (SCA) används i CI-pipeline för att upptäcka sårbarheter och licensinkompatibiliteter (Must use SCA-tools in the CI pipeline to detect vulnerabilities and license incompatibilities).
- [ ] Det finns en rutin för att uppdatera beroenden (patchar, nya versioner) (Must have maintenance to quickly handle updating vulnerabilities).
- [ ] Automatiserad övervakning används för att bevaka kritiska sårbarheter i beroenden (Must use automated tooling to monitor dependency updates for critical vulnerabilities).
- [ ] Tredjepartskomponenters licenser och säkerhetspraxis är kända och dokumenterade.
- [ ] Hälsan hos varje nytt direkt projektberoende utvärderas när det läggs till (Should evaluate the health of every new direct project dependency that is added to the project).
- [ ] Pakethanterare används där möjligt för automatiska och konsekventa beroendeuppdateringar (Should prefer using package managers for automatic and consistent dependency updates).

## C. Kodkvalitet och utvecklingsflöde

- [ ] Statisk kodanalys (SAST) används i CI-pipeline för att upptäcka potentiella sårbarheter och dålig praxis (Should use SAST-tools in the CI pipeline to detect potential vulnerabilities and bad software practices).
- [ ] Linter-verktyg används i CI-pipeline för att upptäcka sårbarheter och dålig utvecklingspraxis (Must use linter tools in the CI pipeline to detect vulnerabilities and bad development practices).
- [ ] Kodgranskning (code review) görs innan ändringar släpps till huvudbranch (Should have a practice of code reviews).
- [ ] Läsbarhet och scope-krav säkerställer att nya PR:er inte är obfuskerade och användning av ogenomskinliga binärer minimeras (Should have good readability and scope requirements to ensure new PRs are not obfuscated).
- [ ] Behörigheter till repos är styrda enligt minsta möjliga behörighet.
- [ ] Skyddade brancher används där det är tekniskt möjligt (Must have enabled branch protection).
- [ ] Signerade commits/taggar används där risknivån motiverar det (Must have a practice of signed commits).
- [ ] Automatiserad testning och testtäckning används, inklusive tester för negativa fall (Should have automated testing and test coverage practices, including tests for negative cases).
- [ ] Projektets testmål och ambitioner är diskuterade och etablerade (Should discuss and establish the project's testing goals and ambitions).

## D. Sårbarhetshantering

- [ ] Det finns en tydlig väg för att rapportera sårbarheter (t.ex. SECURITY.md, kontaktadress) (Must have a security policy in place with information about where to report non-disclosure vulnerabilities).
- [ ] Ansvarig funktion/person för sårbarhetshantering är utsedd.
- [ ] Identifiering, bedömning och åtgärd av sårbarheter dokumenteras spårbart.
- [ ] Rutiner finns för snabb hantering av allvarliga sårbarheter.
- [ ] SBOM (Software Bill of Materials) produceras för projektet så att slutanvändare kan verifiera sårbarheter och licensinkompatibiliteter (Must produce an SBOM for the project).

## E. Data och konfiguration

- [ ] Källkod och data är tydligt separerade enligt informationsklassning.
- [ ] Informationsklassning följer ISO 27001/2 där relevant.
- [ ] Verktyg för secret scanning används för att upptäcka hemligheter (lösenord, loggar, tokens) (Must use secret scanning tools to detect secrets).
- [ ] Ingen intern eller känslig information ligger i öppna repos (personuppgifter, interna miljödetaljer, nycklar m.m.).
- [ ] Det finns riktlinjer för testdata (syntetisk, anonymiserad eller maskerad).

## F. Standarder och ramverk

- [ ] Projektet har tagit del av relevanta rekommendationer från OpenSSF/OWASP.
- [ ] Projektet strävar efter att ligga i linje med ISO/IEC 18974 där det är rimligt (ISO/IEC 18974 - Security Assurance).
- [ ] OpenSSF Scorecard används eller har övervägts för att bedöma och förbättra projektets säkerhetshälsa (OpenSSF Scorecard - Helps assess and improve the security health of our project).
- [ ] Projektets releaser signeras där det är relevant (Should sign any project releases).
- [ ] Publiceringsrättigheter för artefakter är begränsade (Must limit software publishing rights of artifacts).

---

## Se även – alla checklistor

- [Checklista – anskaffning och val av öppen programvara](checklista-anskaffning.md)
- [Checklista – hantering av ärenden, frågor och externa bidrag](checklista-arenden-community.md)
- [Checklista – bidrag till tredjeparts-OSS](checklista-bidrag-uppstrom.md)
- [Checklista – diarieföring och arkivering](checklista-diarie-arkiv.md)
- [Checklista – licensval och licenskompatibilitet](checklista-licenser.md)
- [Checklista – arbete på kodsamverkansplattform](checklista-plattform.md)
- [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md)
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md)
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md) ← du är här
- [Översikt – standarder och specifikationer](checklista-standarder.md)

