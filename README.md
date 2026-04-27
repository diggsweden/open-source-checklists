# Checklistor för öppen programvara

Krav, rekommendationer och stöd för arbete med öppen programvara — från anskaffning till publicering, förvaltning och avveckling.

> **Status:** Utkast. Innehållet är arbetsmaterial och kan komma att ändras.

Bygger på **DIGG:s policy och riktlinje för öppen programvara** (Dnr 2026-02796 / 2026-02797, beslutade 2026-04-07), [OpenSSF OSPS Baseline][osps], [Standard for Public Code][sfpc] och svensk lagstiftning kring offentlig verksamhet. För källöversikt, se [docs/checklista-standarder.md](docs/checklista-standarder.md).

## Hitta rätt checklista för din roll

| Du är …                       | Börja här                                              |
|------------------------------|--------------------------------------------------------|
| Slutanvändare av OSS          | [Använda öppen programvara](docs/checklista-anvandning.md) |
| Beställare / upphandlare      | [Anskaffning](docs/checklista-anskaffning.md) |
| Projektledare                 | [Anskaffning §E](docs/checklista-anskaffning.md#e-dokumentation-av-beslut) + [Förvaltning §A](docs/checklista-publicering-forvaltning.md#a-beslut-ansvar-och-förvaltare) + [Diarieföring](docs/checklista-diarie-arkiv.md) |
| Systemägare / chef            | [Anskaffning §E](docs/checklista-anskaffning.md#e-dokumentation-av-beslut) + [Diarieföring](docs/checklista-diarie-arkiv.md) |
| Arkitekt                      | [Anskaffning §B](docs/checklista-anskaffning.md#b-val-av-projektlösning) + [Säkerhet §B](docs/checklista-sakerhet.md#b-beroenden-och-komponenter) + [Plattform](docs/checklista-plattform.md) |
| Utvecklare som vill publicera | [Förbereda publicering](docs/checklista-publicering-forvaltning.md) → [Publicera 1.0](docs/checklista-publicering-1.0.md) |
| Utvecklare som bidrar uppström| [Bidra till tredjeparts-OSS](docs/checklista-bidrag-uppstrom.md) |
| Maintainer / förvaltare       | [Förvaltning](docs/checklista-publicering-forvaltning.md) + [Ärenden och community](docs/checklista-arenden-community.md) |
| Säkerhetsansvarig             | [Säkerhet](docs/checklista-sakerhet.md) |
| OSPO / juridik                | [Licenser](docs/checklista-licenser.md) + [Säkerhet](docs/checklista-sakerhet.md) |
| Registrator / arkivarie       | [Diarieföring och arkivering](docs/checklista-diarie-arkiv.md) |

## Alla checklistor

- [Anskaffning och val av öppen programvara](docs/checklista-anskaffning.md)
- [Använda öppen programvara (slutanvändarperspektiv)](docs/checklista-anvandning.md)
- [Bidrag till tredjeparts-OSS](docs/checklista-bidrag-uppstrom.md)
- [Diarieföring och arkivering](docs/checklista-diarie-arkiv.md)
- [Hantering av ärenden, frågor och externa bidrag](docs/checklista-arenden-community.md)
- [Licensval och licenskompatibilitet](docs/checklista-licenser.md)
- [Arbete på kodsamverkansplattform](docs/checklista-plattform.md)
- [Förberedelse inför publicering](docs/checklista-publicering-forvaltning.md)
- [Publicering av version 1.0.0](docs/checklista-publicering-1.0.md)
- [Säkerhet i öppna programvaruprojekt](docs/checklista-sakerhet.md)
- [Översikt – standarder och specifikationer](docs/checklista-standarder.md)

## Implementeringsmall

För konkret startkod med alla krav-filer förkonfigurerade:
[diggsweden/open-source-project-template](https://github.com/diggsweden/open-source-project-template).

## Stilkonvention

Checklistorna använder följande markörer:

- **SKA** — krav (motsvarar MUST i RFC 2119).
- **BÖR** — rekommendation (SHOULD).
- *Källa: …* — visar vilken DIGG-paragraf, OSPS Baseline-kontroll eller Standard for Public Code-kriterium som ligger bakom punkten.

## Bidra

Förslag och rättelser tas tacksamt emot via ärenden och ändringsförfrågningar.

[osps]: https://baseline.openssf.org/
[sfpc]: https://standard.publiccode.net/
