---
title: Nieuw in deze release
description: Lees meer over de nieuwe functies en verbeteringen in de november 2023-versie van Adobe Learning Manager.
source-git-commit: 1b0a89bf14ed4e48c3da925686d5e2becd94e320
workflow-type: tm+mt
source-wordcount: '2373'
ht-degree: 70%

---

# Nieuw in deze release

## Vernieuwde gebruikersinterface

De gebruikersinterface van de Adobe Learning Manager heeft een paar updates ondergaan om een schonere en modernere ervaring te bieden. De landingspagina&#39;s voor de rollen Beheerder en Auteur zijn vernieuwd en er zijn thema-updates voor de gebruikersinterface gemaakt voor alle rollen. Er zijn echter geen wijzigingen aangebracht in de locatie van menu&#39;s, knoppen of koppelingen en u kunt deze precies vinden op de plaats waar ze eerder waren geplaatst.

De thema-updates worden automatisch toegepast op accounts die het standaardthema gebruiken. De thema-updates voor de gebruikersinterface hebben geen invloed op accounts waarin een aangepast thema wordt gebruikt. Deze accounts moeten worden teruggezet naar het standaardthema om de nieuwe thema-updates te krijgen.

![UI-afbeelding](assets/refreshed-ui.png)

### Over deze wijziging

**Wat verandert er in deze versie?**

De koptekst bevat een nieuwe sjabloon die het logo automatisch verkleint naar een vaste grootte en positie, terwijl de beeldverhouding van het logo behouden blijft. De wijziging is bedoeld om de visuele aantrekkingskracht van de leerervaring te verbeteren.

De naam van de organisatie in de koptekst wordt ook automatisch aangepast naar 336 (minimaal) x 680 (maximaal) pixels voor studenten.

**Wat is de aanbevolen grootte van het logo?**

De maximale breedte van het logo is 210 px. Logo&#39;s met een breedte van meer dan 210 px of een hoogte van meer dan 42 px worden vergroot of verkleind tot 42 x 210 px.

Als de grootte van het logo kleiner is dan de aanbevolen grootte, wordt het logo zonder wijzigingen geüpload en gecentreerd.

**Wat is de impact?**

Bedrijfsnamen die langer zijn, worden ingekort en de ruimte wordt opgevuld met een ellips.

**Wat bevelen we aan?**

* Pas het formaat van de afbeelding aan zodat de beeldverhouding intact blijft. De aanbevolen maximale grootte van het logo is 42 px (verticaal) x 210 px (horizontaal).
* Bij veel accounts wordt deze automatisch toegepast; er is geen wijziging nodig.

## Systeemeigen uitbreidbaarheid

U kunt aangepaste ervaringen instellen in de systeemeigen versie van Adobe Learning Manager, zodat u niet zonder koppen hoeft te werken voor minder ingewikkelde gebruikssituaties. U kunt ook aangepaste apps maken en deze op verschillende punten plaatsen in de systeemeigen versie van de workflows voor studenten, managers, auteurs en docenten.

Een student kan een aangepaste app of een extensie gebruiken die een beheerder heeft gemaakt.

Ga naar [Systeemeigen uitbreidbaarheid](/help/migrated/administrators/feature-summary/native-extensibility.md) voor meer informatie.

## Gereedschap Quiz maken

U kunt nu beoordelingen maken in Learning Manager met het nieuwe gereedschap voor het maken van quiz op de pagina Inhoudsbibliotheek. De gemaakte beoordelingen worden onderdeel van de inhoudsbibliotheek en kunnen worden toegevoegd aan een openbare map voor hergebruik van de cursus.

Weergave [Een quiz maken](/help/migrated/authors/feature-summary/content-library.md) voor meer informatie.

## Rapportagewijzigingen in deze versie

### Wijzigingen in het inschrijvingsrapport voor taakhulp

In eerdere versies van Adobe Learning Manager bevatte het Rapport Inschrijving taakhulpen geen filters. Adobe Learning Manager heeft alle gegevens van een account gedownload.

In deze versie hebben we een vervolgkeuzelijst toegevoegd in het dialoogvenster Taakhulpenrapport.

### Wijzigingen in aankondigingsrapport

In eerdere versies van Adobe Learning Manager bevatte het meldingsrapport geen filters. Adobe Learning Manager heeft alle meldingen in het account gedownload.

In deze versie hebben we een datumfilter toegevoegd waarmee u de meldingen binnen een opgegeven periode kunt downloaden.  U kunt het rapport echter alleen voor de laatste zes maanden downloaden.

### Wijzigingen in cursusrevisiegegevens in inschrijvingsrapport

In deze versie kunt u de revisiegegevens van de cursus downloaden in een inschrijvingsrapport door een tijd op te geven. De downloadperiode wordt beperkt tot zes maanden voor accounts met meer dan vijf miljoen inschrijvingen. Voor alle andere accounts is deze periode 15 maanden.

U kunt het rapport downloaden van **[!UICONTROL Rapporten]** > **[!UICONTROL Aangepaste rapporten]** > **[!UICONTROL Historische verslagen]** > **[!UICONTROL Cursustoegangsrapport]**.

### Wijzigingen in studenttranscript

In eerdere versies van Adobe Learning Manager bevatte het studenttranscript de verwijderde gebruikers als een aangepaste beheerder het bereik Gebruiker had. In deze versie bevat het studenttranscript de verwijderde gebruikers als de aangepaste beheerder het bereik Gebruiker of toegang tot alle gebruikersgroepen heeft.

### Wijzigingen in aanwezigheidsrapport

Het rapport Aanwezigheid op de aanwezigheidspagina van Cursussen in de Admin-app en op de studentensessiepagina van de app voor docenten werd voorheen synchroon gedownload. In deze versie wordt dit rapport asynchroon gedownload via een melding.

Zie voor meer informatie over rapporten [Rapporten](/help/migrated/administrators/feature-summary/reports.md) in Adobe Learning Manager.

## Opheffing van de Inhoudsmarktplaats

Cursussen in de geïmporteerde catalogus van de Inhoudsmarktplaats die zijn verlopen (Enterprise-training), worden automatisch verwijderd. De cursussen worden gearchiveerd als de inhoud is gemarkeerd voor archivering. Bestaande ingeschreven studenten kunnen deze binnen een beperkte tijd volgen, waarna ze worden verwijderd. Zo blijft de catalogus schoon en krijgen gebruikers geen verlopen cursussen te zien.

## Nieuwe aanbevelingen op basis van vaardigheden

Adobe Learning Manager biedt betere aanbevelingen voor accounts van klanten en partners. Dit verbeterde aanbevelingsalgoritme met een gewijzigd classificatiealgoritme voor cursussen, leerpaden en certificeringen zorgt voor een betere gebruikerservaring bij het zoeken naar inhoud.

Het algoritme staat niet langer aanbevelingen op basis van collega&#39;s toe. De wijziging heeft geen invloed op bestaande gebruikers, maar de optie Afgestemd op de branche blijft bestaan. Voor de optie Aangepast staat Adobe Learning Manager niet langer aangepaste selectie op basis van collega&#39;s toe.

De groep collega&#39;s wordt nu een account en studenten krijgen een tekenreeks te zien met de populaire onderwerpen in de groep. Voor elke aanbeveling is een uitleg beschikbaar. Als u bijvoorbeeld iets over een onderwerp bekijkt, wordt op de kaart op de band de reden van de cursus weergegeven.

## Verbeteringen in de workflow voor aangepaste beheerders

Aangepaste beheerders hebben nu gelijkere toegang tot rapporten ten opzichte van beheerdersrollen. Beheerders kunnen de toegang tot rapporten beter configureren.

In Adobe Learning Manager zijn alleen het studenttransscript en gamificatietranscript beschikbaar voor een aangepaste beheerder. In deze versie heeft een aangepaste beheerder toegang tot alle aangepaste rapporten, behalve xAPI- en e-mailrapporten, die nog steeds alleen beschikbaar zijn voor beheerders. Toegang tot alle rapporten is afhankelijk van de catalogus en het gebruikersbereik dat de aangepaste beheerder heeft. Er zijn weinig rapporten die alleen beschikbaar zijn met een volledig bereik. Dat zijn:

<table>
    <tbody>
        <tr>
            <td>
    <p style="text-align: left;"><b>Rapport</b></p></td>
   <td>
    <p style="text-align: left;"><b>Beschikbaar</b></p></td>
   <td>
    <p style="text-align: left;"><b>Bereik</b></p></td>
        </tr>
    <tr>
   <td>
    <p>Audittrail van inhoud</p></td>
   <td>
    <p>Ja</p></td>
   <td>
    <p>Volledige catalogus</p></td>
  </tr>
  <tr>
   <td>
    <p>Audittrail van gebruiker</p></td>
   <td>
    <p>Ja</p></td>
   <td>
    <p>Volledige gebruiker</p></td>
  </tr>
  <tr>
   <td>
    <p>Aanmeldingstoegang</p></td>
   <td>
    <p>Ja</p></td>
   <td>
    <p>Volledige gebruiker</p></td>
  </tr>
    </tbody>
</table>

**Nieuwe alleen-lezen besturingselementen**

Op de pagina Aangepaste rollen hebben we de volgende opties voor Alleen-lezen toegevoegd om beheerders in staat te stellen flexibelere opties te bieden aan de aangepaste beheerder: aangepaste beheerders hebben nu extra machtiging Alleen-lezen voor gebruikers, E-mailsjablonen en leerplannen.

**Gebruikers**:

Als u Alleen-lezen selecteert, kan de aangepaste beheerder alle gebruikers bekijken, maar geen gebruikersgegevens bewerken of een zelfregistratieportaal voor gebruikers maken.

**Leerplannen**:

Als u Alleen-lezen selecteert, kan een aangepaste beheerder geen leerplan toevoegen of bewerken. Ze kunnen een leerplanrapport wel downloaden en de details ervan bekijken. Ze kunnen de cursusdetails echter niet wijzigen.

>[!NOTE]
>
>Leerplannen zijn een extra alleen-lezen-optie en hebben volledige controle.

**E-mailsjablonen**

Als u Alleen-lezen selecteert, kan een aangepaste beheerder de e-mailsjablonen bekijken. Ze kunnen de instellingen van e-mailsjablonen niet in- of uitschakelen, maar kunnen wel rapporten over e-mailtoegang downloaden.

### Studenttranscripten

Als Gebruikersmachtigingen of Alle gebruikersgroepen zijn geselecteerd en aangepaste beheerders proberen Studenttranscripten te downloaden, retourneert de optie Verwijderde student opnemen alle verwijderde studenten in het rapport.

### Rapporten

Een aangepaste beheerder heeft toegang tot de volgende rapporten volgens het opgegeven bereik:

| Rapport | Beschikbaar | Bereik |
|--- |--- |
| Audittrail van inhoud | Ja | Volledige catalogus |
| Audittrail van gebruiker | Ja | Volledige gebruiker |
| Aanmeldingstoegang | Ja | Volledige gebruiker |

## Uitgebreide Connect-integratie

Docenten kunnen hun sessie-ervaring personaliseren door specifieke ruimten voor docenten te selecteren. In deze release zijn de volgende verbeteringen aangebracht:

### Transcripties importeren

U kunt sessietranscripten importeren uit Connect en de transcripties analyseren. Studenten ontvangen het transcript na de opname, die ze later kunnen downloaden.

### Video&#39;s bewerken

Docenten kunnen de video bewerken en de kijkervaring van de studenten verbeteren. Docenten krijgen een link te zien op de overzichtspagina van de sessie die hen naar de aanmeldingspagina van Adobe Connect leidt. Na het aanmelden ziet de docent de opnamelink. Als deze op de link klikt, wordt de docent omgeleid naar de video, die vervolgens kan worden ingekort.

## Dashboardrapporten beperken tot gebruikers met beheerdersrol

Beheerders kunnen alleen managers zoeken in Dashboard-rapporten.

## Verwerking van oude dashboardrapporten beperken

Wanneer een beheerder een dashboardrapport probeert uit te zetten en het rapport te lang duurt om uit te zetten (meer dan 2,5 min.), geeft Adobe Learning Manager het volgende bericht weer:

![oudere rapportafbeelding](assets/error-message.png)
*Foutbericht wanneer rapport te lang duurt*

Rapporten van deze grootte kunnen niet worden weergegeven in de gebruikersinterface, maar de beheerder kan deze wel downloaden.

## Migratieondersteuning voor cataloguslabels

De migratiewerkstroom ondersteunt nu cataloguslabels. CSV&#39;s voor migratie kunnen worden gebruikt om cataloguslabels en cataloguslabelwaarden te importeren en deze toe te voegen aan cursussen, leerpaden, certificeringen en taakhulpen. De werkstroom kan, indien nodig, ook worden gebruikt om onjuiste waarden en sleutels te verwijderen.

## API-verbeteringen voor complexe cursusfilters

Het geavanceerd filteren van cursussen op tags en cataloguslabels (met een combinatie van de voorwaarden AND en OR) is nu mogelijk via Leermanager-API&#39;s.

## API-wijzigingen in deze versie

### Validatie in taak-API

Als in deze release het taakhulprapport groter is dan 10 miljoen die met de taak-API zijn gegenereerd, krijgt het antwoord het bericht &quot;Gevraagd rapport heeft te veel gegevens om te genereren, probeer taakhulpfilters toe te passen!&quot;

### Melding voor een verwijderd bericht

In vorige versies van Adobe Learning Manager kon u, als een cursus, certificering of leerplan was verwijderd en de bijbehorende melding nog actief was, nog steeds toegang krijgen tot de cursus, het certificaat of het leerplan door de melding te openen.

In deze release zorgen we ervoor dat een verwijderd bericht niet meer toegankelijk is. Als u de id opgeeft in /posts/{id} API, en de id voor de post is niet meer beschikbaar, toont API het bericht &quot;Post not found for the specified resource&quot;.

### Voltooiingsdeadline student-API’s

In vorige versies nam Adobe Learning Manager de deadline over van de inschrijvingstabel. In deze versie berekent Adobe Learning Manager de deadline aan de hand van de tabel met cursusinstanties. Als de deadline niet beschikbaar is, wordt de inschrijvingstabel weergegeven.

### Markering overschrijven

In de Adobe Learning Manager-versie van november 2023 verwijderen we de overschrijvingsmarkering uit de API&#39;s. De overschrijvingsmarkering maakt geen deel uit van de openbare API-specificatie en is bedoeld voor back-endtests. De markering wordt nu stopgezet voor student-API&#39;s. De markering is echter nog steeds geldig voor beheerder-API&#39;s.

De reden dat we de markering voor de API&#39;s van de student afschaffen, is omdat de overschrijvingsvlag een grote hoeveelheid gegevens ophaalt via de API&#39;s van de student.

Voortaan zal de volgende student-API niet meer werken omdat deze de overschrijvingsmarkering heeft.

`https://captivateprime.adobe.com/primeapi/v2/users?page[offset]=0&page[limit]=10&sort=id&override=TRUE`

### Resultaten markeren

In de aanstaande versie van Adobe Learning Manager, bijvoorbeeld, in /search API, veranderen wij het gebrek voor highlightResults in vals.

Bovendien, zullen wij het gebrek van snippetTypes in courseName veranderen. Als u dit doet, worden alleen de cursusnamen in de zoekopdracht gemarkeerd als highlightResults True is.

### Nieuw brontype voor quiz

De `instances.loResources.resources` eindpunt wordt geretourneerd `ResourceContentType` met Quiz.

## Kennisgeving van stopzetting

Op 30 november 2023 zal LinkedIn Learning het gebruik van de HTTP GET-methode voor het verkrijgen van een OAuth-token stopzetten. Na de veroudering kunt u alleen een OAuth-token genereren met de HTTP-POST-methode.
Adobe Learning Manager stopt met BlueJeans in februari 2024. Alle nieuwe accounts na februari 2024 hebben geen BlueJeans-connector.

## Aanvullende informatie

Voor informatie over de huidige en vorige releases van de webapp en de apparaatapp van Learning Manager raadpleegt u de [Opmerkingen bij de release](release-note/release-notes.md).

## Bugs die hersteld zijn in deze versie

* Een miniatuur voor een cursus, die een vereiste is voor een leerpad of een andere cursus, wordt niet weergegeven wanneer een deelnemer de voorvertoningspagina van het leerpad of de cursus opent.
* Als de opties Agenda, Gamificatie en Sociaal leren niet zijn geselecteerd, wordt de volgende instelling van het studentendashboard niet opgeslagen. Opties zoals Aanbevolen in uw interessegebieden en Bladeren op catalogus worden niet als geselecteerd weergegeven, maar wel in de voorvertoning.
* Zelfs nadat een student een VC-cursus heeft afgerond, ontvangt de student een herinneringsmail om de cursus te voltooien.
* Voor collega-accounts kunt u geen dashboardrapporten downloaden.
* Het verwijderen en toevoegen van een controlelijstmodule in een cursus resulteert in een interne fout.
* In het geval van sessie-uitnodigingssjablonen bevat de e-mail-ID van de afzender de tekst captivatePrime in plaats van AdobeLearningManager.
* Wanneer u Cursuseffectiviteit als secundaire Y-as gebruikt, mislukt het downloaden van het rapport met een uitzondering van het type Null Pointer.
* Als aan een student de rol van aangepaste beheerder is toegewezen, navigeert deze standaard naar het profiel voor aangepaste beheerders. Als er echter een URL voor omleiding van studenten in het account is ingesteld, wordt de aangepaste beheerder naar een ander doel geleid, en niet naar het profiel voor de rol Aangepaste beheerder.
* Het gamificatiebereik werkt niet zoals verwacht als de optie disabled_sub_groups op een groot getal is ingesteld.
* In sommige gevallen wordt een migratie geactiveerd door verwijderde gebruikers.
* Een student kan geen LinkedIn-cursussen afspelen in de MS Teams-app.
* De inschrijving-API retourneert de inschrijvingen voor een Flexibel leerplan of Geïntegreerd leerplan niet zoals verwacht.
* In de mobiele app worden de namen van een cursus, certificering of leerplan in kleine letters weergegeven.
* In vorige versies van Adobe Learning Manager kon u, als een cursus, certificering of leerplan was verwijderd en de bijbehorende melding nog actief was, nog steeds toegang krijgen tot de cursus, het certificaat of het leerplan door de melding te openen. In deze release zorgen we ervoor dat een verwijderd bericht niet meer toegankelijk is. Als u de id opgeeft in /posts/{id} API, en de id voor de post is niet meer beschikbaar, toont API het bericht &quot;Post not found for the specified resource&quot;.
* In de student-API wordt het veld voor de voltooiingsdeadline niet weergegeven in de reactie van de inschrijving-API.
* In de API Inschrijving ophalen voor studenten worden de inschrijvingsgegevens weergegeven, zelfs nadat u een onjuiste instantie-id hebt opgegeven.

## Bekende problemen in deze versie

* Een nieuwe inschrijving of het bijwerken van een inschrijving mislukt wanneer een Flexibel leerplan zich in een ander Flexibel leerplan bevindt.
* De transcript-URL geeft de sessieopnamen niet weer in Adobe Connect-sessies.
* Een student kan een offline quiz afleggen in de mobiele app, zelfs als de student niet slaagt.

## Systeemvereisten

[Learning Manager-systeemvereisten](system-requirements.md)

## Eerdere releases van Adobe Learning Manager

* [Versie van juli 2023](whats-new-2023-july.md)
* [Versie van april 2023](whats-new-2023-april.md)
* [Versie van november 2022](whats-new-2022-november.md)
