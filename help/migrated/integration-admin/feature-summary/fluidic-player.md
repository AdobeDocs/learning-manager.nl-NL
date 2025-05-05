---
description: Lees dit artikel voor meer informatie over het integreren van de Fluidic Player in een aangepaste toepassing.
jcr-language: en_us
title: Insluitbare Fluidic Player
contentowner: dvenkate
preview: true
source-git-commit: fba5e5ddc1964b485be473bf356806f234688cf4
workflow-type: tm+mt
source-wordcount: '1626'
ht-degree: 25%

---



# Insluitbare Fluidic Player

Lees dit artikel voor meer informatie over het integreren van de Fluidic Player in een aangepaste toepassing.

Als onderneming kunt u nu een aangepaste ervaring bieden aan uw leerlingen, zelfs buiten Learning Manager om. Met behulp van de openbare API kunt u alle informatie over leerobjecten, inschrijvingen van studenten en leervoortgang ophalen en op uw website weergeven. U kunt zelfs de Fluidic Player van Learning Manager in uw website integreren, zodat de student de inhoud direct binnen uw eigen website kan gebruiken. Met de Fluidic Player kunt u elk inhoudstype afspelen dat ondersteund wordt door Learning Manager. Als de website is ingesloten op uw eigen website, heeft deze precies dezelfde mogelijkheden als wanneer deze wordt gebruikt in Leerbeheer.

**Alle eLearning-inhoud afspelen[&#128279;](../../learners/feature-summary/fluidic-player.md#main-pars_text_779047019)**

De Fluidic Player speelt vrijwel elk type eLearning-inhoud op dezelfde consistente en intuïtieve manier af zonder dat er plugins of downloads nodig zijn. De student kan de inhoud starten en deze wordt ongeacht het type inhoudsbestand afgespeeld.

**Opmerkingen en bladwijzers**

U kunt opmerkingen maken en bij elke inhoud, ongeacht het bestandstype, bladwijzers gebruiken. Als u een bepaalde selectie wilt maken uit een lang bestand of video, kunt u een bladwijzer maken van precies de punten waar u de informatie hebt gevonden die relevant is voor uw behoeften. De opmerkingen en bladwijzers kunnen worden doorzocht of als e-mail worden verzonden. Door erop te klikken opent de Fluidic Player precies op het punt van de video of op de pagina van het document waar u de bladwijzer geplaatst hebt.

Zie voor meer informatie over Fluidic Player [Fluidic Player](../../learners/feature-summary/fluidic-player.md).

Hier volgen enkele voorbeelden van het gebruik van de insluitbare Fluidic Player.

* U kunt de insluitbare Fluidic Player op uw **&#x200B; **&#x200B;website gebruiken om een overzicht te geven van de cursussen waarvoor uw medewerker is ingeschreven en om een koppeling te verschaffen om een training op dezelfde pagina te starten. Dit zou betekenen dat uw studenten trainingen op uw intranetwebsite kunnen volgen.

* Als u in de opleidingssector werkt, hebt u misschien een website waar uw klanten cursussen aanschaffen. U kunt de insluitbare speler met dezelfde website integreren, zodat uw klanten de inhoud die ze kopen, binnen uw website kunnen gebruiken.

## Stappen om een Fluidic Player in uw website te integreren {#stepstoembedfluidicplayerinyourwebsite}

Voor het bouwen van een aangepaste toepassing voor het insluiten van Fluidic Player in uw website moeten drie basisstappen worden gevolgd:

1. Maak een toepassing aan in de integratiebeheerder-app van Learning Manager.
1. Haal een toegangstoken op.
1. Gebruik een toegangstoken om leermiddelen van Leermanager op te halen met behulp van een openbare API.

### 1. Maak een toepassing aan in integratiebeheerder {#1createanapplicationinintegrationadmin}

Deze stap is nodig om een toepassings-/client-ID en toepassings-/clientgeheim aan te maken die gebruikt wordt om een vernieuwingstoken en een toegangstoken op te halen. Ga voor meer informatie over het maken van een toepassing naar  [Ontwikkeling van toepassingen.](developer-manual.md#main-pars_header_994876235)

1. Ga naar de **[!UICONTROL IntegrationAdmin]**-app en open **[!UICONTROL Toepassingen]**.

1. Selecteer **[!UICONTROL Registreren]** in de rechterbovenhoek van de pagina.
1. Het venster **[!UICONTROL Registreer een nieuwe toepassing]** wordt geopend. Vul de verplichte velden in.
1. Als een aangepaste toepassing moet worden gedeeld door meerdere accounts, selecteert u **[!UICONTROL Nee]** in het optieveld  **[!UICONTROL Alleen voor dit account?]**
1. Klik op **[!UICONTROL Opslaan]** om de toepassing op te slaan en uw toepassings-ID en -geheim te genereren.

### 2. Toegangstoken ophalen {#2retrievingaccesstoken}

Aangezien de Leermanager OAUTH2.0. gebruikt, is het toegangstoken vereist om middelen terug te winnen gebruikend openbare API. Het toegangstoken kan worden opgehaald met behulp van een vernieuwingstoken, een client-ID of een clientgeheim.

**2.1 Vernieuwingstoken**

* OAuth Code ophalen

OAuth code is vereist om vernieuwingstoken op te halen. De leermanager leidt de gebruiker naar de omleidings-URL met de OAuth-code wanneer deze zich aanmeldt met de onderstaande url (OAuth-code-extractie wordt geïllustreerd in het bestand &quot;oauthredirect.html&quot; in de voorbeeldtoepassing):

```
code https://learningmanager.adobe.com/oauth/o/authorize  
client_id= <application_id>  
&redirect_uri=<redirect_uri>  
&state=<dummy_data>  
&scope=learner:read,learner:write  
&response_type=CODE  
&account=<account_id>  
&email=<email_id>
```

Hier, **[!UICONTROL client-id]** is de toepassings-id die is verkregen in stap 1.
**[!UICONTROL redirect_url]** is redirect_url ingesteld in stap 1.
**[!UICONTROL status]** is om het even welke dummygegevens waarop wij redirect URL moeten filtreren om code OAuth te krijgen. Bereik is het studentenbereik dat is ingesteld in Stap 1.
**[!UICONTROL response_type]**&#x200B;e is altijd &quot;CODE&quot;.\
**[!UICONTROL account]**&#x200B;is een optioneel veld\
**[!UICONTROL email]** is een optioneel veld\
&#42; Als zowel account-ID als e-mail worden opgegeven, kan de gebruiker zich via de bovenstaande URL bij hetzelfde account aanmelden. Dit eindpuntvoorbeeld wordt weergegeven in het bestand &quot;index.html&quot; in de voorbeeldtoepassing.

* Vernieuwingstoken ophalen

Zodra OAuth code wordt ontvangen, kan het vernieuwingstoken worden teruggewonnen gebruikend de ontvangen code OAuth, cliëntidentiteitskaart, en cliëntgeheim van het hieronder eindpunt:

**https://learningmanager.adobe.com/oauth/token**

Als antwoord op uw postaanvraag ontvangt u het volgende:

i. refresh_token\
ii. access_token\
iii. user_id\
iv. verloopt_in\
v. user_role\
vi. account_id

**2.2 Toegangstoken ophalen uit vernieuwingstoken**

Om uw toegangstoken op te halen, stuurt u een ander verzoek met uw refresh_token, client_id en client_geheic als hoofdtekst van de post naar de onderstaande URL:

**https://learningmanager.adobe.com/oauth/token/refresh**

Als antwoord op uw postaanvraag ontvangt u het volgende:\
i. refresh_token\
ii. access_token\
iii. user_id\
iv. verloopt_in\
v. user_role\
vi. account_id

### 3. Ophalen van leermiddelen met behulp van openbare API {#3retrieveresourcesusingpublicapi}

Als derde stap moet u het toegangstoken gebruiken om leermiddelen op te halen uit Leermanager met behulp van openbare API.  Toegangstoken is vereist om een openbare API-aanroep te maken en moet worden toegevoegd aan de koptekst, zoals wordt geïllustreerd in de voorbeeldtoepassing.

## Insluitbare speler {#embeddableplayer}

Toepassingen van derden kunnen gebruikmaken van een geïntegreerde speler om de inhoud van een leerobject af te spelen.

**Open een cursus in de insluitbare speler**

1. Maak een insluitbare URL aan

   Als u een cursus wilt openen met een insluitbare speler, moet u een insluitbare URL maken, zoals hieronder wordt weergegeven:

   `https://learningmanager.adobe.com/app/player?lo_id=<v2-api course id>&access_token=<access_token>`

   Hier moet lo_id voldoen aan het V2 API cursus-id-formaat.

   Voorbeeld: `https://learningmanager.adobe.com/app/player?lo_id=course:123456&access_token=45b269b75ac65d6696d53617f512450f`

   Certificeringen, leerprogramma&#39;s en taakhulpen kunnen ook worden afgespeeld in de insluitbare speler.

   Voorbeelden: `https://learningmanager.adobe.com/app/player?lo_id=certification:12345&access_token=c1a4847dfbf4007826a027d481b93c1e`

   `https://learningmanager.adobe.com/app/player?lo_id=learningProgram:12345&access_token=c1a4847dfbf4007826a027d481b93c1e`

   `https://learningmanager.adobe.com/app/player?lo_id=jobAid:1234&access_token=c1a4847dfbf4007826a027d481b93c1e`

1. Stel deze URL in het kenmerk &quot;src&quot; van iframe in.

**Insluitbare speler sluiten**

```
code window.addEventListener("message", function closePlayer(){  
   if(event.data === "status:close"){  
     //handle closing event  
   }  
});
```

## Tutorial voor voorbeeldtoepassing {#sampleapplicationtutorial}

Het bijgevoegde pdf-document bevat een voorbeeldtoepassingszelfstudie.
[Voorbeeldzelfstudie en tutorialbron voor het insluiten van Fluidic Player.](assets/sample-applicationtutorial.zip) Alternatieve inhoud

Als beheerder kunt u uw cursusmateriaal zodanig instellen dat u alternatieve inhoud kunt aanbieden aan uw studenten in de Fluidic Player. Als u bijvoorbeeld studenten in verschillende regio&#39;s hebt die meerdere talen willen gebruiken, kunt u dezelfde inhoud in meerdere talen maken. De Fluidic Player zal de student de taal bieden waarvoor hij of zij kan worden ingesteld, maar de student heeft ook de keuze om rechtstreeks vanuit de speler over te schakelen op een andere taal.

Videospecifieke besturingselementen

De streamingtechnologie die wordt gebruikt door de Fluidic Player van Learning Manager, biedt de studenten een ervaring voor het afspelen van video zonder vertraging bij het starten van de video en zonder vereisten voor schijfruimte op elk apparaat. De Fluidic Player biedt ook slimme besturingselementen zoals de afspeelsnelheid (1x, 1,5x) en het overslaan van +-10 seconden. Deze zijn ontworpen om de student precies de controle te geven die ze nodig hebben om hun leersnelheid aan te passen.

Dit is een inspanning die door iemand van uw team van IT of een externe adviseur moet worden ondernomen die een toepassing kan bouwen die dan op uw plaats wordt ontvangen.

1. Wijzig de ingesloten speler-URL van de Learning Manager met parameters die wijzen naar het exacte leerobject dat moet worden gevolgd.

   URL:  [https://learningmanager.adobe.com/app/player](https://cpcontents.adobe.com/public/embedplayer/index22fa615ec2baa034a22090c8cd4289fa.html)

1. Gebruik een van de volgende parameters om een cursus te starten:

   * course_id : Dit is de ID van de cursus die moet worden gestart
   * learning_program_id : Dit is de id van het leerprogramma dat moet worden gestart
   * certification_id: Dit is de id van de certificering die moet worden gestart
   * lo_id: De id van het te spelen leerobject (cursus/leerprogramma/certificering/taakhulp)


1. Gebruik toegangstoken als een verplichte parameter.

   * access_token: Dit is de beveiligingsparameter, gebruik het openbare API-toegangstoken

   U kunt uw token verkrijgen door uw insluitbare Fluidic Player in te stellen in uw integratiebeheerder. U kunt uw verificatietoken ophalen dat u als toegangstoken kunt gebruiken.

   Voorbeeld van gemaakte URL; https://learningmanager.adobe.com/app/player?lo_id=&quot;+lo_id+&quot;&amp;access_token=&quot;+accToken

   Hier is lo_id de id van de cursus, het leerprogramma, de certificering en de taakhulp.

   Voorbeelden van lo_id - course:21324, learningProgram:2143, certification:23432, jobAid:237

1. Maak API-aanroepen van Learning Manager om de bovengenoemde parameters op te halen.

   Deze API-aanroepen moeten worden uitgevoerd door de toepassing die uw IT-team/consultant zou schrijven en hosten op uw site.

   Meer informatie over het gebruik van de API vindt u hier:

   Learning Manager V1 API - [https://learningmanager.adobe.com/docs/primeapi/v1/](https://learningmanager.adobe.com/docs/primeapi/v1/)



   Learning Manager V2 API - [https://learningmanager.adobe.com/docs/primeapi/v2/](https://learningmanager.adobe.com/docs/primeapi/v2/)

   De id&#39;s van de objecten verschillen van de V1- en V2-API. De insluitbare speler verwacht id&#39;s in v2-indeling. Gebruik de ID-mapping-API in V2 om van V1-id&#39;s om te zetten in V2-id&#39;s.

   Nadat de URL is samengesteld, kan de toepassing deze gebruiken voor weergave aan de student door deze in een iFrame te plaatsen. Als u op deze koppeling klikt, wordt de Fluidic Player gestart met de desbetreffende cursus in de context.

   ![](assets/salesforce-player.png)

   Meld u aan bij Learning Manager om de voortgangsrapporten en voltooiingsrapporten te controleren.

   Wanneer de student de Player sluit, stuurt de Fluidic Player een &quot;close&quot;-bericht naar het bovenliggende element met html5 postMessage. De laadcontroller moet dit bericht afhandelen en doorgaan.

Wijzig de ingesloten speler-URL van de Learning Manager met parameters die wijzen naar het exacte leerobject dat moet worden gevolgd.

URL:  [https://learningmanager.adobe.com/app/player](https://learningmanager.adobe.com/app/player)

Met een van deze parameters kunt u een cursus starten:

* course_id : Dit is de ID van de cursus die moet worden gestart
* learning_program_id : Dit is de id van het leerprogramma dat moet worden gestart
* certification_id: Dit is de id van de certificering die moet worden gestart
* lo_id: De id van het te spelen leerobject (cursus/leerprogramma/certificering/taakhulp)

Verplichte parameter:

* access_token: Dit is de beveiligingsparameter, gebruik het openbare API-toegangstoken

Maak API-aanroepen van Learning Manager om de bovengenoemde parameters op te halen. Deze API-aanroepen moeten worden uitgevoerd door de toepassing die uw IT-team/consultant zou schrijven en hosten op uw site.

Meer informatie over het gebruik van de API vindt u hier:

Learning Manager V1 API - [https://learningmanager.adobe.com/docs/primeapi/v1/](https://learningmanager.adobe.com/docs/primeapi/v1/)



Learning Manager V2 API -  [https://learningmanager.adobe.com/docs/primeapi/v2/](https://learningmanager.adobe.com/docs/primeapi/v2/)


