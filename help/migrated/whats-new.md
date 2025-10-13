---
description: Meer informatie over de nieuwe functies en verbeteringen in de oktober 2025-versie van Adobe Learning Manager
jcr-language: en_us
title: Nieuwe functies in de Adobe Learning Manager-versie van oktober 2025
source-git-commit: c1a201e97a8944dddb6361aade0017f5745f933c
workflow-type: tm+mt
source-wordcount: '5638'
ht-degree: 0%

---


# Nieuwe functies in de Adobe Learning Manager-versie van oktober 2025

De Adobe Learning Manager-versie van oktober 2025 introduceert aanzienlijke verbeteringen die zijn ontworpen om de rapportnauwkeurigheid te verbeteren, de integratiemogelijkheden uit te breiden en de leerervaring voor beheerders, auteurs en studenten te verbeteren.

* Experience Builder: ontwerp volledig merkgebonden, op rollen gebaseerde leerportalen die zijn afgestemd op de behoeften van je organisatie. Creëer branded, rolgebaseerde leerportalen met widgets, menu&#39;s en pagina&#39;s.
* Sociaal labelen op leerboards: studenten kunnen nu peers taggen met @username in berichten en opmerkingen, waardoor gerichte samenwerking en meldingen binnen social-learninggemeenschappen mogelijk zijn.
* Machtigingen voor uitgebreide aankondigingen: Aangepaste beheerders kunnen aankondigingen maken die beperkt zijn tot hun toegewezen gebruikersgroepen of catalogi, zodat gerichte communicatie wordt gewaarborgd en de overbelasting van informatie wordt verminderd.
* Op taal gebaseerde voortgangstracering: de voortgang van studenten wordt nu onafhankelijk voor elke landinstelling opgeslagen, zodat u naadloos tussen talen kunt schakelen zonder dat de voortgang verloren gaat.
* Incrementeel aangepast rolbeheer: beheerders kunnen aangepaste rollen nu efficiënter beheren met ondersteuning voor incrementele en meervoudige importbewerkingen in Adobe Learning Manager.
* Verbeterde API’s voor analytics en migratie: nieuwe en verbeterde API’s bieden betere ‘quizprestaties tracking’, monitoring van migratiestatus en ondersteuning voor gebruikerstagging in Sociaal leren.

## Experience Builder

>[!IMPORTANT]
>
>We kondigen met enthousiasme aan dat Experience Builder, de innovatieve tool voor het creëren van aanpasbare leerportalen, beschikbaar zal zijn na de oktober 2025-versie van Adobe Learning Manager.
>
>Blijf op de hoogte voor meer updates vanaf de releasedatum. We kijken ernaar uit hoe je Experience Builder gebruikt om je leerportalen te transformeren.
>
>Neem voor alle vragen of aanvullende informatie contact op met uw Customer Success-manager.

Experience Builder is een niet-code-/low-code-tool in Adobe Learning Manager waarmee je aangepaste leerportalen kunt maken. Zo ontwerp je merkvriendelijke, gebruikersvriendelijke leerportalen zonder dat je technische vaardigheden of uitgebreide codeerkennis nodig hebt.
Met Experience Builder kunnen beheerders eenvoudig pagina&#39;s, menu&#39;s en widgets maken om gepersonaliseerde leerervaringen te bieden die zijn afgestemd op hun doelgroep.

Vóór Experience Builder stonden organisaties voor verschillende uitdagingen:

1. **Beperkte aanpassing**: De havens hadden vaste ontwerpen met weinig opties om op uw merk te wijzen. Beheerders kunnen alleen basiswijzigingen aanbrengen, zoals het wijzigen van kop- en voetteksten of kleuren, waardoor ze minder mogelijkheden hebben om unieke ervaringen te creëren.
2. **Kosten**: De bouw van douaneportalen vereiste dure ontwikkelaars en lange chronologie, vaak het vergen van 6 tot 9 maanden om te voltooien. Deze aanpak verhoogde de totale eigendomskosten en vertraagde implementatie.
3. **Algemene ervaringen**: Iedereen zag de zelfde inhoud, zelfs als het niet relevant voor hun rol of behoeften was. Dit gebrek aan personalisatie verminderde de betrokkenheid en tevredenheid van studenten.
4. **Technische barrières**: De niet-technische Beheerders worstelden om portals te creëren of bij te werken omdat zij coderingskennis of externe steun nodig hadden.

Experience Builder lost deze problemen op door een eenvoudige, no-code/low-code-oplossing te bieden voor het creëren van gepersonaliseerde merkportals.

Beheerders kunnen portalen ontwerpen die voldoen aan de behoeften van hun organisatie zonder te hoeven vertrouwen op technische expertise of externe ontwikkelaars.

**gevallen van het Gebruik**

* **Branded portals**: Creeer een portaal die de website van uw bedrijf met logo&#39;s, kleuren, en lay-outs aanpast. Een zorgbedrijf kan bijvoorbeeld een portal ontwerpen die de bedrijfsmerken weerspiegelt terwijl leerinhoud wordt geleverd.
* **op rol-gebaseerd leren**: Bouw pagina&#39;s die aan specifieke rollen worden aangepast. Verkoopteams kunnen producttraining bekijken, terwijl engineers toegang krijgen tot technische cursussen.
* **opleiding van het Product**: Opstelling specifieke pagina&#39;s voor verschillende producten, zoals Photoshop of Illustrator, met widgets die Cursussen, Certificeringen, en verwante middelen tonen.

De Bouwer van de Ervaring van de mening [ voor meer informatie bij het creëren van douanepagina&#39;s gebruikend widgets.](/help/migrated/administrators/feature-summary/experience-builder/overview.md)

## Op taal gebaseerde voortgang van studenten

Momenteel houdt Adobe Learning Manager alleen de voortgang van de studenten bij voor de geselecteerde landinstelling. Dit leidt tot aanzienlijk voortgangsverlies wanneer wordt geschakeld tussen talen/landinstellingen in de speler. Deze beperking kan leiden tot een slechte gebruikerservaring, aangezien studenten hun voortgang kunnen verliezen bij het benaderen van inhoud in verschillende talen. De voortgang van elke module in de speler wordt zowel op gebruiker- als op moduleniveau bijgehouden. Dit leidt tot een situatie waarin de voortgang van een gebruiker wordt overschreven wanneer de gebruiker voor dezelfde module teruggaat naar een eerder gebruikte landinstelling.

Als een student bijvoorbeeld 75% vooruitgang boekt in landinstelling A (Engels) en vervolgens overschakelt naar landinstelling B (Spaans) en terugkeert naar landinstelling A, wordt de voortgang teruggezet op 0% in plaats van op 75%.

Om deze beperkingen op te lossen, is de functie uitgebreid voor het bijhouden van de landspecifieke voortgang:

* **plaats-specifieke opslag**: Wanneer een student landinstellingen (bijvoorbeeld, van Landinstelling A aan Landinstelling B) binnen de speler schakelt, bewaart Adobe Learning Manager nu afzonderlijk de vooruitgangsstaat voor elke scène van de inhoud.
* **Hervatting van de Voortgang**: Wanneer de gebruiker terug naar eerder gebruikte scène (van Scène B terug naar Scale A) schakelt, hervat de inhoud van waar zij in die specifieke scène weggingen.
* **Onafhankelijke vooruitgang het volgen**: Elke scène handhaaft zijn eigen staat van vooruitgang, die studenten toestaat om inhoud in veelvoudige talen te onderzoeken zonder hun individuele vooruitgang in elke taal te verliezen.

De volgende inhoudstypen worden niet ondersteund voor de voortgang van studenten op basis van hun taal:

* Video- en audio-inhoud wordt niet ondersteund.
* Inhoud van derden, zoals Go1, LinkedIn Learning, getAbstract en Harvard ManageMentor, wordt niet ondersteund.
* Voor de inhoud die geen gegevens naar de LRS (Learning Record Store) verzendt, wordt de voortgang niet bijgehouden of opgeslagen.
* Gebruikers van mobiele apps kunnen de voortgang voor deze functie niet bijhouden in de offline modus.

Bekijk [ Mijn het Leren ](/help/migrated/learners/feature-summary/courses.md#language-based-progress-management) voor meer informatie over op taal-gebaseerde studentvooruitgang.

## Incrementele en meervoudige ondersteuning voor aangepaste rollen

Adobe Learning Manager ondersteunt nu incrementele en meervoudige importbewerkingen voor aangepaste rollen en roltoewijzingen. Met incrementele importbewerkingen kunnen beheerders alleen nieuwe, bijgewerkte of verwijderde records van de gebruikers uploaden in plaats van het volledige CSV-bestand opnieuw te uploaden.

Multi-incrementele import breidt deze mogelijkheid uit door grote organisaties toe te staan incrementele bestanden te splitsen per regio of afdeling (bijvoorbeeld VS, EU, APAC) en deze tegelijkertijd te verwerken. Adobe Learning Manager biedt ook ondersteuning voor maximaal 20 incrementele gebruikers-CSV&#39;s en de bijbehorende aangepaste rollen-CSV&#39;s, waardoor deze schaalbaar zijn voor grote bewerkingen.

Beheerders kunnen nu rol- en gebruikersrolbestanden (role.csv en user_role.csv) stapsgewijs uploaden, samen met gebruikersbestanden (user.csv), in plaats van altijd volledig te uploaden. Elke gebruikersimport (user1.csv) is gekoppeld aan zijn eigen rol- en roltoewijzingsbestanden (user1_role.csv, user1_user_role.csv), opgeslagen in afzonderlijke FTP-mappen.

De volgende drie extra kolommen zijn toegevoegd aan de volgende CSV&#39;s:

* Status gebruikersregistratie (user.csv): geeft de huidige registratiestatus van de gebruiker in het systeem aan (bijvoorbeeld actief, inactief of verwijderd).
* Rolstatus (role.csv): geeft aan of een aangepaste rol momenteel actief of inactief is in het account.
* Rolstatus gebruiker (user_role.csv): definieert de status van de toewijzing tussen een gebruiker en een rol, waarbij wordt aangegeven of de toewijzing actief is of is verwijderd.

De Adobe Learning Manager legt nu acties vast voor het toevoegen, bijwerken en verwijderen van acties in de gebruikerscontrole en aangepaste rolrapporten, waardoor beheerders beter inzicht krijgen in wijzigingen.

>[!NOTE]
>
>Deze wijzigingen zijn alleen van toepassing op accounts die incrementele gebruikers gebruiken.

De incrementele en multi-stijgende steun van de mening [ voor meer informatie over stijgende en multi-stijgende steun voor douanerollen.](/help/migrated/integration-admin/feature-summary/configure-role-csv-files.md#incremental-and-multi-incremental-support-for-custom-roles)

## Verbeterde Go1-integratie

Go1-integratie is verbeterd zodat Go1-cursussen rechtstreeks kunnen worden beheerd voor het maken van LP&#39;s (Learning Programs) in Adobe Learning Manager. Deze update ondersteunt het opnemen van Go1-cursussen in terugkerende certificeringen en introduceert een nieuwe versie van de hubervaring voor Go1-inhoud, waardoor een efficiënter cursusbeheer mogelijk wordt.

* Maak en beheer afspeellijsten rechtstreeks in Go1 met behulp van AI-chatondersteuning of handmatige selectie.
* Neem Go1-cursussen op in terugkerende certificeringscycli met automatische terugzetprocedure. Bekijk [ Certificeringen ](/help/migrated/administrators/feature-summary/certifications.md) voor meer informatie bij het creëren van certificaten.
* Verbeterde interface voor het detecteren van inhoud voor beter bladeren en contentbeheer.

**Belangrijke nota&#39;s**

* Voor alle Go1-functies is een actieve Go1-licentie vereist.
* Eerdere gratis Go1-inhoud wordt uit bedrijf genomen. Organisaties moeten de vereiste inhoudsbundels voorvertonen en aanschaffen.
* Beheerders en auteurs kunnen een of meer afspeellijsten maken en beheren. Studenten behouden alleen toegang tot de weergave.

Bekijk [ Kromme Go1 cursussen aan het Leren Weg ](/help/migrated/administrators/feature-summary/content-marketplace/curate-go1-playlist.md) voor meer informatie bij het toevoegen van Go1 cursussen aan de het Leren Weg.

## Ondersteuning voor video-URL&#39;s in de activiteitenmodule

De module Activiteit ondersteunt nu het insluiten van Vimeo-URL&#39;s, vergelijkbaar met YouTube-insluiting. Dankzij deze verbetering kunnen beheerders rechtstreeks Vimeo-videokoppelingen toevoegen aan de activiteitenmodule. Wanneer auteurs een cursus maken en een activiteitenmodule toevoegen, zien ze nu een optie om een Vimeo-URL op te nemen. Net als bij het toevoegen van YouTube-koppelingen kunnen auteurs een Vimeo-koppeling rechtstreeks in de module-instelling plakken. Na publicatie kunnen studenten de Vimeo-video naadloos afspelen in de Learner-app zonder dat ze buiten het platform worden omgeleid.

De mening [ voegt modules ](/help/migrated/authors/feature-summary/courses.md#add-modules) voor meer informatie toe bij het toevoegen van modules aan de cursussen.

## Tijdzonegegevens voor CR/VC-modules

De tijdzonedetails worden nu weergegeven voor de modules Lesruimte (CR) en Virtuele lesruimte (VC) op de pagina Cursusoverzicht, Instantiepagina, Voorvertoning student en in de agendabreedte. Studenten en beheerders kunnen duidelijk de tijdzone zien die is gekoppeld aan geplande sessies op belangrijke pagina&#39;s en agenda-uitnodigingen. Studenten kunnen beter sessies plannen en deelnemen zonder misverstanden in de tijdzone. Deze verbetering is alleen beschikbaar in de Immersive Learner-app.

Studenten in verschillende regio&#39;s kunnen de sessietijd in de juiste tijdzone bevestigen. Het weergeven van de tijdzone helpt duidelijk gemiste sessies te voorkomen en zorgt voor nauwkeurige kalenderplanning.

## De naam van de auteur automatisch invullen tijdens het maken van een cursus

Tijdens cursusverwezenlijking, is het **[!UICONTROL Auteur(s)]** gebied nu automatisch bevolkt met de naam van de Auteurs die de cursus creëren. Auteurs hoeven niet langer handmatig hun eigen namen in te voeren. U kunt desgewenst nog meer auteurs toevoegen of bijwerken.

Voor organisaties met strikte regels voor contenteigendom zorgt automatische populatie ervoor dat auteurs altijd correct worden toegewezen. Wanneer auteurs een bestaande cursus bewerken, kunnen ze coauteurs bijwerken of toevoegen zonder dat de automatisch ingevulde gegevens verloren gaan.

Bekijk [ creeer een cursus ](/help/migrated/authors/feature-summary/courses.md#create-a-course---advanced-workflow) voor meer informatie over het creëren van een cursus.

## Externe profielen zoeken tijdens wijzigen profiel

Voorheen schuifden beheerders door de volledige lijst met externe profielen en selecteerden ze handmatig het gewenste profiel bij het opnieuw toewijzen van studenten. Dit maakte het proces tijdrovend, vooral voor accounts met veel profielen. Dankzij deze verbetering kunnen beheerders en aangepaste beheerders nu rechtstreeks op het tabblad zoeken naar externe profielen tijdens de workflow voor het wijzigen van profielen.

**gevallen van het Gebruik**

* In accounts met honderden externe profielen (bijvoorbeeld locaties met een licentie, partnerbedrijven of regionale groepen) kunnen beheerders het exacte profiel nu direct vinden door te zoeken, fouten te verminderen en tijd te besparen.
* Tijdens organisatorische veranderingen, zoals fusies of afdelingsaanpassingen, moeten studenten mogelijk bulksgewijs worden verplaatst naar nieuwe externe profielen. Deze taak wordt vloeiender en nauwkeuriger wanneer u een zoekopdracht uitvoert.

De mening [ Verandert het externe profiel ](/help/migrated/administrators/feature-summary/add-users-user-groups.md#change-profile) voor meer informatie bij het veranderen van het profiel.

## Een coorganisator toevoegen voor Microsoft Teams-sessies

Eerder konden auteurs slechts één organisator toewijzen aan Microsoft Teams-sessies. Dankzij deze verbetering kunnen beheerders nu co-organisatoren aan een sessie toevoegen. Een nieuw gebied, **[!UICONTROL Co-Organizer]**, is geïntroduceerd in de zittingen van Microsoft Teams, toestaand Auteurs om extra organisatoren naast de primaire organisator toe te wijzen.

Auteurs kunnen meerdere coorganisatoren toewijzen voor elke sessie met Microsoft Teams. Medeorganisatoren hebben dezelfde toegang en machtigingen als de primaire organisator. Auteurs kunnen per sessie maximaal 10 organisatoren toevoegen, wat meer flexibiliteit biedt en het sessiebeheer verbetert.

**geval van het Gebruik**

Bij het organiseren van grootschalige sessies met veel studenten kunnen coorganisatoren helpen de aanwezigheid te beheren, discussies te matigen en chatten te controleren terwijl de primaire organisator zich richt op het leveren van de training.

Bekijk [ voeg modules ](/help/migrated/authors/feature-summary/courses.md#add-modules) artikel voor meer informatie toe bij het toevoegen van CR/VC zittingen aan de cursussen.

## Rapport met geïnteresseerde studenten downloaden

Wanneer een beheerder alle cursusinstanties (bijvoorbeeld, aan het eind van de cursuslevenscyclus) archiveert, **[!UICONTROL Enroll]** knoop op de **[!UICONTROL pagina van het Overzicht van de Cursus]** wordt vervangen met de optie van de Rente van het a [!UICONTROL  Register ]. Studenten kunnen deze optie selecteren om te laten zien dat ze geïnteresseerd zijn in het volgen van de cursus. Beheerders kunnen nu een lijst weergeven en exporteren van studenten die belangstelling hebben voor een cursus.

Beheerders hebben dan toegang tot deze lijst en kunnen deze downloaden als een rapport. Een **[!UICONTROL Belangrijke studenten]** knoop is toegevoegd aan de cursuspagina wanneer geen actieve instanties beschikbaar zijn. De beheerdersinterface bevat de naam van de student en de datum waarop deze hun interesse hebben geregistreerd.

De beheerders kunnen de **[!UICONTROL Acties]** selecteren en dan **[!UICONTROL Rapport van de Uitvoer]** selecteren om het **[!UICONTROL Belangrijke Rapport van Studenten]** uit te voeren.

![](assets/register-interest.png)
_het overzichtssectie van de Cursus waar de studenten de optie van de Rente van het Register kunnen bekijken_

Bekijk [ Download de geïnteresseerde student ](/help/migrated/administrators/feature-summary/courses.md#download-the-interested-learner-report) voor meer informatie.

## Aanbevelingen opnieuw instellen in de Salesforce-app

Eerder konden studenten die de Adobe Learning Manager Salesforce-app gebruikten slechts eenmaal rollen en aanbevelingsvoorkeuren selecteren. Als hun rol veranderde, moesten ze overschakelen naar de native Adobe Learning Manager-app om hun profiel bij te werken en relevante cursusaanbevelingen te ontvangen. Met de nieuwste verbetering kunnen studenten nu snel hun voorkeuren opnieuw instellen, rechtstreeks in de Salesforce-app, wanneer hun taakrol, team of verantwoordelijkheden veranderen.

Dit gestroomlijnde proces zorgt ervoor dat ze bijgewerkte, relevante cursusaanbevelingen blijven ontvangen zonder Salesforce te verlaten. Beheerders profiteren van hogere leerresultaten en een betere afstemming tussen gebruikersrollen en aanbevolen inhoud, zonder extra ondersteuning of begeleiding bij het schakelen tussen platforms.

Adobe Learning Manager kenmerkt nu de knoop van de Interesten van het a **[!UICONTROL Terugstellen]** binnen Salesforce app. Studenten kunnen hun rollen en leervoorkeuren nu opnieuw instellen zonder Salesforce te moeten verlaten of zich aan te melden bij de native Adobe Learning Manager-app.

Bekijk [ Aanbevelingen van het Terugstellen in Salesforce app ](/help/migrated/learners/feature-summary/sfdc-app.md#reset-recommendations-in-salesforce-app) voor meer informatie over het terugstellen aanbevelingen in Salesforce app.

## Verbetering van de widget Kalender

Studenten kunnen nu zowel vorige als volgende sessies zien in de kalenderwidget. Ze kunnen door de kalender gaan naar een willekeurige datum en de sessiedetails controleren. Dit betekent dat ze sessies kunnen bekijken die al hebben plaatsgevonden, zodat ze kunnen bijhouden wat ze hebben gemist of bijgewoond. Ze kunnen ook alle komende sessies voor de komende 24 maanden bekijken, inclusief de huidige maand, zodat ze gemakkelijker kunnen plannen en hun planning kunnen beheren.

De Kalender van de mening [ voor meer informatie over Widget van de Kalender.](/help/migrated/learners/feature-summary/learner-home-page.md#calendar)

## Tags toewijzen aan gebruikers in sociale boards

Social boards ondersteunen nu de tagfunctie van gebruikers, waardoor gerichtere discussies mogelijk worden en de samenwerking binnen leergemeenschappen wordt verbeterd. Studenten kunnen via de Learner-app, API&#39;s en de Adobe Learning Manager-referentiesite worden gelabeld in berichten en opmerkingen voor Sociaal leren.

Gebruikers buiten het bereik van het board kunnen niet worden getagd om ongewenste meldingen te voorkomen. Als een gecodeerde gebruiker uit het systeem wordt verwijderd, wordt de bijbehorende vermelding weergegeven als &quot;anoniem&quot;. Het labelen van gebruikersgroepen of @all is niet toegestaan om berichtspam te voorkomen.

* **@gebruikersnaam tagging** : gebruikers kunnen andere leden van het board een tag toewijzen met behulp van de &quot;@gebruikersnaam&quot;-indeling.
* **gebied-beperkt het etiketteren**: Slechts kunnen de gebruikers met toegang tot de specifieke raad worden geëtiketteerd, verzekerend privacy en relevantie.
* **Meerkanaalsberichten**: De geëtiketteerde gebruikers ontvangen zowel in-app als e-mailberichten met directe verbindingen aan relevante berichten of commentaren.

**gevallen van het Gebruik**

* Beroepsbeoefenaars in de gezondheidszorg die op zoek zijn naar informatie van specifieke collega&#39;s over medische gevallen: met behulp van tags kunnen artsen en verpleegkundigen snel de juiste specialisten op de hoogte brengen, zodat tijdig en nauwkeurig advies wordt gegeven over complexe patiëntengevallen.
* Experts met onderwerpen die over gespecialiseerde onderwerpen worden geraadpleegd: door deskundigen van tags te voorzien, kunnen teams rechtstreeks de juiste mensen erbij betrekken, de reactietijd verminderen en de besluitvorming voor technische of nichevragen verbeteren.
* Teamdiscussies die input van specifieke belanghebbenden vereisen: Door belanghebbenden te taggen, zijn de relevante besluitvormers op de hoogte van updates en kunnen ze input leveren, projecten op schema houden en aansluiten bij bedrijfsdoelen.

De markering van de Gebruiker van de mening [ in Sociale Boards ](/help/migrated/learners/feature-summary/social-learning-web-user.md#tag-users-in-social-board-posts) voor meer informatie over het etiketteren van gebruikers in Sociale Boards.

## Scoped-aankondigingsmachtigingen voor aangepaste beheerders

Aangepaste beheerders kunnen nu aankondigingen maken, maar alleen voor hun toegewezen gebruikersgroepen of catalogi. Dit voorkomt ongewenste communicatie over organisatorische grenzen heen. Aangepaste beheerders kunnen alleen aankondigingen maken voor gebruikers binnen het toegewezen bereik. Aankondigingen kunnen betrekking hebben op specifieke gebruikersgroepen of catalogi. Volledige beheerders houden zicht op en controle over alle aankondigingen, inclusief de aankondigingen die door bereikbare aangepaste beheerders zijn gemaakt.

**Zeer belangrijke voordelen**

* Gerichte communicatie om ervoor te zorgen dat aankondigingen alleen relevante doelgroepen bereiken.
* Minder informatieoverbelasting doordat niet-relevante meldingen niet bij onbedoelde gebruikers terechtkomen.
* Behoudt organisatorische grenzen en voorkomt toevallige kruiscommunicatie.

**Belangrijke nota&#39;s**

* Als het werkingsgebied van een douanebeheerder verandert, tonen de beïnvloede aankondigingen een waarschuwingspictogram en vereisen individuele werkingsgebied terugstelt.
* Elke aankondiging moet afzonderlijk worden bijgewerkt wanneer het bereik wordt gewijzigd.
* Het [ Meldingsbericht ](/help/migrated/administrators/feature-summary/announcements.md) rapport toont slechts studenten binnen het toegewezen werkingsgebied van de douanebeheerder.

**gevallen van het Gebruik**

* Franchise-organisaties waar regionale managers alleen met hun franchisehouders moeten communiceren.
* Grote organisaties met regionale of afdelingsbeheerders die aankondigingen richten aan hun teams.

De mening [ leidt aankondiging voor het toegewezen werkingsgebied ](/help/migrated/administrators/feature-summary/announcements.md#create-announcement-for-the-assigned-scope) voor meer informatie bij het creëren van aankondiging voor toegewezen werkingsgebied.

## Aangepaste rol selecteren tijdens het publiceren van inhoud uit Adobe Captivate

Als een gebruiker meerdere aangepaste rollen heeft bij het publiceren van inhoud van Adobe Captivate naar Adobe Learning Manager, wordt hem gevraagd om de specifieke aangepaste rol te selecteren waaronder de cursus moet worden gepubliceerd. Dit zorgt ervoor dat de juiste eigenaar en machtigingen van de rol worden toegepast op de gepubliceerde cursus.

De rol van de Douane van de mening [ voor meer informatie bij het creëren van douanerollen voor de gebruikers.](/help/migrated/administrators/feature-summary/custom-role.md)

## Verbeteringen aan de widget Opgeslagen door mij

Eerder, die **[!UICONTROL selecteerde door me]** wordt opgeslagen toon alle cursussen beschikbaar in de catalogus. Nu, zien de studenten slechts hun bookmarked cursussen in de **[!UICONTROL Opgeslagen door me]** strook op de studentenhomepage. Als u deze strook selecteert, gaan studenten naar de cataloguspagina, waar alleen de cursussen die ze hebben opgeslagen, worden weergegeven.

In de catalogus kunnen studenten aanvullende filters toepassen om hun zoekopdracht te verfijnen. Wanneer een filter wordt toegepast, worden alleen cursussen weergegeven die aan de geselecteerde criteria voldoen. Eerder gemarkeerde cursussen worden alleen weergegeven als ze overeenkomen met het toegepaste filter.

De mening [ vormt bewaarde cursuswidgets in AEM plaatsen ](/help/migrated/integrate-aem-learning-manager.md#configure-my-saved-courses-widgets-in-aem-sites) voor meer informatie over bewaarde cursuswidget in AEM plaatsen.

## Ondersteuning voor het weergeven van auteursnamen in gedeelde cursussen

Eerder, toen een cursus met a [ peer rekening ](/help/migrated/administrators/feature-summary/peer-account.md) werd gedeeld, verscheen de Auteur als Externe Auteur. Cursussen geven nu de naam van de auteur weer, ongeacht of het een interne gebruiker van het hoofdaccount of een oudere auteur betreft (dus elke naam die tijdens het maken van de cursus als een tekenreeks is ingevoerd in het veld Auteurs). Als u een auteur selecteert, wordt het aantal cursussen weergegeven dat ze met het collega-account hebben gedeeld. Deze auteurs zijn echter geen daadwerkelijke gebruikers in het collega-account.

Als een gebruiker uit het hoofdaccount wordt verwijderd, worden de gegevens verwijderd, maar blijft de auteurinformatie in collega-accounts waarin de inhoud is gedeeld.

>[!NOTE]
>
>Dit is een op vlag-gebaseerde eigenschap, contacteer ons team van de Steun van de Klant in [ learningmanagersupport@adobe.com ](mailto:learningmanagersupport@adobe.com) om deze optie toe te laten.

De rekening van de mening [ voor meer informatie over het delen van inhoud aan peer rekening.](/help/migrated/administrators/feature-summary/peer-account.md)

## Zichtbaarheid zoeken voor leerobjecten met een lagere volgorde

Eerder werden in de zoekresultaten niet altijd afzonderlijke cursussen weergegeven wanneer deze deel uitmaakten van de leerobjecten in een hogere volgorde, zoals leerpaden of certificeringen. Als een student alleen was ingeschreven voor een leerpad of certificering, retourneerde de zoekopdracht alleen de structuur in een hogere volgorde en niet de individuele cursus.

Dankzij deze verbetering kunnen studenten nu afzonderlijke cursussen in zoekresultaten zien, zelfs als deze cursussen deel uitmaken van leerpaden of certificeringen. Een nieuwe beheerder die, **[!UICONTROL plaatst toont alle ingeschreven cursussen in onderzoeksresultaten]**, is geïntroduceerd. Als deze instelling is ingeschakeld, zorgt u ervoor dat bij het zoeken naar een specifieke cursus altijd de cursus zelf wordt weergegeven, samen met eventuele gerelateerde leerpaden of -certificeringen.

De Montages van de mening [ voor meer informatie over algemene montages.](/help/migrated/administrators/feature-summary/settings.md#general-settings)

## API-wijzigingen

### API-verbeteringen voor migratie

Adobe Learning Manager ondersteunt nu de migratie van verschillende gegevensobjecten naar een account via het migratieproces. Dit proces kan worden gestart via zowel API&#39;s als de gebruikersinterface. Wanneer een migratie mislukt, kunnen fouten via de interface worden gedownload. Deze fouten zijn handig bij het opsporen van fouten in de migratie en het beheren van de migratieuitvoering.

In deze release kunnen de foutlogboeken ook via de API&#39;s worden gedownload voor een efficiënte, programmatische foutopsporing en foutopsporing.

**API veranderingen**

Er is een nieuwe migratie-API, `runStatus` , waarmee integratiebeheerders de status van via de API getriggerde migratiesets kunnen controleren. Dit is niet mogelijk in eerdere versies van Adobe Learning Manager.

Bovendien biedt de `runStatus` API nu een directe koppeling om foutlogbestanden (CSV) te downloaden voor voltooide runs. De koppeling is slechts zeven dagen geldig en de logbestanden worden één maand bewaard.

De reactie van de `startRun` API is bijgewerkt en bevat nu de id van het migratieproject, de sprint-id en de sprint-run-id, die vereist zijn om het nieuwe statuseindpunt op te vragen.

#### runStatus API

**Beschrijving**

Hiermee wordt de status van een bestaande migratieuitvoering opgehaald.

**Eindpunt**

```
GET /bulkimport/runStatus
```

**Parameters**

* **migrationProjectId**: (Vereist). Een unieke id voor een migratieproject. Een migratieproject wordt gebruikt om gegevens en inhoud over te brengen van een bestaand LMS (Learning Management System) naar Adobe Learning Manager. Elk migratieproject kan uit meerdere sprints bestaan, kleinere eenheden migratietaken.

* **sprintId**: (Vereist). Een unieke id voor een sprint binnen een migratieproject. Een sprint is een subset migratietaken met specifieke leeritems (bijvoorbeeld cursussen, modules, studentrecords) die van een bestaand LMS naar Adobe Learning Manager moeten worden gemigreerd. Elke sprint kan onafhankelijk worden uitgevoerd, waardoor gefaseerde migratie mogelijk is.

* **sprintRunId**: (Vereist). Een unieke id die wordt gebruikt om de uitvoering van een specifieke sprint binnen een migratieproject te volgen. Het is gekoppeld aan het feitelijke migratieproces voor de items die zijn gedefinieerd in een sprint. sprintRunId helpt bij het controleren, oplossen van problemen en het beheren van de migratietaak.

**Antwoord**

```
{
  "sprintId": 2510080,
  "sprintRunId": 2740845,
  "migrationProjectId": 2509173,
  "startTime": 1746524711052,
  "endTime": 1746524711052,
  [
    {
      "id": 2609923,
      "lastHeartbeatTime": 1746524711052,
      "objectName": "content",
      "jobState": "COMPLETED",
      "errorCsvLink": "",
      "errorLogLink": "migration/5830/2509173/2510080/2740845/content_err.csv",
      "sequenceNumber": 1
    },
    {
      "id": 2609922,
      "lastHeartbeatTime": 1746524713577,
      "objectName": "course",
      "jobState": "WAITING_IN_QUEUE",
      "errorCsvLink": "",
      "errorLogLink": null,
      "sequenceNumber": 2
    }
  ]
}
```

#### startRun-API

De API-reactie van `startRun` is bijgewerkt en bevat nu drie extra velden: migrationProjectId, sprintId en sprintRunId. Met deze velden kunnen gebruikers de status van specifieke migratietests bijhouden en controleren met behulp van de nieuwe runStatus-API.

```
curl -X GET --header 'Accept: text/html' 'https://learningmanager.adobe.com/primeapi/v2/bulkimport/runStatus?migrationProjectId=001&sprintId=10001&sprintRunId=7'
```

Produceert de volgende reactie. De reactie bevat:

* `migrationId`
* `sprintId`
* `sprintRunId`

**Antwoord**

```
{
  "status": "OK",
  "title": "BULKIMPORT_RUN_INITIATED_SUCCESSFULLY",
  "source": {
    "info": "Success",
    "migrationInfo": {
      "migrationProjectId": "001",
      "sprintId": "10001",
      "sprintRunId": "7"
    }
  }
}
```

Het handboek van de Migratie van de mening [ voor meer informatie over het migreren van inhoud van bestaand LMS.](/help/migrated/integration-admin/feature-summary/migration-manual.md)

### Wijzigingen in de sociale API (gebruikerstag, opmerkingen en antwoorden)

Adobe Learning Manager ondersteunt nu de tagfunctie @user in Social Boards, waarmee studenten peers kunnen vermelden en melden in berichten, opmerkingen en antwoorden. Deze functie verbetert de samenwerking en de detectie van inhoud op het hele platform.

Deze release introduceert nieuwe API-mogelijkheden ter ondersteuning van gebruikersvermeldingen, waaronder verbeterde eindpunten voor POSTEN en GET, en een nieuwe zoekfunctie voor getagde gebruikers.

**API veranderingen overzicht**

* Bijgewerkte POST-API&#39;s voor het maken van berichten/opmerkingen/antwoorden met gebruikersvermeldingen
* Bijgewerkte GET-API&#39;s met gebruikersgegevens in reacties

**Formaat van gebruikersvermeldingen**

Een gebruiker wordt vermeld gebruikend het formaat: @ (gebruiker :userId)

#### Bericht met vermeldingen maken

**Eindpunt**

```
POST /primeapi/v2/posts
```

**Beschrijving**

Maak een nieuw bericht voor Sociaal leren met gebruikersvermeldingen.

**het lichaam van het Verzoek**

```
{
  "data": {
    "type": "post",
    "attributes": {
      "boardId": 13282,
      "accountId": 11152,
      "text": "<p>This is a new post mentioning @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "postType": "discussion"
    },
    "id": null
  }
}
```

**Antwoord**

De standaard post creatiereactie met verwijzingsgegevens inbegrepen in de _userMentions_ verhouding.

#### Opmerking maken met vermeldingen

**Eindpunt**

```
POST /primeapi/v2/comments
```

**Beschrijving**

Voeg een opmerking toe aan een bericht met gebruikersvermeldingen.

**het lichaam van het Verzoek**

```
{
  "data": {
    "type": "comment",
    "attributes": {
      "postId": 20746,
      "accountId": 11152,
      "text": "<p>Test Comment @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "commentLevel": 0
    },
    "id": null
  }
}
```

#### Reactie maken met vermeldingen

**Eindpunt**

```
POST /primeapi/v2/replies
```

**Beschrijving**

Reageer op een opmerking met gebruikersvermeldingen.

**het lichaam van het Verzoek**

```
{
  "data": {
    "type": "reply",
    "attributes": {
      "postId": 20746,
      "accountId": 11152,
      "text": "<p>Thanks for the update @[user:11257229]</p>",
      "createdByUserId": 11257228,
      "commentLevel": 1,
      "parentCommentId": 55621
    },
    "id": null
  }
}
```

#### Publicaties met vermeldingen ophalen

**Eindpunt**

```
GET /primeapi/v2/posts/{id}
```

**Beschrijving**

Haal de postgegevens op, inclusief de vermelde gebruikers.

**Antwoord**

```
{
  "links": {
    "self": "https://learningmanager.adobe.com/primeapi/v2/posts/7522"
  },
  "data": {
    "id": "7522",
    "type": "post",
    "attributes": {
      "commentCount": 3,
      "dateCreated": "2025-06-10T11:33:29.000Z",
      "dateUpdated": "2025-06-25T14:52:04.000Z",
      "downVote": 0,
      "postingType": "DEFAULT",
      "richText": "<p>my updated fourth post @[user:14707776] second mention my first post</p>",
      "state": "ACTIVE",
      "text": "my updated fourth post @[user:14707776] second mention my first post",
      "upVote": 0,
      "viewsCount": 0
    },
    "relationships": {
      "createdBy": {
        "data": {
          "id": "14707776",
          "type": "user"
        }
      },
      "parent": {
        "data": {
          "id": "3971",
          "type": "board"
        }
      },
      "userMentions": {
        "data": [
          {
            "id": "14707776",
            "type": "user"
          }
        ]
      }
    }
  },
  "included": [
    {
      "id": "14707776",
      "type": "user",
      "attributes": {
        "avatarUrl": "https://cpcontents.adobe.com/public/images/default_user_avatar.svg",
        "binUserId": "45664b87-75a3-43ec-b0b7-5064958eac6f",
        "email": "user@example.com",
        "enrollOnClick": false,
        "fields": {
          "Location": "BLR"
        },
        "gamificationEnabled": true,
        "lastLoginDate": "2025-06-27T11:21:17.000Z",
        "name": "John Doe",
        "pointsEarned": 1690,
        "pointsRedeemed": 0,
        "preferredResolution": "AUTO",
        "profile": "admin",
        "roles": [
          "Learner",
          "Admin",
          "Author",
          "Instructor",
          "Integration Admin",
          "Manager"
        ],
        "state": "ACTIVE",
        "userType": "Internal"
      },
      "relationships": {
        "account": {
          "data": {
            "id": "9238",
            "type": "account"
          }
        }
      }
    }
  ]
}
```

### Wijzigingen in de sociale API (gebruikerszoekopdracht)

**Eindpunt**

```
GET /primeapi/v2/users/search?q={searchTerm}&context=tagging
```

**Beschrijving**

Zoek naar gebruikers die beschikbaar zijn voor tags op basis van instellingen voor sociale bereiken.

**parameters van het Verzoek**


* q (vereist): zoekterm (minimaal 3 tekens).
* context: Stel deze optie in op &#39;coderen&#39; om gebruikers in aanmerking te laten komen voor vermeldingen.
* boardId (optioneel): kaart-id om gebruikers te filteren op basis van toegangsrechten.

**Antwoord**

```
{
  "data": [
    {
      "id": "11257229",
      "type": "user",
      "attributes": {
        "name": "Jane Smith",
        "email": "jane.smith@example.com",
        "avatarUrl": "https://cpcontents.adobe.com/public/images/default_user_avatar.svg",
        "userType": "Internal",
        "state": "ACTIVE"
      }
    }
  ]
}
```

### API-verbeteringen voor studenten voor het bijhouden van quizprestaties

De API van `GET /loResourceGrades` is verbeterd en biedt gedetailleerde quizprestatiedata, waardoor geavanceerdere analytics en geautomatiseerde besluitvorming mogelijk zijn.

De API-reactie bevat nu twee extra velden:

* **[!UICONTROL hoogsteScore]**: De beste score die door een student over alle quizpogingen wordt bereikt
* **[!UICONTROL maxScore]**: De totale mogelijke score voor de quiz

**API reactievoorbeeld**

```
{
    "links": {
        "self": "https://learningmanagerstage1.adobe.com/primeapi/v2/loResourceGrades/course:15067_30122_41715_1_3400468"
    },
    "data": {
        "id": "course:15067_30122_41715_1_3400468",
        "type": "learningObjectResourceGrade",
        "attributes": {
            "completed": false,
            "duration": 0,
            "hasPassed": false,
            "highestScore": 0,
            "maxScore": 0,. 
            "progressPercent": 0,
            "score": 0
        },
        "relationships": {
            "loResource": {
                "data": {
                    "id": "course:15067_30122_41715_1",
                    "type": "learningObjectResource"
                }
            }
        }
    }
}
```

In antwoord, **cursus:15067_30122_41715_1_3400468** is identiteitskaart van de het middelgraad van het Leerobject waarvoor de informatie wordt gevraagd. De `learningObjectResourceGrad` e id kan worden verkregen via de `GET /enrollments/{id}` API.

### API-reacties ondersteunen hoofdlettergevoeligheid voor auteursnamen

De API-reactie geeft nu precies het geval van oudere auteursnamen zoals die zijn ingevoerd tijdens het maken of bijwerken van een cursus. Dit zorgt ervoor dat namen consistent worden weergegeven in de gebruikersinterface van de student en in de openbare API&#39;s.

* Wanneer een nieuwe auteursnaam wordt toegevoegd, wordt de case opgeslagen en geretourneerd precies zoals ingevoerd.
* Als een bestaande auteursnaam wordt verwijderd en opnieuw met een ander geval wordt toegevoegd, wordt het bijgewerkte geval gerespecteerd en weerspiegeld in alle cursussen met die auteursnaam.
* Er wordt geen automatische migratie uitgevoerd voor eerder opgeslagen namen. Alleen nieuw toegevoegde of bijgewerkte namen volgen dit gedrag.

### API-uitbreiding voor agenda

De agenda laadt nu sessies voor de maand die door de gebruiker is geselecteerd. Als u zowel eerdere als volgende sessies wilt ophalen via de API, is een nieuwe `year` -parameter toegevoegd aan het eindpunt van de student `GET /users/{id}/calendar` . De parameters `month` en `year` moeten samen worden opgegeven om de sessiedetails op te halen.

**Steekproef krullen**

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth a4ae04eb9f06f4bf88abcde17' 'https://abc.adobe.com/primeapi/v2/users/12345678/calendar?month=7&year=2025&currentMonthOnly=false&filter.allSessions=false'
```

### Ondersteuning voor markeringsvoltooiing via Administrator API

Eerder ondersteunde de openbare API geen ondersteuning voor op instanties gebaseerde voltooiingsmarkeringen in scenario&#39;s voor meerdere inschrijvingen. Dankzij deze verbetering kunt u nu de instantie-id van de cursus opnemen in de hoofdtekst van de aanvraag van `POST /users/{userId}/userModuleGrade` en kan de beheerder de voltooiing van een specifieke instantie markeren.

### Voorkeuren voor gebruikers-id&#39;s instellen voor SCORM-rapportage

Sommige klanten hebben de UUID (Universally Unique Identifier) van de student nodig in plaats van de standaard user_id voor het voltooien van SCORM-inhoud. Het gebruik van de UUID zorgt voor nauwkeuriger tracering in alle leerprogramma&#39;s en voorkomt dubbel licentiegebruik in MAU-accounts (Monthly Active User).

Ter ondersteuning hiervan is een nieuwe instelling op accountniveau, `reporting_userid_preference` , toegevoegd. Als deze instelling is ingeschakeld, wordt de UUID in plaats van de user_id verzonden wanneer studenten SCORM-inhoud voltooien.

>[!NOTE]
>
> Contacteer ons team van de Steun van de Klant in [ learningmanagersupport@adobe.com ](mailto:learningmanagersupport@adobe.com) om dit het plaatsen te vormen.

Het nieuwe kenmerk `reportingUserIdPreference` is toegevoegd aan `get /account` om de voorkeuren voor de gebruikers-id bij te houden.

### Auteursgegevens in gedeelde cursussen

In de API voor leerobjecten is de manier waarop auteursinformatie wordt geretourneerd, bijgewerkt om onderscheid te maken tussen hoofdaccountcursussen en cursussen die met collega-accounts worden gedeeld:

* Gedeelde cursussen (Collega-account): de auteurdetails worden nu geretourneerd onder een nieuw kenmerk, `authorDetails` . Dit kenmerk geeft de naam van de auteur op, zelfs als de cursus van een ander account afkomstig is.

* Hoofdaccountcursussen: auteursinformatie wordt nog steeds geretourneerd onder het bestaande `authors` -kenmerk, zonder wijziging in het huidige gedrag.

Deze wijziging zorgt voor consistentie in de manier waarop auteurgegevens via API beschikbaar worden gemaakt voor zowel hoofd- als gedeelde cursussen, terwijl de compatibiliteit voor bestaande integraties behouden blijft.

## Wijzigingen in webhooks

### LinkedIn Learning-webhooks registreren met behulp van de connector

Voorheen moesten beheerders LinkedIn Learning-webhooks handmatig registreren bij Adobe Learning Manager via API&#39;s. Dankzij deze verbetering ondersteunt de LinkedIn Learning-connector (LIL) nu automatisch webhookregistratie tijdens nieuwe verbindingsinstellingen in ALM. De **URL van de Server OAuth** en **TenantServer URL** zal automatisch bevolkt op de LinkedIn Lerende configuratiepagina zijn.

Bekijk [ LinkedIn Lerend ](/help/migrated/integration-admin/feature-summary/connectors.md#linkedin-learning-connector) voor meer informatie over LinkedIn Lerende integratie.

### Wijzigingen in MAU-licentiegebruik in LinkedIn Learning

Eerder telde Adobe Learning Manager het licentiegebruik niet wanneer een student een LinkedIn Learning-cursus rechtstreeks op het LinkedIn Learning-platform voltooide voor MAU-accounts (maandelijkse actieve gebruikers). Het gebruik van de licentie werd alleen geactiveerd voor cursussen die via de Adobe Learning Manager-speler werden gevolgd, waardoor de maandelijkse actieve gebruikers (MAU) onjuist werden gevolgd.

Dankzij deze verbetering genereert Adobe Learning Manager nu een externe webhook wanneer een student een cursus voltooit in het LinkedIn Learning-platform. Wanneer Adobe Learning Manager deze webhook ontvangt, berekent het het licentiegebruik voor nauwkeurige tracering op beide platforms.

## Wijzigingen rapportage

### Voltooiingen die zijn gemarkeerd als docent in Studenttranscripten

Incrementele studenttranscripten leggen nu door de docent gemarkeerde voltooide taken vast, zelfs als aanwezigheid na de sessiedatum wordt vastgelegd.
Deze verbetering verhelpt een kritieke leemte in incrementele studenttranscripten waarbij de door de docent gemarkeerde voltooiingen eerder werden gemist als aanwezigheid werd vastgelegd na de oorspronkelijke sessiedatum.

Incrementele studenttranscripten zijn geplande rapporten waarin alleen de wijzigingen worden vastgelegd (zoals voltooiingen of voortgangsupdates) die zich binnen een opgegeven periode voordoen, in plaats van een volledige historische datumpdump. Ze worden vaak gebruikt voor automatisering, dashboards en integraties, waardoor gebruikers recente leeractiviteiten efficiënt kunnen volgen zonder dat telkens de volledige transcripthistorie moet worden verwerkt.

* **Teken Voltooide Datum (UTC TimeZone) kolom**: Een nieuwe timestamp kolom die de nauwkeurige datum en de tijd vangt wanneer een instructeur een zitting of een module als volledig merkt.
* **Verbeterde het verbeterde eind bron volgen**: Traceert de specifieke instructeur en de module (bijvoorbeeld, &quot;Klaslokaal&quot;) waar de voltooiing werden geregistreerd.

Deze wijzigingen zorgen ervoor dat voltooide bewerkingen die zijn gemarkeerd na de sessiedatum, correct worden weergegeven in incrementele studenttranscripten.

**gevallen van het Gebruik**

* Organisaties met klassikale sessies waarbij docenten aanwezigheid dagen na de sessie kunnen markeren.
* Geautomatiseerde systemen of dashboards waarbij incrementele studenttranscripten worden gebruikt voor compliance of rapportage.

![ de rapporten van het Transcriptie van de Student die duidelijke voltooide (geel gemarkeerde) data tonen voor het volgen van de cursusvoltooiing in het Leren van de Adobe ](/help/migrated/assets/mark-completion-column.png)
_het rapport van het Transcriptie van de Student toont een nieuwe kolom in geel die individuele voltooiingsdata voor elke gebruiker benadrukt_

Bekijk [ Studenttranscript ](/help/migrated/administrators/feature-summary/learner-transcripts.md) voor meer informatie over het rapport van het Studenttranscript.

### Verbeterd gebruikersrapport met uitgebreide gegevensvelden

Het gebruikersrapport bevat nu extra velden waarmee gebruikers beter kunnen worden gevolgd en de organisatie beter kan worden toegewezen. Deze updates vereenvoudigen gebruikersidentificatie, ondersteunen integratie met downstream-gebruikersbeheerworkflows, verbeteren het inzicht in rapportagerelaties en handhaven organisatorische grenzen om onbedoelde kruiscommunicatie te voorkomen.

* Kolom interne gebruiker-id: verschaft unieke interne id&#39;s voor een vloeiende gebruikersregistratie voor verschillende systemen en API-eindpunten.
* E-mailkolom van manager: bevat contactgegevens van directe managers voor het bijhouden van de hiërarchie van de organisatie.

![ Rapport van de Gebruiker die de interne gebruiker - identiteitskaart en manager e-mailkolommen tonen die in geel worden benadrukt ](/help/migrated/assets/user-report-columns.png)
_Rapporten die van de Gebruiker interne gebruiker IDs en manager e-mailadressen benadrukken om gebruikersbeheer te stroomlijnen_

Bekijk [ Download het gebruikersrapport ](/help/migrated/administrators/feature-summary/add-users-user-groups.md#download-the-user-report) voor meer informatie over het Rapport van de Gebruiker.

### Gebruikersrapport in FTP, aangepaste FTP en Box

**Overzicht**

Het gebruikersrapport is nu beschikbaar voor Box-, FTP- en Aangepaste FTP-connectoren, naast de bestaande taak-API&#39;s. Deze rapporten bevatten gedetailleerde informatie over de interne gebruikers-id, e-mail van de gebruiker, naam, e-mail van de manager, gebruikerstype en andere.

Rapporten kunnen op aanvraag worden gegenereerd of gepland, met gegevens die in de desbetreffende connector zijn opgeslagen voor eenvoudige toegang en analyse. Deze verbetering verbetert het toezicht op en de controle van gebruikersactiviteiten, en ondersteunt betere beveiliging en naleving.

Deze rapporten zijn beschikbaar naast bestaande rapporten, zoals gebruikersregistratie, aanmeldingstoegang, gamification en training, waardoor beheerders toegang hebben tot alle essentiële rapporten op één locatie voor gestroomlijnd gegevensbeheer en -analyse.

De Schakelaar van de mening [ voor meer informatie over FTP, Aangepaste FTP, en de schakelaar van de Doos.](/help/migrated/integration-admin/feature-summary/connectors.md)

### Opgeschorte gebruikers opnemen in Studenttranscripten

**Overzicht**

Organisaties kunnen nu geschorste gebruikers (gebruikers met uitgeschakelde externe profielen) opnemen in Studenttranscripten, zodat u beschikt over uitgebreide bewaarinstellingen voor historische leergegevens.

* Markering op accountniveau om de zichtbaarheid van gebruikers op te schorten, zodat gebruikers met een schorsing kunnen verschijnen in Studenttranscripten.
* Historische databehoud zelfs na deactivering van geschorste externe profielen.

**de vereisten van de Implementatie**

* Neem contact op met uw Customer Success Manager (CSM) om de markering op accountniveau in te schakelen.

>[!NOTE]
>
>Deze markering is standaard uitgeschakeld voor bestaande accounts en moet expliciet worden aangevraagd voor nieuwe accounts.

Bekijk [ artikel van het Transcriptie van de Student ](/help/migrated/administrators/feature-summary/learner-transcripts.md) meer informatie.

### Taakhulpenrapport met directe toegangskoppelingen

**Overzicht**

Het Taakhulpenrapport is uitgebreid en bevat nu directe downloadkoppelingen naar taakhulpen, waarmee het contentmanagement en de auditprocessen voor beheerders en auteurs worden gestroomlijnd. Deze verbetering geeft directe bestandsuploads en URL-toegang vanuit het rapport. Zo voorkomt u handmatige inspanningen bij het zoeken naar en downloaden van taakhulpen voor compatibiliteits- of toegankelijkheidscontroles.

* Kolom voor taakhulp koppelen: directe toegang tot taakhulpbestanden en externe URL&#39;s vanuit het rapport.
* Op rollen gebaseerd toegangsbeheer: toegankelijkheid van koppeling is afhankelijk van gebruikersrollen en catalogusmachtigingen.
* Verwijderde taakhulpen blijven toegankelijk als ze nog steeds aan actieve cursussen zijn gekoppeld.

**gevallen van het Gebruik**

* Auteurs of beheerders voeren regelmatig toegankelijkheidscontroles uit op taakhulpen, zoals vereist door grote organisaties.
* Elk scenario waarin snelle, op rollen gebaseerde toegang tot taakhulpenbestanden nodig is voor revisie of naleving.

![](/help/migrated/assets/job-aid-report.png)
_het Rapport van de Hulp van de Baan toont directe downloadverbindingen, die het gemakkelijk maken om tot taakhulpen in Adobe Learning Manager toegang te hebben en te downloaden_

Het Rapport van de Hulp van de Baan van de mening [ voor meer informatie over het rapport van de Hulp van de Baan.](/help/migrated/administrators/feature-summary/reports.md#job-aids-report)

## Bugfixes in deze update

* L2 Quizscores worden nu correct gegenereerd voor niet-interactieve quizzen, inclusief gegevens van gebruikers die deze hebben voltooid.
* De handtekening wordt nu correct naar de doelhost verzonden wanneer het verificatiemechanisme tijdens de verbindingsconfiguratie is ingesteld op Handtekening.
* Dummygebruikers die tijdens Adobe Connect-sessies zijn gemaakt, zijn niet verwijderd na voltooiing van de sessie. De SnapLogic-pijplijn verwijdert deze gebruikers nu op de juiste wijze, zelfs wanneer de `principals-delete` -API eerder een 200-reactie heeft gegeven zonder ze te verwijderen.
* `null` `eventDetail` -objecten in API-reacties veroorzaken niet langer uitzonderingen. Het systeem slaat nu null-items over en verwerkt de gehele array, zodat volledige opnamen worden gegarandeerd.
* In de kolom Datum van feedback in feedbackrapporten wordt nu de juiste datum weergegeven. Voorheen werden seconden onjuist doorgegeven aan de constructor Date, die milliseconden verwacht, waardoor datums werden weergegeven als januari 1970. Dit is gecorrigeerd voor een nauwkeurige datumweergave bij het genereren van feedbackrapporten.
* Studenten kunnen nu hun inschrijving in een Flex Learning Path bijwerken, zelfs als een van de cursusinstanties is gearchiveerd. Eerder veroorzaakte het selecteren van een nieuwe instantie een consolefout (Kan eigenschappen van ongedefinieerd niet lezen) en werd de update verhinderd.
* Bronnamen in leerpaden worden nu op de juiste wijze weergegeven zonder het woord middenweg te breken.
* LinkedIn Learning-webhooks zijn nu ingeschakeld vanuit de LIL-connector wanneer u verbindingen maakt voor nieuwe gebruikers. Het systeem registreert het account ook via de persoonlijke API en geeft aanvullende configuratiegegevens (OAuth URL en Tenant URL) weer op de LinkedIn Learning-configuratiepagina.
* De gebruikerskenmerkwaarden die via SAML-workflows (`UpdateUserWorkerTask`) worden bijgewerkt, worden nu met hun originele hoofdletters opgeslagen in plaats van te worden omgezet in kleine letters.
* Als u de volgorde van modules in een cursus wijzigt, wordt het aantal verplichte modules niet meer teruggezet op &quot;Alle&quot;. Het aantal blijft nu zoals geconfigureerd.
* Go1-pijplijnen verwerken nu taalcodes consistent door tweelettercodes toe te wijzen aan vierlettercodes, vergelijkbaar met LinkedIn Learning-pijplijnen.
* In Acrobat+-accounts zagen studenten eerder &quot;Deze cursus bestaat niet&quot; toen ze een cursus Leerpad lanceerden na uitschrijving uit een certificering. Inschrijvingsbronnen worden nu correct bijgewerkt, zodat cursussen in leerpaden zonder fouten kunnen worden gestart.
* Wanneer het bestand module_version.csv contenttypevelden met lege of null-waarden bevat, werkt het maken van een cursus nu zonder problemen.
* Cursussen worden nu op de juiste wijze weergegeven wanneer wordt gefilterd op Catalogus of Cataloguslabel. Voorheen werden bij het toepassen van deze filters op de cursuspagina geen cursussen weergegeven, zelfs niet als deze aan de catalogus waren gekoppeld.
* In de Learner-app bleef het drukken op TAB in de Fluidic Player vastzitten op de knop &quot;Enter Fullscreen&quot;. Toetsenbordnavigatie doorloopt nu correct alle schermelementen.
* Als u de muis boven lange cursusnamen in het dashboard Naleving van de Manager-app houdt, wordt nu de volledige naam voor ingeschreven of conforme cursussen weergegeven.
* Alleen Gedeeld of HIDDEN worden geaccepteerd voor de kolom voor de zichtbaarheid van de module in module.csv. Bij elke andere waarde wordt een fout tijdens de migratie gegenereerd, waardoor fouten op de back-end worden voorkomen.
* Als u een nieuwe beheerder maakt met een e-mail met meerdere hoofdletters, worden niet langer dubbele gebruikersgegevens gegenereerd wanneer UUID is uitgeschakeld. Het systeem verwerkt nu consistent e-mailcasings om dubbele gegevens te voorkomen.
* Notities PDF worden nu correct weergegeven voor cursussen in talen zoals Arabisch, Grieks, Hebreeuws, Hindi, Thai en Oekraïens. Voorheen werden tekens vervormd weergegeven in de gedownloade PDF, ook al werden ze correct weergegeven in de speler.

## Systeemvereisten

De systeemvereisten van de mening [ Adobe Learning Manager ](/help/migrated/system-requirements.md).

## Opmerkingen bij de release

Controle uit de [ versienota&#39;s ](/help/migrated/release-note/release-notes.md) voor recentste versieupdates.

## Eerdere releases van Adobe Learning Manager

* [Adobe Learning Manager-versie van mei 2025](/help/migrated/whats-new-may-2025.md)
* [Adobe Learning Manager-versie van november 2025](/help/migrated/whats-new-nov-24.md)


