
# Checklista – publicering av version 1.0.0

**Syfte:** Säkerställa att projekt uppfyller alla tekniska och operativa krav för en stabil 1.0-release.

**Förutsättning:** Denna checklista är en fortsättning och fördjupning av [Checklista – förberedelse inför publicering av öppen programvara](checklista-publicering-forvaltning.md). Grundläggande krav från den checklistan ska vara uppfyllda innan arbete med 1.0-release påbörjas.

---

## ✅ Krav

### Dokumentation

- [ ] **README.md** med:
  - [ ] Badges (version, openssf, licens, reuse-status)
  - [ ] Projektbeskrivning
  - [ ] Installationsinstruktioner
  - [ ] Användningsexempel
  - [ ] Förvaltare (Maintainer)
- [ ] **LICENSE** fil
- [ ] **SECURITY.md** med process för sårbarhetsrapportering
- [ ] **CONTRIBUTING.md** med riktlinjer för bidrag
- [ ] **CODE_OF_CONDUCT.md**
- [ ] **docs/DEVELOPMENT.md** med utvecklingsinstruktioner

### Juridik och efterlevnad

- [ ] REUSE-efterlevnad (SPDX-headers i alla källfiler)
- [ ] Licenskompatibilitet verifierad
- [ ] Namn-/varumärkeskontroll utförd
- [ ] Inga SNAPSHOT-beroenden

### Kodkvalitet

- [ ] Testtäckning ≥ 50%
- [ ] Publika API:er har dokumentation
- [ ] Koden har granskats

### Git hosting och säkerhet – CI/CD

- [ ] Pull request-CI-arbetsflöde
- [ ] Test-CI-arbetsflöde
- [ ] Release-CI-arbetsflöde
- [ ] Branch protection aktiverad
- [ ] Branch ruleset aktiverad – endast auktoriserade har skrivåtkomst
- [ ] Sårbarhetsskanning av beroenden i CI aktiverad
- [ ] Linter konfigurerad
- [ ] Secret scanning aktiverad
- [ ] GPG-signering konfigurerad för releaser
- [ ] SBOM-generering konfigurerad
- [ ] OpenSSF Scorecard-integration
- [ ] Signerade commits dokumenterade
- [ ] CI-linter och kontroller kan köras lokalt utan CI

### Releasekrav

- [ ] API stabilt (eller implementerar stabil specifikation)
- [ ] Inga planerade brytande ändringar
- [ ] Version följer semantisk versionering

### Java Library Maven/POM-konfiguration (om tillämpligt)

- [ ] groupId, artifactId, version (semantisk versionering)
- [ ] name, description, url
- [ ] licenses-block
- [ ] scm-block
- [ ] maven-enforcer-plugin konfigurerad
- [ ] central-release profil med:
  - [ ] maven-gpg-plugin
  - [ ] maven-source-plugin
  - [ ] maven-javadoc-plugin
- [ ] central-publishing-maven-plugin konfigurerad

### Java App Maven/POM-konfiguration (om tillämpligt)

- [ ] groupId, artifactId, version (semantisk versionering)
- [ ] name, description, url
- [ ] licenses-block
- [ ] scm-block
- [ ] maven-enforcer-plugin konfigurerad

### JS/TS Lib-konfiguration (om tillämpligt)

- [ ] name, version (semantisk versionering)
- [ ] description
- [ ] license
- [ ] repository-block

## 🔵 Rekommenderat

### Ytterligare kvalitet

- [ ] Exempel i dokumentation
- [ ] Ändringslogg-flöde i CI
- [ ] **CHANGELOG.md** (Keep-a-Changelog format)
- [ ] Säkerhetsgranskning genomförd och dokumenterad

### Utvecklingspraxis

- [ ] Conventional commits format används
- [ ] Issue-mallar konfigurerade
- [ ] PR-mall konfigurerad

## Kriterier

✅ **Redo för 1.0.0 när**:
- Alla tillämpliga punkter avklarade
- Inga SNAPSHOT-beroenden
- Tester passerar med bra täckning
- API stabilt (inga brytande ändringar planerade)

⚠️ **Stanna i 0.x när**:
- Implementerar utkastspecifikationer
- API utvecklas fortfarande baserat på återkoppling från användare
- Brytande ändringar förväntas

---

---

## Se även – alla checklistor

- [Checklista – anskaffning och val av öppen programvara](checklista-anskaffning.md)
- [Checklista – hantering av ärenden, frågor och externa bidrag](checklista-arenden-community.md)
- [Checklista – bidrag till tredjeparts-OSS](checklista-bidrag-uppstrom.md)
- [Checklista – diarieföring och arkivering](checklista-diarie-arkiv.md)
- [Checklista – licensval och licenskompatibilitet](checklista-licenser.md)
- [Checklista – arbete på kodsamverkansplattform](checklista-plattform.md)
- [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md)
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md) ← du är här
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md)
- [Översikt – standarder och specifikationer](checklista-standarder.md)

## Externa resurser

- [Digg Open Source Checklist](https://github.com/diggsweden/open-source-project-template/blob/main/docs/Open_Source_Checklist.md)
- [Digg Sweden Open Source Project Template](https://github.com/diggsweden/open-source-project-template)
