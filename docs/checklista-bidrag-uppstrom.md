# Checklista – bidrag till tredjeparts-OSS

**Syfte:** Stöd när du som anställd bidrar med programfixar (patches) till ett externt open source-bibliotek som vi använder internt.

**Stilkonvention:** Punkter är krav (**SKA**) om inget annat anges. Punkter markerade **BÖR** är rekommendationer.

## A. Innan du skriver någon kod

- [ ] **SKA** — Kollat intern policy: får jag bidra till detta projekt på arbetstid?
- [ ] **SKA** — Fått godkännande från chef eller uppdragsansvarig vid behov.
- [ ] **SKA** — Identifierat exakt uppströms-repo och versionen som används internt.
- [ ] **SKA** — Verifierat att projektet har en OSI-godkänd licens.
- [ ] **SKA** — Verifierat att licensen är kompatibel med hur vi använder biblioteket — se [checklista-licenser.md §C](checklista-licenser.md#c-beroenden-och-kompatibilitet).
- [ ] **SKA** — Vid minsta tvekan kring licensfrågor: kontaktat juridik/Legal för go/no-go.
- [ ] **SKA** — Kollat om projektet kräver CLA (Contributor License Agreement) eller DCO (Developer Certificate of Origin).
- [ ] **SKA** — Kollat om det redan finns ett företags- eller myndighets-CLA på plats.
- [ ] **SKA** — Inte signerat någon CLA själv utan att först fråga juridik eller behörig person.
- [ ] **SKA** — Läst igenom projektets `CONTRIBUTING.md`, utvecklingsguide eller wiki.
- [ ] **SKA** — Förstår projektets branch-strategi och målbranch (`main`, `develop`, etc.).
- [ ] **SKA** — Vet hur tester och linters körs enligt projektets instruktioner.

## B. Avgränsa ändringen

- [ ] **SKA** — Sökt efter befintliga ärenden (issues) och ändringsförfrågningar (PR/MR) för samma programfel eller funktion.
- [ ] **SKA** — Undvikit att duplicera pågående arbete (kommenterat eller anslutit till befintlig diskussion).
- [ ] **SKA** — Öppnat ett ärende eller kommentar som beskriver problemet och föreslagen lösning.
- [ ] **SKA** — Försäkrat sig om att maintainerna vill ha den här typen av ändring.
- [ ] **SKA** — Verifierat att ingen intern eller känslig information exponeras i programfixen:
  - [ ] Inga interna URL:er, IP-adresser eller systemnamn.
  - [ ] Ingen kund- eller användardata.
  - [ ] Inga interna loggar eller stack traces med känsligt innehåll.

## C. Genomföra programfixen

- [ ] **SKA** — Följer projektets kodstil och konventioner.
- [ ] **SKA** — Använder projektets formatterare och linter-konfiguration.
- [ ] **SKA** — Håller ändringen så liten och fokuserad som möjligt (inga orelaterade refactors).
- [ ] **SKA** — Lägger till eller uppdaterar tester som täcker ändringen.
- [ ] **SKA** — Kör hela testsviten lokalt.
- [ ] **SKA** — Uppdaterar dokumentation eller kommentarer om beteendet ändras.

## D. Förbereda ändringsförfrågan (PR/MR)

- [ ] **SKA** — Synkat med senaste ändringarna i uppströms målbranch.
- [ ] **SKA** — Löst alla merge-konflikter snyggt.
- [ ] **SKA** — Städat commithistoriken (squashat eller ordnat vid behov).
- [ ] **SKA** — Skrivit tydliga commit-meddelanden (imperativ form, referera ärende vid behov).
- [ ] **SKA** — Gett ändringsförfrågan en tydlig, beskrivande titel.
- [ ] **SKA** — Skrivit en beskrivning som inkluderar:
  - [ ] Problembeskrivning (vad är fel eller vad saknas?).
  - [ ] Sammanfattning av lösningen (hur är det fixat?).
  - [ ] Hur man reproducerar före/efter.
  - [ ] Eventuella begränsningar eller bieffekter.
- [ ] **SKA** — Tydligt markerat eventuella breaking changes.
- [ ] **SKA** — Dubbelkollat att det inte finns:
  - [ ] Interna URL:er eller interna systemnamn.
  - [ ] API-nycklar, tokens eller andra hemligheter.
  - [ ] Kunddata eller annan känslig information.
  - [ ] Interna referenser (ärendenummer, loggar) som inte hör hemma publikt.

## E. Under granskning

- [ ] **SKA** — Svarat sakligt och rimligt snabbt på feedback från maintainers.
- [ ] **SKA** — Justerat implementationen enligt feedback (eller förklarat varför inte).
- [ ] **SKA** — Hållit interna intressenter uppdaterade (länkat ändringsförfrågan i intern ticket eller ärende).
- [ ] **SKA** — Noterat om maintainers gör större ändringar i programfixen (för intern uppföljning).

## F. Efter merge eller avslag

- [ ] **SKA** — Noterat vilken uppströms-version som innehåller programfixen.
- [ ] **SKA** — Planerat när beroendet ska uppgraderas internt.
- [ ] **SKA** — Om programfixen behövs före release:
  - [ ] Dokumenterat eventuell tillfällig fork eller intern programfix.
  - [ ] Planerat att ta bort fork eller intern programfix när officiell release finns.
- [ ] **SKA** — Vid avslag:
  - [ ] Dokumenterat motiveringen internt.
  - [ ] Bestämt eventuell intern workaround eller fork om det krävs.

## G. Intern logg

- [ ] **BÖR** — Länk till intern ticket eller ärende.
- [ ] **BÖR** — Länk till uppströms ärende.
- [ ] **BÖR** — Länk till uppströms ändringsförfrågan.
- [ ] **BÖR** — Referens till juridiskt godkännande (för CLA eller specialfall).
- [ ] **BÖR** — Kort sammanfattning: *"Vi bidrog med X till projekt Y, inkluderat i version Z."*

> Checklistan är inspirerad av externa riktlinjer för open source-bidrag (t.ex. TODO Group, GitHub Docs och olika FOSS-policymallar) men är anpassad för intern användning och ska inte ses som juridisk rådgivning.

---

## Källor

- **DIGG: Riktlinje för öppen programvara** (Dnr 2026-02797, beslutad 2026-04-07) — *Hantera bidrag till öppna programvaruprojekt*
- [TODO Group – Open Source Guides](https://todogroup.org/resources/guides/)
- [TODO Group – Policy Examples and Templates](https://github.com/todogroup/policies)
- [GitHub Docs – Contributing to projects](https://docs.github.com/en/get-started/exploring-projects-on-github/contributing-to-a-project)
- [Developer Certificate of Origin (DCO)](https://developercertificate.org/)
- [Open Source Initiative](https://opensource.org/)

För full ramverkslista, se [checklista-standarder.md](checklista-standarder.md).

---

## Se även – alla checklistor

- [Checklista – anskaffning och val av öppen programvara](checklista-anskaffning.md)
- [Checklista – använda öppen programvara](checklista-anvandning.md)
- [Checklista – hantering av ärenden, frågor och externa bidrag](checklista-arenden-community.md)
- [Checklista – bidrag till tredjeparts-OSS](checklista-bidrag-uppstrom.md) ← du är här
- [Checklista – diarieföring och arkivering](checklista-diarie-arkiv.md)
- [Checklista – licensval och licenskompatibilitet](checklista-licenser.md)
- [Checklista – arbete på kodsamverkansplattform](checklista-plattform.md)
- [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md)
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md)
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md)
- [Översikt – standarder och specifikationer](checklista-standarder.md)
