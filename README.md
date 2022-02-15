# Geografiske Referencers (GRFs) programmel-overblik

Af GRFs Team Geodætisk IT

Ansvarlig for dette arkiv: [Joachim](https:/github.com/xidus)


Dette arkiv beskriver inddelingen af Kontoret Geografiske Referencers egenudviklede software [programmel] i kategorier med specifikke krav til programmellet i hver kategori. Indplaceringen i en kategori afhænger af det forretningsmæssige formål med det enkelte stykke programmel. Hvert projekts programmel hører til en kategori, og den enkelte kategoris krav er derfor krav til dét programmel, som det enkelte projekt leverer.

Med inddelingen kan man skabe et systematisk overblik over eksisterende, aktivt anvendt programmel i kontoret fra forskellige synsvinkler. Med overblikket får vi indsigt i de enkelte projekters modenhed og kan derfor se, hvad der skal gøres, og i hvilket omfang.


Til hver enkelt kategori er der oprettet et skabelon-arkiv med GitHub Template Repositories, som gør det nemt for nye og eksisterende projekter at starte (forfra) med den basale opsætning, som den enkelte kategori fordrer.

Selve styringen af projekterne er indtil videre ikke beskrevet yderligere, men en sådan governance-struktur kan muligvis tænkes indlemmet her i fremtiden.

Har du spørgsmål til dette arkiv, de tilhørende arkiver eller tilknyttede emner så som styringen af dette arbejde, så kontakt GRF-teamet Geodætisk Informatik.

Den centrale og aktive version af dette arkiv bliver vedligeholdt på GitHub.


## Indledning

Kontorets egenudviklede programmel bør følge fælles retningslinier for bedste praksis i forhold til software-udvikling. Den overordnede vision for ethvert projekt bør være en tilstand, hvor programmel og dokumentation heraf er fremtidsikret. Når det er fremtidssikret, vil det eksempelvis til alle tider vil være muligt for nye personer på et givet projekt at komme nemt igang og fortsætte, hvor andre slap. Generelt set, vil der være strukturer på plads, som sikrer, at det pågældende programmel kan bruges i fremtiden uden adgang til andet end koden, dokumentation samt historik heraf.

God praksis kan og bør belyses fra flere synsvinkler. Der vil altid være tekniske krav, som eksempelvis kræver overvejelser om software-arkitektur, teknisk infrastruktur eller programmeringskonventioner. Fra den formelle synsvinkel har vi krav til, at et givet projekt er veldokumenteret, at kode og dokumentation har den rigtige licens, at de enkelte dele af projektet er tilgængelige for dem, der skal kunne tilgå dem.


Kategorierne har gradvis flere krav til til det udviklede programmel. Når et stykke programmel bliver placeret i en kategori, stiller vi samtidig specifikke krav til, hvad der skal indgå i projektet. Vi kan spørge os selv, hvor modent et projekts programmel er, ved at se på, hvor mange af kravene inden for kategorien, der er opfyldt.

Indplaceringen sætter altså et mål for, hvornår et projekts programmel er modent nok til fortsat udvikling eller færdigt. Når et projekts programmel opfylder alle kravene i kategorien, vil vi sige, at det er tilpas fremtidssikret i ovennævnte forstand.

Kategori-inddelingen forudsætter, at det pågældende programmel har et værdiskabende formål for forretningen. Det er med andre ord en antagelse, at det pågældende programmel bør eksistere.

Inddelingen er altså fastsat ud fra den nuværende, eksisterende programmel-portefølje, og kravene er valgt ud fra generel bedste praksis i resten af industrien. Kravene i hver kategori kan derfor ændre sig afhængigt af både vores egne behov, men også som en naturlig del af den teknologiske og styringsmæssige tendens, vi ser omkring os. Derfor er dette dokument nødvendigvis også en midlertidig rettesnor, som i sig selv skal fremtidssikres efter bedste praksis.


Nedenfor kommer et kort overblik over de enklte kategorier med links til skabeloner. Dette efterfølges af et afsnit for hver skabelons, hvor de enkelte krav til leverancen beskrives.

Kravene i den mindst krævende kategori **Prototype** er indeholdt i den efterfølgende kategori **Produktion** og denne kategoris krav er igen inkluderet i den sidste kategori **Distribution**. Derfor vil en opfyldelse af alle krav i kategorien **Produktion** medføre, at man opfylder alle krav stillet til programmel i kategorien **Prototype**. På samme måde vil en imødekommelse af alle krav til programmel i kategorien **Distribution** samtidig betyde, at man opfylder alle krav i de to underliggende kategorier **Produktion** og **Prototype**. Det illustreres i følgende figur, der samtidig viser, at der er (uendelige) krav uden for de tre inddelinger, vi har valgt til vores formål lige nu.

<div style="text-align: center">
  <img title="Illustration af kategoriernes overlappende krav" src="./assets/kategorikrav.png" width="50%" />
</div>


## Krav og kategorier

Kravene skal som minimum sikre, at forretningskritisk programmel er tilstrækkeligt dokumenteret og testet, samt at afhængigheden til enkeltpersoner er fjernet eller så vidt muligt minimeret.

Inddelingen i kategorier er til for at skabe en klar ramme for forventningerne til et givet projekts leverance. Kategorierne har forskellige krav afhængig af deres kritikalitet (formål) for forretningen.

Vi har som udgangspunkt samlet de tekniske krav i tre kategorier af egenudviklet programmel i GRF.

|                                                           Kategori                                                           |                               Python-skabelon                               |                                         Formål                                        |
|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <img title="Illustration af kategorien Prototype" src="./assets/kategorikrav-prototype.png" height="20px" /> Prototype       | [skabelon](https://github.com/Kortforsyningen/template-python-prototype)    | Eksperimenter<br />Transient opgaver, fx databasemigrering<br />Diverse småscripts   |
| <img title="Illustration af kategorien Produktion" src="./assets/kategorikrav-produktion.png" height="20px" /> Produktion     | [skabelon](https://github.com/Kortforsyningen/template-python-production)   | Software der aktivt bruges i forretningen, fx tidsserieanalyser eller andre værktøjer |
| <img title="Illustration af kategorien Distribution" src="./assets/kategorikrav-distribution.png" height="20px" /> Distribution | [skabelon](https://github.com/Kortforsyningen/template-python-distribution) | Software der har en offentlig snitflade, fx API eller system til datadistribution     |


### Om brugen af skabelonerne

Der er to måder, at anvende GitHub-skabelonerne på og forudsætter, at man er logget på GitHub:

*   Ved at tilgå skabelon-arkivet og trykke på den grønne knap <kbd>Use this template</kbd>.
*   Ved at oprette et nyt arkiv fa bunden og vælge skabelonen fra rullemenuen **Repository template**.



### Krav-overblik

De enkelte kategorier dækker følgende krav:


|                       Krav                      | Prototype | Produktion | Distribution |
|-------------------------------------------------|-----------|------------|--------------|
| API-dokumentation                               |           |            | x            |
| Continuous Delivery/Deployment (CD)             |           |            | x            |
| Systemafhængigheder                             |           |            | x            |
| Teknisk dokumentation                           |           | x          | x            |
| Versionering (semantisk)                        |           | x          | x            |
| Vedligeholdelsesgren(e) (maintainance branches) |           | x          | x            |
| Continuous Integration (CI)                     |           | x          | x            |
| Test suite                                      |           | x          | x            |
| `.gitignore`                                    | x         | x          | x            |
| Brugervejledning                                | x         | x          | x            |
| Installationsvejledning                         | x         | x          | x            |
| Konfigurationsfiler                             | x         | x          | x            |
| `README.md`                                     | x         | x          | x            |
| Licens (`LICENSE.md`)                           | x         | x          | x            |
| Git-arkiv på GitHub                             | x         | x          | x            |


Fælles for alle arkiverne er, at der overordnet er mindst to modtagere af leverancen: udviklere (herunder de oprindelige forfattere), og brugere (kollegaen, den interne partner, 'kunden'). Modtagerne adskiller sig primært ved deres forskellige formål med at tilgå arkivets indhold, og i forlængelse heraf som regel også i deres evner til at forstå, hvordan arkivet skal bruges. (Domænespecialister hører dog ofte til i begge modtager-grupper.)

Brugeren skal bruge produktet, som arkivet indeholder eller leverer. For brugeren er arkivet ofte adgangen til at komme i besiddelse af produktet, installere det og bruge det. Vejledninger og programmel-pakker er derfor noget, brugeren vil kigge efter, når de tilgår arkivet. De er der først og fremmest for at kunne løse deres egne opgaver i forretningen bedre. For dem er programmellet bare en ekstra kommando eller grafisk brugergrænseflade, som helst skal være let at anvende.

Udvikleren skal kende til forretningen og brugerens behov og har til formål at bringe sit kendskab til værktøjer og software-principper sammen med de muligheder og begrænsninger, som findes i den eksisterende IT-infrastruktur i forretningen, sammen for at opfylde disse behov.

<!-- *** -->

Slutprodukterne i arkivet har altså forskellige formål, som gør dem relevante på forskellige tidspunkter til forskellige modtagergrupper.

De værktøjer, man bruger til at bygge og videreudvikle koden, skal helst være de samme. Git-arkivet har derfor filer, der er relevante for én, der skal tilføje funktionalitet. Alt hvad der skal til for at kunne bygge (videre på) eller vedligeholde projektet er udviklervendte.

Bruger-modtagergruppen er derimod alt fra hovedmodtageren---dén, der bestilte leverancen---eller andre udviklere, der skal bruge programmellets funktionalitet i deres egne projekter, enten via programmelets API eller som applikation, hvis dette er formålet med programmellet.

Der kan være mange formål med programmellet ud over de nævnte, men med kravene inden for disse kategorier, er det primære formål at vi har materiale i et arkiv, som gør det muligt at levere det forventede, uden kendskab til andet end indholdet i arkivet. Alt, hvad der opfylder dette formål vil generelt være et rimeligt fremtidssikret projekt.


### Kravenes gyldighed fra projektbegyndelse til første/primære leverance

Det er i orden, at ikke alt er med fra starten, men det skal være tilfældet, at man kan komme videre og bidrage til projektet fra dét stadium, det er i til et givet tidspunkt.

Det er ikke formålet her at fortælle, hvad der skal laves i hvilken rækkefølge. Det vil altid være kontekstafhængigt. Men hvor rækkefølgen til dels er ligemeget, så skal der som minimum være noget, man kan starte ud fra, som bruger eller udvikler, når man tilgår arkivet.



## Kategori: Prototype

<div style="text-align: center">
  <img title="Illustration af kategorien Prototype" src="./assets/kategorikrav-prototype.png" width="50%" />
</div>

Som nævnt ovenfor, er eksempler på programmel i kategorien Prototype blandt andet eksperimenter---herunder prototyper---, midlertidige opgaver og diverse små-scripts.



### Versionsstyring

*   Alle filer relateret til koden (herunder test-kode, dokumentation, konfigurationsfiler og andet) er samlet og versionsstyret for at sikre, at filerne hænger sammen med hinanden på tværs af arkiv-versionerne.

> Bemærk, at der er forskel på en given version af arkivets indhold (i Git er det en SHA1-hash, der udgør et bidrags [*et* commit] version) og den semantiske version af dét stykke programmel, der ligger i arkivet (eksempelvis version `1.2.3` for en pakke). Versionering af kodeudgivelser er ikke et krav i denne kategori, men se mere om dette [under Produktion](#Produktion) nedenfor.


**Git-arkivet**

Et Git-arkiv har altid en `.git`-mappe som indeholder versionshistorikken. Ud over denne, er der andre muligheder for at konfigurere versionsstyringen:

*   `.gitignore`-filen er vigtig af praktiske og sikkerhedsmæssige grunde.
    -   Arbejdet med koden og andre kildefiler producerer typisk en række sideprodukter så som Python-bytekode, test-cache-filer og andet, som altid kan produceres igen ud fra kildekoden. Filer som disse er derfor ikke nødvendige at versionsstyre.
    -   Andre filer kan være udviklerens egne konfigurationsfiler, som ikke bare er irrelevante, men også kan være sikekrhedsmæssigt uforsvarlige at komme til at knytte til arkivet: det kan være konfiurationsfiler med login-oplysninger.

*   `.gitattributes`
    -   Det kan være nødvendigt at definere nogle særlige atributter for nogle filtyper, så man kan lade Git håndtere dem éns på tværs af arkivets bidragydere. Det kan være markering af særlige filtyper som binære. Eller det kan være énsretning af linieskift-karakterer på tværs af operativsystemer.

> **Bemærk**
> 
> *   Din lokale og personlige `.gitconfig`-fil bør sættes op, inden du laver ændringer.


**Git-arkiv på GitHub**

GitHub er en Microsoft-ejet, online platform, som fungerer som en central placering af vores Git-arkiver. Platformen yder flere ekstra ting, som gør det lettere at administrere de enkelte arkiver, herunder at sammenflette versioner, der kommer fra de enkelte bidragsydere til arkiverne.

*   Git-arkivets centrale version skal indtil videre ligge på GitHub.
*   **Start med at lave arkivet privat.**


### Programmel-kildekode

Programmel-koden udgør programmellets egentlige funktionalitet. Programellets funktionalitet er forskellig fra alle de filer, mekanismer og andet i arkivet, som bruges til at arbejde med koden [installationsprogrammer, konfigurationsfiler, etc.]. Derfor placeres programel-koden  i en separat mappe adskilt fra andet, der ikke er nødvendigt, når programmellet er installeret.

Mere konkret: er programmellet en samling forbundne scripts og moduler, så læg dem i en mappe i arkivets rod kaldet `scripts`. Er det en Python-pakke, så læg pakken i en mappe med navnet `src`.


### Konfigurationsfiler

Konfigurationsfiler kan dække flere formål:

*   Miljø-opsætning for udviklere eller brugere af koden.
    -   Eksempel: `environment.yml` til styring og installation af virtuelle Python miljøer med Mamba Forge-Python-distributionen.
    -   Eksempel: Indstillinger, der er nødvendige for, at koden kan udføre sine opgaver, eksempel login-oplysninger til en database eller andet. Da disse filer kan indeholde følsomme oplysninger, vil indstillingerne typisk være specielt-navngivne filer, der indikerer, at de er eksempler på en opsætning, man som bruger eller udvikler kan have.


### Dokumentation

**README-fil**

I roden af arkivet skal der være en README-fil [kald den `README.md`, og lad være med at oversætte den til dansk]. Dokumentet skal derfor indeholde oplysninger om projektet, vejledninger, hjælp til at installere og komme igang, samt kontaktoplysninger på de aktive vedligeholdere af projektet.

På GitHub er dette dokument den første og dermed vigtigste indgang til projektet, da filen automatisk bliver vist, når man tilgår arkivet. Sørg derfor for som minimum at have en README-fil, og lad den have et basalt indhold.

Inspiration til indholdet af README-filen kan eventuelt hentes i følgende [README-checkliste](https://github.com/ddbeck/readme-checklist/blob/main/checklist.md) ([tilhørende foredrag](https://www.youtube.com/watch?v=2dAK42B7qtw)).


**Licens**

Licensen er en juridisk vejledning i, hvordan man må bruge programellet, samt hvilke rettigheder, man har som bruger af det.

*   Arkivet indeholder en beskrivelse af licens-betingelserne.
*   Anvend konventionen med en fil `LICENSE` i roden af git-arkivet.
    -   [Eksempel](https://github.com/Kortforsyningen/template-python-prototype/blob/main/LICENSE)


**Brugervejledning**

*   Med tanke på modtagerne, skal der være en vejledning til brugeren, der skal anvende programmellet.

*   Brugeren skal vide, hvilket problem programmellet løser, og hvilken værdi det skaber. Dette kan være givet, men det er godt at have med.

*   Så skal brugeren vide, hvordan man kommer igang med at bruge programmellet.

*   Og så er det vigtigt, at brugeren bliver informeret om, hvorhen eller til hvem de kan gå for at få hjælp eller bidrage med feedback.
    -   Brugere (og udviklere) skal vide, hvordan man opretter sager, hvis man oplever fejl i programmellet eller har ændringsønsker. Samtidig lægger vi med al koden på GitHub op til, at man anvender platformen til at bidrage med ændringer, hvis man selv er i stand til at bidrage til projektet, om det så er kode eller dokumentation eller noget tredje.


**Installationsvejledning**

*   Med tanke på modtagerne, skal der være relevante installationsvejledninger, som er relevante i forbindelse med udvikling og brug af programmellet.

*   Udviklere skal vide, hvad de skal installere for at kunne bygge videre på kode og dokumentation, herunder lokal testopsætning i deres egne miljøer.
    -   Man behøver ikke nødvendigvis en vejledning installation af teamets gængse værktøjer. Men tænkt i relevans her og overvej, igen, om en ny udvikler/kollega kan klare sig selv uden den konkrete vejledning.

*   Brugeren skal i arkivet kunne læse sig til, hvordan programmellet installeres, så det kan tages i brug som et færdigt produkt.


**Vedligeholdesvejledning**

Som en del af fremtidssikringen, skal der i denne kategori som minimum være en beskrivelse af, hvordan projektet fortsat kan vedligeholdes til fremtidigt brug.

Her bør man formulere alle relevante oplysninger, som er nødvendige for, at man kan arbejde videre med koden fremover.Ud over de andre vejledninger, kan der her være behov for at nævne andre kontaktpersoner eller samarbejdspartnere.

Man kan også vælge at tilføje denne vejledning en beskrivelse af processen med at modtage og håndtere input fra brugere af programmellet.



## Kategori: Produktion

<div style="text-align: center">
  <img title="Illustration af kategorien Produktion" src="./assets/kategorikrav-produktion.png" width="50%" />
</div>

Som nævnt indeholder kategorien Produktion software, der aktivt bruges i forretningen.

Ud over kravene under kategorien Prototype, skal følgende også være i med i leverancen.

Her er altså tale om mere længerevarende projekter, der dermed også kræver mere omtanke og fokus på vedligehold. Længerevarende kode-udvikling medfører som regel også flere implementeringer---*ikke* nødvendigvis mere kode. Her er også tale om noget, der i lang tid skal understøtte forretnignens behov på et niveau, der i høj grad understøtter kvaliteten af dét arbejde, der udføres af det udviklede programmel.

Derfor er der behov for flere udviklervendte værktøjer, som hjælper udvikleren med at sikre kvaliteten af koden, både designmæssigt, men også funktionsmæssigt.

Med yderligere dokumentation, hjælper man også andre udviklere på projektet til at bibeholde vedtagne standarder og konventioner, så vel som at give det fulde overblik over alt, hvad der er med i arkivet.


### Udviklervendte værktøjer

De udviklervendte værktøjer har til formål at instruere andre, der skal bidrage til og vedligeholde arkivets indhold, herunder kildekode, test-kode og dokumentation.


**Test-funktionalitet (test suite)**

Der skal så vidt muligt være test-funktionalitet---afsondret fra programmellets kode---af alle funktioner i koden.

En test-suite er en organiseret samling af kode, der tester funktionaliteten af koden set fra en brugers synsvinkel.

Test-opsætningen kan være mere eller mindre kompliceret, fra manuel kørsel af test-funktionaliteten til opsætninger, der kan sætte test-miljøer op, der svarer til de miljøer, hvori programmet kan forventes af skulle kunne køre.


**Continuous Integration [CI]**

Når ændringer skubbes til den centrale placering [GitHub] af arkivet, skal koden automatisk hentes og relevant test-funktionalitet afvikles.

Opsætningen bruges til at lade udvikleren vide, om koden virker som forventet ved kilden og ikke bare i udviklerens eget miljø. Dette kaldes continuous integration eller CI.

GitHub har et integreret CI-værktøj kaldet GitHub Actions. Actions kan køre, når en bruger laver ændringer i arkivet eller på fastlagte tidspunkter. Når betingelserne er opfyldt, starter platformen et bruger-defineret workflow op på en virtuel maskine på platformens servere.

Man kan tilføje workflows gennem platformens web-brugergrænseflade, hvorved GitHub opretter følgende mappestruktur i roden af arkivet: `.github/workflows/`. `workflows`-mappen indeholder så de workflows, man har oprettet. Workflows er bare `.yaml`-dokumenter med en bestemt struktur og indhold. Man kan således oprette workflows bare ved at tilføje workflow-filer i denne mappe, og GitHub vil selv opfange dem og køre dem efter foreskrifterne i hver enkelt workflow-fil.


**Teknisk dokumentation**

Teknisk dokumentation er en bred betegnelse for en række forskellige ting, som primært er henvendt til udviklere, men også til drifts-ansvarlige, eller folk, der har brug for at vide, hvordan programmellet indgår i et større systemlandskab.

Der kan også være behov for at beskrive programmellet arkitektur i sig selv, snitflader mod andre systemer; begrundelser herfor og tegninger/illustrationer heraf.

Det nødvendige detalje-niveau afhænger til dels af formålet med leverancen. Det er dog nødvendigt at medtage så meget af det som muligt, i større eller mindre omfang, så vi får en fast ramme, hvorunder vi beskriver tingene.


**Versionering (semantisk)**

Kodeudgivelserne er styret og bruger semantisk versionering som konvention for programmel-udgivelsernes nummerering.


**Vedligeholdelsesgren(e) (maintainance branches)**

Der skal være en vedligeholdesgren i git-arkivet, som indeholder seneste minor version, og som modtager rettelser fra den løbende udvikling.

<span style="background: #ff0">UDDYB</span>


## Kategori: Distribution

<div style="text-align: center">
  <img title="Illustration af kategorien Distribution" src="./assets/kategorikrav-distribution.png" width="50%" />
</div>

Sammen kravene til kategorierne **Prototype** og **Produktion** skal nedenstående være opfyldt for programmel kategoriseret som **Distribution**.

I denne kategori hører software, der har en offentlig snitflade og dermed brugere uden for vores organisation, som er afhængige af ikke bare kvalitet, men også tilgængelighed og driftsikkerhed.


**Systemafhængigheder**

Systemafhængigheder er alt, hvad det pågældende programmel er afhængigt af for at virke, og kan blandt andet bestå af følgende:

*   Forud-installerede programmer, der ikke kommer med programmellet, herunder eksempelvis en Python-distribution til at køre Python-kode.

*   Styresystemer, programmellet kan køre på.

*   Brugerens egne adgange til netværksressourcer som netværksdrev, servere (lokale som eksterne) og Internettet.

*   Separat fra adgange til netværk er systemadgange, der kræver (eksplicitte) login-oplysninger for specifikke brugerkonti, som anvendes af programmet.


Både bruger og udvikler skal få et overblik over afhængigheder som disse, når de tilgår dokumentationen i arkivet. Derfor:

*   Brug gerne diagrammer til illustration af teknisk infrastruktur, databaser og andet, hvor forbindelserne mellem komponenterne kan blive klarere derved.

*   Brug gerne tabeller til konkrete informationer som servernavne/adresser og andet, hvor prosatekst eller punktlister ikke rigtig gør det nemt nok at læse og få overblik over informationerne.

*   Overvej generelt, hvordan informationerne bedst kan præsenteres, så de skaber en klar forståelse af indholdet for læseren.



**Continuous Delivery/Deployment (CD)**

Continuous deployment og continuous delivery [begge forkortet CD] henviser til to processer, der begge kan være en del af éns Continuous-Integration [CI] pipeline:

*   Continous deployment er den automatiske produktion og versionering af pakker baseret på de enkelte commits, der kommer igennem éns krav (kvalitetssikring så som fejlfri testkørsel) i CI-opsætningen. Det betyder, at der for hver arkiv-version, som virker, bliver produktet gjort *klar* til brug.

*   Continuous delivery er den automatiske ibrugtagning af nye programmel-versioner, når de bliver tilgængelige på måden beskrevet under continuous deployment.

Som indikeret er continuous deployment og continuous delivery som regel processer, der sættes op i éns continuous-integration pipeline, som i denne sammenhæng er én eller flere workflow-filer, der kan læses af GitHub Actions.

<span style="background: #f60">Her er det også relevant at nævne at vi på DADs servere deployer vha Jenkins. Fx Valdemar-applikationen der deployes automatisk på test-server og trigges manuelt til deploy på produktionen. WEBPROJ har et tilsvarende setup.</span>

**API-dokumentation**

Programmel kan anvendes af anden kode eller andre systemer på flere måder. Snitfladen til programmellets funktionalitet fra eksterne programmer kaldes for Application Programming Interface [API]. Følgende scenarier er eksempler på API'er:

1.  Et programellet et bibliotek, der kan bruges som tredjepartsmodul i andre sammenhænge, vil API her henvise til dén del af bibliotekets funktionalitet, som har til formål at eksponere funktionaliteten til brugeren.

2.  Programmel, der som selvstændigt programmet [*en* applikation] udstiller eksempelvis en service, når programmet kører, har dermed også en API, som kan tilgås på flere forskellige måder og ikke nødvendigvis med programmel skrevet i samme programmeringssprog som programmet selv.

Der skal være dokumentation af programmellets API med i resten af dokumentationen.

Tilgange til API-dokumentation kan være følgende:

*   Automatisk produktion af dokumentation ud fra signaturer og docstrings i Python-kildekoden.

*   Automatisk produktion og udstilling af konsumérbar API-dokumentation ud fra samme. Konsumérbar vil her sige, at der kan produceres en service med en interface, der i sig selv er en udstilling, hvor det udstillede er noget, der definerer API'en for programmellets service.


---

## Bidrag til dette arkiv

*   Konkrete ønsker kan oprettes som [GitHub issues](https://github.com/Kortforsyningen/grf-programmel-overblik/issues).

*   Bidrag kan oprettes gennem GitHubs forking- og pull-request-mekanisme:
    -   På kodearkivets side, vælg Fork
    -   Fra din egen fork, lav en by branch og foretag rettelserne i denne.
    -   Når du er klar, kan du oprette et pull-request fra den nye branch.

## Vedligeholdesvejledning

### Illustrationer

Der indgår en håndfuld illustrationer i arkivets dokumenter.

Til `README.md` indgår `.png`-billeder, som kan genskabes ud fra `.svg`-filen i mappen `assets/`.

`.svg`-filen er lavet i InkScape og indeholder derfor også metadata om lag og andet, som kan læses og tilpasses i programmet. Inkscape kan hentes som stand-alone-program, som derfor ikke kræver lokal-administrator-rettigheder at 'installere'.
