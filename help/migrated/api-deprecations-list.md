---
jcr-language: en_us
title: API-implementaties in Adobe Learning Manager
description: Naarmate de API's in Adobe Learning Manager zich ontwikkelen, worden API's periodiek gereorganiseerd of bijgewerkt. Wanneer API's evolueren, is de oude API verouderd en uiteindelijk verwijderd. Deze pagina bevat informatie die u moet weten wanneer u van verouderde API-versies naar nieuwere en stabielere API-versies migreert.
contentowner: saghosh
exl-id: 0fe9a3cb-9114-42d6-81ae-1a4f28c984fa
source-git-commit: 670d0477b246af2a0257e41eca799817e391b348
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 32%

---

# API-afwijzingen en -wijzigingen in Adobe Learning Manager

## API-afwijzingen in de Adobe Learning Manager-versie van maart 2024

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

<!--### Exclude paths 

At present, Learning Manager APIs follow a graph data structure, which allows you to fetch data by traversing the API model through includes. Even though you could traverse an API up to seven levels, fetching the data using a single API call is computationally expensive. 

We recommend that all existing and new customers make small calls multiple times instead of one large call. This approach will prevent unwanted data from being loaded in the call. 

We want to enforce these restrictions on new accounts and maintain a whitelist of existing accounts.-->

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

<!--### Instance summary count changes 

Currently, in the LO summary endpoint, you fetch the number of all possible instances. For example, for a course, you can view the number of enrollments and waitlists in the response for **GET /learningObjects/{loId}/instances/{loInstanceId}/summary**. You can then view the completionCount and enrollmentCount in the response. If the course is a VC or classroom, you can also view its seat limit and waitlist limit. 

The process of retrieving the completion and enrollment counts is computationally expensive, therefore the calculation is done on a request basis. If the data is not present in the cache, the data is reloaded, which is computationally intensive. If there are many users enrolling in a course, the counts will be large, and effectively impacts CPU performance. 

In the next release of Adobe Learning Manager, in the LO Instance summary endpoint, the completionCount, enrollmentCount, seatLimit, and waitlistCount are cached. The cached information persists till there are changes in enrollments or unenrollments. For counts exceeding 1000 enrollments, we'll assume the estimated counts, and invalidate the results for all existing and new accounts.

>[!NOTE]
>
>For counts, such as, completionCount, enrollmentCount, seatLimit, and waitlistCount exceeding1000, it's advisable to interpret them as estimates rather than precise figures, as these will be retrieved from cache.-->

### Sorteren op naam

In de volgende versie van Adobe Learning Manager zijn naam en -naam afgekeurd in het sorteerveld van de volgende API&#39;s:

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

_/primeapi/v2/users?page[verschuiven]=0&amp;pagina[limiet]=10&amp;sort=id&amp;override=TRUE_

### API-wijzigingen voor op vaardigheid gebaseerde nieuwe aanbevelingen

Adobe Learning Manager biedt betere aanbevelingen voor accounts van klanten en partners. Dit verbeterde aanbevelingsalgoritme met een gewijzigd classificatiealgoritme voor cursussen, leerpaden en certificeringen zorgt voor een betere gebruikerservaring bij het zoeken naar inhoud.

Het algoritme staat niet langer aanbevelingen op basis van collega&#39;s toe. De wijziging heeft geen invloed op bestaande gebruikers, maar de optie Afgestemd op de branche blijft bestaan. Voor de optie Aangepast staat Adobe Learning Manager niet langer aangepaste selectie op basis van collega&#39;s toe.

De groep collega&#39;s wordt nu een account en studenten krijgen een tekenreeks te zien met de populaire onderwerpen in de groep. Voor elke aanbeveling is een uitleg beschikbaar. Als u bijvoorbeeld iets over een onderwerp bekijkt, wordt op de kaart op de band de reden van de cursus weergegeven.

### Wijzigingen in aankondigingsrapport voor meldingen

In eerdere versies van Adobe Learning Manager beschikte het meldingsrapport niet over filters. Adobe Learning Manager heeft alle meldingen in het account gedownload.

In de versie van november 2023 hebben we een datumfilter toegevoegd waarmee u de meldingen binnen een opgegeven periode kunt downloaden.  U kunt het rapport echter alleen voor de laatste zes maanden downloaden.

### Veroudering van hoge verschuivingswaarden in GET/gebruikers-eindpunt

Om systeemprestaties te verbeteren en middelgebruik effectiever te beheren, heeft de Adobe hoge compensatiewaarden in het GET /users eindpunt voor allebei vervangen **ADMIN** en **STUDENT** bereik. We raden u aan de **Job API** om de records met een verschuivingswaarde op te halen.

