# Checklista för bidrag till tredjeparts-OSS

Den här checklistan är tänkt att användas när du som anställd bidrar med patchar till ett
externt open source-bibliotek som vi använder internt.

---

## Innan du skriver någon kod

- [ ] Kollat intern policy: får jag bidra till detta projekt på arbetstid?
- [ ] Fått godkännande från chef / uppdragsansvarig vid behov
- [ ] Identifierat exakt uppströms-repo och versionen vi använder internt
- [ ] Verifierat att projektet har en **OSI-godkänd licens**
- [ ] Verifierat att licensen är kompatibel med hur vi använder biblioteket
- [ ] Vid minsta tvekan kring licensfrågor: kontaktat **juridik/Legal** för go/no-go
- [ ] Kollat om projektet kräver **CLA** (Contributor License Agreement) eller **DCO**
- [ ] Kollat om det redan finns ett företags-/myndighets-CLA på plats
- [ ] Inte signerat någon CLA själv utan först frågat juridik/behörig person
- [ ] Läste igenom projektets `CONTRIBUTING.md` / utvecklingsguide / wiki
- [ ] Förstår deras branch-strategi och målbranch (`main`, `develop`, etc.)
- [ ] Vet hur man kör tester och linters enligt projektets instruktioner

---

## Avgränsa ändringen

- [ ] Sökt efter befintliga issues/PRs för samma bug/feature
- [ ] Undvikit att duplicera pågående arbete (kommenterat eller anslutit till befintlig diskussion)
- [ ] Öppnat en issue eller kommentar som beskriver problemet och föreslagen lösning
- [ ] Försäkrat mig om att maintainerna faktiskt vill ha den här typen av ändring
- [ ] Verifierat att ingen intern eller känslig information exponeras i fixen
  - [ ] Inga interna URL:er, IP-adresser eller systemnamn
  - [ ] Ingen kund- eller användardata
  - [ ] Inga interna loggar eller stack traces med känsligt innehåll

---

## Genomföra patchen

- [ ] Följt projektets kodstil och konventioner
- [ ] Använt projektets formatterare / linter-konfiguration
- [ ] Hållit ändringen så liten och fokuserad som möjligt (inga orelaterade refactors)
- [ ] Lagt till eller uppdaterat tester som täcker ändringen
- [ ] Kört hela testsviten lokalt
- [ ] Uppdaterat dokumentation / kommentarer om beteendet ändrats

---

## Förbereda pull request

- [ ] Synkat med senaste ändringarna i uppströms målbranch
- [ ] Löste alla merge-konflikter på ett snyggt sätt
- [ ] Städade upp commithistoriken (squashat/ordnat vid behov)
- [ ] Skrev tydliga commitmeddelanden (imperativ form, referera issue vid behov)
- [ ] Gav PR:en en tydlig, beskrivande titel

- [ ] Skrev en PR-beskrivning som inkluderar:
  - [ ] Problembeskrivning (vad är fel / vad saknas?)
  - [ ] Sammanfattning av lösningen (hur är det fixat?)
  - [ ] Hur man reproducerar före/efter
  - [ ] Eventuella begränsningar eller bieffekter

- [ ] Tydligt markerat eventuella breaking changes (om sådana finns)

- [ ] Dubbelkollat att det **inte** finns:
  - [ ] Interna URL:er eller interna systemnamn
  - [ ] API-nycklar, tokens eller andra hemligheter
  - [ ] Kunddata eller annan känslig information
  - [ ] Interna referenser (ärendenummer, loggar) som inte hör hemma publikt

---

## Under review

- [ ] Svarat sakligt, trevligt och rimligt snabbt på feedback från maintainers
- [ ] Justerat implementationen enligt feedback (eller förklarat varför inte)
- [ ] Hållit interna intressenter uppdaterade (länkat PR i intern ticket/ärende)
- [ ] Noterat om maintainers gör större ändringar i din patch (för intern uppföljning)

---

## Efter merge eller avslag

- [ ] Noterat vilken uppströms-version som innehåller fixen
- [ ] Planerat när vi ska uppgradera beroendet internt
- [ ] Om vi behöver fixen innan release:
  - [ ] Dokumenterat eventuell tillfällig fork/patch
  - [ ] Planerat att ta bort fork/patch när officiell release med fixen finns

- [ ] Vid avslag:
  - [ ] Dokumenterat motiveringen internt
  - [ ] Bestämt eventuell intern workaround / fork om det krävs

---

## Intern logg (valfritt men rekommenderat)

- [ ] Länk till intern ticket / ärende
- [ ] Länk till uppströms issue
- [ ] Länk till uppströms PR
- [ ] Referens till juridiskt godkännande (för CLA / specialfall)
- [ ] Kort sammanfattning:  
      “Vi bidrog med X till projekt Y, inkluderat i version Z”

---

## Om denna checklista

> Checklistan är inspirerad av externa riktlinjer för open source-bidrag
> (t.ex. TODO Group, GitHub Docs och olika FOSS-policymallar) men är
> anpassad för vår interna användning och ska inte ses som juridisk
> rådgivning.

---

## Se även – alla checklistor

- [Checklista – anskaffning och val av öppen programvara](checklista-anskaffning.md)
- [Checklista – hantering av ärenden, frågor och externa bidrag](checklista-arenden-community.md)
- [Checklista – bidrag till tredjeparts-OSS](checklista-bidrag-uppstrom.md) ← du är här
- [Checklista – diarieföring och arkivering](checklista-diarie-arkiv.md)
- [Checklista – licensval och licenskompatibilitet](checklista-licenser.md)
- [Checklista – arbete på kodsamverkansplattform](checklista-plattform.md)
- [Checklista – förberedelse inför publicering](checklista-publicering-forvaltning.md)
- [Checklista – publicering av version 1.0.0](checklista-publicering-1.0.md)
- [Checklista – säkerhet i öppna programvaruprojekt](checklista-sakerhet.md)
- [Översikt – standarder och specifikationer](checklista-standarder.md)
