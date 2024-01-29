---
title: Nieuwe functies in deze release (juli 2023)
description: Meer informatie over de nieuwe functies en verbeteringen in Adobe Learning Manager
hidefromtoc: true
source-git-commit: c55f9448082c9971c065eec95b59992db95e53dc
workflow-type: tm+mt
source-wordcount: '2052'
ht-degree: 0%

---

# Nieuwe functies in deze release (juli 2023)

## Verbeterde aanbevelingen

Adobe Learning Manager heeft een nieuw en vernieuwd aanbevelingssysteem voor cursussen geïntroduceerd. Deze aanbevelingsfunctie gebruikt AI-algoritmen en gebruikersinteresses zoals Producten, Rollen en Niveaus om gepersonaliseerde contentaanbevelingen te bieden.

Zie voor meer informatie [Recommendations in Adobe Learning Manager](recommendations-adobe-learning-manager.md).

## Meerdere inschrijvingen

In deze versie van Adobe Learning Manager introduceren we meervoudige inschrijvingen voor studenten waarmee studenten zich in meer dan één instantie van een cursus op een of verschillende tijdsperioden kunnen inschrijven.

Zie voor meer informatie [Meerdere inschrijvingen](/help/migrated/authors/feature-summary/courses.md).

### Meerdere inschrijvingen in mobiele app of meeslepend

Studenten kunnen zich niet in meerdere instanties inschrijven via een mobiele app/immersive. Meerdere inschrijvingen wordt niet ondersteund in mobiele apps en immersive mobile web.

>[!NOTE]
>
>Als u meerdere inschrijvingen inschakelt, worden er meerdere rijen toegevoegd aan het Studenttranscriptrapport voor elke cursus (één rij voor elke instantie).
>
>Als u een automatiseringsinstelling hebt ingesteld die slechts één rij per cursus verwacht, moet u de vereiste aanpassingen in de rapportautomatisering aanbrengen voordat u de functie voor meervoudige inschrijving inschakelt.

### Indeling van badges in een meervoudig ingeschreven instantie

Om badges in een meervoudig ingeschreven instantie te ondersteunen, wordt de badgeindeling gewijzigd in `userId_badgeId_COURSE_courseId_courseInstanceId`.

### De speler starten in meerdere inschrijvingen in de headless modus

In deze release is de bibliotheek gewijzigd die wordt gebruikt voor communicatie met de headless Player.

Bij meervoudige inschrijving moet u de argumenten doorgeven die in een object zijn verpakt.

```
{{startplayer(argument_object) ,
where
argument_object=
{ loId = <loId>, accountId = <accountId>, userId =<userId>, accessToken = <accessToken>, domId = <elementId>, onModuleLoaded = fn(), isMultiEnrolled=<boolean>, instanceId=<instanceId> }
}}
```

## Veroudering van de buitenaardse connector

Deze release van Adobe Learning Manager bevat een nieuwe connector, die gebruikmaakt van het SFTP-protocol van de AWS Transfer-familie.

Deze wijziging vervangt ook de ExaVault-connector, die niet meer beschikbaar is voor nieuwe gebruikers. U kunt elke opensource FTP-client gebruiken als vervanging voor ExaVault. Zie voor meer informatie [Overgang van Adobe FTP Manager](transition-from-ftp-manager.md).

## Herinneringen in vooruitzichten voor klassikale en virtuele sessies

Sessies in de lesruimte en de virtuele lesruimte die zijn gemaakt met de Adobe Learning Manager en die zijn toegevoegd aan de Outlook-agenda van de student, ondersteunen nu consistent herinneringen vanuit Outlook (vergelijkbaar met herinneringen voor vergaderingen in Outlook).

## Verbeteringen voor het toewijzen van vaardigheden aan cursussen

We hebben de workflow voor vaardigheden van auteurs verbeterd. De lijst met vaardigheidssuggesties op de pagina Instellingen van de cursus bevat nu een zoekfunctie voor de typekop. Auteurs kunnen nu zoeken naar Vaardigheden door de eerste paar tekens te typen. Suggesties worden weergegeven in de vervolgkeuzelijst Vaardigheid op basis van de invoer. Dankzij deze verbetering hoeven auteurs niet door de volledige lijst te schuiven om vaardigheden aan cursussen te zoeken en toe te wijzen.

## Verbeteringen van de cursusworkflow die door de manager is goedgekeurd

Door de manager goedgekeurde cursussen bieden nu de juiste foutinformatie aan zowel managers als studenten.

![foutberichten](assets/error-messages.png)

Managers kunnen nu relevante foutberichten met informatie bekijken (de inschrijvingsdeadline is bijvoorbeeld verstreken) wanneer ze een inschrijvingsverzoek voor een cursus niet kunnen goedkeuren. Studenten zien de fout en de herstelactie.

## Rapport over nieuw leerplan

Beheerders/aangepaste beheerders kunnen nu een lijst met alle leerplannen in het account en metagegevens exporteren, zoals status, toepasselijke gebruikersgroepen, triggerinformatie, cursussen/leerpaden die in het leerplan zijn opgenomen, en herinneringsgegevens.

## Rapport voor het bijhouden van aanstaande gearchiveerde instanties

Het trainingsrapport bevat een extra kolom voor het weergeven van de deadline voor voltooiing van de instanties in de cursussen of leerpaden, zodat beheerders en auteurs weten welke instanties worden gearchiveerd en de nodige actie kunnen ondernemen.

## Verbeteringen om cursusbeoordelingen van studenten vast te leggen

Een pop-up om de sterrenclassificatie voor een cursus vast te leggen, wordt weergegeven zodra de gebruiker de laatste module in de cursus heeft voltooid.

![beoordelingen](assets/ratings.png)

## E-mailsjablonen aanpassen

E-mailsjablonen in Leermanager bevatten nu volledig bewerkbare secties die meer flexibiliteit bieden om e-mailcommunicatie aan te passen op basis van voorkeuren voor berichten en branding.

Zie voor meer informatie [E-mailsjabloon aanpassen](/help/migrated/administrators/feature-summary/email-templates.md#flexibility-in-customizing-the-templates).

## Verbeteringen voor het plannen van de assistent

Verfijn het proces waarbij u een docent selecteert voor klassikale of virtuele sessies. Er is een filter Gebruikersgroep toegevoegd aan het veld Docent in de Planningsassistent. Auteurs kunnen nu filteren op docenten op basis van &#39;Vaardigheden van docenten&#39; en op aanvullende parameters zoals locatie, taal, aanduiding, enzovoort.

Zie voor meer informatie [Filter Gebruikersgroep in Planningsassistent](/help/migrated/authors/feature-summary/courses.md#user-group-filter).

## Verbeteringen aan de workflow voor het archiveren van leerobjecten

Auteurs kunnen nu een **Auto Reband** datum voor een cursus. Zo voorkomt u dat de catalogus in de loop der tijd opraakt en dat de cursussen handmatig moeten worden gearchiveerd.

Beheerders kunnen ook op accountniveau bepalen wat de toegang is tot gearchiveerde leerobjecten.

Het trainingsrapport bevat een nieuwe kolom, **Datum van automatische aflossing** om de pensioendatum voor elk leerobject weer te geven (indien ingesteld).

## Cataloguslabelwaarden door auteurs

Auteurs kunnen nu hun waarden voor cataloguslabels toevoegen tijdens het maken of bewerken van een cursus. Beheerders kunnen deze functie op accountniveau inschakelen. Nadat een auteur een nieuwe cataloguslabelwaarde heeft toegevoegd, wordt deze onderdeel van de zoekopdracht naar de typekop.

![catalogus selecteren](assets/select-catalog.png)

## Verbeteringen voor het zoeken naar beheerdersrollen, auteur- en managerrollen

Er zijn zoekverbeteringen doorgevoerd voor de beheerdersrollen, auteur- en managerrollen. Ze kunnen nu met trefwoorden zoeken naar de titels. Dit geldt voor cursussen, leerpaden en certificeringen.

## Meldingen voor migratiefouten

Integratiebeheerders worden via e-mail op de hoogte gesteld als een import- of exportbewerking mislukt tijdens de migratie of tijdens het gebruik van dataconnectoren zoals PowerBI, FTP, Box, enz.

## Configuratie met meerdere managers via API&#39;s

Er is een nieuwe API toegevoegd aan de set met API&#39;s voor beheerde kantoren ter ondersteuning van de configuratie voor meerdere managers.

## Verbeteringen in de API voor aanmelding

De API voor inschrijving is verbeterd en biedt nu ondersteuning voor grootschalige inschrijvingen en optimaliseert deze.

## Mobiele app - Offline content weergeven

Studenten kunnen inhoud downloaden en gebruiken in de offline modus. Geneste en flexibele leerpaden worden niet ondersteund voor offline weergave.

*In deze release wordt het weergeven van offline inhoud alleen ondersteund voor Engelse inhoud.*

## Toegankelijkheid

Er zijn meerdere verbeteringen geïmplementeerd om de toegankelijkheid te verbeteren, waaronder verbeteringen om de leesbaarheid voor schermlezers te optimaliseren.

## Ondersteuning voor mobiele apps

Met de volgende grote release ondersteunt de mobiele app van Adobe Learning Manager alleen de drie meest recente mobiele OS-versies.

## Inhoud op LinkedIn

LinkedIn-inhoud wordt niet zoals verwacht geladen in de Immersive-app in de Safari-browser. Voer als tijdelijke oplossing de volgende handelingen uit:

1. Selecteer op het apparaat **[!UICONTROL Instellingen]** > **[!UICONTROL Safari]**.
1. Uitschakelen **Volgen tussen sites voorkomen**.
1. Uitschakelen **Alle cookies blokkeren**.
1. Meld u aan bij de Immersive-app.
1. Speel de inhoud af.
1. Laat pop-ups toe.

## Andere verbeteringen

### Overschakelen op instanties in MS Teams

Een student kan overschakelen op een andere cursusinstantie totdat deze is voltooid en de voortgang van de cursus behouden.

### Ondersteuning voor meervoudige inschrijving in MS Teams

Een student kan zich in een andere cursusinstantie inschrijven, ongeacht de voltooiingsstatus bij eerdere instanties. De student wordt dan in meerdere instanties van dezelfde cursus ingeschreven.

### Cursusnotities bieden ondersteuning voor meervoudige inschrijving in MS-teams

Cursusnotities zijn beschikbaar op cursusinstantieniveau ter ondersteuning van meervoudige inschrijving.

## API-wijzigingen

Voor meer informatie over de API-wijzigingen raadpleegt u de [Adobe Leermanager-API-referentie](https://captivateprime.adobe.com/docs/primeapi/v2/).

### API-ondersteuning voor nieuwe aanbevelingen

**GET /account**

Retourneert of prlRecommendation is ingeschakeld.

**Verzoek**

`https://learningmanagerstage1.adobe.com/primeapi/v2/account`

**GET /data?filter.aanbevelingCriteria=product**

Retourneert een lijst met producten/onderwerpen. De resultaten zijn afhankelijk van accountinstellingen die bevestigen of alle producten zichtbaar zijn voor de student of voor de producten/onderwerpen in de catalogus.

**Verzoek**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=product&filter.showAllRecommenda`

**`GET /data?filter.recommendationCriteria=role`**

Hiermee wordt de lijst met aanbevolen rollen geretourneerd.

**Verzoek**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=role&filter.showAllRecommendationCriteria=false`

**`GET /data?filter.recommendationCriteria=level`**

Hiermee wordt de lijst met aanbevolen rollen geretourneerd.

**Verzoek**

`https://learningmanagerqe.adobe.com/primeapi/v2/data?filter.recommendationCriteria=level&filter.showAllRecommendationCriteria=false`

**POST/zoekopdracht/query**

Het onderzoek omvat ook producten en rolparameters in vraag. Er is geen verandering in vraag en lichaam. We voegen nieuwe sorteeropties toe

**Verzoek**

`https://learningmanagerstage1.adobe.com/primeapi/v2/search/query?...`

**GET /learningObjects**

Het model van het leerobject retourneert door de auteur gecodeerde aanbevelingen als de PRL-aanbeveling live is.

**URL aanvragen**

`https://learningmanagerstage1.adobe.com/primeapi/v2/learningObjects?sort=recommendationScore&filter.recommendationProducts=...&filter.recommendationRoles=...&filter.excludeIgnoredRecommendations=true`

POST/learningObjects/query

De volgende attributen worden gesteund in het lichaam van vraagvraag:

```javascript {line-numbers="true"}
{
  "filter.announcedGroups": [
    "string"
  ],
  "filter.bookmarks": true,
  "filter.catalogIds": [
    "string"
  ],
  "filter.cityName": [
    "string"
  ],
  "filter.duration.range": [
    "string"
  ],
  "filter.effectiveModifiedDate.fromDate": "string",
  "filter.effectiveModifiedDate.toDate": "string",
  "filter.excludeIgnoredRecommendations": true,
  "filter.ignoreEnhancedLP": true,
  "filter.ignoreHigherOrderLOEnrollment": true,
  "filter.lang.subLOs": true,
  "filter.lang.twoLetterCode": true,
  "filter.learnerState": [
    "string"
  ],
  "filter.loFormat": [
    "string"
  ],
  "filter.loTypes": [
    "string"
  ],
  "filter.price": "string",
  "filter.priceRange": [
    "string"
  ],
  "filter.recommendationLevels": [
    "string"
  ],
  "filter.skill.level": [
    "string"
  ],
  "filter.skillName": [
    "string"
  ],
  "filter.tagName": [
    "string"
  ],
  "language": [
    "string"
  ],
  "preferredSortPartitionOrder": [
    "string"
  ],
  "showLoContentSource": true,
  "useCache": true,
  "filter.recommendationProducts": [
    {
      "levels": [
        "string"
      ],
      "name": "string"
    }
  ],
  "filter.recommendationRoles": [
    {
      "levels": [
        "string"
      ],
      "name": "string"
    }
  ]
}
```

**GET /aanbevelingProducts**

Hiermee wordt het PRL-product opgehaald op aanbevelingProduct ID.

**URL aanvragen**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationProducts`

GET /aanbevelingRoles

Hiermee wordt het PRL-product opgehaald op aanbevelingProduct ID. Alleen zichtbare rollen van (leerobjecten) worden geretourneerd.

**URL aanvragen**

`https://learningmanagerstage1.adobe.com/primeapi/v2/prlRecommendations/roles`

`POST /users/{id}/recommendationPreferences`

Hiermee maakt u voorkeuren voor PRL-aanbevelingen (overschrijven) en maakt u deze opnieuw. Voorbeeld van lading:

```javascript {line-numbers="true"}
{
    "data": {
        "id": "userRecommendationPreferences:14755328",
        "type": "userRecommendationPreferences",
        "attributes": {
            "products": [
                {
                    "id": "recommendationProduct:1",
                    "dateCreated": "2023-05-07T20:00:00.000Z"
                },
                {
                    "id": "recommendationProduct:37",
                    "dateCreated": "2023-05-07T21:00:00.000Z"
                }
            ],
            "roles": [
                {
                    "id": "recommendationRole:23",
                    "dateCreated": "2023-05-07'T'21:00:00.000'Z'"
                },
                {
                    "id": "recommendationRole:1",
                    "dateCreated": "2023-05-07'T'20:01:00.000'Z'"
                },
                {
                    "id": "recommendationRole:2",
                    "dateCreated": "2023-05-07'T'19:02:00.000'Z'"
                },
                 {
                    "id": "recommendationRole:3",
                    "dateCreated": "2023-05-07'T'18:02:00.000'Z'"
                },
                {
                    "id": "recommendationRole:20",
                    "dateCreated": "2023-05-07'T'17:02:00.000'Z'",
                    "levels": [
                        "INTERMEDIATE"
                    ]
                }
            ]
        }
    }
}
```

**`GET /users/{id}/recommendationPreferences`**

**URL aanvragen**

`https://learningmanagerstage1.adobe.com/primeapi/v2//users/123/recommendationPreferences`

**`DELETE /users/{id}/recommendationPreferences`**

Verwijdert de voorkeuren van de PRL-aanbevelingen voor gebruikers van een product of rol.

**URL aanvragen**

`https://learningmanagerstage1.adobe.com/primeapi/v2/users/123/recommendationPreferences?ids=recommendationRole:123,recommendationRole:234`

Params:

Id&#39;s = lijst met id&#39;s die moeten worden verwijderd

**PATCH /gebruikers/{id}/aanbevelingPreferences**

Gedeeltelijke toevoeging/upgrade. Voorbeeld van lading:

```javascript {line-numbers="true"}
{
  "data": {
    "id": "userRecommendationPreferences:<USER_ID>",
    "type": "userRecommendationPreferences",
    "attributes": {
      "roles": [
        {
          "id": "recommendationRole:123",
          "type": "recommendationRole",
          "attributes": {
            "levels": [
              "INTERMEDIATE"
            ]
          }
        },
        {
          "id": "recommendationRole:123",
          "type": "recommendationRole",
          "attributes": {
            "levels": [
              "ADVANCED"
            ]
          }
        }
      ]
    }
  }
}
```

**POST/aanbevelingPreferences/learningObjects/{id}/ignore**

LO toevoegen aan geblokkeerde aanbevelingen.

**URL aanvragen**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationPreferences/learningObjects/{id}/ignored`

**`DELETE /recommendationPreferences/learningObjects/{id}/ignore`**

Verwijdert LO uit geblokkeerde aanbevelingen.

**URL aanvragen**

`https://learningmanagerstage1.adobe.com/primeapi/v2/recommendationPreferences/learningObjects/{id}/ignored`

**`GET /users/{id}/recommendationStrips`**

Hiermee worden alle strips opgehaald die moeten worden gebruikt om aanbevelingen voor prl weer te geven

### Ondersteuning voor meerdere inschrijvingen voor API

**GET /primeapi/v2/account**

Er worden twee nieuwe kenmerken toegevoegd:

* instanceSwitchEnabled
* multiEnrollmentEnabled

**GET /gebruikers/{userId}/userNotifications**

Id van cursusinstantie toegevoegd in meldingen in het nieuwe metagegevenskenmerk.

**GET /learningObjects**

De inschrijvingsrelatie geeft alleen de primaire inschrijving weer, dus eerst ingeschreven of voor het eerst voltooid.

**`GET /learningObjects/{id}`**

De inschrijvingsrelatie geeft alleen de primaire inschrijving weer, dus eerst ingeschreven of voor het eerst voltooid.

**`GET /learningObjects/{loId}/instances/{loInstanceId}`**

Er wordt een nieuwe relatie toegevoegd aan het LO-instantiemodel.

**`GET /enrollments/{id}`**

Inschrijving van cursussen met meerdere personen ophalen.

**`DELETE /enrollments/{id}`**

Uitschrijvingen van een bepaalde leerobjectinstantie.

**POST/inschrijvingen**

Ondersteunt inschrijving in verschillende instanties.

**GET/inschrijvingen**

Hiermee worden alleen inschrijvingen voor primaire inschrijvingen voor het leerobject opgehaald.

**`GET /learningObjects/{id}/note`**

Hiermee wordt een lijst met notities voor een cursus opgehaald.

**`GET /learningObjects/{lo_id}/instances/{loi_id}/note`**

Hiermee wordt een lijst met notities voor een cursus en de instantie opgehaald.

**`GET /learningObjects/{id}/resources/{loResourceId}/note`**

Hiermee wordt een lijst met notities voor een bron in een cursus opgehaald.

**`POST /learningObjects/{id}/resources/{loResourceId}/note`**

Voegt een opmerking toe in een module voor een cursus voor een bepaalde cursus.

**`DELETE /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Verwijdert specifieke notities uit een bepaalde module tegen een specifieke instantie (onderdeel van loResource-id).

**`GET /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Hiermee wordt een specifieke opmerking in een module voor een bepaalde instantie (onderdeel van loResourceId) in een cursus opgehaald.

**`PATCH /learningObjects/{id}/resources/{loResourceId}/note/{noteId}`**

Werkt specifieke notities van een bepaalde module bij voor een specifieke instantie (onderdeel van loResource-id).

**Wijzigingen in Admin API**

* GET /gebruikers/{id}/enrollments
* POST /gebruikers/{id}/enrollments
* DELETE /gebruikers/{id}/enrollments/{enrollmentId}
* PATCH /gebruikers/{id}/enrollments/{enrollmentId}

### Afgedwongen velden voor eindpunten

Producten en rollen worden alleen geladen wanneer deze worden afgedwongen.

Voorbeeldaanvraag

* GET `https://learningmanagerstage1.adobe.com/primeapi/v2/learningObjects/course%3A7418798?enforcedFields[learningObject]=products`
* GET `https://learningmanagerstage1.adobe.com/primeapi/v2/users/11255638/userBadges?include=model&page[offset]=0&page[limit]=10&sort=dateAchieved&enforcedFields[learningObject]=products,roles`

### Zoeken in API-wijzigingen stamimplementatie (landinstelling Engels)

Stemming is het proces waarbij een woord tot de basisvorm wordt verkleind. Dit zorgt ervoor dat er varianten van een woordovereenkomst voorkomen tijdens een zoekopdracht. Zo kunnen lopen en lopen worden gekoppeld aan hetzelfde hoofdwoord: lopen. Als een woord eenmaal is tegengehouden, komt het voorkomen van een woord overeen met het andere woord in een zoekopdracht.

In deze release hebben we stamstamversies toegevoegd voor Engelse landinstellingen, die de volgende varianten omvatten: en_US, en_AU, en_GB.

Het kenmerk stemmed geeft aan of stammen vereist is in zoekresultaten. Dit is standaard ingesteld op Onwaar

### Verwijderen van V1-eindpunten

V1-API&#39;s werken niet meer in deze release. Zie de klasse [Handleiding voor ontwikkelaars](/help/migrated/integration-admin/feature-summary/developer-manual.md).

### Meldingen voor inschrijving of uitschrijving van een cursus

Deze release introduceert ondersteuning voor cursusinstantie-id met meldingen in het nieuwe metagegevenskenmerk.

### Ondersteuning voor L1-feedback

Hiermee kan de student feedback geven op elk instantieniveau van de functie Meerdere inschrijvingen.

**API:** `POST /enrollments/{id}/l1Feedback`

### LO-lijst met afgedwongen velden

In deze release moet u secties, prequezeConstraints, conditionLOs, subLOs, additionalResources, additionalLOs, instances, catalogLabels expliciet naar het learningObject verzenden.

Bijvoorbeeld:

`enforcedFields[learningObject]=prerequisiteLOs,instances`

### Kennisgeving van veroudering voor de volgende release

* Markering voor student-API&#39;s overschrijven.
* We wijzigen de standaardinstelling voor highlightResults=false. Bovendien wijzigen we de standaardinstelling van snippetType=courseName.
* We vervangen matchType=bool in het zoekeindpunt.
* autoCompleteMode heeft de [Vervangen] tag en om dezelfde functionaliteit van autoCompleteMode =false te bieden, hebben we een matchType toegevoegd, genaamd Match.

### Badge-id-indeling met meerdere inschrijvingen

Ter ondersteuning van meervoudige inschrijvingsbadges wijzigen we de indeling van cursusbadges van `userId_badgeId_COURSE_courseId to userId_badgeId_COURSE_courseId_courseInstanceId` om badges op unieke wijze te identificeren.

## Opmerkingen bij de release

Voor informatie over de huidige en vorige releases van de webapp en de apparaatapp van Learning Manager raadpleegt u de [Opmerkingen bij de release](/help/migrated/release-note/release-notes.md).

## Bekende problemen of beperkingen in deze release

Hieronder volgen de beperkingen van deze versie:

### Offlineinhoud weergeven in de mobiele app

De volgende toepassingen worden niet ondersteund tijdens het weergeven van offline inhoud in de app:

* Flex-cursussen, leerplannen of certificeringen.
* Verbeterde cursussen, leerplannen of certificeringen.
* Meerdere quiz ingeschakeld: cursussen, leerplannen of certificeringen.
* Harvard Manage Mentor, Content Marketplace, GetAbstract of LinkedIn Cursussen, Leerplannen of Certificeringen.
* Leerplannen en certificaten met de vereiste waarden ingeschakeld.
* Gearchiveerde cursussen, leerplannen of certificeringen.
* Cursussen, leerplannen of certificeringen waarvan de deadline is verlopen.
* Externe certificaten.
* Voor e-commerce geschikte cursussen, leerplannen of certificeringen.

De volgende leerpaden, cursussen of certificeringen hebben een aantal problemen met offline synchronisatie:

* Alle leerpaden.
* Alle interne certificaten.
* Inhoud met aanroepen van POSTEN.

### Recommendations

Het volgende wordt niet ondersteund voor Product/Rol/Niveau in het nieuwe aanbevelingssysteem:

* Adobe Experience Manager, Teams, SFDC en Non-logged in.
* De mobiele app biedt geen ondersteuning voor het bewerken van producten en rollen op de pagina Aanbevelingen.
* De toewijzing is niet mogelijk tijdens de migratie.
* LinkedIn, Content Marketplace en andere externe cursussen, leerplannen of certificeringen automatisch taggen.
* Terugkeren naar op vaardigheid gebaseerd of Klassiek nadat je live bent gegaan.
* Het zoekmenu voor Producten en rollen in de Learner-app.
* Bulktoewijzing van cursussen, leerplannen of certificeringen en gebruikers in de Admin-app.

## Systeemvereisten

[Systeemvereisten voor Learning Manager](/help/migrated/system-requirements.md)
