# Checklista – publicering av version 1.0.0

**Syfte:** Säkerställa att projekt uppfyller alla tekniska och operativa krav för en stabil 1.0-release.

**Förutsättning:** Den här checklistan är en fortsättning och fördjupning av [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md). Grundkraven där SKA vara uppfyllda innan arbete med 1.0-release påbörjas.

**Stilkonvention:** På grund av att den här checklistan är grupperad efter krav-styrka använder den ✅/🔵-rubriker istället för per-rad **SKA**/**BÖR**-prefix. Alla punkter under ✅ är krav (SKA), alla under 🔵 är rekommendationer (BÖR).

---

## ✅ SKA

### Dokumentation

- [ ] `README.md` med:
  - Badges (version, OpenSSF Scorecard, licens, REUSE-status)
  - Projektbeskrivning + objectives
  - Installationsinstruktioner
  - Användningsexempel
  - Maintainer-sektion (se [forvaltning §A](checklista-publicering-forvaltning.md#a-beslut-ansvar-och-förvaltare))
  - Maturity-status (alpha/beta/stable)
- [ ] `LICENSE`
- [ ] `SECURITY.md` — se [sakerhet §D](checklista-sakerhet.md#d-sårbarhetshantering)
- [ ] `CONTRIBUTING.md`
- [ ] `CODE_OF_CONDUCT.md`
- [ ] `CHANGELOG.md` (Keep-a-Changelog format)
- [ ] `publiccode.yml` (för upptäckbarhet)
- [ ] `docs/DEVELOPMENT.md` med utvecklingsinstruktioner
- [ ] Verifieringsinstruktioner för release-integritet (signaturkontroll, hashar)

### Juridik och efterlevnad

- [ ] REUSE-efterlevnad (SPDX-headers i alla källfiler) — se [licenser §D](checklista-licenser.md#d-copyright-och-märkning-reusespdx)
- [ ] Licenskompatibilitet verifierad
- [ ] Namn-/varumärkeskontroll utförd
- [ ] Inga SNAPSHOT-beroenden

### Kodkvalitet

- [ ] Testtäckning enligt projektets dokumenterade mål
- [ ] Publika API:er har dokumentation
- [ ] Code review genomförd — se [plattform §C](checklista-plattform.md#c-branch-strategi-code-review-och-ändringsflöde)

### CI/CD och säkerhet

- [ ] CI-arbetsflöde för ändringsförfrågningar (PR/MR)
- [ ] Test-CI-arbetsflöde
- [ ] Release-CI-arbetsflöde
- [ ] Branch protection — se [plattform §C](checklista-plattform.md#c-branch-strategi-code-review-och-ändringsflöde)
- [ ] Sårbarhetsskanning av beroenden (SCA) — se [sakerhet §B](checklista-sakerhet.md#b-beroenden-och-komponenter)
- [ ] SAST i CI — se [sakerhet §C](checklista-sakerhet.md#c-kodkvalitet-och-utvecklingsflöde)
- [ ] Linter konfigurerad
- [ ] Secret scanning aktiverad
- [ ] Release-signering konfigurerad (Sigstore/cosign rekommenderas) — se [sakerhet §F](checklista-sakerhet.md#f-releaser-och-leveranskedja)
- [ ] SBOM-generering (SPDX 2.3 eller CycloneDX 1.5) **levereras med varje release** — se [sakerhet §D](checklista-sakerhet.md#d-sårbarhetshantering)
- [ ] CI-linter och kontroller kan köras lokalt utan CI

### Versionshantering och releasekrav

- [ ] API stabilt (eller implementerar stabil specifikation)
- [ ] Inga planerade brytande ändringar
- [ ] Version följer Semantic Versioning 2.0.0
- [ ] Conventional Commits-format används (samma som [forvaltning §G](checklista-publicering-forvaltning.md#g-versionshantering-och-releaser))
- [ ] Stödfönster publicerat ("säkerhetsuppdateringar fram till …")

## 🔵 BÖR

### Ytterligare kvalitet

- [ ] Exempel i dokumentation
- [ ] Ändringsloggflöde i CI (auto-generering ur Conventional Commits)
- [ ] Säkerhetsgranskning genomförd och dokumenterad
- [ ] OpenSSF Scorecard-integration
- [ ] SLSA Build Level ≥ 2
- [ ] Signerade commits

### Utvecklingspraxis

- [ ] Ärendemallar konfigurerade
- [ ] Mall för ändringsförfrågningar konfigurerad

---

## Stack-specifika krav (om tillämpligt)

### Java Library — Maven/POM

- [ ] `groupId`, `artifactId`, `version` (semantisk versionering)
- [ ] `name`, `description`, `url`
- [ ] `licenses`-block
- [ ] `scm`-block
- [ ] `maven-enforcer-plugin` konfigurerad
- [ ] `central-release`-profil med:
  - `maven-gpg-plugin`
  - `maven-source-plugin`
  - `maven-javadoc-plugin`
- [ ] `central-publishing-maven-plugin` konfigurerad

### Java App — Maven/POM

- [ ] `groupId`, `artifactId`, `version` (semantisk versionering)
- [ ] `name`, `description`, `url`
- [ ] `licenses`-block
- [ ] `scm`-block
- [ ] `maven-enforcer-plugin` konfigurerad

### JS/TS Lib — package.json

- [ ] `name`, `version` (semantisk versionering)
- [ ] `description`
- [ ] `license`
- [ ] `repository`-block

---

## Kriterier

**Redo för 1.0.0 när:**
- Alla tillämpliga SKA-punkter är avklarade
- Inga SNAPSHOT-beroenden
- Tester passerar med dokumenterad täckning
- API är stabilt (inga brytande ändringar planerade)

**Stanna i 0.x när:**
- Implementerar utkastspecifikationer
- API utvecklas fortfarande baserat på återkoppling
- Brytande ändringar förväntas

---

## Källor

- **DIGG: Riktlinje för öppen programvara** (Dnr 2026-02797, beslutad 2026-04-07) — *Publicera öppen programvara*, *Dokumentation, rutiner och projekthälsa*
- [diggsweden/open-source-project-template](https://github.com/diggsweden/open-source-project-template) — referensimplementering
- [OpenSSF OSPS Baseline](https://baseline.openssf.org/) — alla kategorier
- [Standard for Public Code](https://standard.publiccode.net/)
- [Semantic Versioning 2.0.0](https://semver.org/)
- [Keep a Changelog 1.1.0](https://keepachangelog.com/)
- [Conventional Commits](https://www.conventionalcommits.org/)
- [REUSE Software](https://reuse.software/) och [SPDX](https://spdx.dev/)
- [Sigstore](https://www.sigstore.dev/) och [SLSA](https://slsa.dev/)
- [PublicCode.yml-specifikationen](https://yml.publiccode.tools/)

För full ramverkslista, se [checklista-standarder.md](checklista-standarder.md).

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
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md) ← du är här
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md)
- [Översikt – standarder och specifikationer](checklista-standarder.md)
