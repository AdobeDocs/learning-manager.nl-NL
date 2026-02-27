---
description: De AI-assistent (bèta) voor studenten is een door GenAI gedreven chatpartner in Adobe Learning Manager die studenten helpt om snel en nauwkeurig te antwoorden op hun toegewezen leerinhoud. Met behulp van zoekopdrachten in natuurlijke talen kunnen studenten onmiddellijk gerichte antwoorden met duidelijke citaten ophalen, waardoor ze gemakkelijk de juiste informatie kunnen vinden, bronnen kunnen verifiëren en efficiënt kunnen leren zonder volledige cursussen te doorzoeken.
jcr-language: en_us
title: AI-assistent voor studenten in Adobe Learning Manager
exl-id: 8203488d-74a6-4463-9383-76d16cabccfa
source-git-commit: 922e6bed551baca8ef0e9f6b8124fb26fcce97e6
workflow-type: tm+mt
source-wordcount: '1995'
ht-degree: 0%

---

# AI-assistent voor studenten

Met de AI-assistent (bèta) voor studenten kunnen ze snel antwoorden vinden in de toegewezen leerinhoud zonder door volledige cursussen te bladeren. U kunt vragen stellen in gewone taal en u ontvangt nauwkeurige, gerichte antwoorden met bronkoppelingen naar de relevante cursusinhoud.

>[!IMPORTANT]
>
>De AI-assistent voor studenten is momenteel beschikbaar als bètafunctie. Mogelijkheden, ondersteunde scenario&#39;s en beperkingen kunnen veranderen naarmate de functie zich ontwikkelt.


## Wat is de AI-assistent voor studenten?

De AI-assistent is een door GenAI gedreven chatpartner in Adobe Learning Manager die snelle, nauwkeurige antwoorden biedt op studentvragen met behulp van de vertrouwde leerinhoud die beschikbaar is in Adobe Learning Manager. Het bevat ook citaten, zodat studenten altijd de bron van de informatie kennen.

### Belangrijkste mogelijkheden van de AI-assistent

1. Intelligente antwoorden op vragen
   * Enkelvoudige en meervoudige gesprekken
   * Natuurlijk taalbegrip in het Engels
   * Antwoorden afgeleid van cursus, certificeringen, leerpaden en taakhulpen
   * Vragen slim verduidelijken wanneer vragen dubbelzinnig zijn
   * Aangestuurd door Azure Open AI LLM-mogelijkheden om reacties te genereren
2. Inhoudsbronnen en citaten
   * Haalt antwoorden op uit beschikbare bronnen in ondersteunde catalogi.
   * Verstrekt citaten met directe verbindingen aan bronmaterialen
   * Ondersteunt alle ALM-inhoudsindelingen statisch en interactief: PDF, DOCX, PPTX, XLSX, Audio (mp3, wav, m4a), Video (mp4, mov, wmv), HTML, SCORM 2004, SCORM 1.2
3. Gebruikerservaring
   * Zijpaneelinterface toegankelijk vanaf alle studentpagina&#39;s
   * Responsief ontwerp dat zich aanpast aan het inhoudsgebied
   * Chatgeschiedenis behouden in browsersessie
   * Schoon de pagina op nieuwe aanmelding of pagina vernieuwen
   * Tint van docent of docent: vriendelijk, helder en pedagogisch verantwoord
4. Controlemiddelen voor beheerders
   * Functie op accountniveau in- of uitschakelen
   * Toegang door gebruikersgroepen beheren
   * Selecteren welke catalogi worden opgenomen voor AI-reacties
   * Voorwaarden voor acceptatie bij gebruik om te voldoen aan de Adobe AI-richtlijnen

## Welke typen inhoud wordt door de AI-assistent ondersteund

De AI-assistent haalt informatie op uit de leerinhoud die aan u is toegewezen, zoals:

* **Documenten:** PDF, Word, PowerPoint, Excel, HTML
* **Media:** Audio (mp3, wav, m4a), Video (mp4, mov, wmv)
* **SCORM 1.2, SCORM 2004**
* **het Leren objecten types:** Cursussen, het leren wegen, certificeringen, taakhulpen

Adobe transcripeert leerinhoud met behulp van vertrouwde externe verwerkingsservices die worden gehost in de particuliere VPC-omgeving van de Adobe.

### Beperkingen van catalogus- en inhoudsbronnen

De Medewerker AI van de Student gebruikt slechts inhoud van **Interne catalogi** die uitdrukkelijk door beheerders worden gevormd.

De volgende inhoudsbronnen worden **niet gesteund** in de huidige versie:

* Gedeelde catalogi
* Opgehaalde catalogi
* Externe catalogi
* Standaardcatalogi
* Bibliotheken met inhoud van derden (bijvoorbeeld LinkedIn Learning of Go1)

Als een student geen toegang heeft tot een cursus of taakhulp, wordt de informatie uit die inhoud niet weergegeven in de AI-assistent en zijn de citaatkoppelingen niet toegankelijk.

## Gebruik gevallen van AI-assistent

### Technische student

Sarah is een verkoopingenieur die leert over grafische kaarten. Ze moet snel inzicht krijgen in de technische specificaties en voordelen om de vragen van klanten met vertrouwen te beantwoorden.

De AI Assistant helpt Sarah met:

* Duidelijke, technische uitleg van complexe GPU-architectuur
* Meer inzicht in verschillende grafische kaarten en de verschillen tussen deze kaarten
* Uitleg van voorbeelden zodat Sarah functies kan relateren aan praktijkvoorbeelden

### Klantenondersteuning

Marcus is een ondersteuningsspecialist bij een partnerbedrijf. Hij heeft snelle antwoorden nodig over productfuncties om klanten te helpen zonder te escaleren naar technische teams.

De AI-assistent helpt Marcus met:

* Relevante ondersteuningscontent vinden voor veelgestelde vragen van klanten
* Vragen verduidelijken wanneer het eerste antwoord niet specifiek genoeg is
* Aanbevelingen voor gerelateerde probleemoplossingscursussen vinden om zijn vaardigheden te verbeteren

### Nieuwe onboarding van werknemers

Jennifer kwam net bij het bedrijf en wordt overweldigd door de hoeveelheid trainingsmateriaal. Ze heeft een manier nodig om specifieke informatie te vinden zonder volledige cursussen te bekijken.

De AI Assistant helpt Jennifer met:

* Stapsgewijze begeleiding krijgen bij het indienen van kostenrapporten
* Cursussen over het bedrijfsbeleid weergeven zonder door de volledige catalogus te bladeren
* Bezoek haar naar het juiste gedeelte van een cursus zonder dat ze uren video hoeft te maken

## Hoe gebruikt de AI-assistent inhoud

Met de AI-assistent vind je snel nauwkeurige antwoorden terwijl je leert. Om het effectief te gebruiken, zou u moeten begrijpen welke inhoud de medewerker gebruikt, wat het niet gebruikt, en hoe het reacties produceert.

### Inhoud van de AI-assistent

De AI-assistent beantwoordt vragen met alleen de leerinhoud die door de accountbeheerder is ingeschakeld. De inhoud van de catalogus wordt geïndexeerd.

De AI-assistent analyseert de leerinhoud die aan u is toegewezen om gerichte en contextuele reacties te genereren.

* Elke reactie bevat verwijzingen naar de oorspronkelijke broninhoud.
* U kunt een citaat selecteren om rechtstreeks naar de desbetreffende cursus, module of document te navigeren.
* Met uitnodigingen kunt u informatie verifiëren en aanvullende context verkennen wanneer dat nodig is.

### Streaming antwoorden

Een streamingreactie betekent dat de AI-assistent het antwoord progressief levert terwijl het wordt gegenereerd, zodat gebruikers direct kunnen beginnen met het lezen van de reactie zonder te wachten totdat het volledige antwoord is geladen.

### Kaarten en brontransparantie

Elke AI-hulpreactie bevat verwijzingen die rechtstreeks zijn gekoppeld aan de oorspronkelijke cursus, module of leerobject. Met behulp van uitnodigingen kunt u:

* Selecteer een inline-citatienummer om naar de exacte sectie waarnaar wordt verwezen te gaan
* Open de volledige bronlijst door Bronnen onder aan de reactie tonen te selecteren
* Verifieer informatie en verken extra context van de gebiedende bron

>[!IMPORTANT]
>
>De AI-assistent geeft antwoorden op basis van de inhoud die door de beheerder is ingeschakeld. Als een gebruiker echter geen toegang heeft tot een item waarnaar wordt verwezen, wordt bij het openen van het bericht een &quot;niet-ondersteund&quot; weergegeven.


## Ingebouwde vragen

De AI-assistent bevat ingebouwde aanwijzingen om studenten te helpen snel aan de slag te gaan met veelgestelde vragen en scenario&#39;s. Deze aanwijzingen helpen studenten bij het werken met de assistent en tonen de typen vragen die ze kunnen stellen.

![ bouwt-in-herinneringen die door de Medewerker van de Student worden verstrekt ](assets/built-in-prompt-new.png)

Ingebouwde vragen kunnen per account worden aangepast. Organisaties kunnen ze aanpassen aan hun leerdoelen, rollen van studenten, terminologie of specifieke gebruikssituaties. Beheerders kunnen met hun Customer Success Manager (CSM) samenwerken om ingebouwde vragen te configureren of bij te werken.

Aanpassing op verzoek wordt beheerd op accountniveau en kan niet rechtstreeks worden geconfigureerd in de Adobe Learning Manager-gebruikersinterface in de huidige release.

## Beheerdersinstellingen - AI-assistent voor studenten inschakelen

![ AI-Toegelaten Medewerker van de Student ](assets/learner-ai-assistant-new.png)

Beheerders selecteren welke gebruikersgroepen en interne catalogi toegang hebben tot de AI-assistent-functie. Ze moeten ervoor zorgen dat de toegewezen catalogi alleen de leerinhoud bevatten die geschikt is om door AI-reacties en -citaten te worden opgezocht, en dat die catalogi standaard, intern, niet gedeeld, verworven of extern zijn.

Voordat u de AI-assistent configureert, moet u controleren of u beheerdersreferenties hebt en hebt bepaald welke gebruikersgroepen en catalogi toegang moeten hebben tot de functie.

### Toegang tot AI-assistent configureren

AI-assistent van student inschakelen:

1. Meld u als beheerder aan bij Adobe Learning Manager.

2. Selecteer **Montages** van de homepage.
   ![ console van de Beheerder met de optie van Montages op de linkerruit ](assets/settings-menu.png)

3. Selecteer {Medewerker AI van de Leerling (Bèta) **van het** 3} menu van Montages {.
****   ![ de consolevertoningen van de Beheerder de HulpAI van de Student optie op de linkerruit ](assets/learner-assistant-ai-beta.png)

4. Selecteer de knevelschakelaar om de **Medewerker AI van de Student (Bèta) toe te laten**.
   ![ de consolevertoningen van Beheerders de knevel die voor de Medewerker AI van de Student wordt toegelaten ](assets/learner-assistant-toggle.png)

5. Selecteer één of meerdere gebruikersgroepen van de **In aanmerking komende gebruikersgroepen** optie.

6. Selecteer **sparen** om de montages van de gebruikersgroep toe te passen.

7. Selecteer één of meerdere catalogi van de **In aanmerking komende optie van Catalogi**.

8. Selecteer **sparen** om de catalogusmontages toe te passen.

>[!IMPORTANT]
>
>Alleen interne catalogi worden ondersteund door de AI-assistent. Als u een gedeelde, verworven, externe of andere niet-interne catalogus selecteert, wordt de inhoud ervan niet weergegeven door de AI-assistent, zelfs niet als de catalogus wordt weergegeven in de lijst In aanmerking komende catalogi.

## Leergids - De AI-assistent starten

### De AI-assistent starten

De AI-assistent starten:

1. Meld u als student aan bij Adobe Learning Manager.

2. Selecteer **Vraag AI Medewerker** op de homepage.
   {de vertoningen van de homepage van 0} Leerling vragen AI Medewerker om het Leerling AI Hulppaneel te selecteren en te openen ](assets/ask-ai-assistant.png)![

3. Wanneer het **scherm van de Medewerker AI van 0} Leerling verschijnt, uitgezocht** begin **.**   ![ Uitgezochte worden begonnen om de Medewerker van de Student te lanceren ](assets/get-started-learner-assistant.png)

>[!NOTE]
>
>Wanneer u de AI Assistant voor het eerst start, moet u eerst uw toestemming geven voordat u deze kunt gebruiken. Het dialoogvenster voor toestemming wordt alleen weergegeven tijdens deze eerste keer dat u de toepassing start. Voor alle volgende keren starten, wordt u rechtstreeks naar de AI-assistent geleid om uw vragen in te voeren.

&#x200B;4. Typ uw vraag in het tekstveld.
<!-- ![Type prompt in the Learner Assistant](assets/type-prompt-new.png) -->

5.Pers **ga** binnen om een reactie te ontvangen. Bekijk uw antwoord, bronnen en aanbevelingen.

U kunt:

* Selecteer het animatienummer inline om naar de exacte sectie waarnaar wordt verwezen te gaan
* Open de volledige lijst van bronnen door **te selecteren toon Bronnen** bij de bodem van de reactie

![ bronnen van de Vertoning in de reactie ](assets/show-sources-latest.png)

De AI Assistant bevat citaten met elk antwoord om te laten zien waar de informatie vandaan komt. Elke aanhaling is rechtstreeks gekoppeld aan de oorspronkelijke cursus, module of leerobject dat wordt gebruikt om het antwoord te genereren.

U kunt elke gewenste vermelding selecteren om de feitelijke cursuspagina in de Adobe Leermanager te openen en de volledige inhoud in context te bekijken. Met behulp van uitnodigingen kunt u informatie verifiëren, aanvullende details verkennen en blijven leren van de gezaghebbende bron.

## De AI-assistent openen via zoeken

U kunt de AI-assistent ook rechtstreeks vanuit de zoekbalk starten. Typ uw vraag op het onderzoeksgebied, dan uitgezocht **vraag AI Medewerker** van de opties die lijken om antwoorden van uw toegewezen het leren inhoud te krijgen.he toegewezen leerinhoud.

![ heb toegang tot de Medewerker van de Student van onderzoeksbar ](assets/learner-assistant-search-new.png)


## Feedback geven op reacties van de AI-assistent van studenten

Uw feedback over de reacties die worden gegenereerd door de Learner AI Assistant (Beta) verbetert de nauwkeurigheid, relevantie en algehele prestaties.

### Een reactie leuk vinden of niet leuk vinden

* Selecteer **Duims omhoog**, kies wat u behulpzaam in de reactie vond, voeg naar keuze commentaren toe, en selecteer dan **voorleggen**.

<!-- ![Select Thumbs Up to upvote a response](assets/la-feedback.png) -->

* Selecteer **Duimen neer**, kies de reden de reactie niet nuttig was, voeg om het even welke commentaren toe, en selecteer dan **voorleggen**.

## Een nieuwe chat starten in AI Assistant

Het beginnen van een nieuw praatje staat de gebruiker toe om met een vers gesprek te beginnen, ontruimend vroegere context zodat kan de medewerker zich op het nieuwe onderwerp concentreren zonder van verwijzingen vorige interactie te voorzien. Dit is belangrijk wanneer u van onderwerp wisselt of antwoorden zoekt die niets te maken hebben met eerdere vragen.

Wis het huidige gesprek en start op elk gewenst moment een nieuwe chat.

Selecteer **Nieuw praatje** in het AI Hulpscherm en selecteer dan **Ja**.

![ Begin een nieuw praatje in de Medewerker van de Student ](assets/start-new-chat.png)

De AI-assistent geeft studenten snelle, contextuele antwoorden, ondersteunt meerdere inhoudstypen en biedt inline citaties voor transparantie. Beheerders kunnen de toegang beheren, ervoor zorgen dat de AI-assistent is afgestemd op de organisatorische behoeften en de leerervaring verbetert.


## Problemen oplossen

>[!NOTE]
>
>Nadat u een nieuwe catalogus hebt geconfigureerd, kunt u de inhoud binnen 4 tot 5 uur indexeren en beschikbaar stellen voor AI-hulpreacties.

### Scenario 1: Geen toegang tot inhoud

Probleem: de student heeft toegang tot de Studentenassistent, maar ontvangt de antwoorden &#39;Ik heb geen antwoord op deze vraag&#39;.

**Mogelijke oorzaken**

* De catalogi van de student zijn niet inbegrepen bij het configureren van AI Assistant
* Inhoud met betrekking tot de vraag bevindt zich niet in geselecteerde catalogi of catalogi zijn leeg
* Student heeft geen zicht op relevante inhoud

**Oplossing**

* De toegang tot de catalogus van de student controleren
* Controleren welke catalogi zijn ingeschakeld in de instellingen van de Studentenassistent
* Ervoor zorgen dat er relevante inhoud in deze catalogi aanwezig is
* Enkele uren na het toevoegen van nieuwe inhoud voor indexering wachten

### Scenario 2: Onrelevante of slechte antwoorden

**Probleem**: De AI Medewerker verstrekt antwoorden die niet de vraag aanpassen of lage kwaliteit zijn.

**Mogelijke oorzaken**

* De vraag is te breed of dubbelzinnig
* Relevante inhoud heeft slechte metagegevens (beschrijvingen, tags)
* De contentstructuur maakt het moeilijk om informatie te extraheren

**Oplossing**

* Studenten aanmoedigen om specifiekere vragen te stellen
* Cursusbeschrijvingen en metagegevens bekijken en verbeteren
* Zorg ervoor dat inhoud duidelijke koppen en structuur heeft
* Bekijk het gedetailleerde gebruiksrapport om patronen te identificeren
* U kunt taakhulpen maken voor veelgestelde vragen

### Scenario 3: Vragen over onvoldoende bereik

**Probleem**: De student stelt vragen los van trainingsinhoud.

**Voorbeelden**:

* Algemene kennisvragen (&#39;Wie is de president?&#39;)
* Persoonlijke meningen (&#39;Wat denk je van X?&#39;)
* Onjuiste inhoud
