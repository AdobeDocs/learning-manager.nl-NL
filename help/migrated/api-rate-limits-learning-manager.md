---
jcr-language: en_us
title: API-snelheidslimieten in Learning Manager
contentowner: saghosh
preview: true
source-git-commit: 544c695a77c21dd9162b9b943b6119d27aa373dc
workflow-type: tm+mt
source-wordcount: '1757'
ht-degree: 0%

---



# API-snelheidslimieten in Learning Manager

## Inleiding tot tariefbeperking {#introductiontoratelimiting}

Adobe Learning Manager maakt een uitgebreide suite van REST API beschikbaar waarmee klanten toepassingen kunnen bouwen die integreren met Learning Manager, of zelfs aangepaste gebruikerservaringen en -uitbreidingen kunnen maken voor workflows die hun bedrijf helpen.

Telkens wanneer een API wordt aangeroepen, zijn er gedeelde computerbronnen die worden gebruikt in de Learning Manager-servers. Daarom moeten we zorg en voorzichtigheid betrachten om ervoor te zorgen dat de toepassingen goed worden afgespeeld en de prestaties en beschikbaarheidskenmerken van het platform niet in gevaar brengen. Dit wordt bereikt door beperkingen in te voeren op de manier waarop API-clients aanroepen (frequentie en snelheid).

Een toepassing kan bijvoorbeeld proberen alle gebruikers in dat account op te halen en kan snel meerdere gepagineerde API-aanroepen uitvoeren. Een ontwikkelaar zou dit per ongeluk kunnen aanroepen in een krappe lus, met als gevolg een enorme belasting van de server, waardoor toepassingen traag worden en zelfs het platform in gevaar wordt gebracht door meer middelen te verbruiken dan bedoeld of vereist.

Om dit probleem op te lossen, introduceren wij tariefgrenzen op hoeveel API vraag door één enkele gebruiker in een specifieke cliënttoepassing van een specifiek rekening kan worden gemaakt. We meten dit in termen van verzoeken per minuut, afgekort tot RPM. Als we bijvoorbeeld zeggen dat de limiet voor API-aanroepen van GET 600 rpm is, betekent dit dat één gebruiker niet meer dan 600 aanroepen per minuut kan uitvoeren. Als de gebruiker deze limiet overschrijdt, krijgt de gebruiker een beperkte snelheid. De verzoeken worden bijgehouden op milliseconde granulariteit, zodat beantwoordt deze grens aan 1 verzoek elke 100 milliseconden (ms). Er is nog een parameter, Burst, die ook samen met de snelheidslimiet wordt gedefinieerd, die bepaalt hoeveel verzoeken een gebruiker kan indienen boven de opgegeven snelheid (in ons geval 600 RPM). Als de Burst-parameter bijvoorbeeld 10 is, betekent dit dat er maximaal 10 sleuven in een wachtrij worden toegewezen en dat wanneer een verzoek &quot;te vroeg&quot; arriveert (in ons geval eerder dan 100 ms), de Burst-parameter onmiddellijk wordt verwerkt als er een sleuf beschikbaar is voor de wachtrij in de wachtrij. De sleuf wordt dan gemarkeerd als &#39;ingenomen&#39; en wordt niet vrijgemaakt voor gebruik door een ander verzoek totdat het juiste tijdstip is verstreken (in ons geval na 100 ms). Het echte verkeer is over het algemeen met barsten, en dat is waar de parameter van de Burst helpt. Voor het Learning Manager-platform definiëren we limieten voor een specifieke API-versie (bijvoorbeeld V2), de rol (student/beheerder) en een werkwoord (GET/PUT/POST/DELETE/PATCH). In het voorbeeld zouden we hierboven beschrijven dat de tarieflimiet (600, 10) is.

Hoewel we in Learning Manager altijd tarieflimieten voor openbare API hebben gehad, hebben we tot nu toe vrij liberaal gewerkt aan het toestaan van een zeer hoge RPM. Door de groei van uw favoriete leerplatform hebben we echter een snelle groei gezien in het gebruik van onze API en hebben we besloten om deze tarieflimieten expliciet te documenteren ten behoeve van al onze klanten en voor een beter beheer van het platform. In deze context hebben we onze API bijgewerkt om te beginnen met het retourneren van een nieuwe API-respons (HTTP Status Code 429), die u tot nu toe nog niet hebt gezien. Deze reactie wordt gegeven aan API cliënten, wanneer de tariefgrens wordt overschreden. Clienttoepassingen moeten deze responscode nu afhandelen om aan te passen aan de logica van hun toepassing. Dit document is voornamelijk bedoeld om ontwikkelaars te helpen met de informatie die ze nodig hebben om de juiste logica in hun code op te nemen wanneer ze een dergelijke reactie zien.

## Hoe kan ik de afgedwongen tarieflimieten bevestigen? {#howtoconfirmtheenforcedratelimits}

Voor elke aanvraag bevatten de antwoordheaders de volgende informatie:

```
x-rate-limit: 600r/m 
x-burst: 10
```

* x-rate-limit specificeert de drempel van het basisvraagtarief in termen van verzoeken per minuut.
* x-burst specificeert hoeveel het overschrijden van verzoeken boven het tarief van het basisverzoek om onmiddellijk worden verwerkt worden aanvaard.

## Hoe kan ik fouten afvangen die worden veroorzaakt door tarieflimieten? {#howtocatcherrorscausedbyratelimits}

U kunt voor elk verzoek controleren of u bent overgegaan tot de tarieflimiet. Als u een antwoordcode van 429 krijgt, &quot;{&quot;message&quot;:&quot;429 Te veel verzoeken&quot;}&quot;, hebt u de tarieflimiet bereikt.

Het is aan te raden code in uw script op te nemen die 429 reacties afvangt. Als uw script de fout &#39;Te veel verzoeken&#39; negeert en steeds probeert verzoeken te doen, krijgt u mogelijk null-fouten. Op dat punt is de foutinformatie niet nuttig bij het diagnosticeren van het probleem.

Een krullverzoek dat in de tarieflimiet springt, kan bijvoorbeeld de volgende reactie retourneren:

```
< HTTP/2 429 
< date: Wed, 04 Nov 2020 06:53:04 GMT 
< content-type: application/json; charset=utf-8 
< server: openresty 
< x-rate-limit: 60r/m 
< x-burst: 10 
< retry-after: 10.752 
< access-control-allow-credentials: true 
< access-control-allow-methods: GET, POST, OPTIONS, PUT, HEAD, DELETE, PATCH 
< access-control-allow-headers: X-acap-all-roles, X-acap-account,X-acap-user,X-acap-caller-role,Keep-Alive,User-Agent,X-Requested-With,If-Modified-Since,Cache-Control,Content-Type, x-experience-api-version, Authorization, X-CSRF-TOKEN, X-HTTP-Method-Override 
< strict-transport-security: max-age=31536000; includeSubDomains 
< x-frame-options: SAMEORIGIN 
< x-xss-protection: 1 
< x-content-type-options: nosniff 
< x-request-id: gwBBFC9741-58A5-43B1-B1FE-7D14275961E7 
< strict-transport-security: max-age=31536000; includeSubDomains
```

De reactie bevat informatie over de volgende toetsen:

```
status: 429 
retry-after: 10.752
```

De statuscode van 429 betekent &quot;te veel verzoeken&quot; en dat het huidige verzoek niet wordt verwerkt. De header die verschijnt nadat het opnieuw is geprobeerd, geeft aan dat u de API-aanroep in 10,752 seconden opnieuw kunt proberen. Uw code moet stoppen met het indienen van extra API-verzoeken totdat voldoende tijd is verstreken om het opnieuw te proberen.

De volgende pseudo-code laat een eenvoudige manier zien om snelheidslimietfouten af te vangen:

```
response = request.get(url) 
if response.status equals 429: 
    alert('Rate limited. Waiting to retry…') 
    wait(response.retry-after) 
    retry(url)
```

We hebben zelfs een dummy-API voor de leermanager gemaakt waarmee je kunt spelen en vertrouwd kunt raken met de 429-statuscode.

```
curl -X GET --header 'Accept: application/json' --header 'Authorization: oauth < 
<token>
  >' 'https://learningmanager.adobe.com/learningmanagerapi/v2/dummy 
</token>
```

Deze dummy-API heeft een limiet van:

```
x-rate-limit: 5r/m 
x-burst: 2
```

De limiet voor de dummy-API is opzettelijk laag, zodat u snel binnen de maximale snelheden kunt vallen en u zich vervolgens meer kunt richten op het ontwikkelen van de code voor het afvangen en afhandelen van de maximale snelheden.

## De dummy-API testen {#testingthedummyapi}

We hebben een eindpunt voor je om te zien hoe snelheidsbeperking werkt. Hiervoor hebben we een speciaal eindpunt gemaakt met de naam GET/dummy, waarvoor de student het bereik heeft gelezen. Deze API is opzettelijk geconfigureerd voor een zeer strikte tarieflimiet van 5 verzoeken per minuut, met een Burst Limiet = 2.

U kunt dit gemakkelijk testen door dit eindpunt te bereiken met tarieven onder 5 RPM en boven 5 RPM. Schrijf code voor het afhandelen van de HTTPS-statuscode van 429 op basis van de informatie in antwoordheaders.

Om het voor u gemakkelijk te maken kunt u dit voorbeeld van JavaScript-code uitchecken die dit illustreert. Klik hier [sluimeren](https://jsfiddle.net/ACAPJS/9yv8zcmL/) en bekijk de code in actie.

Deze toepassing vereist dat u een token voor de studentroltoepassing voor uw account opgeeft. Raadpleeg [Handleiding voor toepassingsontwikkelaars](https://captivateLearning Manager.adobe.com/docs/Learning) voor informatie over API-tokens en u kunt de Token Helper in de sectie met ontwikkelaarsbronnen van de toepassing Learning Manager Integration Admin gebruiken om de tokens te genereren.

Deze toepassing doet 10 aanroepen van de dummy-API in een lus, in één keer. Aangezien de snelheidsgrens (5, 2) voor de dummy API is; de tariefgrens zal worden overschreden na de eerste 5+2 vraag die door de Leermanager wordt ontvangen zal slagen en u zult een succesvolle reactie voor hen zien.

Houd er echter rekening mee dat deze toepassing op zoek is naar 429-statuscode als reactie hierop en om deze te verwerken. Wanneer deze toepassing een dergelijke reactie krijgt, worden de details in de API-reactie afgedrukt, wordt gewacht op de voorgestelde hoeveelheid tijd en worden de mislukte pogingen opnieuw uitgevoerd.

## Aanbevolen procedures voor het verwerken van tariefbeperkingen {#bestpracticestohandleratelimiting}

Vaak veranderen gegevens in een account niet zo vaak. Zo kunnen de cursussen in een account dat niet vaak veranderen. In plaats van elke keer weer alle gegevens op te halen, moet u nagaan of u de specifieke gegevens kunt ophalen wanneer u ze nodig hebt en kunt u overwegen een cachemechanisme te gebruiken. Op deze manier, wanneer uw toepassing echt veel vraag moet maken, zult u voldoende quota binnen uw tariefgrenzen hebben om die belangrijke vraag te maken.

Sommige gegevens veranderen mogelijk vaker en moeten mogelijk vaker worden verwerkt. Zelfs als dat het geval is, vraag dan uzelf of uw toepassing het zich kan veroorloven om over enigszins verouderde gegevens te beschikken (iets dat zich mogelijk in uw cache bevindt, dat u N minuten geleden hebt opgehaald), omdat dit geen invloed kan hebben op de workflow van de gebruiker. Zelfs als je nieuwe data van de servers moet ophalen, kun je weer verstandig zijn om alleen de specifieke data op te halen die je nodig hebt, in plaats van alles op te halen.

Er zullen ook tijden zijn, wanneer u geen keus hebt om veel gegevens te krijgen omdat API niet flexibel genoeg kan zijn om u precies te geven wat u met enkel één vraag wilt. Kijk of de API u filters en sorteercriteria biedt die kunnen worden gebruikt om het aantal aanroepen te minimaliseren; en u zou toch in cache moeten plaatsen overwegen omdat veel gebruikers in uw account dezelfde gegevens nodig kunnen hebben.

Wanneer u te veel gegevens ontvangt in de context van een interactieve toepassing met een GUI, is het waarschijnlijk dat de toepassing te veel probeert te doen en de gebruiker kan overspoelen met veel informatie/functionaliteit die van invloed is op de gebruikerservaring van uw toepassing.

Wanneer u een niet-interactieve toepassing ontwikkelt (bijvoorbeeld een dagelijkse taak), moet u mogelijk een groot aantal gegevens in bulk ophalen. In dergelijke gevallen kunt u de taak-API gebruiken die voornamelijk is ontworpen om bulkgegevens in CSV-indeling te retourneren. TaakAPI heeft een quotabeperking die u ze N keer per dag kunt aanroepen.

Aangezien Learning Manager de JSONAPI-specificaties heeft geïmplementeerd, is er een API waarmee u ook bepaalde gegevens kunt sideloaden. Zo bespaar je het maken van extra API-aanroepen, maar je moet dit wegwerken door te gemakkelijk data op te halen. Aangezien de sideloade gegevens soms erg groot kunnen zijn, kunt u in API-gepagineerde aanroepen de maximale paginagrootte beperken tot 10. Voor API-aanroepen zonder include-bestanden kunt u echter een grotere paginagrootte opgeven (maximaal 100)

Uiteindelijk, als u veel API verzoeken in een korte tijd maakt, zult u binnen de API tariefgrens voor verzoeken vallen. Wanneer u de limiet bereikt, stopt Leermanager met het verwerken van verzoeken totdat een bepaalde hoeveelheid tijd is verstreken.

De tarieflimieten worden beschreven in het laatste gedeelte van dit artikel. U wordt aangeraden de grenzen te kennen.

## Snelheidslimieten voor V2 API-eindpunten {#ratelimitsforv2apiendpoints}

De volgende tabel bevat de limieten voor de verschillende V2-eindpunten. Op dit moment worden de tarieflimieten niet aan klanten opgelegd, maar deze limieten zullen worden opgelegd aan DD/MM/JJJJ. Daarom wordt het belangrijk voor klanten om de code van hun bestaande toepassingen te bekijken om te zien hoe ze hun code kunnen aanpassen om zich bewust te zijn van deze tariefbeperkingen en de API-reacties te verwerken met HTTP-statuscode 429.

<table> 
 <tbody>
  <tr> 
   <td><p><b>Bewerking</b></p></td> 
   <td><p><b>Admin API</b></p></td> 
   <td><p><b>Learner-API</b></p></td> 
  </tr> 
  <tr> 
   <td><p>DELETE</p></td> 
   <td><p>(25, 10) <br></p></td> 
   <td><p>(20, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>PATCH</p></td> 
   <td><p>(60, 20)</p></td> 
   <td><p>(15, 5) <br></p></td> 
  </tr> 
  <tr> 
   <td><p>POST</p></td> 
   <td><p>(30, 10)<br></p></td> 
   <td><p>(30, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>PUT</p></td> 
   <td><p>(20, 10)<br></p></td> 
   <td><p>(20, 10)<br></p></td> 
  </tr> 
  <tr> 
   <td><p>GET</p></td> 
   <td><p>(100, 100)<br></p></td> 
   <td><p>(100, 30)<br></p></td> 
  </tr> 
 </tbody>
</table>

