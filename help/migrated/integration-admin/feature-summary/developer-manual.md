---
jcr-language: en_us
title: Handleiding voor toepassingsontwikkelaars
description: Learning Manager V1 API is nu verouderd. De V1 API's werken niet meer vanaf 28 februari 2021. We raden u aan om V2 API's te gebruiken voor interactie met Learning Manager.
contentowner: jayakarr
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '3279'
ht-degree: 0%

---



# Handleiding voor toepassingsontwikkelaars

Learning Manager V1 API is nu verouderd. De V1 API&#39;s werken niet meer vanaf 28 februari 2021. We raden u aan om V2 API&#39;s te gebruiken voor interactie met Learning Manager.

## Overzicht {#overview}

[Adobe Learning Manager](http://www.adobe.com/in/products/learningmanager.html) is een cloudgehoste, studentgerichte en zelfservice Learning Management Solution. Klanten hebben via de API van de Learning Manager toegang tot leermanschappen om deze te integreren met andere bedrijfstoepassingen. De API kan ook door Adobe partners worden gebruikt om de waardepropositie van Learning Manager te verbeteren door de functionaliteit ervan uit te breiden of door deze te integreren met andere toepassingen of services.

### Gebruiksscenario {#usagescenario}

Met de Learning Manager-API kunnen ontwikkelaars zelfstandige toepassingen bouwen die de functionaliteit van Learning Manager uitbreiden of de Learning Manager integreren met de workflows van andere bedrijfstoepassingen. U kunt een webtoepassing, desktopclient of mobiele app ontwikkelen met elke technologie van uw keuze. Als ontwikkelaar hebt u vanuit Learning Manager toegang tot uw toepassingsgegevens. De implementatie van de toepassing die u ontwikkelt, vindt plaats buiten het Learning Manager-platform en u hebt volledige controle over de levenscyclus van de softwareontwikkeling naarmate de toepassing zich ontwikkelt. Toepassingen worden meestal ontwikkeld door een klantorganisatie voor gebruik met hun Learning Manager-account en deze toepassingen zijn persoonlijk voor die specifieke klantorganisatie. Ook kunnen Adobe-partners generieke toepassingen maken met de Learning Manager API, die door een grote groep klanten van Learning Manager kunnen worden gebruikt.

## Learning Manager-API {#apidescription}

De API voor Learning Manager is gebaseerd op de principes van REST en maakt belangrijke elementen van het Learning Manager Object Model beschikbaar voor ontwikkelaars van toepassingen via HTTP. Voordat ontwikkelaars de details van de API-eindpunten en de HTTP-methoden kennen, kunnen ze vertrouwd raken met de verschillende objecten van de Learning Manager, hun kenmerken en onderlinge relaties. Als de modellen eenmaal zijn begrepen, is het handig om basiskennis op te doen van de structuur van API-verzoeken en -reacties en van enkele algemene programmeertermen die we algemeen gebruiken in de API.

Raadpleeg voor meer informatie over de verschillende API-eindpunten en -methoden de  [API-documentatie van Learning Manager](https://learningmanager.adobe.com/docs/primeapi/v2/).

## API-verificatie {#apiauthentication}

Wanneer u een toepassing schrijft die API-aanroepen naar Leermanager maakt, moet u uw toepassing registreren met behulp van de integratiebeheerder-app.

Leermanager-API&#39;s gebruiken het OAuth 2.0-framework om uw clienttoepassingen te verifiëren en autoriseren.

**Procedure**

**1. Uw toepassing instellen**

U kunt uw toepassing instellen met de client-ID en het clientgeheim om de juiste eindpunten te gebruiken. Zodra u uw toepassing registreert, kunt u clientId en clientSecret krijgen. U kunt de URL ophalen beter gebruiken in een browser omdat deze de gebruikers van de Leermanager verifieert met behulp van hun vooraf geconfigureerde accounts zoals SSO, Adobe ID, enzovoort.

```
GET https://learningmanager.adobe.com/oauth/o/authorize?client_id=<Enter your clientId>&redirect_uri=<Enter a url to redirect to>&state=<Any String data>&scope=<one or more comma separated scopes>&response_type=CODE.
```

Na succesvolle verificatie wordt uw browser omgeleid naar de redirect_uri die in de bovenstaande URL wordt vermeld. Een parameter **code** wordt toegevoegd samen met de omleidingslink.

**2. Vernieuwingstoken ophalen uit code**

`POST https://learningmanager.adobe.com/oauth/token Content-Type: application/x-www-form-urlencoded`

Hoofdtekst van de postaanvraag:

```
client_id: 
<enter your clientid>
 & 
 client_secret: 
 <enter your clientsecret>
  & 
  code: 
  <code from step 1></code>
 </enter>
</enter>
```

**3.** **Verkrijg een toegangstoken van vernieuwingstoken**

URL om toegangstoken te verkrijgen:

POST [https://learningmanager.adobe.com/oauth/token/refresh](https://learningmanager.adobe.com/oauth/token/refresh) Inhoudstype: application/x-www-form-urlencoded

Hoofdtekst van de postaanvraag:

```
client_id: 
<enter your clientid>
 & 
 client_secret: 
 <enter your clientsecret>
  & 
  refresh_token: 
  <refresh token>
   
  </refresh>
 </enter>
</enter>
```

**URL om de toegangstokendetails te verifiëren**

`GET https://learningmanager.adobe.com/oauth/token/check?access_token=<access_token>`

**Gebruiksbeperking**

Een toegangstoken is zeven dagen geldig. Na een dag moet u een nieuw toegangstoken genereren met een vernieuwingstoken. Als u een nieuw toegangstoken genereert van een vernieuwingstoken terwijl een bestaand toegangstoken nog geldig is, wordt het bestaande token geretourneerd.

Hieronder worden enkele veelgebruikte termen in de Leermanager-API ter referentie uitgelegd.

**Omvat**

Ontwikkelaars hebben toegang tot één API-objectmodel en ook tot meerdere modellen die aan dat model zijn gekoppeld. Om toegang te krijgen tot de volgende gerelateerde modellen, moet u de relatie van elk model met andere modellen begrijpen. **Omvat** parameter laat ontwikkelaars toe om tot de afhankelijke modellen toegang te hebben. U kunt een kommascheidingsteken gebruiken om toegang te krijgen tot meerdere modellen. Voor voorbeeldgebruik en meer informatie over **include**, raadpleeg de voorbeeldsectie voor het API-model op deze pagina.

**API-verzoek**

De API-verzoeken kunnen worden gedaan door een HTTP-aanvraag in te dienen. Afhankelijk van het eindpunt en de methode kan de ontwikkelaar kiezen uit verschillende HTTP-werkwoorden zoals GET, PUT, POST, DELETE, PATCH, enz. Voor sommige verzoeken kunnen queryparameters worden doorgegeven. Bij het aanvragen van een specifiek gegevensmodel kan de gebruiker ook om verwante modellen vragen, zoals beschreven in de JSON API-specificaties. De structuur van een standaard API-verzoek wordt beschreven in [voorbeeldmodelgebruik](#main-pars_header_1415780624).

**API-reactie**

Wanneer een API-verzoek wordt gedaan door een client, wordt een SON-document verkregen volgens de JSON API-specificatie. De reactie bevat ook de HTTP-statuscode, die de ontwikkelaar kan verifiëren om de juiste volgende stappen in zijn toepassingslogica uit te voeren. De structuur van een typische API-respons wordt beschreven in  [voorbeeldmodelgebruik](#main-pars_header_1415780624).

**Fouten**

Wanneer een API-verzoek mislukt, wordt een foutreactie verkregen. De HTTP-statuscode die in de reactie wordt geretourneerd, geeft de aard van de fout aan. Foutcodes worden weergegeven met nummers voor elk model in de API-referentie. 200, 204, 400 en 404 zijn enkele veelvoorkomende fouten in API&#39;s die wijzen op problemen met HTTP-toegang.

**Velden**

De kenmerken en relaties van API-objecten worden gezamenlijk velden genoemd. Raadpleeg [JSON API voor meer informatie.](http://jsonapi.org/format/#document-resource-object-fields) U kunt Velden als parameter gebruiken tijdens het maken van API-aanroepen om een of meer specifieke kenmerken van het model op te halen. Bij gebrek aan de parameter Fields worden met de API-aanroep alle beschikbare kenmerken van het model opgehaald. In de volgende API-aanroep worden bijvoorbeeld velden[vaardigheid]=name haalt u het naamkenmerk van het vaardigheidsmodel alleen op.

https://learningmanager.adobe.com/primeapi/v2/users/{userId}/userSkills/{id}?include=skillLevel.skill&amp;fields[skill]=name

**Paginering**

Soms leidt een API-aanvraag tot een lange lijst met objecten die in de reactie moeten worden geretourneerd. In dergelijke gevallen stelt het pagineringskenmerk de ontwikkelaar in staat om de resultaten opeenvolgend op te halen in termen van meerdere pagina&#39;s, waarbij elke pagina een reeks records bevat. Met het pagineringskenmerk in Leerbeheer kunt u bijvoorbeeld het maximum aantal records instellen dat op een pagina moet worden weergegeven. U kunt ook de bereikwaarde definiëren van de records die op de pagina moeten worden weergegeven.

**Sorteren**

Sorteren is toegestaan in API-modellen. Kies op basis van het model het type sortering dat op de resultaten moet worden toegepast. Sorteren kan oplopend of aflopend worden toegepast. Als u bijvoorbeeld `code sort=name`, dan wordt er oplopend gesorteerd op naam. Als u `code sort=-name`, wordt er aflopend gesorteerd op naam. Raadpleeg [JSON API-specificaties voor meer informatie](http://jsonapi.org/format/#fetching-sorting).

## API-gebruiksillustratie {#samplemodel}

Laten we een scenario overwegen waarbij een ontwikkelaar vaardigheidsnaam, maximale punten voor vaardigheidsniveau en punten die de student voor die vaardigheid heeft verdiend, wil ophalen.

Een userSkill-model in API&#39;s van Learning Manager bestaat uit id, type, dateAchieved, dateCreated, pointsEarned als standaardkenmerken. Dus wanneer een ontwikkelaar de methode GET gebruikt om details van userSkill-model te verkrijgen, worden de huidige gegevens met betrekking tot de standaardkenmerken weergegeven in de uitvoer van de respons.

Maar in dit scenario wil de ontwikkelaar de vaardigheidsnaam en het vaardigheidsniveau voor de gebruiker ophalen. Via de API voor leerbeheer hebt u toegang tot deze gerelateerde informatie met behulp van relatievelden en parameters. De bijbehorende modellen voor userSkill worden verkregen in relatietags. U kunt de details van elke bijbehorende modellen verkrijgen door deze modellen samen met de userSkill aan te roepen. Voor deze informatie gebruikt u **`code include`** parameter met door punt (punt) gescheiden waarden voor elk van de bijbehorende modellen. U kunt een komma als scheidingsteken gebruiken om een ander model aan te vragen, zoals user include=skillLevel.skill,course

**API-aanroep**

`https://learningmanagerqe1.adobe.com/primeapi/v1/users/%7buserId%7d/userSkills/%7bid%7d?include=skillLevel.skill&fields%5bskill%5d=name&fields%5bskillLevel%5d=maxCredits&fields%5buserSkill%5d=pointsEarned`

UserId kan bijvoorbeeld 746783 zijn en de userSkills id: 746783_4426_1.

**Reactie van API-aanroep**

```
\{ 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/users/746783/userSkills/746783_4426_1?include=skillLevel.skill&fields[userSkill]=pointsEarned&fields[skillLevel]=maxCredits&fields[skill]=name"}, 
 "data": { 
 "id": "746783_4426_1", 
 "type": "userSkill", 
 "attributes": {"pointsEarned": 5}, 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/users/746783/userSkills/746783_4426_1"} 
 }, 
 "included": [ 
 { 
 "id": "4426", 
 "type": "skill", 
 "attributes": {"name": "Java"}, 
 "links": {"self": "https://learningmanager.adobe.com/primeapi/v2/skills/4426"} 
 }, 
 { 
 "id": "4426_1", 
 "type": "skillLevel", 
 "attributes": {"maxCredits": 10} 
 } 
 ] 
} 
```

## Leermansmodellen {#models}

Met de Leermanager-API hebben ontwikkelaars toegang tot leermantobjecten als RESTful-bronnen. Elk API-eindpunt vertegenwoordigt een bron, doorgaans een objectinstantie zoals Badge, of een verzameling van dergelijke objecten. De ontwikkelaars gebruiken dan de werkwoorden van HTTP zoals PUT, GET, POST en DELETE om de verrichtingen CRUD op die voorwerpen (inzamelingen) uit te voeren.

+++V1 API

In het volgende diagram worden de verschillende elementen van het Leermanager-objectmodel in V1 API weergegeven.

![](assets/er-diag-primemodels.png)

In de volgende tabel worden verschillende elementen van het objectmodel van Leermanager V1 beschreven:

<table border="1" cellspacing="0" cellpadding="0">
 <tbody>
  <tr>
   <td>
    <p><strong>Serienummer</strong></p></td>
   <td>
    <p><strong>Object van Learning Manager</strong></p></td>
   <td>
    <p><strong>Beschrijving</strong></p></td>
  </tr>
  <tr>
   <td>
    <p>1.      </p></td>
   <td>
    <p>gebruiker</p></td>
   <td>
    <p>Gebruiker is het belangrijkste model in Leermanager. Gebruikers zijn doorgaans de interne of externe studenten van een organisatie die leerobjecten gebruiken. Ze kunnen echter ook een andere rol spelen, zoals auteur en manager, samen met de rol van de student. Gebruikers-ID, type, e-mail zijn enkele inline kenmerken. </p></td>
  </tr>
  <tr>
   <td>
    <p>2.      </p></td>
   <td>
    <p>cursus</p></td>
   <td>
    <p>Cursus is een van de leerobjecten die worden ondersteund in Leerbeheer en bestaat uit een of meer modules. </p></td>
  </tr>
  <tr>
   <td>
    <p>3.      </p></td>
   <td>
    <p>module</p></td>
   <td>
    <p>Module is een bouwsteen voor het maken van leerobjecten in Learning Manager. De modules kunnen uit vier verschillende typen bestaan, zoals klaslokaal, virtuele klasruimte, activiteit en op eigen tempo. Gebruik dit modulemodel om de details van alle modules in een account op te halen. </p></td>
  </tr>
  <tr>
   <td>
    <p>4.      </p></td>
   <td>
    <p>certificatie</p></td>
   <td>
    <p>De certificering wordt toegekend aan studenten op basis van het succesvol afronden van cursussen. Voordat u certificeringen gebruikt, moet u eerst cursussen volgen in de toepassing. </p></td>
  </tr>
  <tr>
   <td>
    <p>5.      </p></td>
   <td>
    <p>leerprogramma</p></td>
   <td>
    <p>Leerprogramma's zijn uniek ontworpen cursussen die voldoen aan specifieke leerbehoeften van gebruikers. Meestal worden leerprogramma's gebruikt om leerdoelen te stimuleren die zich uitstrekken over afzonderlijke cursussen. </p></td>
  </tr>
  <tr>
   <td>
    <p>6.      </p></td>
   <td>
    <p>badge</p></td>
   <td>
    <p>Een badge is een vorm van prestatiebeloning die studenten krijgen wanneer ze specifieke mijlpalen bereiken terwijl ze binnen een cursus verdergaan. </p></td>
  </tr>
  <tr>
   <td>
    <p>7.      </p></td>
   <td>
    <p>vaardigheid</p></td>
   <td>
    <p>Het vaardighedenmodel bestaat uit niveaus en punten. Studenten kunnen vaardigheden verwerven na voltooiing van de cursus. </p></td>
  </tr>
  <tr>
   <td>
    <p>8.      </p></td>
   <td>
    <p>certificationEnrollment</p></td>
   <td>
    <p>Dit model biedt details over een inschrijving door een gebruiker voor één certificering.</p></td>
  </tr>
  <tr>
   <td>
    <p>9.  </p></td>
   <td>
    <p>courseEnrollment</p></td>
   <td>
    <p>Dit model bevat details over een inschrijving van een gebruiker voor één cursus. </p></td>
  </tr>
  <tr>
   <td>
    <p>10.  </p></td>
   <td>
    <p>courseInstance</p></td>
   <td>
    <p>Aan een cursus kunnen een of meer instanties zijn gekoppeld. U kunt een cursusinstantie krijgen </p></td>
  </tr>
  <tr>
   <td>
    <p>11.  </p></td>
   <td>
    <p>courseSkill</p></td>
   <td>
    <p>Een courseSkill-model specificeert de voortgang van één vaardigheid die wordt bereikt door het voltooien van een cursus.</p></td>
  </tr>
  <tr>
   <td>
    <p>12.  </p></td>
   <td>
    <p>courseModule</p></td>
   <td>Een courseModule-model specificeert hoe een module in een cursus wordt opgenomen. Bijvoorbeeld, of de module wordt gebruikt voor pretest of voor inhoud.</td>
  </tr>
  <tr>
   <td>
    <p>13.  </p></td>
   <td>learningProgramInstance</td>
   <td>
    <p>Een leerprogramma kan bestaan uit meerdere instanties die soortgelijke eigenschappen van een leerprogramma of aangepaste instanties bevatten. </p></td>
  </tr>
  <tr>
   <td>
    <p>14.  </p></td>
   <td>
    <p>taakhulp</p></td>
   <td>
    <p>Taakhulp is een leerinhoud die zonder enige inschrijvings- of voltooiingscriteria toegankelijk is voor studenten. U kunt informatie ophalen, bijwerken, datum, status, id, samen met de bijbehorende modellen, zoals de versie van de taakhulp, auteurs en vaardigheidsniveau. </p></td>
  </tr>
  <tr>
   <td>
    <p>15.  </p></td>
   <td>
    <p>jobAidVersion</p></td>
   <td>
    <p>Aan taakhulp kunnen een of meer versies zijn gekoppeld op basis van numerieke herzieningen in de inhoud en het aantal uploads. Dit model bevat details over één taakhulpenversie. </p></td>
  </tr>
  <tr>
   <td>
    <p>16.  </p></td>
   <td>
    <p>learningProgramInstanceEnrollment</p></td>
   <td>
    <p>Het leerprogramma bestaat uit een of meer instanties. Studenten kunnen zich alleen inschrijven voor een leerprogramma-instantie of worden toegewezen door de beheerder. Dit model geeft details over een inschrijving door een gebruiker voor één leerprogramma-instantie. </p></td>
  </tr>
  <tr>
   <td>
    <p>17.  </p></td>
   <td>
    <p>moduleVersion</p></td>
   <td>
    <p>Een module kan een of meer versies hebben op basis van het uploaden van gereviseerde inhoud. Gebruik dit model om specifieke informatie over om het even welke enige moduleversie te verkrijgen. </p></td>
  </tr>
  <tr>
   <td>
    <p>18.  </p></td>
   <td>
    <p>skillLevel</p></td>
   <td>
    <p>Een vaardigheidsniveau bestaat uit een of meer cursussen die moeten worden gevolgd om een niveau te bereiken met de bijbehorende punten. </p></td>
  </tr>
  <tr>
   <td>
    <p>19.  </p></td>
   <td>
    <p>userBadge</p></td>
   <td>
    <p>UserBadge koppelt één badge aan één gebruiker. Het bevat details zoals wanneer het werd bereikt, assertionUrl etc. </p></td>
  </tr>
  <tr>
   <td>
    <p>20.  </p></td>
   <td>
    <p>userSkill</p></td>
   <td>
    <p>UserSkill geeft aan hoeveel van één vaardigheidsniveau door één gebruiker wordt bereikt.</p></td>
  </tr>
 </tbody>
</table>

+++

+++V2 API

Hieronder vindt u de verschillende elementen van het klassediagram Leermanager in V2 API.

![](assets/v2api-class-diagram.jpg)

<table>
 <tbody>
  <tr>
   <th><b>Object van Learning Manager</b></th>
   <th><b>Beschrijving</b></th>
  </tr>
  <tr>
   <td>account</td>
   <td>Omvat de gegevens van een leermanklant.</td>
  </tr>
  <tr>
   <td><code>
     badge
    </code></td>
   <td>Een badge is een vorm van prestatiebeloning die studenten krijgen wanneer ze specifieke mijlpalen bereiken terwijl ze binnen een cursus verdergaan. <br></td>
  </tr>
  <tr>
   <td><code>
     catalog
    </code></td>
   <td>Catalogus is een verzameling leerobjecten.</td>
  </tr>
  <tr>
   <td><code>
     user
    </code></td>
   <td>Gebruiker is het belangrijkste model in Leermanager. Gebruikers zijn doorgaans de interne of externe studenten van een organisatie die leerobjecten gebruiken. Ze kunnen echter ook een andere rol spelen, zoals auteur en manager, samen met de rol van de student. Gebruikers-ID, type, e-mail zijn enkele inline kenmerken. </td>
  </tr>
  <tr>
   <td>resource</td>
   <td>Dit wordt gebruikt om elke inhoudsbron te modelleren die een module probeert in te kapselen. Alle bronnen ingekapseld in <code>
     an
    </code> <code>
     loResource
    </code> zijn gelijkwaardig in termen van het leerdoel, maar verschillen van elkaar in termen van leveringstype of landinstelling van inhoud.<br></td>
  </tr>
  <tr>
   <td>userNotification</td>
   <td>Dit model bevat meldingsgegevens voor een student.<br></td>
  </tr>
  <tr>
   <td>userSkill</td>
   <td>UserSkill geeft aan hoeveel van één vaardigheidsniveau door één gebruiker wordt bereikt.<br></td>
  </tr>
  <tr>
   <td>userBadge</td>
   <td>UserBadge koppelt een enkele badge <code>
     with
    </code> één gebruiker. Het bevat details zoals wanneer het werd bereikt, <code>
     assertionUrl
    </code> enzovoort. <br></td>
  </tr>
  <tr>
   <td>vaardigheid</td>
   <td>Het vaardighedenmodel bestaat uit niveaus en punten. Studenten kunnen vaardigheden verwerven na voltooiing van de cursus. <br></td>
  </tr>
  <tr>
   <td>skillLevel</td>
   <td>Een vaardigheidsniveau bestaat uit een of meer cursussen die moeten worden gevolgd om een niveau te bereiken met de bijbehorende punten. <br></td>
  </tr>
  <tr>
   <td>learningObject</td>
   <td>Een leerobject is een abstractie voor verschillende soorten objecten waarvoor gebruikers zich kunnen inschrijven en waaruit ze kunnen leren. Op dit moment heeft Leermanager de vier typen leerobjecten: Cursus, Certificering, Leerprogramma <code>
     and
    </code> Taakhulp.<br></td>
  </tr>
  <tr>
   <td>learningObjectInstance<br></td>
   <td>Een specifieke instantie van een leerobject.<br></td>
  </tr>
  <tr>
   <td>learningObjectResource</td>
   <td>Dit komt overeen met het concept <code>
     module
    </code>. Een cursus bestaat uit één <code>
     of
    </code> meer modules. In Learning Manager kan een module op verschillende vergelijkbare manieren worden geleverd. Daarom <code>
     loResource
    </code> omvat in wezen al die gelijkwaardige middelen.<br></td>
  </tr>
  <tr>
   <td>loResourceGrade<br></td>
   <td>Dit omvat het resultaat van de gebruiker die een specifieke bron gebruikt in de context van een leerobject waarvoor hij is ingeschreven. Het bevat informatie zoals de duur die door <code>
     user
    </code> in de resource, de procentuele voortgang die de gebruiker heeft geboekt, de status geslaagd/gezakt en de score die de gebruiker heeft behaald in een bijbehorende quiz.<br></td>
  </tr>
  <tr>
   <td>kalender<br></td>
   <td>Een kalenderobject is een lijst met <code>
     upcoming classroom
    </code> of virtuele klassikale cursussen waarvoor de gebruiker zich kan inschrijven.<br></td>
  </tr>
  <tr>
   <td>l1FeedbackInfo<br></td>
   <td>L1-feedback omvat de antwoorden van een student op de feedbackvragen die zijn gekoppeld aan leerobjecten. Meestal wordt dit verzameld nadat de gebruiker een leerobject heeft voltooid indien dit is geconfigureerd om dergelijke feedback van studenten te verzamelen.<br></td>
  </tr>
  <tr>
   <td>inschrijving<br></td>
   <td>Deze abstractie omvat de details met betrekking tot de transactie die de toewijzing van een specifieke gebruiker aan een specifieke leerobjectinstantie vertegenwoordigt.<br></td>
  </tr>
 </tbody>
</table>

+++

Lijst met objectkenmerken en -relaties.

+++account

**Kenmerken**
dateCreated\
gamificationEnabled\
id\
landinstelling\
loginUrl\
logoUrl\
name\
subdomein\
themeData\
timeZoneCode

**Relaties**
contentLocales(localizationMetadata)\
gamificationLevels(gamificationLevel)\
timeZones(timeZone)\
uiLocales(localizationMetadata)

+++

+++badge

**Kenmerken**
id\
imageUrl\
name\
status

+++

+++catalogus

**Kenmerken**
dateCreated\
dateUpdated\
beschrijving\
id\
isDefault\
isInternalSearchable\
isListable\
name\
status

+++

+++data

**Kenmerken**
id\
names

+++

+++gamification

**Kenmerken**
kleur\
name\
punten

+++

+++learningObject

**Kenmerken**
authorNames\
dateCreated\
datePublished\
dateUpdated\
effectiviteitIndex\
enrollmentType\
id\
imageUrl\
isExternal\
isSubLoOrderEnForce\
loType\
status\
tags

**Relaties**
auteurs (gebruiker)\
enrollment(learningObjectInstanceEnrollment)\
instances(learningObjectInstance)\
conditionLOs (learningObject)\
skills(learningObjectSkill)\
subLOs(learningObject)\
aanvullende LO&#39;s (learningObject)\
additionalResources(resource)

+++

+++learningObjectInstance

**Kenmerken**
completionDeadline\
dateCreated\
enrollmentCount\
id\
isDefault\
seatLimit\
status\
geldigheid

**Relaties**
badge(badge)\
l1FeedbackInfo(feedbackInfo)\
learningObject(learningObject)\
loResources(learningObjectResource)\
localizedMetadata(localizationMetadata)\
subLoInstance(learningObjectInstance)

+++

+++learningObjectInstanceEnrollment

**Kenmerken**
dateCompleted\
dateEnrolled\
dateStarted\
hasPassed\
id\
progressPercent\
score\
status

**Relaties**
student (gebruiker)\
learnerBadge(userBadge)\
learningObject(learningObject)\
loInstance(learningObjectInstance)\
loResourceGrades(learningObjectResourceGrade)

+++

+++learningObjectResource

**Kenmerken**
externalReporting\
id\
loResourceType\
resourceType\
versie

**Relaties**
learningObject(learningObject)\
loInstance(learningObjectInstance)\
localizedMetadata(localizationMetadata)\
resources (resource)

+++

+++learningObjectResourceGrade

**Kenmerken**
dateCompleted\
dateStarted\
dateSuccess\
duur\
hasPassed\
id\
progressPercent\
score

**Relaties**
loResource(learningObjectResource)

+++

+++learningObjectSkill

**Kenmerken**
credits\
id\
**Relaties**
learningObject(learningObject)\
skillLevel(skillLevel)

+++

+++aanbeveling

**Kenmerken**
id\
reden

**Relaties**
learningObject(learningObject)

+++

+++resource

**Kenmerken**
authorDesiredDuration\
completionDeadline\
contentStructureInfoUrl\
contentType\
contentZipSize\
contentZipUrl\
dateCreated\
dateStart\
gewensteDuration\
downloadUrl\
extraData\
hasQuiz\
hasToc\
id\
instructorNames\
isDefault\
landinstelling\
locatie\
name\
onlyQuiz\
reportingInfo\
reportingType\
seatLimit

+++

+++skill

**Kenmerken**
beschrijving\
id\
name\
status

**Relaties**
niveaus (skillLevel)

+++

+++skillLevel

**Kenmerken**
id\
niveau\
maxCredits\
name\
**Relaties**
badge(badge)\
skill(skill)

+++

+++gebruiker

**Kenmerken**
avatarUrl\
bio\
contentLocale\
email\
velden\
id\
name\
pointsEarned\
profiel\
rollen\
status\
timeZoneCode\
uiLocale

**Relaties**
account(account)\
manager(gebruiker)

+++

+++userBadge

**Kenmerken**
assertionUrl\
dateAchieved\
id\
modelType

**Relaties**
badge(badge)\
student (gebruiker)\
model (learningObject)

+++

+++userCalendar

**Kenmerken**
cursus\
courseType\
dateStart\
ingeschreven\
id\
maand\
kwart

**Relaties**
containerLO (learningObject)\
course (learningObject)

+++

+++userNotification

**Kenmerken**
actiontaken\
kanaal\
dateCreated\
id\
bericht\
modelIds\
modelNames\
modelTypes\
lezen\
rol

+++

+++userSkill

**Kenmerken**
dateAchieved\
dateCreated\
id\
pointsEarned

**Relaties**
learnerBadge(userBadge)\
learningObject(learningObject)\
skillLevel(skillLevel)\
user(user)

+++

## Ontwikkeling van toepassingen {#registration}

## Voorwaarden {#prerequisites}

Als ontwikkelaar moet u een proefaccount maken op Learning Manager, zodat u volledige toegang hebt tot alle rollen in dat account. Om een toepassing te kunnen schrijven, moet een ontwikkelaar een aantal gebruikers en cursussen maken en het account in een redelijke staat brengen, zodat de toepassing die wordt ontwikkeld, toegang kan krijgen tot enkele voorbeeldgegevens.

## Client-id en -geheim maken {#createclientidandsecret}

1. In **Integratiebeheerder** aanmelden, klikken **[!UICONTROL Toepassingen]** in het linkerdeelvenster.

   ![](assets/application-development-menu.png)

   *Toepassingen selecteren op integratiebeheerder*

1. Klikken **[!UICONTROL Registreren]** rechtsboven op de pagina om uw toepassingsgegevens te registreren. Registratiepagina verschijnt.

   ![](assets/register-application.png)

   *De toepassing registreren*

   U moet alle velden op deze pagina invullen.

   **Toepassingsnaam**: Voer de naam van uw toepassing in. Het is niet verplicht om dezelfde toepassingsnaam te gebruiken; het kan elke geldige naam zijn.

   **URL**: Als u de exacte URL weet waar de toepassing wordt gehost, kunt u deze vermelden. Als u het niet weet, kunt u de URL van uw bedrijf vermelden. Geldige URL-naam is verplicht in dit veld.

   **Domeinen omleiden**: Voer de domeinnaam in van de toepassing waarin u de Leermiddeltoepassing na OAuth-verificatie wilt omleiden. U kunt hier meerdere URL&#39;s vermelden, maar u moet wel geldige URL&#39;s gebruiken, zoals `http://google.com`, `http://yahoo.com` enzovoort.

   **Omschrijving:** Voer een korte beschrijving in voor uw toepassing.

   **Bereiken:** Kies een van de vier beschikbare opties om het bereik van uw toepassing te definiëren. Op basis van uw hier vermelde keuze is het API-eindpunt van Learning Manager toegankelijk voor uw toepassing. Als u bijvoorbeeld **Leestoegang studentrol** en zijn alle API-eindpunten voor studenten van de Learning Manager alleen-lezen voor uw toepassing toegankelijk.

   **Alleen voor dit account?**\
   **Ja** - als u Ja kiest, is de toepassing niet zichtbaar voor andere accountbeheerders.\
   **Nee** - als u Nee kiest, kunnen andere accountbeheerders deze toepassing ook openen, maar ze moeten de toepassings-id gebruiken om toegang te krijgen tot deze toepassing. Toepassings-id wordt gegenereerd en weergegeven in de bewerkingsmodus van de Learning Manager-toepassing.

   Als u **Beheerdersrol lees- en schrijftoegang** als bereik tijdens de registratie van de toepassing en kies **Leestoegang beheerdersrol** tijdens het ontwerpen van de API&#39;s kunt u nog steeds schrijftoegang voor de toepassing hebben, aangezien het registratiebereik van de app de autorisatieworkflow vervangt.

1. Klikken **[!UICONTROL Registreren]** in de rechterbovenhoek na het invullen van de details op de registratiepagina.

## Ontwikkeling en testen van toepassingen {#applicationdevelopmentandtesting}

De Leermanager-API kan door ontwikkelaars worden gebruikt om elke toepassing te bouwen. Ontwikkelaars moeten ervoor zorgen dat hun accounts bestaan uit enkele geldige gebruikers en cursussen. Ze kunnen een paar dummygebruikers en cursussen maken en activiteiten in het proefaccount simuleren, zodat ze de functionaliteit van de toepassing kunnen testen.

## Toepassingsimplementatie {#applicationdeployment}

We raden de beheerder van de leermanager of een integratiebeheerder voor het productieaccount aan om de toepassing beschikbaar te maken voor gebruikers binnen hun organisatie. Als de toepassing is getest en klaar is voor productie, stelt u de beheerder op de hoogte van het productieaccount. Idealiter genereren de beheerders een nieuwe client-id en een nieuw clientgeheim voor de toepassing in het productieaccount en voeren ze de noodzakelijke stappen uit om deze op een veilige manier in de toepassing op te nemen. De daadwerkelijke procedure voor het opstellen van toepassingen varieert van onderneming aan onderneming, en de Leermanagerbeheerder van uw organisatie moet steun van de afdeling IT/IS binnen uw organisatie nemen om de plaatsing te voltooien.

## Externe goedkeuring van de toepassing {#externalapplicationapproval}

U kunt externe toepassingen toevoegen door op **Goedkeuren** in de rechterbovenhoek van het deelvenster **Toepassingen** pagina. Geef de externe toepassings-id op en klik op **Opslaan.**

![](assets/add-external-application.png)

*Een externe toepassing toevoegen en goedkeuren*

## Veelgestelde vragen

+++Heeft Learning Manager een e-commerce-integratie?

Adobe Learning Manager heeft geen e-commerce-integratie. Wij bieden echter API&#39;s waarmee u uw eigen headless LMS kunt maken en functies voor e-commerce kunt implementeren.
+++
