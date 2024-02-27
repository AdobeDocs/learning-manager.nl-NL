---
jcr-language: en_us
title: API-implementaties in Adobe Learning Manager
description: Naarmate de API's in Adobe Learning Manager zich ontwikkelen, worden API's periodiek gereorganiseerd of bijgewerkt. Wanneer API's evolueren, is de oude API verouderd en uiteindelijk verwijderd. Deze pagina bevat informatie die u moet weten wanneer u van verouderde API-versies naar nieuwere en stabielere API-versies migreert.
contentowner: saghosh
source-git-commit: 24c886fcd9448b7f1d71526794a3c46a0f91d017
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 21%

---


# API-veroudering en wijzigingen in Adobe Learning Manager

## API-afwijzingen in de maart 2024-versie van Adobe Learning Manager

<!-- ### Changes in Rate Limits

With the next release of Adobe Learning Manager, we're restructuring API rate limits for new accounts. For existing accounts, only the Admin APIs will be rate-limited. After 90 days (about 3 months), we will restructure rate limits for all APIs, but existing accounts will be whitelisted according to current usage. Existing accounts need to revisit their learner API usage. 

For new accounts, if they want to increase the rate limits, they must contact the Customer Success team of ALM. 

#### Which APIs will be rate limited 

For new accounts, all Admin, Learner, and Search APIs will have rate limits and burst enforced.  

The API burst rate or burst limit refers to the maximum number of requests allowed to be made to an API in a short burst within a limited timeframe. 

The following table lists the rate and burst limits for the APIs.

<table>
    <tr>
        <th>API</th>
        <th>Number of requests-RPM</th>
        <th>Number of requests-Burst</th>
    </tr>
    <tr>
        <td>Admin</td>
        <td>5</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Learner</td>
        <td>20</td>
        <td>5</td>
    </tr>
    <tr>
        <td>Search</td>
        <td>50</td>
        <td>5</td>
    </tr>
</table>
-->

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

In de november 2023-versie van Adobe Learning Manager hebben we de overschrijvingsvlag van de API&#39;s stopgezet. De overschrijvingsmarkering maakt geen deel uit van de openbare API-specificatie en is bedoeld voor back-endtests. De markering wordt nu stopgezet voor student-API&#39;s. De markering is echter nog steeds geldig voor beheerder-API&#39;s.

De reden dat we de markering voor de API&#39;s van de student afschaffen, is omdat de overschrijvingsvlag een grote hoeveelheid gegevens ophaalt via de API&#39;s van de student.

Voortaan zal de volgende student-API niet meer werken omdat deze de overschrijvingsmarkering heeft.

<code>https://captivateprime.adobe.com/primeapi/v2/users?page[verschuiven]=0&amp;pagina[limiet]=10&amp;sort=id&amp;override=TRUE</code>

### API-wijzigingen voor op vaardigheid gebaseerde nieuwe aanbevelingen

Adobe Learning Manager biedt betere aanbevelingen voor accounts van klanten en partners. Dit verbeterde aanbevelingsalgoritme met een gewijzigd classificatiealgoritme voor cursussen, leerpaden en certificeringen zorgt voor een betere gebruikerservaring bij het zoeken naar inhoud.

Het algoritme staat niet langer aanbevelingen op basis van collega&#39;s toe. De wijziging heeft geen invloed op bestaande gebruikers, maar de optie Afgestemd op de branche blijft bestaan. Voor de optie Aangepast staat Adobe Learning Manager niet langer aangepaste selectie op basis van collega&#39;s toe.

De groep collega&#39;s wordt nu een account en studenten krijgen een tekenreeks te zien met de populaire onderwerpen in de groep. Voor elke aanbeveling is een uitleg beschikbaar. Als u bijvoorbeeld iets over een onderwerp bekijkt, wordt op de kaart op de band de reden van de cursus weergegeven.

### Wijzigingen in aankondigingsrapport voor meldingen

In eerdere versies van Adobe Learning Manager bevatte het meldingsrapport geen filters. Adobe Learning Manager heeft alle meldingen in het account gedownload.

In de versie van november 2023 hebben we een datumfilter toegevoegd waarmee u de meldingen binnen een opgegeven periode kunt downloaden.  U kunt het rapport echter alleen voor de laatste zes maanden downloaden.