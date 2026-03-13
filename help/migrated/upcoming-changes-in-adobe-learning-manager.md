---
title: Nieuwe functies in de Adobe Learning Manager-versie van april 2026
description: Meer informatie over de nieuwe functies, verbeteringen en belangrijke updates in de Adobe Learning Manager-versie van april 2026.
exl-id: 4d2129c4-42d8-446f-8837-879b5c2f42bf
source-git-commit: 1cbdd4ca217ecc760e942e99303ca7841a20c5b6
workflow-type: tm+mt
source-wordcount: '20211'
ht-degree: 0%

---

# Updates in Adobe Learning Manager

>[!IMPORTANT]
>
>De functies in deze release zijn beschikbaar in bèta. Functionaliteit en gedrag kunnen vóór algemene beschikbaarheid veranderen. Deel feedback via je gebruikelijke kanalen voor ondersteuning van Adoben.


Dit document geeft een overzicht van de nieuwe functies, verbeteringen en updates in de Adobe Learning Manager-versie van april 2026. Gebruik dit om wijzigingen voor uw organisatie te plannen en te begrijpen wat er beschikbaar is voor studenten, beheerders en auteurs.

**voor studenten:** De Fluidic Player toont nu de volgende modulenaam en een duidelijke knoop van de Uitgang. De Player-taal kan via LTI worden ingesteld voor een consistente ervaring op alle platforms. De inhoud van een Captivate bevat een uniforme inhoudsopgave, afsluitingstekens op dianiveau en een betrouwbare exporteerfunctie voor notities. Er is ondersteuning voor meerdere talen beschikbaar voor taakhulpen, vragen over checklist en videoteksttracks (VTT). Met de AI-assistent krijgen studenten antwoorden binnen de leerervaring.

**voor beheerders en auteurs:** De schakelaar van het Gezoem steunt veelvoudige gezamenlijke VILT zittingen. Gedeelde cursussen in collega-accounts geven de echte auteur weer in plaats van &quot;Externe auteur&quot;. Beheerders kunnen het starten van modules beperken. Vervaldatums van leerobjecten worden weergegeven in de API&#39;s voor studenten. De controlelijstmodules bieden ondersteuning voor gewogen scores, meertalige vraagtekst en optionele revisieopmerkingen. Aangepaste certificaten bieden een editor voor slepen en neerzetten met dynamische velden en door AI gegenereerde achtergronden. Met de niet-aangemelde Experience Builder kunt u leerpagina&#39;s voor het publiek maken zonder dat u zich hoeft aan te melden.

**voor instructeurs:** produceer QR codes voor instantienrollment en zittingsaanwezigheid. Opmerkingen of feedback toevoegen tijdens evaluatie van checklist.

**het Melden en de analyse:** de inhoud SCORM kan veelvoudige quizpogingen in L2 nu melden rapporterend. De berekening van de bestede leertijd wordt verbeterd in Studenttranscripten. Leertranscriptrapporten voor beheerders worden bijgewerkt. Er zijn geavanceerde zoekverbeteringen beschikbaar.

## Navigatie voor Fluidic Player: de naam van de volgende module weergeven

### Overzicht

Deze verbetering is al opgenomen in de november 2025-versie van Adobe Learning Manager.

De actie &quot;Volgende&quot; in de speler geeft aan wat er gebeurt wanneer erop wordt geklikt door de naam van de volgende module of cursus weer te geven en door expliciet te signaleren wanneer de student op het punt staat de speler af te sluiten.

### Nieuwe functies

**label &quot;Next Module: {ModuleName}&quot; in de speler**

Het volgende pictogram in de Fluidic Player toont nu de naam van de volgende module in de cursus. Bijvoorbeeld Volgende module: Les 2 - Aan de slag.

Dit is van toepassing wanneer de student in dezelfde cursus van de ene module naar de andere overschakelt.

**Duidelijke uitgangsactie op de laatste module**

Wanneer de student zich in de laatste module van een cursus bevindt, verschijnt er een knop Handeling afsluiten om aan te geven dat de speler wordt gesloten wanneer deze erop klikt en naar de cursuscontext terugkeert.

**Responsief gedrag voor mobiele en PDF-inhoud**

In kleinere viewports (bijvoorbeeld ~320 px breedte) kan het label Volgende worden ingekort of verborgen, waarbij alleen het pictogram wordt weergegeven, om overlapping met de PDF-besturingselementen te voorkomen.

Voor PDF-modules past de speler besturingselementen aan op een aparte regel, zodat navigatielabels en PDF-besturingselementen elkaar niet beïnvloeden.

**Bijgewerkte Admin > Branding > de voorproef van de Speler**

De voorvertoning van de speler in Beheer > Branding geeft nu het nieuwe label weer, bijvoorbeeld Next Module: Les 2. Zo kunnen beheerders het bijgewerkte navigatiegedrag zien.

### Belangrijkste voordelen

**de duidelijkere navigatie voor studenten**

Studenten hoeven niet meer te raden wat er gebeurt als ze &quot;Volgende&quot; selecteren. Het label geeft duidelijk aan wat er hierna komt, of het nu een module of een cursus is. Deze vermindering van dubbelzinnigheid helpt aarzeling en verwarring te verminderen, met name bij grote doelgroepen in de klanteneducatie waar veel studenten wellicht niet vertrouwd zijn met LMS-interfaces.

**hogere cursus-voltooiing tarieven**

Het duidelijk aangeven van de volgende stap (Volgende module: {ModuleName}) en het toevoegen van een duidelijke actie Afsluiten voor de uiteindelijke module vermindert de kans dat studenten de cursus verlaten of de laatste voltooiingsstap negeren.

**voorspelbaardere gebruikerservaring over apparaten**

De bijgewerkte labels worden uitgelijnd op het gedrag Volgende of Vorige en de pictogrammen op desktops, tablets en mobiele apparaten. Layoutbeperkingen worden gerespecteerd op alle apparaten en PDF-flows, zodat de besturingselementen bruikbaar en toegankelijk blijven.

Dit is met name belangrijk voor headless implementaties, waarbij de Fluidic Player is ingesloten in een aangepaste leerervaring.

### Gebruiksscenario&#39;s

**de portals van het de onderwijspas van de Klant en van de partner (headless of AEM-geïntegreerd)**

Accounts gebruiken Adobe Learning Manager in een volledig headless setup, waardoor studenten worden geleid van externe marketingkanalen. Deze studenten:

* Gebruik vaak video-inhoud in lange reeksen.

* Verwacht een ervaring in de vorm van een studieprogramma waarbij het systeem duidelijk de volgende aflevering of module aangeeft.

In deze milieu&#39;s, **Volgende Module:{ModuleName}** etiket:

* Versterkt de geleide aard van de reis.

* Minimaliseert drop-off tussen modules.

**de cursussen van de Naleving en van de certificatie met bevolen modules**

In gereguleerde of nalevingszware scenario&#39;s:

* Studenten moeten een strikte reeks modules voltooien.

* Auteurs schakelen de inhoudsopgave vaak uit om overslaan te voorkomen.

Hier ziet u de **volgende module:{ModuleName}**

* Bevestigt studenten dat zij de juiste volgorde volgen.

* Maakt het minder waarschijnlijk dat ze de volgende actie verkeerd interpreteren en vroegtijdig afsluiten.

**het Leren Wegen waar de cursussen elkaar volgen**

Waar leerpaden of equivalenten meerdere cursussen koppelen. Dit is handig wanneer u reeksen maakt die in het studieprogramma staan voor grote doelgroepen.

**mobiel-eerste consumptie**

Voor studenten die voornamelijk telefoons of tablets gebruiken:

* Door bijgewerkte labels en responsief gedrag blijft de navigatie begrijpelijk zonder dat je afhankelijk bent van kleine, gesloten pictogrammen of verborgen besturingselementen.

* Dit is belangrijk voor de voorlichting van klanten, het geven van assistenten of vooraf gedefinieerde studenten die in korte sessies op mobiele apparaten toegang hebben tot inhoud.

## Zoomconnector - meerdere gelijktijdige zoomsessies maken

### Overzicht

De Zoom Connector-upgrade verbetert hoe Adobe Learning Manager Virtual Instructor-Led Training (VILT) beheert. Voorheen konden gebruikers slechts één zoomsessie tegelijk maken. Met de nieuwe update kunnen beheerders en auteurs meerdere Zoom-sessies tegelijk plannen met behulp van de standaardintegratie.

### Nieuwe functies

#### Ondersteuning voor meerdere gelijktijdige zoomsessies via de connector

* Met de Zoom-connector kunnen nu meer dan één VILT-sessie op dezelfde datum/tijd worden gemaakt vanuit ALM.

* De planningslogica dwingt niet langer een &#39;één zoomvergadering tegelijk&#39;-beperking op account-/verbindingsniveau af.

* Beheerders en auteurs kunnen overlappende VILT-sessies configureren (bijvoorbeeld regionale lesruimten, parallelle tracks of herhaalde sessies voor verschillende partnergroepen) zonder tussenruimten.

#### Vergaderingen worden gemaakt met de zoomidentiteit van de docent (niet met de Zoom-superbeheerder)

Om veilige steun gezamenlijke vergaderingen, is de schakelaar bijgewerkt zodat:

* Zoomvergaderingen worden nu gemaakt met behulp van het e-mailadres van de docent in plaats van de e-mail met de Zoom-superbeheerder.

* De rekening van het Gezoem van elke instructeur kan zijn eigen vergaderingen naast andere instructeurs, met inachtneming van de grenzen van het bestaande plan van het Gezoem ontvangen.

**Nota**:

* Er wordt nog slechts één docent per vergadering ondersteund.

* Als de e-mail van een docent later in Adobe Learning Manager wordt bijgewerkt, blijven bestaande vergaderingen gekoppeld aan de oorspronkelijke e-mail die bij het maken is gebruikt.

#### Geen URL meer handmatig in-/uitzoomen voor gelijktijdige sessies

Eerder, toen een tweede of derde zitting van het Gezoem tezelfdertijd moest lopen:

* Auteurs moesten handmatig zoomvergaderingen buiten ALM maken en vervolgens de Zoom join-URL in de configuratie van de cursusinstantie plakken.

* Dit was foutgevoelig en profiteerde niet van verbindingsfuncties zoals het bijhouden van aanwezigheid.

Met de bijgewerkte connector:

* Alle sessies kunnen rechtstreeks vanuit de ALM-gebruikersinterface worden gemaakt met behulp van de zoomconnector, zelfs als ze overlappen in de tijd.

* De levenscyclus van sessies (maken/annuleren) wordt centraal beheerd via integratie.

### Belangrijkste voordelen

#### Betere planning van VILT op schaal

Organisaties kunnen nu:

* Voer tegelijkertijd meerdere op zoomen gebaseerde virtuele lesruimten uit (bijvoorbeeld parallelle tracks op een virtuele top, regionale cohorten of afzonderlijke trainingssessies van partners).

* Vermijd knelpunten waardoor beheerders eerder gedwongen werden om sessies te serialiseren of gebruik te maken van handmatig zoombeheer.

#### Minder overhead voor beheerders en auteurs

De verbetering elimineert:

* Handmatig Zoomvergaderingen buiten Adobe Learning Manager maken.

* Kopieer van Zoomen-URL&#39;s naar elke cursusinstantie voor overlappende sessies.

* Risico van verkeerd-gevormde verbindingen, verkeerde vergaderingen die worden vastgemaakt, of gemiste aanwezigheid het volgen.

Beheerders en auteurs kunnen alle Zoom-sessies vanuit Adobe Learning Manager beheren met behulp van vertrouwde workflows.

#### Betere uitlijning met Zoom-provisioning en docentrollen

Door vergaderingen aan individuele docenten te koppelen Zoom accounts:

* Elke docent kan binnen zijn eigen zoomlicentielimieten werken.

* Organisaties kunnen hun bestaande Zoom-inrichtingsmodel gebruiken (één account per trainer, per eenheid, enz.) en toch volledig geïntegreerd met Adobe Learning Manager.

* Zo voorkomt u het knelpunt met één punt bij het gebruik van een gedeelde superbeheerder-zoomgebruiker voor alle sessies.

### Gebruiksscenario&#39;s

#### Virtuele gebeurtenissen en topconferenties met meerdere tracks

Klanteducatieteams die grote evenementen uitvoeren (bijvoorbeeld productlokalen, partnertoppen of certificeringsweken) kunnen:

* Configureer meerdere op zoomen gebaseerde sessies in dezelfde periode (voor verschillende tracks of onderwerpen).

* Beheer al deze modules als VILT-modules onder de cursussen en leerpaden van Adobe Learning Manager.

* Geef studenten een uniforme ervaring terwijl de connector alle onderliggende Zoom-vergaderingen verwerkt.

#### Wereldwijde partner- en klantentraining

Organisaties die klanten en partners in verschillende regio&#39;s trainen, kunnen:

* Voer op overlappende tijden afzonderlijke zoomsessies uit voor EMEA, APAC en Amerika om de lokale werkuren af te stemmen.

* Vermijd het forceren van één algemene tijdsleuf of handmatige zoominstelling voor extra cohorten.

#### Interne activering

Interne actieteams (verkoop, ondersteuning, enzovoort) kunnen:

* Plan parallelle onboardingsessies of op rollen gebaseerde brainstormsessies (bijvoorbeeld aparte zoomruimten voor ontwikkelaars, beheerders en stakeholders uit het bedrijfsleven) in ALM.

* Houd alle sessies binnen het VILT-model van ALM voor rapportage- en nalevingsdoeleinden, in plaats van gedeeltelijk over te gaan naar onbeheerde Zoomvergaderingen.

## Oorspronkelijke auteur tonen voor gedeelde cursussen in collega-accounts

### Overzicht

Wanneer een cursus via de catalogus wordt gedeeld met een collega-account, labelt Adobe Learning Manager de auteur momenteel als &quot;Externe auteur&quot; in de weergaven Student, Beheerder en Auteur van het ontvangende account. Dit kan uitdagingen met zich meebrengen voor studenten en beheerders, met name in grote ondernemingen, omdat het moeilijk wordt om de juiste eigenaar van de inhoud te identificeren en te benaderen wanneer er problemen of vragen optreden.

De verbetering zorgt ervoor dat auteursinformatie voor gedeelde cursussen in collega-accounts wordt behouden en opgehaald, in plaats van te worden vervangen door een generieke plaatsaanduiding.

### Nieuwe functies

De werkelijke auteursnaam van gedeelde cursussen in collega-accounts tonen

Voor cursussen die via externe of collega-catalogi worden gedeeld, wordt de oorspronkelijke auteursnaam van het bronaccount nu weergegeven in het ontvangende account in plaats van &quot;Externe auteur&quot;.

Dit geldt voor:

* Learner-app (cursuskaart of cursusgegevens).

* Weergaven beheerder en auteur wanneer u een voorbeeld bekijkt als student.

### Belangrijkste voordelen

#### Rechtstreekse zichtbaarheid van gedeelde inhoud door eigenaars

Studenten en beheerders in collega-accounts kunnen nu:

* Zie wie de cursus heeft geschreven, zelfs wanneer deze via een gedeelde catalogus is verkregen.

* Vermijd het algemene en onnuttige label &#39;&#39;Externe auteur&#39;&#39;.

#### consistentere ervaring met meerdere tenant en collega-accounts

Voor klanten die scenario&#39;s voor meerdere tenant of uitgebreide ondernemingen uitvoeren:

* Dezelfde cursus wordt weergegeven met consistente merknamen van auteurs in verschillende accounts.

* De ervaring van de student is afgestemd op de verwachtingen van het primaire account (bijvoorbeeld: de auteursnaam van het bronaccount bekijken in plaats van &quot;Externe auteur&quot;).

### Gebruiksscenario&#39;s

#### Grote onderneming met collega-accounts

De onderneming gebruikt ALM met:

* Een hoofdaccount dat eigenaar is van de canonieke cursussen, en

* Collega-accounts die inhoud ophalen via gedeelde catalogi.

Studenten in collega-accounts moeten weten welk Enterprise-team een cursus heeft gemaakt om vragen of verbeteringssuggesties correct door te sturen.

Met deze verbetering:

* Gedeelde cursussen geven nu de juiste naam van de auteur van de onderneming weer in collega-accounts.

* De interne belasting van de ondersteuning van het bedrijf wordt verminderd omdat studenten en lokale beheerders weten met wie ze contact moeten opnemen.

#### Intern delen met meerdere bits per eenheid

Waar een bedrijfseenheid het leren voor anderen beheert:

* De eigendom van de BU kan in het auteurveld worden geïdentificeerd voor alle accounts die worden gebruikt.

* Lokale L&amp;D-beheerders kunnen snel zien of een cursus lokaal of door een andere BU wordt onderhouden en kunnen dienovereenkomstig samenwerken.

## Vervaldatum (automatisch archiveren) van leerobject weergeven in API&#39;s voor studenten

### Overzicht

Deze verbetering maakt de automatisch gearchiveerde datum van een leerobject (LO) direct beschikbaar via de studentgerichte API&#39;s van Adobe Learning Manager. Wanneer een cursus, leerpad of certificering is geconfigureerd met een vervaldatum of datum voor automatisch archiveren, maakt die informatie nu deel uit van de LO-gegevens die worden geretourneerd door de belangrijkste eindpunten voor studenten.

### Nieuwe functies

#### Nieuw verloopveld/automatisch archiefveld in LO-API&#39;s van student

* De LO-API&#39;s van de student (bijvoorbeeld de eindpunten die leerobjecten terugsturen naar de leerervaring en naar externe platforms) bevatten nu de vervaldatum van de LO (de voor dat leerobject geconfigureerde datum voor automatisch archiveren).

* Dit veld wordt geretourneerd als onderdeel van de LO-entiteit in reacties zoals:

   * Leerobject ophalen (LO-details).

   * LO-gegevens die worden gebruikt om de startpagina, catalogus en zoekresultaten van de student in te vullen.

* Het veld vult de bestaande deadline voor voltooiing aan die al bestaat op instantieniveau; het nieuwe veld is specifiek de datum voor automatisch archiveren op LO-niveau.

#### Beschikbaarheid in door zoekopdrachten ondersteunde leerervaringen

Omdat de vervaldatum als deel van de onderzoek-gesteunde vertegenwoordiging LO wordt blootgesteld, is het nu beschikbaar overal ALM of een extern platform gebruikt:

* zoekAPI&#39;s of

* zoekgestuurde catalogi en suggesties om studentweergaven samen te stellen.

**Reikwijdte en uitsluitingen**

De verbetering is alleen van toepassing op API&#39;s voor studenten.

### Belangrijkste voordelen

#### Vervalbestendige leerervaring in aangepaste LXP&#39;s

Voor grote en middelgrote ondernemingen kan hun aangepaste LXP nu rechtstreeks van ALM informatie over de LO-vervaldatum verkrijgen, zodat deze:

* Toon de labels &quot;Verlopen op {date}&quot; of &quot;Verlopen binnenkort&quot; op cursuskaarten en detailpagina&#39;s.

* Communiceer duidelijker met de urgentie, zodat studenten prioriteit geven aan training die op het punt staat met pensioen te gaan.

Dit is met name belangrijk voor compliance of een aan de tijd gebonden producttraining, waarbij leerobjecten regelmatig worden vernieuwd en oudere versies worden gearchiveerd.

#### Betere begeleiding voor studenten over welke training ze nu moeten volgen

Door het verstrijken van de LO zichtbaar te maken, kan de ervaring van de student:

* Markeer cursussen die nog geldig zijn in plaats van cursussen die binnenkort worden gearchiveerd.

* Voorkom dat studenten zich inschrijven voor trainingen die in de nabije toekomst niet meer beschikbaar of geldig zullen zijn.

#### Samenhang met bestaande gegevens van de voltooiingsdeadline

Voorheen werden de API&#39;s van de student al beschikbaar gesteld als voltooiingsdeadline op instantieniveau, maar niet als de datum voor automatisch archiveren op LO-niveau. Met deze wijziging:

De volgende aspecten van een training zijn beschikbaar:

* &quot;Tegen wanneer moet ik deze instantie voltooien?&quot; (voltooiingsdeadline).

* &quot;Tot wanneer wordt deze training aangeboden?&quot; (automatisch archiveren/vervaldatum).

### Gebruiksscenario&#39;s

#### Een wereldwijd bedrijf met een strikt levenscyclusbeheer voor cursussen

Ondernemingen die regelmatig cursussen archiveren en vervangen (bijvoorbeeld update van regelgeving, product of methodologie) kunnen:

* Vermijd verwarring bij studenten over de vraag of een training al dan niet moet worden afgebroken.

* Leerlingen naar het nieuwste, langlevende aanbod leiden.

Hun aangepaste portals en interne tools kunnen de vervaldatum nu rechtstreeks vanuit ALM lezen via de API&#39;s voor studenten.

#### Externe klant- of partneracademies

Voor het onderwijs aan klanten en partners leggen marketingpagina&#39;s en portals vaak de nadruk op actuele training.

Met vervaldatums in de LO API kunnen ervaringenbouwers:

* Inhoud die bijna is gepensioneerd verbergen of de nadruk erop leggen.

* Bouw &quot;Laatste kans om te voltooien&quot; campagnes.

## Meertalige ondersteuning voor taakhulpen

### Overzicht

De verbetering breidt het lokalisatiemodel van Adobe Learning Manager uit tot taakhulpen, waardoor auteurs verschillende inhoudsbestanden per taal kunnen koppelen aan één taakhulp. In plaats van afzonderlijke taakhulpen voor elke taal te maken, kunnen auteurs nu alle gelokaliseerde versies als één logische taakhulp beheren.

### Nieuwe functies

#### Taalspecifieke inhoud uploaden voor taakhulpen

Auteurs kunnen verschillende bestanden per ondersteunde taal aan één taakhulp koppelen, zoals cursussen en andere LO&#39;s.

Het maken/bewerken van taakhulp ondersteunt nu:

* Taal selecteren.

* Het taalspecifieke bestand voor die taal uploaden binnen dezelfde taakhulpentiteit.

#### Consistente taalverwerking in de gebruikersinterface van speler en student

De Fluidic Player is bijgewerkt zodat wanneer een student een taakhulp opent, de inhoudvariant wordt weergegeven die overeenkomt met de taal van de student (indien beschikbaar).

Beheerders en auteurs kunnen taakhulpen bekijken als afzonderlijke objecten met taalvarianten in plaats van afzonderlijke items per taal.

### Belangrijkste voordelen

#### Eén taakhulp voor alle talen

Auteurs kunnen voorkomen dat er afzonderlijke taakhulpen per taal worden gemaakt.

Alle taalvarianten van dezelfde taakhulp (bijvoorbeeld een procedure, SOP, checklist PDF of naslaggids) kunnen op één plaats worden beheerd.

#### Betere ervaring voor wereldwijde studenten

Studenten zien de taakhulp automatisch in hun voorkeurstaal, wat betekent dat er:

* Minder verwarring over welke versie moet worden geopend.

* Minder risico op het verkrijgen van toegang tot niet-lokale of verouderde kopieën.

Dit is vooral handig in meertalige organisaties waar hetzelfde proces of dezelfde productdocumentatie in meerdere talen beschikbaar moet zijn.

### Gebruiksscenario&#39;s

#### Globale uitrol van referentie-inhoud

Een onderneming moet studenten wereldwijd taakhulpen in verschillende talen bieden, zoals:

* Productreferentiebladen.

* Controlelijsten verwerken.

* Afspeelboeken ondersteunen

In plaats van afzonderlijke taakhulpen te maken zoals &quot;Product Quick Start - EN&quot;, &quot;Product Quick Start - DE&quot;, &quot;Product Quick Start - JP&quot;, enz., kunnen ze één taakhulp maken, gelokaliseerde bestanden voor elke taal koppelen en ALM de juiste versie laten leveren aan elke student op basis van taalinstellingen.

#### Klant- of partnergerichte documentatie voor meerdere markten

Voor klanten- en partneracademies kunnen taakhulpen het volgende omvatten:

* Productbedrukte vellen

* Integratiehandleidingen

* Workflows voor ondersteuning

Met meertalige taakhulpen:

* Elke partner ziet de gelokaliseerde versie zonder dat er een keuze hoeft te worden gemaakt tussen taalspecifieke items.

* Marketing- en actieteams kunnen één taakhulp per onderwerp beheren voor alle landinstellingen.

## Beperking voor begintijd module instellen

### Overzicht

Dankzij deze verbetering kunnen auteurs en beheerders in Adobe Learning Manager een tijdvenster definiëren waarin studenten een module mogen starten. Buiten het geconfigureerde begin-/eindvenster blijft de module zichtbaar in de cursusstructuur, maar studenten kunnen deze niet starten.

Deze mogelijkheid is van essentieel belang voor gebruikers die een betere controle nodig hebben over het moment waarop bepaalde inhoud beschikbaar komt of die niet meer mogen worden gestart, bijvoorbeeld in programma&#39;s op tijd, cohorttraining of tijdgevoelige oefeningen.

### Nieuwe functies

Auteurs kunnen nu op moduleniveau binnen een cursus een begindatum/tijd en einddatum/tijd configureren die bepalen wanneer studenten die module mogen starten. Binnen dit venster gedraagt de module zich zoals gewoonlijk; voor de begintijd of na de eindtijd ziet de student de module in het cursusoverzicht, maar kan deze niet starten.

De configuratie wordt in de gebruikersinterface voor het ontwerpen van de cursus weergegeven als extra besturingselementen voor specifieke moduletypen, zoals inhoud op eigen tempo, quizzen of activiteiten. Beheerders kunnen deze besturingselementen gebruiken om modules te maken die in fasen worden geopend of om te voorkomen dat programma&#39;s met een laat programma worden gestart waarin de inhoud binnen een bepaald tijdsbestek moet worden opgenomen.

#### Belangrijkste voordelen

Het belangrijkste voordeel is de mogelijkheid om te controleren wanneer de modules toegankelijk zijn. Trainingsteams kunnen de beschikbaarheid van modules synchroniseren met gebeurtenissen uit de praktijk, zoals het starten van nieuwe producten, deadlines en interne programma&#39;s. Zo zorgt u ervoor dat studenten de vereiste inhoud voltooien voordat ze toegang krijgen tot latere modules.

Cohort 1 heeft bijvoorbeeld alleen toegang tot module 2 in week 2, terwijl module 3 vergrendeld blijft tot week 3, zodat u niet handmatig inhoud hoeft te verbergen of te verbergen of afzonderlijke cursusversies hoeft te maken.

Dit verbetert de ervaring van de student: in plaats van modules te bekijken die technisch toegankelijk zijn maar op dat moment niet zouden moeten zijn (of die al zouden moeten worden voltooid), zien studenten een cursusstructuur waarbij de modules die ze mogen starten duidelijk worden afgestemd op het geplande schema.

#### Gebruiksscenario&#39;s

* **op cohort-gebaseerd educatieprogramma**: In dit programma, opent elke week een nieuwe module. De inhoud voor Week 1 is onmiddellijk beschikbaar, terwijl Week 2 zichtbaar is maar niet kan worden gestart tot een bepaalde datum. Week 3 volgt hetzelfde gatingproces. Studenten kunnen het volledige leerpad zien, maar het systeem bepaalt wanneer ze daadwerkelijk met elke stap kunnen beginnen.

* **tijd-gebonden product of campagneopleiding**: De marketing of productteams kunnen een trainingsmodule tot stand brengen die slechts zou moeten worden betreden terwijl een campagne actief is of wanneer een specifieke versie van een product nog beschikbaar is. Dit toegewezen beginvenster zorgt ervoor dat studenten na de opgegeven eindtijd niet met een module over een beëindigde productversie beginnen.

* **de milieu&#39;s van de Beoordeling of van het examen**: De organisaties kunnen een module (zoals een test) voor een kort, duidelijk-bepaald venster openen (bijvoorbeeld, &quot;u kunt het examen op elk ogenblik tussen 9 :00 en 12 :00 op een bepaalde datum&quot;beginnen). Studenten kunnen niet buiten dat venster beginnen met het examen, dat eerlijke planning over tijdzones en cohorten ondersteunt.

## Taal van speler beheren via aangepaste LTI-parameter

### Overzicht

Dankzij deze verbetering kunnen externe platforms met behulp van LTI (Learning Tools Interoperability) de taal voor Adobe Learning Manager-inhoud opgeven op het moment dat de toepassing wordt gestart. In plaats van dat de student de taal binnen de Fluidic Player moet wijzigen, kan de LTI-consument een taalcode verzenden via een aangepaste LTI-parameter. Adobe Learning Manager gebruikt deze code vervolgens om de juiste taalvariant te selecteren.

### Nieuwe functies

Externe platforms die fungeren als LTI-consumenten kunnen nu een aangepaste taalparameter (en verwante spelerinstellingen) doorgeven bij het starten van ALM-inhoud. ALM leest deze parameter en:

* Hiermee wordt de taal van de speler overeenkomstig ingesteld.

* Opent de overeenkomstige taalvariant van de module, wanneer de meertalige inhoud wordt gevormd.

Dit betekent dat een nieuwe student, die Frans selecteert op het externe platform, de ALM-speler ziet en de module direct in het Frans start, zonder dat hij iets hoeft aan te passen binnen ALM.

De uitbreiding biedt ook ruimte voor scenario&#39;s waarin ALM door het externe platform wordt behandeld als een headless contentspeler. Zo kunt u bijvoorbeeld navigatie-elementen en de inhoudsopgave verbergen door extra aangepaste parameters te verzenden om bepaalde gebruikersinterface-instellingen aan te passen. Deze instellingen werken in combinatie met de taalparameter, waardoor het externe platform een vloeiende merkervaring kan bieden terwijl ALM wordt gebruikt voor afspelen en bijhouden.

### Belangrijkste voordelen

* **Consistente taalervaring over systemen**: Wanneer een student een taal in het externe portaal selecteert, wordt die keuze onmiddellijk weerspiegeld in ALM. Zo voorkomt u dat studenten de taal van de portal en de cursus niet tegenkomen. Als gevolg hiervan hoeven ze niet te zoeken naar een taalwisseling binnen de speler.

* **taal-specifieke het melden**: In hun platform, is de taalselectie verenigbaar met ALM, dat de nauwkeurigheid van hun analytics en het leren volgen verbetert. Deze uitlijning ondersteunt ook configuraties waarbij de eigen taalbesturingselementen van ALM opzettelijk worden uitgeschakeld of verborgen in de Fluidic Player voor specifieke cursussen. In deze gevallen fungeert het externe platform als enige bron van waarheid voor taal.

### Gebruiksscenario&#39;s

* Een belangrijk gebruiksgeval betreft grote ondernemingen die gebruikmaken van op LTI gebaseerde integraties. Studenten schrijven zich eerst in en selecteren een taal op het platform. Vervolgens worden ALM-trainingssessies gestart via LTI. Als een student Spaans selecteert, wordt de ALM-module automatisch in het Spaans geopend. Dit betekent dat studenten de taalinstellingen in ALM niet hoeven aan te passen. Bovendien blijft taalgebaseerde rapportage consistent met wat studenten zien en ervaren in ALM.

* Een andere toepassing is het aanbieden van headless cursuservaringen binnen een klant- of partnerportaal. In deze setup kan de portal ALM-inhoud insluiten via een iframe, terwijl alle navigatie- en taalgebruikerservaring (UX) buiten ALM wordt beheerd. Door aangepaste LTI-parameters te gebruiken, kan de portal ervoor zorgen dat de ALM-speler wordt weergegeven in de juiste taal en dat overbodige gebruikersinterface-elementen (zoals de inhoudsopgave en navigatieknoppen) verborgen zijn. Zo kunnen studenten één coherente toepassing ervaren in plaats van een onsamenhangende verzameling tools.

* Dit is gunstig voor organisaties die grootschalige trainingen in meerdere talen uitvoeren met een ander LMS of leerplatform. Ze kunnen hun gebruik van dat platform standaardiseren voor het beheren van studentprofielen, het selecteren van landinstellingen en het presenteren van catalogi. Ondertussen fungeert ALM als een betrouwbare engine voor inhoud en tracering, waarbij de taalvoorkeuren en gebruikersinteracties worden gerespecteerd die tijdens elke LTI-lancering door het externe systeem worden opgegeven.

## Dekkingsgewicht van de checklist-vraag voor beoordelingen van docenten

### Overzicht

De verbetering introduceert gewogen controlelijsten, die instructeurs en managers toestaan om studenten te evalueren gebruikend scoreschalen en totale scores, eerder dan het behandelen van elke checklist vraag als gelijk. Het doel is het creëren van checklist te vergemakkelijken door het uitvoeren van gewogen evaluaties van vragen, waardoor het relatieve belang van verschillende acties of vaardigheden binnen één enkele checklist kan worden weerspiegeld.

### Nieuwe functies

Controlelijsten ondersteunen de volgende typen:

1. Ja/Nee
Het gedrag blijft hetzelfde als vandaag: elke vraag is Ja/Nee en de criteria voor het doorgeven zijn gebaseerd op het aantal &quot;Ja&quot;-antwoorden.

2. Vragen met hetzelfde gewicht

   * Vragen worden op een numerieke schaal (standaard 0-10) gescore, waarbij:

      * De maximale/minimale waarden op de schaal kunnen worden aangepast op controlelijstniveau.

      * De schaal kan nu beginnen bij 0 (de vorige minimumscore was 1).

   * Alle vragen hebben dezelfde maximale score. De checklist gedraagt zich dus als een uniforme scoreschaal voor elke vraag.

3. Verschillende vragen

   * Elke vraag heeft een eigen maximumscore (gewicht).

   * De criteria om te slagen zijn afhankelijk van het percentage van de totale mogelijke score die de student behaalt in de hele checklist (bijvoorbeeld &quot;geslaagd als de student ≥ 70% van de totale beschikbare score behaalt&quot;).

Voor alle typen controlelijsten:

* De **Recensent** (instructeur of manager) evalueert de student volgens het gevormde controlelijsttype:

   * Ja/Nee selecteren.

   * Selecteer scores op de gedefinieerde schaal.

* Het **Checklist** rapport wordt bijgewerkt om, voor vragen met verschillend gewicht te omvatten:

   * De maximale score voor elke vraag.

   * De score die elke leerling voor die vraag heeft behaald.

Op deze manier kunt u de algehele prestaties en de vraagspecifieke prestaties analyseren op basis van de bedoelde gewichten.

### Belangrijkste voordelen

* **Rijkere, realistischere beoordelingen**: De instructeurs kunnen echte prioriteiten weerspiegelen door meer punten aan kritisch gedrag en minder aan minder kleine te geven, terwijl nog het gebruiken van een controlelijstwerkschema geschikt aan waargenomen of praktische taken.

* **op totaal-score-gebaseerde pas/ontbreekt**: de evaluaties kunnen op de algemene percentagescore worden gebaseerd, niet alleen hoeveel vragen een drempel passeren, die dichter bij typische bekwaamheids of gradingsregelingen richt.

* **Betere rapportering**: De bijgewerkte controlelijstrapporten stellen max score bloot en behaalden score per vraag, toestaand programmaeigenaars en kwaliteitsteams om specifieke zwakke vlekken te identificeren en opleiding of evaluatierichtlijnen te verfijnen.

### Gebruiksscenario&#39;s

* **de vaardigheidsbeoordelingen van de Onderneming**: De ingenieurs worden beoordeeld via praktische, op scenario-gebaseerde checklists waar bepaalde diagnostische of communicatie stappen meer gewicht moeten dragen dan cosmetische of laag-risicopauters. Gewogen vragen en criteria voor het halen van de score maken deze beoordelingen geloofwaardiger en voorspelbaarder van real-world prestaties.

* **de observaties van de Veiligheid en van de naleving**: In gezondheidszorg, de productie, of de velddienst, kunnen de kritieke veiligheidsstappen hogere maximumscores worden gegeven, die ervoor zorgen dat het missen van een veiligheid-kritieke actie een grotere invloed op de totale score heeft dan het missen van een minder belangrijke procedurele stap.

* **Coaching en kalibratie**: Met max. en behaalde scores per vraag in het rapport, kunnen de managers precies zien waar de studenten onderpresteren en docenten kalibreren op hoe te om constant te scoren.

## Meertalige ondersteuning voor vragen over checklist

### Overzicht

De verbetering introduceert meertalige steun voor checklist vragen, die recensenten toestaan om controlelijsten in hun aangewezen taal te evalueren en te scoren. Deze functie is vooral handig in meertalige regio&#39;s en wereldwijde implementaties, omdat auteurs zo gelokaliseerde vragen over checklist kunnen maken voor elke ondersteunde inhoudstaal, terwijl één controlelijstmodule en een consistent evaluatieproces behouden blijven.

Vandaag in Adobe Learning Manager:

* Alle studentgerichte modules (SCORM, PDF, HTML, enz.) kunnen in meerdere inhoudstalen worden aangeboden, zodat studenten de taal van hun voorkeur kunnen kiezen.

* In een controlelijstmodule evalueren revisoren (docenten/managers) studenten op basis van de vragen die in die controlelijst zijn gedefinieerd.

### Nieuwe functies

**Auteurs**

* Auteurs kunnen nu vragen toevoegen met een checklist in alle talen die op cursusniveau zijn geselecteerd.

* Voor elke controlelijst:

   * Van de auteur wordt verwacht dat deze equivalente vraagtekst levert in elke inhoudstaal waarin de cursus bestaat.

   * Auteurs moeten ervoor zorgen dat de betekenis van elke vraag in alle talen consistent is.

**ervaring van het Overzicht**

* Revisoren zien vragen over checklist en evaluatie-UI in hun geselecteerde inhoudstaal.

* Wanneer een vraag in één taal wordt geëvalueerd:

   * De evaluatie (score, Ja/Nee, status) is logischerwijze hetzelfde in alle talen. Het is één controlelijst met meerdere taalweergaven, niet afzonderlijke controlelijsten per taal.

**Rapportage**

In het controlelijstrapport wordt de vraagtekst weergegeven in de inhoudstaal van de gebruiker:

* Een beheerder of revisor die het rapport in elke taal uitvoert, ziet de gelokaliseerde vraagnamen voor die taal.

* De onderliggende reacties en scores blijven hetzelfde; alleen vraaglabels worden vertaald.

### Belangrijkste voordelen

* **Betere reviewerervaring**: de recensenten kunnen volledig in hun eigen taal werken, het lezen van vragen en het registreren van evaluaties zonder taalbarrières.

* **regelgevende en beleidsgroepering**: In gebieden met de eisen van de taalgelijkheid (bijvoorbeeld, Nederlands/Frans in België), kunnen de checklists aan de zelfde normen nu voldoen zoals andere het leren materialen, die nalevingsrisico verminderen.

* **Consistente evaluatielogica**: Terwijl de tekst wordt gelokaliseerd, worden de evaluatie en het scoren gedeeld over alle talen, die ervoor zorgen dat de resultaten vergelijkbaar en centraal beheerd zijn.

### Gebruiksscenario&#39;s

* Licenties voor meerdere landen die in meerdere talen werken, kunnen één cursus en checklist implementeren en tegelijkertijd de gelokaliseerde revisieervaringen bieden op elk gebied.

* Elke internationale onderneming met lokale docenten (bijvoorbeeld EMEA, LATAM, APAC) kan revisoren in hun lokale taal laten werken terwijl ze hetzelfde ontwerp en dezelfde rapportage van de wereldwijde checklist delen.

## Controlelijst met opmerkingsmogelijkheden voor revisor

### Overzicht

De verbetering introduceert een opmerkingseigenschap voor checklist evaluaties, die recensenten, zoals instructeurs en managers, toestaan om kwalitatieve feedback naast de numerieke scores te verstrekken. Deze feedback kan indien nodig zichtbaar worden gemaakt voor studenten.

Het doel is op checklist gebaseerde evaluaties te ondersteunen waarbij mentor feedback even belangrijk is als het numerieke resultaat. Dit omvat het benadrukken van specifieke sterke punten, gebieden voor verbetering, of het verstrekken van context voor de bepaalde score.

Tegenwoordig kunnen revisoren:

* Evalueer een checklist voor elke student, vraag per vraag.

* Bekijk resultaten en evalueer de mislukte studenten opnieuw.

In echte scenario&#39;s, zoals de luchtvaart, beoordelen praktijkopleiders vakmensen en luchthavenpersoneel. Ook docenten en mentoren in het midden- en kleinbedrijf (MKB) maken vaak gebruik van checklists om de prestaties van hun werk te evalueren. Deze checklists bevatten doorgaans echter geen gestructureerde sectie voor het vastleggen van commentaar met betrekking tot de evaluatie.

### Nieuwe functies

#### Ontwerpopties

Auteurs kunnen elke checklist als volgt configureren:

* De mogelijkheid om opmerkingen toe te voegen aan revisoren in of uit te schakelen.

* Bepaal of de naam van de revisor samen met opmerkingen aan de studenten moet worden getoond.

Zo kunnen organisaties de zichtbaarheid van opmerkingen afstemmen op hun cultuur- en privacyvereisten.

#### Revisor-ervaring

Als opmerkingen zijn ingeschakeld:

* Revisoren (docenten/managers) kunnen optionele opmerkingen toevoegen tijdens het evalueren van een controlelijst.

* Ze kunnen op basis van de instellingen van de controlelijst kiezen of de opmerkingen zichtbaar zijn voor de studenten.

Als ze een student opnieuw evalueren, kunnen ze opmerkingen bijwerken of wijzigen om de laatste beoordeling weer te geven.

#### Rapportage en kennisgevingen

* Het controlelijstrapport krijgt een nieuwe kolom voor de opmerkingen van de revisor, waarin de opmerking wordt vastgelegd die tijdens de evaluatie is toegevoegd.

* Studenten ontvangen meldingen (op het platform en via e-mail) wanneer een checklist-evaluatie plaatsvindt. Deze meldingen omvatten:

   * De opmerking en

   * De naam van de revisor, als deze is geconfigureerd om zichtbaar te zijn.

Zo weet u zeker dat de feedback niet alleen wordt opgeslagen, maar ook actief aan de studenten wordt getoond.

### Belangrijkste voordelen

* **rijkere, coach-als terugkoppelen**: De numerieke scores worden aangevuld met contextuele opmerkingen, die checklists een effectiever hulpmiddel maken om te coachen, niet alleen naleving.

* **Traceerbaarheid en controleerbaarheid**: De organisaties krijgen een permanent verslag van wie evalueerde wie, wanneer, en wat zij zeiden, wat in gereglementeerde milieu&#39;s en high-stakes rollen belangrijk is.

* **Betere studentbetrokkenheid**: De studenten ontvangen duidelijke begeleiding verbonden aan specifieke evaluaties, die hun inzicht in verwachtingen en verdere stappen verbetert.

### Gebruiksscenario&#39;s

* Organisaties met gereguleerde omgevingen kunnen opmerkingen gebruiken om klinische beoordelingen of procedurele feedback te documenteren voor personeel dat op het terrein wordt geobserveerd.

* Luchtvaart- en grondafhandelingsorganisaties kunnen gedetailleerde notities toevoegen over operationele prestaties, veiligheidspraktijken en klantgericht gedrag, waardoor een checklist verandert in een gestructureerde debrieftool.

* In mentoring en SME-evaluatie kunnen docenten genuanceerde observaties vastleggen die niet alleen in een score passen, bijvoorbeeld ‘afgehandelde escalatie goed maar moet tijdbeheer verbeteren’ of ‘uitstekende workflow voor probleemoplossing; een documentatiestap gemist.’

## Meerdere pogingen en quizrapportage op inhoudsniveau

### Overzicht

>[!IMPORTANT]
>
>Let op: deze functie is alleen beschikbaar nadat u deze in het account hebt ingeschakeld. Contact opnemen met ALM-ondersteuning.


Momenteel ondersteunt ALM meerdere pogingen op LMS-niveau via de MQA (Multiple Quiz Attempt):

* Auteurs kunnen pogingen op cursusniveau (toegepast op alle quizdragende modules in de cursus) of op moduleniveau (per quizmodule) configureren.

* Pogingen kunnen zijn:

   * Een specifiek getal (bijvoorbeeld 3 pogingen), of

   * Oneindige pogingen, bestuurd op LMS-niveau.

* Wanneer een student een module via de Fluidic Player afsluit en de speler vervolgens sluit of de module voltooit, wordt die sessie behandeld als een enkele LMS-poging.

* Elke LMS-poging wordt in het L2-quizrapport vastgelegd als een nieuwe rij.

Als het inhoudsbestand zelf (bijvoorbeeld een Articulate SCORM-quiz) echter zijn eigen logica voor meerdere pogingen implementeert, wordt in het L2-quizrapport van ALM deze interne pogingen momenteel niet goed onderscheiden of bijgehouden.

Deze verbetering introduceert meerdere pogingen bijhouden op inhoudsniveau voor quizzen, zodat Adobe Learning Manager elke poging in de inhoud zelf nauwkeurig kan vastleggen in het L2-quizrapport. Het is ontworpen voor situaties waarin het inhoudsontwerpgereedschap (zoals Articulate SCORM) quizpogingen onafhankelijk beheert. Met deze functie worden pogingen correct weerspiegeld in ALM-rapportage, zonder dat dit afhankelijk is van de MQA-instellingen (Multiple Quiz Attempt) op LMS-niveau.

### Nieuwe functies

#### Auteurmarkering voor pogingen op inhoudsniveau

* Wanneer auteurs inhoud naar de inhoudsbibliotheek uploaden, kunnen ze nu aangeven dat er meerdere pogingen in zijn ingesloten voor een bepaald inhoudsbestand.

* Dit is een instelling per inhoud die ALM vertelt om pogingen die in de inhoud zijn gedefinieerd, te behandelen als de bron van de waarheid.

#### Cursus-/modulegedrag

Wanneer dergelijke inhoud in een cursus wordt gebruikt:

* De module zal zijn pogingen uit de inhoud, niet uit MQA leiden LMS.

* Studenten zien slechts één poging op LMS-niveau:

   * Het cursusoverzicht en de moduleweergave geven geen LMS-knop &quot;Opnieuw proberen&quot; voor die module weer.

   * De afhandeling van pogingen (bijvoorbeeld opnieuw proberen in de quiz) wordt bepaald door de inhoud zelf.

#### Rapportage

In het L2-quizrapport wordt elke poging op inhoudsniveau behandeld als een afzonderlijke poging:

* Elke interne quizpoging die in de inhoud is geconfigureerd, wordt als een eigen rij weergegeven in het L2-quizrapport, zoals hoe pogingen op LMS-niveau vandaag worden weergegeven.

* De opmaak van elke rij blijft hetzelfde als bestaande rijen met meerdere pogingen in L2-rapportage (dezelfde kolommen, structuur en semantiek).

* Dit biedt een consistente rapportage-ervaring:

   * Of pogingen nu door LMS MQA of door de inhoud worden bepaald, het L2 quizrapport toont één rij per poging.

#### Belangrijkste voordelen

* Nauwkeurige zoekgeschiedenis voor SCORM-quizzen waarbij pogingen intern worden bestuurd door gereedschappen zoals Articulate, zonder dat MQA-configuratie op LMS-niveau bovenaan hoeft te staan.

* Mindere ervaring voor studenten: voor pogingen met inhoudsregeling zien studenten één sleuf op LMS-niveau en hoeven ze niet te communiceren met de besturingselementen voor nieuwe pogingen in LMS; alle pogingen worden afgehandeld binnen de quizinterface die ze al kennen.

* Flexibele architectuur: gebruikers kunnen kiezen of ALM MQA of pogingen op inhoudsniveau gedrag per module moeten aansturen, afhankelijk van hoe hun inhoud is gemaakt en hoe ze pogingen liever beheren.

* Consistent rapportmodel: downstream-consumenten van het L2-quizrapport kunnen elke rij als &quot;één poging&quot; behandelen, ongeacht waar de logica van de poging vandaan komt.

#### Gebruiksscenario&#39;s

* Organisaties die Articulate SCORM gebruiken, kunnen zelfstandige quizlogica binnen het SCORM-pakket houden en tegelijkertijd een nauwkeurige rapportage op proberen-niveau bereiken in ALM zonder extra LMS-configuratie.

* Organisaties die door leveranciers verschafte SCORM-inhoud gebruiken, kunnen voorkomen dat ze aanvullende pogingen moeten wijzigen of implementeren en opnieuw logica moeten proberen met MQA op LMS-niveau.

## QR-codes voor docenten, bijvoorbeeld inschrijving en aanwezigheid van sessies

### Overzicht

Deze verbetering voegt de mogelijkheid toe voor docenten om zelf QR-codes te genereren voor:

* Inschrijving van cursusinstantie,

* aanwezigheid van een sessie, of

* Inschrijving + aanwezigheid samen

op sessieniveau. Het is ontworpen voor situaties waarin studenten een fysieke of hybride lesruimte betreden en een snelle, selfserviceoptie nodig hebben om zich in te schrijven en hun aanwezigheid vast te leggen met een QR-code.

### Nieuwe functies

#### Door docenten gegenereerde QR-codes

* Docenten kunnen op sessieniveau QR-codes genereren voor:

   * Inschrijven in instantie: studenten kunnen zich inschrijven voor de instantie die de huidige sessie bevat.

   * Aanwezigheid van sessie markeren: studenten scannen tijdens/na de sessie om aanwezigheid voor die specifieke sessie vast te leggen.

   * Aanwezigheid voor instance- en markeringssessie: een gecombineerd QR voor walk-ins die nog niet zijn ingeschreven en hun aanwezigheid in één stap moeten markeren.

* Docenten kunnen de QR-codes die ze nodig hebben exporteren op basis van het scenario (inschrijving, aanwezigheid of beide).

#### Verpakken van QR-code

De geëxporteerde PDF van de QR-code bevat:

* Cursusnaam

* Instantienaam

* Naam van sessie

Hiermee kunnen docenten en coördinatoren eenvoudig de juiste QR-code voor elke sessie identificeren en afdrukken.

### Belangrijkste voordelen

* **autonomie van de Instructeur**: De instructeurs hoeven niet meer op beheerders te wachten om QR codes te creëren. Ze kunnen ze direct voor elke sessie genereren, waardoor ze flexibeler worden en de overhead op het gebied van coördinatie vermindert.

* **Betere klaslokaallogistiek**: voor loop-binnen of on-site doelgroepen (zoals gebiedsarbeiders, werkplaats personeel, of externe aanwezigen), kunnen de instructeurs inschrijving en aanwezigheid op de plaats beheren gebruikend QR codes.

* **Verminderde admin werkbelasting**: De teams van Admin kunnen zich op configuratie en beheer in plaats van het behandelen van routine QR de verzoeken van de codegeneratie voor elke zitting concentreren.

### Gebruiksscenario&#39;s

* Organisaties die grote hoeveelheden on-site sessies uitvoeren (bijvoorbeeld producttraining voor professionals) kunnen docenten in staat stellen sessiespecifieke QR-codes af te drukken waarmee ze kunnen inschrijven en aanwezigheid kunnen markeren met één scan.

* In retail-, productie- en gezondheidszorgtrainingen, waar studenten vaak rechtstreeks vanuit de vloer of zonder voorafgaande inschrijving deelnemen aan sessies, kan een QR-code voor Inschrijven + Aanwezigheid bij de deur worden geplaatst. Zo kunnen studenten hun inschrijving en aanwezigheid zelf bedienen via hun telefoon.

* Door trainingsgebeurtenissen voor partners of klanten kan de trainer ter plaatse zich gemakkelijk aanpassen aan wijzigingen in de ruimte, extra sessies of extra aanwezigen zonder dat hij of zij de beheerder om nieuwe QR-codes hoeft te vragen.

## Verbeteringen op gebied van Captivate en ALM-speler

### Overzicht

Deze verbetering verbetert de ervaring van het afspelen van Adobe Captivate-inhoud in de Adobe Learning Manager-speler (ALM), met name na de recente wijzigingen in de architectuur van de Captivate. Het doel is om studenten in staat te stellen om zelf Captivate-modules te gebruiken in ALM, terwijl ze er zeker van zijn dat navigatie, het volgen van de voltooiing en het nemen van notities duidelijk, consistent en betrouwbaar zijn.

### Nieuwe functies

#### Uniforme ervaring voor inhoudsopgave

* Aan de linkerkant van de speler wordt alleen de ALM-inhoudsopgave weergegeven.

* De eigen inhoudsopgave van de Captivate wordt verborgen wanneer de module wordt afgespeeld binnen ALM.

* Zo voorkomt u dubbel werk, zorgt u voor één bron van waarheid voor navigatie en maakt u ruimte in het scherm vrij.

#### Feedback voor visuele voltooiing

* De TOC ALM toont groene vinkjes (of gelijkwaardige visuele aanwijzingen) die op dianiveau voltooiing wijzen.

* Naarmate studenten de dia&#39;s met Captivates doorlopen, geeft de ALM-inhoudsopgave aan welke dia&#39;s zijn voltooid, in overeenstemming met de verwachtingen van de studenten voor moderne cursusspelers.

#### Besturingselementen voor contextafhankelijke voortgang

* De besturingselementen van de speler worden aangepast op basis van het diatype:

   * Voor videodia&#39;s:

      * Tijdvoortgangsbalk weergeven die het afspelen van video weerspiegelt.

* Voor niet-videodia&#39;s:

   * Besturingselementen voor dianavigatie weergeven (volgende/vorige dia, enz.) in plaats van een niet-functionele tijdbalk.

      * Hiermee voorkomt u dat er irrelevante of niet-werkende besturingselementen voor bepaalde diatypen worden weergegeven.

#### Vereenvoudigde navigatie

* De afzonderlijke navigatiebalk voor de module (ALM) en de navigatiebalk voor de cursus worden samengevoegd tot één intuïtieve balk.

* Deze geïntegreerde navigatie:

   * Hiermee maakt u duidelijk onderscheid tussen het bewegen door de module Captivate en het teruggaan naar het cursus-/moduleniveau.

   * Hiermee vermindert u verwarring die wordt veroorzaakt door meerdere balken met overlappende doeleinden.

#### Betrouwbare aantekeningen

* Notities zijn gekoppeld aan dianummers in plaats van tijdstempels.

* Deze wijziging:

   * Hiermee worden exportfouten gecorrigeerd die worden veroorzaakt door ontbrekende of onjuiste tijdstempels.

   * Hiermee zorgt u ervoor dat notities consistent als PDF kunnen worden geëxporteerd, waarbij notities op betrouwbare wijze kunnen worden toegewezen aan de diacontext waartoe ze behoren.

### Belangrijkste voordelen

* Duidelijkere ervaring met één speler: studenten communiceren met één inhoudsopgave en één navigatiemodel, waardoor verwarring en cognitieve belasting afnemen.

* Nauwkeurige informatie over voltooiing en voortgang: dankzij tikken op dia-niveau en contextuele besturingselementen kunnen studenten zien waar ze zich bevinden en wat er nog over is.

* Betere notities maken en exporteren: gebruikers koppelen notities aan dia&#39;s in plaats van fragiele tijdstempels om een betrouwbare workflow voor notities naar PDF te maken, zelfs met op dia&#39;s gebaseerde Captivate-inhoud.

* Workflow van gereserveerde auteurs: auteurs behouden de eenvoud van directe publicatie door de Captivate naar ALM, terwijl studenten een moderne, geïntegreerde afspeelervaring krijgen zonder extra authoringlasten.

### Gebruiksscenario&#39;s

* Met behulp van integratieprogramma&#39;s die voor interactieve simulaties afhankelijk zijn van Captivate, kan inhoud in ALM worden geïmplementeerd, zodat navigatie, het bijhouden van de voltooiing en notities consistent blijven voor studenten.

* Organisaties die Captivate als hun belangrijkste inhoudsontwerpprogramma gebruiken, kunnen publiceren met één klik en verwarrend voorkomen met dubbele inhoudsopgaven en niet-functionele besturingselementen voor studenten.

* Organisaties die gebruikmaken van notities die zijn geëxporteerd uit Captivate-inhoud in ALM (voor coaching, compliance of records), hebben toegang tot:

   * Notities worden correct gekoppeld aan dia&#39;s.

   * PDF worden gegenereerd zoals verwacht.

## Verbeterde leertijd voor berekening in Studenttranscripten

### Overzicht

Adobe Learning Manager heeft met zijn release van april 2026 herzien hoe het de leertijd in Studenttranscripten berekent. Voorheen kon de rapportlogica leiden tot onnauwkeurige tijden als studenten de speler open lieten zonder zich met de inhoud bezig te houden, waardoor er discrepanties ontstonden. De nieuwe methode houdt nu de actieve tijd bij op basis van de gebruikersbetrokkenheid, met name wanneer de focus op de tab ligt en wanneer er gebruikersactiviteit is. Deze wijziging resulteert in nauwkeurigere gegevens.

Deze update verbetert rapporten en dashboards, helpt beheerders beter naleving te garanderen en de voortgang van studenten bij te houden. Controleer na de release uw studenttranscripten om deze verbeteringen te zien.

De bijgewerkte berekeningsmethode richt zich op daadwerkelijke betrokkenheid, zoals actieve tabfocus en recente gebruikersinteracties, waardoor de nauwkeurigheid van tijdrapportage op de volgende gebieden wordt verbeterd:

* Studenttranscripten (UI)
* Dashboardmetrics voor beheerders
* Cursusinschrijvingsrapporten
* API&#39;s en connectoren

### Gewijzigde functies

De **bestede tijd van het Leren** kolom in de Transcripten van de Student gebruikt nu betere logica om tijd nauwkeuriger te berekenen. In plaats van alleen de openings- en sluitingstijden van de speler te volgen, maakt het systeem nu onderscheid tussen actieve en inactieve perioden op basis van gebruikersbetrokkenheid.

* **Actieve tijd**: Tijd wanneer de student actief wordt betrokken (bijvoorbeeld, op het correcte lusje, uitvoerend acties zoals het scrollen of het letten van video).
* **nutteloze tijd**: Tijd wanneer de student niet wordt betrokken (bijvoorbeeld, tabel geschakeld, geen activiteit voor 10+ minuten), die van het totaal wordt uitgesloten.

Dit geldt voor de meeste moduletypen, met uitzondering van SCORM-, Captivate- en XAPI-modules, die de oorspronkelijke logica behouden.

### Zo werkt het

De nieuwe berekening varieert per moduletype:

* **Video en audiomodules**: Actief wanneer de inhoud speelt, zelfs als de student aan een andere tabel overschakelt. Tabfocus is niet vereist voor het bijhouden van de afspeeltijd.
* **Statische modules (PDF, PPT, Excel, etc.)**: Actief als op het lusje en uitvoerend activiteiten (muisbeweging, het scrollen, het klikken, toetsenbordinput) binnen de laatste 10 minuten. Als er gedurende 10 minuten geen activiteit is, wordt er overgeschakeld op inactief.
* **SCORM en Captivate** behouden de originele open/dichte logica.
* **xAPI** gebruikt nu op lusje-gebaseerde actieve tijdopsporing, waar de tijd slechts wordt geteld wanneer het lusje actief is. Merk op dat AICC inhoud **niet** wordt gesteund.
* **HTML, LTI, en Andere Inhoud**: kan variëren; controleer de Transcripten van de Student voor nauwkeurigheid.

De inactieve tijd wordt afgetrokken, zodat alleen de werkelijke betrokkenheidstijd wordt gerapporteerd.

>[!NOTE]
>
>Als uw laptop overschakelt naar de slaapmodus, wordt de leertijd mogelijk niet goed bijgehouden. Dit komt doordat het volgen van de activiteit pauzeert terwijl het systeem in slaap is en pas hervat wanneer de laptop wakker wordt.


### Samenvattingstabel

| **Type van Module** | **Actieve tijd (geteld)** | **Niet-actieve tijd (uitgesloten)** |
| --- | --- | --- |
| **Video / Audio** | Afspeeltijd | Niet gestart; beëindigd; gepauzeerd **\>10 min** |
| **Statisch (PDF/PPT/DOC)** | Het actieve lusje **en** activiteit in laatste **10 min** | Geen activiteit **\>10 min**; tab inactief |
| **SCORM** | Tijd gerapporteerd door inhoudruntime | Niet-actief kan niet worden gedetecteerd |
| **Captivate** | Op dia&#39;s gebaseerde timing | Niet-actief kan niet worden gedetecteerd |
| **xAPI** | Tab actief | Tab niet actief |
| **HTML** | De open tijd van de speler met lusje actief | Tab niet actief |
| **LTI Producer/Consument** | Als de inhoud LTI binnen de speler van ALM (namelijk ALM wordt gespeeld die inhoud LTI op een andere LMS wordt ontvangen handelend als Producent), dan is deze tijd-bestede logica van toepassing.<br><br> Nochtans, als de inhoud buiten LMS (namelijk wordt de inhoud ontvangen in ALM, dan is ALM de Producent, maar de playback gebeurt in een externe speler), dit gedeelte van de tijd-berekening niet toepassen.  <br>**Nota**: De consument LTI wordt niet gesteund in Adobe Learning Manager. | Tab niet actief |

**Nota**:

* **Revisits en parallelle zittingen**: Telling als actief wanneer de bovengenoemde voorwaarden worden voldaan aan.
* **Alle apparaten, browsers, talen**: Omvat; het off-line mobiele gebruik wordt toegevoegd na synchronisatie.

### Voordelen van de nieuwe berekening

* **nauwkeurige het melden**: Elimineert opgeblazen tijden van onbeheerde spelers, die realistische het leren duur verstrekken.
* **Betere naleving**: Steunt nauwkeurige het volgen voor verplichte opleiding (bijvoorbeeld, het maandelijkse vereiste van 5 uur van een bedrijf).
* **Verbeterde dashboards**: De grafieken van de gebruikersactiviteit en de tijd-bestede rapporten wijzen nu op daadwerkelijke betrokkenheid.
* **de inzichten van de Student**: Helpt beheerders echte vooruitgang identificeren en ontkoppelde studenten richten.

### Effecten van rapportage en analytics

* **Transcripten van de Student:** &quot;het Leren bestede tijd&quot;wijst nu op **daadwerkelijke engagement**.
* **Dashboard Admin:** Metriek die tijd (bijvoorbeeld, &quot;bestede tijd&quot;tegels, tendensen) omvatten zal **lagere maar meer realistische** waarden in scenario&#39;s tonen waar de nutteloze tijd eerder opblaasde resultaten.
* &lbrace;de rapporten van de Inschrijving van de cursus:**Op tijd betrekking hebbende gebieden keuren de** nieuwe berekening **post-lancering goed.**
* **de nota van de Vergelijkbaarheid:** omdat de historische gegevens niet worden herberekend, tijd-reeksen analyses die de versiedatum overspannen kunnen a **stapverandering** tonen. Overweeg annotatie of segmentatie op datum in analytics-tools.

### API en connectoren

* **geen schemaveranderingen** in bestaande eindpunten/gebieden die bestede tijd melden.
* **semantiek van het Gebied** wordt bijgewerkt om _actief-tijdberekening_ voor zittingen **na** de eigenschaplancering te wijzen.
* **de schakelaars en de uitvoer** verbruikende tijd-bestede gebieden zullen automatisch de bijgewerkte waarden ontvangen die vooruit gaan.

### Achterwaartse compatibiliteit en gegevensmigratie

* **Historische zittingen:** niet herberekend.
* **Nieuwe zittingen:** Gebruik de **nieuwe** actief-tijdberekening.
* **Gemengde periodes:** voor controles of longitudinale rapportering, segment door **pre/post-lancering** om misinterpretatie te vermijden.

### Bekende beperkingen

* **de Interactieve inhoud** (SCORM/Captivate) blijft zich op inhoud-verstrekte timing baseren; de nutteloze opsporing binnen de inhoud is niet beschikbaar.
* **op iframe-gebaseerde inhoud** (HTML/xAPI) beperkt opsporing van fijnkorrelige interactie; de lusjespiegels worden in plaats daarvan gebruikt.

### Veelgestelde vragen

**verandert deze update historische verslagen?**

Aantal De wijziging is alleen van toepassing op sessies nadat de functie is gestart.

**Hoe verifieer ik de veranderingen?**

Controleer de studenttranscripten voor recente modules; vergelijk de tijden met de verwachte duur.

**beïnvloedt dit alle rekeningen?**

Ja, het is een algemene update voor alle Adobe Learning Manager-accounts.

**moeten de studenten actie ondernemen?**

Aantal De wijziging is automatisch en transparant voor studenten.

**wat als de studenten open inhoud verlaten?**

De inactieve tijd wordt nu uitgesloten, waardoor overrapportage wordt voorkomen.

**zijn video/audiozittingen auto-gepauzeerd wanneer het lusje inactief is?**

Aantal Het afspeelgedrag blijft ongewijzigd. Tijd is uitgesloten wanneer gepauzeerd > 10 minuten of wanneer niet actief wordt afgespeeld.

**zal de offline mobiele activiteit worden weerspiegeld?**

Ja. Offlinegebruik wordt opgenomen wanneer het apparaat wordt gesynchroniseerd.

**wat zou ik als mijn dashboards nu lagere gemiddelden tonen moeten doen?**

Dit wordt verwacht wanneer inactieve tijd eerder opgeblazen resultaten had. Annoteer dashboards en pas doelen waar nodig aan.

**zijn er om het even welke eerste vereisten?**

Geen; de wijziging wordt automatisch uitgevoerd.

## Bijwerken naar leertranscriptrapporten voor beheerders

We werken de Leertranscript-rapporten (LT) voor beheerders bij ter betere ondersteuning van op checklist gebaseerde evaluaties en feedback van revisoren.

## Wat verandert?

### &#x200B;1. Naam kolom wijzigen in beheerdertranscript

De bestaande **kolom van de Commentaar van de Indiening** in het Leren Admin
Transcriptie is:

1. **anders genoemd aan:** `Reviewer's remarks`

### Gegevens weergegeven in deze kolom:

* **voor voorleggingsmodules:**
In de kolom wordt de opmerking bij verzending nog steeds weergegeven (er wordt geen gedragswijziging toegepast).

* **voor checklist modules:**
In de kolom wordt nu de opmerking bij de evaluatie weergegeven (de opmerkingen van de revisor op de controlelijst).

Deze wijziging is van toepassing op alle LT-bronnen van de beheerder:

* LT gedownload van beheerinterface
* LT verkregen via de taak-API
* LT gegenereerd via connectoren

Na deze wijziging staat in dezelfde kolom het volgende: - Opmerkingen verzenden voor verzendmodules

* Opmerkingen bij de evaluatie van controlelijstmodules

Onder de nieuwe kopbalnaam {de opmerkingen van 0} Recensent **.**

### &#x200B;2. Nieuwe kolom in op connector gebaseerd leertranscript exporteert

Voor door connector geëxporteerde leertranscripten:

* Een nieuwe kolom genoemd {de opmerkingen van 0} Recensent **wordt toegevoegd aan het eind van het rapport.**
* Deze kolom bevat de opmerkingen van de revisor, uitgelijnd op het hierboven beschreven gedrag:
   * Opmerkingen bij indiening voor indieningsmodules
   * Opmerkingen bij de evaluatie van controlelijstmodules

## Gevolgen voor bestaande integraties en automatiseringen

Als u leertranscriptrapporten gebruikt in aangepaste integraties, automatiseringsprogramma&#39;s of externe rapportagetools, bekijkt u de volgende scenario&#39;s:

| Scenario | Gevolgen | Vereiste actie |
|----------|--------|----------------|
| U identificeert velden in Admin LT op kolomnaam (bijvoorbeeld &quot;Opmerking voor verzending&quot;) | De kolomkop verandert in de opmerkingen van de revisor. | Ja. Werk de toewijzingen of logica bij die verwijzen naar de opmerking bij Verzending om de opmerkingen van de Revisor te gebruiken. |
| U identificeert velden in Admin LT alleen op kolompositie (op basis van index) | De positie van deze kolom blijft dezelfde in Admin LT. | Meestal geen actie. Als uw logica niet afhankelijk is van de koptekst, hoeft u niets te wijzigen voor Admin LT, wijzigt u alleen de kolomnaam als de kolom Opmerkingen verzenden is gebruikt. |
| U gebruikt door connector geëxporteerde LT en vertrouwt op een vast aantal kolommen of een specifieke positie in de laatste kolom | Aan het einde van het rapport wordt een nieuwe kolom toegevoegd. | Ja. Pas de parserings- of validatielogica aan om rekening te houden met een extra kolom aan het einde van het bestand. |
| U gebruikt door connector geëxporteerde LT en kaart op kolomnaam | Er is een nieuwe kolom Opmerkingen van Revisor beschikbaar. | Optioneel. U hoeft niets te wijzigen, tenzij u de nieuwe reviewer/checklist met opmerkingen wilt gebruiken. |

**wat u** zou moeten doen

* Bekijk alle scripts, ETL-taken, dashboards of integraties die gebruikmaken van beheertranscriptrapporten.
* Als u de oude kolomnaam _commentaar van de Voorlegging_ van verwijzingen voorziet, werk uw configuratie of code bij om de nieuwe opmerkingen van de recensent van de kolomnaam te gebruiken.
* Als u op connector gebaseerde LT-exports gebruikt en ervan uitgaat dat er een vast aantal kolommen of een vaste laatste kolom is, moet u uw logica bijwerken om een extra kolom aan het einde van de export te verwerken.

Als uw huidige implementatie uitsluitend gebaseerd is op kolomposities in Admin LT en niet valideert of afhangt van de kolomkoptekst, hoeft de LT-beheerder zelf niets te wijzigen. Alleen connector-exports hebben aandacht nodig wanneer u afhankelijk bent van een vaste indeling.


## Niet-aangemelde ervaring in Experience Builder

Dankzij de niet-aangemelde ervaring in Experience Builder kunnen organisaties hun leerinhoud en portalpagina&#39;s weergeven aan alle bezoekers, ook aan bezoekers die zich niet hebben aangemeld. Deze functie is ontworpen om toekomstige studenten aan te trekken, te informeren en te boeien door een soepele en branded voorvertoning van uw trainingsaanbiedingen te bieden voordat ze zich hoeven aan te melden of zich in te schrijven.

Met deze functie kunt u openbare pagina&#39;s maken en aanpassen met dezelfde gebruikersvriendelijke interface voor slepen en neerzetten als in de standaard Experience Builder. U kunt cursuscatalogi, categorieën, paden en rijke statische inhoud, inclusief afbeeldingen, tekst, HTML en ingesloten iframes, weergeven voor iedereen die uw portal bezoekt. Zo kun je eenvoudig je leerprogramma’s benadrukken, nieuwe cursussen promoten en essentiële informatie bieden aan een breder publiek.

Bezoekers kunnen door de catalogus bladeren, details over cursussen en instanties bekijken en de algemene zoekopdracht gebruiken om beschikbare trainingsmogelijkheden te verkennen. Voor handelingen waarvoor de identiteit van een gebruiker vereist is, zoals inschrijving in een cursus, toegang tot gepersonaliseerde functies (zoals agenda, naleving, leaderboard of Sociaal leren) of volgen van training, wordt de bezoeker echter gevraagd zich aan te melden. Deze benadering zorgt ervoor dat gevoelige en gepersonaliseerde informatie veilig blijft, terwijl een uitgebreide voorvertoning mogelijk blijft.

Beheerders kunnen configureren welke pagina&#39;s en widgets zichtbaar zijn voor gebruikers die zich niet hebben aangemeld, zodat alleen geschikte inhoud wordt weergegeven. Pagina&#39;s kunnen worden ingesteld om toegankelijk te zijn voor zowel aangemelde als niet-aangemelde gebruikers, of uitsluitend voor een van deze groepen. De Experience Builder beschikt over een voorbeeldmodus waarmee u precies kunt zien hoe uw pagina&#39;s aan bezoekers worden weergegeven voordat ze worden gepubliceerd.

Om deze functie in te schakelen, moet uw ALM-integratiebeheerder de connector voor toegang tot trainingsgegevens activeren. Deze connector zorgt ervoor dat de metagegevens van de cursus openbaar toegankelijk zijn.

Branding en lokalisatie worden volledig ondersteund, zodat u paginatitels, favicons en taalinstellingen kunt aanpassen aan de identiteit van uw organisatie en aan de behoeften van uw doelgroep kunt voldoen. Als onderdeel van de overgang naar deze verbeterde ervaring, is de verouderde homepage-functie voor niet-aangemelde gebruikers verouderd. Daarom moet alle nieuwe openbare inhoud worden gemaakt met Experience Builder.

### Doel van de functie

Dankzij de niet-aangemelde ervaring in Experience Builder kunnen organisaties hun leerinhoud en portalpagina&#39;s aan iedereen tonen, zonder dat gebruikers zich hoeven aan te melden. Dit helpt potentiële studenten aan te trekken, te informeren en te boeien door een voorvertoning van de beschikbare training en bronnen te leveren voordat inschrijving of verificatie nodig is.

### Gebruiksscenario’s in de praktijk voor niet-aangemelde ervaringen

* **Marketing en outreach**: De organisaties kunnen hun opleidingsprogramma&#39;s aan externe doelgroepen, zoals potentiële klanten, partners, of baanaanvragers, bevorderen door cursuscatalogi en programmadetails openbaar toegankelijk te maken.
* **Verkenning van de pre-inschrijving**: De studenten kunnen beschikbare cursussen doorbladeren, overzichten bekijken, en categorieën onderzoeken alvorens te beslissen om zich aan te melden of aan te melden, hen helpen geïnformeerde inschrijvingsbesluiten nemen.
* **Collectieve opleidingsportals**: De bedrijven kunnen een openbaar-onder ogen ziend portaal voor naleving of onboardinginformatie verstrekken, toestaand nieuwe huurders of contractanten om te zien welke opleiding beschikbaar is alvorens zij geloofsbrieven ontvangen.
* **Gebeurtenis of campagne landende pagina&#39;s**: De organisaties die het leren campagnes of gebeurtenissen in werking stellen kunnen specifieke openbare pagina&#39;s tot stand brengen om gespiegelde cursussen, programma&#39;s, of middelen te benadrukken, die zicht en betrokkenheid verhogen.
* **SEO en vindbaarheid**: Door geselecteerde pagina&#39;s en catalogi openbaar te maken, verbeteren de organisaties hun zicht van het onderzoeksmotor, die mensen helpen om hun het leren online aanbieden te ontdekken.

### Belangrijke concepten van niet-aangemelde ervaring

Dankzij de niet-aangemelde ervaring van Experience Builder kun je leerinhoud en portalpagina’s publiekelijk presenteren, zodat bezoekers kunnen bladeren zonder zich aan te melden.

* **creeer openbare pagina&#39;s en menu&#39;s**: U opstelling pagina&#39;s en één enkel menu dat iedereen, ongeacht login status kan toegang hebben.
* **voeg slechts gesteunde widgets** toe: U omvat widgets die geen gebruikerscontext (categorieën, cursussen en leerwegen, inhoudsdoos, HTML, iframe) nodig hebben, terwijl het systeem gebruiker-specifieke widgets verbergt.
* **vorm adaptief paginagedrag**: U besluit als een pagina voor zowel het programma geopende als niet het programma geopende gebruikers verschijnt, en het systeem past zichtbare widgets en inhoud aan die op login staat wordt gebaseerd.
* **Voorproef beide ervaringen**: U gebruikt voorproefopties om te zien hoe de pagina&#39;s voor het programma geopende en niet het programma geopende gebruikers, met verschillen in widgetzicht en inhoud kijken.
* **laat globaal onderzoek** toe: Bezoekers zoeken naar cursussen en inhoud, maar krijgen slechts basisonderzoekseigenschappen zonder geavanceerde integratie AI.
* **laat bezoekers doorbladeren catalogus en cursusoverzichten**: Bezoekers onderzoeken cataloguspagina&#39;s, cursusdetails, en instanties, maar moeten login om gepersonaliseerde eigenschappen in te schrijven of toegang te hebben.
* **pas branding en lokalisatie** aan: U plaatst favicons, en taalmontages om de branding en toegankelijkheidsbehoeften van uw organisatie aan te passen.
* **laat de Schakelaar van de Toegang van de Gegevens van de Opleiding toe**: U activeert deze schakelaar om cursusmeta-gegevens voor openbare vertoning uit te voeren, die niet-het programma geopende pagina&#39;s bijgewerkt houden.
* **Handvat hoog verkeer met gedeelde infrastructuur**: Het systeem beheert grote volumes van anonieme bezoekers gebruikend gedeelde middelen en tarief het beperken.
* **optimaliseer voor SEO**: Het platform bereidt openbare pagina&#39;s voor het indexeren van de onderzoeksmotor voor, die uw het leren inhoud gemakkelijker maken te vinden.

### Vereisten voor niet-aangemelde ervaring

* U moet de connector voor toegang tot trainingsgegevens inschakelen in de integratiebeheerder voordat u de niet-aangemelde ervaring kunt gebruiken.
* De connector exporteert cursusmetagegevens naar een openbare opslagplaats, zodat niet-aangemelde pagina&#39;s worden bijgewerkt.

#### initialisatie van de connector Trainingsgegevenstoegang

De TDA-connector (Training Data Access) is een essentiële voorwaarde voor het inschakelen van de nieuwe functie voor het niet-aanmelden van ervaringenbouwers in ALM. Deze connector vereenvoudigt het exporteren van trainingsmetagegevens, zodat uw portal cursusinformatie kan weergeven voor gebruikers die zich niet hebben aangemeld.

* **activatie van de Verbinding**: U moet de schakelaar TDA van het integratiebeheerpaneel toelaten. Met deze stap wordt de functionaliteit van de niet-aangemelde ervaringenbouwer ingeschakeld en worden relevante UI-opties zichtbaar in uw beheerinterface.
* **de uitvoer van Meta-gegevens**: Zodra geactiveerd, voert de schakelaar essentiële opleidingsmeta-gegevens (zoals cursusnaam, beschrijving, overzicht, classificatie, duur, en vaardigheden) van ALM naar een openbare bewaarplaats uit. Deze gegevens worden gebruikt om niet-aangemelde pagina&#39;s en widgets te vullen.
* **Plannend en synchronisatie**: Het de uitvoerproces kan (bijvoorbeeld, dagelijks) worden gepland om uw portaal te verzekeren wijst op de recentste cursusupdates. Wijzigingen in ALM worden na de volgende exportcyclus op de niet-aangemelde pagina&#39;s weergegeven, afhankelijk van caching en exportfrequentie.
* **beschikbaarheid van de Eigenschap**: De niet-het programma geopende eigenschappen van de ervaringenbouwer, met inbegrip van menuverwezenlijking, widget steun, en cataloguszicht, zijn slechts toegankelijk nadat de schakelaar TDA wordt geïnitialiseerd. Als de connector niet is ingeschakeld, blijft uw ervaringenbouwer beperkt tot aangemelde gebruikersscenario&#39;s.
* **Migratie en steun**: Voor rekeningen die van erfenis niet-geregistreerde homepage eigenschappen overgaan, is het initialiseren van de schakelaar TDA de eerste stap naar migratie. Zo kun je gebruikmaken van de flexibiliteit en verbeterde mogelijkheden van de nieuwe ervaringenbouwer.


### Wat bezoekers kunnen doen zonder zich aan te melden

Bezoekers kunnen op een niet-aangemelde Experience Builder-site door de trainingscatalogus bladeren door de cataloguspagina voor openbare catalogi te openen. Ze kunnen filters gebruiken zoals catalogus, product, rol, type, vaardigheden en tags, afhankelijk van de manier waarop u de site hebt geconfigureerd. Bezoekers kunnen ook naar trainingen zoeken met de algemene zoekbalk in de koptekst (indien ingeschakeld) en de zoekresultaten rechtstreeks op de cataloguspagina bekijken.

Bezoekers kunnen de trainingsdetails bekijken door overzichtspagina&#39;s voor cursussen, leerpaden en certificeringen te openen. Op deze pagina&#39;s worden de belangrijkste metagegevens weergegeven, zoals de titel, beschrijving, auteur, duur, indeling, tags en vaardigheden.

Bovendien kunnen bezoekers statische en promotionele content verkennen. Ze kunnen tekst en rijke contentblokken lezen, banners en afbeeldingstegels weergeven en werken met ingesloten iframes zoals externe microsites, video&#39;s of gereedschappen.

Als een bezoeker op Inschrijven klikt of de training probeert te starten, vraagt het systeem hen zich aan te melden of zich aan te melden. Na geslaagde aanmelding wordt de bezoeker omgeleid naar de juiste pagina, ongeacht of het de startpagina, een aangepaste pagina of de specifieke training betreft die hij of zij heeft geselecteerd.

### Wat niet beschikbaar is zonder aanmelden

Op een niet-aangemelde Experience Builder-site hebben bezoekers geen toegang tot functies of inhoud waarvoor gebruikersverificatie is vereist. Ze kunnen zich niet inschrijven voor trainingen, cursussen starten of volgen of toegang krijgen tot gepersonaliseerde widgets zoals Mijn leerervaring, Kalender, Naleving, Leaderboard of Sociaal leren. Deze widgets zijn afhankelijk van gebruikersspecifieke gegevens en zijn alleen beschikbaar nadat u zich hebt aangemeld.

Bezoekers kunnen ook geen handelingen uitvoeren zoals het inschrijven in een cursus of het benaderen van inhoud waarvoor de voortgang of de context van de gebruiker moet worden gevolgd. Wanneer wordt geprobeerd om zich in te schrijven of een training te starten, wordt de bezoeker gevraagd zich aan te melden of zich aan te melden voordat hij verdergaat.

### Ondersteunde widgets in niet-aangemelde modus

In de niet-aangemelde modus worden alleen widgets ondersteund waarvoor geen gebruikersspecifieke gegevens nodig zijn. Deze omvatten:

* Categoriewidget waarin beschikbare trainingscategorieën worden weergegeven.
* Widget Cursussen en paden, waarin cursussen en leerpaden uit de openbare catalogus worden weergegeven.
* Inhoudsvak, voor het toevoegen van statische tekst, afbeeldingen of promotionele inhoud.
* HTML-widget, voor het insluiten van aangepaste HTML-inhoud.
* iFrame-widget, voor het weergeven van externe sites, video&#39;s of gereedschappen op de pagina.
* Widgets die gebruikerscontext vereisen, zoals Mijn leerervaring, Kalender, Naleving, Leaderboard en Sociaal leren, zijn niet beschikbaar in de niet-aangemelde modus.

### Pagina&#39;s en menu&#39;s in niet-aangemelde ervaring

* Er wordt slechts één niet-aangemeld menu ondersteund, dat zonder verificatie zichtbaar is voor alle bezoekers.
* U kunt pagina&#39;s toevoegen aan zowel aangemelde als niet-aangemelde menu&#39;s. Als een pagina zich in beide menu&#39;s bevindt, worden de widgets en inhoud aangepast op basis van de aanmeldingsstatus van de gebruiker.
* Niet-aangemelde menu&#39;s bieden geen doelgroeptargeting of personalisatie. Iedereen ziet dezelfde set pagina&#39;s.
* Widgets die niet worden ondersteund in de niet-aangemelde modus worden automatisch verborgen. De paginalay-out wordt aangepast om tussenruimten op te vullen.
* Menu- en paginabeheer (toevoegen, voorvertonen, verwijderen) lijkt op de aanmeldingsmodus, maar met aanpassingen voor niet-aangemelde beperkingen.

### Gedrag van zoeken en catalogi

In de niet-aangemelde modus kunnen gebruikers de cataloguspagina openen en met de zoekfunctie door beschikbare cursussen en leerpaden bladeren. Op de cataloguspagina worden alle openbare cursussen weergegeven, samen met filters en zoekfunctionaliteit, waarbij dezelfde accountinstellingen worden gevolgd als in de aanmeldingsmodus. Wanneer een gebruiker zoekt, worden de resultaten op de cataloguspagina weergegeven en kunnen gebruikers de pagina&#39;s met het overzicht van de cursus en de instantie weergeven zonder zich aan te melden. Voor acties zoals inschrijving moet u zich echter aanmelden.

Als een gebruiker zich probeert in te schrijven, moet de gebruiker zich eerst aanmelden. Het zoeken naar niet-aangemelde gebruikers is eenvoudiger dan het zoeken naar aangemelde gebruikers en biedt geen geavanceerde functies zoals AI Assistant-integratie.

### Technische implementatie

#### Setup connector voor toegang tot trainingsgegevens

U moet de connector voor toegang tot trainingsgegevens inschakelen in het deelvenster voor integratiebeheer voordat u de functie voor het niet-aanmelden van de ervaringenbouwer kunt gebruiken. Deze connector exporteert trainingsmetagegevens van ALM naar een openbare opslagplaats, zodat deze toegankelijk zijn via API&#39;s voor uw niet-aangemelde pagina&#39;s. De verbindingsopstelling is een eerste vereiste voor het activeren van de eigenschap en zorgt ervoor dat uw portaal bijgewerkte trainingsinformatie toont.

#### Metagegevens exporteren en synchroniseren

De connector exporteert belangrijke metagegevensvelden zoals cursusnaam, overzicht, beschrijving, beoordeling, duur en vaardigheden. U kunt de export (bijvoorbeeld dagelijks) plannen om uw portal synchroon te houden met ALM. Mogelijk worden niet alle metagegevensvelden opgenomen. Raadpleeg de technische documentatie voor een volledige lijst. Geëxporteerde gegevens worden gebruikt om niet-aangemelde pagina&#39;s te vullen en wijzigingen in ALM worden na de volgende exportcyclus weergegeven.

#### Caching en exportfrequentie

Het systeem gebruikt back-end exportfrequentie en front-end caching om gegevensupdates te beheren. Wijzigingen in ALM worden weerspiegeld in uw portal nadat de geplande export en cache zijn vernieuwd. Sommige updates worden mogelijk niet onmiddellijk weergegeven als gevolg van deze mechanismen. Als u snellere updates nodig hebt, past u het exportschema aan of wist u de cache wanneer dat nodig is.

#### Ondersteuning voor CSS/JS-aanpassing

Met het tabblad Aanpassing kunt u aangepaste CSS en JavaScript toepassen op zowel aangemelde als niet-aangemelde pagina&#39;s. Zo kunt u consistente branding behouden, aangepaste UI-elementen toevoegen en de gebruikerservaring in uw portal verbeteren. Alle aanpassingen worden wereldwijd toegepast, zodat je een uniform uiterlijk hebt.

#### URL-verschillen en branding (favicon, paginatitel)

Niet-aangemelde en aangemelde pagina&#39;s kunnen verschillende URL&#39;s hebben om de gebruikersstatus te onderscheiden. U kunt het favicon en de paginatitel voor uw portal aanpassen en zo uw merkidentiteit versterken. Deze functies zijn beschikbaar in de ervaringenbouwer; raadpleeg engineering voor de nieuwste status op niet-aangemelde ondersteuning.

### Prestaties en schaalbaarheid

#### Gedeelde stapel versus premium stapel

De gedeelde stapel staat veelvoudige klanten toe om de niet-het programma geopende ervaringenbouwer op gemeenschappelijke infrastructuur te gebruiken, ondersteunend standaardverkeersniveaus. De premium stack is een betaalde optie die speciale resources, real-time functies en hogere licentielimieten biedt voor klanten met geavanceerde behoeften. Selecteer de stapel op basis van uw verwachte verkeer en bedrijfsvereisten.

#### Verkeersbeperkingen en snelheidsbeperking

De gedeelde stapel dwingt verkeersbeperkingen af om een eerlijk gebruik door klanten te waarborgen. De techniek zal tarief het beperken uitvoeren om het even welke enige klant te verhinderen alle middelen te verbruiken. Als je marketingcampagnes plant of veel verkeer verwacht, kun je coördineren met technische voorzieningen om inzicht te krijgen in je beperkingen en om onderbreking van de service te voorkomen. Snelheidsbeperking helpt bij het handhaven van systeemstabiliteit en -prestaties voor alle gebruikers.

#### Overwegingen met betrekking tot meervoudig gebruik en SEO

Het platform biedt ondersteuning voor meerdere huurders, zodat meerdere klanten hun portals kunnen hosten op een gedeelde infrastructuur. Niet-aangemelde pagina&#39;s zijn SEO-vriendelijk, samen met sitemap.xml en robots.txt om de zichtbaarheid van zoekprogramma&#39;s te optimaliseren. Zo zorg je dat je portal op de juiste manier kan worden ontdekt en geïndexeerd door zoekmachines.

### Migratie en veroudering

#### Overgang van bestaande niet-aangemelde startpagina

Gebruik de nieuwe ervaringenbouwer om uw startpagina opnieuw te maken voor meer flexibiliteit, widgetondersteuning en een verbeterde gebruikerservaring. Het overgangsplan zorgt voor minimale verstoring en voortdurende ondersteuning.

#### Communicatieplan

Klanten die de verouderde startpagina gebruiken, ontvangen duidelijke informatie over de verouderde tijdlijn en migratiestappen. Er wordt ondersteuning geboden om u te helpen uw startpagina over te brengen naar het nieuwe ervaringenbouwerplatform, zodat u kunt profiteren van nieuwe functies en doorlopende updates.

### Ondersteuning voor lokalisatie en aanmelding

#### Logica voor alternatieven voor landinstellingen

Het systeem geeft de pagina&#39;s weer in de landinstelling waarin ze zijn gemaakt. Als de landinstelling van een gebruiker niet beschikbaar is, gebruikt het systeem een fallback-logica om de volgende best beschikbare landinstelling te selecteren. Zo weet u zeker dat gebruikers de inhoud altijd in een ondersteunde taal zien, wat de toegankelijkheid en de tevredenheid van de gebruiker ten goede komt.

#### Ondersteunde aanmeldingstypen

De niet-aangemelde ervaring ondersteunt alle aanmeldingstypen die beschikbaar zijn in ALM, inclusief SSO en standaardaanmelding. Gebruikers kunnen door inhoud bladeren zonder zich aan te melden en worden gevraagd zich aan te melden wanneer dat nodig is, zoals zich inschrijven voor een cursus of toegang krijgen tot gepersonaliseerde functies. Dit zorgt voor een vloeiende overgang van bladeren naar betrokkenheid.


### Niet-aangemelde API&#39;s

#### Admin Learning Object API

Niet-aangemelde Experience Builder-pagina&#39;s en headless portals organiseren of filteren vaak cursussen op basis van product en rol. De LO-API van de beheerder is verbeterd om ervoor te zorgen dat deze koppelingen consistent toegankelijk zijn voor back-end- en headless-integraties en voor de TDA-connector.

**Eindpunt en gedrag**

U kunt het bestaande LO-eindpunt van Admin blijven gebruiken:

```
GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles
```

Waar:

* loId is het leerobject-ID (bijvoorbeeld cursus :12345).
* cedFields [ learningObject ] instrueert API om producten en rollen voor die LO uitdrukkelijk te omvatten.

Dit wordt bereikt door ervoor te zorgen dat de product- en rolverenigingen van de LO aanwezig zijn in de reactie wanneer hierom wordt gevraagd via StandaardFields. Het antwoord bevat vervolgens, in kenmerken, de metagegevens van het product en de rol die nodig zijn om de aanbevolen producten (rec\_products) en rollen (rec\_rollen) voor Experience Builder en andere consumenten te berekenen of beschikbaar te maken.

Een typische vraag van een beheerder of een integratie kijkt als:

```
url -X GET \
 "https://{your-domain}/primeapi/v2/learningObjects/course:12345?enforcedFields[learningObject]=products,roles" \
 -H "Authorization: Bearer {admin\_token}" \
 -H "Accept: application/vnd.api+json
```

De geretourneerde LO JSON is dezelfde basisstructuur als voorheen, maar u kunt er nu op vertrouwen dat er product-/rolvelden aanwezig zijn wanneer u deze vraagt met afgedwongen velden. Integraties die geen gebruik maken van gedwongen velden, gedragen zich nog steeds zoals voorheen.

#### Lijst met leerobjecten - Taakhulpenondersteuning in filter effectiveModifiedDate

**Doel**

De schakelaar van de Toegang van de Gegevens van de Opleiding (TDA) en de headless implementaties moeten vaak stijgende synchronisatie uitvoeren, die op de **efficiënte wijzigingsdatum** van het leren voorwerpen wordt gebaseerd. Tot deze release werden Taakhulpen (LO-type jobAid) niet correct verwerkt in combinatie met de filters effectiveModifiedDate. In deze release is dit gecorrigeerd, zodat taakhulpen stapsgewijs kunnen worden gesynchroniseerd als cursussen en leerpaden.

**Eindpunt en gedrag**

U gebruikt het bestaande eindpunt van de LO-lijst met datumfilters en LO-type:

```
GET /primeapi/v2/learningObjects
 ?filter.effectiveModifiedDate.fromDate=2025-03-15T13:14:56.000Z
 &filter.effectiveModifiedDate.toDate=2025-03-20T13:14:56.000Z
 &filter.loTypes=jobAid
```

Eerder, toen filter.loTypes=jobAid met een effectiefModifiedDate waaier werd gecombineerd, sloot het filter effectief JobAids uit, en de vraag gedraagt zich alsof niet JobAids werd gesteund.

Vanaf deze update retourneert de aanroep alleen JobAid-leerobjecten waarvan de effectiveModifiedDate binnen het opgegeven venster valt.

```
{
 "links": {
 "self": "https://acapapiserver/primeapi/v2/learningObjects?page[limit]=10&filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z&filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z&filter.loTypes=jobAid"
 },
 "data": [
 {
 "id": "jobAid:144968",
 "type": "learningObject",
 "attributes": {
 "authorNames": ["Author"],
 "dateCreated": "2026-01-20T08:48:55.000Z",
 "datePublished": "2026-01-20T08:48:55.000Z",
 "dateUpdated": "2026-01-20T08:48:55.000Z",
 "effectiveModifiedDate": "2026-01-05T07:31:18.000Z",
 "loType": "jobAid",
 "loFormat": "Content",
 "loResourceType": "Content",
 "localizedMetadata": [
 {
 "description": "Link jobAid new",
 "locale": "en-US",
 "name": "Link jobAid new"
 },
 {
 "description": "Link jobAid new fre",
 "locale": "fr-FR",
 "name": "Link jobAid new fre"
 }
 ],
 "relationships": {
 "authors": {
 "data": [
 { "id": "13385176", "type": "user" }
 ]
 },
 "instances": {
 "data": [
 { "id": "jobAid:144891\_-1", "type": "learningObjectInstance" }
 ]
 }
 }
 }
 }
 ]
}
```

Dit betekent dat u nu veilig incrementele JobAid-synchronisaties kunt implementeren op basis van effectiveModifiedDate, op dezelfde manier als u dat al doet voor andere typen.

Als u filter.loTypes=jobAid weglaat, is het gedrag voor andere types LO onveranderd; de verandering beïnvloedt slechts de combinatie van JobAid met dat filter.

#### **Menu API: Niet-het programma geopend menusilter**

**Doel**

De Bouwer van de ervaring en de headless frontends hebben een ongecompliceerde manier nodig om **niet-het programma geopend menu** terug te winnen, dat navigatie voor openbare bezoekers bepaalt. Voor deze release moest u alle menu&#39;s ophalen en vervolgens aangepaste logica toepassen om te bepalen welke van de niet-aangemelde navigatie de naam heeft. Deze versie voegt een eenvoudig serverfilter toe.

**Eindpunt en gedrag**

U gebruikt het bestaande eindpunt van de menulijst met een nieuwe queryparameter:

```
GET /primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true
```

De belangrijkste punten:

* include=pages,subMenus.pages is optioneel maar wordt aanbevolen wanneer u de pagina- en submenu-paginagegevens in hetzelfde antwoord nodig hebt.
* isNonLoggedIn=true is nieuw in deze release en geeft de server de opdracht alleen menu&#39;s te retourneren die zijn gemarkeerd als niet-aangemelde menu&#39;s.

Zonder de parameter isNonLoggedIn gedraagt het eindpunt zich precies zoals voorheen en retourneert het menu&#39;s volgens het bestaande standaardgedrag. Met isNonLoggedIn=true, keert het typisch het enige menu terug dat door de niet-het programma geopende ervaring voor uw rekening wordt gebruikt (aangezien er normaal één niet-het programma geopend menu per rekening is).

In de praktijk kan een klant nu de volgende uitgaven doen:

```
curl -X GET \
 "https://{your-domain}/primeapi/v2/templates/menus?include=pages,subMenus.pages&isNonLoggedIn=true" \
 -H "Authorization: Bearer {admin\_token}" \
 -H "Accept: application/vnd.api+json"
```

en krijg de niet-aangemelde navigatiestructuur terug in één aanroep, met alle pagina&#39;s die zichtbaar moeten zijn voor anonieme bezoekers.

Dit is met name handig wanneer u een headless niet-aangemelde site maakt en dezelfde navigatie wilt spiegelen die door Experience Builder wordt gebruikt, of wanneer u fouten opspoort in het niet-aangemelde menu dat correct is geconfigureerd.

### Lijst met aangepaste domeinen toestaan

De niet-aangemelde stapel bestaat uit:

* Een openbaar CDN-domein (bijvoorbeeld cpcontents.adobe.com of yourdomain.example.com) dat lay-outs, config JSON en statische elementen bevat.
* Een openbaar Elasticsearch (ES) eindpunt dat catalogus en onderzoeksgegevens dient, maar slechts als het verzoek uit een **toe:staan-vermeld domein** voor die rekening ALM komt.

Wanneer u een aangepast domein introduceert, werkt het naadloos zonder extra inspanning na het bestaande proces om een douanedomein toe te voegen.

#### Vereisten

Voordat u een aangepast domein op de whitelist plaatst voor een niet-aangemelde toepassing:

1. Het aangepaste domein wordt geconfigureerd voor uw ALM-account (bijvoorbeeld DNS voor academy.yourcompany.com punten naar Adobe/Akamai en certificaten worden ingericht).
2. De **schakelaar van de Toegang van de Gegevens van de Opleiding (TDA)** wordt toegelaten voor de rekening.
3. De **niet-het programma geopende eigenschap van de Bouwer van de Ervaring** wordt toegelaten (Adobe-kant).

Deze stappen zorgen ervoor dat:

* Uw rekening heeft een niet-het programma geopend **rekening JSON** (die vaak als accountConfig/experienceBuilderConfig) wordt van verwijzingen voorzien, die gebieden zoals cpDomain, almDomain, almCdnBaseUrl, esBaseUrl, en toe:staan-vermeld domeinen omvat.
* De niet-aangemelde stapel weet waar gegevens moeten worden aangeboden en van welke domeinen de stapel aanvragen moet accepteren.

#### Hoe het toestaan van lijsten werkt

De allow-list wordt opgeslagen in de configuratie die de uitvoer TDA en de niet-het programma geopende stapel leest. Deze configuratie omvat:

* De ALM-domeinen (cpDomain, almDomain).
* De **CDN basis URL** voor niet-het programma geopende inhoud (almCdnBaseUrl).
* De **openbare onderzoeksbasis URL** (esBaseUrl).
* De lijst met domeinen die openbare niet-aangemelde aanroepen voor dat account mogen maken.

Als u wilt dat niet-aangemelde Experience Builder werkt aan een aangepast domein:

* De browser moet de niet-aangemelde HTML uit dat aangepaste domein laden (of uit het niet-aangemelde ALM-CDN-domein, afhankelijk van uw instelling).
* Oproepen van dat domein aan het openbare ES en eindpunten CDN moeten worden goedgekeurd. Dat gebeurt alleen als het domein voorkomt in de lijst allow-list.

Deze versie voegt een nieuw niet-geregistreerd-in CDN domein, cpcontents.adobe.com toe, en specificeert dat het in de **toe:staan-lijst domeinen** in de schakelaar TDA moet worden geplaatst. Voor bestaande niet-aangemelde native gebruikers is een update vereist.

#### Een aangepast domein toestaan

**vorm het douanedomein in ALM**

Werk met Adobe om uw domein te registreren, bijvoorbeeld academy.yourcompany.com, als het aangepaste domein voor uw ALM-account. U werkt DNS bij om aan Adobe Akamai te wijzen zoals geïnstrueerd en op SSL en het verpletteren te wachten om te voltooien.

Op dit punt, zowel kan het het programma geopende als niet-het programma geopende verkeer ALM door dat domein bereiken, maar het niet-het programma geopende onderzoek en catalogusvraag kunnen nog worden geblokkeerd als het domein niet toe:staan-vermeld is.

**laat TDA en niet-het programma geopende Bouwer van de Ervaring toe**

Zorg ervoor dat:

* De **schakelaar van de Toegang van de Gegevens van de Opleiding** wordt toegelaten.
* De **niet-het programma geopende eigenschap van de Bouwer van de Ervaring** wordt aangezet voor de rekening.

Als u TDA inschakelt, wordt het niet-aangemelde JSON-account gemaakt of bijgewerkt. Voor nieuwe rekeningen, staat het proces ook toe-maakt een lijst van het nieuwe niet-het programma geopende CDN domein (cpcontent.adobe.com) door gebrek, zodat verwacht het openbare ES eindpunt vraag van dat domein.

Voor accounts die al gebruikmaken van de oudere, niet-aangemelde stapel, moeten bestaande connectoren worden verwijderd en opnieuw worden gemaakt om het nieuwe domein op te halen.

**voeg het douanedomein aan toe toestaan-lijst**

Het kritieke deel is het vertellen van de niet-het programma geopende stapel ES dat academy.yourcompany.com een goedgekeurde oorsprong is. Er zijn twee algemene paden.

1. **re-laat de schakelaar TDA (eenvoudig, zelf-dienstvriendelijk)** toe

Bestaande native niet-aangemelde gebruikers moeten de TDA-verbinding verwijderen en opnieuw inschakelen, zodat het nieuwe domein automatisch wordt weergegeven op de lijst met toegestane items. Hiervoor zijn twee dingen mogelijk:

1. Het niet-aangemelde account JSON wordt opnieuw gegenereerd.
2. De domeinen die op de lijst staan, worden bijgewerkt met het nieuwe CDN-domein zonder aanmelding en uw aangepaste domein.

Dit wordt aanbevolen als u een klein aantal accounts hebt en tijdelijk de connector uitschakelt en weer inschakelt.

1. **Verifieer dat het domein eigenlijk toe:staan-vermeld** is

Na het toestaan-lijst, open uw niet-geregistreerde plaats op het douanedomein en inspecteer de vraag van het browser netwerk.

U wilt zien:

* Verzoeken om almCdnBaseUrl (bijvoorbeeld <https://cpcontent.adobe.com/>...) succesvol met 200/304.
* Verzoeken om esBaseUrl (openbare zoek-API, bijvoorbeeld <https://primeapps.adobe.com/almsearch/api/v1/>..) JSON met zoek-/catalogusgegevens weer te geven.

Als deze aanroepen 4xx-fouten of expliciete fouten retourneren die &#39;niet-vertrouwd domein&#39; of &#39;oorsprong niet toegestaan&#39; suggereren, is de allow-list onvolledig of onjuist geconfigureerd en moet de ondersteuning deze aanpassen.

De niet-aangemelde LLD merkt ook op dat de accountconfiguratie een verwachte domeinwaarde kan bevatten. Tijdens runtime controleert de site of het domein in de URL overeenkomt met wat in de configuratie is ingesteld. Als dit niet het geval is, kan de gebruiker worden omgeleid naar een foutpagina. Dit beschermt tegen toegang tot de configuratie van een klant via het domein van een andere klant.

### Aanbevelingen gebruiken in de niet-aangemelde Experience Builder

Met de niet-aangemelde Experience Builder kunt u openbare leerpagina&#39;s maken waar bezoekers door uw catalogus kunnen bladeren en gemarkeerde inhoud kunnen zien voordat ze zich aanmelden. Hoewel deze bezoekers anoniem zijn, kunt u aanbevolen trainingen toch presenteren met behulp van metagegevens en widgets.

In de aangemelde Learner-app kunnen aanbevelingen worden gepersonaliseerd: deze kunnen afhankelijk zijn van het profiel, de geschiedenis, de vaardigheden en de voortgang van de student. In de **niet-het programma geopend** ervaring, is er nog geen studentidentiteit, zodat kan het platform niet personaliseren per gebruiker.

Recommendations in niet-aangemelde modus is daarom:

* **gekromde of op regel-gebaseerd**: gebaseerd op catalogus, product, rol, etiketten, markeringen, en andere meta-gegevens.
* **segment-georiënteerd**: &quot;geadviseerd voor ontwikkelaars&quot;, &quot;geadviseerd voor partners&quot;, &quot;gefeatureerd voor beginners&quot;.
* **marketing-geconcentreerd**: gebruikt om bezoekers aan te trekken en te leiden om in te schrijven zodra zij login.

### Metagegevens en API&#39;s die aanbevelingen ondersteunen

Achter de schermen gebruiken niet-aangemelde pagina&#39;s:

* De **schakelaar TDA** om het leren objecten meta-gegevens (cursussen, wegen, certificeringen, taakhulpen) naar een openbare onderzoeksindex uit te voeren.
* De **openbare onderzoeksstapel** om vragen van niet-het programma geopende widgets (catalogus, onderzoek, Cursussen en wegen, Categorieën) te beantwoorden.
* De **Admin die Objecten API** leren om product en rolmeta-gegevens bloot te stellen die voor aanbevelingsregels kunnen worden gebruikt.

In deze release is de LO-API van de beheerder uitgebreid, zodat de product- en rolkoppelingen betrouwbaar beschikbaar zijn:

```
GET /primeapi/v2/learningObjects/{loId}?enforcedFields[learningObject]=products,roles
```

Hierdoor kunnen widgets en headless integraties op regels gebaseerde aanbevelingen consistent samenstellen met producten, rollen, cataloguslabels, tags en andere velden.

### Aanbevelingssecties ontwerpen met Experience Builder-widgets

U creeert aanbevelingssecties op niet-het programma geopende pagina&#39;s door **widgets van de Bouwer van de Ervaring** met meta-gegevensfilters te combineren.

#### **Cursussen en Widget van Wegen**

Gebruik de **Cursussen en Wegen** widget wanneer u een rij of een net van geadviseerde punten wilt tonen. In zijn configuratie kunt u kiezen:

* Welke catalogi moeten worden opgehaald.
* Welke cataloguslabels, producten, rollen of tags als filters moeten worden gebruikt.
* Of je cursussen, paden, certificeringen, taakhulpen of een mix wilt weergeven.
* Sorteren en maximumaantal items.

U kunt bijvoorbeeld het volgende maken:

* &quot;Aanbevolen voor ontwikkelaars&quot;: filteren op een product of rol die u gebruikt voor inhoud voor ontwikkelaars.
* &quot;Begin hier&quot;: filter op een label zoals &quot;Starter&quot; of &quot;Onboarding&quot;.
* &quot;Aanbevolen in dit kwartaal&quot;: filter op een gebonden label zoals aanbevolen-q3-2026.

De widget leert niet van gedrag, maar toont alles wat overeenkomt met de metagegevensregels die u definieert. Vanuit het oogpunt van de bezoeker lijkt het echter op een aanbevelingsstrook.

#### **widget van Categorieën**

Gebruik de **Categorieën** widget om bezoekers te helpen in &quot;geadviseerde&quot;reeksen inhoud navigeren, zelfs als zij uw productnamen niet kennen.

U kunt tegels configureren die elk een segment vertegenwoordigen, zoals:

* &quot;Voor beheerders&quot;
* &quot;Voor verkoopteams&quot;
* &quot;Voor partners&quot;
* &quot;Op productlijn&quot;

Elke tegel kan worden gekoppeld aan:

* Een gefilterde cataloguspagina (bijvoorbeeld de catalogus die is gefilterd op bepaalde producten of labels).
* Een speciale, niet-aangemelde pagina die vooraf geconfigureerde cursussen en paden voor dat segment gebruikt.

Zo beschik je over een ‘aanbevolen paden per segment’-ervaring zonder personalisatie.

### Op segmenten gebaseerde aanbevelingen maken

Omdat de niet-geregistreerde bezoekers geen profiel ALM nog hebben, is het nuttig om aanbevelingen **door segment** te ontwerpen en bezoekers te laten zelf-selecteren.

1. Gebruik a **niet-het programma geopende homepage** die kort verklaart wie uw academie voor is en een klein aantal punten van de segmentingang toont (bijvoorbeeld, &quot;Ontwikkelaars&quot;, &quot;Marketeers&quot;, &quot;Partners&quot;, &quot;Nieuwe werknemers&quot;). U kunt dit doen met een widget Categorieën of een eenvoudig vak Inhoud of een sectie HTML met knoppen.
2. Voor elk segment, creeer a **gewijde niet-het programma geopende pagina** in de Bouwer van de Ervaring. Op die pagina gebruikt u een of meer widgets Cursussen en paden die zijn geconfigureerd met filters die aangeven wat &quot;aanbevolen&quot; is voor die groep. Voor &quot;Ontwikkelaars&quot; kunt u bijvoorbeeld filteren op:
   1. Catalogus = &quot;Openbare training&quot;
   2. Product = &quot;Adobe Experience Manager&quot;
   3. Tags = &quot;Basisbegrippen voor ontwikkelaars&quot;
3. Gebruik die segmentpagina&#39;s als het doel van uw marketingcampagnes en als het doel van de tegels op de niet-aangemelde introductiepagina.

Bezoekers zien dat ze aanbevelingen zien die zijn toegesneden op hun situatie, ook al is de logica in de ontwerpfase vastgelegd via metagegevens.

### Overstappen van niet-aangemelde naar gepersonaliseerde aanbevelingen

Niet-het programma geopende aanbevelingen zijn hoofdzakelijk over **vindbaarheid** en **omzetting**. Wanneer bezoekers besluiten zich in te schrijven of te beginnen met de training, zullen ze zich aanmelden en volledige studenten met een profiel en geschiedenis worden.

De gebruikelijke stroom is:

1. Een bezoeker ontdekt inhoud door uw niet-het programma geopende aanbevelingssecties (huisaanbevelingen, segmentlandingspagina&#39;s, aanbevolen rijen).
2. Ze klikken in een cursus- of padoverzicht en kiezen ervoor in te schrijven of te starten.
3. ALM vraagt hen zich aan te melden of zich aan te melden.
4. Nadat ze zich hebben aangemeld, neemt de standaard aangemelde leerervaring de overhand, waaronder:
   1. &quot;Mijn leerervaring&quot;
   2. Inlogcatalogus met persoonlijke voortgang
   3. Alle interne aanbevelingssystemen die u voor bestaande studenten gebruikt.

Met andere woorden, de aangemelde aanbevelingen helpen hen te beslissen wat ze moeten doen en doorgaan.

### Hoe taakhulpen kunnen worden gebruikt in de nieuwe, niet-aangemelde Experience Builder

Op het **Gebruikersinterface**, nemen de baanhulpmiddelen aan niet-geregistreerde ervaringen hoofdzakelijk door widgets deel die het leren voorwerpen kunnen tonen:

1. **Cursussen en wegen widget**
Deze widget kan meerdere LO-typen weergeven, inclusief taakhulpen. Op niet-aangemelde pagina&#39;s kunt u het volgende configureren:
   1. Voeg taakhulpen expliciet toe of sluit deze uit.
   2. Filter taakhulpen op catalogus, product, rol, labels, tags en andere metagegevens.
   3. Presenteer ze naast cursussen en paden of als een aparte &#39;Bronnen&#39;-strook.

Zo kunt u bijvoorbeeld op een openbare landingspagina een strook met de naam &quot;Nuttige bronnen&quot; configureren die alleen taakhulpen weergeeft, en een andere strook met de naam &quot;Aanbevolen cursussen&quot; die cursussen en paden weergeeft.

1. **pagina van de Catalogus en onderzoek**
De niet-het programma geopende **catalogus** en **onderzoek** oppervlakten gebruiken de openbare onderzoeksindex (die door de schakelaar van de Toegang van de Gegevens van de Opleiding wordt gevoed). Die index ondersteunt nu taakhulpen correct, dus:
   1. Niet-aangemelde zoekresultaten kunnen taakhulpen bevatten.
   2. Filters voor niet-aangemelde catalogus (op type, product, tags, enz.) U kunt taakhulpen opnemen zolang de accountconfiguratie en widgets zo zijn ingesteld dat ze worden weergegeven.
2. **LO overzichtspagina&#39;s**
Wanneer een bezoeker een taakhulp van om het even welke widget of van de catalogus klikt, gaan zij naar een **LO overzichtspagina** voor die baanhulp op niet-het programma geopende wijze. Daar kunnen ze de beschrijving en metagegevens lezen. Voor het downloaden of gebruiken van een taak is doorgaans nog steeds aanmeldingsnaam vereist, maar de aanwezigheid en vindbaarheid van de taakhulp zelf worden afgehandeld door de niet-aangemelde ervaring.

### Hoe taakhulpen worden weergegeven via niet-aangemelde API&#39;s

Op de **API kant**, worden de taakhulpen gesteund door:

1. De **schakelaar van de Toegang van de Gegevens van de Opleiding en openbaar onderzoek**
TDA exporteert metagegevens voor taakhulp samen met andere LO-typen naar de openbare zoekindex die niet-aangemelde zoekopdrachten en catalogusquery&#39;s levert. Hierop vertrouwen Experience Builder en headless frontends.
2. De **het Leren Objecten die met effectiveModifiedDate**
In deze versie is het eindpunt van de LO-lijst gecorrigeerd zodat taakhulpen correct werken met het filter effectiveModifiedDate. U kunt nu bellen:

```
GET /primeapi/v2/learningObjects
 ?filter.effectiveModifiedDate.fromDate=2026-01-19T13:14:56.000Z
 &filter.effectiveModifiedDate.toDate=2026-01-21T13:14:56.000Z
 &filter.loTypes=jobAid
```

Vóór deze wijziging retourneert het combineren van effectiveModifiedDate met loTypes=jobAid geen betrouwbare taakhulpen. Dat betekent:

1. Uw banen TDA of ETL kunnen **banen taakhulpen** voor niet-geregistreerde ervaringen incrementeel synchroniseren, de zelfde manier zij voor cursussen en wegen doen.
2. Elke headless implementatie die een openbare taakhulpenmap maakt, kan wijzigingen opvragen op basis van effectiveModifiedDate en loType=jobAid.

**Nota**:

In de status Niet aangemeld:

* De hulpmiddelen van de baan zijn hoofdzakelijk **vindbaar**: de bezoekers kunnen zien dat zij bestaan, beschrijvingen lezen, en begrijpen hoe zij onderwerpen of cursussen steunen.
* De daadwerkelijke **consumptie** (het downloaden van of het openen van de inhoud van de taakhulp) vereist typisch nog login, vooral als de taakhulpen als deel van vergunning of interne inhoud worden beschouwd.

### Wijzigingen in korte beschrijving in LO-zoekopdracht (niet-aangemeld)

In de niet-aangemelde stapel worden het zoeken naar en het weergeven van leerobjecten (LO&#39;s) aangestuurd door de TDA-connector (Training Data Access) en een openbare Elasticsearch-index. In het verleden werd in deze stapel één overzicht/beschrijvingsveld gebruikt voor elke LO. Klanten die headless niet-aangemelde portals bouwen, wilden dezelfde korte beschrijving op LO-tegels laten zien als de aangemelde interface voor studenten, in plaats van alleen het lange overzicht.

De verandering introduceert steun voor de LO **korte beschrijving** in niet-het programma geopende onderzoek en het van een lijst maken APIs:

* Voor **cursussen**, zijn de bestaande semantiek UI:
* Op inlogkaarten wordt een korte beschrijving (veld van 140 tekens) weergegeven, als deze aanwezig is. Als dit niet het geval is, worden de kaarten teruggezet naar het lange gedetailleerde overzicht.
* Voor **het leren wegen**, gebruikt het het programma geopende UI het gebied van Voordelen als korte beschrijving, als bepaald, en valt terug naar het overzicht anders.
* Voor **certificatie**, wordt een korte Beschrijving gebruikt, met een langer overzicht van de Certificatie als reserve.
* Voor **taakhulpen**, wordt het belangrijkste beschrijvingsgebied gebruikt.

### Andere wijzigingen

#### Beperking dat geen twee accounts hetzelfde aangepaste domein kunnen delen

In de niet-het programma geopende en het programma geopende architectuur van Adobe Learning Manager, wordt het a **douanedomein** (bijvoorbeeld, academy.example.com) behandeld als globaal unieke sleutel die aan precies één rekening moet in kaart brengen ALM, zodat dwingt het platform een harde beperking dat **geen twee rekeningen het zelfde douanedomein** kunnen delen. Dit is vereist voor veiligheid, het verpletteren, en SEO: de verpletterende laag en niet-het programma geopende stapel gebruiken het domein om de correcte rekeningsconfiguratie (met inbegrip van zijn niet-het programma geopende rekening JSON, de menu&#39;s van de Bouwer van de Ervaring, het branding, en TDA/het onderzoek eindpunten) op te zoeken,

Als hetzelfde aangepaste domein op twee accounts wordt toegestaan, is het onmogelijk te garanderen welke accountgegevens worden geretourneerd. Dit kan leiden tot lekkage tussen verschillende tenant-objecten en tot beschadiging van gegenereerde artefacten zoals sitemap.xml en robots.txt die per account worden gemaakt, maar worden ontdekt door zoekmachines per host. Operationeel gezien betekent dit dat wanneer u een aangepast domein toewijst of verplaatst, u er eerst voor moet zorgen dat het niet aan een ander account is gekoppeld (of dat u de registratie daar ongedaan maakt), en dat de interne gereedschappen van de Adobe pogingen om hetzelfde domein aan meerdere accounts te binden, zullen afwijzen.

#### Het in cache plaatsen van bronnen in de niet-aangemelde ervaring

In de niet-gelogde ervaring van Adobe Learning Manager is het in cache plaatsen van bronnen in de browser een kernonderdeel van de strategie voor prestaties en schaal, omdat openbare pagina&#39;s grote, soms scherpe marketingberichten met een lage latentie en een minimale belasting van de oorsprong moeten verwerken. Statische en semi-statische elementen, zoals de niet-aangemelde HTML shell (bijvoorbeeld index.html/guest.html), configuratie op accountniveau JSON (account.json of config.json), Experience Builder-paginalay-out JSON (menu&#39;s, widgetlay-outs, kaartinstellingen), CSS, JS, afbeeldingen en favicons worden aangeboden in een Akamai CDN (cpcontents.adobe.com / cpcontent.adobe.com) met cachekopteksten die beide CDN stimuleren hergebruik aan de zijkant en aan de browser, zodat de browser na het laden van de eerste pagina de volgende niet-aangemelde pagina&#39;s grotendeels kan renderen uit de cache, en alleen opnieuw kan valideren wanneer dat nodig is via ETag of Last-Modified.

## Meertalige taakhulpen

### Inleiding

Met meertalige taakhulpen in Adobe Learning Manager (ALM) kunnen auteurs en beheerders ondersteunende documenten, handleidingen of bronnen in meerdere talen in één taakhulpitem opgeven. Studenten in verschillende regio&#39;s hebben toegang tot relevante materialen in de taal van hun voorkeur, waardoor het begrip, de compatibiliteit en de gebruikerservaring worden verbeterd.

### Vorig gedrag

Eerder werden taakhulpen in ALM ondersteund door slechts één inhoudsbestand per taakhulp, zelfs als de naam en beschrijving konden worden gelokaliseerd. Om dezelfde bron in meerdere talen te bieden, moesten auteurs voor elke taal afzonderlijke taakhulpen maken. Dit leidde tot duplicatie, verwarring en verhoogde administratieve overhead. Er was geen uniforme manier om meertalige middelen te beheren, waardoor het moeilijk was om consistentie te garanderen en het gebruik te volgen.

### Gebruiksscenario&#39;s

* **Globale arbeidskrachtenactivering**: Lever veiligheidshandleidingen, procesgidsen, of verwijzingsdocumenten in veelvoudige talen aan een diverse arbeidskrachten.
* **Regelgevende naleving**: Zorg ervoor alle werknemers de zelfde nalevingsdocumentatie in hun inheemse taal ontvangen.
* **Consistent onboarding**: Verstrek onboardingchecklists of FAQs in lokale talen voor nieuwe hires wereldwijd.
* **Verminderde duplicatie**: beheer alle taalversies van een taakhulp in één enkele ingang, die updates en rapportering vereenvoudigt.

### Belangrijkste kenmerken

* **veelvoudige taalsteun**: Band een uniek dossier of URL voor elke gesteunde taal binnen één enkele taakhulp vast.
* **Gelokaliseerde naam en beschrijving**: ga de naam en de beschrijving van de taakhulp in elke taal in.
* **Verenigd beheer**: geef, werk, en rapport over alle taalversies van één plaats uit.
* **Achterwaartse verenigbaarheid**: De bestaande single-language taakhulpen worden automatisch herhaald over alle toegevoegde talen tot de nieuwe dossiers worden geupload.

### Een meertalige taakhulp maken

1. Ga naar de rol van de Auteur en selecteer **Hulp van de Baan**.
2. Selecteer **creeer Taakhulp**.
3. Voer de naam en beschrijving van de taakhulp in de standaardtaal in.
4. Voeg het primaire inhoudsbestand of de URL voor de standaardtaal toe.
5. Sla de taakhulp op.

### Extra talen toevoegen

1. In de redacteur van de baanhulp, uitgezocht **voeg Taal** toe.
2. Selecteer de gewenste taal of talen in de lijst.
3. Voor elke toegevoegde taal:
   * Voer de gelokaliseerde naam en beschrijving in.
   * Upload het bijbehorende inhoudsbestand of geef een taalspecifieke URL op.
4. Herhaal dit voor alle vereiste talen.

### Talen bewerken en beheren

1. Als u een bestand of beschrijving voor een specifieke taal wilt bijwerken, selecteert u het tabblad Taal en brengt u de gewenste wijzigingen aan.
2. Als een taal wordt toegevoegd nadat de taakhulp is gepubliceerd, wordt het oorspronkelijke bestand automatisch toegewezen aan de nieuwe taal totdat een uniek bestand is geüpload.
3. Verwijder of vervang bestanden voor elke taal zoals vereist.

### Publish en leerervaring

1. Nadat alle talen en bestanden zijn toegevoegd, publiceert u de taakhulp.
2. Studenten zien de taakhulp in hun geselecteerde inhoudstaal, met het juiste bestand of de juiste URL.
3. Als de taal van een student niet beschikbaar is, wordt het standaardtaalbestand weergegeven.

### Rapportage

1. Download taakhulpenrapporten om details weer te geven van alle bestanden en talen die bij elke taakhulp horen.
2. Rapporten bevatten taal, bestandsnaam en gebruiksgegevens voor bijhouden.

### Best practices

* Zorg voor nauwkeurige vertalingen voor namen, beschrijvingen en inhoudsbestanden.
* Reviseer en werk bestanden regelmatig bij om consistentie in verschillende talen te waarborgen.
* Gebruik duidelijke naamconventies om bestanden voor verschillende talen van elkaar te onderscheiden.
* Test de ervaring van de student door van inhoudstalen te wisselen om te controleren of het bestand correct wordt geleverd.

### Problemen oplossen

* **Ontbrekend dossier voor een taal**: Het standaarddossier wordt getoond. Zorg ervoor dat alle talen het juiste bestand hebben geüpload.
* **Verouderde taakhulpen**: Voeg nieuwe taaldossiers toe om automatisch herhaalde originelen te vervangen.
* **Verkeerde getoonde taal**: Controleer de de taalmontages van de de inhoudstaal van de student en de de taalconfiguratie van de taakhulp.

Met meertalige taakhulpen kunt u in één keer ondersteunende hulpmiddelen aan een wereldwijd publiek leveren, duplicatie verminderen en ervoor zorgen dat elke student de juiste informatie in zijn/haar voorkeurstaal ontvangt. Deze functie verbetert de toegankelijkheid, compatibiliteit en administratieve efficiëntie in Adobe Learning Manager.

## Vind antwoorden met AI Assistant voor studenten

AI Assistant voor studenten is een conversationele, AI-gedreven assistent binnen Adobe Learning Manager die je moet begeleiden naar de informatie die je sneller nodig hebt. Door vragen in natuurlijke taal te stellen, krijg je contextuele uitleg, open je relevante cursussen en krijg je inzichten uit leercontent - zonder handmatig door catalogi te bladeren.

### Mogelijkheden

* **Slimme vraag-antwoordend:** behandelt zowel single-turn als multi-turn gesprekken, latend u vragen natuurlijk stellen. Reacties worden afgeleid van cursussen, leerpaden, certificeringen en taakhulpen.
* **inhoud-gegrond antwoorden met citaties:** trekt direct informatie van het leren materialen en omvat citaties die terug naar de originele cursus, de module, of het middel wijzen.
* **Uitgebreide inhoudsverenigbaarheid:** steunt een brede waaier van formaten, met inbegrip van documenten, presentaties, video&#39;s, audiodossiers, de inhoud van de HTML, en de Gedeelde modules van de Verwijzing van de Objecten van de Inhoud van het Model (SCORM).
* **Seamless user experience:** Available as a side panel across learner pages, maintaining session-based chat history for continuity.
* **Robust administrator controls:** Administrators can enable or disable the assistant, limit access by user groups, and choose which internal catalogs are used as the source for AI-generated responses.

### Benefits

* **Faster access to knowledge:** You receive instant answers to your questions, eliminating the need to navigate through multiple courses or documents.
* **Higher engagement:** Conversational interactions make the learning experience more natural, intuitive, and accessible.
* **Better understanding:** You can ask follow-up questions to clarify concepts and explore topics more thoroughly.
* **Scalable learning support:** Automated, AI-driven responses minimize dependence on subject-matter experts and support teams.

Learn more about [AI Assistant for learners](/help/migrated/learners/feature-summary/learner-ai-assistant.md).

## Multi-lingual Video Text Tracks (VTT) support

Multi-lingual Video Text Tracks (VTT) support in Adobe Learning Manager enables authors to provide subtitles and captions for video and audio content in multiple languages. This feature streamlines localization, making training accessible to a global audience and ensuring compliance with accessibility standards. Authors can auto-generate, translate, review, and edit VTT files directly within the platform.

### Use Cases

* **Global Training:** Deliver video content with subtitles in multiple languages to reach international learners.
* **Accessibility Compliance:** Provide captions for hearing-impaired users in their preferred language.
* **Faster Localization:** Reduce manual effort and accelerate content rollout by auto-generating and translating VTT files.
* **Consistent Experience:** Ensure all learners receive the same information, regardless of language.

### Belangrijkste kenmerken

* **Multi-language translation:** Translate captions into any of the 39 supported non-English languages.
* **In-app review and editing:** Review, edit, and download VTT files before publishing.
* **Notifications:** Receive in-app notifications when VTT generation and translation are complete.
* **Smooth publishing:** Publish finalized captions for learners to access in their chosen language.

### Upload content and generate VTT

1. Go to the Content Library and select **Add > Content**.
2. Upload your MP3 or MP4 file.
3. In uploadt dialoog, selecteer de optie **om Vertalingen** te produceren.
4. Selecteer de oorspronkelijke inhoudstaal (standaard is de taal van het bestand).
5. Selecteer extra doeltalen voor vertaling (maximaal 39 ondersteund).
6. Selecteer **Opslaan**. Het systeem begint met het genereren en vertalen van VTT-bestanden.

### Voortgang van monitor

1. Na het opslaan wordt het nieuwe inhoudsitem weergegeven in de inhoudsbibliotheek.
2. Een voortgangsindicator geeft de status van het genereren en vertalen van VTT weer.
3. U ontvangt een melding in de app wanneer het proces is voltooid.

### VTT-bestanden bekijken en bewerken

1. In de Bibliotheek van de Inhoud, open de inhoud op **geef** wijze uit.
2. Voor elke taal, selecteer de **verbinding van de Overzicht** naast het VTT dossier.
3. Er verschijnt een pop-upvenster met de bijschriften voor die taal.
4. Bewerk de bijschriften rechtstreeks in de pop-up of download het VTT-bestand voor offline bewerking.
5. Nadat u wijzigingen hebt aangebracht, uploadt of plakt u de herziene bijschriften weer in de pop-up.
6. Sla uw bewerkingen op.

### Publish-bijschriften

1. Publiceer de inhoud als u tevreden bent met alle taalbijschriften.
2. Studenten zien ondertitelopties in alle gepubliceerde talen wanneer ze de video bekijken.

### Aanvullende informatie

* **Gesteunde Talen:** Alle 39 niet-Engelse talen die door Adobe Learning Manager worden gesteund.
* **Meldingen:** de Auteurs worden op de hoogte gebracht wanneer de generatie en de vertaling van VTT volledig zijn.
* **het uitgeven flexibiliteit:** de Bijschriften kunnen in-app of offline worden uitgegeven en opnieuw-geupload.
* **Schaalbaarheid:** Ontworpen voor onderneming-schaal lokalisatie en toegankelijkheidsbehoeften.
* **Geen behoefte aan Hand VTT uploadt:** het systeem kan VTT dossiers van kras produceren gebruikend de geuploade video/audio.

### Beste werkwijzen

* Bekijk automatisch gegenereerde bijschriften altijd voor nauwkeurigheid voordat u ze publiceert.
* Vertaal alle grote studentengroepen om de toegankelijkheid te maximaliseren.
* Gebruik het meldingssysteem om bij te blijven met de verwerkingsstatus.
* Bijschriften worden regelmatig bijgewerkt als de video-inhoud verandert.

### Problemen oplossen

* Als het genereren van VTT mislukt, moet u ervoor zorgen dat uw bestand een ondersteunde indeling heeft (MP3/MP4).
* Controleer of ontbrekende talen worden ondersteund en selecteer deze tijdens het uploaden.
* Als bijschriften niet gesynchroniseerd zijn, gebruikt u de in-app editor om de timing aan te passen.

Dankzij meertalige VTT-ondersteuning kun je op een efficiënte manier toegankelijke, gelokaliseerde videoleerervaringen bieden. Door automatisch te genereren, te vertalen en in-app te bewerken, kunt u ervoor zorgen dat uw inhoud alle studenten bereikt en ondersteunt, ongeacht de taal.

## Aangepaste certificaten ontwerpen

Met aangepaste certificaten in Adobe Learning Manager (ALM) kunnen beheerders en auteurs gepersonaliseerde certificaten voor studenten ontwerpen, beheren en uitgeven. De functie omvat een editor voor slepen en neerzetten, dynamische velden, meertalige ondersteuning en door AI gegenereerde achtergronden, zodat organisaties zonder technische expertise branded certificaten kunnen maken.

### Vorig gedrag

Eerder was het maken van certificaten in ALM beperkt door de rigiditeit van sjablonen, het gebrek aan aanpassing en technische obstakels (zoals HTML-bewerking). Klanten vroegen om eenvoudigere manieren om certificaten te ontwerpen, dynamische velden toe te voegen (zoals de naam van de student of de docent) en meerdere talen te ondersteunen, terwijl ze tegelijkertijd de merkconsistentie en het visuele aspect behouden.

### Gebruiksscenario&#39;s

* **Branded erkenning**: Geef certificaten met collectieve logo&#39;s, kleuren, en doopvonten voor naleving, opleiding, of verwezenlijking uit.
* **Dynamische verpersoonlijking**: bevolk automatisch studentnamen, instructornamen, en andere actieve gebieden.
* **Meertalige levering**: Verstrek certificaten in veelvoudige talen voor globale studenten.
* **Flexibel ontwerp**: Creeer landschap of staande certificaten, gebruik AI-Geproduceerde achtergronden, en voorproef alvorens te publiceren.

### Toegang tot aangepaste certificaten

1. Ga naar de **sectie van Prestaties** in de Admin homepage (eerder genoemd **Badges**).
2. Selecteer **Certificaten** om, certificaatmalplaatjes te bekijken tot stand te brengen of te beheren.

### Een certificaat maken

1. Selecteer **tot Certificaat** leiden.
2. Selecteer de afdrukstand Staand of Liggend.
3. Selecteer een bestaande sjabloon of begin op een leeg canvas.
4. Voer een certificaatnaam en standaardtaal in.
5. Voeg met de editor voor slepen en neerzetten het volgende toe:
   * Tekstvelden (met opties voor lettertype, kleur en positionering)
   * Afbeeldingen (logo&#39;s, pictogrammen, enz.)
   * Dynamische velden (naam student, naam docent, enz.)
   * Certificaatachtergronden (effen kleur, geüploade afbeelding of door AI gegenereerde afbeelding)
6. Voor door AI gegenereerde achtergronden: voer een vraag in (bijvoorbeeld &quot;studenten in een lesruimte&quot;) om achtergronden te genereren met behulp van AI.

### Dynamische velden toevoegen

Dynamische velden in aangepaste Adobe Learning Manager-certificaten zijn plaatsaanduidingen die automatisch worden gevuld met relevante informatie, zoals de naam van de student, de naam van de docent of andere accountspecifieke gegevens, wanneer het certificaat wordt gegenereerd. Zo kunnen gepersonaliseerde en contextbewuste certificaten worden gegenereerd zonder dat deze handmatig hoeven te worden bewerkt.

1. Voeg dynamische variabelen in, zoals de naam van de student, de naam van de docent of andere actieve velden.
2. Velden worden automatisch ingevuld wanneer het certificaat wordt uitgegeven.

### Meertalige ondersteuning

1. Voeg nieuwe talen toe (bijvoorbeeld Frans of Duits) aan het certificaat.
2. Voer voor elke taal vertaalde tekst in.
3. Beheer vertalingen en bekijk een voorvertoning van certificaten in elke taal.

### Voorvertonen en publiceren

1. Gebruik de voorvertoningsfunctie om te zien hoe het certificaat voor de studenten wordt weergegeven.
2. Download de voorvertoning of druk deze af voor revisie.
3. Opslaan als concept om later verder te bewerken of publiceren wanneer gereed.

### Certificaten toepassen

1. Beheerders kunnen standaardcertificaten voor het account instellen.
2. Auteurs kunnen certificaten aan specifieke leerobjectinstanties (cursussen, paden, enz.) koppelen.
3. Selecteer desgewenst verschillende certificaten op instantieniveau.

### Certificaten beheren

1. Gepubliceerde en conceptcertificaten weergeven in de bibliotheek.
2. Bewerk, werk of verwijder sjablonen naar wens.
3. Certificaten kunnen in meerdere instanties opnieuw worden gebruikt.

Aangepaste certificaten in ALM bieden een flexibele manier om gepersonaliseerde, merkgebonden en meertalige certificaten te ontwerpen en af te geven. De functie vereenvoudigt certificaatbeheer, verbetert de herkenning van studenten en ondersteunt wereldwijde compliance- en brandingbehoeften.

## Meertalige taakhulpen

Met meertalige taakhulpen in Adobe Learning Manager (ALM) kunnen auteurs en beheerders ondersteunende documenten, handleidingen of bronnen in meerdere talen in één taakhulpitem opgeven. Studenten in verschillende regio&#39;s hebben toegang tot relevante materialen in hun voorkeurstaal, waardoor de toegankelijkheid, compatibiliteit en gebruikerservaring worden verbeterd.

### Vorig gedrag

Eerder stond ALM slechts één inhoudsbestand per taakhulp toe, ook al konden de naam en beschrijving worden gelokaliseerd. Om dezelfde bron in meerdere talen te bieden, moesten auteurs voor elke taal afzonderlijke taakhulpen maken. Dit leidde tot duplicatie, verwarring en grotere administratieve inspanningen. Er was geen uniforme manier om meertalige middelen te beheren, waardoor het moeilijk was om consistentie te garanderen en het gebruik te volgen.

### Gebruiksscenario&#39;s

* **Globale arbeidskrachtenactivering**: Lever veiligheidshandleidingen, procesgidsen, of verwijzingsdocumenten in veelvoudige talen aan een diverse arbeidskrachten.
* **Regelgevende naleving**: Zorg ervoor alle werknemers de zelfde nalevingsdocumentatie in hun inheemse taal ontvangen.
* **Consistent onboarding**: Verstrek onboardingchecklists of FAQs in lokale talen voor nieuwe hires wereldwijd.
* **Verminderde duplicatie**: beheer alle taalversies van een taakhulp in één enkele ingang, die updates en rapportering vereenvoudigt.

### Een meertalige taakhulp maken

1. Ga naar de rol van de Auteur en selecteer **Hulp van de Baan**.
2. Selecteer **creeer Taakhulp**.
3. Voer de naam en beschrijving van de taakhulp in de standaardtaal in.
4. Upload het primaire inhoudsbestand of geef een URL op voor de standaardtaal.
5. Sla de taakhulp op.

### Extra talen toevoegen

1. In de redacteur van de baanhulp, uitgezocht **voeg Taal** toe.
2. Selecteer de gewenste taal of talen in de lijst.
3. Voor elke toegevoegde taal:
   * Voer de gelokaliseerde naam en beschrijving in.
   * Upload het bijbehorende inhoudsbestand of geef een taalspecifieke URL op.
4. Herhaal dit voor alle vereiste talen.

### Talen bewerken en beheren

1. Als u een bestand of beschrijving voor een specifieke taal wilt bijwerken, selecteert u het tabblad Taal en brengt u de gewenste wijzigingen aan.
2. Als een taal wordt toegevoegd nadat de taakhulp is gepubliceerd, wordt het oorspronkelijke bestand automatisch toegewezen aan de nieuwe taal totdat een uniek bestand is geüpload.
3. Verwijder of vervang bestanden voor elke taal zoals vereist.

### Publish en leerervaring

1. Nadat alle talen en bestanden zijn toegevoegd, publiceert u de taakhulp.
2. Studenten zien de taakhulp in hun geselecteerde inhoudstaal, met het juiste bestand of de juiste URL.
3. Als de taal van een student niet beschikbaar is, wordt het standaardtaalbestand weergegeven.

### Rapportage

1. Download taakhulpenrapporten om details weer te geven van alle bestanden en talen die bij elke taakhulp horen.
2. Rapporten bevatten taal, bestandsnaam en gebruiksgegevens voor bijhouden.

Met meertalige taakhulpen in ALM kunt u in één keer ondersteunende hulpmiddelen leveren aan een wereldwijd publiek, het dupliceren verminderen en ervoor zorgen dat elke student de juiste informatie in de voorkeurstaal ontvangt. Deze functie verbetert de toegankelijkheid, compatibiliteit en administratieve efficiëntie in Adobe Learning Manager.

## Verbeteringen in het afspelen van cursussen die door Captivates worden gegenereerd

De update verbetert aanzienlijk de afspeelervaring voor Adobe Captivate-inhoud binnen ALM door een uniforme en gestroomlijnde interface te introduceren.

De ALM-speler geeft nu één geconsolideerde inhoudsopgave weer, verbergt de inhoudsopgave van de Captivate en verschaft duidelijke voltooiingsindicatoren op dianiveau, inclusief groene vinkjes voor visuele voortgangscontrole.

Het systeem vereenvoudigt navigatie door module- en cursusbesturingselementen samen te voegen tot één intuïtieve balk, waardoor de verwarring onder studenten wordt beperkt.

Met de contextbewuste voortgangsbesturingselementen wordt de bruikbaarheid verbeterd doordat alleen op videopresentaties en dia-navigatiebesturingselementen op niet-videodia&#39;s videovoortgangsbalken worden weergegeven.

Bovendien koppelt het systeem nu notities aan dianummers in plaats van tijdstempels, zodat de PDF betrouwbaar wordt geëxporteerd en eerdere inconsistenties in de indeling worden opgelost.

## Verbeteringen voor checklist

### Ondersteuning voor meerdere talen voor checklist

Met deze functie kunt u controlelijstmodules in meerdere talen maken en beheren. Elke vraag, instructie en evaluatiecriterium van de checklist kan worden vertaald, zodat revisoren en studenten in hun voorkeurstaal met de checklist communiceren. Het systeem geeft de controlelijst weer in de door de gebruiker geselecteerde inhoudstaal, waardoor de toegankelijkheid en compatibiliteit voor internationale teams worden verbeterd.

1. Voeg een controlelijstmodule toe aan of bewerk deze in uw cursus.
2. Selecteer in de taalopties alle talen die u wilt ondersteunen.
3. Voer voor elke taal vertalingen in voor elke vraag, instructie en evaluatiecriterium in de checklist.
4. Sla uw wijzigingen op. De controlelijst wordt weergegeven in de door de revisor of student geselecteerde inhoudstaal.
5. Als u later een nieuwe taal toevoegt, moet u vertalingen leveren voor alle vragen en criteria voordat u gaat publiceren.
6. Wanneer u controlelijstrapporten downloadt, selecteert u de voorkeurstaal om het rapport in die taal weer te geven.

### Dekkingsgewicht van de checklist-vraag voor beoordelingen van docenten

Met deze functie kunt u verschillende maximumscores (gewicht) toewijzen aan elke vraag in de controlelijst. U kunt het verschillende belang of de moeilijkheid van elke vraag weerspiegelen, die nauwkeurigere en betekenisvollere evaluaties steunt. Het systeem berekent de totale score op basis van uw invoer en bepaalt of de student slaagt of niet volgens de criteria die u instelt.

1. Wanneer het toevoegen van een controlelijstmodule, selecteer **het Scheuren van de Douane**.
2. Stel voor elke vraag over een checklist een unieke maximumscore in die het belang ervan weerspiegelt.
3. Definieer de algemene voldoende score voor de checklist.
4. Sla de controlelijst op en publiceer deze.
5. Als docent of revisor evalueert u elke student door een score toe te wijzen voor elke vraag (tot het maximum dat u instelt).
6. Het systeem berekent de totale score en bepaalt de status geslaagd/gezakt.
7. Download controlelijstrapporten om zowel de behaalde scores als de maximale scores voor elke vraag en de totale score te bekijken.

### Controlelijst met opmerkingsmogelijkheden voor revisor

Met deze functie kunnen revisoren opmerkingen of feedback toevoegen tijdens de evaluatie van de controlelijst. U kunt voor elke student gepersonaliseerde, actiegerichte feedback geven. U kunt er ook voor kiezen om uw naam met uw opmerkingen weer te geven voor transparantie. Alle opmerkingen worden opgeslagen in het transcript van de student en opgenomen in controlelijstrapporten.

1. Wanneer vestiging laat checklist, {de opmerkingen van de Recensent van 0} toe **.**
2. Naar keuze, laat **de naam van de kijker aan student** toe als u uw naam met uw commentaren wilt verschijnen.
3. Tijdens de evaluatie voert u in het veld Opmerkingen opmerkingen of feedback voor de student in.
4. Geef op of uw opmerkingen zichtbaar moeten zijn voor de student.
5. Verzend uw evaluatie. Indien ingeschakeld ziet de student uw opmerkingen en uw naam naast de resultaten.
6. Alle opmerkingen worden opgeslagen in het transcript van de student en opgenomen in controlelijstrapporten voor toekomstig gebruik.

## Geavanceerde zoekverbeteringen

Zoekresultaten in Geavanceerd zoeken zijn nu nauwkeuriger en relevanter. Exacte overeenkomsten met trefwoorden worden hoger gerangschikt in zoekopdrachten binnen inhoud en metagegevens, waardoor studenten gemakkelijker kunnen vinden wat ze zoeken.

Studenten kunnen nu ook ingeschreven leerobjecten in zoekresultaten zien, zelfs als ze geen deel uitmaken van een toegankelijke catalogus, zodat er geen relevante inhoud wordt gemist. Bovendien is de rangschikking van taakhulp verbeterd voor zowel Geavanceerd zoeken als zoekopdrachten binnen de inhoud, waardoor de meest relevante bronnen sneller worden weergegeven.


## Equivalenten en plaatsvervangers

### Overzicht

In veel organisaties komen studenten trainingssituaties tegen waarin verschillende cursussen rechtmatig aan dezelfde vereiste kunnen voldoen?Bijvoorbeeld wanneer een nieuwe cursus een oudere cursus vervangt, wanneer een uitgebreidere cursus voor een kortere cursus kan worden gevolgd of wanneer een speciale vervangende cursus moet worden aangeboden.

De functie Alternatieve cursussen of Leerpad biedt ALM een formele manier om te zeggen:

&quot;Als de leerling deze training heeft voltooid, behandelt u deze als voldeed aan dat gerelateerde trainingsvereiste.&quot;

De functie werkt in cursussen en leerpaden, zorgt ervoor dat stroomafwaartse vereisten zoals voorwaarden en nalevingsregels worden nageleefd, en dwingt studenten niet om overbodige inhoud te bekijken. Het blijft ook nauwkeurig rapporteren door te registreren wat direct werd voltooid versus wat via een alternatief werd tevreden.

In de kern introduceert de functie het concept van een alternatieve voltooiing: een speciale voltooiingsstatus die automatisch wordt gemaakt wanneer een student een geconfigureerde brontraining voltooit die telt voor een andere doeltraining.

### Equivalentie vs. alternatieven

Sommige trainingsrelaties zijn bidirectioneel, wat betekent dat elke cursus kan voldoen aan de behoefte van de ander. Dit is in feite een scenario waarin twee trainingen als onderling vervangbaar worden behandeld. In tegenstelling tot eenrichtingsrelaties kunnen opleidingen voldoen aan de eisen van een andere, maar niet andersom. ALM modelleert beide scenario&#39;s gebruikend het zelfde onderliggende afwisselende*voltooiingsmechanisme.

* **Bidirectionele verhouding:** Voltooiend of voldoet de opleiding aan het vereiste voor andere.
* **Unidirectionele verhouding:** Voltooiend Opleiding A voldoet Opleiding B, maar de voltooiing B voldoet geen A. Dit komt vaak voor wanneer een nieuwere of uitgebreidere versie telt voor een oudere vereiste, maar niet omgekeerd.

De alternatieven worden het vaakst gebruikt in **unidirectionele** scenario&#39;s?bijvoorbeeld, wanneer een uitvoeriger superset cursus alles in een eenvoudigere subsetcursus behandelt. Het voltooien van de superset moet voldoen aan de eisen voor de subset, maar niet noodzakelijkerwijs omgekeerd.

* Een nieuwere, uitgebreide cursus die moet tellen voor een oudere vereiste.
* Een cursus die is ontworpen voor een specifieke doelgroep (bijvoorbeeld een regionale of door toegankelijkheid* aangepaste variant) die nog steeds aan dezelfde vereisten voldoet als de primaire cursus.
* Een verbeterde nieuwe versie van een cursus die de organisatie wil tellen voor een oudere vereiste, maar de oudere versie mag niet tellen voor de nieuwe vereiste.

In Plaatsen, is de verhouding normaal **one*way**. Als Cursus A een alternatief is voor Cursus B, kan het voltooien van A voldoen aan B&#39;s vereiste, maar het voltooien van B voldoet niet noodzakelijkerwijs aan A.

Zowel equivalentie als alternatief delen hetzelfde onderliggende mechanisme in ALM: wanneer een geconfigureerde brontraining is voltooid, levert ALM automatisch een alternatieve voltooiing voor een of meer doeltrainingen.

### Welke problemen lost dit op?

Zonder alternatieven en equivalentie hebben beheerders en studenten te maken met verschillende terugkerende problemen:

* Studenten wordt vaak gevraagd om cursussen te herhalen die betrekking hebben op inhoud die ze al in een andere versie of indeling hebben voltooid.
* Het bijwerken van compatibiliteitsprogramma&#39;s is eenvoudiger omdat beheerders trainingen kunnen vervangen of herstructureren zonder studenten die oudere versies hebben voltooid, te dwingen equivalente of vervangen inhoud opnieuw op te nemen.
* Vereiste logica is rigide. Als een pad een bepaalde cursus als voorwaarde vereist, is er geen duidelijke manier om te erkennen dat een andere training goed genoeg is.
* Verslaglegging en audits zijn moeilijker. Er is geen formeel signaal dat aantoont dat aan een vereiste is voldaan via een alternatieve voltooiing en geen eenvoudige manier om de bron van het krediet te traceren.

Met de functie Alternatieven en Gelijkwaardigheid worden deze problemen opgelost door:

* Het voorkomen van dubbele inspanning voor studenten wanneer alternatieven geldig zijn.
* Beheerders toestaan om trainingsstructuren te wijzigen (bijvoorbeeld een cursus in een pad omwisselen) zonder de voltooide taken te doorbreken voor studenten die de eerdere versie hebben aangenomen.
* Voorwaarden en nalevingscontroles toestaan om zowel directe voltooiing als alternatieve of gelijkwaardige voltooiing te respecteren.
* In transcripties en rapporten moet duidelijk worden vermeld of een opleiding rechtstreeks of naar tevredenheid is afgerond via een alternatieve relatie, waarbij de opleiding als bron diende.

### Hoe de functie conceptueel werkt

De eigenschap wordt voortgebouwd op drie belangrijkste ideeën: **verhoudingen**, **afwisselende voltooiing**, en **stroomafwaarts gedrag**.

#### Relaties tussen trainingen

Beheerders definiëren de relaties tussen cursussen en leerpaden. Voor elke verhouding, kiezen zij a **bron** en één of meerdere **doelstellingen**. Afhankelijk van het aantal eerdere of verwante trainingen waaraan een cursus moet voldoen, kan deze een of meer van de 30 doelen hebben.

Voor Gelijkwaardigheid, kunnen de beheerders de verhouding **bidirectioneel** maken als zij beide trainingen willen elkaar tevreden stellen. Bij Alternatieven behouden beheerders doorgaans de richting één*manier om aan te geven dat slechts enkele vervangingen zijn toegestaan.

Deze relaties worden opgeslagen op het trainingsniveau, niet op het niveau van de student. Zodra geconfigureerd en ingeschakeld, zijn ze van toepassing op alle huidige en toekomstige voltooide brontraining, met inachtneming van de instellingen op account*level, zoals of retroactief afronden is ingeschakeld.

### Alternatieve voltooiing

Wanneer een student een bronopleiding voltooit, onderzoekt ALM alle gevormde afwisselende of gelijkwaardige verhoudingen en, voor elke relevante doelopleiding, leidt tot een **afwisselend voltooiingsverslag**. Deze record verschilt van een normale voltooiing:

* Het markeert de doeltraining voor de student, maar houdt bij dat deze is voltooid via een alternatieve of equivalente training in plaats van rechtstreeks.
* Het registreert welke bronopleiding werd gebruikt om aan het doel te voldoen.
* Het wordt opgeslagen in een specifieke structuur zodat de rapportering tussen directe en afwisselende voltooiing kan onderscheiden.

Studenten zien een alternatieve voltooiing, zelfs als ze niet zijn ingeschreven. Het LT-rapport (Studenttranscript) bevat alleen records van trainingen waarvoor de student zich heeft ingeschreven.

### Ervaring in de Learner-app voor alternatieve en gelijkwaardige voltooide taken

Alternatieve en gelijkwaardige voltooide taken worden afzonderlijk in de Learner-app opgehaald, zodat studenten duidelijk kunnen zien hoe aan een trainingsvereiste is voldaan, terwijl ze consistentie behouden met transcripten en rapporten.

#### LO-kaartgedrag

#### Andere voltooiingsstatus

Wanneer een student een opleiding via een afwisselende of gelijkwaardige verhouding voltooit, toont de het Leren kaart van Objecten (LO) een duidelijke status zoals **die via Afwisselend** wordt voltooid.\
Dit visuele verschil helpt studenten onderscheid te maken tussen directe voltooide en voltooide bewerkingen die zijn verleend via geconfigureerde relaties.

#### Indicator van de voltooiingsmethode

De kaart LO omvat een indicator van de voltooiingsmethode (bijvoorbeeld, een etiket of een pictogram) om te tonen dat de voltooiing door een **Afwisselend** werd bereikt.\
Als een afwisselende voltooiing later wegens veranderingen zoals retroactieve voltooiing of schrapping van de bronopleiding wordt herroepen, de LO kaartupdates om **(Ingetrokken) Afwisselend te wijzen**.

#### Transparantie- en auditgegevens

Studenten kunnen de LO-kaart openen om aanvullende gegevens te bekijken, zoals:

* De broncursus of het leerpad dat de alternatieve voltooiing heeft toegekend
* De voltooiingsdatum die is gekoppeld aan de brontraining

Dit zorgt voor transparantie en ondersteunt controle en nalevingscontroles.

#### Filteren en weergaven

#### Filter van de uitvoeringsmethode

De Learner-app biedt een filter waarmee studenten onderscheid kunnen maken tussen:

* **Directe** voltooiing
* **afwisselende** voltooiing
* **Alle** voltooiing

Zo kunnen studenten snel begrijpen hoe aan hun leervereisten is voldaan.

#### Weergave van transcripten en voortgang

Het filter van de voltooiingsmethode is beschikbaar in de weergaven student*tegenover elkaar, zoals:

* Teksttranscripten
* Secties voor bijhouden van voortgang en voltooiing

Deze weergaven geven duidelijk aan welke trainingen rechtstreeks zijn voltooid en aan welke opleidingen met alternatieven of equivalentie is voldaan.

#### Uitlijning van rapporten

De het filtreren logica in de student app richt zich op de **kolom van de Methode van de Voltooiing** die in rapporten wordt gebruikt.\
Dit zorgt voor consistentie tussen wat studenten zien in de gebruikersinterface en wat beheerders zien in export- en nalevingsrapporten.

#### Eind *aan* eindstroom

#### Voor studenten

1. Navigeer aan **Mijn Leren** of **Voltooide Cursussen** in de student app.
2. De kaarten van het overzicht LO om trainingen te identificeren die als **worden gemerkt via Afwisselend** worden voltooid.
3. Open een LO-kaart voor meer informatie over de brontraining en de voltooiingsdatum.
4. Gebruik het filtermenu in transcript of cursuslijstmeningen om **Direct** te selecteren, **Afwisselend**, of **allen**.
5. Bekijk de bijgewerkte lijst op basis van de geselecteerde voltooiingsmethode.

#### Voor beheerders en auteurs

1. Configureer gelijkwaardige of alternatieve relaties tussen cursussen of leerpaden in de beheerinterface.
2. Controleer of de alternatieve voltooide bewerkingen correct worden weerspiegeld op LO-kaarten en in filters voor studenten*onder elkaar.
3. Gebruik de studentweergaven en -rapporten om de consistentie tussen de gebruikersinterface en de geëxporteerde gegevens te bevestigen.
4. Als een bronopleiding wordt gearchiveerd of geschrapt, bevestig dat de beïnvloede LO kaartenupdate dienovereenkomstig (bijvoorbeeld, tonend **Afwisselend (ingetrokken)** wanneer toepasselijk).

## Gedrag van retroactieve voltooiing en voltooiing

ALM ondersteunt retroactief invullen en retroactief invullen om ervoor te zorgen dat alternatieve en gelijkwaardige relaties in de loop der tijd accuraat blijven, zelfs wanneer relaties worden gemaakt, gewijzigd of verwijderd nadat studenten de training al hebben voltooid.

### Retroactieve voltooiing

#### Definitie

Wanneer retroactief afronden is ingeschakeld, ontvangen studenten die in het verleden een broncursus hebben voltooid automatisch een alternatieve voltooiing voor de doelcursus als later een gelijkwaardige of alternatieve relatie wordt gecreëerd.\
Zo wordt ervoor gezorgd dat het historische leerproces wordt gerespecteerd zonder dat studenten de training opnieuw hoeven te volgen.

#### Zo werkt het

1. Een beheerder schakelt retroactieve voltooiing op accountniveau in.
2. De beheerder definieert een equivalente of alternatieve relatie tussen een bron- en doeltraining.
3. Het systeem scant historische voltooiingsrecords voor de brontraining.
4. Studenten die in aanmerking komen, krijgen een alternatieve voltooiing voor de doeltraining.
5. Deze verslagen verschijnen zoals **Voltooid via Afwisselend** in studenttranscripten en rapporten.

### Retroactive incomplete

#### Definitie

Wanneer retroactive incompletion is ingeschakeld, worden alternatieve voltooide bewerkingen ingetrokken als de onderliggende equivalente of alternatieve relatie wordt verwijderd of als de brontraining wordt verwijderd.\
Dit zorgt ervoor dat het systeem de huidige en geldige trainingsrelaties weerspiegelt.

#### Zo werkt het

1. Een beheerder schakelt retroactief invullen in op accountniveau.
2. De beheerder verwijdert een alternatieve of gelijkwaardige relatie of verwijdert de brontraining.
3. Het systeem identificeert studenten die via de betreffende relatie een alternatieve voltooiing hebben ontvangen.
4. De bijbehorende alternatieve voltooiingsrecords worden ingetrokken.
5. De ingetrokken verslagen worden gemerkt als **Afwisselend (ingetrokken)** in transcripten en rapporten voor controlezicht.

### Gevolgen voor de vereisten

Alternatieve voltooide bewerkingen, inclusief voltooide bewerkingen die met terugwerkende kracht zijn toegekend, worden behandeld als geldige voltooide bewerkingen bij de evaluatie van de voorwaarden.\
Als een student **via Afwisselend** is voltooid, mogen zij met cursussen verdergaan die de doelopleiding vereisen.

Als een alternatieve voltooiing later wordt herroepen door retroactief inVoltooien, kan de student niet langer in aanmerking komen voor cursussen die afhankelijk zijn van die voorwaarde.

### Gevolgen voor leerpaden en certificeringen

Alternatieve voltooide bewerkingen dragen bij tot de voortgang en voltooiing van leerpaden en certificeringen.\
Studenten kunnen deze programma&#39;s voortzetten of voltooien wanneer de vereiste trainingen via alternatieve of gelijkwaardige relaties worden gevolgd.

Als een alternatieve voltooiing wordt ingetrokken, kunnen de betrokken leerpaden of certificeringen de voortgang of voltooiingsstatus verliezen totdat aan de vereiste is voldaan door een geldige voltooiing.

### Eind *aan* eindwerkschema

#### Inschakelen van retroactieve voltooiing of incompleet

1. Beheerders navigeren naar accountinstellingen en schakelen retroactief invullen en/of retroactief incompleteren in.
2. Beheerders maken, wijzigen of verwijderen equivalente of alternatieve relaties tussen trainingen.

#### Systeemhandelingen

* **voor retroactive voltooiing:**\
  Het systeem biedt alternatieve voltooide bewerkingen op basis van historische bronvoltooiing.
* **voor retroactive incompletion:**\
  Het systeem herroept alternatieve voltooide bewerkingen wanneer relaties worden verwijderd of brontrainingen worden verwijderd.

#### Ervaring van de student

Studenten zien de bijgewerkte voltooiingsstatus op LO-kaarten en in transcripten, zoals:

* **Voltooid via Afwisselend**
* **Afwisselend (ingetrokken)**

Vereiste controles, voortgang van leerpad en status van certificering worden dynamisch bijgewerkt op basis van de huidige voltooiingsstatus.

#### Rapportage en audit

Alle wijzigingen met terugwerkende kracht worden weergegeven in het Leertranscript-rapport (LT).\
In rapporten wordt een duidelijk onderscheid gemaakt tussen directe voltooiing, alternatieve voltooiing en herroepen, om naleving te ondersteunen, onderzoeken en audits te ondersteunen.

### Gedrag van retroactieve voltooiing en voltooiing

ALM ondersteunt retroactief invullen en retroactief invullen om ervoor te zorgen dat alternatieve en gelijkwaardige relaties in de loop der tijd accuraat blijven, zelfs wanneer relaties worden gemaakt, gewijzigd of verwijderd nadat studenten de training al hebben voltooid.

#### Retroactieve voltooiing

#### Definitie

Wanneer retroactief afronden is ingeschakeld, ontvangen studenten die in het verleden een broncursus hebben voltooid automatisch een alternatieve voltooiing voor de doelcursus als later een gelijkwaardige of alternatieve relatie wordt gecreëerd.\
Zo wordt ervoor gezorgd dat het historische leerproces wordt gerespecteerd zonder dat studenten de training opnieuw hoeven te volgen.

#### Zo werkt het

1. Een beheerder schakelt retroactieve voltooiing op accountniveau in.
2. De beheerder definieert een equivalente of alternatieve relatie tussen een bron- en doeltraining.
3. Het systeem scant historische voltooiingsrecords voor de brontraining.
4. Studenten die in aanmerking komen, krijgen een alternatieve voltooiing voor de doeltraining.
5. Deze verslagen verschijnen zoals **Voltooid via Afwisselend** in studenttranscripten en rapporten.

#### Retroactive incomplete

#### Definitie

Wanneer retroactive incompletion is ingeschakeld, worden alternatieve voltooide bewerkingen ingetrokken als de onderliggende equivalente of alternatieve relatie wordt verwijderd of als de brontraining wordt verwijderd.\
Dit zorgt ervoor dat het systeem de huidige en geldige trainingsrelaties weerspiegelt.

#### Zo werkt het

1. Een beheerder schakelt retroactief invullen in op accountniveau.
2. De beheerder verwijdert een alternatieve of gelijkwaardige relatie of verwijdert de brontraining.
3. Het systeem identificeert studenten die via de betreffende relatie een alternatieve voltooiing hebben ontvangen.
4. De bijbehorende alternatieve voltooiingsrecords worden ingetrokken.
5. De ingetrokken verslagen worden gemerkt als **Afwisselend (ingetrokken)** in transcripten en rapporten voor controlezicht.

#### Gevolgen voor de vereisten

Alternatieve voltooide bewerkingen, inclusief voltooide bewerkingen die met terugwerkende kracht zijn toegekend, worden behandeld als geldige voltooide bewerkingen bij de evaluatie van de voorwaarden.\
Als een student **via Afwisselend** is voltooid, mogen zij met cursussen verdergaan die de doelopleiding vereisen.

Als een alternatieve voltooiing later wordt herroepen door retroactief inVoltooien, kan de student niet langer in aanmerking komen voor cursussen die afhankelijk zijn van die voorwaarde.

#### Gevolgen voor leerpaden en certificeringen

Alternatieve voltooide bewerkingen dragen bij tot de voortgang en voltooiing van leerpaden en certificeringen.\
Studenten kunnen deze programma&#39;s voortzetten of voltooien wanneer de vereiste trainingen via alternatieve of gelijkwaardige relaties worden gevolgd.

Als een alternatieve voltooiing wordt ingetrokken, kunnen de betrokken leerpaden of certificeringen de voortgang of voltooiingsstatus verliezen totdat aan de vereiste is voldaan door een geldige voltooiing.

#### Eind *aan* eindwerkschema

#### Inschakelen van retroactieve voltooiing of incompleet

1. Beheerders navigeren naar accountinstellingen en schakelen retroactief invullen en/of retroactief incompleteren in.
2. Beheerders maken, wijzigen of verwijderen equivalente of alternatieve relaties tussen trainingen.

#### Systeemhandelingen

* **voor retroactive voltooiing:**\
  Het systeem biedt alternatieve voltooide bewerkingen op basis van historische bronvoltooiing.
* **voor retroactive incompletion:**\
  Het systeem herroept alternatieve voltooide bewerkingen wanneer relaties worden verwijderd of brontrainingen worden verwijderd.

#### Ervaring van de student

Studenten zien de bijgewerkte voltooiingsstatus op LO-kaarten en in transcripten, zoals:

* **Voltooid via Afwisselend**
* **Afwisselend (ingetrokken)**

Vereiste controles, voortgang van leerpad en status van certificering worden dynamisch bijgewerkt op basis van de huidige voltooiingsstatus.

#### Rapportage en audit

Alle wijzigingen met terugwerkende kracht worden weergegeven in het Leertranscript-rapport (LT).\
In rapporten wordt een duidelijk onderscheid gemaakt tussen directe voltooiing, alternatieve voltooiing en herroepen, om naleving te ondersteunen, onderzoeken en audits te ondersteunen.

### Webhooks voor equivalenten en alternatieven

ALM biedt speciale webhookgebeurtenissen voor equivalente en alternatieve voltooiing ter ondersteuning van automatisering, integraties en synchronisatie met externe systemen.

Deze gebeurtenissen stellen externe consumenten in staat op een betrouwbare manier onderscheid te maken tussen directe voltooiing en voltooiing via alternatieve of gelijkwaardige relaties.

#### Overzicht

Wanneer een student een cursus voltooit via een alternatieve of gelijkwaardige relatie, activeert ALM een webhook-gebeurtenis die losstaat van de webhook voor standaardvoltooiing van de cursus.\
Dit zorgt ervoor dat integraties waar nodig anders kunnen reageren op alternatieve voltooide bewerkingen.

Webhook-gebeurtenissen worden ook geactiveerd wanneer de bewerking met terugwerkende kracht wordt voltooid of terugwerkende kracht wordt voltooid. Dit betreft zowel historische updates als relatiewijzigingen.

#### Gebeurtenis webhook

* Een verschillende webhookgebeurtenis wordt teweeggebracht wanneer een student **wordt voltooid via Afwisselende** status voor een doelcursus ontvangt.
* De gebeurtenis wordt gegenereerd wanneer de student een geconfigureerde broncursus voltooit die voldoet aan het doel via een equivalente of alternatieve relatie.
* Deze webhook wordt niet geactiveerd voor directe voltooiing van de cursus.
* Wanneer retroactief afronden of retroactief voltooien is ingeschakeld, worden webhookgebeurtenissen uitgezonden voor elke betrokken student en doelcursus.

#### Details webhook-lading

De webhook-lading voor alternatieve voltooiing bevat de volgende sleutelkenmerken:

* **identiteitskaart van de Student**\
  Hiermee wordt aangegeven welke student de alternatieve voltooiing heeft ontvangen.

* **Broncursus**\
  De cursus of het leerpad dat de leerling rechtstreeks heeft voltooid.

* **cursus van het Doel**\
  De cursus die als voltooid is gemarkeerd via de alternatieve of gelijkwaardige relatie.

* **methode van de Voltooiing**\
  Wijst erop dat de voltooiingsmethode **afwisselend** is.

* **de datum van de Voltooiing**\
  Voortgekomen uit de voltooiingsdatum van de broncursus.

* **het type van Verhouding**\
  Specificeert of de verhouding **equivalent** of **afwisselend** is.

Voor scenario&#39;s met terugwerkende kracht geven webhookgebeurtenissen aan dat een bestaande alternatieve voltooiing is ingetrokken.

#### Integratieoverwegingen

Externe systemen kunnen deze webhookgebeurtenissen gebruiken om:

* Studentrecords bijwerken
* Voltooiingsstatus synchroniseren
* Meldingen activeren of workflows stroomafwaarts
* Audittrails onderhouden voor nalevingsdoeleinden

De consumenten van het Web zouden tussen **direct** en **afwisselende** voltooiing uitdrukkelijk moeten onderscheiden.\
Alternatieve voltooiingen geven geen beloningen voor vaardigheden, badges of gamification en moeten dienovereenkomstig worden verwerkt in downstreamsystemen.

### Gevolgen van het afschaffen en verwijderen van brontraining in equivalenten en alternatieven

De levenscyclusstatus van een brontraining (gearchiveerd of verwijderd) is rechtstreeks van invloed op de manier waarop alternatieve en gelijkwaardige voltooide taken voor studenten worden onderhouden. ALM handelt deze scenario&#39;s verschillend af om historische nauwkeurigheid te bewaren terwijl het verzekeren van huidige verhoudingen geldig blijven.

#### Brontraining archiveren

##### Definitie

Het intrekken van een cursus maakt deze niet beschikbaar voor nieuwe inschrijvingen, maar houdt deze wel in het systeem voor historische referentie-, rapportage- en auditdoeleinden.

##### Gevolgen

* Bestaande alternatieve voltooide bewerkingen die via de gearchiveerde broncursus zijn toegekend, blijven geldig.
* Studenten die de broncursus eerder hebben voltooid, kunnen de doelcursus op een andere manier voltooien.
* Er worden geen nieuwe alternatieve voltooide cursussen gegenereerd vanuit de gearchiveerde cursus, aangezien deze niet door nieuwe studenten kunnen worden voltooid.
* Studenttranscripten en rapporten blijven **Voltooid via Afwisselend** voor beïnvloede studenten tonen.

#### Brontraining verwijderen

#### Definitie

Als u een cursus verwijdert, wordt deze volledig uit het systeem verwijderd, inclusief de voltooiingsrecords en geconfigureerde relaties.

#### Gevolgen

* Als terugwerkende kracht is ingeschakeld, worden alle alternatieve voltooide bewerkingen die via de verwijderde broncursus zijn toegekend, ingetrokken.
* De transcripten en de rapporten van de student werken bij om **Afwisselend (ingetrokken)** voor controle en nalevingszicht te tonen.
* Studenten kunnen de status voor voortgang of voltooiing kwijtraken in leerpaden, certificeringen of voorwaarden die afhankelijk zijn van de ingetrokken alternatieve voltooiing.
* De verwijderde cursus kan niet verder worden voltooid.

#### Workflow

1. Een beheerder archiveert of verwijdert de broncursus via de beheerinterface.
2. Het systeem evalueert alle alternatieve en gelijkwaardige voltooide bewerkingen die uit de broncursus zijn afgeleid.
3. Voltooiingsstatus wordt bijgewerkt op basis van de cursusstatus:
   * **Gearchiveerd:** de bestaande afwisselende voltooiing blijft onveranderd.
   * **Geschrapt:** de afwisselende voltooiing wordt herroepen als de retroactieve voltooiing wordt toegelaten.
4. Studenttranscripten en -rapporten geven de bijgewerkte status weer ter ondersteuning van compatibiliteits- en auditvereisten.

### Geen keten van relaties

ALM ondersteunt geen ketting van alternatieve of gelijkwaardige relaties. Alternatieve voltooide cursussen worden alleen toegekend voor rechtstreeks geconfigureerde relaties en worden niet verspreid over meerdere niveaus van cursussen.

#### Concept: geen keten van relaties

#### Definitie

Chaining verwijst naar het toestaan van alternatieve of gelijkwaardige relaties om zich over meerdere cursussen te verspreiden.\
Als Cursus A bijvoorbeeld een alternatief is voor Cursus B en Cursus B een alternatief voor Cursus C, zou een ketting impliceren dat het voltooien van Cursus A voltooiing van Cursus C toelaat.

#### Beleid

Chaining wordt niet ondersteund.\
Alternatieve en gelijkwaardige relaties worden slechts op één niveau geëvalueerd. Als u een broncursus voltooit, wordt de alternatieve voltooiing alleen toegewezen aan de directe doelcursus of -cursussen, niet aan stroomafwaartse doelen.

#### Workflow

#### Relatie instellen

Een beheerder definieert alternatieve of gelijkwaardige relaties tussen cursussen, zoals:

* Cursus A → Cursus B
* Cursus B → Cursus C

#### Voltooiingsgebeurtenis

Een student voltooit cursus A rechtstreeks.

#### Systeemactie

* Het systeem kent een alternatieve voltooiing toe voor cursus B, als de relatie A → B is gedefinieerd.
* Het systeem kent geen alternatieve voltooiing voor cursus C toe, zelfs niet als er een B → C-relatie bestaat.

#### Vereiste voor directe voltooiing

Om een alternatieve voltooiing voor Cursus C te ontvangen, moet de student:

* Cursus B rechtstreeks voltooien, of
* Voltooi een cursus die expliciet is geconfigureerd als direct alternatief of equivalent voor Cursus C.

### Implicaties

#### Geen indirecte voordelen

Studenten kunnen geen voltooiingskrediet ontvangen voor cursussen die zich verder in een relatieketen bevinden, tenzij elke cursus (of de directe alternatieve cursus) is voltooid.\
Dit zorgt ervoor dat aan de leervereisten expliciet en voorspelbaar wordt voldaan.

#### Vereenvoudigde audit en verslaglegging

Rapporten en studenttranscripten geven alleen alternatieve voltooide bewerkingen weer voor directe relaties.\
Zo voorkomt u complexe multihop-audittrails en zorgt u ervoor dat u weet hoe voltooiing is toegestaan.

### Delen van catalogi met collega-accounts: relaties niet gedeeld

Met het delen van catalogi kunnen leerobjecten (LO&#39;s) worden gedeeld tussen collega-accounts, maar alternatieve en gelijkwaardige relaties worden onafhankelijk binnen elk account beheerd en worden niet gedeeld.

#### Concept: het delen van catalogi en relaties

#### Catalogus delen

Accounts kunnen catalogi met collega-accounts delen om toegang te bieden tot cursussen, leerpaden en andere leerobjecten in verschillende accounts.

#### Relaties niet gedeeld

In het bronaccount geconfigureerde relaties voor alternatief, equivalent en afwisselend aanvullen worden niet gedeeld of gerepliceerd wanneer een catalogus wordt gedeeld.\
Elke account onderhoudt en evalueert zijn eigen relaties onafhankelijk.

### Workflow

#### Catalogus delen

Een beheerder in **Rekening A** deelt een catalogus die het leren voorwerpen met **Rekening B** bevat.

#### Relatie-configuratie

Account A kan alternatieve of gelijkwaardige relaties hebben gedefinieerd tussen de leerobjecten in de gedeelde catalogus.

#### Toegang tot Collega-account

Account B krijgt toegang tot de gedeelde leerobjecten, maar neemt geen alternatieve of gelijkwaardige relaties over die zijn geconfigureerd in account A.

#### Onafhankelijk beheer

Als Account B een vergelijkbaar alternatief of equivalent gedrag vereist, moet een beheerder in Account B de relaties binnen dat account handmatig configureren.

#### Implicaties

#### Geen automatische relatiedoorgave

Alternatieve en gelijkwaardige relaties zijn niet automatisch beschikbaar in collega-accounts via het delen van catalogi.

#### Handmatige installatie is vereist

Elk collega-account is verantwoordelijk voor het definiëren en beheren van zijn eigen relaties voor gedeelde leerobjecten.

#### Consistentie

Voltooiingsgedrag, vereiste tevredenheid en rapportage kunnen per account verschillen, tenzij relaties opzettelijk worden uitgelijnd via handmatige configuratie.


### Downstream, gedrag

Zodra een afwisselende voltooiing voor een doelopleiding bestaat, gebruikt ALM het in stroomafwaartse controles:

* Als de doelopleiding a **eerste vereiste** voor andere trainingen is, wordt de student verkiesbaar voor die trainingen alsof zij het doel hadden voltooid.
* Als het doel a **verplichte cursus in een het leren weg** is, kan de de voltooiingslogica van de weg de student behandelen zoals voltooid dat deel en te werk gaan om de weg volledig te merken wanneer andere voorwaarden worden voldaan aan.
* Compatibiliteit en andere dashboards, zoals het groepssuccesdashboard, die afhankelijk zijn van het feit of aan een trainingsvereiste is voldaan, kunnen studenten omvatten die alleen alternatieve voltooide taken hebben.

Het systeem maakt een onderscheid tussen feitelijke voltooiing en afwisselende voltooiing, zodat:

* Als de student de doeltraining later rechtstreeks uitvoert en deze voltooit, kan deze directe voltooiing de behoefte aan een alternatieve voltooiing overschrijven.
* Als de relatie tussen bron en doel wordt verwijderd of gewijzigd, kan ALM de alternatieve voltooide bewerkingen verwijderen of aanpassen zonder dat dit ten koste gaat van echte voltooide bewerkingen, op voorwaarde dat retroactieve invullingen zijn ingeschakeld voor het account.

Alternatieve voltooide trainingen hebben geen invloed op de werkelijke leeractiviteiten in de doeltraining. Ze fungeren als een overlay die kan worden herzien als de relaties veranderen.
