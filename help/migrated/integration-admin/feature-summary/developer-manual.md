---
jcr-language: en_us
title: Handleiding voor toepassingsontwikkelaars
description: Versie 1 van de Learning Manager-API is nu verouderd. De API's van versie 1 werken niet meer vanaf 28 februari 2021. We raden u aan om V2 API's te gebruiken voor interactie met Learning Manager.
contentowner: jayakarr
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '3279'
ht-degree: 65%

---



# Handleiding voor toepassingsontwikkelaars

Versie 1 van de Learning Manager-API is nu verouderd. De API&#39;s van versie 1 werken niet meer vanaf 28 februari 2021. We raden u aan om V2 API&#39;s te gebruiken voor interactie met Learning Manager.

## Overzicht {#overview}

[Adobe Learning Manager](http://www.adobe.com/in/products/learningmanager.html) is een studentgerichte, selfservice Learning Management Solution die in de cloud wordt gehost. Klanten kunnen toegang krijgen tot Learning Manager-leermiddelen met behulp van de Learning Manager-API om deze te integreren met andere bedrijfstoepassingen. De API kan ook door Adobe-partners worden gebruikt om de waardepropositie van Learning Manager te verbeteren door de functionaliteit ervan uit te breiden of door middel van integratie met andere toepassingen of diensten.

### Gebruiksscenario {#usagescenario}

Met behulp van Learning Manager-API kunnen ontwikkelaars autonome toepassingen bouwen die de functionaliteit van Learning Manager uitbreiden of Learning Manager integreren met andere bedrijfsapplicatieworkflows. U kunt met technologie naar keuze een webtoepassing, desktopclient of mobiele app ontwikkelen. Als ontwikkelaar hebt u vanuit Learning Manager toegang tot uw toepassingsgegevens. De implementatie van de toepassing die u ontwikkelt, vindt plaats buiten het Learning Manager-platform en u hebt volledige controle over de levenscyclus van de softwareontwikkeling naarmate de toepassing zich ontwikkelt. Toepassingen worden meestal ontwikkeld door een klantorganisatie voor gebruik met hun Learning Manager-account, en deze toepassingen zijn &#39;privé&#39; voor die specifieke klantorganisatie. Adobe-partners kunnen daarnaast met de Learning Manager-API generieke toepassingen bouwen die gebruikt kunnen worden door een grote groep Learning Manager-klanten.

## Learning Manager-API {#apidescription}

De Learning Manager-API is gebaseerd op de principes van REST en maakt belangrijke elementen van het Learning Manager-objectmodel beschikbaar voor ontwikkelaars van toepassingen via HTTP. Voordat ze volledig op de hoogte zijn van de API-eindpunten en HTTP-methoden kunnen ontwikkelaars eerst vertrouwd raken met de verschillende Learning Manager-objecten, hun attributen en onderlinge relaties. Nadat een inzicht in de modellen is verworven, is het handig om enige basiskennis van de structuur van API-verzoeken en -reacties op te doen, evenals van enkele gemeenschappelijke programmeertermen die we algemeen ondersteunen in de API.

Raadpleeg voor meer informatie over de verschillende API-eindpunten en -methoden de  [API-documentatie van Learning Manager](https://learningmanager.adobe.com/docs/primeapi/v2/).

## API-verificatie {#apiauthentication}

Wanneer u een toepassing schrijft die API-oproepen naar Learning Manager verstuurd, moet u uw toepassing registreren met behulp van de integreatiebeheerder-app.

Learning Manager xAPI gebruikt OAuth 2.0 framework om uw cliëntapplicaties te verifiëren en autoriseren.

**Procedure**

**1. Uw toepassing instellen**

U kunt uw toepassing instellen met de client-ID en het clientgeheim om de juiste eindpunten te gebruiken. Zodra u uw toepassing registreert, kunt u clientId en clientSecret krijgen. U gebruikt GET URL in uw browser omdat deze de Learning Manager-gebruikers authenticeert met behulp van hun vooraf geconfigureerde accounts zoals SSO, Adobe ID enzovoort.

```
GET https://learningmanager.adobe.com/oauth/o/authorize?client_id=<Enter your clientId>&redirect_uri=<Enter a url to redirect to>&state=<Any String data>&scope=<one or more comma separated scopes>&response_type=CODE.
```

Na succesvolle authenticatie wordt uw browser omgeleid naar de redirect_url die in de bovenstaande URL staat vermeld. Er wordt samen met de omleidingslink een **parametercode** toegevoegd.

**2. Ontvang vernieuwingstoken via code**

`POST https://learningmanager.adobe.com/oauth/token Content-Type: application/x-www-form-urlencoded`

De hoofdtekst van de berichtaanvraag:

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

POST [https://learningmanager.adobe.com/oauth/token/refresh](https://learningmanager.adobe.com/oauth/token/refresh) Content-Type: application/x-www-form-urlencoded

De hoofdtekst van de berichtaanvraag:

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

**URL om de details van de toegangstoken te controleren**

`GET https://learningmanager.adobe.com/oauth/token/check?access_token=<access_token>`

**Gebruiksbeperking**

Een toegangstoken is zeven dagen geldig. Na een dag moet u met behulp van een vernieuwingstoken een nieuw toegangstoken genereren. Als u met een vernieuwingstoken een nieuw toegangstoken genereert terwijl een bestaand toegangstoken nog geldig is, wordt het bestaande token geretourneerd.

Enkele van de meestgebruikte termen in Learning Manager-API worden hieronder uitgelegd, ter referentie.

**Inclusief**

Ontwikkelaars hebben toegang tot één API-objectmodel en ook tot meerdere modellen die bij dat model horen. Om toegang te krijgen tot de volgende gerelateerde modellen, moet u de relatie van elk model met andere modellen begrijpen. **Omvat** parameter laat ontwikkelaars toe om tot de afhankelijke modellen toegang te hebben. U kunt een kommascheidingsteken gebruiken om toegang te krijgen tot meerdere modellen. Voor voorbeeldgebruik en meer informatie over **include**, raadpleeg de voorbeeldsectie voor het API-model op deze pagina.

**API-verzoek**

De API-verzoeken kunnen worden gedaan door een HTTP-verzoek in te dienen. Afhankelijk van het eindpunt en de methode kan de ontwikkelaar een keuze maken uit verschillende HTTP-woorden zoals GET, PUT, POST, DELETE, PATCH, enz. Voor sommige verzoeken kunnen queryparameters worden doorgegeven. Bij het aanvragen van een specifiek gegevensmodel kan de gebruiker ook een verzoek indienen voor gerelateerde modellen zoals beschreven in de JSON API-specificaties. De structuur van een typisch API-verzoek wordt beschreven in [voorbeeld modelgebruik](#main-pars_header_1415780624).

**API-respons**

Wanneer een API-verzoek wordt gedaan door een klant, wordt een SON-document verkregen volgens de JSON API-specificatie. De reactie bevat ook de HTTP-statuscode, die de ontwikkelaar kan verifiëren om de juiste volgende stappen in zijn toepassingslogica uit te voeren. De structuur van een typische API-respons wordt beschreven in  [voorbeeldmodelgebruik](#main-pars_header_1415780624).

**Fouten**

Wanneer een API-verzoek mislukt, wordt een Foutreactie verkregen. De HTTP-statuscode die in de reactie wordt teruggestuurd, geeft de aard van de fout aan. Foutcodes worden weergegeven met nummers voor elk model in de API-referentie. 200, 204, 400 en 404 zijn enkele veelvoorkomende fouten in API&#39;s die wijzen op problemen met HTTP-toegang.

**Velden**

De attributen van API-objecten en hun relatie worden gezamenlijk velden genoemd. Raadpleeg de [JSON API voor meer informatie.](http://jsonapi.org/format/#document-resource-object-fields) U kunt Velden als parameter gebruiken tijdens het maken van API-aanroepen om een of meer specifieke kenmerken van het model op te halen. Bij afwezigheid van de parameter Velden, haalt de API-aanroep alle beschikbare attributen van het model op. In de volgende API-aanroep worden bijvoorbeeld velden[vaardigheid]=name haalt u het naamkenmerk van het vaardigheidsmodel alleen op.

https://learningmanager.adobe.com/primeapi/v2/users/{userId}/userSkills/{id}?include=skillLevel.skill&amp;fields[skill]=name

**Paginering**

Soms resulteert een API-verzoek in een lange lijst van objecten die in de reactie moeten worden geretourneerd. In dergelijke gevallen stelt het pagineringsattribuut de ontwikkelaar in staat om de resultaten achter elkaar op te halen in termen van meerdere pagina&#39;s, waarbij elke pagina een reeks records bevat. Met het pagineringsattribuut in Learning Manager kunt u bijvoorbeeld het maximale aantal records instellen dat op een pagina moet worden weergegeven. Ook kunt u het waardebereik van de records definiëren die op de pagina moeten worden weergegeven.

**Sorteren**

Sorteren is toegestaan in API-modellen. Kies op basis van het model het type sortering dat op de resultaten moet worden toegepast. Sorteren kan oplopend of aflopend worden toegepast. Als u bijvoorbeeld `code sort=name`, dan wordt er oplopend gesorteerd op naam. Als u `code sort=-name`, wordt er aflopend gesorteerd op naam. Raadpleeg [JSON API-specificaties voor meer informatie](http://jsonapi.org/format/#fetching-sorting).

## API-gebruiksillustratie {#samplemodel}

Laten we een scenario overwegen waarbij een ontwikkelaar vaardigheidsnaam, maximale punten voor vaardigheidsniveau en punten die de student voor die vaardigheid heeft verdiend, wil ophalen.

Een userSkill-model in Learning Manager-API&#39;s heeft id, type, dateAchieved, dateCreated en pointsEarned als standaardattributen. Dus, wanneer een ontwikkelaar de GET-methode gebruikt om details van userSkill-model te verkrijgen, worden de huidige gegevens met betrekking tot de standaardattributen getoond in de responsuitvoer.

Maar in dit scenario wil de ontwikkelaar de naam van de vaardigheid en het vaardigheidsniveau van de gebruiker weten. Learning Manager-API stelt u in staat om toegang te krijgen tot deze gerelateerde informatie met behulp van relatievelden en de parameter include. De bijbehorende modellen voor userSkill worden verkregen in relatietags. U kunt de details van elk van de bijbehorende modellen opvragen door deze modellen samen met de userSkill op te roepen. Voor deze informatie gebruikt u **`code include`** parameter met door punt (punt) gescheiden waarden voor elk van de bijbehorende modellen. U kunt een komma als scheidingsteken gebruiken om een ander model aan te vragen, zoals user include=skillLevel.skill,course

**API-aanroep**

`https://learningmanagerqe1.adobe.com/primeapi/v1/users/%7buserId%7d/userSkills/%7bid%7d?include=skillLevel.skill&fields%5bskill%5d=name&fields%5bskillLevel%5d=maxCredits&fields%5buserSkill%5d=pointsEarned`

UserId kan bijvoorbeeld 746783 zijn en het userSkills id: 746783_4426_1.

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

## Learning Manager-modellen {#models}

De Learning Manager-API geeft ontwikkelaars toegang tot Learning Manager-objecten als RESTful-resources. Elk API-eindpunt vertegenwoordigt een bron, meestal een object zoals een badge, of een verzameling van dergelijke objecten. De ontwikkelaars gebruiken vervolgens de HTTP-werkwoorden zoals PUT, GET, POST en DELETE om de CRUD-bewerkingen op die objecten (collecties) uit te voeren.

+++V1 API

Het volgende diagram geeft de verschillende elementen van het Learning Manager-objectmodel in V1 API weer.

![](assets/er-diag-primemodels.png)

In de volgende tabel worden verschillende elementen van het objectmodel van Leermanager V1 beschreven:

<table border="1" cellspacing="0" cellpadding="0">
 <tbody>
  <tr>
   <td>
    <p><strong>Serienummer</strong></p></td>
   <td>
    <p><strong>Learning Manager-object</strong></p></td>
   <td>
    <p><strong>Beschrijving</strong></p></td>
  </tr>
  <tr>
   <td>
    <p>1.      </p></td>
   <td>
    <p>gebruikersinterface</p></td>
   <td>
    <p>Gebruiker is het belangrijkste model in Learning Manager. Gebruikers zijn meestal de interne of externe studenten van een organisatie die leerobjecten gebruiken. Zij kunnen echter ook een andere rol spelen, zoals auteur en manager, naast de rol van de student. Gebruikers-ID, -type en -e-mail zijn enkele van de inline attributen. </p></td>
  </tr>
  <tr>
   <td>
    <p>2.      </p></td>
   <td>
    <p>cursus</p></td>
   <td>
    <p>Cursus is een van de leerobjecten die in Learning Manager wordt ondersteund en bestaat uit een of meer modules. </p></td>
  </tr>
  <tr>
   <td>
    <p>3.      </p></td>
   <td>
    <p>module</p></td>
   <td>
    <p>Module is een bouwsteen om leerobjecten te maken in Learning Manager. De modules kunnen bestaan uit vier verschillende soorten modules, zoals klassikaal, virtueel klassikaal, activiteit en op eigen tempo. Gebruik dit modulemodel om de details van alle modules in een account te krijgen. </p></td>
  </tr>
  <tr>
   <td>
    <p>4.      </p></td>
   <td>
    <p>certification</p></td>
   <td>
    <p>De certificering wordt toegekend aan studenten op basis van het succesvol afronden van een cursus. Voordat u gebruik kunt maken van certificeringen moeten in de toepassing cursussen worden aangemaakt. </p></td>
  </tr>
  <tr>
   <td>
    <p>5.      </p></td>
   <td>
    <p>learning program</p></td>
   <td>
    <p>Leerprogramma's zijn uniek ontworpen cursussen die voldoen aan de specifieke leerbehoeften van gebruikers. Gewoonlijk worden de leerprogramma's gebruikt om leerdoelen die zich over de individuele cursussen uitstrekken, aan te sturen. </p></td>
  </tr>
  <tr>
   <td>
    <p>6.      </p></td>
   <td>
    <p>badge</p></td>
   <td>
    <p>Een badge is een vorm van prestatiebeloning die studenten krijgen als ze specifieke mijlpalen bereiken. </p></td>
  </tr>
  <tr>
   <td>
    <p>7.      </p></td>
   <td>
    <p>skill</p></td>
   <td>
    <p>Het vaardighedenmodel bestaat uit niveaus en punten. Vaardigheden kunnen door de studenten worden verworven na het afronden van de cursus. </p></td>
  </tr>
  <tr>
   <td>
    <p>8.      </p></td>
   <td>
    <p>certificationEnrollment</p></td>
   <td>
    <p>Dit model geeft details over een inschrijving door een gebruiker voor één enkele certificering.</p></td>
  </tr>
  <tr>
   <td>
    <p>9.  </p></td>
   <td>
    <p>courseEnrollment</p></td>
   <td>
    <p>Dit model geeft details over een inschrijving door een gebruiker voor één enkele cursus. </p></td>
  </tr>
  <tr>
   <td>
    <p>10.  </p></td>
   <td>
    <p>courseInstance</p></td>
   <td>
    <p>Aan een cursus kunnen één of meerdere instanties verbonden zijn. U kunt een cursusinstantie krijgen </p></td>
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
    <p>job aid</p></td>
   <td>
    <p>Een taakhulp is een leerinhoud die toegankelijk is voor studenten zonder inschrijvings- of afrondingscriteria. U kunt informatie ophalen, zoals bijgewerkte datum, status, ID-informatie samen met de bijbehorende modellen, zoals de versie van de taakhulp, de auteurs en het vaardigheidsniveau. </p></td>
  </tr>
  <tr>
   <td>
    <p>15.  </p></td>
   <td>
    <p>jobAidVersion</p></td>
   <td>
    <p>Een taakhulp kan één of meerdere daaraan gekoppelde versies hebben, gebaseerd op nummerherzieningen in inhoud en aantal uploads. Dit model geeft details over één enkele taakhulpversie. </p></td>
  </tr>
  <tr>
   <td>
    <p>16.  </p></td>
   <td>
    <p>learningProgramInstanceEnrollment</p></td>
   <td>
    <p>Het leerprogramma bestaat uit één of meerdere instanties. Studenten kunnen zichzelf inschrijven voor een leerprogramma of krijgen deze toegewezen door de beheerder. Dit model geeft details over een inschrijving door een gebruiker voor één leerprogramma. </p></td>
  </tr>
  <tr>
   <td>
    <p>17.  </p></td>
   <td>
    <p>moduleVersion</p></td>
   <td>
    <p>Een module kan één of meerdere versies hebben op basis van de uploads van herziene inhoud. Gebruik dit model om specifieke informatie te verkrijgen over elke afzonderlijke moduleversie. </p></td>
  </tr>
  <tr>
   <td>
    <p>18.  </p></td>
   <td>
    <p>skillLevel</p></td>
   <td>
    <p>Een vaardigheidsniveau bestaat uit één of meer cursussen die moeten worden gevolgd om een niveau te bereiken met de bijbehorende punten. </p></td>
  </tr>
  <tr>
   <td>
    <p>19.  </p></td>
   <td>
    <p>userBadge</p></td>
   <td>
    <p>Gebruikersbadge koppelt afzonderlijke badges aan afzonderlijke gebruikers. Het bevat details zoals wanneer de het is verdiend, assertionUrl etc. </p></td>
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

Hieronder volgen de verschillende elementen van het Learning Manager-klasdiagram in V2 API.

![](assets/v2api-class-diagram.jpg)

<table>
 <tbody>
  <tr>
   <th><b>Learning Manager-object</b></th>
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
   <td>Een badge is een vorm van prestatiebeloning die studenten krijgen als ze specifieke mijlpalen bereiken. <br></td>
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
   <td>Gebruiker is het belangrijkste model in Learning Manager. Gebruikers zijn meestal de interne of externe studenten van een organisatie die leerobjecten gebruiken. Zij kunnen echter naast de rol van de student een andere rol op zich nemen, zoals auteur en manager. Gebruikers-ID, -type en -e-mail zijn enkele van de inline attributen. </td>
  </tr>
  <tr>
   <td>resource</td>
   <td>Leermiddel wordt gebruikt voor het modelleren van elke inhoudsbron die voor een module moet worden geordend. Alle bronnen ingekapseld in <code>
     an
    </code> <code>
     loResource
    </code> zijn gelijkwaardig in termen van het leerdoel, maar verschillen van elkaar in termen van leveringstype of landinstelling van inhoud.<br></td>
  </tr>
  <tr>
   <td>userNotification</td>
   <td>Dit model bevat kennisgevingsinformatie over een student.<br></td>
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
   <td>skill</td>
   <td>Het vaardighedenmodel bestaat uit niveaus en punten. Vaardigheden kunnen door de studenten worden verworven na het afronden van de cursus. <br></td>
  </tr>
  <tr>
   <td>skillLevel</td>
   <td>Een vaardigheidsniveau bestaat uit één of meer cursussen die moeten worden gevolgd om een niveau te bereiken met de bijbehorende punten. <br></td>
  </tr>
  <tr>
   <td>learningObject</td>
   <td>Een leerobject is een abstractie voor verschillende soorten objecten waar gebruikers zich voor kunnen inschrijven en van kunnen leren. Op dit moment heeft Leermanager de vier typen leerobjecten: Cursus, Certificering, Leerprogramma <code>
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
    </code> meer modules. In Learning Manager kan een module op verschillende gelijkwaardige manieren worden geleverd. Daarom <code>
     loResource
    </code> omvat in wezen al die gelijkwaardige middelen.<br></td>
  </tr>
  <tr>
   <td>loResourceGrade<br></td>
   <td>Dit vat het resultaat samen van de gebruiker die een specifieke bron gebruikt in de context van een leerobject waarvoor hij/zij is ingeschreven. Het bevat informatie zoals de duur die door <code>
     user
    </code> in de resource, de procentuele voortgang die de gebruiker heeft geboekt, de status geslaagd/gezakt en de score die de gebruiker heeft behaald in een bijbehorende quiz.<br></td>
  </tr>
  <tr>
   <td>calendar<br></td>
   <td>Een kalenderobject is een lijst met <code>
     upcoming classroom
    </code> of virtuele klassikale cursussen waarvoor de gebruiker zich kan inschrijven.<br></td>
  </tr>
  <tr>
   <td>l1FeedbackInfo<br></td>
   <td>L1-Feedback omvat de antwoorden van een student op de feedbackvragen die betrekking hebben op leerobjecten. Meestal wordt dit verzameld nadat de gebruiker een leerobject heeft voltooid indien dit is geconfigureerd om dergelijke feedback van studenten te verzamelen.<br></td>
  </tr>
  <tr>
   <td>enrollment<br></td>
   <td>Deze abstractie omvat de details met betrekking tot de transactie die de toewijzing van een specifieke gebruiker aan een specifieke leerobjectinstantie weergeeft.<br></td>
  </tr>
 </tbody>
</table>

+++

Lijst met objectkenmerken en -relaties.

+++account

**Kenmerken**
dateCreated\
gamificationEnabled\
op\
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
op\
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
op\
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
op\
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
op\
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
op\
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
op\
progressPercent\
score

**Relaties**
loResource(learningObjectResource)

+++

+++learningObjectSkill

**Kenmerken**
credits\
op\
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
op\
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
op\
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
e-mail\
velden\
op\
name\
pointsEarned\
profile\
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
op\
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
op\
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
op\
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
op\
pointsEarned

**Relaties**
learnerBadge(userBadge)\
learningObject(learningObject)\
skillLevel(skillLevel)\
user(user)

+++

## Het ontwikkelingsproces van toepassingen {#registration}

## Vereisten {#prerequisites}

Als ontwikkelaar moet u een proefaccount bij Learning Manager aanmaken, zodat u volledige toegang hebt tot alle rollen binnen dat account. Om een toepassing te kunnen schrijven, moet een ontwikkelaar een aantal gebruikers en cursussen aanmaken en het account in een redelijke staat brengen, zodat de toepassing in ontwikkeling toegang kan krijgen tot wat voorbeeldgegevens.

## Maak client-ID en -geheim {#createclientidandsecret}

1. In **Integratiebeheerder** aanmelden, klikken **[!UICONTROL Toepassingen]** in het linkerdeelvenster.

   ![](assets/application-development-menu.png)

   *Toepassingen selecteren op integratiebeheerder*

1. Klikken **[!UICONTROL Registreren]** rechtsboven op de pagina om uw toepassingsgegevens te registreren. Registratiepagina verschijnt.

   ![](assets/register-application.png)

   *De toepassing registreren*

   Het is verplicht om alle velden op deze pagina in te vullen.

   **Naam van de toepassing**: voer uw aanvraagnaam in. Het is niet verplicht om dezelfde toepassingsnaam te gebruiken; het kan elke geldige naam zijn.

   **URL**: als u de exacte URL weet waar de toepassing gehost wordt, kunt u deze vermelden. Als u die niet weet, kunt u de URL van uw bedrijf vermelden. Geldige URL-naam is verplicht in dit veld.

   **Doorstuurdomeinen**: voer de domeinnaam in van de toepassing waarnaar u de Learning Manager-toepassing na de OAuth-authenticatie wilt omleiden. U kunt hier meerdere URL&#39;s vermelden, maar u moet wel geldige URL&#39;s gebruiken, zoals `http://google.com`, `http://yahoo.com` enzovoort.

   **Omschrijving:** Voer een korte beschrijving in voor uw toepassing.

   **Bereiken:** Kies een van de vier beschikbare opties om het bereik van uw toepassing te definiëren. Op basis van uw hier vermelde keuze zijn Learning Manager-API-eindpunten toegankelijk voor uw toepassing. Als u bijvoorbeeld **Leestoegang studentrol** en zijn alle API-eindpunten voor studenten van de Learning Manager alleen-lezen voor uw toepassing toegankelijk.

   **Alleen voor dit account?**\
   **Ja** - als u Ja kiest, is de toepassing niet zichtbaar voor andere accountbeheerders.\
   **Nee** - als u Nee kiest, kunnen andere accountbeheerders deze toepassing ook openen, maar ze moeten de toepassings-id gebruiken om toegang te krijgen tot deze toepassing. Toepassings-id wordt gegenereerd en weergegeven in de bewerkingsmodus van de Learning Manager-toepassing.

   Als u **Beheerdersrol lees- en schrijftoegang** als bereik tijdens de registratie van de toepassing en kies **Leestoegang beheerdersrol** tijdens het ontwerpen van de API&#39;s kunt u nog steeds schrijftoegang voor de toepassing hebben, aangezien het registratiebereik van de app de autorisatieworkflow vervangt.

1. Klik na het invullen van de gegevens op de registratiepagina op **[!UICONTROL Registreren]** in de rechterbovenhoek.

## Ontwikkeling en testen van toepassingen {#applicationdevelopmentandtesting}

De Learning Manager-API kan door ontwikkelaars worden gebruikt om een willekeurige toepassing te bouwen. Ontwikkelaars moeten ervoor zorgen dat hun accounts bestaan uit een aantal geldige gebruikers en cursussen. Ze kunnen dummygebruikers en cursussen aanmaken en activiteiten simuleren in het proefaccount, zodat ze de functionaliteit van de toepassing kunnen testen.

## Toepassingsimplementatie {#applicationdeployment}

We raden aan dat de Learning Manager-beheerder of een integratiebeheerder voor het productieaccount de toepassing beschikbaar maakt voor gebruikers binnen hun organisatie. Zodra de toepassing is getest en klaar is voor productie, informeert u de beheerder over het productieaccount. Idealiter genereren de beheerders een nieuw client-ID en clientgeheim voor de toepassing in het productie-account en voeren ze de nodige stappen uit om deze op een veilige manier in de toepassing te integreren. De eigenlijke procedure voor de implementatie van toepassingen varieert van onderneming tot onderneming en de Learning Manager-beheerder van uw organisatie moet ondersteuning krijgen van de IT/IS-afdeling binnen uw organisatie om de implementatie te voltooien.

## Externe goedkeuring van de toepassing {#externalapplicationapproval}

U kunt externe toepassingen toevoegen door op **Goedkeuren** in de rechterbovenhoek van het deelvenster **Toepassingen** pagina. Geef de externe toepassings-ID op en klik op **Opslaan.**

![](assets/add-external-application.png)

*Een externe toepassing toevoegen en goedkeuren*

## Veelgestelde vragen

+++Heeft Learning Manager een e-commerce-integratie?

Adobe Learning Manager heeft geen e-commerce-integratie. We bieden echter wel API&#39;s zodat u uw eigen headless LMS kunt maken en e-commerce functies kunt implementeren.
+++
