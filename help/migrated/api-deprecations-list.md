---
jcr-language: en_us
title: API-implementaties in Adobe Learning Manager
description: Naarmate de API's in Adobe Learning Manager zich ontwikkelen, worden API's periodiek gereorganiseerd of bijgewerkt. Wanneer API's evolueren, is de oude API verouderd en uiteindelijk verwijderd. Deze pagina bevat informatie die u moet weten wanneer u van verouderde API-versies naar nieuwere en stabielere API-versies migreert.
contentowner: saghosh
source-git-commit: 83fdd06aed823a50458d50c8ac240d56af873a6d
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 0%

---


# API-implementaties in Adobe Learning Manager

## API-afwijzingen in de maart 2024-versie van Adobe Learning Manager

### Wijzigingen in snelheidslimieten

Met de volgende release van Adobe Learning Manager herstructureren we API-tarieflimieten voor nieuwe accounts. Voor bestaande accounts zijn alleen de beheer-API&#39;s tariefbeperkt. Na 90 dagen (ongeveer 3 maanden) zullen we de tarieflimieten voor alle API&#39;s herstructureren, maar bestaande accounts worden op de whitelist volgens het huidige gebruik. Bestaande accounts moeten hun API-gebruik voor studenten opnieuw bekijken.

Als ze voor nieuwe accounts de tarieflimieten willen verhogen, moeten ze contact opnemen met het Customer Success-team van ALM.

#### Welke API&#39;s zijn tariefbeperkt

Voor nieuwe accounts gelden tariefbeperkingen voor alle Admin-, Student- en Search-API&#39;s en worden deze afgedwongen.

De API-burstsnelheid of burstlimiet verwijst naar het maximum aantal verzoeken dat in een korte tijd in een beperkte tijd aan een API mag worden gedaan.

In de volgende tabel staan de maximale snelheid en uitbarstingen voor de API&#39;s.

<table>
    <tr>
        <th>API</th>
        <th>Aantal verzoeken-RPM</th>
        <th>Aantal aanvragen-Burst</th>
    </tr>
    <tr>
        <td>Beheerder</td>
        <td>5</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Student</td>
        <td>20</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Zoeken</td>
        <td>50</td>
        <td>5</td>
    </tr>
</table>

### Wijzigingen in verschuivingslimieten

Omdat veel records worden opgehaald door de verschuivingswaarde en de algehele prestaties worden vertraagd, houden we een limiet in voor **500** records. In de volgende release geldt voor zowel de beheerder als de student het **GET Gebruikers** API retourneert maximaal **500** records.

Als u meer records wilt ophalen, gebruikt u de opdracht **GET-taken** API.

De verschuivingslimieten zijn van toepassing op alle nieuwe klanten. Voor bestaande klanten geldt de regel van 90 dagen.

### Paden uitsluiten

Op dit moment volgen API&#39;s van Learning Manager een grafiekgegevensstructuur waarmee u gegevens kunt ophalen door het API-model door include-bestanden te doorlopen. Hoewel u een API tot zeven niveaus kunt doorlopen, is het ophalen van de gegevens met behulp van één API-aanroep computerduur.

Wij adviseren dat alle bestaande en nieuwe klanten kleine vraag veelvoudige tijden in plaats van één grote vraag maken. Deze benadering zal ongewenste gegevens verhinderen in de vraag worden geladen.

We willen deze beperkingen voor nieuwe accounts opleggen en een whitelist van bestaande accounts bijhouden.

#### Welke paden zijn vervangen

De volgende paden zijn afgekeurd:

* /learningObjects
   * Afgekeurde paden:
      * enrollment.loInstance.loResources.resources
      * instances.loResources.resources
   * Nieuwe paden:
      * enrollment.loInstance.loResources
      * instances.loResources

* /learningObjects/{id}
   * Vervangen pad:
      * enrollment.instances.subLoInstances.learningObject
   * Nieuw pad:
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

### Wijzigingen in aantal samenvattingen van instanties

Op dit moment haalt u in het LO-overzichtseindpunt het aantal mogelijke instanties op. U kunt bijvoorbeeld voor een cursus het aantal inschrijvingen en wachtlijsten bekijken in de reactie op **GET /learningObjects/{loId}/instances/{loInstanceId}/summary**. Vervolgens kunt u de informatie over het aantal afhandelingen en het aantal inschrijvingen bekijken in de reactie. Als de cursus een VC of een lesruimte is, kunt u ook de limiet van de zitplaatsen en de wachtlijst bekijken.

Het ophalen van de aantallen voor voltooiing en inschrijving is een kostbare rekenkracht, zodat de berekening op aanvraagbasis wordt uitgevoerd. Als de gegevens niet aanwezig zijn in het cachegeheugen, worden de gegevens opnieuw geladen. Dit is verwerkingsintensief. Als er veel gebruikers zijn die zich inschrijven voor een cursus, zijn de tellingen groot en hebben deze invloed op de CPU-prestaties.

In de volgende versie van de Leermanager van de Adobe, in het overzichtseindpunt van de Instantie LO, worden de completionCount, enrollmentCount, seatLimit, en wachtlistCount in het cachegeheugen ondergebracht. De gegevens in de cache blijven behouden totdat er wijzigingen zijn opgetreden in inschrijvingen of uitschrijvingen. Voor aantallen die meer dan 1000 inschrijvingen tellen, gaan we ervan uit dat de geschatte aantallen zijn en maken we de resultaten ongeldig voor alle bestaande en nieuwe accounts.

>[!NOTE]
>
>Voor tellingen, zoals, completionCount, enrollmentCount, seatLimit, en wachtlistCount groter dan1000, is het raadzaam om hen als schattingen eerder dan nauwkeurige cijfers te interpreteren, aangezien deze uit geheim voorgeheugen zullen worden teruggewonnen.

### Sorteren op naam

In de volgende release van Adobe Learning Manager zijn naam en -naam afgekeurd in het sorteerveld van de volgende API&#39;s:

* GET /userGroups/{userGroupId}/users
* GET/gebruikers

>[!NOTE]
>
>Voor alle bestaande en nieuwe accounts wordt sorteren op naam en -naam afgekeurd.


## API-afwijzingen in de november 2023-versie van Adobe Learning Manager

### Markering overschrijven

In de november 2023-versie van Adobe Learning Manager hebben we de overschrijvingsvlag van de API&#39;s stopgezet. De overschrijvingsvlag maakt geen deel uit van de openbare API-specificatie en is bedoeld voor back-endtesten. De markering wordt nu stopgezet voor studenten-API&#39;s. De markering is echter nog steeds geldig voor Admin API&#39;s.

De reden dat we de markering voor de API&#39;s van de student afschaffen, is omdat de overschrijvingsvlag een grote hoeveelheid gegevens ophaalt via de API&#39;s van de student.

De volgende Learner-API werkt niet meer omdat deze de overschrijvingsvlag heeft.

<code>https://captivateprime.adobe.com/primeapi/v2/users?page[verschuiven]=0&amp;pagina[limiet]=10&amp;sort=id&amp;override=TRUE</code>

### API-wijzigingen voor op vaardigheid gebaseerde nieuwe aanbevelingen

Adobe Learning Manager verbetert de aanbevelingen voor accounts die geschikt zijn voor klanten en partners. Deze verbetering in het aanbevelingsalgoritme met de wijziging in het ranking-algoritme voor cursus, leerpad en certificering biedt een betere gebruikerservaring bij het vinden van inhoud.

Het algoritme staat geen peer-based aanbevelingen meer toe. De wijziging is niet van invloed op de bestaande gebruikers, maar de optie Uitgelijnde sector blijft bestaan. Voor de optie Aangepast staat Adobe Learning Manager geen aangepaste peer-gebaseerde selectie meer toe.

De collega-groep wordt nu een account en studenten zien een tekenreeks met de trending topics in de groep. Alle aanbevelingen kunnen worden uitgelegd. Als u bijvoorbeeld iets op een onderwerp bekijkt, wordt op de kaart op de strook de reden voor de cursus weergegeven.

### Wijzigingen in aankondigingsrapport voor meldingen

In eerdere versies van Adobe Learning Manager bevatte het meldingsrapport geen filters. Adobe Learning Manager heeft alle meldingen in het account gedownload.

In de versie van november 2023 hebben we een datumfilter toegevoegd waarmee u de meldingen binnen een opgegeven periode kunt downloaden.  U kunt het rapport echter alleen voor de laatste zes maanden downloaden.