---
description: Meer informatie over de nieuwe functies en verbeteringen in de Adobe Learning Manager van maart 2024
jcr-language: en_us
title: Overzicht van nieuwe functies
contentowner: jayakarr
source-git-commit: c58ebebeb671bdb47a752b8f3a9ab673a638dd80
workflow-type: tm+mt
source-wordcount: '3528'
ht-degree: 1%

---



# Overzicht van nieuwe functies {#new-features-summary}

Meer informatie over de nieuwe functies en verbeteringen in Adobe Learning Manager

## Nieuw in deze release {#whatsnewandchanged}

### Vaardigheden importeren uit externe bronnen

Importeer Vaardigheden van contentproviders, zoals LinkedIn en Go1, met behulp van de respectievelijke connectoren. Deze verbetering maakt deel uit van de doelstelling van de Learning Manager om te integreren met externe Skills Clouds en Talent Management Systems. De geïmporteerde vaardigheden worden toegevoegd aan de door de beheerder gedefinieerde vaardigheden in Leerbeheer en zijn beschikbaar voor auteurs tijdens de workflow voor het maken van de cursus. Er zijn ook verbeteringen aangebracht in de zoekfunctionaliteit voor vaardigheden op het hele platform om een betere zoekervaring te bieden wanneer het account een groot aantal vaardigheden heeft.

Weergave [Vaardigheden importeren](administrators/feature-summary/import-skills-external-sources.md) voor meer informatie.

### Aangepaste branding

U kunt nu bepaalde gebruikersinterface-elementen aanpassen, zoals de naam van de organisatie, het logo en het thema van de gebruikersinterface op basis van de gebruikersgroepen die beschikbaar zijn in het account. Een organisatie met meerdere divisies kan bijvoorbeeld een aangepast logo en UI-thema instellen dat voor elke divisie moet worden weergegeven.

>[!NOTE]
>
>Deze functie voor meerdere branding is niet van toepassing op het standpunt van de beheerder. Ze zullen altijd merken op organisatieniveau in hun account zien. Dit komt doordat deze functie voor studenten zichtbaar is en beheerders deze niet in hun account willen opnemen.

Weergave [Meerdere aangepaste branding](administrators/feature-summary/themes.md#multiple-branding) voor meer informatie.


## Wijzigingen voor accounts met een grote gebruikersbasis

### Beheerder- Pagina&#39;s voor cursussen of leerpaden

Als een groot aantal studenten voor de cursus is ingeschreven, bijvoorbeeld meer dan 50.000, wordt de lijst met studenten niet weergegeven. U kunt naar een student zoeken in het dialoogvenster *Studenten zoeken* zoekbalk of selecteer de **Downloaden** link boven aan de zoekbalk om de lijst met studenten te downloaden.

### Beheerder- pagina Studenten

Wanneer u op een gebruiker zoekt, wordt **Student downloaden** en **Exporteren** dezelfde opties downloaden. Tijdens het zoeken naar een gebruikersgroep kunt u nu gefilterde gebruikers downloaden van die gebruikersgroep. Bij het zoeken in een gebruikersgroep wordt **Studentenlijst downloaden** wijzigingen in **Leerlijst voor gebruikersgroep downloaden** De **Exporteren** wordt de gehele lijst gedownload.

### Beheerderspagina - Gebruikers

#### Interne gebruikers

Als het aantal gebruikers bijvoorbeeld 50.000 overschrijdt, wordt er een bericht weergegeven om de gegevens later te downloaden voor een meer gedetailleerde analyse. De zoekbalk is nu prominent aanwezig en geeft een gebruiker weer in de indeling *Naam, e-mail | UUID*.

>[!NOTE]
>
>De UUID wordt alleen weergegeven als UUID is ingeschakeld voor het account.

#### Externe gebruikers

Voor externe gebruikers geldt hetzelfde. Als het aantal gebruikers groot is, kunt u de gebruikers downloaden en ook de gegevens van een gebruiker ophalen na een zoekopdracht in de indeling *Naam, e-mail | UUID*.

#### Pagina Gebruikersopschoning

Op de pagina Gebruikers opschonen hebben we voor verwijderde gebruikers de sorteerfunctie verwijderd op **Datum verwijderd**. U kunt alleen op de UUID&#39;s sorteren.

### Beheerderspagina&#39;s

#### Cursus of leerpad

Als het aantal inschrijvingen groot is, geeft Adobe Learning Manager niet het aantal studenten weer. In plaats daarvan is er een pictogram dat u kunt selecteren, het aantal studenten kunt bekijken en naar de pagina Studenten kunt navigeren.

Het aantal studenten wordt bij benadering weergegeven. Als het aantal studenten bijvoorbeeld meer dan 50.000 is, wordt de waarde weergegeven als 50K+.

### Beheerder- L1/L3-pagina&#39;s

Als het aantal cursusinschrijvingen groot is op de L1-feedbackpagina, wordt de lijst met studenten niet weergegeven. In plaats daarvan kunt u de gebruikerslijst later exporteren voor een gedetailleerdere analyse.

De zoekopdracht ondersteunt automatisch tekst en de resultaten zijn beperkt tot het geselecteerde exemplaar.

#### Pagina Aanwezigheid en scores

Wanneer u op de pagina een gebruiker doorzoekt, wordt de zoekopdracht uitgevoerd in alle beschikbare instanties. Het resultaat is echter voor de geselecteerde instantie.

Als u op de pagina Aanwezigheid zoekt naar een gebruikersgroep en het aantal gebruikers in de gebruikersgroep groter is dan 10.000, ongeacht de inschrijving, kunt u alleen acties op bulkniveau uitvoeren. U kunt de lijst met gebruikers niet weergeven.

Als het aantal gebruikers in de gebruikersgroep minder dan 10.000 is, kunt u afzonderlijke acties op gebruikersniveau en acties op bulkniveau uitvoeren. In dit geval is de gebruikerslijst niet uitgeschakeld.

### Beheerder - pagina Certificeringen

Als er in de huidige versies van Adobe Learning Manager een groot aantal gebruikers is ingeschreven voor een certificering, kunt u de uitgeschreven studenten sinds de **Status** is uitgeschakeld.

Als het aantal ingeschreven gebruikers groot is, wordt in deze versie van Adobe Learning Manager **Status** vervolgkeuzelijst geeft slechts twee opties weer **Ingeschreven** en **Uitgeschreven**. De optie **Ingeschreven** is standaard geselecteerd. Als u **Uitgeschreven** wordt de lijst met uitgeschreven studenten weergegeven.

#### Wijzigingen in gebruikersgroep

Als het aantal gebruikers in de gebruikersgroep lager is dan bijvoorbeeld 50.000, wordt in het geval van een gebruikersgroep het **Status** in het vervolgkeuzemenu ziet u alle opties: Gecertificeerd, Toegewezen en Verlopen.

Als een gebruikersgroep een groot aantal gebruikers bevat, wordt de **Status** vervolgkeuzelijst geeft slechts twee opties weer **Ingeschreven** en **Uitgeschreven**, volgens het nieuwe ontwerp.

### Vergelijkingstabel

<table>
    <tbody>
        <tr>
            <td><b>Pagina</b></td>
            <td><b>Voor drempelwijziging</b></td>
            <td><b>Na wijziging van de drempelwaarde</b></td>
        </tr>
        <tr>
            <td>Beheerder- Cursusinstantie</td>
            <td>Instanties worden als volgt weergegeven:
            <ul>
                <li>Modules</li>
                <li>Ingeschreven studenten</li>
                <li>Sessies</li>
                <li>Badge</li>
                <li>L1-feedback ingeschakeld</li>
                <li>Meldingswaarschuwingen</li>
                <li>Gamification-punten</li>
                <li>QR-code</li>
                <li>Leerpad-extensie</li>
            </ul>
            <td>
                <ul>
                    <li>Als het aantal ingeschreven personen de vooraf gedefinieerde drempel overschrijdt, wordt het aantal niet weergegeven door ALM. Het aantal wordt vervangen door een pictogram dat, wanneer erop wordt geklikt, het werkelijke aantal studenten en een koppeling weergeeft waarmee u naar de pagina Studenten gaat.</li>
                    <li>Het aantal ingeschreven personen wordt bij benadering weergegeven. Als het aantal bijvoorbeeld meer dan 50.000 is, wordt het aantal weergegeven als 50K+ op cursusniveau.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Beheerder- pagina Studenten</td>
            <td>
                    <ul>
                        <li>De lijst met studenten wordt voor elke instantie weergegeven.</li>
                        <li>U kunt zoeken in een gebruiker of gebruikersgroep die voor een cursus is ingeschreven.</li>
                        <li>Het geëxporteerde rapport bestaat niet uit een filter voor Gebruikersgroep.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Selectie van instantie is uitgeschakeld.</li>
                    <li>Download ook de studentenlijst en downloadt dezelfde gegevens, op één geval na. Als u naar een gebruikersgroep zoekt en vervolgens de Studentenlijst downloaden selecteert, worden de gegevens van die gebruikersgroep gedownload.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Beheerder- L1/L3-feedbackpagina</td>
            <td>
                <p>Geen wijziging in bestaand gedrag</p>
            </td>
            <td>
                <ul>
                    <li>Selectie van instantie is uitgeschakeld.</li>
                    <li>Als de inschrijving voor een cursus boven 50 kB ligt, vermeldt ALM geen studenten en wordt alleen de zoekbalk weergegeven. Als de inschrijving minder dan 50 kB is, worden zowel de studentenlijst als de zoekbalk weergegeven.</li>
                    <li>Lijsten is standaard uitgeschakeld.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Beheerder - Pagina Aanwezigheid en scores</td>
            <td>
                <p>Geen wijziging in bestaand gedrag</p>
            </td>
            <td>
                <ul>
                    <li>Selectie van instanties is uitgeschakeld wanneer u een gebruiker zoekt.</li>
                    <li>Als het aantal gebruikers bijvoorbeeld 50.000 overschrijdt, verschijnt er een extra bericht om de gegevens later te downloaden voor een meer gedetailleerde analyse. De zoekbalk is nu prominent aanwezig en geeft een gebruiker weer in de indeling Naam, E-mail | UUID.</li>
                    <li>Als het aantal gebruikers in de gebruikersgroep minder dan 10.000 is, ongeacht de inschrijving, kunt u afzonderlijke acties op gebruikersniveau samen met acties op bulkniveau uitvoeren. In dit geval is de gebruikerslijst niet uitgeschakeld.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Admin-L2 Quiz Score-pagina</td>
            <td>
                    <ul>
                        <li>Gebruikerszoekopdracht wordt ook geïmplementeerd.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Gebruikerszoekopdracht wordt ook geïmplementeerd. Terwijl de typeahead-zoekopdrachten op LO-niveau worden uitgevoerd, wordt de lijst gefilterd naar de geselecteerde instantie.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Beheerder- Gebruikers-pagina (intern, extern)</td>
            <td>
                    <ul>
                        <li>De e-mail-ID wordt weergegeven wanneer een gebruiker wordt gezocht.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Als het aantal gebruikers bijvoorbeeld 50.000 overschrijdt, verschijnt er een extra bericht om de gegevens later te downloaden voor een meer gedetailleerde analyse. De zoekbalk is nu prominent aanwezig en geeft een gebruiker weer in de indeling Naam, E-mail | UUID.</li>
                    <li>Op de pagina Gebruikersopschoning hebben we voor verwijderde gebruikers de sorteerfunctie verwijderd op **Datum verwijderd**. U kunt alleen op de UUID's sorteren.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Docenten - Inzending</td>
            <td>
                    <ul>
                        <li>Paginering van in te dienen modules.</li>
                        <li>Als docent kunt u nu bestandsverzendingen van studenten filteren op basis van status, einde revisie, In afwachting van inzending, Geslaagd en Mislukt. </li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>U kunt alleen in dat geval zoeken naar gebruikers, niet naar gebruikersgroepen.</li>
                </ul>
            </td>
        </tr>
        <tr>
            <td>Tellen bij voorvertoning als studentenpagina</td>
            <td>
                    <ul>
                        <li>Tellen bevat de gegevens van inschrijvingen in een hogere volgorde.</li>
                    </ul>
            </td>
            <td>
                <ul>
                    <li>Met Aantal worden gegevens uitgesloten van inschrijving in hogere volgorde.</li>
                </ul>
            </td>
        </tr>
    </tbody>
</table>

## Geavanceerde zoekmogelijkheden

In deze release hebben we de zoekervaring verbeterd. De zoekresultaten worden niet alleen opgehaald op basis van de metagegevens, maar ook op basis van semantische zoekresultaten en zoekopdrachten in de inhoud om resultaten af te leiden op basis van precisie, recentheid en relevante inhoud.

Deze wijziging heeft betrekking op het volgende:
* Pagina Catalogus en Mijn leerervaring: de aanwijsactie voor de cursus, het leerpad en de certificering is verwijderd.
* De weergave van de zoekbalk.
* Filtertags toegevoegd in de leerapp.

Neem contact op met het CSAM-team van Adobe Learning Manager om de zoekmogelijkheden in te schakelen.

## Wijzigingen in rapporten

* De kolommen Tag(s) en Vaardigheid(en) in het trainingsrapport worden gewijzigd in Tag en Vaardigheden.
* Het rapport is toegevoegd [Audittrail van gamification](administrators/feature-summary/reports.md#gamification-audit-trail).
* Als een account meer dan 280000 studenten bevat die aan een vaardigheid zijn toegewezen, wordt het vaardigheids-studentrapport gedownload als gecomprimeerde CSV.
Als het account minder dan 250000 studenten heeft, wordt hetzelfde rapport gedownload als een CSV-bestand.
Selecteer op de beheerpagina de optie **Beheerder** > **Vaardigheden** > **Vaardigheid** > **Studenten**. Het rapport wordt gedownload als CSV.
* De [Samenvattingsrapport van sessie](administrators/feature-summary/reports.md#session-summary-report) heeft twee nieuwe kolommen: Locatie-informatie en Locatiegebied.

## Wijzigingen in het maken van lesruimten

Gebaseerd op [Beheerdersinstellingen](administrators/feature-summary/classroom.md#classroom-settings)kunt u als auteur [locaties maken, wijzigen en verwijderen](administrators/feature-summary/classroom.md#add-classroom-location).
>[!NOTE]
>
>Tijdens het toevoegen van locatie- en cataloguslabels zien auteurs (op de pagina voor het maken van cursussen) en beheerders (op de instantiepagina) respectievelijk een automatisch gevulde lijst met locaties en cataloguslabels.

Net als beheerder kunt u beperkingen opleggen aan auteurs om een locatie in een lesruimte te wijzigen of te verwijderen. Weergave [Klaslokaalinstellingen](administrators/feature-summary/classroom.md#classroom-settings) voor meer informatie.

## Wijzigingen in flexibel leerpad

Alle accounts (oud en nieuw) in worden gestart, inclusief inschrijvingsdeadline, uitschrijvingsdeadline en plaatslimiet in de Learner-app voor een flexibel leerpad.
Studenten kunnen zich nu inschrijven voor Flexible Learning Path zonder een instantie van de cursus te selecteren.

## Nieuwe trigger voor leerplannen

Er is een nieuwe trigger toegevoegd aan de pagina voor het instellen van het leerplan. Auteurs en beheerders kunnen nu handelingen activeren wanneer een student een module van een cursus niet heeft gehaald.

Weergave [Leerplannen](administrators/feature-summary/learning-plans.md) voor meer informatie.

## Nieuwe verzendstatus

Als docent kunt u nu bestandsverzendingen van studenten filteren op basis van status, einde revisie, In afwachting van inzending, Geslaagd en Mislukt.

Weergave [Verzendstatus](instructors/feature-summary/learners.md#filter-file-submissions) voor meer informatie.

## Verbeteringen voor checklist

In de maart 2024-versie van Adobe Learning Manager zijn de volgende verbeteringen aangebracht in de workflow voor checklist:

### Voortgang bij mislukken van checklist niet toestaan

Bij het maken van een controlelijst kan een auteur **Inschakelen** in de sectie Verplichte checklist. Zo voorkomt u dat een student in de module doorgaat als deze niet aan de controlelijst voldoet. Ze kunnen alleen doorgaan als ze de controlelijst hebben gehaald.

De controleurs, d.w.z. instructeurs of managers, kunnen dan de status van de controlelijst controleren. Revisoren kunnen ook de checklist van een student buiten bestelling controleren.

### Herbeoordeling van een checklist

Bij het maken van een controlelijst kan een auteur **Inschakelen** in de sectie Herbeoordeling. Hiermee kan een manager of docent een student opnieuw evalueren totdat deze de controlelijst doorstaan.

Als de module verplicht is, is het selectievakje voor herevaluatie standaard ingeschakeld.

Een docent of manager kan ook de status van een checklist wijzigen van Niet geslaagd in geslaagd wanneer herevaluatie is ingeschakeld.

Op de pagina Controlelijst ziet een docent het aantal studenten in de status In behandeling. Als docent kunt u een student evalueren en hem of haar laten slagen. Als de status van een student is mislukt, kunt u de controlelijst alleen weergeven als herevaluatie niet is ingeschakeld.

Dit betekent dat de **Inschakelen** Selectievakje is niet geselecteerd in de sectie Herbeoordeling tijdens het maken van de controlelijst. Als dit selectievakje is ingeschakeld, ziet u de knop Weergeven/Opnieuw evalueren op de pagina Controlelijst voor docenten.

Als u de knop selecteert, kunt u een student opnieuw evalueren en markeren dat deze geslaagd of gezakt is.

>[!NOTE]
>
>Beide functies - herevaluatie en verplichte checklist - zijn alleen van toepassing op nieuwe modules. Nadat een cursus is gepubliceerd, kan deze niet in- of uitschakelen.


Weergave [Een checklist maken](authors/feature-summary/courses.md#checklist-fail) voor meer informatie.

## Verdere verbeteringen

### Sessiegerelateerde e-mailmeldingen

In eerdere versies van Adobe Learning Manager heeft een student geen sessiegerelateerde e-mails, sessiedetails bijgewerkt, Sessieuitnodiging en Sessieherinnering verzonden wanneer:

* Studenten hebben een cursus voltooid,
* Nieuwe sessies aan een cursus worden toegevoegd, of
* Er zijn wijzigingen in bestaande sessies.

In de maart 2024-versie van Adobe Learning Manager zijn de volgende wijzigingen aangebracht:

* Sessiedetails bijgewerkt en Sessieuitnodiging (voor student en docent)
   * Voor toekomstige sessies, e-mails voor **Sessiedetails bijgewerkt**, **Uitnodiging voor sessie** voor ingeschreven studenten en huidige docenten worden vervangen. Voor eerdere sessies, e-mails voor **Sessiedetails bijgewerkt** en **Uitnodiging voor sessie** voor ingeschreven studenten en huidige docenten blijven zoals het is.
* E-mails over herinneringen (voor beheerder en student)
   * Alleen voor toekomstige sessies **Sessieherinnering** e-mails worden verzonden.

>[!NOTE]
>
>De mails zijn niet afhankelijk van de voltooiing van de sessie en cursus.


### Wijzigingen op de verwijzingssite AEM

In een AEM-naslagsite hebben we ondersteuning toegevoegd voor het toevoegen van het token voor beheerders vernieuwen aan het toegangstoken voor studenten.

### Inzendingen verbergen voor docenten

Als studenten hun bestanden hebben geüpload met behulp van de workflow voor het verzenden van bestanden en als een docent geen actie onderneemt (goedkeuren of afwijzen) voor de verzending, wordt de URL van de verzending na een vooraf gedefinieerd aantal dagen verborgen in de weergave. Neem contact op met de CSAM-teams van Adobe Learning Manager om het aantal dagen in te stellen of te wijzigen.

### Wijzigingen in productterminologie

We hebben de kolommen toegevoegd *Instantie* en *Student* op de woordenlijst van de productterminologie.

### Wijzigingen in mobiele apps

In deze release van de mobiele app kunnen studenten achterstallige cursusherinneringen plannen en beheren. Als u klikt op een melding voor een verstreken herinnering, hebt u toegang tot de volgende opties:

* Annuleren
* Naar de cursus
* Herinneren over 3 dagen
* Herinneren in een week

Op Android: als u op de pushmelding klikt, wordt de **Cursusoverzicht** pagina.
In iOS: als u op de pushmelding klikt, gaat u naar de startpagina van de app. Dit is een bekende beperking in iOS.

### Wijzigingen in keuzelijst in Learner-app in Salesforce

Als een student een controlelijst niet heeft, kan hij of zij niet verder gaan naar de volgende module of cursus. Wanneer het selectievakje Verplichte checklist is ingeschakeld, kan de student niet verder gaan in een cursus als deze niet aan de checklist voldoet.

Net als bij de webapp ziet een student een bericht als een controlelijst in de Salesforce-app mislukt en gaat niet verder.

### Wijzigingen in Connect VC

In de huidige versies van Adobe Learning Manager wordt een student gemarkeerd **Niet aanwezig** als ze zijn ingeschreven voor een Connect VC-sessie, maar niet aan de voltooiingscriteria voldeden.

In deze release verandert de status in **Toch te markeren**.

### Witte labels in Adobe Learning Manager

De mobiele app van Adobe Learning Manager ondersteunt nu witte labels, wat betekent dat u de app nu onder uw eigen merknaam kunt uitbrengen.

Witte labels weergeven in [Adobe Learning Manager mobiele app](white-label.md) voor meer informatie.

### Toepassingsclassificatie

Een student kan feedback geven over de app Adobe Learning Manager om de app-ervaring verder te verbeteren. Als de student vier sterren of meer telt, verschijnt er een pop-upvenster met een verzoek aan de student om de app te beoordelen in de Play Store of App Store.

### Blauwjeans heeft in februari 2024 zijn einde bereikt

We wilden u laten weten dat Bluejeans op februari 2024 zijn levenseinde (EOL) heeft bereikt. Na februari 2024 ontvangen Bluejeans geen updates of ondersteuning meer. Onze CSAM- en ondersteuningsteams helpen je bij vragen of zorgen die je tijdens deze overgangsperiode hebt.

Weergave [Connectoren in Adobe Learning Manager](integration-admin/feature-summary/connectors.md) voor meer informatie over het configureren van connectoren.

## API-wijzigingen in deze versie

### Student-API&#39;s

In deze release hebben we API-ondersteuning voor studenten toegevoegd om het merklogo en de gepersonaliseerde thema&#39;s weer te geven op het niveau van de gebruikersgroep.

De API&#39;s /account en /user?include=account retourneert vier velden, die specifiek voor het actieve veld van de gebruiker zijn overschreven, behoren tot logoUrl, logoStyling en themeData.

### Nieuwe kenmerken

Een nieuw kenmerk, isExpiredSubmission, in learningObjectResource, dat aangeeft of de verzending in de resource al dan niet is verlopen.

* GET/account-API: retourneert nieuw kenmerk **expiredSubmissionDuration** X, waarbij X het aantal ingestelde dagen is. Indien niet ingesteld, wordt 0 geretourneerd
* GET/LO API met resource bevat nieuw attribuut **isExpiredSubmission**&quot; Waar of Onwaar.
   * True, if the submission is expired and &quot;submissionUrl&quot; is not displayed.
   * Als de waarde Onwaar is, is de verzending niet verlopen en wordt &quot;submissionUrl&quot; opgehaald.

### API-wijzigingen in Checklist

Een cursus kan uit verschillende modules bestaan, waarvan de Checklist een type module is. Deze controlelijstmodule wordt geëvalueerd door de docent en kan worden gemarkeerd als Mislukt of Succes op basis van evaluatie.

Maar in beide gevallen wordt de status van de checklist als Voltooid gemarkeerd en op deze manier wordt de cursus als Voltooid gemarkeerd.

In deze release bevat de LO API de parameter *isChecklistMandatory*. Als de waarde Waar is, is de controlelijst verplicht.

### Ondersteuning voor meerdere landinstellingen

Een beheerder kan nu L1-feedbackrapport downloaden in de taal van zijn of haar keuze. U kunt echter nog geen L1-feedbackrapporten downloaden voor Power BI. Gebruik in de API-aanvraag de parameter preferredLocale om de landinstelling van uw keuze op te geven.

### Wijzigingen in het aantal exemplaren van het overzicht

Dit is van toepassing op accounts waarvoor de inschrijvingen voor een klassikale/VC-cursus groter zijn dan 1000.

Als het aantal minder dan 1000 is, maken de inschrijvingen het geheime voorgeheugen ongeldig en keert de bijgewerkte waarden in een Samenvatting API vraag van de GET, zoals, aantal inschrijving, voltooiing, en seatLimit terug.

Als de account voor deze functie is ingeschakeld en het aantal inschrijvingen groter is dan 1000, worden de waarden opgehaald uit de cache.

### Verouderde paden

Op dit moment volgen API&#39;s van Learning Manager een grafiekgegevensstructuur waarmee u gegevens kunt ophalen door het API-model door include-bestanden te doorlopen. Hoewel u een API tot zeven niveaus kunt doorlopen, is het ophalen van de gegevens met behulp van één API-aanroep computerduur.

Wij adviseren dat alle bestaande en nieuwe klanten kleine vraag veelvoudige tijden in plaats van één grote vraag maken. Deze benadering zal ongewenste gegevens verhinderen in de vraag worden geladen.

#### Welke paden zijn vervangen

De volgende paden zijn afgekeurd:

* /learningObjects
   * Afgekeurde paden:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Bestaande paden:
      * enrollment.loInstance
      * instances.loResources
* /learningObjects/{id}
   * Vervangen pad:
      * enrollment.instances.subLoInstances.learningObject
   * Bestaand pad:
      * enrollment.instances.subLoInstances
* /enrollments
   * Vervangen pad:
      * loInstance.learningObject.enrollment
   * Nieuw pad:
      * loInstance.learningObject
* /learningObjects/{id}
   * Vervangen pad:
      * instance.subLoInstances.learningObject.enrollment.loResourceGrades
   * Nieuw pad:
      * instance.subLoInstances

### Wijzigingen in het archiveringsrapport van aanmeldtoegang en gebruikerscontrole voor taak-API

Met deze release bewaart de API voor aanmelding maximaal vijf kwartalen en een controlerapport van de gebruiker voor zes maanden. Als u de gegevens ouder dan deze tijdsperiode wilt downloaden, moet u de archiefparameter doorgeven, waarbij u een kwartaal en jaar opgeeft. Verwijs naar de monsterlading.

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

Als u de **Toegang tot aanmelding** een rapport dat meer dan vijf kwart gaat, een foutenmelding toont. Er wordt een vergelijkbaar foutbericht weergegeven als u de **Gebruikerscontrole** een verslag dat langer dan zes maanden duurt .

### Verouderde API&#39;s

Weergave [API-afwijzingen in Adobe Learning Manager](api-deprecations-list.md) voor een cumulatieve lijst van alle verouderde API&#39;s in het product.

## Bugfixes in deze update {#bug-fixes}

* Wanneer een student is ingeschreven voor een cursus en vervolgens probeert zich voor een andere cursus in te schrijven, verschijnt er een waarschuwingsbericht.
* Een gebruikersgroep is zichtbaar in Zoeken, zelfs nadat deze is verwijderd.
* Wanneer gebruikers veel studenttranscripten met een grote hoeveelheid gegevens activeren, wordt de wachtrij voor studenttranscripten geblokkeerd en wordt een nieuwe aanvraag voorkomen.
* Als een onderliggend account een verzoek indient om een rapport te delen, kan het bovenliggende account dit niet doen.
* De URL&#39;s van een cursus en leerpad worden omgeleid naar onjuiste locaties.
* Een student bekijkt de cursusinstantie van een andere cursus af en toe door op de cursuskoppeling op de cataloguspagina te klikken.
* De **Uitschrijven** wordt niet weergegeven zoals verwacht na de eerste inschrijving, maar de knop wordt weergegeven nadat de gebruiker is vernieuwd.
* U kunt Inhoud of een Quiz met een lege ruimte in de naam niet opslaan.
* In cursussen die door de manager zijn goedgekeurd, kunt u studenten opnieuw inschrijven voor een gebruikersgroep.
* In sommige gevallen wordt het foutbericht &#39;&#39;Actieve velden kunnen niet worden opgeslagen&#39;&#39; weergegeven als u een extra actief veld probeert toe te voegen.
* De tekst stroomt over in de naam van een cursus binnen een cursuskaart in de sectie Verwante cursussen.
* Nadat u van instantie hebt gewisseld en een student voor de instantie hebt ingeschreven, bestaan de oude exemplaren nog steeds in de Outlook-agenda.
* Wanneer een student van een collega-account de miniatuur van een cursus probeert te selecteren, wordt een foutbericht weergegeven.
* Wanneer studenten zich voor een cursus inschrijven, ontvangen ze meerdere meldingen voor de inschrijving.
* Als een gebruiker de naam van de catalogi die in een connector zijn gemaakt handmatig wijzigt, worden nieuwe catalogi gemaakt en worden de cursussen gepubliceerd naar de onjuiste catalogi.
* Gebruikers die tot inactieve accounts behoren, ontvangen nog steeds e-mails met een abonnement.

### API-gerelateerde bugcorrecties

* De API-GET/gebruikers halen de gegevens van een manager niet op.
* In een account zijn gebruikers gemaakt via een geplande FTP-gebruikersimport tijdens een geplande downtime.
* In de mobiele app of in de immersive modus, nadat u een cursusinstantie hebt verwijderd of gearchiveerd en de volgende actieve instantie hebt geselecteerd, wordt het **Interesse registreren** wordt weergegeven in plaats van **Inschrijven**.
* Wanneer een student van een collega-account de miniatuur van een cursus probeert te selecteren met behulp van de API voor leerobject, wordt de fout 403 Verboden weergegeven.

## Systeemvereisten

Weergave [Systeemvereisten voor Adobe Learning Manager](system-requirements.md).

## Eerdere releases van Adobe Learning Manager

* [Versie van november 2023](whats-new-november-2023.md)
* [Versie van juli 2023](whats-new-2023-july.md)
