---
jcr-language: en_us
title: Gebruiksgids voor webhooks
description: Meer informatie over het gebruik van Webhooks, best practices en beperkingen
contentowner: chandrum
exl-id: e6a63ffb-7fdd-46e4-b5e6-20ce36861cef
source-git-commit: 4c04757d78d599ca30e3cd26257a967d5b9e3fdc
workflow-type: tm+mt
source-wordcount: '3369'
ht-degree: 1%

---

# Gebruiksgids voor webhooks

Webhooks zijn een manier waarop webtoepassingen automatisch en in real-time met elkaar kunnen communiceren.

In tegenstelling tot traditionele API&#39;s, die wachten tot een gebruiker informatie aanvraagt, delen real-time API&#39;s gegevens op het moment dat het gebeurt. Webhooks fungeren als een real-time API en helpen de gegevens direct te delen wanneer de opgegeven gebeurtenis plaatsvindt.

## Entiteiten

Om webhooks-gebeurtenissen te begrijpen, moeten we ons eerst bewust zijn van de entiteiten en de triggervoorwaarden voor deze gebeurtenissen.

### Leerobjecten

Hieronder volgen de ondersteunde gebeurtenissen voor leerobjecten (cursus, leerpad of certificeringen).

#### Concept

Wanneer een het leren voorwerp van UI wordt gecreeerd, begint het op **Laag** wijze. Dit betekent dat het leerobject nog niet is gepubliceerd en niet beschikbaar is voor de studenten. De **LEARNING_OBJECT_DRAFT** gebeurtenis wordt teweeggebracht zolang het het leren voorwerp een ontwerp blijft. Deze gebeurtenis wordt ook geactiveerd als het concept wordt bijgewerkt.

#### Update

Zodra het het leren voorwerp wordt gepubliceerd, verandert zijn staatsveranderingen van **Ontwerp** in **Gepubliceerd**. Tijdens deze overgang, produceert Webhook **LEARNING_OBJECT_MODIFICATION** gebeurtenis omdat het het leren voorwerp van **Ontwerp** aan **Gepubliceerd** wordt gewijzigd. Alle verdere wijzigingen en updates aan LO zullen ook a **LEARNING_OBJECT_MODIFICATION** gebeurtenis teweegbrengen.

De **LEARNING_OBJECT_MODIFICATION** gebeurtenis wordt ook teweeggebracht wanneer het het leren voorwerp wordt gearchiveerd. Deze gearchiveerde bewerking markeert de onderliggende instanties zoals bijgewerkt, aangezien deze instanties worden gearchiveerd zodra het bovenliggende leerobject zich in de gearchiveerde status bevindt.

#### Verwijderen

Op het schrappen van een het leren voorwerp, wordt de **LEARNING_OBJECT_DELETION** gebeurtenis geproduceerd. Deze gebeurtenis geeft aan dat het leerobject is verwijderd en niet langer beschikbaar is voor studenten om toegang te krijgen.

Naast gebeurtenissen in real time, hebben de het leren objecten gebeurtenissen ook een partij (niet in real time) tegenhanger, die als deel van de **LEARNING_OBJECT_MODIFICATION_BATCH** gebeurtenis wordt teweeggebracht. Deze gebeurtenis vindt plaats tijdens het maken of aanpassen van een leerobject via de migratieworkflow. Aangezien het concept- en verwijderingsbewerkingen van leerobjecten niet worden ondersteund door migratie, zijn er geen overeenkomende concept- of verwijderingsgebeurtenissen voor deze handelingen.

### Leerobjectinstanties

Hier volgen de ondersteunde gebeurtenissen voor leerobjectinstanties.

#### Update

Zodra een instantie wordt gecreeerd, wordt de **LEARNING_OBJECT_INSTANCE_MODIFICATION** gebeurtenis geproduceerd. De het leren objecten instanties in Adobe Learning Manager hebben a **Laag** staat niet; daarom steunt Adobe Learning Manager a **LEARNING_OBJECT_INSTANCE_DRAFT gebeurtenis** niet. Deze gebeurtenis wordt gegenereerd wanneer een instantie wordt gemaakt, gewijzigd of gearchiveerd.

Naast wordt geproduceerd wanneer een instantie wordt gecreeerd, bijgewerkt, of gearchiveerd, wordt deze gebeurtenis ook auto-geproduceerd wanneer zijn ouder leervoorwerp als **Gearchiveerd** wordt gemerkt. Dit is omdat wanneer een het leren voorwerp wordt gearchiveerd, de onderliggende instanties ook als **Gearchiveerd** moeten worden gemerkt.

#### Verwijderen

Wanneer een instantie wordt geschrapt, wordt de **LEARNING_OBJECT_INSTANCE_DELETION** gebeurtenis geproduceerd. Deze gebeurtenis is alleen van toepassing op cursusinstanties die modules op eigen tempo bevatten, aangezien in Adobe Learning Manager alleen beheerders cursusinstanties kunnen verwijderen waarvan het moduletype op eigen tempo is. Adobe Learning Manager ondersteunt geen expliciete verwijderingen voor andere typen cursusmodules, niet voor leerpadinstanties of certificeringsinstanties.

De het leren objecten instantie heeft ook een non-real-time tegenhanger, die als deel van de **wordt blootgesteld LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH** gebeurtenis. Deze gebeurtenis wordt geactiveerd tijdens het maken of wijzigen van een leerobjectinstantie via de migratieworkflow. Aangezien concept- of verwijderbewerkingen voor leerobjectinstanties niet worden ondersteund in migratie, zijn er geen corresponderende concept- of verwijderingsgebeurtenissen beschikbaar.

### Inschrijving

Zodra een student een inschrijvingsactie uitvoert, wordt een real-time inschrijvingsgebeurtenis geactiveerd. Afhankelijk van het type leerobject kan de gebeurtenis voor realtime inschrijving in een van de volgende categorieën vallen:

* COURSE_ENROLLMENT
* LEREN_PATH_ENROLLMENT
* CERTIFICATION_ENROLLMENT

Naast deze real-time gebeurtenissen hebben inschrijvingsgebeurtenissen ook batchalternatieven. Wanneer een inschrijving wordt geactiveerd door een beheerder, manager of platform, worden niet-real-time inschrijvingsgebeurtenissen geactiveerd. Op basis van het leerobjecttype kan de blokinschrijvingsgebeurtenis een van de volgende zijn:

* COURSE_ENROLLMENT_BATCH
* LEREN_PATH_ENROLLMENT_BATCH
* CERTIFICATION_ENROLLMENT_BATCH

### Uitschrijving

Wanneer een student een uitschrijvingsactie uitvoert, wordt er een real-time uitschrijvingsgebeurtenis geactiveerd. Afhankelijk van het type leerobject kan de gebeurtenis voor real-time uitschrijven in een van de volgende categorieën vallen:

* CURSE_UNENROLLMENT
* LEARNING_PATH_UNENROLLMENT
* CERTIFICATION_UNENROLLMENT

Naast deze gebeurtenissen zijn er ook batch-uitschrijvingsgebeurtenissen. Wanneer een uitschrijving wordt gemarkeerd door een beheerder, manager of platform, worden niet-real-time uitschrijvingsgebeurtenissen geactiveerd. Op basis van het type leerobject kan de gebeurtenis voor het uitschrijven van batch een van de volgende zijn:

* CURSE_UNENROLLMENT_BATCH
* LEREN_PATH_UNENROLLMENT_BATCH
* CERTIFICATION_UNENROLLMENT_BATCH

### Voltooiing

De gebeurtenis &#39;realtime voltooiing&#39; wordt geactiveerd wanneer een student een leerobject voltooit. Op basis van het type leerobject kan de gebeurtenis realtime voltooiing in een van de volgende categorieën vallen:

* CURSE_COMPLETED
* LEREN_PATH_COMPLETED
* CERTIFICATION_COMPLETED

Naast deze real-time gebeurtenissen zijn er ook batch-voltooiingsgebeurtenissen. Wanneer een beheerder, manager of platform een leerobject als voltooid markeert, worden de niet-realtime voltooiingsgebeurtenissen geactiveerd. Op basis van het leerobjecttype kan de gebeurtenis voor batchvoltooiing in een van de volgende categorieën vallen:

* CURSE_COMPLETED_BATCH
* LEREN_PATH_COMPLETED_BATCH
* CERTIFICATION_COMPLETED_BATCH

### Voortgang student

Wanneer een student zich inschrijft voor een leerobject en de module start, wordt de voortgang bijgehouden. Dit gegeven is inbegrepen in de **LEARNER_PROGRESS** gebeurtenis. De gebeurtenis kan met maximaal 15 minuten worden vertraagd, omdat het volgen van de voortgang afhankelijk is van complexe aggregatielogica, wat geen real-time is.

### CI-statussen

**CI_STATS** gebeurtenis in real time wordt teweeggebracht wanneer er een verandering in plaats of wachtlijstbeschikbaarheid voor een cursusinstantie is. Deze gegevens worden alleen op instantieniveau vastgelegd. Bovendien wordt deze gebeurtenis geactiveerd voor cursussen en niet voor andere leerpaden of certificeringen, aangezien de beschikbaarheid van licenties en wachtlijsten kenmerken zijn die specifiek zijn voor een cursus en de instantie ervan.

## Volgorde van gebeurtenissen

Adobe Learning Manager zorgt ervoor dat gebeurtenissen voor elk account worden geordend. Er kunnen echter discrepanties optreden bij het correleren van berichten tussen inschrijving of voltooiing en voortgangsgebeurtenissen. Dit gebeurt omdat de gebeurtenis progress van de student maximaal 15 minuten kan worden vertraagd, omdat het volgen van de voortgang afhankelijk is van complexe aggregatielogica, wat geen real-time is. Bovendien komen voortgangsgebeurtenissen uit verschillende gegevensbronnen, zodat hun volgorde niet kan worden gegarandeerd met betrekking tot inschrijvings- en voltooiingsgebeurtenissen. Daarom biedt Adobe Learning Manager aanbevolen procedures voor clients wanneer u naar deze gebeurtenissen luistert.

Als de voltooiingsgebeurtenis plaatsvindt vóór de gebeurtenis &#39;progress&#39; van de student, kan de client de gebeurtenis &#39;progress&#39; van de student negeren. De reden hiervoor is dat de gebeurtenis progress van de student maximaal 15 minuten kan worden vertraagd, terwijl de gebeurtenis complete mogelijk wordt geactiveerd voordat de gebeurtenis progress wordt ontvangen. Aangezien het ontvangen van een voltooiingsgebeurtenis aangeeft dat het leerobject is voltooid, betekent dit dat de voortgang 100% is.

In het zeldzame geval dat de inschrijvingsgebeurtenis na de gebeurtenis progress van de student komt, kan de client de inschrijvingsgebeurtenis negeren. Dit komt doordat de voortgang pas kan worden bijgehouden nadat de student zich heeft ingeschreven voor het leerobject. Met andere woorden, het ontvangen van een gebeurtenis progress geeft aan dat het leerobject is gestart, wat alleen gebeurt na een geslaagde inschrijving.

## Realtime gebeurtenissen versus batchgebeurtenissen

Sommige gebeurtenissen hebben real-time en niet-real-time tegenhangers, zoals hierboven vermeld. Er kunnen vragen zijn over wanneer u zich moet abonneren op realtime gebeurtenissen en wanneer u zich moet abonneren op niet-real-time gebeurtenissen. Hieronder volgen enkele richtlijnen die kunnen worden gevolgd op basis van de hierboven beschreven entiteiten.

### Real-time gebeurtenissen

| S.No | Webhook-gebeurtenissen | Beschrijving |
|---|---|---|
| 1 | CI_STATS | Wordt geactiveerd wanneer de beschikbaarheid van de licentie of wachtlijst voor een cursusinstantie wordt gewijzigd. |
| 2 | COURSE_ENROLLMENT | Wordt geactiveerd wanneer een student zich voor een cursus inschrijft. |
| 3 | CURSE_COMPLETED | Wordt geactiveerd wanneer een student een cursus heeft voltooid. |
| 4 | LEREN_PATH_ENROLLMENT | Wordt geactiveerd wanneer een student zich inschrijft voor een leerpad. |
| 5 | LEREN_PATH_COMPLETED | Wordt geactiveerd wanneer een student een leerpad heeft voltooid. |
| 6 | CERTIFICATION_ENROLLMENT | Wordt geactiveerd wanneer een student zich inschrijft voor een certificering. |
| 7 | CERTIFICATION_COMPLETED | Wordt geactiveerd wanneer een student een certificering heeft voltooid. |
| 8 | CURSE_UNENROLLMENT | Wordt geactiveerd wanneer een student zich uitschrijft voor een cursus. |
| 9 | LEARNING_PATH_UNENROLLMENT | Wordt geactiveerd wanneer een student zich uitschrijft vanuit een leerpad. |
| 10 | CERTIFICATION_UNENROLLMENT | Wordt geactiveerd wanneer een student zich uitschrijft voor een certificering. |
| 11 | LEARNING_OBJECT_DRAFT | Wordt geactiveerd tijdens het maken van een leerobject in conceptstatus. |
| 12 | LEARNING_OBJECT_DELETION | Wordt geactiveerd tijdens het verwijderen van een leerobject. |
| 13 | LEREN_OBJECT_MODIFICATION | Wordt geactiveerd tijdens de wijziging van een leerobject. |
| 14 | LEARNING_OBJECT_INSTANCE_MODIFICATION | Wordt geactiveerd tijdens het maken of wijzigen van een leerobjectinstantie.<div><b> Nota:</b> het wordt geadviseerd om cursusinstanties slechts te gebruiken nadat de cursus wordt gepubliceerd.</div> |
| 15 | LEARNING_OBJECT_INSTANCE_DELETION | Wordt geactiveerd tijdens het verwijderen van een leerobjectinstantie. |

### Niet-realtime gebeurtenissen

| S.No | Webhook-gebeurtenissen | Beschrijving |
|---|---|---|
| 1 | COURSE_ENROLLMENT_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform studenten voor een cursus inschrijft. |
| 2 | CURSE_COMPLETED_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform een cursus als voltooid markeert. |
| 3 | LEREN_PATH_ENROLLMENT_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform studenten inschrijft in een leerpad. |
| 4 | LEREN_PATH_COMPLETED_BATCH | Wordt geactiveerd wanneer een beheerder/manager een leerpad als voltooid markeert. |
| 5 | CERTIFICATION_ENROLLMENT_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform studenten voor een certificering inschrijft. |
| 6 | CERTIFICATION_COMPLETED_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform een certificering als voltooid markeert. |
| 7 | LEARNER_PROGRESS | Traceert de voortgang van een student wanneer een module is voltooid. |
| 8 | CURSE_UNENROLLMENT_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform studenten van een cursus uitschrijft. |
| 9 | LEREN_PATH_UNENROLLMENT_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform studenten uitschrijft van een leerpad. |
| 10 | CERTIFICATION_UNENROLLMENT_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform studenten van een certificering uitschrijft. |
| 11 | LEREN_OBJECT_MODIFICATION_BATCH | Wordt geactiveerd tijdens de wijziging van een leerobject via de migratieworkflow. |
| 12 | LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH | Wordt geactiveerd tijdens het maken of wijzigen van een leerobjectinstantie via de migratieworkflow. |

### Leerobjecten en de bijbehorende instanties

* Abonneer u op real-time gebeurtenissen wanneer u wilt luisteren naar wijzigingen in leerobjecten die via UI-handelingen zijn aangebracht door rollen zoals beheerder, auteur, enz.
* Abonneer u op niet-real-time of batchgebeurtenissen wanneer u wilt luisteren naar wijzigingen in leerobjecten die zijn aangebracht via migratieworkflows.

### Inschrijving, uitschrijving en voltooiing

* Abonneer u op real-time gebeurtenissen wanneer u wilt luisteren naar inschrijvingen, uitschrijvingen of voltooide taken die door studenten worden uitgevoerd.
* Abonneer u op niet-real-time of batchgebeurtenissen wanneer u wilt luisteren naar inschrijvingen, uitschrijvingen of voltooide bewerkingen gemarkeerd door beheerder, manager, platform, enz.

### Voortgang student

* Meld u aan bij de gebeurtenis wanneer u wilt luisteren naar de voortgangswijzigingen van een student.

>[!NOTE]
>
>In de bovenstaande scenario&#39;s (inschrijving, uitschrijving, voltooiing en voortgang) kunnen de kenmerksamenstellingen bestaande uit userId en loInstanceId een record op unieke wijze identificeren.

### Status van cursusinstantie

* Abonneer aan de gebeurtenis in real time **CI_STATS** wanneer u op veranderingen in plaats of wachtlijstbeschikbaarheid wilt luisteren.

## Webhook-gebeurtenislading

Als onderdeel van de Webhooks-responslading zal Adobe Learning Manager de kenmerken verzenden die vereist zijn om een entiteit op unieke wijze te identificeren. Deze worden in dezelfde indeling en volgens de normen die worden gebruikt door de openbare API, zodat de webhookgegevens synchroon zijn met de openbare API-gegevens. Bekijk [&#x200B; lading van de Steekproef &#x200B;](/help/migrated/integration-admin/feature-summary/webhooks-usage-guide.md#sample-payloads-for-the-events) voor zie nuttige ladingen voor de diverse gebeurtenissen.

## Webhooks gebruiken om een externe DB- of meldingsservice te maken

Een van de gebruiksscenario&#39;s die we hebben gehoord en waar Webhooks nuttig kunnen zijn, is het samenstellen van een database aan de kant van de klant. Adobe Learning Manager heeft een eigen database en schema, maar klanten hebben er geen toegang toe.

De vraag is: hoe kunnen klanten een database bouwen met behulp van gebeurtenissen van webhooks?

Aangezien Adobe Learning Manager de tabelrecords en het schema niet direct beschikbaar maakt, kunnen klanten op de Webhooks-oplossing vertrouwen om een externe database te bouwen door de gebeurtenissen te gebruiken om deze te vullen. In deze release bieden we gebeurtenissen voor leerobjecten, leerobjectinstanties, inschrijving, uitschrijving, voltooiing, voortgang en status van cursusinstanties.

### Een database samenstellen op basis van leerobjectgebeurtenissen

De leerobjectgebeurtenissen stellen `loId` en `loType` beschikbaar om een entiteit te identificeren. Deze kenmerken alleen zijn echter niet voldoende om een externe database voor leerobjecten samen te stellen. Klanten hebben extra velden nodig om het leerobject verder te beschrijven.
Er zijn twee manieren om de aanvullende gegevens op te halen:

#### Een rapport met trainingsgegevens genereren om alle gegevens op te halen

Deze benadering moet worden gebruikt wanneer leerobjecten in bulk worden gemaakt via workflows zoals migratie. Het doel is hier het **[!UICONTROL rapport van de Gegevens van de Opleiding]** met alle het leren voorwerpen te produceren die als deel van het migratiewerkschema worden opgenomen. U kunt het importproces optimaliseren door de begintijd voor het exporteren in te stellen op het tijdstip waarop de migratie werd geactiveerd. Dit zorgt ervoor dat alleen de leerobjecten die via migratie worden ingevoerd, in het rapport worden geëxporteerd, aangezien historische gegevens al beschikbaar zijn in de database van de klant.

#### Vraag de informatie op van de openbare API-GET/learningObjects - beheerbereik

Deze benadering moet worden gebruikt wanneer leerobjecten worden gemaakt via realtime workflows. De klant moet een eigen cachelaag hebben om de leerobjecten die via de gebeurtenissen worden verzonden in een batch te plaatsen en vervolgens de `GET /learningObjects` -API opvragen door deze leerobject-id&#39;s door te geven. De reden voor het hebben van een caching laag is ervoor te zorgen dat de openbare API tariefgrenzen niet worden overschreden. Momenteel hebben we beheerdersbeperkingen ingesteld op 500 verzoeken per uur voor ` GET /learningObject` API&#39;s. Als deze grens wordt overschreden, zal de openbare API dienst met een **HTTP 429 Te Vele bericht van Verzoeken** antwoorden.

### Database samenstellen op basis van leerobjectinstantie en CI_STATS-gebeurtenissen

De leerobjectinstantie verzendt de kenmerken `loInstanceId` , `loId` en `loType` voor cursussen en leerpaden. Op dezelfde manier is de **CI_STATS** gebeurtenis van toepassing slechts op cursussen aangezien `seatLimit`, `seatAvailability`, `waitListLimit`, `waitlistAvailability`, etc., slechts op cursussen van toepassing zijn.

In bepaalde gebruiksgevallen zijn aanvullende instantienaam, status enz. vereist. Voor het ophalen van aanvullende instantiedata moet de volgende aanpak worden gevolgd:

#### Vraag informatie op van public-api GET/learningobjects - beheerbereik

Klanten kunnen de `GET /learningObjects` API gebruiken zoals hierboven vermeld, samen met instanties die zijn opgenomen om informatie over instanties op te halen. Zij zouden nog de benadering moeten volgen die in de [&#x200B; sectie &#x200B;](/help/migrated/integration-admin/feature-summary/webhooks-usage-guide.md#query-the-information-from-the-public-api-get-learningobjects-admin-scope) wordt vermeld om ervoor te zorgen dat de tariefgrenzen niet worden geschonden.


>[!NOTE]
>
>1. Certificeringen hebben niet het concept van instanties in ALM.
>2. Er is geen behoefte om extra gegevens voor CI_STATS op te halen aangezien de zelfde informatie reeds als deel van de het leren gebeurtenissen van de Instantie van de objecten zou zijn opgehaald.

### Database samenstellen op basis van gebeurtenissen voor inschrijving, uitschrijving, voltooiing en voortgang

Inschrijving, uitschrijving, voltooiing en voortgang van studenten worden als afzonderlijke gebeurtenissen uitgezonden in Adobe Learning Manager. De student wordt geïdentificeerd door het kenmerk `userId` . Er kunnen echter bepaalde scenario&#39;s zijn waarin aanvullende studentinformatie, zoals Naam, E-mail, enz., vereist is voor stroomafwaartse workflows aan de kant van de klant. Om deze data op te halen, kunnen klanten de onderstaande benadering volgen:

#### Het gebruikersrapport exporteren van de beheerder of connectoren

Deze aanpak moet worden gevolgd wanneer het gaat om bulkworkflows, zoals bulkinschrijving, bulkuitschrijving, enz. Het gebruikersrapport van Adobe Learning Manager bevat alle informatie over een gebruiker. Door de `userId` van de webhook-gebeurtenis te corrigeren, kunnen klanten dit rapport opzoeken (dat aan de kant van de klant als database-, cache- of API-eindpunt kan worden weergegeven) om aanvullende gegevens op te halen, zoals Naam, E-mail, UUID, enz. Deze benadering kan worden gebruikt om gebruikers wekelijks of dagelijks te synchroniseren.

#### Query-informatie van openbare API-GET /gebruikers - beheerbereik

Deze benadering kan worden gevolgd wanneer de gebruikers niet beschikbaar zijn in het bovenstaande rapport. De combinatie benaderingen 1 en 2 zorgt ervoor dat alle bestaande gebruikers die in het verleden werden gecreeerd door het **[!UICONTROL Rapport van de Gebruiker]** kunnen worden behandeld, terwijl de pas gecreëerde gebruikers nog van API kunnen worden opgehaald. Als het **[!UICONTROL Rapport van de Gebruiker]** niet de gegevens heeft, kan de klant userIds als inputargumenten naar `GET /users` API verzenden om gebruikersinformatie te halen. Deze informatie moet aan de kant van de klant in de cache worden geplaatst om te voorkomen dat de openbare API voor dezelfde groep gebruikers herhaaldelijk wordt aangeroepen. Voor de Admin-tarieven voor GET-/gebruikers-API&#39;s gelden momenteel beperkingen van 500 aanvragen per uur. Om het even welke verzoeken voorbij deze grens zullen in een **HTTP 429 Te Vele reactie van Verzoeken** resulteren.

## Fouttolerantie

De fout-verdraagzaamheid van het ALM webhooksysteem verstrekt aanbevelingen voor abonnees om potentiële kwesties, zoals gebeurtenisverlies, dubbele gebeurtenissen, en uit-van-orde levering te behandelen.

Voor ALM is een time-out voor de verbinding ingesteld op 10 seconden en een time-out voor de socket ingesteld op 5 seconden. De verwachting is dat de client het bericht erkent zodra het het ontvangt. Dit moet ervoor zorgen dat de client niet vertraagt tijdens het verwerken van berichten. Als er enige downstream-verwerking is die tijdrovend is, moet de klant de gebeurtenis nog steeds onmiddellijk erkennen en de downstream-verwerking aan het einde afhandelen.

### Bewaring van gegevens

Gebeurtenissen worden 7 dagen bewaard. Als ze niet binnen deze tijd worden verwerkt, gaan ze definitief verloren. Als de terugwinning op de laatste dag gebeurt en meer tijd nodig is, zal het systeem niet de retentieperiode verlengen.
Als gebeurtenissen sneller worden geproduceerd dan ze worden gebruikt, kunnen sommige gebeurtenissen verloren gaan. Hoewel dit niet gebruikelijk is, moeten abonnees erop toezien dat dit geen langetermijnprobleem wordt.

### Webhooks uitschakelen

Wanneer een abonnee niet reageert op webhookgebeurtenissen, probeert het ALM-systeem de webhooks opnieuw met exponentiële back-up om te voorkomen dat de abonnee overweldigt.

Het proces voor opnieuw proberen begint met een eerste interval van 5 seconden. Als de abonnee niet antwoordt, verdubbelt de wachttijd aan 10, 20, 40, en 80 seconden, uiteindelijk stijgend tot een maximum van 5 minuten. Zodra het 5 minuten bereikt, zal het systeem elke 5 minuten opnieuw proberen tot de retentieperiode van 7 dagen voorbij is. Als de abonnee nog steeds niet reageert tijdens deze hele periode, wordt de webhook automatisch uitgeschakeld. Er wordt regelmatig een herinnerings-e-mail naar de abonnee verzonden.

### Gebeurtenissen dupliceren

Als een abonnee na het verwerken van een gebeurtenis meer dan 5 seconden nodig heeft om te reageren, probeert het systeem dezelfde gebeurtenis mogelijk opnieuw te verwerken. Het wordt aanbevolen om gebeurtenis-id&#39;s te gebruiken om bij te houden welke gebeurtenissen al zijn verwerkt. Ook als de webhook vastloopt na het verzenden van de gebeurtenis, maar voordat het opslaan is voltooid, kan dezelfde groep gebeurtenissen opnieuw worden geprobeerd. Het wordt aanbevolen batch-id&#39;s of afzonderlijke gebeurtenis-id&#39;s te gebruiken om eventuele duplicaten te herkennen en te negeren.

### Aanbeveling voor fouttolerantie

Om deze fouten te voorkomen, moeten abonnees webhookgebeurtenissen actief controleren en waarschuwingen instellen voor problemen zoals gemiste gebeurtenissen, dubbele leveringen of reeksen die niet op volgorde staan.

## Specifieke richtlijnen voor webhookgebeurtenissen

1. Als u eerst een LEARNER_PROGRESS-gebeurtenis krijgt, negeert u de onderstaande gebeurtenissen:

   * COURSE_ENROLLMENT
   * COURSE_ENROLLMENT_BATCH
   * LEREN_PATH_ENROLLMENT
   * LEREN_PATH_ENROLLMENT_BATCH
   * CERTIFICATION_ENROLLMENT
   * CERTIFICATION_ENROLLMENT_BATCH

2. Negeer de gebeurtenis LEARNER_PROGRESS als deze na de volgende gebeurtenissen komt:

   * CURSE_COMPLETED
   * CURSE_COMPLETED_BATCH
   * LEREN_PATH_COMPLETED
   * LEREN_PATH_COMPLETED_BATCH
   * CERTIFICATION_COMPLETED
   * CERTIFICATION_COMPLETED_BATCH

3. Gebruik het tijdstempelveld om te bepalen of de gebeurtenis moet worden genegeerd of verwerkt, behalve voor de gebeurtenis LEARNER_PROGRESS.

## Webhooks Events gebruiken best practices

* De webhook-oplossing wordt gebruikt voor systemen met een hoge doorvoer waarbij snelheid en lage latentie essentieel zijn. Daarom moet de klant ervoor zorgen dat de gebeurtenis wordt bevestigd zodra deze is ontvangen. Zelfs als er extra verwerkingstijd aan de kant van de klant nodig is (zoals het ophalen van gegevens uit rapporten, API&#39;s of het uitvoeren van andere handelingen), moet de bevestiging worden verzonden zodra de gebeurtenis is ontvangen en moet de client de gebeurtenis later verwerken.
* Als u de gebeurtenis niet zo snel mogelijk bevestigt, kan dit gevolgen hebben voor het realtime karakter van de gebeurtenissen, aangezien volgende gebeurtenissen pas worden uitgezonden nadat de vorige bevestiging is ontvangen.
* Clients kunnen reageren met een HTTP 202 Accepted-statuscode om te bevestigen dat de gebeurtenis is geaccepteerd.

## Beperkingen

* Taakhulpen worden niet overwogen voor webhookgebeurtenissen in de categorie LO&#39;s omdat ze doorgaans worden gebruikt om studenten te helpen andere leerobjecten te voltooien.
* Uittreding van een leerobjectinstantie wordt beschouwd als een update-gebeurtenis. Er is geen verwijderingsgebeurtenis voor een instantie omdat deze alleen gearchiveerd en niet verwijderd kan worden.
* Sessiewijzigingen worden vastgelegd als onderdeel van de gebeurtenis voor het bijwerken van de instantie. Dit geldt alleen voor cursussen. Er zal geen opwaartse propagatie van lagere-niveauentiteiten voor de instanties van de leerweg of certificatieinstanties zijn.
* Als een het leren weg een cursus bevat en een student de cursus via de het leren weg voltooit, zullen twee **LearnerProgress** gebeurtenissen worden geproduceerd-voor de cursus en voor de het leren weg.
* Bepaalde workflows berekenen asynchroon kenmerken van leerobjecten, zoals duur en leveringstype. Daarom worden gebeurtenissen voor dit leerobject gegenereerd zodra de uitsnijdtaak is voltooid met de verwerking.
* Als een cursus is ingeschreven via een bovenliggend leerprogramma of certificering, worden de gebeurtenissen voor inschrijving, uitschrijving en voltooiing alleen geactiveerd voor het bovenliggende leerprogramma of de bovenliggende certificering. Deze gebeurtenissen worden niet geactiveerd voor de onderliggende cursus sinds de inschrijving indirect plaatsvindt.
* Webhooks worden slechts gesteund voor rekeningen met **[!UICONTROL ACTIEVE]** status. Zij zijn niet beschikbaar voor **[!UICONTROL PROEF]** of **[!UICONTROL INACTIEVE]** rekeningen.

## Voorbeelden van ladingen voor de gebeurtenissen

+++CI_STATS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345-0458-4450-b5dd-6bc1ef4f8b50",
      "eventName": "CI_STATS",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123456785-LoSt",
      "data": {
        "loInstanceId": "course:12345678_14448475",
        "waitlistCount": 0,
        "enrollmentCount": 10,
        "seatLimit": 30
      }
    }
  ]
}
```

+++

+++COURSE_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345c1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123424713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++COURSE_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234ec1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123424713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++COURSE_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c2345c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "12345823000-040363-12018-0",
      "data": {
        "userId": 11080928,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14448484",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
  ]
}
```

+++

+++COURSE_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c23458c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123456823000-040363-12018-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14448484",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
    ]
}
```

+++

+++LEARNING_PATH_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234791-338f-4c4c-83bc-9f73ea794965",
      "eventName": "LEARNING_PATH_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:1234567",
        "loInstanceId": "learningProgram:1234567_109139",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12340791-338f-4c4c-83bc-9f73ea794965",
      "eventName": "LEARNING_PATH_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:1234557",
        "loInstanceId": "learningProgram:1234557_109139",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123404e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234604391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:92348",
        "loInstanceId": "learningProgram:92348_95662",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12344e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123404391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:92348",
        "loInstanceId": "learningProgram:92348_95662",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z",
        "hasPassed": true
      }
    } 
    ]
    }
```

+++

+++CERTIFICATION_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234e776-148e-4128-80e9-b896a460b655",
      "eventName": "CERTIFICATION_ENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "12344672000-040654-559128-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:123418",
        "loInstanceId": "certification:123418_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
}
```

+++

+++CERTIFICATION_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123472ec1-4576-4ec5-a057-3a6f078cc9d6",
      "eventName": "CERTIFICATION_ENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234524713000-040366-10488-0",
      "data": {
        "userId": 12345678,
        "loId": "course:123456798",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123454768000-040654-756257-0",
      "data": {
        "userId": 123456728,
        "loId": "certification:123418",
        "loInstanceId": "certification:134518_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "123453bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234604768000-040654-756257-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:123418",
        "loInstanceId": "certification:123418_160299",
        "loType": "certification",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": "2024-11-08T03:49:52.000Z"
      }
    }
  ]
  }
```

+++

+++LEARNER_PROGRESS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "d1234d3a4-c3df-44fa-a1cf-7edd6e3d2075",
      "eventName": "LEARNER_PROGRESS",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235604551000-297002-5823-0",
      "data": {
        "loId": "course:7542090",
        "loType": "course",
        "userId": 12380928,
        "loInstanceId": "course:7232090_10423047",
        "dateStarted": "2024-11-08T03:49:52.000Z",
        "progressPercent": 50
      }
}
]
}
```

+++

+++COURSE_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f3237817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1345506253000-040298-24078-0",
      "data": {
        "userId": 12311591,
        "loId": "course:12324298",
        "loInstanceId": "course:12324298_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
      }
    }
  ]
}
```

+++

+++COURSE_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f2317817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "17235506253000-040298-24078-0",
      "data": {
        "userId": 12311591,
        "loId": "course:12324298",
        "loInstanceId": "course:12324298_14450088",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL"
    }
   }
  ]
}
```

+++

+++LEARNING_PATH_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "823df878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235506667000-040299-28209-0",
      "data": {
        "userId": 12311591,
        "loId": "learning_program:123157",
        "loInstanceId": "learning_program:123157_109139",
        "loType": "learning_program",
        "enrollmentSource": "SELF_ENROLL",
      }
    }
]
}
```

+++

+++LEARNING_PATH_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8e23f878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235506667000-040299-28209-0",
      "data": {
        "userId": 12311591,
        "loId": "learning_program:123157",
        "loInstanceId": "learning_program:123157_109139",
        "loType": "learning_program",
        "enrollmentSource": "ADMIN_ENROLL"
      }
    }
]
}
```

+++

+++CERTIFICATION_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7232766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235507900000-040304-1065-0",
      "data": {
        "userId": 12311591,
        "loId": "certification:123199",
        "loInstanceId": "certification:123199_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++CERTIFICATION_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7202766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1735507900000-040304-1065-0",
      "data": {
        "userId": 12511591,
        "loId": "certification:139199",
        "loInstanceId": "certification:139199_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DRAFT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12345da9f-26ec-453c-b56a-cdf18a841948",
      "eventName": "LEARNING_OBJECT_DRAFT",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1234519188000-040344-48604-0",
      "data": {
        "loId": "course:1234091",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234a690-5517-4c09-9cde-d953cdd8582c",
      "eventName": "LEARNING_OBJECT_DELETION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235605296000-040656-662792-0",
      "data": {
        "loId": "course:12319716",
        "loType": "course"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION

```
{
  "accountId": 8308,
  "events": [
    {
      "eventId": "223e068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123350842000-039736-54153-0",
      "data": {
        "loId": "learningProgram:123836",
        "loType": "learningProgram"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION_BATCH

```
{
  "accountId": 8308,
  "events": [
    {
      "eventId": "1234e068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235350842000-039736-54153-0",
      "data": {
        "loId": "learningProgram:123836",
        "loType": "learningProgram"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "121da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235603297000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12324298_14453691",
        "loId": "course:12324298",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1231da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "123603297000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12324298_14453691",
        "loId": "course:12324298",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "12d16e90-d73a-457b-83f3-666ba9654edb",
      "eventName": "LEARNING_OBJECT_INSTANCE_DELETION",
      "timestamp": "2024-11-08T03:49:52.000Z",
      "eventInfo": "1235605491000-040657-236307-0",
      "data": {
        "loInstanceId": "course:12319674_14453849",
        "loId": "course:12319674",
        "loType": "course"
      }
    }
  ]
}
```

+++
