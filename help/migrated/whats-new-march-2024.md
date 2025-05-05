---
description: Meer informatie over de nieuwe functies en verbeteringen in de release van Adobe Learning Manager (maart 2024)
jcr-language: en_us
title: Overzicht van nieuwe functies
contentowner: jayakarr
exl-id: 603f1f1c-bf8d-4807-b9f7-b10ded19a91e
source-git-commit: c833d92533b7fbf5a87c980d8b5e088185d02ef5
workflow-type: tm+mt
source-wordcount: '3903'
ht-degree: 1%

---

# Overzicht van nieuwe functies {#new-features-summary}

Meer informatie over de nieuwe functies en verbeteringen in de release van Adobe Learning Manager van maart 2024.

Ontdek enkele van de nieuwste functies van Adobe Learning Manager, zoals:

1. Vaardigheden importeren uit externe bronnen
1. Ondersteuning voor meerdere merken
1. Module Voor het opnieuw evalueren van checklists
1. White-labeled mobiele leer-app

>[!NOTE]
>
>Bekijk dit [webinar](https://learningmanager.adobe.com/app/learner?accountId=98632#/course/9212121) voor meer informatie over de nieuwe functies in deze versie.


## Nieuw in deze release {#whatsnewandchanged}

### Vaardigheden importeren uit externe bronnen

Importeer vaardigheden van inhoudsproviders, zoals LinkedIn en Go1, door de respectievelijke connectors te gebruiken. Deze verbetering maakt deel uit van het doel om Learning Manager te integreren met externe skillsclouds en talentbeheersystemen. De geïmporteerde vaardigheden worden toegevoegd aan de door beheerders gedefinieerde vaardigheden in Learning Manager en zijn beschikbaar voor auteurs tijdens de workflow voor het maken van cursussen. Ook zijn er verbeteringen aangebracht aan de functie voor het zoeken naar vaardigheden op het hele platform om een betere zoekervaring te bieden wanneer het account beschikt over een groot aantal vaardigheden.

Bekijk [de importvaardigheden](administrators/feature-summary/import-skills-external-sources.md) voor meer informatie.

### Aangepaste branding

U kunt nu bepaalde ui-elementen, de naam van de organisatie, het logo en het ui-thema, aanpassen op basis van de gebruikersgroepen die beschikbaar zijn in het account. Een organisatie met meerdere divisies kan bijvoorbeeld een aangepast logo en ui-thema instellen dat voor elke afdeling wordt weergegeven.

>[!NOTE]
>
>Deze functie voor meerdere branding is niet van toepassing op de weergave Beheerder. Ze zien altijd branding op organisatieniveau in hun account. Dit komt omdat dit een functie voor het leren leren is en beheerders deze functie mogelijk niet in hun account willen opnemen.

Meerdere [aangepaste branding weergeven](administrators/feature-summary/themes.md#multiple-branding) voor meer informatie.


## Wijzigingen voor accounts met een groot aantal gebruikers

### Admin- Cursus- of Leerpadpagina&#39;s

Als er bijvoorbeeld meer dan 50.000 studenten zijn ingeschreven voor de cursus, wordt de lijst met studenten niet weergegeven. U kunt zoeken naar een leerling in de *zoekbalk voor* studenten of de **downloadkoppeling** boven aan de zoekbalk selecteren om de lijst met studenten te downloaden.

### Pagina Beheerders en studenten

Wanneer u een gebruiker zoekt, worden hetzelfde rapport gedownload met de **opties Downloadgebruiker** en **Exporteren** . Terwijl u een gebruikersgroep zoekt, kunt u nu gefilterde gebruikers uit die gebruikersgroep downloaden. Wanneer u in een gebruikersgroep zoekt,
De lijst&#x200B;**met studenten downloaden verandert in** Lijst met studenten voor gebruikersgroepen **downloaden Met de**&#x200B;**optie Exporteren** downloadt u opnieuw de hele lijst.

### Beheer- de pagina Gebruikers

#### Interne gebruikers

Als het aantal gebruikers hoger is dan bijvoorbeeld de 50.000, zal er later een bericht zijn om de gegevens te downloaden voor een meer gedetailleerde analyse. De zoekbalk is nu prominent en toont een gebruiker in de indeling *Naam, e-mail | UUID*.

>[!NOTE]
>
>De UUID wordt alleen weergegeven als UUID is ingeschakeld voor de account.

#### Externe gebruikers

Voor externe gebruikers is hetzelfde gedrag van toepassing. Als het aantal gebruikers groot is, kunt u de gebruikers downloaden en na een zoekopdracht ook de gegevens van een gebruiker ophalen in de indeling *Naam, e-mail | UUID*.

#### Pagina Gebruikers opruimen

Voor verwijderde gebruikers hebben we de sorteerfunctie op **Datum verwijderd** op de pagina Gebruikersopruiming verwijderd. U kunt alleen sorteren op UUID&#39;s.

### Pagina&#39;s van beheerders en instanties

#### Cursus of leerpad

Als het aantal inschrijvingen groot is, wordt het aantal studenten niet weergegeven door Adobe Learning Manager. In plaats daarvan ziet u een pictogram dat u kunt selecteren, het aantal studenten kunt weergeven en naar de pagina Studenten kunt navigeren.

Het aantal leerlingen wordt bij benadering weergegeven. Als het aantal studenten bijvoorbeeld meer dan 50.000 is, wordt de waarde weergegeven als 50K+.

### Admin- L1/L3-pagina&#39;s

Als het aantal cursusinschrijvingen groot is op de L1-feedbackpagina, wordt de lijst met studenten niet weergegeven. In plaats daarvan kunt u de lijst met gebruikers exporteren voor een meer gedetailleerde analyse later.

De zoekopdracht ondersteunt type-ahead en de resultaten zijn beperkt tot de geselecteerde instantie.

#### Aanwezigheids- en scorepagina

Wanneer u op de pagina naar een gebruiker zoekt, wordt de zoekopdracht uitgevoerd op alle beschikbare instanties. Het resultaat is echter voor de geselecteerde instantie.

Als u op de aanwezigheidspagina een gebruikersgroep zoekt en het aantal gebruikers in de gebruikersgroep groter is dan 10.000, ongeacht uw inschrijving, kunt u alleen handelingen op bulkniveau uitvoeren. U kunt de lijst met gebruikers niet weergeven.

Als de gebruikersgroep minder dan 10.000 gebruikers bevat, kunt u acties op gebruikersniveau en meerdere handelingen op bulkniveau uitvoeren. In dit geval is de lijst met gebruikers niet uitgeschakeld.

### Beheer- pagina Certificeringen

Als in huidige versies van Adobe Learning Manager een groot aantal gebruikers is ingeschreven voor een certificering, kunt u de niet-ingeschreven studenten niet bekijken omdat de **vervolgkeuzelijst Status** is uitgeschakeld.

Als in deze versie van Adobe Learning Manager het aantal ingeschreven gebruikers groot is, worden in het **vervolgkeuzemenu Status** slechts twee opties weergegeven: **Ingeschreven** en **Niet ingeschreven**. De optie **Ingeschreven** is standaard geselecteerd. Als u Niet **ingeschreven selecteert**, wordt de lijst met niet-ingeschreven studenten weergegeven.

#### Wijzigingen in gebruikersgroepen

Als in het geval van een gebruikersgroep het aantal gebruikers in de gebruikersgroep lager is dan bijvoorbeeld 50.000, ziet u in het **vervolgkeuzemenu Status** alle opties Gecertificeerd, Toegewezen en Verlopen.

Als het aantal gebruikers in een gebruikersgroep groot is, worden in het **vervolgkeuzemenu Status** slechts twee opties **&#x200B;**&#x200B;weergegeven: Ingeschreven en **Niet ingeschreven** volgens het nieuwe ontwerp.

### Vergelijkingstabel

<table>
    <tbody>
        <tr>
            <td><b>Pagina</b></td>
            <td><b>Vóór wijziging drempel</b></td>
            <td><b>Nadat drempel is gewijzigd</b></td>
        </tr>
        <tr>
            <td>Admin - Cursusinstantie</td>
            <td>De instanties worden weergegeven zoals is ontworpen met het volgende:
            <ul>
                <li>Modules</li>
                <li>Ingeschreven studenten</li>
                <li>Sessies</li>
                <li>Badge</li>
                <li>L1-feedback ingeschakeld</li>
                <li>Meldingswaarschuwingen</li>
                <li>Gamification-punten</li>
                <li>QR-code</li>
                <li>Uitbreiding Leerpad</li>
            </ul>
            <td>
                <ul>
                    <li>Als het aantal inschrijvingen de vooraf gedefinieerde drempel overschrijdt, zal ALM het aantal niet weergeven; Het aantal wordt vervangen door een pictogram dat, wanneer je erop klikt, het werkelijke aantal leerlingen weergeeft en een koppeling waarmee je naar de pagina Studenten gaat.</li>
                    <li>Het aantal inschrijvingen wordt bij benadering weergegeven. Als het getal bijvoorbeeld meer dan 50.000 is, wordt het aantal weergegeven als 50 K+ op cursusniveau.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Pagina Beheerders en studenten</td>
            <td>
                    <ul>
                        <li>De lijst met studenten wordt weergegeven voor elke instantie.</li>
                        <li>U kunt zoeken naar een gebruiker of gebruikersgroep die is ingeschreven voor een cursus.</li>
                        <li>Het geëxporteerde rapport bestaat niet uit een filter voor gebruikersgroep.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>De selectie van de instantie is uitgeschakeld.</li>
                    <li>Met de lijst voor studenten downloaden worden ook dezelfde gegevens gedownload, behalve voor één aanvraag. Als u een gebruikersgroep zoekt en vervolgens de lijst Studenten downloaden selecteert, worden de gegevens van die gebruikersgroep gedownload.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Beheer- L1/L3-feedbackpagina</td>
            <td>
                <p>Geen wijziging in bestaand gedrag</p>
            </td>
            <td>
                <ul>
                    <li>De selectie van de instantie is uitgeschakeld.</li>
                    <li>Als de inschrijving voor een cursus hoger is dan 50 kB, geeft ALM geen lijst met studenten op en wordt alleen de zoekbalk weergegeven. Als de inschrijving minder dan 50.000 is, geeft ALM zowel de lijst met leerlingen als de zoekbalk weer.</li>
                    <li>De aanbieding is standaard uitgeschakeld.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Beheer- Aanwezigheids- en scorepagina</td>
            <td>
                <p>Geen wijziging in bestaand gedrag</p>
            </td>
            <td>
                <ul>
                    <li>De selectie van de instantie is uitgeschakeld bij het zoeken naar een gebruiker.</li>
                    <li>Als het aantal gebruikers hoger is dan bijvoorbeeld de 50.000, zal er later een extra bericht zijn om de gegevens te downloaden voor een meer gedetailleerde analyse. De zoekbalk is nu prominent en toont een gebruiker in de indeling Naam, e-mail | UUID.</li>
                    <li>Als het aantal gebruikers in de gebruikersgroep minder dan 10.000 is, ongeacht de inschrijving, kunt u individuele acties op gebruikersniveau uitvoeren, samen met acties op bulkniveau. In dit geval is de lijst met gebruikers niet uitgeschakeld.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Beheer- L2 Quiz Score pagina</td>
            <td>
                    <ul>
                        <li>Zoeken voor gebruikers is ook geïmplementeerd.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Zoeken voor gebruikers is ook geïmplementeerd. Terwijl u op LO-niveau zoekt naar typeahead, wordt de lijst gefilterd op de momenteel geselecteerde instantie.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Beheer- pagina Gebruikers (intern, extern)</td>
            <td>
                    <ul>
                        <li>Het e-mail-id wordt weergegeven bij het zoeken naar een gebruiker.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Als het aantal gebruikers overschrijdt, bijvoorbeeld, 50.000, zal er later een extra bericht zijn om de gegevens te downloaden voor een meer gedetailleerde analyse. De zoekbalk is nu prominent en toont een gebruiker in de indeling Naam, e-mail | UUID.</li>
                    <li>Voor verwijderde gebruikers hebben we de sorteerfunctie op **Datum verwijderd**, op de pagina Gebruikersopruiming verwijderd. U kunt alleen sorteren op UUID's.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Cursusleiders- inzending</td>
            <td>
                    <ul>
                        <li>Paginering van de nog in te dienen modules.</li>
                        <li>Als cursusleider kunt u nu filteren op bestandsinzendingen van studenten op basis van status, revisie beëindigen, In behandeling, Doorgegeven en Mislukt. </li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>U kunt in dat geval alleen zoeken naar gebruikers en niet in gebruikersgroepen.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Rekenen op voorvertoning als lerende pagina</td>
            <td>
                    <ul>
                        <li>Het aantal omvat de gegevens van inschrijvingen met een hogere order.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Met het aantal gegevens worden gegevens uitgesloten van inschrijvingen met een hogere volgorde.</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Geavanceerde zoekfuncties

In deze versie is de zoekervaring verbeterd. De zoekresultaten worden niet alleen op basis van de metagegevens, maar ook op basis van semantische zoekopdrachten en zoekopdrachten in de inhoud om resultaten af te leiden op basis van precisie, recentheid en relevante inhoud.

Deze wijziging geldt voor het volgende:

* Catalogus en mijn leerpagina: De muisaanwijzer voor een cursus, leerpad en certificering is verwijderd.
* De weergave van de zoekbalk.
* Filtertags toegevoegd in de lerende app.

Neem contact op met het CSAM team van Adobe Learning Manager om zoekfuncties in te schakelen.

## Veranderingen in gebruikersinterface {#ui-changes}

### Pagina voor het maken van cursussen

Bij het toewijzen van de cursussen aan een vaardigheidsniveau, is de lijst met vaardigheden op de eerste plaats. Met andere woorden, zoek naar vaardigheden, dan wordt een lijst met vaardigheden weergegeven die overeenkomt met de gezochte term.

### Gebruikersgroepen

#### Beheer: pagina Studenten

Wanneer u een gebruiker zoekt, worden hetzelfde rapport gedownload met de **opties Downloadgebruiker** en **Exporteren** . Terwijl u een gebruikersgroep zoekt, kunt u nu gefilterde gebruikers uit die gebruikersgroep downloaden. Als u in een gebruikersgroep zoekt, verandert de **lijst** met downloadgebruikers in **Lijst met studenten downloaden voor gebruikersgroep** . Met de **optie Exporteren** downloadt u opnieuw de hele lijst.

## Wijzigingen in rapporten

* De kolommen Tag(s) en Skill(s) in Trainingsrapport worden gewijzigd in Tag en vaardigheden.
* De Gamification-audittrail van het rapport [is](administrators/feature-summary/reports.md#gamification-audit-trail) toegevoegd.
* Als een account meer dan 280000 leerlingen bevat die aan een vaardigheid zijn toegewezen, wordt het rapport met de vaardigheidsdeelnemer gedownload als een zip-bestand (CSV-bestand).
Als het account minder dan 250000 gebruikers heeft, wordt hetzelfde rapport gedownload als een CSV-bestand.
Selecteer op de pagina Beheerder de optie **Vaardigheden >**&#x200B;**beheren** > **Vaardigheid** > **studenten**. Het rapport wordt gedownload als CSV-bestand.
* Het [rapport van het sessieoverzicht](administrators/feature-summary/reports.md#session-summary-report) heeft twee nieuwe kolommen: Locatie-informatie en Locatiegebied.

## Wijzigingen in het maken van klaslokalen

[Op basis van de beheerdersinstellingen](administrators/feature-summary/classroom.md#classroom-settings) kunt [u als auteur locaties](administrators/feature-summary/classroom.md#add-classroom-location) maken, wijzigen en verwijderen.

>[!NOTE]
>
>Bij het toevoegen van locatie- en cataloguslabels zien auteurs (op de pagina voor het maken van cursussen) en beheerders (op de instantiepagina) respectievelijk een automatisch ingevulde lijst met locaties en cataloguslabels.

Als beheerder kunt u een auteur beperkingen opleggen om een locatie in een klaslokaal te wijzigen of te verwijderen. Bekijk [de instellingen](administrators/feature-summary/classroom.md#classroom-settings) voor Klaslokalen voor meer informatie.

## Wijzigingen in flexibel leerpad

Alle accounts (oud en nieuw) beginnen, inclusief inschrijvingsdeadline, inschrijvingsdeadline en licentielimiet in de app Lerende voor een flexibel leerpad.
Studenten kunnen zich nu inschrijven voor een flexibel leerpad zonder een instantie van de cursus te selecteren.

## Nieuwe trigger voor leerplannen

Er is een nieuwe trigger toegevoegd aan de pagina instellen van het leerplan. Auteurs en beheerders kunnen nu acties activeren wanneer een leerling een module van een cursus mislukt.

Bekijk [leerplannen](administrators/feature-summary/learning-plans.md) voor meer informatie.

## Status van nieuwe inzending

Als cursusleider kunt u nu filteren op bestandsinzendingen van studenten op basis van status, revisie beëindigen, In behandeling, Doorgegeven en Mislukt.

Bekijk [de inzendingsstatus](instructors/feature-summary/learners.md#filter-file-submissions) voor meer informatie.

## Verbeteringen in controlelijst

In de Adobe Learning Manager-versie van maart 2024 zijn de verbeteringen aan de controlelijstworkflow als volgt:

### Voortgang bij mislukken van een controlelijst verhinderen

Bij het maken van een controlelijst kan een auteur Inschakelen **selecteren** in de sectie Verplichte controlelijst. Zo voorkomt u dat een leeraar doorgaat in de module als de controlelijst mislukt. Ze kunnen alleen doorgaan als ze de controlelijst doorgeven.

De controlelijstvisoren, dus cursusleiders of managers, kunnen vervolgens de status van de controlelijst controleren. Revisoren kunnen ook de controlelijst voor een leeraar niet aan de orde stellen.

### Herevaluatie van een checklist

Bij het maken van een controlelijst kan een auteur Inschakelen **selecteren** in de sectie Opnieuw evalueren. Als u dit doet, kan een manager of cursusleider een leerling opnieuw evalueren totdat hij voor de controlelijst is geslaagd.

Als de module verplicht is, is het selectievakje voor opnieuw evalueren standaard ingeschakeld.

Een cursusleider of manager kan ook de status van een controlelijst wijzigen van Mislukt in Geslaagd wanneer nieuwe evaluatie is ingeschakeld.

Op de controlelijstpagina kan een cursusleider het aantal studenten zien in de status In behandeling. Als cursusleider kun je een leerling evalueren en deze geslaagd of mislukt. Als een leerling is mislukt, kunt u de controlelijst alleen weergeven als opnieuw evalueren niet is ingeschakeld.

Dit betekent dat het **selectievakje Inschakelen** niet was ingeschakeld in de sectie Opnieuw evalueren tijdens het maken van de controlelijst. Als dit selectievakje is ingeschakeld, zie je de knop Weergeven/Opnieuw evalueren op de pagina Controlelijst voor docenten.

Als u de knop selecteert, kunt u een leerling opnieuw evalueren en markeren dat deze geslaagd of mislukt is.

>[!NOTE]
>
>Beide functies - herevaluatie, en checklist verplicht maken - gelden alleen voor nieuw gemaakte modules. Als een cursus eenmaal is gepubliceerd, kunnen deze niet worden in- of uitgeschakeld.


Ga [naar Create a checklist (Een controlelijst maken](authors/feature-summary/courses.md#checklist-fail) ) voor meer informatie.

## Verdere verbeteringen

### E-mailmeldingen met betrekking tot sessies

In eerdere versies van Adobe Learning Manager had een leerling geen sessiegerelateerde e-mails, Sessiegegevens bijgewerkt, Sessieuitnodiging en Sessieherinnering bijgewerkt als:

* De studenten hebben een cursus voltooid,
* Er worden nieuwe sessies toegevoegd aan een cursus, of
* Er zijn wijzigingen in bestaande sessies.

In de Adobe Learning Manager-versie van maart 2024 zijn de volgende nieuwe wijzigingen:

* Sessiedetails bijgewerkt en sessie-uitnodiging (voor lerende en cursusleider)
   * In toekomstige sessies worden e-mails voor **Sessiegegevens bijgewerkt**, **Uitnodiging** tot sessie voor ingeschreven studenten en huidige cursusleiders verwijderd. In vorige sessies blijven e-mails met **sessiegegevens bijgewerkt** en **een uitnodiging tot een sessie voor** ingeschreven studenten en huidige docenten behouden.
* Herinneringse-mails (voor de beheerder en de leerling)
   * Voor toekomstige sessies worden alleen **e-mails met sessieherinnering** verzonden.

>[!NOTE]
>
>De mails zijn niet afhankelijk van sessie en cursus voltooiing.


### Wijzigingen op de site AEM Reference

Op een AEM Reference-site is ondersteuning toegevoegd voor het toevoegen van een token voor het vernieuwen van de beheerfunctie aan het token voor leerdertoegang.

### Inzendingen van cursusleiders verbergen

Nadat studenten hun bestanden hebben geüpload via de workflow voor bestandsindiening en een cursusleider geen actie onderneemt (goedkeuren of weigeren) bij de inzending, wordt de indienings-URL na een vooraf gedefinieerd aantal dagen verborgen voor de weergave. Neem contact op met de CSAM teams van Adobe Learning Manager om het aantal dagen in te stellen of te wijzigen.

### Wijzigingen in productterminologie

We hebben de kolommen *Instantie* en *Leerling* toegevoegd aan de woordenschat van de productterminologie.

### Wijzigingen in mobiele apps

In deze release van de mobiele app kunnen studenten achterstallig cursusherinneringen plannen en beheren. Als u op een melding voor een achterstallig herinnering klikt, hebt u toegang tot de volgende opties:

* Annuleren
* Naar de cursus
* Herinner me over 3 dagen opnieuw
* Over een week opnieuw herinneren

Op Android: als je op dit bericht klikt, ga je naar de **pagina Cursusoverzicht** .
In iOS: klik op de pushmelding om naar de startpagina van de app te gaan. Dit is een bekende beperking in iOS.

### Wijzigingen controleren in de app Learner in Salesforce

Als een leerling niet kan doorstaan voor een controlelijst, kan hij niet doorgaan naar de volgende module of cursus. Wanneer het selectievakje Verplichte controlelijst is geselecteerd, kan de leerling niet doorgaan in een cursus als hij of zij niet geslaagd is voor de controlelijst.

Net als bij de web-app geldt dat als een lerende een controlelijst in de Salesforce-app mislukt, deze een bericht te zien krijgt en niet doorgaat.

### Wijzigingen in Vc verbinden

In de huidige versies van Adobe Learning Manager wordt een leerling gemarkeerd **als niet aanwezig** wanneer hij of zij is ingeschreven voor een Connect VC-sessie, maar niet voldoet aan de voltooiingscriteria.

In deze versie verandert de status in **Nog te markeren**.

### White labels in Adobe Learning Manager

De mobiele app van Adobe Learning Manager ondersteunt nu whitelabels. Dit betekent dat je de app nu kunt uitbrengen onder je eigen merknaam.

Bekijk whitelabels in [de mobiele app](white-label.md) van Adobe Learning Manager voor meer informatie.

### Nieuwe kolom in migratie-CSV&#39;s

In deze versie wordt er een nieuwe, optionele kolom uniekeLoId weergegeven in de volgende migratie-CSV&#39;s.

* certification.csv
* course.csv
* learning_program.csv

>[!NOTE]
>
>De **kolom uniqueLoId** is optioneel.


Als u een migratie uitvoert om een bestaande cursus of leerplan of certificering bij te werken, wordt de cursus, het leerplan of de certificering met de **uniekeLOId&#39;s** toegevoegd aan de auteurs-app.

Tijdens de migratie moet u de **uniekeLOId-waarden** in de CSV&#39;s bijwerken voor een cursus, leerplan of certificering, ook al is dit een optionele kolom.

Als de **kolom uniqueLoId** niet wordt toegevoegd voordat de migratie wordt uitgevoerd en de bestaande cursus of het leerlidmaatschap bijwerkt of voor een certificering met **uniqueLOId-s**, worden na de migratie de **uniekeLOId-waarden** overschreven door NULL-waarden.

>[!NOTE]
>
>De kolom uniqueLoId **&#x200B;**&#x200B;is niet van toepassing op het BANENHULP-CSV-bestand.


>[!IMPORTANT]
>
>De kolomwaarden moeten uniek zijn voor het hele account. U kunt dezelfde waarde niet gebruiken voor een cursus of certificering.

Download de CSV&#39;s uit de [migratiehandleiding](integration-admin/feature-summary/migration-manual.md#csv-specifications-and-sample-csvs).


### App-classificatie

Een leerling kan feedback geven via de Adobe Learning Manager-app om de ervaring van de app verder te verbeteren. Als de leerling vier sterren of meer beoordeelt, wordt een pop-up weergegeven waarin de leerling wordt gevraagd de app te beoordelen in de Play Store of App Store.

### Bluejeans heeft zijn einde van levensduur (EOL) bereikt in februari 2024

Hierbij willen we u laten weten dat Bluejeans op februari 2024 zijn einde van levensduur (EOL) heeft bereikt. Na februari 2024 zullen Bluejeans geen updates of ondersteuning meer ontvangen. Onze CSAM- en ondersteuningsteams helpen u tijdens deze overgangsperiode bij vragen of problemen.

View [Connectors in Adobe Learning Manager](integration-admin/feature-summary/connectors.md) voor meer informatie over het configureren van connectors.

### Wijzigingen in het rapport Voor aanmeldingstoegang

Het rapport voor aanmeldingstoegang is alleen beschikbaar gedurende de afgelopen vijf kwartalen. Als een integratiebeheerder een aanvraag indient om uniforme export met **toegang tot aanmelding** op aanvraag te downloaden, wordt er een foutbericht weergegeven in Adobe Learning Manager. De andere verslagen zijn echter niet van invloed.

### ADFS-wijzigingen

De velden Employee Type en Employee ID van ADFS zijn nu beschikbaar op Adobe Learning Manager, op basis van de toewijzingen.

## API-wijzigingen in deze versie

### API&#39;s voor studenten

In deze release is API-ondersteuning toegevoegd, zodat studenten het branding-logo en persoonlijke thema&#39;s kunnen weergeven op gebruikersgroepsniveau.

De API&#39;s /account en /user?include=account retourneert vier velden die specifiek worden overschreven die specifiek zijn voor het actieve veld van de gebruiker: logoUrl, logoStyling en themeData.

### Nieuwe kenmerken

Een nieuw kenmerk, isExpiredSubmission, in learningObjectResource, dat aangeeft of de inzending in de resource is verlopen of niet.

* GET /account API: retourneert nieuw kenmerk **expireSubmissionDuration** X, waarbij X het aantal ingestelde dagen is. Als deze niet is ingesteld, wordt 0 geretourneerd
* GET /LO-API met bron bevat het nieuwe kenmerk **isExpiredSubmission**&quot; True of False.
   * True, als de inzending is verlopen en &quot;submissionUrl&quot; niet wordt weergegeven.
   * Als False is verstreken, is de inzending niet verlopen en wordt &quot;submissionUrl&quot; opgehaald.

### API-wijzigingen in controlelijst

Een cursus kan bestaan uit meerdere modules waarvan Checklist een soort module is. Deze controlelijstmodule wordt door de cursusleider geëvalueerd en kan op basis van de evaluatie als Mislukt of Geslaagd worden gemarkeerd.

In beide gevallen is de controlelijststatus echter gemarkeerd als Voltooid en op deze manier wordt de cursus gemarkeerd als Voltooid.

In deze versie bevat de LO-API de parameter *isChecklistMandatory*. Als de waarde True is, is de controlelijst verplicht.

### Ondersteuning voor meerdere landinstellingen

Een beheerder kan het L1-feedbackrapport nu downloaden in de gewenste taal. U kunt echter nog geen L1-feedbackrapporten voor Power BI downloaden. Gebruik in de API-aanvraag de parameter preferredLocale om de gewenste landinstelling op te geven.

### Wijzigingen in het aantal instantiesoverzicht

Dit is van toepassing op accounts met meer dan 1000 inschrijvingen voor een Classroom/VC-cursus.

Als het aantal lager is dan 1000, maken de inschrijvingen de cache ongeldig en worden de bijgewerkte waarden geretourneerd in een GET Summary API-aanroep, zoals het aantal inschrijvingen, voltooiing en seatLimit.

Als het account voor deze functie is ingeschakeld en het aantal inschrijvingen meer dan 1000 is, worden de waarden opgehaald uit de cache.

### Verouderde paden

Momenteel volgen Learning Manager-API&#39;s een structuur voor grafiekgegevens, waarmee u gegevens kunt ophalen door het API-model te doorlopen via includes. U kunt een API tot zeven niveaus doorkruisen, maar het ophalen van de gegevens met behulp van één API-aanroep kost berekeningen.

We raden aan dat alle bestaande en nieuwe klanten meerdere keren kleine gesprekken voeren in plaats van één groot telefoongesprek. Op deze manier voorkomt u dat er ongewenste gegevens in de aanroep worden geladen.

#### Welke paden zijn verouderd

De volgende paden zijn verouderd:

* /learningObjects
   * Verouderde paden:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Bestaande paden:
      * enrollment.loInstance
      * instances.loResources
* /learningObjects/{id}
   * Verouderd pad:
      * enrollment.instances.subLoInstances.learningObject
   * Bestaand pad:
      * enrollment.instances.subLoInstances
* /Inschrijvingen
   * Verouderd pad:
      * loInstance.learningObject.enrollment
   * Nieuw pad:
      * loInstance.learningObject
* /learningObjects/{id}
   * Verouderd pad:
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Nieuw pad:
      * instance.subLoInstances

### Wijzigingen in archivering voor taak-API&#39;s voor aanmeldingstoegang en gebruikerscontrolerapport

In deze versie bewaart de Job API het rapport over aanmeldingstoegang tot maximaal vijf kwartalen en een Rapport voor gebruikerscontrole zes maanden. Als u gegevens die ouder zijn dan deze periode wilt downloaden, moet u de parameter archief doorgeven en kwartaal en jaar opgeven. Raadpleeg de voorbeeldpayload.

```
{
    "data": {
        "type": "job",
        "attributes": {
            "description": "description of your choice",
            "jobType": "generateLoginAccessReport",
            "payload": {
                "fromDate": "2023-04-01T18:30:00.000Z",
                "toDate": "2023-04-30T18:30:00.000Z",
                "archive": {
                    "quarter": "4",
                    "year": "2021"
                }
            }
        }
    }
}
```

Als u het **rapport voor aanmeldtoegang** dat langer dan vijf kwartalen mag duren, probeert te downloaden, verschijnt er een foutbericht. Als u probeert het rapport voor gebruikerscontrole **&#x200B;**&#x200B;te downloaden dat langer duurt dan zes maanden.

### Niet meer ondersteunde API&#39;s

Bekijk [API-verouderde functies in Adobe Learning Manager](api-deprecations-list.md) voor een cumulatieve lijst van alle verouderde API&#39;s in het product.

## Bugfixes in deze update {#bug-fixes}

* Wanneer een leeraar is ingeschreven voor een cursus en vervolgens probeert zich voor een andere cursus in te schrijven, verschijnt er een waarschuwingsbericht.
* Een gebruikersgroep is zichtbaar in Zoeken, zelfs nadat deze is verwijderd.
* Wanneer gebruikers veel transcripties voor studenten met een grote hoeveelheid gegevens activeren, wordt de wachtrij voor de transcripties voor lerende gebruikers geblokkeerd en voorkomt u een nieuwe aanvraag.
* Als een onderliggend account het bovenliggende account vraagt om een rapport te delen, kan het bovenliggende account dit niet doen.
* De URL&#39;s van een cursus en een leerpad worden doorverwezen naar onjuiste locaties.
* Een leerling kan de cursusinstantie van een andere cursus af en toe bekijken door op de cursuskoppeling op de cataloguspagina te klikken.
* De **knop Uitschrijven** wordt niet meer zoals verwacht weergegeven na de eerste inschrijving, maar de knop wordt na een vernieuwing weergegeven.
* Je kunt inhoud of een quiz met een leeg spatievak niet opslaan.
* In door de manager goedgekeurde cursussen kunt u studenten opnieuw inschrijven voor een gebruikersgroep.
* Als u probeert een extra actief veld toe te voegen, verschijnt in bepaalde gevallen het foutbericht &#39;Actieve velden kunnen niet worden opgeslagen&#39;.
* De tekst loopt over in de naam van een cursus binnen een cursuskaart in het gedeelte Gerelateerde cursussen.
* Nadat u overschakelt naar een andere instantie en een leerling hebt ingeschreven voor deze instantie, staan de oude instanties nog steeds in de Outlook-kalender.
* Wanneer een leerling van een collega-account probeert de miniatuur van een cursus te selecteren, wordt er een foutbericht weergegeven.
* Wanneer studenten zich inschrijven voor een cursus, ontvangen ze meerdere meldingen voor de inschrijving.
* Als een gebruiker de naam van de catalogi die in een connector zijn gemaakt, handmatig wijzigt, worden er nieuwe catalogi gemaakt en worden de cursussen gepubliceerd naar onjuiste catalogi.
* Gebruikers die tot inactieve accounts behoren, ontvangen nog steeds lidmaatschapse-mails.

### Opgeloste API-gerelateerde problemen

* API GET/-gebruikers kunnen de gegevens van een manager niet ophalen.
* In een account zijn gebruikers gemaakt via een geplande FTP-importbewerking tijdens een geplande uitvaltijd.
* In de mobiele app of in de immersieve modus wordt, nadat een cursusinstantie is verwijderd of afgehouden en de volgende actieve instantie is geselecteerd, de **knop Interesse** registreren weergegeven in plaats van Inschrijven.**&#x200B;**
* Wanneer een leerling van een peer-account probeert de miniatuur van een cursus te selecteren met behulp van de Leerobject-API, wordt de fout 403 Verboden weergegeven.

## Systeemvereisten

Bekijk de [systeemvereisten](system-requirements.md) voor Adobe Learning Manager.

## Eerdere releases van Adobe Learning Manager

* [Versie van november 2023](whats-new-november-2023.md)
* [Versie van juli 2023](whats-new-2023-july.md)
