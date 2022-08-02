# Geografiske Referencers programmel-overblik

Af GRF-team Geodætisk Informatik

Ansvarlig for dette arkiv: [Joachim](https:/github.com/xidus)


[kategorier.md](kategorier.md) beskriver Kontoret Geografiske Referencers [GRFs] inddeling af egenudviklede software [programmel] i kategorier med specifikke krav til programmellet i hver kategori. Med inddelingen skaber vi et systematisk **overblik** over eksisterende, aktivt anvendt programmel i kontoret fra forskellige synsvinkler. Overblikket giver os **indsigt** i de enkelte projekters **modenhed**, så vi kan se, hvad der skal gøres, og i hvilket omfang.

Indplaceringen i en kategori afhænger af det forretningsmæssige formål med det enkelte stykke programmel. Hvert projekts programmel hører til en kategori, og den enkelte kategoris krav er derfor krav til dét programmel, som det enkelte projekt leverer.

Formålet med kravene er at sikre, at forretningskritisk programmel som minimum er tilstrækkeligt dokumenteret og testet, samt at afhængigheden til enkeltpersoner er fjernet eller så vidt muligt minimeret.

Vi har som udgangspunkt samlet de tekniske krav i tre kategorier af egenudviklet programmel i GRF.

|     Kategori     |          Python-skabelon          |                                              Formål                                             |
|------------------|-----------------------------------|-------------------------------------------------------------------------------------------------|
| [Prototype][]    | [Skabelon][skabelon-prototype]    | Eksperimenter<br />Kortvarige opgaver, eksempelvis databasemigrering<br />Diverse små-scripts   |
| [Produktion][]   | [Skabelon][skabelon-produktion]   | Software, der aktivt bruges i forretningen, eksempelvis tidsserieanalyser eller andre værktøjer |
| [Distribution][] | [Skabelon][skabelon-distribution] | Software, der har en offentlig snitflade, eksempelvis API eller system til datadistribution     |

[Prototype]: prototype.md
[Produktion]: produktion.md
[Distribution]: distribution.md

[skabelon-prototype]: https://github.com/Kortforsyningen/template-python-prototype
[skabelon-produktion]: https://github.com/Kortforsyningen/template-python-production
[skabelon-distribution]: https://github.com/Kortforsyningen/template-python-distribution

Til hver enkelt kategori er der oprettet et skabelon-arkiv med GitHub Template Repositories, som gør det nemt for nye og eksisterende projekter at starte (forfra) med den basale opsætning, som den enkelte kategori fordrer.

Der er to måder, at anvende GitHub-skabelonerne på og forudsætter, at man er logget på GitHub:

*   Ved at tilgå skabelon-arkivet og trykke på den grønne knap <kbd>Use this template</kbd>.
*   Ved at oprette et nyt arkiv fa bunden og vælge skabelonen fra rullemenuen **Repository template**.


## Governance

Selve styringen af projekterne er indtil videre ikke beskrevet yderligere, men en sådan governance-struktur kan muligvis tænkes indlemmet her i fremtiden.


## Kontakt

Har du spørgsmål til dette arkiv, de tilhørende arkiver eller tilknyttede emner så som styringen af dette arbejde, så kontakt GRF-teamet Geodætisk Informatik.


## Vedligehold

Den centrale og aktive version af dette arkiv bliver vedligeholdt på GitHub.

*   Konkrete ønsker kan oprettes som [GitHub issues](https://github.com/Kortforsyningen/grf-programmel-overblik/issues).

*   Bidrag kan oprettes gennem GitHubs forking- og pull-request-mekanisme:
    -   På kodearkivets side, vælg Fork
    -   Fra din egen fork, lav en by branch og foretag rettelserne i denne.
    -   Når du er klar, kan du oprette et pull-request fra den nye branch.


### Illustrationer

Der indgår en håndfuld illustrationer i arkivets dokumenter.

Der indgår `.png`-billeder med kategori-illustrationer, som kan genskabes ud fra `.svg`-filen i mappen `assets/`.

`.svg`-filen er lavet i InkScape og indeholder derfor også metadata om lag og andet, som kan læses og tilpasses i programmet. Inkscape kan hentes som stand-alone-program, som derfor ikke kræver lokal-administrator-rettigheder at 'installere'.
