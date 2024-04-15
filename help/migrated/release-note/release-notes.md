---
description: Opmerkingen bij de release van Adobe Learning Manager
jcr-language: en_us
title: Opmerkingen bij de release van Adobe Learning Manager
contentowner: jayakarr
exl-id: ae9251b6-5326-42c2-881e-2ab3393d9e17
source-git-commit: 5525aa6f5b4c795e4ffbd008e9fe865abfbe4980
workflow-type: tm+mt
source-wordcount: '26223'
ht-degree: 72%

---

# Opmerkingen bij de release van Adobe Learning Manager

<!--<table>
 <tbody>
  <tr>
   <td><img src="assets/cp-prime-appicon-88x84.png"></td>
   <td>
    <p><a href="https://business.adobe.com/products/learning-manager/adobe-learning-manager.html">Adobe Learning Manager</a> was launched in August 2015. As part of our continuous improvement efforts to enhance the product, we have been rolling out regular updates. Read on to know the features enhanced/issues fixed in update releases.<br></p></td>
  </tr>
 </tbody>
</table>-->

+++Update 96: De Adobe Learning Manager-versie van maart 2024

**Releasedatum:** 1 maart 2023

## Nieuw in deze release

Bekijk [Wat is er nieuw in Adobe Learning Manager](/help/migrated/whats-new.md) voor meer informatie.
+++

+++Update 95: de november 2023-versie van Adobe Learning Manager

**Releasedatum:** 18 november 2023

## Nieuw in deze release

Bekijk [Wat is er nieuw in Adobe Learning Manager](https://experienceleague.adobe.com/en/docs/learning-manager/using/introduction/whats-new-november-2023) voor meer informatie.
+++

+++Update 94

**Releasedatum:** donderdag 23 augustus 2023

## Nieuw in deze update

* Selecteer het tandwielpictogram van de speler om de kwaliteit van de video te wijzigen.
* Wijzig de kwaliteit en snelheid van een video op social media.
+++

+++Update 93: de juli 2023-versie van Adobe Learning Manager

**Releasedatum:** 10 jul. 2023

Nieuw in deze release

### Verbeterde aanbevelingen

Adobe Learning Manager heeft een nieuw en verbeterd aanbevelingssysteem voor cursussen geïntroduceerd. Deze aanbevelingsfunctie gebruikt AI-algoritmen en gebruikersinteresses zoals Producten, Rollen en Niveaus om gepersonaliseerde contentaanbevelingen te bieden.

### Meerdere inschrijvingen

In deze versie van Adobe Learning Manager introduceren we meerdere inschrijvingen voor studenten, waardoor studenten zich kunnen inschrijven voor meer dan één instantie van een cursus in één of verschillende tijdsperioden.

### Verplaatsing van de Exavault-connector

Deze versie van Adobe Learning Manager bevat een nieuwe connector die gebruik maakt van het SFTP-protocol van AWS Transfer Family.

Zie voor meer informatie [Nieuwe functies in de juli 2023-versie van Adobe Learning Manager](/help/migrated/whats-new-2023-july.md).
+++

+++Update: 92

**Releasedatum:** 23 juni 2023

**bugs gecorrigeerd in deze update**

* Nadat u een module hebt voltooid, wordt de graad-API niet automatisch geactiveerd, wat resulteert in een groen vinkje dat niet wordt weergegeven zoals verwacht in de gebruikersinterface.
* Na het voltooien van een paar modules in een leerpad of een certificering wordt het groene vinkje, dat aangeeft dat het pad of de certificering is voltooid, niet weergegeven zoals verwacht.
* Adobe Learning Manager wordt niet gestart zoals verwacht nadat een gebruikers-CSV met onjuiste velden is geüpload.
* In het pop-upvenster met waarschuwingen over hoe u contact opneemt met de beheerder worden ook andere e-mailadressen weergegeven.
* Alle badges die een student heeft verdiend, worden niet weergegeven in het antwoord.
* Tijdens gebruikersregistratie moet een gebruikersnaam met &quot; &quot; worden geaccepteerd.

#### Speler

* Voeg een menu toe om de schermresolutie te selecteren bij het afspelen van een video.
+++

+++Update 91

**Releasedatum:** vrijdag 1 juni 2023

### Connectoren

* De Adobe Connect-connector vereist API&#39;s om CSRF-tokens te verzenden. Zie De beveiliging van Adobe Connect-accounts verbeteren voor meer informatie.

### Tekenreekswijziging

* We hebben de naam van de tekenreeks Rate this training gewijzigd om deze cursus te beoordelen, dit leerpad te beoordelen of deze certificering te beoordelen op basis van de training die een student volgt. Afhankelijk van het type training ziet een student de tekenreeks dienovereenkomstig.

### Bugfixes in deze update

* In de beschrijving van de mobiele app Adobe Leermanager van de Play Store wordt ten onrechte gezegd dat een student een cursus offline kan volgen.
* Er zijn problemen opgetreden bij het migreren van inhoud (module_version.csv en course_module.csv) van LinkedIn naar Adobe Learning Manager.
* Als een account inactief is en meer dan drie jaar geleden is aangemaakt, worden alle gebruikers van het account verwijderd uit de AVG, ongeacht de status van de gebruikers.
* Wanneer u in de app voor docenten de wachtlijstlimiet instelt op nul in een sessie en de sessie opslaat, wordt in de gebruikersinterface onjuist &#39;Niet van toepassing&#39; weergegeven in plaats van nul.
* Bij het genereren van studenttranscripten voor de Power BI-connector geeft de kolom Training of Moduleduur (minuten) de null-waarden weer voor bepaalde klassikale of VC-modules.
* Nadat u een cursus voor studenten als voltooid hebt gemarkeerd in een of meerdere instanties, worden alle studenten in de cursus als voltooid gemarkeerd, niet alleen de studenten in de huidige instantie(s).
+++

+++Update 90

**Releasedatum:** 4 april 2023

### In deze update opgeloste bugs

SAML-aanmelding mislukt als de SSO-aanmeldings-URL de entity_id bevat.
+++

+++Update 89: De Adobe Learning Manager-versie van maart 2023

**Releasedatum:** 4 april 2023

### Nieuw in deze update

**Verbeteringen aan de ILT-ervaring (Instructor Led Training)**

Er zijn verschillende verbeteringen aangebracht in de ILT-ervaring (Instructor-Led Training). Belangrijke verbeteringen zijn: de mogelijkheid om klassikale sessies te filteren op basis van locatie, de mogelijkheid om van instantie te wisselen (VILT) zonder dat de voortgang verloren gaat, een nieuwe &quot;Planningsassistent&quot; voor het beheren van conflicten in het boeken van docenten en klaslokalen, de mogelijkheid om &quot;Vaardigheden&quot; aan docenten te koppelen en op vaardigheden gebaseerde docenten te kiezen.

**Verbeteringen van de controlelijst voor waarneming**:

Auteurs kunnen nu &quot;Manager&quot; en &quot;Winkelmanager&quot; selecteren als waarnemer voor checklists. Managers kunnen de controlelijsten bekijken en invullen binnen de Manager-interface zonder dat ze de rol hoeven wijzigen naar een docent. Wanneer een controlelijst aan een manager is toegewezen, krijgt hij/zij hier een melding van.

**Gebruik elke app-/smartphone-camera om QR-codes voor Learning Manager te scannen**

Studenten kunnen nu elke QR Code scanning-app of hun smartphone gebruiken om de door de Learning Manager gegenereerde QR-codes te scannen voor cursusinschrijving, voltooiing en meer.

**Rapportageverbeteringen**

Een nieuw gebruiksrapport voor docenten, Revisit-rapport voor trainingen, taakhulpenrapport en andere rapportverbeteringen.

**Ondersteuning voor &#39;hybride&#39; sessies**

Adobe Learning Manager ondersteunt nu de mogelijkheid om &quot;hybride&quot; ILT-sessies (Instructor Led Training) te maken. Virtuele ILT-sessies kunnen worden gemaakt met optionele locatie-informatie zodat studenten ook fysiek kunnen deelnemen aan de sessie als ze beschikbaar zijn op de locatie.

**Betere voortgang bijhouden voor klaslokaal en virtuele ILT**

De klassikale en virtuele ILT-modules bieden nu de mogelijkheid om de quizstatus van een student (geslaagd of gezakt) samen met de aanwezigheidsstatus te melden. Zowel vastgelegde aanwezigheid als geslaagde quiz kunnen in acht worden genomen bij het beslissen van de voortgang van de student.

**Adobe Learning Manager-app voor Microsoft Teams**

De nieuwe Adobe Learning Manager-app op Microsoft Teams is ontworpen om leren in de flow van het werk te bevorderen en sociaal leren te stimuleren. Studenten hebben binnen het Microsoft Teams-platform toegang tot leermateriaal zonder over te hoeven schakelen op een browser. Neem contact op met uw CSAM voor de bèta-release van Adobe Learning Manager-app op MS Teams.

### Bugfixes in deze update

**Cursus**

* Een Aangepaste auteur kan geen voorbeeld bekijken van een module wanneer de cursus de status &#39;UNDER_CONSTRUCTION&#39; heeft. De reactie toont Fout 404.
* De titel van de cursus op de pagina Cursus/Toevoegen van een auteur-app loopt over wanneer de titel van de cursus bepaalde tekenlimiet overschrijdt.

**Auteur**

* In de auteur-app overschrijdt de titel van de cursus (indien deze lang is) de paginagrenzen tijdens het maken van een cursus.
* Soms wordt een cursus toegevoegd, zelfs als er geen auteur is geselecteerd.

**Dashboardrapporten**

* Knopinfo wordt mooi weergegeven wanneer de interfacetaal Engels is, maar genereert een consolefout wanneer de interfacetaal anders is.
* Wijzig de naam &quot;Verplicht&quot; in &quot;Vereist&quot; in het Studentendashboard.

**Docent-app**

* De tijdnotatie in de docent-app is niet consistent met de andere apps.

**Sociaal**

* Voor bepaalde typen berichten opent het sociale board na het plaatsen niet zoals verwacht.

**Beheer**

* Een gebruiker met een aangepaste rol kan geen resources downloaden wanneer deze een voorbeeld van de cursus bekijkt.

**E-mailsjablonen**

* Wanneer een student zich uitschrijft bij een Leerprogramma dat een Klaslokaal-/VC-cursus bevat, ontvangt hij/zij geen annulerings-e-mail.

**Taakhulpen**

* U kunt de naam van de cursus niet zien op de widget Taakhulp.

**Publiceren**

* De modulebeschrijving die is toegevoegd in Adobe Captivate is niet zichtbaar in Learning Manager wanneer de module wordt gepubliceerd in ALM.

**Actieve velden**

* Wanneer een CSV met een groot aantal verslagen in proces is, vergt het een significante hoeveelheid tijd, waarin, als een gebruiker het programma opent en een waarde voor één van de attributen ingaat, het tot een nieuwe gebruikersgroep kan leiden die in fouten CSV zou kunnen resulteren. Om dat te verhelpen, wordt het pop-upbericht voor het kenmerk Actieve velden uitgeschakeld en wordt het opnieuw ingeschakeld zodra het CSV-uploaden is voltooid. Dit bericht wordt weergegeven wanneer de CSV-bestanden worden geïmporteerd.
* Als de kolom in het CSV-bestand van Gebruikers dezelfde naam heeft als het actieve veld voor externe gebruikers, mislukt het uploaden van de CSV.

**API-gerelateerde oplossingen**

* In de learningObjects-reactie ontbreekt het bladwijzerattribuut.
* Er wordt een toegangsinvoer gemaakt tijdens het genereren van een oauth-vernieuwingstoken voor verwijderde gebruikers.
* De LO-API retourneert een onjuiste loFormat, omdat er voor de berekening van het cursustype samen met de kerninhoud rekening is gehouden met voorbewerkingsmodules.

**Bekende problemen in deze update**

* De knop Delen in de studentencatalogus werkt niet zoals verwacht in de Safari-browser, de mobiele en iPad MS Teams-app.
* Meldingen worden niet weergegeven op het tabblad Activiteit nadat de app is verwijderd op andere computers.
Er gebeurt niks wanneer u op de meldingen klikt op het tabblad Activiteit van de app op iPhone 14.
* Op de MS Teams-app tonen de Learning Manager-meldingen (voltooid, ingeschreven, deadline en te laat) niet de status en naam van de cursus op het tabblad Activiteit.
* Een pop-upvenster met XML-inhoud wordt weergegeven wanneer de Integratiebeheerder de MS Teams-app niet goedkeurt.
* De taal van de gebruikersinterface op de Adobe Learning Manager-app op MS Teams verandert soms niet zoals verwacht wanneer de taal wordt gewijzigd.
* U kunt niet reageren op de eerste melding wanneer de focus in het Iframe ligt (tabbladen Start en Catalogus).

**Beperkingen van de mobiele app van Adobe Learning Manager**

* Offline inhoud weergeven.
* De raster-/lijstweergave op de pagina Catalogus/Mijn leermateriaal.
* Meerdere pogingen om een cursus te volgen.
* Inschrijvingsdeadline op een cursuskaart.
* Op iOS-apparaten worden pushmeldingen niet weergegeven wanneer de app op de voorgrond staat.
* Diepe links in pushmeldingen worden niet omgeleid naar de bedoelde openingspagina.
* Als u op de knop Interesse tonen klikt, wordt het programma omgeleid naar het web.
* Tijdens het reageren op of het plaatsen van opmerkingen in Sociaal leren, kunt u geen bestand bijvoegen.
* U kunt zich niet aanmelden bij LinkedIn Learning.
+++

+++Update 88

**Releasedatum:** 7 maart 2023

### Prestatieverbeteringen in deze release

Wanneer een bulkinschrijving van studenten wordt uitgevoerd, wordt er geen logbestand gegenereerd voor elke student.
We hebben het verwerken van Leerplannen voor grote accounts geoptimaliseerd. Zo voorkomt u zoekproblemen of vertragingen.
+++

+++Update 87

**Releasedatum:** 1 maart 2023

## In deze update opgeloste bugs

* Een student ontvangt geen e-mail over de sessieannulering als de CR/VC-module uit de ingeschreven cursus is verwijderd.
* Wijzig GetNotificationData van GET naar POST. De oorspronkelijke implementatie heeft de fout veroorzaakt, **IllegalArgumentException: Request header is too large**, wat heeft geleid tot mislukte meldingen.
+++

+++Update: 86

**Releasedatum:** 17 februari 2023

### Fout in deze versie opgelost

In de Learner-app mislukt zoeken naar gebruikers en gebruikersgroepen vanwege bepaalde problemen met taalinstellingen.
+++

+++Update 85

**Releasedatum:** dinsdag 13 februari 2023

### Wat is gewijzigd in deze update

Er is ondersteuning toegevoegd voor vierletterige taalcode tijdens het filteren van talen in GET learningmanagerapi/v2/learningObjects.

### In deze update opgeloste bugs

Voor sommige landinstellingen retourneert de zoekopdracht onjuiste resultaten.
De metadata van de cursus worden overschreven als de cursus meer dan één variant van dezelfde taal heeft.
+++

+++Update 84

**Releasedatum:** vrijdag 2 februari 2023

### Wat is gewijzigd in deze update

**Taakhulpenrapport**

Deze update bevat een nieuw taakhulprapport met alle taakhulpen in het account.

**Versiebeheer**

Er is versiebeheer voor resources toegevoegd wanneer u tijdens het maken van een cursus resources toevoegt.

**Rapport voor pogingen**

U kunt een rapport bekijken waarin staat hoe vaak een student elke training opnieuw heeft geprobeerd en bezocht.

**Module reset API**

Een beheerder kan nu modules herstellen met behulp van de API voor moduleherstel. Ga voor meer informatie naar de [Adobe Learning Manager API-referentie](https://captivateprime.adobe.com/docs/primeapi/v2/).

**E-mailsjabloon**

Voor een aantal e-mailsjablonen kunt u nu een vereiste aan de sjabloon toevoegen.

**Overige wijzigingen**

* U kunt een door de manager goedgekeurde cursus als vereiste toevoegen.
* Verbeterde prestaties bij het vernieuwen van het dashboard met een overzicht van het leermateriaal.
* E-mail-ID&#39;s en account-ID&#39;s worden geverifieerd voordat een terugstuurrapport wordt verzonden.

### BUGS DIE ZIJN OPGELOST IN DEZE UPDATE

* Er worden dubbele auteursnamen weergegeven op de pagina Cursusoverzicht.
* Een hyperlink op de pagina voor het maken van accounts leidde tot Fout 404.
* De landinstellingen voor Tsjechië werden niet zoals verwacht weergegeven in de spelerinstellingen.
* In sommige gevallen worden vaardigheden weergegeven als Niet gedefinieerd voor studenten die bezig zijn of die nog niet zijn gestart.
* De tijd die over meerdere dagen is doorgebracht, laat zien dat er verschillende tijd is doorgebracht in het Studenttranscript en de inschrijvingsrapporten.
* De knop Terug reageert niet voor de beheerders- en beheerdersprofielen in Cursus > L2 Quizscore > Op tabblad Vraag en Aanwezigheid en scores.
* Voor een paar landinstellingen ontbreekt in een e-mailsjabloon inhoud in de hoofdtekst van de e-mail en is de taalvertaling in de sjabloon niet consistent.
+++

+++Update 83

**Releasedatum:** 18 januari 2023

### Wat is gewijzigd in deze update

**Nieuwe kolom**

Een nieuwe kolom, **uitschrijvingToegestaan**, wordt toegevoegd aan course.xlsx. Download het bestand uit deze handleiding.

**LinkedIn Learning-connector**

Voor de LinkedIn Learning-connector staat er een nieuw selectievakje Student kan zich uitschrijven op de pagina Filters. Zie voor meer informatie [LinkedIn Learning-connector](/help/migrated/integration-admin/feature-summary/connectors.md).

### In deze update opgeloste bugs

* Als u de muisaanwijzer op staafdiagrammen plaatst, wordt de knopinfo van het dashboardrapport weergegeven zoals verwacht.
* In Rapporten onder Gebruikersactiviteit geeft het rapport Bestede leertijd onjuiste gegevens voor dagelijkse/maandelijkse gegevens weer.
* In sommige gevallen geeft de grafiek met de quizscore onjuiste waarden weer.
* In een cursus met SCORM-inhoud waarvoor meerdere pogingen zijn ingesteld, wordt de knop Opnieuw bezoeken uitgeschakeld wanneer een student de cursus probeert.
* In sommige gevallen wordt, na het inschrijven van een student voor een cursus en het downloaden van een e-mailcontrolelogboek, de e-mail wel afgeleverd, maar verschijnt deze niet in het logboek.
* De agenda-uitnodiging voor een docent moet de tekstdocent in het onderwerp opnemen.
* Het pictogram Trainingskaart heeft geen betrekking op gerelateerde cursusaanbevelingen en Leerpadkaarten die op de cursusoverzichtspagina staan.
* Voeg een sectie Opgeslagen door mij toe aan de instellingen van de startpagina voor studenten.
* Voor bepaalde accounts wordt een gebruiker om een SSO-login gevraagd voor een account waar een Adobe ID vereist is.
* In tijdzones met zomer- en wintertijd wordt het veld &#39;start_time&#39; berekend op basis van het huidige tijdverschil, niet op basis van het tijdverschil op de werkelijke startdatum en -tijd. Dit veroorzaakt uitnodigingen met onjuiste tijden.
* Als een certificering wordt herhaald, wordt een kopie van de onderliggende cursussen intern in de database gemaakt. Deze cursussen worden dan in zoekacties weergegeven, in tegenstelling tot het verwachte gedrag.
* Als het uploaden van een CSV-bestand niet lukt, ontvangt u geen e-mailmelding.
* Als de namen van de actieve velden nogal lang zijn, verdwijnen de namen bij het slepen en neerzetten. Hierna werkt de knop Opslaan ook niet zoals verwacht.
* Een sessierapport wordt niet geëxporteerd via een cursusdeelname en scorepagina als de eerste gebruiker in het rapport een record heeft in de activiteitsklassetabel met het commentaar als null.
* Als u het beheerdersaccount gebruikt om de badges op te halen, krijgt u de lijst met de verwachte sortering. Maar als u hetzelfde voor een student uitvoert, worden de resultaten niet gesorteerd.
* Als u een cursus kiest uit uw zoekresultaten en vervolgens probeert terug te gaan naar de zoekresultaten met de knop Vorige, verdwijnen de zoekresultaten.
* Niet alle gebruikers worden als docenten in een sessie aan een gebruikersgroep toegevoegd.
* Sjablonen die meerdere gebruikerssjablonen bevatten, hebben een aantal waarden op het onderwerp.
+++

+++Update 82

**Releasedatum:** 15 december 2022

* De GET LO-API bevat nu prijsinformatie, indien beschikbaar.
* Aan LT-rapporten wordt een nieuwe kolom, Voltooid door, toegevoegd. Zo kan de beheerder de voltooiingsbron van een LO beter identificeren.
* We hebben een nieuwe ILT-module toegevoegd die het slagings- en deelnamepercentage van studenten kan bijhouden. Docenten kunnen nu een optie gebruiken om een student te markeren als geslaagd of als deelgenomen maar niet geslaagd.
* Een beheerder kan nu verplichten dat studenten een module moeten afronden en moeten slagen voordat ze doorgaan naar de volgende module/cursus. Dit geldt voor vereisten, bestelde cursussen en LP&#39;s.

**Opgeloste problemen**

* Taalproblemen voor Bahasa in de zijbalk en voettekst van de immersieve mobiele ervaring.
* Er zijn problemen opgelost met de immersieve weergave van de voorbeeldweergave van de module.
* Het zoeken naar een cursus via beheerder en auteur resulteert in een andere landinstelling dan die is ingevoerd.
* Wijzigingen in welkomst-e-mailsjablonen werden niet opgeslagen na het bewerken.
* Gebruikers met verschillende id&#39;s voor e-mail en Adobe konden zich niet aanmelden bij de mobiele app.
* Gebruikers werden verkeerd geïdentificeerd bij deelname aan Zoom- of BJ VC-sessies.
+++

+++Update 81 - november 2022-versie van Adobe Learning Manager

**Releasedatum:** 5 november 2022

**Opmerking:** Met deze versie van Adobe Learning Manager hebben gebruikers met inactieve accounts geen toegang meer tot hun accounts met behulp van subdomeinen. De accounts kunnen worden geopend met de account-id of door de pagina acapindex.html te gebruiken en de e-mail-ID in te voeren.

### Nieuw in deze release

De release van november 2022 van Adobe Learning Manager bestaat uit de volgende verbeteringen:

* Configuratie van meerdere SSO&#39;s
* Ondersteuning voor niet-aangemelde functie
* Verbeteringen in de pagina met trainingsoverzicht
* Speler aanpassen
* Nabootsing van student en manager

Voor meer informatie zie [Nieuw in de Adobe Learning Manager-release van november 2022](/help/migrated/whats-new-2022-november.md).

**Opmerking:** Met de november 2022-versie van Adobe Learning Manager wordt Zoomen afgekeurd [JWT-verificatie in juni 2023](https://marketplace.zoom.us/docs/guides/auth/jwt/). Volgens deze aankondiging werkt de Zoom-connector met JWT tot de genoemde datum, maar wij raden gebruikers aan om een server-naar-server OAuth-app te maken om deze functionaliteit in de accounts te vervangen. Elke nieuwe verbinding beschikt standaard over Zoom OAuth-verificatie.

### Bugfixes in deze update

* Als u als student op een mobiel apparaat een leerprogramma met meer dan 10 cursussen probeert te openen, verschijnt een foutbericht.
* Als voor een cursus een herinnering is ingesteld die n dagen na een gemiste deadline wordt verzonden, wordt de e-mail zoals verwacht na n dagen verzonden maar is het aantal dagen na de gemiste deadline n-1 in plaats van n.
* Een video wordt niet in de speler geladen als L1-feedback voor de cursus is ingeschakeld in de Learner-app en de gebruiker alleen een studentrol heeft.
* Een e-mail met een voltooiingsherinnering geeft niet de tijd weer in de tijdzone van de gebruiker zoals verwacht.
* Studenttranscripten die via dashboardrapporten worden gegenereerd, respecteren de filters niet en geven meer informatie weer dan vereist.
* U kunt geen inhoud selecteren waarin de interfacetaal niet als inhoudstaal is toegevoegd.
* Er werd een onjuiste URL weergegeven wanneer zelfregistratie voor een cursus voor de tweede keer werd uitgevoerd.
* Wanneer een instructeur uit een VC-sessie wordt verwijderd, ontvangt deze geen mail waarin wordt meegedeeld dat de sessie is geannuleerd.
* De tekst &#39;minuut&#39; op een tegel op de trainingspagina van de leerling wordt niet vertaald naar Bahasa Indonesië zoals verwacht.
* Het dashboard Naleving geeft onjuiste gegevens voor niet-conforme studenten weer.
* Tijdens het toevoegen van een rapport kunt u geen cursussen of catalogi selecteren waarvan de interfacetaal niet als inhoudstaal is toegevoegd.
* In deze versie hebben we de volgende inhoudstalen toegevoegd:
   * Bulgaars
   * Vlaams
   * Portugees (Brazilië)

### Bekende problemen in deze update

* In sommige gevallen wordt de grafiek met de quizscore niet weergegeven zoals verwacht. Wanneer u de grootte van de grafiek aanpast, verschijnt er een lege ruimte aan het begin. Bovendien verschijnen niet alle vragen, en onjuiste gegevens worden met tussenpozen weergegeven.
+++

+++Update 80

**Releasedatum:** 20 september 2022

* Aanmeldingsproblemen met de mobiele app in iOS zijn nu opgelost.
* Er is een probleem met niet-bezorgde e-mails opgelost.
* Docenten werden verkeerd op de hoogte gesteld, zelfs voordat ze door studenten werden ingediend.
* Een docent ontvangt een e-mailmelding hoewel een student geen activiteit heeft verzonden.
* Na het maken van een VC-sessie in MS Teams of Adobe Connect ontvangen de docenten geen uitnodigingen voor de sessie.
* Onjuiste status in een leerpad.
* De prestaties van de app zijn verbeterd.
+++

+++Update 79

**Releasedatum:** vrijdag 18 augustus 2022

* Bevestiging agenda-uitnodiging voor ILT-/VILT-sessies werkt nu met Google Agenda.
* Een manager van de winkel kan nu meldingen voor gebruikers onder hen zien, zelfs als ze als manager zijn verwijderd.
* In bepaalde gevallen mislukt het inschrijven en wordt de foutmelding 500 weergegeven.
* In bepaalde gevallen kunt u een virtuele cursusinstantie niet aanpassen voor teams.
* Beheerders en docenten kunnen opmerkingen toevoegen voor gebruikers die nog geen ILT-/VILT-sessies hebben gevolgd.
* Prestatieverbeteringen bij het downloaden van grote rapporten.
* Als een e-mail van een gebruiker wordt teruggestuurd, ontvangt de beheerder een e-mailmelding. De e-mail bevat een link waarop kan worden geklikt om een csv-bestand te downloaden met de lijst van gebruikers wiens e-mail is teruggestuurd. De beheerder kan dan de nodige actie uitvoeren.
   * De e-mail wordt geactiveerd als een e-mail wordt teruggestuurd of verwijderd.
   * Deze e-mail wordt eens per dag geactiveerd voor alle beheerders die aan de lijst zijn toegevoegd.
   * De link verloopt over zeven dagen.
* Er wordt een foutmelding weergegeven als u probeert een reeds geïntegreerd Adobe Connect-account te integreren met een ander Learning Manager-account.
+++

+++Update 78

**Releasedatum:** 4 augustus 2022

### Bugfixes in deze update

* Als u een cursus hebt die een module met een voorvertoning bevat en vervolgens een API gebruikt om de leermiddelen van de cursus op te halen, bevat de reactie geen gegevens van locatie, contentZipUrl en contentStructureInfoUrl.
* Onjuiste reactie na het verzenden van een XAPI-aanvraag van het Swagger-document, waarin de domeinnaam LearningManager is.
* In de map /boards/{id}/posts-API-reactie, wordt de eigenschap &quot;post.attributes.myPoll&quot; weergegeven als een leeg object.
* In sommige gevallen is voor een niet-aangemelde gebruiker de knop Toevoegen aan winkelwagen uitgeschakeld voor sommige cursussen of leerpaden.
* Onjuiste subdomein-URL op de brandingpagina.
+++

+++Update 77

**Releasedatum:** 24 mei 2022

**Opgeloste problemen in deze update:**

* In nieuwe cursussen wordt geen rekening gehouden met de volgorde in de Salesforce-app. Als u de volgorde wijzigt, wordt de cursus niet weergegeven in de bedoelde volgorde.
* Nadat u de instellingen op de klassieke startpagina hebt aangepast en opgeslagen, worden de wijzigingen niet opgeslagen zoals verwacht. Dit gebeurt af en toe.
* Wanneer studenten hun meldingen controleren, wordt HTML-code weergegeven wat een negatieve invloed heeft op de ervaring.
* Op het dashboard wordt de bestede leertijd onjuist weergegeven als nul uur.

## UPDATE: Adobe Learning Manager wordt hernoemd naar Adobe Learning Manager

Dit is een update over een aanstaande wijziging en helpt u zich hierop voor te bereiden.

**Adobe Learning Manager als product zal in juli 2022 worden hernoemd naar Adobe Learning Manager**. Deze strategische inspanning wordt gedaan om de aansluiting van het product op bepaalde bedrijfsprioriteiten beter uit te dragen.

Het productteam neemt alle nodige stappen om ervoor te zorgen dat dit geen effect heeft op uw gebruik van het platform. U kunt het product op dezelfde manier blijven gebruiken. Voor beheerders van het platform is de nieuwe merknaam vanaf juli in bepaalde vensters zichtbaar.

Als onderdeel van deze wijziging worden de toegangs-URL&#39;s voor Leerbeheer beïnvloed.

Als de toegangs-URL voor uw account bijvoorbeeld `https://learningmanager.adobe.com/XYZ`, wordt de nieuwe URL `https://learningmanager.adobe.com/XYZ`.

Alle bestaande URL&#39;s blijven werken.

Werk samen met de IT-afdeling van uw organisatie om deze actie te voltooien. Neem voor meer informatie contact met ons op via `learningmanagersupport@adobe.com`.
+++

+++Update 76

**Releasedatum:** donderdag 20 april 2022

* Oplossingen voor productterminologie in een paar dashboardrapporten.
* Een dubbele schuine streep (&#39;//&#39;) in de URL van een eindpunt resulteerde in validatiefouten.
* Na het vernieuwen van een pagina werd er verkeerde informatie weergegeven in de velden voor voltooiingspercentage en laatst bezocht.
* De manier waarop de waarde Certificaat of een leerplan wordt berekend, is op bepaalde punten aangepast.
* Een aangepaste beheerder kon alle gebruikers als docenten toevoegen, ook al mocht hij/zij slechts één gebruiker toevoegen.
* Er werd een verkeerde voltooiingsdatum weergegeven op een badge-pdf.
+++

+++Update 75

**Releasedatum:** woensdag 29 maart 2022

* In sommige gevallen wordt na het kopiëren van het onbewerkte CSV-bestand op de FTP-locatie de gebruikersimport niet uitgevoerd zoals verwacht en worden er meerdere foutmeldingen weergegeven.
* In eerdere releases van Learning Manager moest u voor het configureren van een Zoom-connector eerst Exavault FTP configureren voor het kopiëren van het CSV-bestand. In deze release wordt de FTP-connector niet meer gebruikt voor het CSV-bestand en daarom hoeft u niet eerst de FTP te configureren.
+++

+++Update 74: Learning Manager AWS India-instantie

**Releasedatum:** woensdag 15 februari 2022

### Overzicht

An [instantie](https://learningmanagerapac.adobe.com/acapindex.html) van Learning Manager wordt nu gehost op AWS in Mumbai (ap-south-1). Voor klanten die dit Indiase exemplaar gebruiken, worden de persoonlijk geïdentificeerde informatie (PII) en de leerrecords van gebruikers alleen in India opgeslagen.

### Wat wordt ondersteund

De India-instantie van Adobe Learning Manager heeft dezelfde functiemogelijkheden als andere instanties, zoals die in de EU en VS. Er zijn enkele functies die niet worden ondersteund in de India-instantie. Dit zijn:

* Creditcard betaling voor aankoop van licenties
* Creative Cloud-inhoudscatalogus
* Slack-app
* **&#42;** Wachten op certificering voor SOC2-compatibiliteit

### Veelgestelde vragen

**Hoe verschilt deze instantie in Mumbai van andere omgevingen met alleen AWS?**

Er is geen verschil. De instantie in Mumbai is hetzelfde als de [AWS US](http://learningmanager.adobe.com/)- of [AWS EU](http://learningmanagereu.adobe.com/)-instantie. Deze instantie wordt in India gehost en alle leer- en gebruikersgegevens blijven in India. De volgende functies worden ondersteund in de India-instantie:

* Creditcard betaling voor aankoop van licenties
* Creative Cloud-inhoudscatalogus
* Slack-app
* **&#42;** Wachten op certificering voor SOC2-compatibiliteit

**Zal dit milieu gemeenschappelijk Kader van Controles (CCF)-Volgzaam zijn?**

Ja. De nieuwe instantie voldoet aan Common Control Framework (CCF).
+++

+++Update 73

Releasedatum: 05 februari 2022

* Ondersteuning voor e-mailsjablonen is nu beschikbaar voor inhoudstalen, waaronder Hongaars en Fins.
+++

+++Update 72 - januari 2022-versie van Learning Manager

Releasedatum: 28 januari 2019

### Nieuwe functies en wijzigingen

* Locaties van klaslokalen toevoegen
* Gamificationwijzingen
* Microsoft Teams-connector
* API-wijzigingen
* Mobile Immersive-webwijzigingen

<!--
For more information, see What's new in the [**January 2022 release of Adobe Learning Manager**](../whats-new.md).
-->

### Bugs die hersteld zijn in deze versie

**Inhoudsbibliotheek**

* Het zoeken naar inhoudsbestanden in mappen met persoonlijke inhoud werkte niet voor gebruikers met aangepaste rolbevoegdheden. Dit is nu opgelost.

**Cursussen**

* Verwijderen van een cursus of leerpad was niet mogelijk als ze een historische associatie hadden met een leerplan. Dit is nu opgelost. Gebruikers kunnen nu een cursus of leerpad verwijderen als deze niet aan een leerplan zijn gekoppeld.
* Als u een voorbeeld van een cursus of leerpad bekijkt en het bronbestand een lange naam zonder spaties heeft, loopt de bestandsnaam niet terug zoals verwacht en loopt deze over op de volgende regel. Dit probleem is opgelost.
* In het geval van een virtuele lesruimte kon u eerder een module maken zonder daar een VC-conferentiesysteem te selecteren omdat in een nieuwe instantie VC URL niet de vereiste informatie had. Dit wordt nu vermeden door een foutbericht in het ontwerpstadium van de module waarin u wordt gevraagd het VC-conferentiesysteem op te geven voordat u de module kunt opslaan.
* Op de wachtlijstpagina werd een misleidend bannerbericht voor geregistreerde gebruikers weergegeven, dat nu wordt verwijderd.
* Bij bulkuitschrijving voor cursussen werd het pop-upvenster voor het invoeren van e-mailadressen niet weergegeven. Dit probleem is nu opgelost.
* De optie om e-mail naar studenten te sturen vanaf het tabblad Aanwezigheid en scores in de app voor beheerders en docenten sloot niet-geselecteerde studenten niet uit nadat alles is geselecteerd. Daarom stuurde Learning Manager e-mails naar alle studenten. Dit probleem is nu opgelost.
* Het inschrijvingsrapport wordt weergegeven als &quot;Niet gestart&quot;, ook al heeft een student de cursus al voltooid.

**SSO**

* In opstelling SSO, als entiteitsidentiteitskaart om het even welke belangrijke of trainingsruimten had toen login configuratie niet werkte, wordt dit nu behandeld als deel van de moeilijke situatie.

**Aankondigingen**

* Als beheerder werden de begin- en einddatums voor een aankondiging niet opgeslagen als de interface- en inhoudstaal was ingesteld op Deutsch/Espanol. Dit probleem is nu opgelost.

**E-mailsjabloon**

* Sessieuitnodigingen die meerdere dagen beslaan, waarbij de uitnodigingen niet de juiste informatie weerspiegelen op dagen, worden geblokkeerd door sommige e-mailclients. Dit is nu opgelost.
* De variabele &#39;Venue Name&#39; ontbrak in de e-mailsjabloon &#39;Herinnering voor aanstaande sessie&#39; voor studenten met een Duitse landinstelling. Dit is nu toegevoegd.
* De link om een account aan te maken als onderdeel van de welkomstmail aan de gebruiker hield geen rekening met de landinstellingen voor de gebruiker. Dit is nu opgelost.

**E-mailherinneringen**

* Als studenten waren ingeschreven voor een training via een leerplan, werden de e-mails met herinneringen voor voltooiing meerdere keren verzonden op basis van het aantal bewerkingen dat was aangebracht in de voltooiingsdatums van hetzelfde leerplan. Dit probleem is nu opgelost.

**Gebruiker**

* Het bericht dat aan gebruikers wordt getoond wanneer zijn/haar account inactief/geschorst is verbeterd om hun beheerder te bereiken dat hun accounts opnieuw worden ingeschakeld.

**Activiteit**

* Een docent kon de inzendingen van de student niet bekijken als de naam van het ingezonden bestand een speciaal teken bevatte. Dit is nu opgelost.

**Rapporteren**

* Een beheerder kon het cursusinschrijvingsrapport niet downloaden als het een student bevat die indirect is ingeschreven voor deze cursus via een flexibel leerpad, maar nog een instantie voor deze cursus in een leerpad moet kiezen. Dit probleem is nu opgelost.
* Het herschikken van rapporten in het dashboard Rapporten voor beheerder- en managerrollen bleef de status van de rapportvolgorde niet behouden. Dit probleem is nu opgelost.

**Inhoud**

* Audio in trainingsinhoud werd niet automatisch afgespeeld in de voorvertoning als studentenmodus vanwege het automatisch afspeelbeleid van de browser. Dit probleem is nu opgelost voor ondersteunde browsers, behalve Safari.

**Gamification**

* Als een externe student in hetzelfde account is omgezet als interne student, heeft hij/zij geen toegang tot het leaderboard voor gamification in de Learner-app. Dit probleem is nu opgelost.

**Speler**

* De speler gaf geen waarschuwingsbericht weer wanneer de gebruiker naar modules probeerde te gaan in een cursus op volgorde met AICC-type modules. Dit is nu opgelost.
* Voor bepaalde verworven cursussen werkte het afspelen van videomodules in headless LMS niet voor sommige gebruikers. Dit probleem is nu opgelost.

**Managerdashboard**

* Een manager kan het rapport voor zijn directe team niet exporteren van de pagina met teamvaardigheden van het Managerdashboard. Dit probleem is nu opgelost.

**Publiceren**

* In de European instance of Learning Manager content die rechtstreeks vanuit Adobe Captivate naar Adobe Learning Manager werd gepubliceerd, werd standaard gepubliceerd in de landinstelling Deutsch. Dit is nu opgelost.

**API**

* Het veld Duur wordt nu toegevoegd aan het taakhulpmodel.
* Voor de aanbeveling-API&#39;s retourneert een verzoek van een GET soms Error 500.
* Wanneer u trainingen migreert via Exavault en als de tekst niet-Engelse tekens bevat, werd deze altijd bijgewerkt met extra tekens in de tekst. Dit probleem is nu opgelost.

**Lokalisatie**

* `NormalTextRun  BCX0 SCXW38820519 For the`Admin-, auteur- en Learner-apps, sommige inhoud in het Duits wordt niet weergegeven zoals verwacht.

## Bekende problemen in deze release

* Op de pagina Sociaal leren kunt u bij het maken van een bericht geen audio opnemen of de audio uploaden nadat u op de microfoonknop hebt getikt. Dit is een beperking van de browser.
* In iOS worden H264- en WMA-audiobestanden niet ondersteund in de mobiele browser.
* De voortgang wordt niet gemarkeerd voor studenten met een + in hun e-mailadres. Dit is nadat ze een VC-cursus in Microsoft Teams hebben gevolgd.
* In de mobiele Safari-browser kunnen studenten geen bestanden uploaden die groter zijn dan 200 MB in Sociaal leren. Dit is een browserbeperking.
+++

+++Update 71

Releasedatum: 17 november 2021

### Training delen met managers

Learning Manager biedt het dashboard Naleving aan alle beheerders en managers. Managers vinden het zeer nuttig om naleving van hun teamleden voor een bepaalde opleiding te volgen. Tegelijkertijd willen beheerders dat alle managers compatibiliteitstrainingen toevoegen aan hun dashboard en deze bijhouden.

In Learning Manager wordt de **Delen met managers** Met deze workflow kunnen beheerders training delen met managers, zodat ze kunnen worden toegevoegd aan het dashboard Naleving van een manager. Managers hoeven dus geen actie te ondernemen en kunnen meteen beginnen met het volgen van de naleving.

Zie voor meer informatie  [**Training delen met managers**](../administrators/feature-summary/reports.md#share_training_managers).

### Bugfixes in deze update

* Als er twee accounts zijn en de uitgebreide functie Leerpad uitgeschakeld is, en er een gedeelde catalogus is van het eerste account naar het andere, dan heeft het Leerpad in het tweede account dubbele secties op de cursuspagina.
* Door een aangepaste FTP wordt nu ook sftp:// ondersteund, naast http:// en https://
* In de Exavault-connector worden nu API&#39;s van versie 2 gebruikt.
* De kwaliteit van video&#39;s was soms suboptimaal. Dit probleem is nu opgelost.
* Zelfs nadat een student een verplichte cursus voltooid heeft en de manager goedkeuring heeft gegeven, blijft de status van de certificering In afwachting van goedkeuring.
* Als de namen van auteurs geaccentueerde tekens bevatten, mislukt de migratie van de cursus.
* Als er in het actieve veld waarden in hoofdletters staan, wordt het actieve veld niet naar verwachting opgeslagen.
* Kan leerpaden niet filteren op basis van vaardigheden.
* Wanneer een beheerder een instantie aanmaakt en een nieuwe sessie toevoegt, ontvangt een docent geen uitnodigings-e-mail voor de sessie. Dit probleem treedt op in Zoom VC-cursussen.
+++

+++Update 70

Releasedatum: 28 oktober 2021

### Bugfixes in deze update

* In bepaalde gevallen wordt de informatie over een leerpad niet weergegeven in een studenttranscript.
* De tekst in het dialoogvenster **Voltooiing markeren** is bijgewerkt om aan te geven dat de actie niet-omkeerbaar is.
* De Leerobjecten-API heeft in sommige gevallen een fout met metadata gegeven.
+++

+++Update 69 - oktober 2021-versie van Learning Manager

**Releasedatum:** 9 oktober 2021

### Leerpad

De **Oktober 2021-versie van Adobe Learning Manager** introduceert het concept leerpaden.

>[!NOTE]
>
>De **Instellingen > Algemeen** Deze pagina heeft een nieuwe optie om de uitgebreide mogelijkheden van leerpaden in te schakelen. Als deze optie is ingeschakeld, kunt u leerpaden toevoegen aan een ander leerpad. U kunt de optie niet wijzigen als deze eenmaal is ingeschakeld.

Leerpaden vervangen onze bestaande functie van leerprogramma&#39;s. Stel je leerprogramma&#39;s voor die krachtige verbeteringen krijgen zonder dat je bestaande mogelijkheden kwijtraakt. Bovendien wordt de functie gemarkeerd als een leerpad.

Zie voor meer informatie [***Leerpaden***](../administrators/feature-summary/learning-paths.md).

### Andere wijzigingen

* Nieuwe Salesforce-app
* Inhoudshub
* Wijzigingen rapportage
* Overzichtsrapport van de sessie
* Wijzigingen TOC Player
* API-wijzigingen
* Connectorgerelateerde wijzigingen

Zie voor meer informatie [***Nieuw in de Learning Manager-release van oktober 2021***](../whats-new.md).

### Bugfixes in deze update

* E-mailsjablonen, zoals Cursusuitschrijving, Uitschrijving van leerprogramma of Uitschrijving van certificering, weerspiegelen niet de nieuwste productterminologieën zoals gedefinieerd in de CSV. De standaardtekst in e-mailsjablonen ondersteunt nu aangepaste terminologieën.
* De gebruikerstaal in Learning Manager wordt niet ondersteund in de workflow Publiceren naar Learning Manager. Als de gebruikerstaal anders is, wordt Publiceren naar Leermanager in het Engels uitgevoerd.
* Als u veel catalogi toevoegt aan een aangepaste rol, treedt er een fout op wanneer u de rol bijwerkt. Nu wordt de limiet van het aantal catalogi verhoogd tot 50 catalogi.
* In sommige gevallen zijn verwijderde trainingen nog steeds zichtbaar in een catalogus. Dit probleem deed zich alleen voor in de beheerdersapp en is nu opgelost.
* Wanneer de beheerdersrol van de ene gebruiker naar de andere gebruiker wordt gewijzigd, wordt de beheerdersrol van de vorige gebruiker nog steeds weergegeven in de gebruikersinterface. Dit is nu opgelost. Dit probleem is alleen aanwezig voor externe gebruikers en niet voor interne gebruikers.
* In sommige specifieke scenario&#39;s is het importeren mislukt voor een grote groep gebruikers die worden geïmporteerd via gebruikers-CSV. Dit probleem is nu opgelost.
* Een leertranscript geeft de voltooiingsdatum voor een extern certificaat niet weer als een verplichte cursus wordt toegevoegd nadat een extern certificaat is gemaakt en een gebruiker ervoor is ingeschreven. Dit is nu opgelost.
* Een certificaat geeft de gelokaliseerde naam van de student niet weer zoals verwacht. Dit is nu opgelost.
* Bij Zoom VC-sessies ontvangt een docent niet altijd de uitnodiging voor de sessie. Dit is nu opgelost. De docent ontvangt nu de vereiste communicatie.
* Een student ontvangt geen uitnodigingen voor een sessie als sjablonen op cursusniveau zijn ingeschakeld, maar sjablonen op accountniveau zijn uitgeschakeld. Dit is nu opgelost.
* Voor specifieke tijdzones kwamen e-mailherinneringen een dag later aan dan verwacht. Dit is nu opgelost.
* Studenten ontvangen geen e-mails met meldingen over sessies als bepaalde e-mailsjablonen zijn uitgeschakeld.
* In het geval dat een BlueJeans-vergadering wordt bijgewerkt door auteurs, beheerders, werd de URL van de BJ-vergadering onbruikbaar. Dit is nu opgelost.
* Bij het uitvoeren van de GET/LO-API worden in sommige gevallen de cursussen die deel uitmaken van een leerprogramma niet geretourneerd.
* Als de student inhoud probeert te uploaden waarvan de naam een spatie bevat, komt de student een interne serverfout tegen.
* Badge-PDF&#39;s die voor studenten werden gegenereerd, hadden opmaakproblemen wanneer ze werden gegenereerd in een niet-Engelstalige landinstelling. Dergelijke problemen zijn nu opgelost.
+++

+++Update 68

Releasedatum: 28 september 2021.

### Bugfixes in deze update

* Op de mobiele browser zijn diepe links ingeschakeld voor het volgende:

   * Alle boards
   * Openbare boards en posts
   * Privéboards en posts met toegang
   * Privéboards en posts zonder toegang
   * Beperkte boards en posts
   * Opmerking bij post
   * Reactie op opmerking
   * Socialemediaprofiel gebruiker

* Voor accounts die een aangepast domein gebruiken, toont de Learner-app geen favicon.
* Op AEM verwijdert de Learning Manager-component de configuratie van andere componenten.
* De helppagina voor de AEM-component verwijst naar een onjuiste locatie.
* Extern ophalen en opslaan van e-mails/tokens van gebruikers zodat gebruikers hun eigen back-end voor opslag kunnen implementeren in plaats van AEM gebruikersknooppunten te gebruiken.
* Bij het bewerken van een tekstbeschrijving in Cursussen, Leerprogramma&#39;s, Certificaten en Taakhulpen wordt er een waarschuwingsbericht getoond.
* De rapporten van het Manager Dashboard worden niet gedownload als een gebruiker zowel aangepaste als managerrollen heeft.
* Een e-mailsamenvatting toont onjuiste waarde voor trainingsactiviteit.
* In sommige gevallen gedraagt Learning Manager zich onvoorspelbaar als u van de marktplaats voor inhoud naar de Studentpagina gaat.
* In de Sociaal-app werken de filters niet zoals verwacht in de lijstweergave.
* De e-mailverwelkoming die interne gebruikers ontvangen, wordt ook door externe gebruikers ontvangen.
* Learning Manager-widget toegevoegd aan paginasjabloon in AEM.
* Als u een certificaat opnieuw wilt publiceren na het verwijderen van een cursus, mislukt dit.
* Studenten ontvangen geen e-mails met sessiedetails.
+++

+++Update 67 - Updates voor Azure

Deze update introduceert een nieuwe instantie van Azure.

>[!NOTE]
>
>De volgende functies worden niet ondersteund in de instantie:
>
>* [Aangepast domein](../custom-domain.md)
>* [Aankoop creditcard](../administrators/feature-summary/billing-management.md)
>* [Inhoudscatalogus](../administrators/feature-summary/content-catalogs.md)

+++

+++Update 66 - Augustus 2021-versie van Learning Manager

De **Augustus 2021** **release van Adobe Learning Manager** is gericht op het verbeteren van de leerervaring, rapportage en administratieve workflows. Een aantal belangrijke punten zijn:

* **Contentmarktplaats:** Learning Manager biedt nu meer dan 70000 cursussen op verschillende domeinen, zoals Technologie, Beheer, Leiderschap, enzovoort.
* **Verbeterde toegankelijkheidsondersteuning:** Toegankelijkheidsondersteuning voor de studentrol versterkt via verbeterde toetsenbordnavigatie, mogelijkheden voor schermlezers en compliance met contrastverhouding.
* **RTF-opmaak:** Learning Manager biedt nu uitgebreide tekstbewerking voor beschrijvingen in cursussen, programma&#39;s, certificaten en taakhulpen. Op deze manier kunnen auteurs beschrijvingen in tekst met opmaak opgeven, zoals hyperlinks, afbeeldingen en andere tekstopmaakopties, in plaats van tekst zonder opmaak.
* **Sterrenclassificatie:** Een student kan nu een cursus beoordelen op een schaal van 5 punten. Een beheerder kan kiezen uit een bestaande effectiviteitsscore of een classificatie van 5 sterren.
* **Badgr-integratie:** Studenten kunnen Leermanager nu toestaan om badges die ze in Leermanager hebben verdiend, automatisch naar hun Badgr-account te pushen, vanwaar ze hun badges in hun sociale netwerken kunnen delen.
* **Leergebeurtenissen exporteren naar Salesforce:** Learning Manager biedt nu de mogelijkheid om bepaalde specifieke gebeurtenissen in Learning Manager te exporteren, zoals toevoeging, inschrijving en voltooiing van nieuwe gebruikers, naar een Salesforce-tenant, en biedt de mogelijkheid om deze te koppelen aan het juiste gebruikersobject of Contact-object in Salesforce.

Voor meer informatie zie [***Nieuwe functies en wijzigingen in de Learning Manager-release van augustus 2021***](../whats-new.md).


**Releasedatum:** 7 augustus 2021

### Bugfixes in deze update

**Leerervaring**

* Als een student is toegevoegd aan twee gebruikersgroepen en er een leerplan wordt toegevoegd, wordt de student ingeschreven voor een andere instantie van dezelfde cursus.
* Na het inschrijven voor een cursus, speelt de inhoud in sommige situaties niet af zoals verwacht.
* De cursusbeschrijving toont HTML-tags. Dit is nu opgelost.
* Als u op een post in een social-board reageert met meerdere regels, wordt de opmerking op één regel weergegeven. Dit is nu opgelost.

**Auteurs**

* In sommige situaties met automatische inschrijvingen ontvangen studenten meerdere inschrijvingsmails.

**Rapportage**

* Als de interface wordt ingesteld op bepaalde niet-Engelse talen, worden Studenttranscripten niet gegenereerd zoals verwacht.
* Mogelijkheid om de voortgang van een cursus opnieuw in te stellen binnen een Leerprogramma en Certificering.
* Als een CSV actieve velden bevat met dezelfde naam maar met andere hoofdlettergevoeligheid, produceert de CSV een uitzondering.

**Overige**

* De optie om scores en opmerkingen te bewerken moet worden uitgeschakeld als er geen student is geselecteerd of als de aanwezigheid van de geselecteerde student niet is gemarkeerd.
* Waarden in actieve velden worden in kleine letters weergegeven in het dialoogvenster Gebruiker bewerken, hoewel een gebruiker de waarden eerder in hoofdletters heeft toegevoegd.
* Mogelijkheid voor beheerders en managers om cursussen in afwachting van goedkeuringen te bekijken. Hierdoor kan het management ervoor zorgen dat managers het leren en trainen van werknemers volgen en kunnen beheerders van leerprogramma&#39;s cursusinschrijving goedkeuren als dat nodig is.
* Een gebruiker met een auteur- of aangepaste beheerders-/auteurmachtiging kan een taakhulp die door een andere gebruiker is gemaakt, niet bewerken.
* Wanneer de gebruiker vanuit de beheerdersrol naar Cursus > Instantie navigeert en voor een instantie de optie &#39;Ingeschreven studenten&#39; selecteert, toont deze eerder de studenten uit &#39;Standaardinstantie&#39;. De beheerder moest handmatig de instantie wijzigen in het dropdown-menu. Nu navigeert Leermanager correct de gebruiker naar de studentenpagina met de juiste instantie geselecteerd.

**Apparaatapp**

* Op Android- en iPhone-apparaten kan een student op willekeurige momenten geen cursusmodules openen. Dit leidt tot een 401-fout (geen toegang).
* Een student kan twee QR-codes scannen, maar bij het scannen van de derde QR-code wordt een foutmelding weergegeven.
* Op sommige Android- en iOS-apparaten wordt een bestand niet geopend zoals verwacht voor sommige gedownloade cursussen.
* Als u een taakhulp probeert te openen, wordt er een foutmelding weergegeven.
* De apparaattoepassing reageert onverwacht wanneer een leerprogramma offline wordt gevolgd.
* Wanneer een student weer online gaat en de toepassing opent, loopt deze vast op het opstartscherm.
* Wanneer een gebruiker weer online is, schakelt de app soms over naar de klassieke weergave.
* Wanneer een cursus offline wordt gevolgd, wordt de voortgang soms niet opgeslagen.
* Soms wordt een cursusnaam niet direct weergegeven zoals verwacht als de naam lang is.
* Op de cataloguspagina worden de cursussen niet gesorteerd zoals verwacht.
+++

+++Update 65

Releasedatum: juli 2021

### Bugfixes in deze update

* Problemen met aanmelden voor gebruikers.
* Het e-mailsjabloon Cursusinschrijving voor Manager geeft niet de deadline voor voltooiing van de cursus weer als de variabele aan het sjabloon is toegevoegd.
* TLS 1.0 en TLS 1.1 zijn verouderd.
* Problemen met AVG-gegevensverwijdering voor een gebruiker.
+++

+++Update 64

Releasedatum: juli 2021

### Bugfixes in deze update

* Er wordt een melding voor inschrijving verzonden naar studenten die al zijn ingeschreven voor een cursus.
* Wanneer een aangepast certificaat is genereerd als een badge, wordt in het Duits de datumnotatie niet ondersteund.
+++

+++Update 63

Releasedatum: juni 2021

### Bugfixes in deze update

* U kunt een gebruiker met een lege naam maken in een csv.
* Als het teken &#39;/&#39; in het actieve veld staat, verandert de status van de taak niet van &#39;Ingediend&#39; naar &#39;Voltooid&#39; wanneer een taak wordt gemaakt voor het downloaden van user.csv.
* Bestelde modules houden zich niet aan de volgorde.
* Als een externe auteur verwijderd is, is de cursus die door de auteur is gemaakt niet meer beschikbaar.
* Zoeken naar een Leerobject met meer dan één vaardigheid levert onverwachte resultaten op.
+++

+++Update 62

Releasedatum: juni 2021

### Bugfixes in deze update

* Kan niet aanmelden bij de app wanneer de SP-aanmelding voor het account is geïnitieerd.
* Video&#39;s worden niet zoals verwacht weergegeven van Brightcove.
* De userGroupInfo-API is niet zichtbaar tijdens een bezoek aan het leerprogramma in een van de apps.
* Kan niet zoeken naar een gearchiveerd Leerprogramma en certificering wanneer een Dashboardrapport wordt gemaakt.
* Een auteur kan een Taakhulp die is gemaakt voor een andere auteur, niet bewerken of bijwerken.
* De API voor bestand verzenden werkt niet zoals verwacht in het EU-cluster.
+++

+++Update 61

Releasedatum: mei 2021

### Bugfixes in deze update

* Prestatieverbetering voor userGroupInfo-aanroepen.
* Na het inschakelen van nieuwe Helderheidsprofielen ondersteunt Learning Manager inhoud met video- en audiomodules.
* De gegevens vastleggen in Leertranscripten mislukt als een krap datumbereik wordt geselecteerd.
* Er wordt een sessie-uitnodiging verzonden naar de ingeschreven studenten voor alle sessies, zelfs wanneer er slechts één nieuwe sessie wordt toegevoegd.
* Audiomodules worden niet zoals verwacht geüpload.
+++

+++Update 60

Releasedatum: april 2021

### Bugfixes in deze update

**Rapporteren**

* Als u zoekt naar een gearchiveerd rapport na het maken van een rapport, mislukt dit.
* Fouten in één rapport worden doorgegeven aan andere rapporten. Het resultaat is dat deze rapporten tot fouten leiden.

**Taakhulpen**

* Na het downloaden van een Taakhulp kunt u de Taakhulp niet verwijderen.

**Speler**

* WebVTT-ondertiteling wordt niet weergegeven zoals verwacht.

**Learner-app**

* Op de pagina Overzicht van certificering wordt bij Externe certificering niet de duur weergegeven die is toegevoegd door een auteur.
* De optie toevoegen **Alles** in het filter Vaardigheid.
* Studenten hebben meerdere overzichtsmails ontvangen.
* Het aantal geselecteerde rijen wordt niet zoals verwacht aangegeven op een pagina.

**AEM**

* Widgets worden niet zoals verwacht bijgewerkt na het vernieuwen van een pagina.

**Lokalisatie**

* Een aantal Duitse tekenreeksen zijn niet gelokaliseerd zoals verwacht.
* De vertaling van tekenreeksen gaat standaard naar Engels als een student geen taal heeft geselecteerd voor de interface en inhoud.

**Certificering**

* Het bestellen van de module kan worden omzeild als de vereisten niet worden afgedwongen.

**Browser**

* Auteur-, manager- of studentapps worden niet zoals verwacht weergegeven in IE 11.

**Gamification**

* Gamificatiepunten worden niet zoals verwacht verzilverd.

**Inhoudsbibliotheek**

* Cursussen uit de app voor inhoud testen werken niet zoals verwacht.

**Speler**

* De speler wordt alleen geladen in de ruimte waar de widget zich bevindt.
* Video&#39;s in een Captivate-module worden niet zoals verwacht afgespeeld.

**Connector**

* In bepaalde gevallen worden bestanden verwijderd van een FTP-/Box-connector.
* Bestanden worden verwijderd van een ftp wanneer de bestanden worden bijgewerkt met dezelfde namen.
* Een BlueJeans-gebeurtenis ondersteunt paginering wanneer het aantal gebeurtenissen groter dan 100 is.

**Update 3.3 voor mobiele app - maart 2021**

Releasedatum: 26 maart 2021.

### Nieuwe functies en wijzigingen {#whatsnewandchanged}

Captivate Learning Manager Mobile App-update 3.3 introduceert een gloednieuwe startpagina die mastheads en op AI gebaseerde trainingsaanbevelingen ondersteunt. Deze startpagina is beschikbaar voor alle accounts die zijn geconfigureerd voor de nieuwe optie Immersive Layout. Voor de accounts die zijn geconfigureerd met de klassieke lay-out, wordt de klassieke/verouderde startpagina nog steeds weergegeven. Zij zullen geen veranderingen in de startpagina opmerken.

Bovendien kunnen studenten met deze update ook hun badge als PDF en een afbeelding downloaden. De update introduceert ook een pop-up met feedback, waarmee studenten anoniem feedback over de app kunnen geven.

Zie voor meer informatie  [Apparaatapp van Learning Manager](../learners/feature-summary/ipad-android-tablet-users.md).

Lees verder om hier meer over te weten te komen.

#### Nieuwe startpagina.

Voor alle accounts waarvoor de optie Immersive Layout ingeschakeld is, is er een gloednieuwe startpagina die de configuratie van Immersive Layout ondersteunt.

#### Feedbackbeoordeling

In deze release vraagt Leermanager de gebruiker om feedback te geven over de ervaring die de mobiele app heeft opgedaan.

#### Badge downloaden

Deze update biedt studenten de mogelijkheid om hun badges te downloaden als een PDF-bestand of een Image-bestand.

<!--## Previous update releases {#previousupdatereleases}-->
+++

+++Update 60 - Februari 2021-versie van Learning Manager

Releasedatum: 20 februari 2021

### Nieuwe functies en wijzigingen {#Whatsnewandchanged-1}

* Board-weergave in sociaal.
* De social-banner aanpassen
* Catalogusfilters in Student-app.
* Uitschrijven uit een training
* Gebruikers importeren van Salesforce-contacten.
* ... en nog veel meer.

Voor meer informatie zie [Nieuw in de Learning Manager-update van februari 2021](../whats-new.md).

### Bugfixes in deze update {#bug-fixes}

**Certificering**

* In sommige gevallen kon een student een cursus, die deel uitmaakt van een certificering, niet opnieuw proberen, ondanks dat het maximum aantal pogingen voor de cursus op oneindig is gezet. Dit probleem is nu opgelost.
* In sommige gevallen kan een student zich niet inschrijven voor een certificering vanwege de **Inschrijven** niet zichtbaar zijn zoals verwacht.

**Inhoudsbibliotheek**

* Onjuiste help-URL op de pagina **Voeg nieuwe inhoud** toe. De juiste URL is bijgewerkt.

**Cursus**

* Een L2 Quizscore-rapport dat voor een AICC-inhoudsmodule is gedownload, geeft een onjuiste score weer onder de kolom Totale gebruikersscore/Quizscore. Dit probleem is opgelost.
* Bronnen van een cursus downloaden werkte niet als deze vanuit een andere cursus worden gedupliceerd als de student geen toegang had tot de oorspronkelijke cursus die werd gebruikt om een dubbele cursus te maken.
* Bannerafbeeldingen waar deze niet worden verwijderd wanneer de auteur deze verwijdert terwijl de cursus in de conceptstatus staat. Dit probleem is opgelost.

**AEM**

* Na het invoegen van de Learning Manager-component in AEM, duurde het lang voor de pagina geladen was, waardoor de andere componenten niet meer toegankelijk waren. Dit probleem is opgelost.

**Beheer**

* Gearchiveerde cursussen worden niet zoals verwacht weergegeven in de zoekresultaten. Dit probleem is opgelost.
* Beheerder kan niet zoeken naar gearchiveerde cursussen in **Admin-app** -> **Aangepaste rapporten** -> **Excel-rapporten** -> **Cursusrapporten**, die nu is opgelost.

* Het downloaden van een quizrapport als Excel werkt niet als het bestand studenten bevat die de trainingen hebben gevolgd voor en na de inhoudsupdate. Dit probleem is opgelost.
* Een CSV-upload mislukt als de actieve velden speciale tekens bevatten. Dit is opgelost.
* In enkele gevallen, wanneer een student een test aflegt in Captivate, worden de antwoorden niet vastgelegd zoals het hoort.
* Nadat u een abonnement hebt gemaakt en hebt geprobeerd het abonnement te bewerken, kunt u het **Opslaan** en **Annuleren** knoppen worden niet zoals verwacht weergegeven. Dit is opgelost.

**Speler**

* Voor een specifiek type inhoud van het SCORM-2004-cv-scenario werkte niet. Studenten moesten dus naar het punt navigeren waar ze waren opgehouden. Dit is nu opgelost. De inhoud moet nu worden hervat vanaf het punt waar deze eerder werd gebruikt.
* Na het inschrijven voor een cursus wordt de inhoud in sommige gevallen niet zoals verwacht afgespeeld. Dit probleem is opgelost.

**Uitschrijving**

* In een inschrijvingsrapport worden alleen 20 uitgeschreven studenten weergegeven, zelfs als er meer studenten zijn uitgeschreven voor de cursus/certificering. Dit probleem is opgelost.
* In sommige gevallen was er een probleem met het exporteren van de lijst van niet-ingeschreven studenten bij Inschrijvingsrapport. Dit is nu opgelost.

**Leerprogramma**

* Als een student is ingeschreven voor slechts één van de cursusonderdelen in een flexibel leerplan, dan zal bij het klikken op de cursuslink van de andere cursussen waarvan de onderdelen niet zijn geselecteerd, een lege pagina worden geopend.

**Student**

* Enkele studenten, van wie de gebruikersnaam speciale tekens bevat, ontvangen geen e-mail meldingen zoals verwacht.
* In de immersieve weergave geeft de Kalenderwidget in sommige gevallen de komende VC-sessies niet weer zoals verwacht.
* In de Learner-app **Vaardigheid** werkt niet zoals verwacht. Dit probleem is opgelost.

**Zoeken**

* In een bepaald scenario kon de manager niet eerder naar de gebruikersgroep van een manager zoeken. Dit probleem is nu opgelost voor de rol van manager.

**Gebruikersgroep**

* Bij het exporteren van een gebruikersgroeprapport met meer dan 500 gebruikers kwamen de gegevenswaarden en de kolomkoppen in het rapport niet overeen wat nu is gecorrigeerd.
* Wanneer een beheerder een E-mailhandtekening bewerkt in een E-mailsjabloon en meerdere regels toevoegt, zag hij de html-tags alleen in de Beheerdersinterface. Dit probleem is nu opgelost.
* In **Admin App > Catalog > Zoeken naar catalogus**, kunt u niet zoeken.

**Gebruikers**

* Enkele actieve externe gebruikers werden verwijderd. We hebben een aantal veranderingen aangebracht en het probleem is nu opgelost.

**Importeren**

* Het importeren van een CSV mislukt als de CSV-koptekst spaties bevat of als het e-mailadres van een gebruiker accenten of diakritische tekens bevat.

**Het indienen van een activiteit**

* In de app voor docenten, op de pagina voor het indienen van activiteiten, overlapte de waarde van de ingediende datum met de bestandsnaam als deze lang was. Dit probleem van de gebruikersinterface is nu opgelost.

**Docent**

* Een docent ontvangt sessieuitnodigingen voor al zijn/haar sessies, ook al wordt alleen een nieuwe sessie toegevoegd. Dit probleem is opgelost.

**SCORM**

* Voor bepaalde SCORM-inhoud zijn er enkele browser-gerelateerde problemen, problemen met het navigeren met de speler en inconsistenties in de registratie van de quizscore. Deze problemen zijn opgelost.

**SAML en SSO**

* We hebben de foutmelding bijgewerkt die je te zien krijgt als de SSO referenties verlopen zijn.

**Learning Manager-API**

* De getlearningObject API retourneerde onjuiste inschrijvingsgegevens als gevolg van problemen met het opnemen in cache. Dit probleem is opgelost.
* Een VC-sessie toont nu de URL van de vergadering in het Locatie veld in een uitnodiging voor een vergadering.
* Als u meerdere VC-providerintegraties heeft opgezet en als één of meer van hen niet werkt zoals verwacht, zal de VC-selectie vervolgkeuzelijst een lege lijst tonen. Dit is nu opgelost. De resterende VC-integratie wordt nu correct vermeld.
* Connect VC-sjablonen laden niet zoals verwacht wanneer een docent zich bij de sessie aansluit.
* Er wordt een onjuiste duur getoond in de gebruikersinterface na het migreren van modules met een duur in een module_version CSV-bestand.
* Voor sommige accounts werkt het bijwerken van een gebruiker niet zoals verwacht. Dit is opgelost.

### Bekende problemen in deze update {#known-issues}

* Als u de **Duur** in de Learner-app. De inhoud en het filter zijn mogelijk niet synchroon als de student een andere landinstelling voor inhoud gebruikt en geen deel uitmaakt van de standaardinstantie wat betreft inschrijving.

>[!NOTE]
>
>De training &#39;**Duur**&#39; en &#39;**Indeling**&#39;-filters worden geïdentificeerd op basis van de trainingsinhoud die beschikbaar is voor de standaardinstantie en voor de voorkeurslandinstelling van het account.

+++

+++Update 59

## Update 59

Releasedatum: 18 december 2020.

### BlueJeans Events-connector {#bluejeanseventconnector}

BlueJeans Events-connector verbindt Learning Manager met Blue Jeans-systemen om de synchronisatie van gegevens te automatiseren. Met deze connector kunt u:

* **Virtuele sessies instellen met BlueJeans Events:** Configureer een nieuwe gebeurtenis in BlueJeans en stel een VC-sessie in Learning Manager in door de juiste BlueJeans-gebeurtenis te selecteren. Details over datum en tijd worden automatisch uit de BlueJeans-events gehaald.
* **Synchronisatie van geautomatiseerde gebruikersvoltooiing:** Via een geautomatiseerd proces voor het synchroniseren van gebruikersvoltooi kan de beheerder van de leermanager automatisch voltooiingsrecords voor BlueJeans-gebeurtenissen ophalen.

Deze nieuwe connector vereist een afzonderlijke set referenties om de connector te configureren.

Ga voor meer informatie naar [***BlueJeans Events-connector***](../integration-admin/feature-summary/connectors.md#bj-events).

+++

+++Update 58- December 2020-versie van Learning Manager

## Update 58 - Learning Manager-release van december 2020

Releasedatum: 05 december 2020.

### Nieuwe functies en wijzigingen {#Whatsnewandchanged-2}

Deze release focust op het volgende:

* Nieuwe startpagina-ervaring van student
* Responsieve lay-out voor mobiel web voor studentrol
* Op AI gebaseerde aanbeveling voor studenten
* Wekelijkse overzichtsmails
* Controlelijst
* Marketo Engage-integratie
* Aangepast domein
* Quizscores importeren uit Adobe Connect
* Diepe link naar catalogus voor studenten
* Verbeteringen in LinkedIn Learning
* ... en veel meer

Zie voor meer informatie  [***Nieuwe functies in de december 2020-versie van Adobe Learning Manager***](../whats-new.md).

### Niet-ondersteunde functies in de Mobile Immersive-ervaring {#unsupportedfeaturesinmobileimmersiveexperience}

De volgende functies worden niet ondersteund:

* Sociale app: een student wordt omgeleid naar de klassieke ervaring als hij/zij op de sociale widget op de startpagina klikt
* Profielinstellingen/profiel bewerken
* Badge/vaardigheden weergeven
* Leaderboard: een student wordt omgeleid naar de klassieke ervaring als hij/zij op de Leaderboard-widget op de startpagina klikt
* Taakhulpen downloaden.
* Filteropties in Zoeken.

### Bugfixes in deze update {#bug-fixes-1}

* U kunt een inhoudsmap niet verwijderen als de inhoudsmap verwijderde inhoud bevat.
* Met een leerplan kunnen beheerders een cursus opzetten met de instantie Automatisch. De docentinformatie voor een cursus met een module voor inzending van activiteiten was eerder niet juist opgezet. Nu wijst Learning Manager automatisch de docent van de standaardinstantie toe aan de instantie Automatisch.
* Een aangepaste badge met een cataloguslabel met een spatie staat het downloaden van de PDF niet toe zoals verwacht.
* Een rapport dat is gedownload van het dashboard, verschilt van de abonnementsmail die is ontvangen voor het dashboardrapport.
* Een studenttranscript bevat geen bijgewerkte gegevens voor een terugkerende certificering.
* Als er na het starten van een cursus een time-out optreedt, wordt het aantal pogingen niet weergegeven zoals verwacht. Af en toe is er ook een leeg scherm als u een cursus meerdere keren probeert.
* Er is een 5xx-fout nadat u een module hebt geüpload.
* Een sociaal privébord is niet voor alle studenten zichtbaar.

### Bekende problemen in deze update {#known-issues-1}

Na het afronden van een cursus of een certificering ziet u niet direct het pop-upvenster met feedback. Dit probleem doet zich alleen voor als u de cursus volgt in de ingesloten gebruikersinterface. Als u de cursus in de klassieke gebruikersinterface volgt, ziet u het pop-upvenster met feedback zoals verwacht.

+++

+++Update 57

## Update 57

Releasedatum: 23 september 2020.

**Inhoudsbibliotheek**

* Als u een inhoud uit de inhoudsbibliotheek archiveert, wordt de inhoud in de **Gepubliceerd** tabblad. Wanneer u de pagina vernieuwt, wordt de gearchiveerde inhoud niet meer weergegeven.
* Wanneer u een inhoudsmap maakt, **Naam** het veld is niet als verplicht gemarkeerd , hetgeen in feite een verplicht veld is .

**Klantenverzoek**

* Neem de volgende velden op het dashboard, Abonnementsrapport, op om te zien voor welke cursussen elke student is ingeschreven en of hij of zij de cursussen heeft voltooid:

   * UUID
   * E-mailadres

**Studenttranscript**

* Een Studenttranscript genereren in de Indonesische taal leverde fouten op.

**Zoeken**

* U kunt niet zoeken naar een specifieke cursus. Dit is opgelost.

+++

+++Update 56 - Mobiele app

Releasedatum: 25 augustus 2020

### Cursussen volgen van LinkedIn Learning {#takecoursesfromlinkedinlearning}

Learning Manager ondersteunt al cursussen van LinkedIn Learning binnen het studieplatform. Studenten kunnen nu dergelijke cursussen van LinkedIn Learning volgen in de mobiele app van Learning Manager. Zoek in de apparaat-app naar een cursus en start deze vervolgens.

Zie Cursussen volgen van [***LinkedIn Learning***](../learners/feature-summary/ipad-android-tablet-users.md#linkedin) voor meer informatie.

### Pushmeldingen voor inschrijvingen door beheerders {#pushnotificationforadminenrollments}

Wanneer de beheerder studenten inschrijft voor trainingen, ontvangen de studenten meldingen inzake de inschrijvingen.

Pushmeldingen wordt nu ook ondersteund voor aankondigingen.

### Verplichte L1-feedback {#mandatoryl1feedback}

In de nieuwste release van augustus 2020 maakt Learning Manager het voor beheerders mogelijk om L1-feedback dusdanig te configureren dat alle vragen verplicht worden. Hetzelfde wordt nu ondersteund vanuit het perspectief van de student in de mobiele app.

### Verbeteringen in de gebruikersinterface {#userinterfaceenhancements}

**Links in voettekst**

De beheerder kan in de beheerderweergave op het internet meerdere links in de voettekst instellen. Studenten kunnen deze links nu openen door op het hamburgerpictogram en het helppictogram te tikken.

Standaard zijn er twee links en de beheerder kan nog eens drie links toevoegen (via de beheerderweergave op internet) die in de app zichtbaar zijn.

**Kaartweergave voor leerobjecten**

In de delen Mijn Leerervaring en Catalogus van de app worden de trainingen standaard als kaarten weergegeven in plaats van lijsten. Dit is een wijziging voor studenten zoals eerder was de standaardweergave &quot;Lijstweergave&quot;.

Studenten kunnen echter wisselen tussen de lijst- en kaartweergave.

+++

+++Update 55- augustus 2020-versie van Learning Manager

Releasedatum: 23 augustus 2020

### Nieuwe functies en wijzigingen {#Whatsnewandchanged-3}

Deze release focust op het volgende:

* Verbeterde rapportage
* Persoonlijke inhoudsmappen
* Aangepaste FTP
* Ondersteuning van bijschriften voor video&#39;s
* Power BI-verbeteringen
* Verbeterde feedback
* Nieuwe en gewijzigde API&#39;s
* Wijzigingen aan beleid voor gegevensbewaring
* ... en veel meer

Zie voor meer informatie  [***Nieuwe functies in de augustus 2020-versie van Adobe Learning Manager***](../whats-new.md).

### Opmerkingen over deze release {#notes}

* Het duurt minder dan 15 minuten om een studenttranscript (~1 GB) te genereren.
* In eerdere versies van Learning Manager stonden in de kolommen Quizscore en Hoogste quizscore van het studenttranscript de score en de maximumscore in de indeling 25/100. Om de leesbaarheid en analyse te verbeteren, is de quizscore nu ook opgenomen in aparte kolommen: **Quiz_score, Quiz_score_max, Highest_Quiz_score en Highest_Quiz_score_max**. Daardoor kunnen beheerders snel berekeningen en analyses uitvoeren.

### Bugfixes in deze update {#bug-fixes-2}

**Connector**

* Een student kan niet aan twee verschillende vergaderingen tegelijk deelnemen, die door twee verschillende auteurs zijn gemaakt.
* Als u vanaf de Adobe Connect-kaart op de optie Verbindingen beheren klikt, navigeert u naar de pagina FTP-verbinding.
* Een geplande FTP-sync eindigt met een uitzondering.
* Er traden problemen met het wachtwoord op toen u verbinding wilde maken met Exavault.

**Cursus**

* U kunt een VC-module maken zonder een conferentiesysteem te selecteren. Een neveneffect daarvan is dat het proces om een cursus aan te maken Fout 500 veroorzaakt.
* Een student kan geen bronnen downloaden, zelfs niet als de student is ingeschreven voor een cursus die is gedupliceerd.
* Wanneer een beheerder of auteur een voorbeeld van een cursus bekijkt als student, kan hij/zij geen bronnen downloaden, tenzij hij/zij voor de cursus is ingeschreven.

**Apparaatapp**

* Bij bepaalde aanmeldingen geeft de donutgrafiek onder Mijn openstaande leermateriaal verschillende waarden van de studententoepassing weer van de browser naar de mobiele toepassing.

**Certificering**

* Het rapportfilter Status werkt niet zoals verwacht wanneer u een dashboardrapport voor certificering probeert te downloaden.

**Zoeken**

* Wanneer u op de pagina Studentencatalogus een cursus op opmerking probeert te zoeken, worden er geen zoekresultaten weergegeven.

**SCORM**

* Voor sommige inhoud geeft de SCORM-speler een leeg scherm weer.
* Verhaallijn-inhoud wordt geïdentificeerd als Captivate-inhoud als het gepubliceerde Verhaallijn-project een web object bevat dat naar de gepubliceerde Captivate-uitvoer verwijst.
* SCORM-inhoud kan niet worden gelanceerd door een foutieve URL.

**Aangepaste rol**

* Voor bepaalde scenario&#39;s kan een aangepaste beheerder niet de volledige lijst van Leerobjecten zien.
* Een aangepaste beheerder kan niet naar een leerprogramma of certificering zoeken in de dashboardrapporten.
* Een aangepaste beheerder kan niet zoeken naar een manager in een dashboard.
* Studenttranscripten die door een aangepaste beheerder zijn gegenereerd bevatten geen gegevens van verwijderde gebruikers.
* Een aangepaste auteur of aangepaste beheerder kan geen Leerprogramma, cursus of certificering dupliceren.

**Rapporten**

* De kolom Type in een studententranscript geeft de waarde als cursus weer voor de cursussen die deel uitmaken van een certificering, als de student is uitgeschreven voor de certificering.

**Vaardigheden**

* Terwijl u een vaardigheid voor een cursus toevoegt, treden er enkele problemen op wanneer u naar een vaardigheid zoekt.

**Gamification**

* Als veel gebruikers vertrouwelijk worden gemaakt, vertoont Edge en Internet Voorbeeld onverwacht gedrag wanneer er in de browser op het tabblad Vertrouwelijke student wordt geklikt.
* Wanneer de frequentie van een criterium wordt veranderd, worden de punten die met de oudere frequentie zijn berekend aan de huidige berekening toegevoegd.

**Beheerder **

* Studenten kunnen niet als aanwezig worden gemarkeerd als de cursusinstantie die aan een leerprogramma is toegewezen is veranderd.

**E-mailsjablonen**

* Voor leerprogramma&#39;s en certificeringen ontbreekt de wisselknop in het e-mailsjabloon.

**Inhoudsbibliotheek**

* SCORM-inhoud wordt niet gelanceerd zoals verwacht door een foutieve URL.

**Studenttranscripten**

* Wanneer u tijdens het genereren van studententranscripten een verwijderde student toevoegt aan het invoervak Studenten selecteren en daarna bij Geavanceerd de optie &#39;Gegevens van verwijderde cursisten opnemen&#39; inschakelt, gedraagt de pagina zich onverwacht.

**Zoeken**

* U kunt niet zoeken naar een cursus met behulp van de opmerkingen.

**Excel-rapporten**

* Als het langer dan een uur duurt om een rapport Audittrail van gebruiker te downloaden door de grote omvang of de trage verwerking, valt de verbinding weg en wordt het rapport niet gedownload.
* Is een student uitgeschreven voor een certificering? Dan wordt de kolom Type in een studententranscript weergegeven als &#39;Cursus&#39; in plaats van &#39;Certificering&#39; voor de cursussen die deel uitmaken van de certificering.

**Learner-app**

* Een student kan een bestelde cursus op een niet-bestelde manier volgen door naar de cursussen te gaan via een e-mail of een melding voor uitschrijving.
* Een student krijgt geen e-mails met herinneringen voor sessies zoals verwacht.
* Een cursus lanceert niet zoals verwacht als een bepaalde module ontbreekt.

**Aankondigingen**

* Als een aankondiging de tag bevat `<a>`, wordt de aankondiging niet zoals verwacht tot stand gebracht.

**Account**

* Accounts worden gedeactiveerd, zelfs als een account een geldige PO heeft.

**API**

* Als u vanuit de Adobe Connect-kaart op Verbindingen beheren klikt, wordt u omgeleid naar de pagina FTP-verbinding.
* Voor sommige scenario&#39;s krijgt de Connect-beheerder foutieve waarschuwingen.
* LinkedIn Learning-migratie veroorzaakt enkele fouten.

### Bekende problemen in deze update {#known-issues-2}

**Dashboardrapporten**

* Wanneer een leerprogramma van een certificering is verwijderd, geeft het rapport over actieve trainingen de cursussen weer die aanwezig zijn in het leerprogramma of certificering, zelfs als het leerprogramma of de certificering geen enkele inschrijving heeft.

+++

+++Update 54 - Mobiele app

## Update 54 - Mobiele app

Releasedatum: 16 april 2020

Werk de apparaattoepassing bij naar de nieuwste versie voor de nieuwste functies, updates en een betere gebruikservaring. De update is **verplicht**.

### Nieuwe en verbeterde functies {#newandenhancedfeatures}

Beheerders kunnen belangrijke informatie doorgeven aan alle gebruikers van de app. Aankondigingen kunnen van het type video of afbeelding zijn, of gewoon een sms-bericht. Dankzij deze release worden aankondigingen nu ondersteund in de apparaattoepassing. Zodra de app wordt gestart, verschijnt er een nieuwe aankondiging, zodat studenten geen belangrijke communicatie van de beheerders missen. Studenten kunnen het direct lezen of het later nog doorlezen door naar het tabblad **Aankondigingente** gaan.

Als er een of meerdere nieuwe aankondigingen zijn, kunt u deze zien in het gedeelte **Aankondigingen**.

Tik op **Aankondigingen** om een aankondiging weer te geven. De nieuwste aankondiging wordt op het scherm weergegeven.

Tik op **Naar links vegen voor Volgende** om de volgende aankondiging weer te geven.

### Aankondigingen {#announcements}

![](assets/read-later.png)

Als u de aankondiging op dat moment niet wilt lezen, kunt u er altijd voor kiezen om de hem later te lezen. Tik op **Later lezen** op de aankondiging zodat deze weer de status Ongelezen krijgt.

### Bugfixes in deze update {#bugsfixedinthisupdate}

* Op iOS worden podcasts niet meer afgespeeld wanneer het scherm is vergrendeld. Dit probleem is verholpen en het geluid wordt ook afgespeeld wanneer het scherm is vergrendeld.
* Als u een cursus volgt in de apparaattoepassing, kan de dia met het resultaat leeg worden weergegeven. Dit probleem is opgelost in deze update.

+++

+++Update 53 - April 2020-versie van Learning Manager

Releasedatum: 04 april 2020

De Learning Manager-release van april 2020 legde zich op het volgende toe:

* [Prestatieverbetering](../whats-new.md#performance)
* [Klassikale training](../whats-new.md#classroom)
* [Managerworkflows](../whats-new.md#manager)
* [Sociaal leren](../whats-new.md#social)
* [Rapportage](../whats-new.md#reporting)
* [Ervaring van de student](../whats-new.md#learner)
* [Wijzigingen op API-niveau](../whats-new.md#api)

Voor meer informatie, zie [***Nieuw in de Adobe Learning Manager-release van april 2020***](../whats-new.md).

+++

+++Update 52 - Mobiele app

## Update 52 - Mobiele app

Releasedatum: 20 december 2019

### Nieuwe en verbeterde functies {#Newandenhancedfeatures-1}

#### Merklogo van bedrijf {#companybrandinglogo}

U kunt nu de merknaam, het merklogo of beide in de apparaatapp weergeven, afhankelijk van de instellingen die de beheerder heeft geselecteerd.

#### Diepe links {#deeplinks}

Learning Manager start nu de apparaatapp zodra u op een link/URL klikt die door Learning Manager wordt ondersteund. Als de app niet op het apparaat is geïnstalleerd, wordt de URL in de browser geopend.

Hier zijn enkele gebruikscases, die in deze update worden ondersteund.

* Klik op een URL voor training die u in een e-mail hebt ontvangen.
* Standaard-URL&#39;s voor training die in de e-mailsjablonen worden weergegeven.
* Account-URL&#39;s die in de e-mailsjablonen worden weergegeven.
* Mijn leerervaring en Catalogus go-URL&#39;s.

Bovendien wordt elke URL met het domein *learningmanager.adobe.com* in de apparaatapp geopend.

#### Items in extern certificaat uploaden als bewijs van voltooiing {#uploadassetsinexternalcertificateasproofofcompletion}

In deze update kan een student activa uploaden als bewijs van voltooiing voor een extern certificaat.

Een student kan een extern certificaat openen en activa uploaden, zoals een PDF, tekst of beeldbestanden.

Zie voor meer informatie  [***Elementen uploaden in extern certificaat***](../learners/feature-summary/ipad-android-tablet-users.md#externalcert).****

### Opgeloste problemen in deze release {#issuesfixedinthisrelease}

* Een gebruiker kan zich niet bij de apparaatapp aanmelden als de e-mail speciale tekens bevat.
* Tijdens het scrollen knippert het pictogram Leerobject, wanneer u zich in een lijstweergave bevindt.
* U kunt nu alle pushmeldingen bekijken zonder op de pijl omlaag te tikken en berichten één voor één te bekijken.
* Nadat u op een melding hebt geklikt voor een bericht dat in beheer is geaccepteerd of afgewezen, wordt er een lege pagina geopend in de app. In deze update wordt de boardpagina geopend.

+++

+++Update 51

In deze update kunt u ook de bannerafbeelding voor een leerobject wijzigen.

U kunt de banner ook aanpassen op een pagina voor Sociaal leren.

## Update 51

Releasedatum: 17 december 2019

### Nieuwe en verbeterde functies {#Newandenhancedfeatures-2}

### Bereik van leerprogramma’s op basis van rollen {#learningplansscopedbyconfigurableroles}

U kunt aangepaste rollen maken voor leerprogramma&#39;s om het bereik van gebruikers en leerobjecten in te stellen. Met andere woorden, u kunt leerprogramma&#39;s maken met een beperkt bereik op basis van door de beheerder ingestelde rollen.

Een beheerder kan nu het bereik definiëren of beperken en tegelijkertijd toegang verlenen voor het beheer van leerprogramma&#39;s.

Zie [***Bereik van leerprogramma&#39;s op basis van rollen***](../administrators/feature-summary/custom-role.md#scopeconfigure) voor meer informatie.

### Actieve velden in rapporten beperken {#restrictactivefieldsinreports}

Voor actieve velden hebben we twee nieuwe opties toegevoegd: **Te rapporteren** en **Exportable**.

Voor CSV-velden en handmatig toegevoegde velden geldt dat als een actief veld is gemarkeerd als **Rapporteerbaar**, het actieve veld kan worden gezocht in een filter in een dashboardrapport.

Zie voor meer informatie  [***Actieve velden in rapporten beperken***](../administrators/feature-summary/add-users-user-groups.md#restrictactivefields)***.**

### Beschrijving van inhoudsmodule bekijken {#viewdescriptionofcontentmodule}

Als auteur ziet u de beschrijving van de modules terwijl u de module aan een cursus toevoegt.

Tijdens het maken van een module voegt u een beschrijving toe. Zie [***Een cursus maken***](../authors/feature-summary/courses.md) voor meer informatie over het maken van een cursus.

### Cursus- en sessienamen weergeven {#displaycourseandsessionnames}

Als docent kunt u de sessie- en cursusnamen zien in de weergave Aanwezigheid. U kunt volgen welke sessies worden aangepast.

### Aankondiging voor studenten {#announcementforlearners}

Studenten kunnen nu een aankondiging in volledige weergave in plaats van in lijstweergave zien. Dit gebeurt wanneer de student één ongelezen aankondiging heeft. Hierdoor kan de student de aankondiging gemakkelijker lezen.

Met Adobe Learning Manager kunt u uw account aanpassen om een rijkere gebruikerservaring te bieden. Hier volgt een lijst met elementen die kunnen worden aangepast. Contact [Ondersteuning voor Learning Manager](mailto:learningmanagersupport@adobe.com)om deze wijzigingen aan te brengen.

* Kleuren trainingskaart.
* Voortgangspictogram
* Afbeelding muisaanwijzer
* Lettertype

Zie [***Uw account aanpassen***](../administrators/feature-summary/themes.md#customize) voor meer informatie.

### Bannerafbeeldingen uploaden {#uploadbannerimages}

In deze update kunt u ook de bannerafbeelding voor een leerobject wijzigen.

U kunt de banner ook aanpassen op een pagina voor Sociaal leren.

### API-ondersteuning {#apisupport}

Deze update van Learning Manager bevat een API voor de volgende handelingen:

**Badge-PDF downloaden**

Deze update bevat een student-API waarmee een PDF van een badge kan worden gedownload.

**Studenttranscript downloaden**

Deze update bevat een student-API waarmee studenttranscripten kunnen worden gedownload.

**Quizrapport downloaden**

Deze update bevat een admin-API waarmee quizrapporten kunnen worden gedownload.

**Paginering van gamification**

Alle student- en gamificationpunten in het bereik van een student kunnen nu worden opgehaald met een student-API. Dit is handig voor het opbouwen van een gamification-leaderboard.

**API:** `GET /users`

**Verzoek:** `GET\\ users?page[offset]=0&page[limit]=10&sort=id&filter=gamification`

**Reactie:** *Het antwoord bevat de gesorteerde gebruikers in volgorde van gamificationpunten.*

**Niet storen**

Op dit moment kunnen alleen beheerders gebruikers toevoegen aan een Niet storen-lijst via de gebruikersinterface. Na deze release kan een student deze machtigingen voor zichzelf instellen via een API, mits deze API door de beheerder is ingeschakeld. Voor het inschakelen van deze API voor een account is een back-endinstelling nodig. Deze API biedt de student de mogelijkheid om onderstaande machtigingen met betrekking tot e-mails te bewerken.

* Directe e-mails naar student
* Escalatiemails naar Managers van Student
* Informatie over directe rapporten
* Informatie over rapporten voor het overslaan van niveaus

Zie het volgende voor meer informatie over API&#39;s in Learning Manager:

* [***API-referentie***](<https://learningmanager.adobe.com/docs/Learning> Managerapi/v2/)
* [***Handleiding voor API-ontwikkelaars***](<https://helpx.adobe.com/captivate-Learning> Manager/integration-admin/feature-summary/developer-manual.html)

### Opgeloste problemen in deze release {#Issuesfixedinthisrelease-1}

* Alleen gebruikers die bij een specifieke gebruikersgroep horen, moeten aankondigingen ontvangen die voor hen bedoeld zijn. Andere gebruikers mogen de aankondigingen niet ontvangen.
* De speler geeft een laadspinner weer voordat de inhoud wordt weergegeven.
* Gebruikersmetadata in rapporten veroorzaken een Null Pointer Exception.
* Bij het toevoegen van een instructeur voor een standaardinstantie van de Connect VC-cursus wordt het bericht *&#39;Geen sessie voor deze module&#39;* weergegeven op de pagina Cursusinstantie in de Admin-app.

* Het exporteren van een studenttranscript leidt tot onverwacht gedrag tijdens een FTP-overdracht.
* De naam van een auteur wordt niet correct weergegeven bij cursussen in een leerprogramma.
* De wijzigingen in productterminologie van taakhulpen worden niet weergegeven zoals verwacht.
* De naam van een module wordt afgekapt als de naam lang is en wordt weergegeven in mobiele portretmodus.
* Kan geen instantie maken voor een oudere Connect-cursus na het bijwerken van de standaardinstantie met een oudere Connect-implementatie.
* Een docent ontvangt een agenda-uitnodiging nog voordat de cursus is gepubliceerd.

+++

+++Update 50

## Update 50

Releasedatum: 24 oktober 2019

### Nieuwe en verbeterde functies {#Newandenhancedfeatures-3}

#### Maak een aangepaste rol met meerdere catalogusbereiken {#createcustomrolewithmultiplecatalogscopes}

Als beheerder kunt u een aangepaste rol beperken op basis van catalogi en gebruikersgroepen. Alle gebruikers die tot dergelijke rollen behoren, kunnen alleen leerobjecten van de catalogus in hun bereik zien. Deze gebruikers kunnen alleen acties uitvoeren die zijn gedefinieerd in het kader van hun gebruikersgroepen.

Tot nu toe kon in Learning Manager een aangepaste rol voor meerdere bereiken worden ingesteld voor één gebruikersgroep met volledige machtigingen.

In deze update van Learning Manager kunt u een aangepaste rol voor meerdere catalogi instellen, waarbij aan elke catalogus verschillende machtigingen worden toegewezen. Zie [***Bereik instellen van aangepaste rollen voor meerdere catalogi***](../administrators/feature-summary/custom-role.md#multi-scope) voor meer informatie.

### Zoekverbeteringen {#enhancementstosearch}

**Leerplan**

De pagina Leerplannen voor Beheerders en Auteurs bevat nu een zoekbalk, die u kunt gebruiken om naar een leerplan te zoeken.

![](assets/search-for-as-learningplan.png)

**Beheerders- en auteursapps**

In deze update van Learning Manager kunt u, als Beheerder of Auteur, vrij zoeken naar een leerobject. Daarnaast kunt u zoeken met automatisch aangevulde zoeksuggesties.

### Zoekfilter is behouden {#searchfilterispreserved}

Dit geldt alleen voor een studentenprofiel.

Op de pagina&#39;s **Catalogus** en **Mijn leerervaring** kan een cursist een filter toepassen op het linkerdeelvenster, bijvoorbeeld **Cursussen** of **Leerprogramma&#39;s**. Vervolgens kan op een cursus of catalogusitem worden geklikt.

![](assets/choose-learning-objects.png)

Wanneer de cursist terugkeert naar de pagina&#39;s **Catalogus** of **Mijn leerervaring** met behulp van de knop Vorige van de browser, blijft het filter behouden. Het filter dat een leerling eerder had toegepast, wordt niet meer gereset.

### Zichtbaarheid van zoekfilters regelen {#controlvisibilityofsearchfilters}

In eerdere versies van Learning Manager hebben beheerders geen controle over de zichtbaarheidsopties van een catalogusfilter, zodat leerlingen de vaardigheden en tags niet zien. In deze versie van Learning Manager kan een beheerder filteren op de typen, vaardigheden en tags van een catalogus.

U kunt de volgende opties zien als u op de pagina **Instellingen** voor de categorie Filterpanelen weergeven op **[!UICONTROL Bewerken]** klikt. De opties bepalen welke filterpanelen studenten kunnen zien, zodat zij hun zoekresultaten kunnen verfijnen.

Zie [***Filterpanelen weergeven***](../administrators/feature-summary/settings.md#filter-panels) voor meer informatie.

### QR-code van beheerdersapp downloaden {#downloadqrcodefromadministratorapp}

In eerdere updates van Learning Manager ondervonden aangepaste beheerders problemen bij het downloaden van een QR-code. In deze update kan een aangepaste beheerder die toegang had tot **Alle studenten** en machtigingen had voor **Cursusinschrijving** de QR-code downloaden.

QR-code is nog steeds niet beschikbaar voor gebruikers met een aangepaste rol wanneer zij machtigingen hebben voor een beperkt aantal gebruikers.

### Opmerkingen toevoegen tijdens het inschrijven van studenten {#addcommentswhileenrollinglearners}

Als beheerder of manager kunt u opmerkingen toevoegen terwijl u studenten voor een cursus inschrijft. U kunt aanvullende informatie geven over de groep gebruikers die zich inschrijven. Deze gegevens worden geëxporteerd in cursusrapporten.

Zie [***Opmerkingen toevoegen tijdens het inschrijven van studenten***](../administrators/feature-summary/courses.md#enroll-comments) voor meer informatie.

### Ondersteuning voor permanente vergaderruimte van Adobe Connect {#supportforadobeconnectpersistentmeetingroom}

In Adobe Connect gebruiken klanten bestaande vergaderruimtes die ze al hebben gemaakt in Connect. Alle vergaderruimtes in Connect zijn permanent en de sjablonen voor de vergaderruimtes zijn zorgvuldig ingesteld om een uniforme ervaring voor elke permanente ruimte te bieden.

In deze versie van Learning Manager is de integratie met Adobe Connect verbeterd om ook permanente ruimtes te ondersteunen. Dit betekent dat u nu een virtueel klaslokaal kunt maken met behulp de ruimte die al in Adobe Connect is gemaakt.

In Learning Manager kunnen studenten de verbonden ruimte voor hun virtuele sessie nu ook betreden met behulp van verificatie via eenmalige aanmelding.

Zie [***Ondersteuning voor permanente ruimtes in Adobe Connect***](../integration-admin/feature-summary/connectors.md#persistent) voor meer informatie.

### Waarschuwing voordat aanwezigheid wordt gemarkeerd als de duur van de sessie nul is {#warningbeforemarkingattendanceifthesessiondurationiszero}

Een auteur of beheerder kan een sessie met een duur van 0 maken. Dit is mogelijk wanneer:

* begindatum en/of einddatum leeg zijn.
* begintijd en/of eindtijd leeg zijn.

In deze update ziet de beheerder, manager of docent een **waarschuwing, waarin staat dat de duur van een sessie nul is**.

### Waarschuwing als er een klassikale module wordt gemaakt zonder sessiegegevens toe te voegen {#warningifaclassroommoduleiscreatedwithoutaddingsessiondata}

Als een auteur een cursus maakt door een klassikale of VK-module toe te voegen, kan de auteur het volgende doen:

* geen begin-/einddatum en begin-/eindtijd toevoegen.
* datum toevoegen, maar geen begin-/eindtijd.
* datum en een begintijd toevoegen.

In alle bovenstaande gevallen, wanneer een beheerder, manager of docent aanwezigheid of voltooiing markeert, worden de waarden van de begin- en einddatum van de sessie gelijk, wat betekent dat in een Studenttranscript de waarde voor Bestede leertijd als 0 (nul) wordt weergegeven.

In deze update ziet de auteur een **waarschuwingsbericht waarin staat dat de sessiegegevens onvolledig zijn**.

### Opgeloste problemen in deze release {#Issuesfixedinthisrelease-2}

**Learner-app**

* Een student kan een cursus in een leerprogramma niet zien als de cursus door een externe auteur is gemaakt.
* Als een beheerder een functie aan een externe bord toevoegt, gaat het verzoek voor inhoudsbeheer naar een interne SME, die aan die vaardigheid is toegewezen.
* Een cursist ziet de knop Start of Doorgaan niet nadat hij/zij zich voor LinkedIn-cursussen heeft ingeschreven.

**E-mail**

* Als een lijst met DND&#39;s van e-mail een groot aantal gebruikers bevat, laadt de pagina **Instellingen** erg langzaam. In deze update is paginering toegevoegd aan een lijst met DND&#39;s van e-mail.
* Een docent ontvangt updates/mails voor sessies waar hij/zij geen deel van uitmaakt. Dit is opgelost in deze update.

**Vaardigheden**

* Het type waarde van een vaardigheid verschijnt verkeerd als tekst in een Studenttranscript.

**Mobiele app**

* De student kon in de mobiele app een leerplan bekijken en zich hiervoor inschrijven, wat niet de bedoeling was. Dit is opgelost in deze update.

**Aangepaste rollen**

* Als aangepaste beheerder kunt u naar een manager in een dashboardrapport zoeken.

**Meerdere pogingen**

* In sommige scenario&#39;s worden enkele cursusmodules niet aan de deelnemers getoond.

**Externe inschrijving**

* U kunt het externe profiel van een gebruiker niet wijzigen als plaatsen voor de bovenste profielen zijn gevuld.

### Bekende problemen in deze release {#knownissuesinthisrelease}

* Als u in de onderstaande browsers met de muis over het linkerdeelvenster gaat, verschijnt de tekst na een kleine vertraging.

   * Edge 42.17134.1.0
   * Edge 44.1763.1.0
   * Internet Explorer 11.1006
   * Internet Explorer 11.615

* Een student mag voor en na de sessie een Connect-vergaderruimte betreden.

+++

+++Update 49

## Update 49

Releasedatum: 26 augustus 2019

### Nieuwe en verbeterde functies {#Newandenhancedfeatures-4}

**Prestatieverbetering**

* Het importeren van gebruikers in het systeem is sneller dan in vorige releases. Er is een aanzienlijke verbetering bij het importeren van grote gebruikersgegevens.
* Voor managers en beheerders zijn de opties in de vervolgkeuzelijst Rapportconfiguratie nu gewijzigd om de gegevens op aanvraag te laden.
* API-prestaties zijn verbeterd. Veel API&#39;s zouden nu een verbeterde responstijd moeten hebben.
* De tijd die nodig is om studenttranscripten te genereren is verbeterd.
* Er is geen vertraging op de pagina&#39;s waarop interne en externe studenten worden vermeld, met name als er een groot aantal gebruikers is.

**Speciale gebruikersbevoegdheden**

Een beheerder kan een gebruikersgroep speciale bevoegdheden geven op basis van welke groepsleden aan alle boards kunnen deelnemen. Beperkingen die zijn ingesteld in het gedeelte Omvanginstellingen worden omzeild door de speciale gebruikersgroep. Zie [***Speciale gebruikersbevoegdheden***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#privilege) voor meer informatie.

**Veranderingen in de gebruikersinterface**

* In het dialoogvenster **Rapport toevoegen** de **Tijdspanne** en **Filters** kiezers worden weergegeven als afzonderlijke secties, die standaard zijn samengevouwen. Zie [***Rapporten maken***](../administrators/feature-summary/reports.md#report) voor meer informatie.

* In het dialoogvenster **Rapport toevoegen** voor een gebruikersgroep kunt u de functie voor automatisch aanvullen van zoekresultaten gebruiken om één of meerdere gebruikersgroepen te kiezen. Zie [***Gebruikersgroeprapporten***](../administrators/feature-summary/reports.md#user-group-reporting) voor meer informatie.

**Veranderingen in waarden in tijdkolommen**

In de studenttranscripten zijn in de tijdkolommen de minuten afgerond tot de dichtstbijzijnde minuut en is de secondewaarde 00. Zie [***Tijdkolommen***](../administrators/feature-summary/learner-transcripts.md#datetime) voor meer informatie.

### Opgeloste problemen in deze release {#Issuesfixedinthisrelease-3}

**Studentendashboard**

* De status wordt weergegeven in een studentenagenda **Ingeschreven sessie** zelfs als een manager de inschrijving nog moest goedkeuren. Nu de juiste status **In behandeling** wordt weergegeven aan de student totdat de manager de inschrijving goedkeurt.

* In een bepaald geval werd voor een sessie de status weergegeven in de studentenagenda **Ingeschreven** ook al heeft de student een cursus voltooid.

**Managerdashboard**

* Managers konden nalevingstrainingen van hun team niet volgen als de teamleden via leerplannen waren ingeschreven.

**Zoeken**

* In de docentenweergave was het niet mogelijk om een student te zoeken.

**Gebruikersinterface**

* Voor een account waarop classificatiewijzigingen waren toegepast, werden de wijzigingen niet zoals verwacht weergegeven in de meldingen.

### Bekende problemen in deze release {#Knownissuesinthisrelease-1}

* Het is niet mogelijk om met de zoekbalk verwijderde gebruikers te zoeken in de lijst Externe gebruikers. Als tussenoplossing kunt u omlaag schuiven om de lijst met alle gebruikers weer te geven en de gewenste gebruiker handmatig te vinden.
* Als een Speciale gebruiker een bericht plaatst op een extern board, wordt het verzoek voor inhoudsbeheer ontvangen door vakexperts in zijn/haar bereik.

+++

+++Update 48

## Update 48

Releasedatum: 2 augustus 2019

### Nieuwe en verbeterde functies {#Newandenhancedfeatures-5}

**Scheiding van het bereik in Sociaal leren voor interne en externe gebruikers** Een beheerder kan afzonderlijke bereiken definiëren voor interne en externe studenten. Er zijn twee nieuwe secties voor interne en externe gebruikers.  U kunt het bereik voor studentengroepen in beide secties bepalen.  De waarden van gebruikerseigenschappen kunnen voor interne gebruikers worden bepaald.  Het externe profiel, waarin studenten dezelfde sociale ruimte kunnen delen, kan voor externe gebruikers worden bepaald.  Zie voor meer informatie [***Bereik-instellingen***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#scopesettings).  **Sociaal-Beperken van het maken van sociale boards** Om het maken van boards door alle studenten te beperken en de boards effectief te modereren, kan een beheerder een bepaalde groep gebruikers machtigingen verlenen om boards te maken. De beheerder kan het maken van boards tot een selecte groep beperken zodat niet elke student die deelneemt aan Sociaal leren boards kan maken.  Zie voor meer informatie [***Machtigingen voor het maken van boards***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#permission).  **Alleen lege actieve velden voor studenten weergeven** Een beheerder kan ervoor kiezen om de actieve velden weer te geven of te verbergen nadat de waarden zijn ingevuld. Zie voor meer informatie [***Gebruikersweergave***](../administrators/feature-summary/add-users-user-groups.md#activefields).  **Interne gebruikers worden na een opgegeven inactiviteitsduur verwijderd** Een beheerder kan de duur (in dagen) instellen waarbinnen een interne student wordt verwijderd als de student tijdens de opgegeven periode inactief blijft. Zie *** voor meer informatie[Gebruikers automatisch verwijderen](../administrators/feature-summary/settings.md#autodelete)***.  **Koppelingen in de voettekst aanpassen** Een beheerder kan koppelingen toevoegen aan en aanpassen in de voettekst. De links kunnen ook voor verschillende talen aangepast worden.  De bestaande methode voor het toevoegen van de koppeling Contact opnemen met beheerder aan de voettekst is ook beschikbaar in het dialoogvenster **Voettekstkoppelingen** sectie. Zie voor meer informatie [***Voettekstkoppelingen aanpassen***](../administrators/feature-summary/settings.md#footer).

### Bekende problemen in deze release {#Knownissuesinthisrelease-2}

* Aangepaste links in de voettekst worden niet weergegeven voor integratiebeheerders.

+++

+++Update 47 - Mobiele app

## Update 47 - Mobiele app

Releasedatum: 24 juli 2019

Android-gebruikers:

Deze update ondersteunt ook de noodzakelijke wijzigingen om te voldoen aan de herziene aanbevelingen van Google voor het implementeren van pushmeldingen. Daarom ontvangt u niet langer **meldingen** als u versie 2.7.4 of ouder gebruikt.

Het is raadzaam naar versie 2.8 te upgraden om meldingen te ontvangen.

### Nieuwe en verbeterde functies {#Newandenhancedfeatures-6}

**Sociaal leren**

Deel uw expertise met collega&#39;s in de vorm van door gebruikers gegenereerde inhoud die op thematische discussieboards wordt geplaatst.  Andere studenten die in vergelijkbare vaardigheden geïnteresseerd zijn, kunnen deze boards volgen om bij te leren en zelfs aan het onderwerp bij te dragen, vergelijkbaar met een socialmediaplatform.

Deel ideeën en zinvolle inzichten in een informele omgeving.  Vind berichten wel of niet leuk, upload inhoud en reageer op berichten.  Zie [***Sociaal leren in de mobiele app***](../learners/feature-summary/ipad-android-tablet-users.md#socialmobile) voor meer informatie.

**Media op een board delen**

Deel afbeeldingen, documenten, audio- of videobestanden op elk board, zodat andere leden van het board uw bericht kunnen bekijken en een interactie kunnen starten.  Zie voor meer informatie [***Bericht delen***](../learners/feature-summary/ipad-android-tablet-users.md#socialmobile).

**Bestanden inzenden voor klassikale en activiteitsmodules**

Stuur bestanden naar uw docent als bewijs van voltooiing.  De docent kan uw inzending vervolgens goedkeuren of weigeren op basis van de inhoud van het bestand.  Zie [***Bestanden inzenden voor goedkeuring***](../learners/feature-summary/ipad-android-tablet-users.md#submitfile) voor meer informatie.

**Bijgewerkte platformondersteuning**

De mobiele Learning Manager-app wordt nu ondersteund op apparaten met Android 7 en hoger, en iOS 10 en hoger. Zie [***Systeemvereisten***](../system-requirements.md) voor meer informatie.

### Bekende problemen in deze release {#Knownissuesinthisrelease-3}

1. Op Android kunt u geen GIF-bestand uploaden in een bericht, opmerking, of als antwoord op een opmerking.
1. Als moderator van een board kunt u geen berichten, opmerkingen of antwoorden van gebruikers verwijderen.  Dit kan wel via de web-app.
1. In de app kunt u geen vraagtype markeren.
1. Nadat u Sociaal leren in de app hebt ingeschakeld, start u de app opnieuw om het tabblad **Sociaal leren** weer te geven.  Als u Sociaal leren niet ziet, sluit u de app en start u deze vervolgens opnieuw.  Het tabblad Sociaal leren moet zichtbaar zijn.

+++

+++Update 46

### Nieuwe en verbeterde functies {#Newandenhancedfeatures-7}

## Update 46

Releasedatum: 20 juni 2019

**Automatisch beheer van inhoud**

Met Sociaal leren kunt u inhoud die door studenten is geplaatst op twee manieren beheren, namelijk: - **Geen beheer** en **Handmatig beheer**. In deze release verbetert Adobe Learning Manager de mogelijkheden voor sociaal leren door functies voor automatisch beheer op basis van AI te bieden. Wanneer inhoud wordt plaatst, wordt de inhoud geanalyseerd om te zien of de inhoud bij de vaardigheid hoort waarvoor de inhoud is geplaatst. Op basis van de vertrouwensscore wordt de inhoud live geplaatst of verzonden voor handmatig beheer. Zie voor meer informatie *[** Auto-ondersteund beheer **](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#autocuration)**.***

**Vaardigheid toewijzen aan vaardigheidsdomeinen**

Wijs vaardigheden in uw account toe aan de vaardigheidsdomeinen die aanwezig zijn in het LMS van de Learning Manager. Zo kunt u uw accountvaardigheden koppelen aan de vaardigheidsdomeinen die worden ondersteund door de Learning Manager voor automatisch beheer. Zie [***Vaardigheid toewijzen aan domeinen***](../administrators/feature-summary/curation-skills.md) voor meer informatie.

**CSV-specificaties en voorbeeld-CSV&#39;s**

Bijgewerkte CSV-specificaties die u kunt gebruiken om uw bestaande LMS-migratiegegevens toe te wijzen. Gebruik de nieuwste downloadbare CSV-specifications en sample-csvs zip-bestanden om inzicht te krijgen in de voorgeschreven indeling van in te voeren gegevens. Zie voor meer informatie  [***Migratiehandleiding***.](../integration-admin/feature-summary/migration-manual.md)

### Opgeloste problemen in deze release {#Issuesfixedinthisrelease-4}

**Learning Manager-API**

* Wanneer een extern profiel werd toegevoegd met behulp van de POST-methode van de API *externalProfile*, werd de welkomstmail niet weergegeven.

**Managerdashboard**

* Wanneer een manager de optie heeft geselecteerd **Dit kwartaal**, werden de gegevens over inschrijving, voortgang en voltooiing van een leerobject niet weergegeven. In deze release worden deze gegevens wel weergegeven.

**Studenten op de wachtlijst**

* Als in eerdere releases van Learning Manager een manager studenten had ingeschreven en de instructeur de studenten op de wachtlijst wilde weergeven, verscheen een foutbericht. In deze release kan een instructeur de wachtlijst met studenten bekijken zonder dat er een foutbericht verschijnt.

**Overzicht van certificering**

* Wanneer een auteur een cursus en certificering had gemaakt met een beschrijving en overzicht van de inhoud, en de student op de cursuspagina kwam, werd de inhoud van het overzicht niet weergegeven. De inhoud was echter wel zicht baar op de voorbeeldpagina&#39;s voor studenten in de Admin- en Author-apps. In deze release wordt de inhoud van het overzicht wel weergegeven in de Learner-app.

**Catalogus**

* Een student kan alle leerobjecten van elke catalogus bekijken. Als in eerdere releases een catalogus geen leerobject bevatte, werd de catalogus toch weergegeven vóór ander catalogi. In deze release worden alle catalogi die geen leerobjecten bevatten onderaan de catalogi weergegeven.

+++

+++Update 45

Releasedatum: 30 mei 2019

**Nieuwe en verbeterde functies**

* Geconsolideerd zoeken in alle instanties naar ingeschreven studenten in de studentsectie van het leerobject. Zoek naar ingeschreven gebruikers in de sectie Student van het leerobject met automatisch aangevulde zoeksuggesties. Zie [***Naar ingeschreven gebruikers zoeken***](../administrators/feature-summary/courses.md#searchforusers) voor meer informatie.
* Volledige bewerkingsmogelijkheden van leerobjecten die via een gedeelde catalogus zijn verkregen. Zie voor meer informatie [***Besturing gedeelde catalogus***](../administrators/feature-summary/shared-catalog-full-control.md). Neem contact op met de ondersteuning van Adobe Learning Manager om de functie in te schakelen.
* Docenten kunnen nu gemakkelijk de sessies en modules identificeren met openstaande beoordelingen. Zie voor meer informatie [***Beoordelingen in behandeling***](../instructors/feature-summary/learners.md#pending).

* Vaardigheden ondersteunen nu het toekennen van puntwaarden in decimale notatie. Op deze manier kunnen auteurs een decimaal niveau aan een bepaalde cursus toekennen. Zie voor meer informatie [***Decimale ondersteuning***](../administrators/feature-summary/skills-levels.md#decimal).
* Automatiseer het maken van aangepaste rollen. Zie [***Rollen configureren via CSV-bestanden***](../integration-admin/feature-summary/configure-role-csv-files.md) voor meer informatie.
* Inzendingen vereist voor externe certificeringen en activiteitenmodules zijn nu optioneel. Hierdoor kunnen managers en docenten evalueren zonder indiening. Zie voor meer informatie [***Optionele indiening***](../managers/feature-summary/learning-objects.md#optional).
* Download Studenttranscripten voor verwijderde gebruikers. Zie [***Studenttranscripten***](../administrators/feature-summary/learner-transcripts.md) voor meer informatie.
* Ondersteuning voor de volgende talen:

   * Koreaans
   * Turks
   * Nederlands
   * Pools

**Bekend problemen**

* Ondersteuning voor decimalen in vaardigheidspunten wordt alleen ondersteund voor Engels.
* Voor Koreaans, Japans en Russisch wordt de tijd van de sessie niet als verwacht weergegeven.

**Opgeloste problemen in deze release**

* De quizscores worden niet opgeslagen voor een leerprogramma of certificering op het tabblad Aanwezigheid en scores.
* Een beheerder of manager kan een externe certificering niet als voltooid markeren.
* Een beheerder kan in het dialoogvenster Studenttranscripten geen aangepast datumbereik selecteren als de taal op Portugees of Spaans is ingesteld.
* Een beheerder kan geen extern profiel maken als de profieltaal Frans is.
* Actieve velden zijn niet zichtbaar in het dialoogvenster Gebruiker bewerken als voor de landinstellingen een andere taal dan Engels is geselecteerd.

+++

+++Update 44 - Mobiele app

Releasedatum: 26 april 2019

* **Wijzigingen in gebruikersinterface:** In de app  ![](assets/hamburger.jpg) en de  ![](assets/search-magnifying-glass-icon.png) boven in het scherm worden nu opties weergegeven.

![](assets/1.png)

* **QR-code scannen voor inschrijving:** De mogelijkheden voor QR-codes zijn verbeterd. QR-code ondersteunt nu niet alleen het markeren van aanwezigheid, maar ook het inschrijven voor een cursus en het voltooien van een cursus.

  Als u zich voor een cursus wilt inschrijven en de cursus wilt voltooien, kunt u een QR-code scannen die uw beheerder heeft verstrekt. Ga voor meer informatie over het scannen van QR-codes in de webversie van Learning Manager naar  [***QR-code scannen***](<https://helpx.adobe.com/captivate-Learning> Manager/whats-new.html#QRcodetoenrollcompletenrollcompleteaccourse).

* **Meerdere pogingen op cursus:** Met de app Leermanager kan de student cursussen volgen waarvoor meerdere pogingen zijn ingeschakeld. Zie voor meer informatie over het instellen van meerdere pogingen  [***Meerdere pogingen***](<https://helpx.adobe.com/captivate-Learning> Manager/authors/feature-summary/courses.html#multiPogingen).

+++

+++Update 43

## Update 43

Releasedatum: 28 januari 2019

* De leertijd die een student aan een module heeft besteed, kan meerdere keren worden geteld door de aanwezigheid meermaals aan te duiden. Dit probleem is opgelost.
* Aanwezigheid voor een leerobject binnen een meerdaagse sessie markeren kan de verkeerde startdatum voor de sessie voor een student in een leertranscript weergeven. Dit probleem is opgelost.
* Gebruikers kunnen een cursus mogelijk niet bekijken wanneer deze is toegevoegd aan een voltooid leerprogramma of afgeronde certificering. Dit probleem is opgelost.
* Gebruikers kunnen zich ten onrechte inschrijven wanneer ze uit een gebruikersgroep worden verplaatst. Dit probleem is opgelost.
* Studenten en docenten ontvangen mogelijk geen e-mail wanneer de sessiedetails zijn gewijzigd in de app voor docenten. Dit probleem is opgelost.
* URL van Adobe Connect werkt mogelijk niet juist wanneer er &#39;/&#39; aan het einde van de URL staat. Dit probleem is opgelost.
* Er wordt een foutmelding weergegeven wanneer er ten minste één verplichte module voor een reeds gepubliceerde cursus wordt geselecteerd. Dit probleem is opgelost.
* Wanneer een student een cursus heeft voltooid en deze als verplicht is gemarkeerd door de auteur, wordt de voltooiing van de cursus mogelijk niet als voltooid gemarkeerd. Dit probleem is opgelost.
* Gecontroleerde waarde van een geselecteerde module voor een dubbele cursus verschijnt mogelijk niet meteen. Het wordt alleen weergegeven als een dubbele cursus wanneer de pagina wordt vernieuwd. Dit probleem is opgelost.
* Nadat een cursus is gepubliceerd worden alle modules als ongecontroleerd weergegeven in de bewerkingsmodus. De pagina moet worden vernieuwd om de wijzigingen te zien. Dit probleem is opgelost.
* Selectie van een verplichte module is beschikbaar voor een bestelde cursus, terwijl dit niet de bedoeling is. Dit probleem is opgelost.
* Een verplichte module blijft in het vervolgkeuzemenu staan, zelfs nadat deze verwijderd is tijdens het bewerken van de cursus. Dit probleem is opgelost.
* Voorwerk- en testmodules worden standaard als verplicht gemarkeerd. Dit probleem is opgelost.
* Als u op de L3-feedbacklink in uw e-mail klikt, wordt het modale venster Feedback niet geopend. Dit probleem is opgelost.
* Certificering ontbreekt in de vervolgkeuzelijst van dashboardrapporten, hoewel deze zichtbaar is in de manager-app en in de API-lijst met gegevens. Dit probleem is opgelost.
* Enkele leerobjecten konden niet door de beheerder worden gearchiveerd vanwege een gebrek aan machtigingen, hoewel gedeelde catalogi onafhankelijk zijn van LMS-accounts. Dit probleem is opgelost.

+++

+++Update 42

Update 42

Releasedatum: 11 januari 2019.

* Het invoegen van gebruikersmeldingen kan willekeurig mislukken, waardoor de bijbehorende e-mails niet worden bezorgd. Dit probleem is opgelost.
* `If a Learner is enrolled in Learning Program 1 and a Course in Learning Program 2, when the Learning Transcript is downloaded for a user group or more than one individual, the Learning Transcript may have missing data. This issue is fixed.`

+++

+++Update 41

Update 41Releasedatum: 1 december 2018.

* Beheerders kunnen bepalen welke machtigingen de studenten krijgen om quizscores in Studenttranscripten te bekijken. Dit kan via de pagina Instellingen worden in- of uitgeschakeld.
* Het invoegen van gebruikersmeldingen kan willekeurig mislukken, waardoor de bijbehorende e-mails niet worden bezorgd. Dit probleem is opgelost.
* Gegevens over Bestede leertijd verschijnen niet in het Studenttranscript en op het Dashboard Rapporten. Dit probleem is opgelost.
* Informatie over activiteiten zoals inschrijving/voltooiing is mogelijk niet aanwezig in het Studenttranscript dat door een manager is gedownload. Dit is opgelost.
* Modules die deel uitmaken van een cursus waar een student nog mee bezig is, worden als voltooid in het Studenttranscript weergegeven. Dit probleem is opgelost.
* Het Studenttranscript geeft de gedownloade gegevens niet weer volgens het geselecteerde datumbereik. Dit probleem is opgelost.
* Voor gebruikers aan wie alleen de rol Auteur is toegewezen, worden catalogi niet weergegeven. Dit probleem is opgelost.
* Wanneer een aangepaste rolbeheerder het Studenttranscript downloadt, bevat het gedownloade rapport geen informatie over de LO&#39;s die alleen deel uitmaakten van standaardcatalogi. Dit probleem is opgelost.
* Het totaalaantal gebruikers en de lijst met gebruikers op de pagina Gebruikersgroep komt niet overeen. Dit is opgelost.
* De pop-up van het Leerprogramma verschijnt niet, zelfs niet wanneer deze is ingeschakeld, en gebruikers worden omgeleid naar de LO-pagina. Dit probleem is opgelost.
* Wanneer de wachtlijst is gewist en de studenten voor een cursus worden ingeschreven, kan de beheerder een e-mailbericht ontvangen met zijn/haar naam in plaats van de naam van de student. Dit probleem is opgelost.
* Achternaam wordt mogelijk niet weergegeven in de gebruikersinterface voor een gebruiker die via de POST-gebruikers-API is toegevoegd. Dit probleem is opgelost.

+++

+++Update 40

Update 40

Releasedatum: september 2018.

Prestatieverbetering

* Gebruikers ondervinden time-outs tijdens het downloaden van een groot aantal studenttranscripten. Dit probleem is opgelost.
* Gebruikers ondervinden vertragingen tijdens het downloaden van een groot aantal inschrijvingsrapporten waarin de quizscore van de student is vastgelegd. Dit probleem is opgelost.
* Het downloaden van een groot aantal quizscorerapporten duurt langer dan normaal. Dit is opgelost.
* Wanneer de student een leerprogramma voltooit, verschijnt het L1-feedbackformulier niet automatisch, zelfs wanneer de automatische pop-up door de beheerder is ingeschakeld. Dit probleem is opgelost.
* Het is mogelijk dat in de gedownloade rapporten Audittrail van gebruiker en Audittrail van inhoud de kolommen Gewijzigd in gebruikersnaam en Gewijzigd in e-mailadres van gebruiker niet zijn vastgelegd. Het rapport geeft in dergelijke gevallen Systeem weer. Dit is bijgewerkt zodat Onbekend wordt weergegeven.

+++

+++Update 39

Releasedatum: 19 mei 2018.

* In deze release van Adobe Learning Manager worden nieuwe functies en verbeteringen uitgerold. Het biedt de mogelijkheid om aangepaste rollen te maken, cataloguslabels toe te voegen, gebruikers leegte, tags te beheren, leerobjecten een andere naam te geven, Slack-integratie, nieuwe connectorintegraties, ondersteuning voor xAPI en nog veel meer. Ga voor meer informatie over de nieuwe functies en verbeteringen naar  [Overzicht van de nieuwe functie](../whats-new.md#main-pars_text).

* Learning Manager voldoet aan de AVG. Zie voor meer informatie [Compatibiliteit van Learning Manager met AVG](/help/migrated/kb/prime-gdpr.md).

## Bekend probleem {#knownissue}

* De hyperlink naar het aantal cursussen en certificeringen binnen het modaal venster Tags bevat schaduwcursussen en terugkerende certificeringen. Wanneer u op de hyperlink klikt, worden deze cursussen en certificeringen niet in de lijst weergegeven, waardoor de cijfers niet overeenkomen.

+++

+++Update 38

* Studenten met de status In behandeling of met de status In afwachting van acceptatie werden als voltooid gemarkeerd. Dit probleem is opgelost.
* Wanneer een docent alle studenten zoekt en selecteert, verschillen het aantal geselecteerde studenten en het getoonde aantal. Dit probleem is opgelost.
* Wanneer u een student zoekt en deze selecteert en aanwezigheid markeert, kan de leermanager aanwezigheid voor alle studenten markeren. Dit is opgelost.
* Leermanager geeft de tijd in e-mails weer in 24-uursnotatie. Dit is opgelost. De tijd wordt nu weergegeven in 12-uursnotatie.
* Wanneer een manager een student aanwijst voor een cursus met behulp van de knop Aanwijzen op de meldingenpagina, wordt het modale venster Aanwijzen niet geladen. Dit is opgelost.
* In geëxporteerde Excel-rapporten zou de deadline (inschrijvingsdatum + dagen om de waarde in automatische instantie van de LO&#39;s te voltooien) onjuist worden weergegeven. Dit probleem is opgelost.

* Zoekresultaten van gebruikers worden leeg weergegeven wanneer er geen gebruikers aanwezig zijn in de groep waarin gezocht wordt. Dit is nu opgelost.
* Managers kunnen niet worden verwijderd, zelfs niet als er geen directe rapporten zijn. Dit probleem is opgelost. Managers kunnen nu worden verwijderd.
* Functie om voortgang van module opnieuw in te stellen werkt niet. Dit is nu opgelost.
* Verwijderde certificering kan worden weergegeven in de widget voor studenten. Dit probleem is opgelost.
* Het probleem van het berekenen van de effectiviteit van de cursus is opgelost.

* Probleem bij de integratie van nieuw Connect-account is opgelost.
* Automatische pop-up van L1-feedback verschijnt niet als deze is ingeschakeld voor niet-standaardinstanties. Dit probleem is opgelost.
* Docenten kunnen aanwezigheid voor alle gebruikers niet tegelijk markeren voor sessies die deel uitmaken van het leerprogramma/certificering. Dit is opgelost.

+++

+++Update 37

Releasedatum: 25 maart 2018.

In de Adobe Learning Manager-versie van maart 2018 worden aantrekkelijke nieuwe functies en verbeteringen uitgerold. Het biedt u de mogelijkheid om rapporten van de audittrail van gebruikers en aanmeldings-/toegangsrapporten te genereren, studenten de mogelijkheid te bieden cursusinstanties te kiezen, klaslokalen en virtuele lesruimten te verbeteren, en nog veel meer. Deze release omvat daarnaast ook bugfixes en prestatieverbeteringen.

Als u alle nieuwe functies in deze versie wilt lezen, raadpleegt u  [Nieuwe functies in Adobe Learning Manager](../whats-new.md).

### Bekend probleem {#KnownIssue-1}

**Probleem:** Het openen van een aantal specifieke leerobjecten met Internet Explorer v11.1478.10586.0 kan ertoe leiden dat de leermanager vastloopt.

**Oplossing:** Werk uw Internet Explorer 11-browser bij naar de nieuwste versie door contact op te nemen met het IT-team in uw organisatie.

+++

+++Update 36

Releasedatum: 22 januari 2018.

### Opgeloste problemen {#issuesfixed}

* Bij een wijziging in de instelling van de e-mailsjabloon verdwijnt de E-mailbanner. Dit probleem is opgelost.
* Studenten kunnen geen persoonlijke taakhulpen toevoegen/starten. Dit is opgelost.
* Aangepaste gebruikersgroepen in een account worden niet weergegeven in het gebruikersgroepveld in het modale venster Toevoegen/bewerken. Dit probleem is opgelost.
* Als de naam van een badgeafbeelding ruimte bevat, wordt deze mogelijk niet weergegeven op de startpagina voor de student.
* Wanneer een ingeschreven gebruiker uit een cursus wordt verwijderd, worden het cursus- en quizrapport niet gegenereerd voor die specifieke cursus. Dit probleem is opgelost.
* Als de beheerder het aantal aangewezen plaatsen voor een manager wijzigt, wordt het aantal verkeerd weergegeven in het aanwijzingsverzoek wanneer dit vanuit een ander venster wordt geopend. Dit probleem is opgelost.
* Bij conversie van een externe gebruiker naar een interne gebruiker, wordt de gebruiker niet aan de groep Alle interne studenten toegevoegd. Dit probleem is opgelost.
* Als u naar een individuele student zoekt, deze selecteert en de uitschrijfactie uitvoert, worden alle studenten in die groep uitgeschreven. Dit probleem is opgelost.
* U kunt als beheerder het selectievakje niet gebruiken om een student binnen de certificeringen te selecteren. Dit probleem is opgelost.
* Het maken en updaten van gebruikersgroepen met meer dan 600 individuele gebruikers mislukt. Dit probleem is opgelost. U kunt nu gebruikersgroepen met meer dan 600 individuele gebruikers maken.
* Als u een aangepaste gebruikersgroep verwijdert die deel uitmaakt van een andere aangepaste gebruikersgroep, rolt de intersectieregel het gebruikersnummer naar de hogere groep door. Dit probleem is opgelost.
* Wanneer de standaardcatalogus is uitgeschakeld en er een nieuwe catalogus wordt gemaakt en de manager toegang heeft tot deze nieuw gemaakte catalogus, kan hij mogelijk geen cursus onder die catalogus zoeken. Dit probleem is opgelost.
* Gebruikers van mobiele toepassingen ontvangen geen L1-feedback als pushberichten. Dit is opgelost.

+++

+++Update 35

Releasedatum: 7 januari 2018.

Deze release van Learning Manager biedt u prestatie-optimalisaties om de schaalbaarheid, prestaties en veiligheid te verbeteren.

### Verbeteringen {#enhancements}

* Ervaar flexibel zoeken wanneer u zoekt naar cursussen en gebruikers in alle toepassingen. Dit omvat zoeken in cursussen, gebruikers en gebruikersgroepen.
* Ondersteunt het gebruik van de Box-connector om Learning Manager met externe systemen te integreren om gegevenssynchronisatie te automatiseren. Zie [Box connector](../integration-admin/feature-summary/connectors.md#main-pars_header_302653946) voor meer informatie.
* Bijgewerkte CSV-specificaties die u kunt gebruiken om uw bestaande LMS-migratiegegevens toe te wijzen. Gebruik de nieuwste downloadbare CSV-specifications en sample-csvs zip-bestanden om inzicht te krijgen in de voorgeschreven indeling van in te voeren gegevens. Zie [Migratiehandleiding](../integration-admin/feature-summary/migration-manual.md) voor meer informatie.

+++

+++Update 34

### Opgeloste problemen {#IssuesFixed-1}

* Aankondigingen mislukken wanneer het aantal gebruikers groot is. Dit probleem is opgelost.
* Bij openen van Learning Manager-account via de subdomein-URL in de EU worden gebruikers naar een andere pagina doorverwezen. Dit probleem is opgelost.
* Wanneer een LP wordt besteld, moet een student de LP alleen in de opgegeven volgorde kunnen gebruiken. Studenten konden cursussen die niet werden weergegeven, eerst volgen via de cursushyperlinks. Dit probleem is opgelost. Studenten kunnen een cursus pas starten nadat hij de vorige heeft voltooid.

* Foutmelding van niet-ondersteunde browserversie verschijnt niet in niet-ondersteunde versies van Internet Explorer (IE 7, IE 8, IE 9 en IE 10) en Safari (versie 7, 8 en 9). Dit probleem is opgelost.



+++

+++Update 33

Releasedatum: 5 oktober 2017.

### Opgeloste problemen {#IssuesFixed-2}

* Wijzigingen in een gedeelde cursus worden niet doorgegeven aan het gedeelde account als de auteur de cursus automatisch opslaat in het oorspronkelijke account. Dit probleem is opgelost.
* Voor specifieke Leerbeheerprojecten werd content soms vastgezet in de Fluidic Player. Dit probleem is opgelost.

* De kalenderlijst onder de widget Studentenagenda op het Studentendashboard verschijnt in willekeurige volgorde. Dit probleem is opgelost. De lijst wordt nu op een overzichtelijke manier weergegeven.
* Bij het markeren van aanwezigheid met behulp van de optie Alles selecteren, worden studenten voor alle leerobjecten voor dezelfde sessie als Aanwezig gemarkeerd. Dit probleem is opgelost.
* In bepaalde schermen met hoge resolutie werden de bannerafbeelding en tekst in de e-mail van Learning Manager niet goed uitgelijnd en afgekapt. Dit is opgelost.
* Bepaalde e-mails van Learning Manager, zoals e-mails zonder enige meldingsgegevens, werden niet geactiveerd voor de gebruikers. Voorbeeld: e-mail ontvangen bij het maken en inschakelen van een extern profiel en e-mail ontvangen bij het configureren van een Connect-account. Dit probleem is opgelost.
* Wanneer u een LP maakt, een herinnering instelt, gebruikers inschrijft en vervolgens de deadline van de instantie wijzigt, wordt de gewijzigde deadline mogelijk niet weergegeven voor de herinneringen. Dit is opgelost. De herinneringen hebben nu de gewijzigde deadline.
* In bepaalde gevallen waren voor inhoud die is gemaakt met Adobe Presenter het totaal en de verstreken tijd in de Fluidic Player niet gelijk aan de inhoud. Dit probleem is opgelost.
* In bepaalde gevallen is de optie om toe te voegen nog steeds ingeschakeld nadat u een leerprogramma aan een catalogus hebt toegevoegd. Dit probleem is opgelost.
* Als u Leerbeheer opent in een apparaatbrowser, wordt een optie weergegeven voor het ervaren van Leerbeheer op de apparaatapp. Klik op Ja om de Play Store (Android) te starten als de app niet is geïnstalleerd, of start de app als deze is geïnstalleerd (in Android en iOS). Er waren problemen met deze workflow. Deze zijn opgelost.

+++

+++Update 32

Releasedatum: 17 augustus 2017.

### Opgeloste problemen {#IssuesFixed-3}

**Cursus met meerdere moduleversies wordt teruggedraaid naar de vorige versie bij een verwijderingsactie.**

Wanneer een cursus meerdere moduleversie-items heeft voor specifieke modules, wordt de module bij verwijdering teruggedraaid naar de vorige versie en niet volledig verwijderd. Dit probleem is opgelost.

**Wijzigingen in een gedeelde cursus worden niet doorgegeven als deze automatisch wordt opgeslagen door deze tussen tabbladen te verplaatsen.**

Wijzigingen in een gedeelde cursus worden niet doorgegeven naar een tenantaccount als de auteur in het bovenliggende account de cursus automatisch opslaat door naar het volgende tabblad te gaan. Dit probleem is opgelost.

**Gebruikers kunnen de deadline van instanties niet wijzigen voor een cursus met enkel activiteiten.**

Gebruikers konden de deadline van een instantie niet wijzigen in activiteitscursussen, omdat de vorige deadline dan werd hersteld. Dit probleem is opgelost.

**Geen mogelijkheid om een unieke id te gebruiken nadat deze uit een leerobject is verwijderd.**

Wanneer u een unieke ID aan een cursus toewijst en deze verwijdert, kunt u de ID niet meer gebruiken. Dit probleem is opgelost.

**Een leerprogramma dat al is ingeschreven als onderdeel van een leerplangebeurtenis, verschijnt opnieuw als onderdeel van een andere gebeurtenis in de Learner-app.**

Als een leerprogramma al is ingeschreven als onderdeel van een leerplangebeurtenis, verschijnt het opnieuw als onderdeel van een andere gebeurtenis in de Learner-app. Dit probleem is opgelost.

**Studenten krijgen herinneringsmails met onjuiste deadline of sessietijd.**

Studenten kregen vaak e-mails met onjuiste herinneringen voor de deadline of de sessietijd vanwege tijdzonecorrecties. Dit probleem is opgelost.

**De tijdlijn van het gamificationleaderboard toont externe studenten als hij wordt omgezet van een externe student in een interne student.**

De tijdlijn van het gamificationleaderboard van een interne student kan externe student tonen wanneer deze van een externe naar een interne student wordt geconverteerd. Dit probleem is opgelost.

**Het UUID-veld voor een student wordt in bewerkbare indeling weergegeven terwijl er één gebruiker en CSV-gebruikers in een UUID-account worden gemaakt.**

De student zag het UUID-veld tijdens het invullen van diens profiel, zelfs wanneer de beheerder de UUID voor één gebruiker of CSV-gebruikers heeft verstrekt. Dit probleem is opgelost.

**In bepaalde gevallen wordt de bestede leertijd niet vastgelegd in rapporten.**

Bestede leertijd werd niet weergegeven in rapporten voor een student

* Als zijn/haar aanwezigheid automatisch wordt gemarkeerd door het systeem voor het aansluiten van modules.
* Wanneer een QR-code wordt gescand voor CR- en VC-modules met behulp van de toepassing Learning Manager-apparaat.

**Deze release van Learning Manager introduceerde ook verbeteringen en foutoplossingen met betrekking tot de apparaatspeler.**

* Problemen met de voltooiing van activiteitenmodules. Dit is opgelost.
* Wanneer de student een video in staande modus afspeelt, werken de knoppen +10 en -10 niet. Dit is opgelost
* Verbeterd afspelen van bepaalde voorbeeldprojecten bij het afspelen op een Android-apparaat (mobiel en tablet) waar inhoud voorheen zou flikkeren.
* Wanneer u een nieuwe notitie toevoegt, moet het notitievenster worden gesloten en het afspelen in de speler worden hervat. In bepaalde gevallen gebeurt dit niet. Dit is opgelost.
* Wanneer u de notities opent die aan een module zijn toegevoegd, wordt de knop Sluiten niet weergegeven. Dit probleem is opgelost.
* Wanneer de student het notitievenster opent met behulp van Notities markeren, moet deze mogelijk twee keer op het notitiepictogram klikken om het deelvenster te sluiten.
* Als u op de inhoudsopgave klikt, wordt deze mogelijk niet automatisch samengevouwen en moet u de inhoud handmatig sluiten. Dit probleem is opgelost.
* Een cursus die een module met meerdere talen heeft, geeft niet alle beschikbare talen weer, omdat de schuifbalk niet meeschaalt. Dit is opgelost.
* Wanneer u een activiteitenmodule van een externe cursus opent in de modus Liggend in een speler, wordt tekstrichting mogelijk niet aangepast wat scrollen moeilijk maakt. Dit is opgelost.
* Het tikgebied voor de sluitknop van de speler is in online en offline modus vergroot.
* De inhoudsopgave wordt niet automatisch gesloten wanneer de oriëntatie van het apparaat wordt gewijzigd. Dit is opgelost.
* Enkele kleine problemen met betrekking tot de gebruikersinterface, zoals de uitlijning van de afspeelknop, het keuzerondje en andere instellingen in de liggende en staande modus, zijn opgelost.

* Het probleem met de zoekbalk die wordt weergegeven, zelfs als de afspeeloptie voor de show uitgeschakeld is in inhoud, is opgelost.
* De sluitknop van de speler was niet zichtbaar voor bepaalde projecten wanneer de oriëntatie van het apparaat was gewijzigd. Dit is opgelost.
* Het probleem dat de inhoudsopgave van de module in liggende modus wordt afgekapt op de apparaatspeler, is opgelost. De inhoudsopgave was soms niet zichtbaar voor inhoud in de apparaatspeler. Dit is ook gecorrigeerd.

**In deze release van Learning Manager worden ook de onderstaande verbeteringen en oplossingen voor de apparaattoepassing.**

* Pushmelding met betrekking tot voltooiingsdeadlines wordt niet geleverd op bepaalde apparaten. Dit probleem is opgelost.
* We ondersteunen nu ook de levenscyclus van leerobjecten op apparaattoepassing. Studenten hebben nu toegang tot de nieuwste inhoud in leerobjecten als deze door de auteur zijn bewerkt.

* Problemen met de toepassingsoriëntatie (inclusief de standaardoriëntatie - staande modus) van de Learning Manager-toepassing is opgelost.
* Er is geen optie is om de inhoud bij te werken wanneer de gebruiker van offline naar online modus overgaat.
* Het bestellen van modules wordt nu ondersteund voor cursussen in apparaattoepassing in online modus.

* Als een gebruiker geen taakhulpen heeft gedownload, kan het klikken op het tabblad Mijn taakhulpen in de offline modus ertoe leiden dat de app in IOS vastloopt en een bericht verschijnt met de melding dat er een fout is opgetreden bij het laden van gegevens in Android. Dit is opgelost.
* De Learning Manager-toepassing wordt gesloten of geeft een fout als de cursus wordt geopend direct nadat internet is uitgeschakeld, zelfs als het een gedownloade cursus is. Dit probleem is nu opgelost.
* Wanneer u de QR-code scant, wordt soms de vastgelegde afbeelding van de vorige QR-codescan weergegeven. Dit is opgelost.
* Als u probeert een taakhulp te verwijderen die al op het tabblad Taakhulpen is toegevoegd, wordt er een foutbericht weergegeven. Dit probleem is opgelost.

+++

+++Update 31

Releasedatum: 16 juli 2017.

### Verbeteringen {#Enhancements-1}

**Gamification**

In deze release wordt gamification uitgebreid. Externe gebruikers kunnen nu deelnemen aan Gamification. Als beheerder kunt u de omvang van gamification definiëren door de omvangsinstellingen te wijzigen. U kunt gamification selectief inschakelen onder vergelijkbare profielgebruikers, groepen of locatie.

**Verbeteringen voor externe gebruikers**

Dankzij deze verbetering kunt u een tijdsbereik instellen waarna gebruikers automatisch worden verwijderd na de periode van inactiviteit. De beheerder kan hierdoor ook de gebruiker opnieuw toevoegen als externe student voor zowel automatisch als handmatig verwijderde studenten.

**Taakhulp, aankondigingen en uitschrijvingsrapport**

Taakhulpen zijn trainingsinhoud waartoe een studenten toegang hebben zonder dat zij zich moeten inschrijven voor een specifiek leerobject zoals een cursus of leerprogramma. Dankzij deze verbetering kunnen beheerders het Taakhulpenrapport extraheren en downloaden. Als beheerder kunt u ook een rapport genereren van alle aankondigingen die door u zijn verzonden. Beheerders en managers kunnen ook een rapport extraheren van de studenten die zijn uitgeschreven.

**Leermanagerconnectoren**

U kunt nu gebruikersvaardigheden exporteren naar een FTP-locatie voor integratie met systemen van derden via de optie Gegevensexport. U kunt de verbindingsnaam voor uw integratie opgeven en kiezen of u interne gebruikers wilt importeren of gebruikersvaardigheden wilt exporteren door deze te configureren of op verzoek op te halen.

**Cursusinstanties kopiëren**

U kunt nu de instantie-URL kopiëren door op de vervolgkeuzepijl in de rechterbovenhoek van een instantie te klikken.

### Opgeloste problemen {#IssuesFixed-4}

**Gebruikers ontvangen geen agenda-uitnodiging wanneer ze voor een leerprogramma worden ingeschreven**

Gebruikers kregen soms geen agenda-uitnodiging (ICS-bestand) wanneer ze zich inschrijven voor Leerprogramma&#39;s, Certificaten met Klaslokaal, en Connect-sessies. Dit probleem is opgelost. Gebruikers ontvangen nu bij de inschrijvingsmail ICS-bestanden als bijlagen met de sessiegegevens.

**Beschrijving van activiteit verschijnt in het Engels, zelfs als deze in meerdere talen beschikbaar is**

Een gebruiker wiens taalvoorkeur niet op Engels is ingesteld, kan de beschrijving van de activiteitenmodule toch in het Engels zien. Dit probleem is opgelost.

+++

+++Update 30

Releasedatum: 30 juni 2017.

### Verbeteringen {#Enhancements-2}

**Ondersteuning voor meerdere leerobjecten in leerplan**

Als beheerder of auteur kunt u nu meerdere leerobjecten aan een Leerplan toewijzen. Als een van de leerobjectinstanties wordt gearchiveerd of verloopt, wordt het hele leerplan automatisch uitgeschakeld. Dankzij deze verbetering kunt u ook zoeken naar de velden **[!UICONTROL Voltooid leermateriaal]** en **[!UICONTROL Leermateriaal toewijzen]** met behulp van unieke ID&#39;s voor leerobjecten.

**Toegankelijkheid**

Met deze update ondersteunt de leerervaring van Learning Manager nu sectie 508 voor toegankelijkheid. Learning Manager is ook compatibel met de nieuwste versie van **[!UICONTROL JAWS]**. Deze functie wordt alleen ondersteund voor de Learner-toepassing. Gebruik Internet Explorer 11, Windows Chrome of macOS Safari om toegang te krijgen tot deze functie.

### Opgeloste problemen {#IssuesFixed-5}

**Onjuiste informatie in bepaalde tijdzones**

In herinneringen voor deadlines werd het aantal resterende dagen voor studenten in bepaalde tijdzones onjuist vermeld. Dit probleem is opgelost.

**Problemen met het leerprogramma in het geval van een verlopen programma-instantie**

Er waren problemen bij het starten van modules vanuit Leerprogramma als programma-instantie was verlopen. Hierdoor werkte de uitbreiding van de module niet, en studenten konden de speler niet starten en de inhoud niet bekijken. Dit probleem is opgelost.

**Vertaalproblemen in de toepassing in Learner-app**

Learning Manager-gebruikers ondervonden bepaalde vertaalproblemen in de Learner-app. Deze problemen zijn opgelost.

**Problemen met een abonnement op een vaardigheid**

In bepaalde gevallen konden studenten zich niet abonneren op een nieuwe vaardigheid. Dit probleem is opgelost.

+++

+++Update 29

Releasedatum: 9 april 2017.

### Nieuwe functies {#newfeatures}

Voor een lijst met nieuwe functies en verbeteringen in de Learning Manager-release van april raadpleegt u [Nieuwe functies.](../whats-new.md)

**Op widgets gebaseerde Learner-app**

Gebruik widgets op de startpagina om uw cursussen, vaardigheden en resultaten te beheren. Gebruik de zoekbalk om het gehele LMS te doorzoeken dat alle leerobjecten, catalogi, vaardigheden, notities en discussies omvat

Ga voor meer informatie over de nieuwe startpagina naar  [Startpagina voor studenten in Leermanager](../learners/feature-summary/getting-started-learner.md).

**Beheerdersinstellingen voor het Studentendashboard**

Als beheerder kunt u de startpagina van de student beheren door verschillende widgets in en uit te schakelen.

**Mobiele app van Learning Manager voor studenten**

De nieuwe mobiele Learning Manager-app laat studenten de app gebruiken om zich in te schrijven voor cursussen en deze te volgen. De app kan ook gebruikt worden om dashboards te beheren.

Ga voor meer informatie over het gebruik van Learning Manager in mobiele telefoons naar  [Leerprogramma van Learning Manager voor mobiele telefoons](../learners/feature-summary/ipad-android-tablet-users.md#main-pars_header_1451175907).

**Aanwezigheid noteren met behulp van QR-code**

Gebruik de QR-code scannen om uw aanwezigheid voor klassikale sessies met een mobiele apparaat te markeren.

**Docentrol**

Learning Manager heeft nu modules voor docenten. Docenten kunnen modulesessies beheren, waaronder de tijd, locatie en het maximumaantal plaatsen, voor de modules die aan hen zijn toegewezen.

Zie voor gedetailleerde informatie over docenten  [Docenten in Leermanager](../instructors/feature-summary/getting-started.md#main-pars_header).

**Collega-account**

Als u een beheerder bent, kunt u collega-accounts maken waarmee u uw gekochte plaatsen kunt delen.

Zie voor meer informatie over het maken en beheren van collega-accounts  [Collega-accounts](../administrators/feature-summary/peer-account.md#main-pars_text).

**Aanbod equivalente cursussen**

Gebruik **[!UICONTROL Nieuwe taal toevoegen]** wanneer u een module of cursus toevoegt om deze beschikbaar te maken in meerdere talen en in verschillende indelingen.

**Studenttranscript**

Learning Manager biedt managers en beheerders de mogelijkheid om transcriptgegevens te downloaden om de leergeschiedenis van zowel individuen als teams bij te houden.

**Integratie met andere contentproviders**

Learning Manager heeft drie nieuwe connectoren in deze release geïntroduceerd, zodat studenten cursussen van de volgende contentproviders kunnen openen en volgen: Lynda.com, getAbstract en Harvard ManageMentor.

Om te weten te komen hoe te om elk van deze schakelaars te vormen en te gebruiken, zie  [Connectoren](../integration-admin/feature-summary/connectors.md#main-pars_header).

**Uniek ID voor leerobjecten**

Tijdens het maken van leerobjecten kunnen auteurs en beheerders nu unieke id&#39;s opgeven voor de cursussen, leerprogramma&#39;s of certificeringen. Als u een unieke ID wilt inschakelen wanneer u een leerobject maakt, klikt u op Instellingen > Algemeen. Selecteer het vakje Inschakelen naast de optie Unieke ID&#39;s voor leerobject.

**Discussieboard voor studenten**

Gebruik het Discussieboard in cursussen om met uw collega&#39;s en docenten te communiceren. Als student kunt u alle berichten voor cursussen bekijken. U kunt echter ook alleen de berichten verwijderen die u hebt ingevoerd. Zie voor meer informatie over het Discussieboard  [Weergeven van en deelnemen aan discussies](../learners/feature-summary/courses.md#main-pars_header_1772461149).

### Verbeteringen {#Enhancements-3}

**X van y cursussen**

De voltooiingscriteria voor leerobjecten zoals cursussen, certificeringen en leerplannen kunnen zo worden ingesteld dat studenten slechts X van Y modules of cursussen hoeven te voltooien. Auteurs kunnen ook de criteria voor de voltooiing van certificeringen en leerplannen bepalen.

Zie voor meer informatie over deze functie  [Voltooiingscriteria voor cursussen](../learners/feature-summary/courses.md#main-pars_image_1164377098).

**Cursusmoderatie**

Beheerders ontvangen nu meldingen telkens wanneer een auteur modules bewerkt of bijwerkt en een cursus opnieuw publiceert.

**Beheerderinstellingen voor het herstellen van modules**

Beheerders kunnen nu de optie Modules herstellen configureren zodat studenten een niet gehaalde of voltooide cursus opnieuw kunnen instellen.

**Rapportencatalogus**

Wanneer u rapporten maakt in Leerbeheer, kunt u nu rapporten en grafieken voor catalogi genereren.

**Verbeteringen van leerplannen**

Beheerders kunnen nu leerplannen van het type Op datum maken. Een beheerder kan met het leerplan Op datum de gebeurtenisnaam specificeren, de datum voor de gebeurtenis kiezen en de gebruikersgroep waartoe de gebeurtenis behoort selecteren.

**Cursusspecifieke inschrijvingsberichten**

Beheerders kunnen nu cursusspecifieke inschrijvingsberichten configureren en naar studenten e-mailen.

**Sticky-aankondigingen**

Als beheerder kunt u nu de functie Sticky voor aankondigingen inschakelen.

**Ondersteuning voor URL in aankondigingen**

U kunt URL&#39;s toevoegen als aankondigingen door de URL in HTML toe te voegen.

**Nieuwe leveringstypes toevoegen (cursussen)**

Met Adobe Learning Manager kunt u nu leveringstypen toevoegen voor uw cursussen.

**Verbeteringen van auteursrol**

Voorheen konden auteurs alleen modules en cursussen maken. Auteurs kunnen nu ook certificeringen en leerprogramma&#39;s voor studenten maken.

**Auteursrol aan externe gebruikers**

Als beheerder kunt u nu auteursrollen aan externe gebruikers toewijzen.

**Meerdere auteurs**

Met Learning Manager kunnen meerdere auteurs nu tegelijkertijd dezelfde inhoudsgroep bewerken.

**Verbeteringen van Adobe Connect**

U kunt nu één Adobe Connect-URL configureren met meerdere Learning Manager-accounts.

**Ondersteuning voor nieuwe talen**

Ondersteuning voor Japans, Braziliaans Portugees en Italiaans is vanaf deze release beschikbaar.



+++

+++Update 28

Releasedatum: 30 januari 2017

### Opgeloste problemen {#IssuesFixed-6}

#### Accountinstellingen {#accountsettings}

Wanneer u als Beheerder op Extern profiel klikt en Acties > Profiel wijzigen kiest, worden niet alle profielen weergegeven. Dit probleem is nu opgelost.

#### Levenscyclus van cursus {#courselifecycle}

* Wanneer u een cursus start die is gemaakt met het e-learningprogramma van de Biz-bibliotheek, werkte de actie &quot;Hervatten&quot; niet. Dit probleem is opgelost.
* Sommige gebruikers konden cursussen niet starten op een iPad via de cursuslink in Aankondigingen. Dit is nu opgelost.
* Wanneer u op de knop Doorgaan in het programma van de student klikt, hebt u de cursussen niet op volgorde kunnen openen. Dit is nu opgelost.
* Het label Cursusoverzicht voor cursussen in het programma van de student was eerder misplaatst. Dit probleem is nu opgelost.

#### Learner-app {#learnerapp}

* Als u op uw apparaat een berichtafbeelding op volledig scherm opent, kunt u niet naar de toepassing terugkeren. Dit is nu opgelost.
* Tincan-inhoud die vanuit Captivate werd geüpload, werd niet afgespeeld in online modus op Android- en iOS-besturingssystemen. Dit probleem is opgelost.

#### Cursusrapporten {#coursereports}

In Learning Manager worden onjuiste studenttranscriptrapporten gegenereerd wanneer de cursus meerdere versies van modules heeft. Dit is nu opgelost.

#### API-laag {#apilayer}

Er trad een fout op telkens wanneer u de informatie over de versie van de module probeerde op te halen met behulp van AP/courses/{coursesid}. Dit is nu opgelost.

+++

+++Update 27

Releasedatum: 23 december 2016.

### Nieuwe functies {#Newfeatures-1}

Adobe stelt ondernemingen in staat om de opleidingsgegevens en trainingsinhoud van hun organisatie van hun bestaande Learning Management Systems (LMS) naar de Learning Manager LMS-toepassing te migreren.

Learning Manager biedt de tools en sjablonen waarmee de integratiebeheerder van uw organisatie de migratietaken kan opzetten en uitvoeren.

Raadpleeg voor meer informatie over de functie Migratie  [Help bij Migratiehandleiding](../integration-admin/feature-summary/migration-manual.md)

### Verbeteringen {#Enhancements-4}

**Gebruikersregistratie**

Als beheerder kunt u nu specifieke domeinnamen toevoegen terwijl u externe gebruikers toevoegt. Wanneer studenten zich bij het account registreren, kunnen ze alleen e-mailadressen van die domeinnamen invoeren.

U kunt ook e-mailverificatielinks naar het e-mailadres van gebruikers sturen wanneer zij zich bij het account registreren. Zie voor meer informatie over deze verbetering  [Gebruikers/gebruikersgroepen toevoegen](../administrators/feature-summary/add-users-user-groups.md#main-pars_header_1217981931).

**Fluidic Player**

U kunt nu de afspeelsnelheid aanpassen met Fluidic Player. U kunt kiezen uit vijf snelheden. U kunt ook het volume van een cursus regelen met Fluidic Player.

Als student kunt u ook 10 seconden vooruit- of achteruitspringen met behulp van de nieuwe pictogrammen aan weerszijden van de afspeelknop in de Fluidic Player. Zie voor meer informatie over deze verbeteringen  [Fluidic Player](../learners/feature-summary/fluidic-player.md).

De verbeteringen van de Fluidic Player zijn alleen van toepassing op video.

+++

+++Update 26

Releasedatum: 6 december 2016.

### Verbetering {#enhancement}

Als onderdeel van deze update biedt Learning Manager een eindpunt [PATCH/gebruikers/{id}](<https://learningmanager.adobe.com/docs/Learning> Managerapi/v1/#!/user/patch_users_id) om gebruikers in een toepassing bij te werken. U moet de beheerdersrol hebben om toegang te krijgen tot dit API-eindpunt. Met****dit eindpunt kunt u de volgende informatie over gebruikers van Learning Manager bijwerken:

* Naam
* E-mail
* Profiel
* Rol
* Manager

### Probleem opgelost {#issuefixed}

**Fluidic Player**

Wanneer u een cursus volgt die in de Captivate is ontwikkeld met  `code cpQuizInfoStudentName` variabele, verscheen de studentnaam niet zoals verwacht. Dit probleem is opgelost.

+++

+++Update 25

Releasedatum: 17 november 2016.

### Verbeteringen {#Enhancements-5}

**Gedeelde catalogi**

Met de functie Gedeelde catalogi kunnen beheerders van verschillende accounts catalogi met leerobjecten delen of verwerven. Als uitbreiding op deze functie ondersteunen we het doorgeven van de updates naar leerobjecten zoals badges, vaardigheden, modules, cursussen, leerprogramma&#39;s, certificaten en taakhulpen.

Raadpleeg voor meer informatie over deze functie  [Help voor gedeelde catalogi](../administrators/feature-summary/catalogs.md#propagation)

**L1- en L3-feedback**

* Het dialoogvenster L1-feedback verschijnt zodra een student een cursus heeft afgerond. De student ontvangt ook een bericht over het invullen van L1-feedback.
* De functie voor L1- en L3-feedback biedt de optie om beschrijvende vragen toe te voegen. Beheerders kunnen deze beschrijvende vragen voor studenten toevoegen. Deze is in aanvulling op de standaard vragenreeks van Learning Manager. U kunt twee beschrijvende vragen toevoegen voor L1-feedback en één vraag voor L3-feedback.\
  Raadpleeg voor meer informatie over deze functie [Help voor beschrijvende vragen over L1- en L3-feedback](../administrators/feature-summary/courses.md#descriptive)

**Gebruikers exporteren**

* Op verzoek van enkele grote zakelijke gebruikers is er een nieuwe optie toegevoegd om de lijst van alle gebruikers in het Learning Manager-account te downloaden. Klik in Beheerdersaanmelding op **[!UICONTROL Gebruikers]** in het linkerdeelvenster en klik op **[!UICONTROL Gebruikersgegevens exporteren]** om de lijst met gebruikers als Excel-blad te downloaden.

### Opgeloste problemen {#Issuesfixed-1}

**Cursusinschrijvingen**

* Wanneer een beheerder de inschrijvingen voor een cursus probeert te bekijken via het tabblad Studenten, worden een aantal namen van ingeschreven studenten niet weergegeven. Dit probleem is opgelost.

**Cursussen toevoegen**

* Er treedt een fout op wanneer een auteur bij het toevoegen van een vaardigheid aan de cursus een spatie achter de cursusnaam zet. De cursus wordt niet opgeslagen. Dit probleem is opgelost.

**Cursussen volgen**

* Sommige studenten konden in een cursus op volgorde niet van de ene module naar de andere gaan, omdat de modules niet als voltooid werden gemarkeerd. Dit probleem is opgelost.
* Studenten konden niet tussen modules navigeren in de inhoudsopgave van een cursus op volgorde in de modi Normaal en Opnieuw bekijken. Dit probleem is opgelost.

**Fluidic Player**

* Wanneer een gebruiker module-inhoud met verborgen frames/dia&#39;s uploadt, geeft de inhoudsopgave in het linkerdeelvenster de verborgen frames/dia&#39;s weer. Dit probleem is opgelost.

**Rapporten**

* Het duurt langer om rapporten te laden in de recentste update van Learning Manager. Dit probleem is opgelost.

+++

+++Update 24

Releasedatum: 12 oktober 2016.

### Verbeteringen {#Enhancements-6}

**Cursusrapporten**

* Voor Learning Manager-accounts met UUID (Universal Unique Identifier), verschijnt de UUID in het cursusinschrijvingsrapport, studenttranscripten en quizscorerapporten.

### Opgeloste problemen {#Issuesfixed-2}

**Taakhulpen**

* Wanneer een student van Leermateriaal>Taakhulpen naar Leermateriaal>Cursussen wilde navigeren, werden de cursussen soms niet geladen zoals verwacht op het tabblad Leermateriaal>Cursussen. Dit probleem is opgelost.

**Gebruikers toevoegen**

* Wanneer één gebruiker aan de Learning Manager-toepassing wordt toegevoegd, ontvangt de gebruiker geen e-mailmelding. Dit probleem is opgelost.
* Beheerders kunnen het CSV-bestand niet downloaden als het uploadproces van de CSV mislukt. Dit probleem is opgelost, Beheerders kunnen de nieuwste CSV downloaden, zelfs als het uploadproces van de CSV mislukt.
* Als een CSV wordt geïmporteerd nadat informatie in kleine letters en hoofdletters van een gebruiker die zichzelf heeft geregistreerd is gewijzigd, worden de gegevens van de gebruiker die zichzelf heeft geregistreerd, niet in de beheerders-UI weergegeven. Dit probleem is opgelost.

**Cursusrapporten**

* Quizscores verschijnen niet voor cursussen, ook al staan de scores in de studenttranscripten. Dit probleem is opgelost.

**Inschrijvingsrapporten**

* De Excel-inschrijvingsrapporten voor de student werden niet gedownload voor de leerobjecten. Dit probleem deed zich voor wanneer niet-ASCII of speciale tekens werden gebruikt in de naam van leerobjecten. Dit probleem is opgelost.

**Gebruikersaanmelding**

* Bij het instellen van een wachtwoord tijdens registreren of opnieuw instellen, verscheen geen foutmelding wanneer het ingevoerde wachtwoord niet in overeenstemming was met het wachtwoordbeleid. Dit probleem is opgelost.

**Cursuseffectiviteit**

* In de studentrol werd de effectiviteit van de cursus weergegeven als een van de **Sorteren op** filteropties, zelfs als een beheerder de cursuseffectiviteit voor studenten heeft uitgeschakeld. Dit probleem is opgelost.

**Certificeringen**

* Wanneer een beheerder studenten uit een terugkerende certificering verwijderde, trad er een fout op en werd de Learning Manager-toepassing beëindigd. Dit probleem is opgelost.

**Rapporten**

* Wanneer een beheerder een certificeringsrapport probeert te genereren met **Einddatum** als optie, werden de inactieve gebruikers niet getoond in het rapport. Dit probleem is opgelost.
* Wanneer een beheerder op de link Cursusrapporten klikte op het tabblad Rapporten>Mijn rapporten, verscheen een pop-upvenster zonder de knop Sluiten. Dit probleem is opgelost.

**Fluidic Player**

* Wanneer een gebruiker de modus Volledig scherm kiest in Fluidic Player terwijl hij een voorvertoning weergeeft van cursussen als beheerder of auteur, wordt het scherm leeg weergegeven. Dit probleem is opgelost.

**Meertalige ondersteuning**

* In antwoord op API-aanroepen van gebruikers verschenen vraagtekens in plaats van Chinese tekens. Dit probleem is opgelost.

**API-laag**

* Er trad een fout op wanneer een gebruiker de standaard catalogus-id probeerde op te halen met behulp van get/catalog/catalog ID API. Een standaardcatalogus-ID kan eruitzien als &#39;970_default&#39;. Dit probleem is opgelost.

**Gebruikersinterface**

* Enkele kleine typfouten in de gebruikersinterface van de Learning Manager-toepassing voor de studentrol zijn verbeterd.

+++

+++Update 23

Releasedatum: 19 september 2016.

### Opgeloste problemen {#Issuesfixed-3}

**Studenttranscripten**

* Als er meer dan twintig inactieve/verwijderde studenten in een account zaten, werden de inactieve studenten na twintig niet weergegeven in de vervolgkeuzelijst voor Zoeken van het dialoogvenster Studenttranscript. Dit probleem is opgelost.
* Als een extern gebruikersaccount was verlopen, werden de studenten ervan niet in het gegenereerde studenttranscript weergegeven. Dit probleem is opgelost.

**Catalogi**

* Sommige klanten hadden problemen met het weergeven van gebruikersgroepen in een catalogus. Zelfs als er meer dan twintig gebruikersgroepen in een catalogus zaten, werden er slechts 20 weergegeven. We hebben dit probleem opgelost door op een pagina 200 gebruikersgroepen weer te geven.

+++

+++Update 22

Releasedatum: 13 september 2016.

In deze updaterelease hebben we een aantal back-endproblemen met productengineering opgelost om de klantervaring te verbeteren.

### Opgeloste problemen {#Issuesfixed-4}

* Er was een probleem met het exporteren van modulegegevens in studenttranscripten wat resulteerde in onjuiste exportgegevens. Dit probleem is opgelost.
* Als een gebruiker een e-mail-ID-extensie met meer dan vier tekens gebruikte, werd deze niet ondersteund. Als een e-mail-ID bijvoorbeeld <abcd@company.world> het werd niet ondersteund omdat de extensiewereld uit meer dan vier tekens bestaat. We hebben dit opgelost om extensies met meer dan vier tekens te ondersteunen.

+++

+++Update 21

Releasedatum: 1 september 2016.

### Verbeteringen {#Enhancements-7}

**Cursuseffectiviteit**

Beheerders kunnen de effectiviteitsfunctie voor cursussen of leerprogramma&#39;s nu aanpassen om de effectiviteitsscore voor studenten te verbergen.

**Externe gebruikers toevoegen**

Learning Manager heeft de maximale limiet voor externe zelfregistraties verhoogd tot 5 cijfers.

**Rapporten**

Alle gedownloade rapporten en studentenlijsten voor alle leerobjecten geven nu verwijderde gebruikers weer met een duidelijke afbakening voor verwijderde gebruikers.

### Opgeloste problemen {#Issuesfixed-5}

**Levenscyclus van cursus**

Wanneer een auteur een gedeelde cursus bewerkte om gewijzigde module-informatie bij te werken, verscheen er soms een waarschuwingsbericht dat de gebruiker niets kan wijzigen omdat eerdere wijzigingen worden verwerkt. Dit probleem is opgelost.

**Meertalige ondersteuning**

Berichten werden niet goed vertaald en weergegeven in enkele functies van de Learning Manager-gebruikersinterface. Dit probleem is opgelost.

**Gebruikers toevoegen**

* Wanneer een verwijderde gebruiker weer werd toegevoegd als één gebruiker, werd de gebruiker niet standaard aan de gebruikersgroep Alle gebruikers toegevoegd. Dit probleem is opgelost.
* Er werd een beperkt aantal profielen weergegeven in dialoogvensters voor profielwijziging voor externe of zelfinschrijving. Paginering is nu geïmplementeerd.

**Taakhulpen**

Telkens wanneer een student het tabblad Taakhulpen opende, verscheen een foutmelding als &#39;Deze taakhulp staat niet meer in uw lijst&#39; voordat de inhoud werd geladen. Dit probleem is opgelost.

**Catalogi**

Tijdens het maken van de catalogus, werkte het filter Sorteren op niet zoals verwacht terwijl cursussen als inhoud aan de catalogus werden toegevoegd. Dit probleem is opgelost.

**Instellingen**

Wanneer een beheerder een subdomein gebruikt dat al door een ander account wordt gebruikt, verschijnt geen foutmelding in de accountinstellingen. Dit probleem is opgelost.

**API-laag**

* Wanneer &#39;include manager&#39; werd gebruikt tijdens het ophalen van gebruikers, werd de volledige hiërarchie van managers opgehaald in plaats van de directe manager van de gebruiker. Dit probleem is opgelost.
* Wanneer een gebruiker met machtigingen voor autorisatie van de studentenomvang gebruikers probeert toe te voegen, verschijnt een algemene foutmelding. Dit probleem is opgelost en de student ziet nu het bericht Onbevoegde toegang.
* Wanneer een gebruiker probeert de laatste gebruiker in een gebruikersgroep te verwijderen, ziet de gebruiker de foutmelding 204. Dit probleem is nu opgelost en er wordt een relevante foutmelding weergegeven waarin staat dat de groep minstens één gebruiker moet hebben.
* Als er aan het begin van de naam een spatie stond, werd deze afgekapt wanneer de gebruikersnaam in GET/users API werd weergegeven. Dit is nu opgelost.
* De conceptcursussen werden ook geretourneerd wanneer de beheerder alle cursussen probeerde op te halen. Deze conceptcursussen moeten privé zijn voor de auteur. Dit probleem is opgelost, conceptcursussen worden niet meer geretourneerd.

**Adobe Connect-integratie**

* De aanwezigheid voor sessies in virtuele Adobe Connect-klaslokalen werd soms niet automatisch gemarkeerd na de sessie. Dit probleem deed zich alleen voor wanneer een docent een aanmeldings-ID gebruikte om zich aan te melden in plaats van een e-mail-ID. Dit is nu opgelost.
* De naam van de docent verscheen soms meerdere malen in de vervolgkeuzelijst Docent wanneer er modules werden gemaakt in virtuele Adobe Connect-klaslokalen. Dit probleem is opgelost.

+++

+++Update 20

Releasedatum: 22 augustus 2016.

### Verbeteringen {#Enhancements-8}

**API-laag**

Als onderdeel van deze update hebben we de volgende nieuwe API&#39;s toegevoegd om aan een aantal klantbehoeften tegemoet te komen:

1. POST Users
1. DELETE Users
1. GET userGroups
1. GET userGroups /{id}
1. DELETE userGroups /{id}/Users
1. POST userGroups /{id}/Users
1. GET /users/userId/userGroups

We hebben ook het bestaande gebruikersmodel uitgebreid met de volgende toevoegingen:

1. Managementmodel is toegevoegd als relatie aan gebruikersmodel
1. userGroupId is als nieuwe parameter toegevoegd aan GetUsers

**Studenttranscript**

Wanneer een gebruiker een studenttranscript genereert voor een student, verscheen het pop-upvenster zeer kort om weer te verdwijnen zonder de gebruiker te vragen iets te doen. We hebben de gebruikerservaring verbeterd met een pop-upvenster dat blijft staan en de gebruiker vraagt om op OK te klikken.

**Adobe Connect-integratie**

Aanmeldings-id staat als een nieuw optioneel veld in de Adobe Connect-integratie-instellingen voor gebruikers die zich niet met hun e-mailadres aanmelden.

### Opgeloste problemen {#Issuesfixed-6}

**Cursusrapporten**

* Wanneer een cursusmodule uit open vragen of enkel enquêtevragen bestaat, verschijnt er bij export een leeg quizscorerapport. Dit probleem is opgelost.
* Het quizscorerapport werd soms niet gedownload wanneer een gebruiker de link Quizscores exporteren gebruikte. Dit probleem is opgelost.

**Cursussen maken**

In de auteursrol verscheen de pagina Instellingen niet voor de cursus wanneer een vaardigheid van de cursus door de beheerder werd gearchiveerd. Dit probleem is opgelost.

**Slimme inschrijving**

Speciale tekens werden niet ondersteund als invoer in het zoekveld waardoor de zoekresultaten niet werden weergegeven. Dit probleem is opgelost.

+++

+++Update 19

Releasedatum: 11 augustus 2016.

### Verbeteringen {#Enhancements-9}

**Slimme inschrijving**

De prestaties van de zoekmachine zijn verbeterd voor nauwkeurigere zoekresultaten.

**Adobe Connect-integratie**

Het verificatie-/authenticatieproces voor integratieverzoeken is verbeterd in de Learning Manager-toepassing.

### Opgeloste problemen {#Issuesfixed-7}

**Gebruikers toevoegen**

* Wanneer er veel Learning Manager-gebruikers waren, duurde het lang voordat gebruikers en gebruikersgroeppagina waren geladen. Dit probleem is opgelost.
* Nadat de beheerder CSV-bestanden met nieuwe gebruikers had geüpload, werd de lijst van gebruikers op de pagina niet bijgewerkt met nieuwe gebruikers totdat de pagina was vernieuwd. Dit probleem is opgelost.
* Na import van gebruikers met CSV werd de waarde van de gebruikers-ID op de pagina soms vervangen door de e-mail-ID. Dit probleem is opgelost.

**Gebruikersgroepen maken**

Het aantal gebruikers werd soms niet weergegeven op de standaardpagina voor gebruikersgroepen in Learning Manager. Dit probleem is opgelost.

**Studenttranscript**

Attribuutwaarden van actieve velden werden onjuist weergegeven in studenttranscripten voor Certificeringen. Dit probleem is opgelost.

**Meerdere accounts delen**

In een scenario waarin een accountbeheerder een cursuscatalogus deelde met de ontvanger en later een test- of voorwerkmodule bijwerkte, werd de inhoud van de test- of voorwerkmodule gebruikt voor het afspelen van de inhoudsmodule voor de ontvanger. Dit probleem is opgelost.

**Thema&#39;s en branding**

Wanneer een beheerder een thema in de toepassing wijzigt met behulp van de widget Livevoorbeeld en van rol verandert, functioneert de widget niet zoals verwacht in de nieuwe rol. Dit probleem is opgelost.

**Meertalige ondersteuning**

Wanneer een beheerder de locatie van de landinstellingen van de toepassing wijzigt in Vereenvoudigd Chinees of Spaans, worden bepaalde menu-inhoud in het linkerdeelvenster, online instructies en pop-upberichten niet in betekenisvolle woorden of zinnen weergegeven. Dit probleem is opgelost.

**Fluidic Player**

* Wanneer een auteur een cursus maakt met AICC- of Tin Can-inhoud en een voorbeeld van de inhoud probeert te bekijken, wordt de inhoud niet afgespeeld. Dit probleem is opgelost.
* Modulevoorbeeld functioneert niet tijdens het maken van een cursus of wanneer een auteur de cursus bewerkt. Dit probleem is opgelost.

**Catalogi**

Wanneer een student rechtstreeks via de browser de URL van catalogi of leerprogramma&#39;s probeert te openen wordt deze omgeleid naar cursussen. Dit probleem is opgelost.

**Salesforce-integratie**

* Nadat een Salesforce- of FTP-verbinding tot stand was gebracht, werden op de pagina Kenmerken toewijzen de vervolgkeuzepijlen voor de velden niet weergegeven in de browsers IE, Edge en Safari. Ook werden een aantal pop-upberichten niet weergegeven in de workflows. Dit probleem is opgelost.
* Wanneer een beheerder probeerde de geïmporteerde CSV-gegevens te synchroniseren in een FTP-connector, mislukte de synchronisatie met gerepliceerde items. Dit probleem is opgelost.

**API-laag**

* Wanneer een beheerder de externe student toestemming gaf OAuth-authenticatie te gebruiken, konden de externe studenten zich soms niet aanmelden bij de toepassing. Dit probleem is opgelost.
* Bij een API-aanroep voor Taakhulpen werd soms een fout voor onbevoegde toegang weergegeven. Dit probleem is opgelost.

**Instellingen**

Wanneer op de pagina Gegevensbronnen een automatische planningstijd wordt ingesteld en opgeslagen, wordt deze soms teruggezet naar de oude status. Dit probleem is opgelost.

**Rapportage van gebruikersgroep**

Waarden van gebruikersgroepen in filter worden niet ingevuld wanneer het rapporttype Aangepast wordt gekozen. Dit probleem is opgelost.

**Adobe Connect-integratie**

Onjuiste titel verscheen voor Adobe Connect-integratie nadat de verbinding was gemaakt. De tekst van de paginatitel is gecorrigeerd.

**Rapporten**

Zelfs als de optie Gegevens voor huidige waarden weergeven is geselecteerd, worden de meest recente gegevens niet weergegeven in de rapporten. Dit probleem is opgelost.

+++

+++Update 18

Releasedatum: 31 juli 2016.

## Nieuwe functies en verbeteringen {#newfeaturesandenhancements}

Zie [Nieuw](../whats-new.md) voor een lijst van nieuwe functies en verbeteringen in de Learning Manager-release van juli.

Hieronder vindt u een aantal van de verbeteringen en functies ter referentie.

**Studenttranscript**

Learning Manager biedt u een functie om transcripten te genereren voor de Learning Manager-studenten in uw organisatie. Raadpleeg voor meer informatie  [Help-inhoud van de functie Studenttranscripten](../administrators/feature-summary/learner-transcripts.md).

**Badge exporteren als PDF**

Met Learning Manager kunt u uw badges als PDF-bestanden exporteren. Raadpleeg voor meer informatie  [Inhoud van badges](../administrators/feature-summary/badges.md).

**Quizscore voor modules**

U kunt quizscores toevoegen voor de modules Klaslokaal, Virtueel klaslokaal en Activiteiten.

**Gebruikers toevoegen**

* U kunt studenten van de ene zelfregistratiegroep naar de andere verplaatsen.
* U kunt gebruikers van de ene externe groep naar de andere externe groep verplaatsen.
* U kunt een gebruiker van een externe groep maken als manager van dezelfde externe groep.
* Nadat u een externe gebruikersgroep aan Learning Manager hebt toegevoegd, kunt u het registratieproces voor externe gebruikers ook onderbreken. U kunt de blokkering (pauzeren) op elk gewenst moment opheffen door de optie Hervatten te kiezen.
* U kunt nu de naam en het e-mailadres van de studenten bewerken.

**Zelfinschrijving**

Studenten kunnen zich ook van leerobjecten, zoals cursussen, leerprogramma&#39;s of certificeringen uitschrijven. Studenten kunnen zich echter niet van een leerobject uitschrijven nadat ze een leerobject hebben voltooid.

**Leerobjecten voltooien**

Beheerders kunnen nu een leeractiviteit van studenten als compleet markeren.

**Rapporten**

* U kunt zich abonneren op cursusrapporten, leerprogramma- of certificaatrapporten. U kunt zich ook abonneren op individuele cursusrapporten voor gegevens zoals quizscore en studentstatus. De abonnementen worden naar uw e-mailadres gestuurd zoals dat is geregistreerd in het Learning Manager-account. U kunt deze e-mail-ID ook wijzigen.
* Bij het exporteren van een inschrijvingsrapport voor certificering, wordt een nieuwe kolom met de naam **Vervaldatum** wordt ook geëxporteerd. Met deze kolomgegevens kunnen beheerders de studenten kennen die de consumptietermijnen van hun leerobject niet hebben gehaald.

**E-mailsjablonen**

U kunt nu de koptekst van e-mailsjablonen bewerken.

+++

+++Update 17

Releasedatum: 15 juni 2016.

### Opgeloste problemen {#Issuesfixed-8}

**Gebruikers toevoegen**

Wanneer er veel Learning Manager-gebruikers waren, duurde het lang voordat gebruikers en gebruikersgroeppagina waren geladen. Dit probleem is opgelost.

**Gebruikersgroepen maken**

Het aantal gebruikers werd soms niet weergegeven op de standaardpagina voor gebruikersgroepen in Learning Manager. Dit probleem is opgelost.

+++

+++Update 16

Releasedatum: 10 juni 2016.

## Probleem opgelost {#Issuefixed-1}

Sommige klanten ondervonden problemen bij eenmalige aanmelding in Learning Manager. Dit probleem is opgelost door de entityId van de leermanager naar een URL te verwijzen (<https://learningmanager.adobe.com>) in plaats van een trefwoord. Learning Manager voldoet aan de SAML 2.0-specificatie.

+++

+++Update 15

Releasedatum: 25 mei 2016.

### Verbeteringen {#Enhancements-10}

**Certificeringen/leerprogramma&#39;s**

* In de inschrijvingslijst voor certificeringen en leerprogramma&#39;s wordt de volledige naam (voor- en achternaam) van studenten weergegeven. Eerder verscheen alleen de voornaam van de studenten.
* Vaardigheden van het hoogste niveau worden uit de lijst van cursussen in certificeringen/leerprogramma&#39;s overgenomen en op kaarten weergegeven als certificerings-/leerprogrammavaardigheid. Als er meerdere cursussen met dezelfde puntenwaarde zijn, worden deze in alfabetische volgorde opgehaald. Eerder werden de namen van vaardigheden voor certificering/leerprogramma&#39;s willekeurig uit een lijst van respectieve cursussen overgenomen.

**CSV importeren**

Voor het automatisch uploaden van CSV met behulp van FTP ontvangen beheerders e-mailmeldingen als er iets misgaat bij het uploaden van CSV.

**Externe partners toevoegen**

Wanneer externe studenten de registratiepagina bezoeken met behulp van de URL van een extern profiel, wordt de naam van het externe profiel weergegeven op de registratiepagina voor een betere identificatie.

### Opgeloste problemen {#Issuesfixed-9}

**Cursussen bekijken en publiceren**

* Als u in de auteursrol een voorvertoning weergeeft van een cursus die vanuit de Captivate is geüpload als SCORM+SWF-inhoud met `code $$cpQuizInfoStudentName$$` variabele, null-waarde weergegeven voor variabele. Dit probleem is opgelost.
* Wanneer er een apostrof (&#39;) in de titel van een Presenter-cursus stond en deze werd gepubliceerd en bekeken in Learning Manager, verschenen er vraagtekens (???) in de inhoudsopgave. Dit probleem is opgelost.

**Certificeringen**

* Als een certificering aan een catalogus is gekoppeld en wanneer de certificering terugkeert, verschijnt deze in alle bijbehorende catalogi. Eerder konden gebruikers de terugkerende certificeringen soms niet zien in hun catalogi.
* Als een beheerder tijdens het maken van certificeringen de **dagen om te voltooien** een waarde die groter is dan of gelijk is aan de geldigheidsperiode van de certificering, wordt een waarschuwingsbericht weergegeven. Eerder werd het waarschuwingsbericht niet weergegeven aan de beheerders.
* Gebruiker zien de **geldigheid** van de certificering in maanden. Eerder verscheen de basiswaarde in jaren.

**Leerprogramma&#39;s definiëren**

De deadline verschijnt niet voor standaardinstanties van leerprogramma&#39;s. Eerder verscheen een vooraf bepaalde deadline die mogelijk niet relevant was voor gebruikers.

**Cursussen maken met behulp van modules**

* Wanneer een auteur een module van een blended-cursus bijwerkte, verscheen de aanwezigheidspagina niet in de beheerdersrol. Dit probleem is opgelost.
* Wanneer de naam van een cursusinstantie een dubbele punt (:) bevat, mislukte de exportactie voor de studentenlijst. Dit probleem is opgelost.

+++

+++Update 14

Releasedatum: 4 mei 2016

### Verbeteringen {#Enhancements-11}

**Catalogi**

Wanneer een student een catalogus opent, verschuift de standaardfocus tussen de tabbladen op basis van de beschikbaarheid van leerobjecten, in deze volgorde: 1. Cursussen 2. Programma&#39;s 3. Certificeringen en 4. Taakhulpen. Als de cursussen bijvoorbeeld niet beschikbaar zijn op het tabblad Cursussen voor die student, verschuift de focus naar het volgende leerobject, Programma&#39;s, als er leerprogramma&#39;s zijn.

**Accountinstellingen**

Het bevestigingsvenster van Account deactiveren biedt een feedback-optie wanneer een beheerder ervoor kiest om een account uit te schakelen.

### Opgeloste problemen {#Issuesfixed-10}

**Rapporten exporteren**

* Exporteren van studentenlijst mislukte wanneer een groot aantal gebruikers voor een leerprogramma was ingeschreven. Dit probleem is opgelost.
* Wanneer een cursus twee instanties met dezelfde naam heeft en de naam van de instantie lang is, worden er niet twee werkbladen gemaakt in het geëxporteerde Excel-bestand. Dit probleem is opgelost.

**Bulkinschrijvingen**

Wanneer een groot aantal studenten voor leerobjecten, zoals leerprogramma&#39;s, cursussen, certificeringen, taakhulpen en leerplannen, is ingeschreven, mislukt de inschrijving. Dit probleem is opgelost.

+++

+++Update 13

Releasedatum: 20 april 2016.

### Opgeloste problemen {#Issuesfixed-11}

**Cursussen maken met behulp van modules**

Wanneer een module-inhoud met een lange bestandsnaam werd geüpload, waren er problemen met de weergave van knoppen. Ook het uploaden en verwijderen van de modules werkte niet zoals verwacht. Dit probleem is opgelost.

**CSV importeren**

Op verzoek van Amerikaanse klanten is de FTP-tijd voor automatisch uploaden van CSV veranderd van middernacht GMT naar middernacht PST.

**Rapporten exporteren**

Exporteren van inschrijvingsgegevens mislukte als een van de ingeschreven studenten wordt verwijderd nadat de cursus is gevolgd. Dit probleem is opgelost.

**E-mailsjablonen**

* Het woord **partners,** die werd gebruikt om externe groepen te vertegenwoordigen,**** is **** verwijderd uit de hoofdtekst en titel van e-mailsjablonen. Externe groepen worden niet noodzakelijkerwijs partners genoemd.\
  **Opmerking:** Deze bijgewerkte sjabloon wordt niet weergegeven als de standaardsjabloon al is gewijzigd. Klik op **Origineel herstellen** in **Sjabloonvoorbeeld** in.

* Er kan niet op de URL worden geklikt in het e-mailbericht dat Beheerders altijd ontvangen **Profiel gemaakt (zelfregistratie)** en **Profiel gemaakt (extern/partners)** e-mailsjablonen worden bewerkt. Dit probleem is opgelost.

+++

+++Update 12

Releasedatum: 7 april 2016.

### Verbeteringen {#Enhancements-12}

**Taakhulpen**

Maak Taakhulpen met behulp van een URL. U kunt alleen een URL-naam vermelden in de workflow voor het maken van een taakhulp en de taakhulp maken als u bestaande online inhoud wilt gebruiken als taakhulp.

**Studenten toevoegen**

Het is toegestaan gegevens van één gebruiker, zoals naam, e-mailadres, profiel en naam van manager, te bewerken. Alle overeenkomstige gebruikersgroepen worden bijgewerkt met de recentste gebruikersgegevens.

**Rapporten exporteren**

Naam van de manager, naam van leerobject en gebruikergedefinieerde kolommen met niet-unieke waarde uit CSV worden aan de geëxporteerde studentenlijst voor leerobjecten toegevoegd. Eerder verschenen alleen de basisgegevens van studenten, zoals naam, datum, e-mailadres en status.

**Externe partners toevoegen**

Externe studenten kunnen zich niet bij de Learning Manager-toepassing aanmelden nadat hun account is verlopen. Externe partners kunnen hun accountstatus in de toepassing bekijken.

**Certificeringen**

U kunt certificeringen in maanden verlengen door de waarde in het veld **Geldigheid** te vermelden. Eerder was verlenging van de certificering alleen toegestaan in termen van jaren.

### Opgeloste problemen {#Issuesfixed-12}

**Aankondigingen**

Paginering werkte niet op de pagina Aankondigingen in Beheerdersaanmelding. Dit probleem is opgelost.

**Leerprogramma&#39;s en -plannen**

* Wanneer een student een cursusmodule op volgorde in een leerprogramma probeerde over te slaan, werd er geen foutmelding weergegeven. Dit probleem is nu opgelost. Een foutbericht **Kan modules niet overslaan** wordt weergegeven.
* Cursussen werden niet aan leerprogramma&#39;s toegevoegd wanneer paginering werd gebruikt in de cursussenlijst. Dit probleem is opgelost.
* **Gearchiveerd** werd twee keer weergegeven in Leerprogramma&#39;s > Instanties. Dit probleem is opgelost.

**Taakhulpen**

* Wanneer een student taakhulpmiddelen van het tabblad **Leermateriaal** verwijderde, werkte het sorteren van **namen** niet zoals verwacht totdat de pagina was vernieuwd. Dit probleem is opgelost.

* Als een taakhulp deel uitmaakte van meerdere cursussen, werden de cursussen niet weergegeven in de lijst Taaklijst. Dit probleem is opgelost.
* Als een student in- of uitzoomde in de browser, werkte de paginering niet zoals verwacht voor de lijst Taakhulpen. Dit probleem is opgelost.

**Cursus volgen**

* Als een student in- of uitzoomde in de browser, werkte de paginering niet zoals verwacht voor cursussen. Dit probleem is opgelost.

**Vaardigheden maken**

In de aanmelding van studenten verschijnt de knopinfo voor vaardigheidsnaam in **Vaardighedenkaart **was** **geeft de***volledige naam niet weer. Dit probleem is opgelost.

**Externe partners toevoegen**

* Er is een tekstbericht opgenomen op de registratiepagina voor externe gebruikers als **Gebruikers moeten zich eerst registreren en een gebruikersnaam-wachtwoord maken voor volgende aanmeldingen**.

**Gebruikersmeldingen**

* Wanneer een externe student op de knop **Notities openen** in E-mailmelding Cursus opnieuw bekijken wordt de speler geopend, maar het deelvenster Notities werkte niet. Dit probleem is opgelost.
* Wanneer een externe student de voorbereidings- of evaluatiemodules probeert te openen met **Notities openen** koppeling in e-mailmelding Cursus opnieuw bekijken. Notitie-inhoud is niet zichtbaar. Dit probleem is opgelost.

**Cursussen maken met behulp van modules**

Wanneer een beheerder probeerde studenten in te schrijven voor een blended-cursus die verlopen klaslokaalmodules bevatte, werd het inschrijvingsvenster niet geopend. Dit probleem is opgelost.

**Rapporten exporteren**

Als een vraagtekst meer dan 255 tekens bevat en is ingeschakeld voor de SCORM 1.2-indeling, werkte quizrapportage voor dergelijke vragen niet. Dit probleem is opgelost.

+++

+++Update 11

Releasedatum: 15 maart 2016.

### Opgeloste problemen {#Issuesfixed-13}

**Cursussen met modules maken**

* Wanneer u in Beheerdersaanmelding probeert een nieuwe instantie voor cursussen te maken van **Gearchiveerd** is opgetreden, is een fout opgetreden. Dit probleem is opgelost.
* De indelingen voor de acties en het inschrijvingsscherm waren vervormd in Beheerdersaanmelding van gelokaliseerde inhoud, tijdens het inschrijven van studenten voor cursusinstanties. Dit probleem is opgelost.
* Wanneer een auteur klassikale of virtuele klassikale modules maakte, werd de kalendermaand standaard weergegeven als januari 2015. Dit probleem is opgelost. De huidige datum wordt standaard weergegeven.
* Wanneer de naam van een cursusinstantie een schuine streep vooruit of achteruit bevatte, mislukte de export van de studentenlijst. Dit probleem is opgelost.

**Aankondigingen**

Wanneer een student met de muis op een videomelding ging staan, veranderde de cursor niet in een wijzende vinger. Dit probleem is opgelost.

**Gebruikersmeldingen**

Wanneer een externe student op de knop **Notities openen** koppeling in e-mailmelding Cursus opnieuw bezoeken, werkt niet. Dit probleem is nu opgelost. Deze koppeling opent de speler met notities, zelfs als de gebruiker niet is aangemeld bij Leermanager.

**Ondersteuning voor Frans en Duits**

De Help-URL&#39;s in de functie CSV-upload gingen naar Help-inhoud in het Engels. Dit probleem is opgelost.

**Cursussen bekijken en publiceren**

Wanneer u als auteur was aangemeld en een voorbeeld van Presenter 10- en 11 TinCan API (SWF/HTML)-inhoud wilde bekijken, werkte de inhoud niet. Dit probleem is opgelost.

**Aanpasbare e-mails**

De titelnamen in e-mailsjablonen waren niet toepasselijk. De inhoud wordt in deze sjabloontitels bijgewerkt om ze leesbaar te maken.

**Taakhulpen**

In de browser Internet Explorer 11 verschenen de naam en het pictogram van de taakhulp vervormd in het voorbeeld voor auteurs en beheerders. Dit probleem is opgelost.

+++

+++Update 10

Releasedatum: 28 februari 2016.

## Nieuwe functies {#Newfeatures-2}

### Taakhulpen

Taakhulpen is een opslagplaats van trainingsinhoud die zonder enige inschrijvings- of voltooiingscriteria toegankelijk is voor studenten. Studenten kunnen naar deze taakhulpen verwijzen om hulp te krijgen bij het uitvoeren van activiteiten of taken in een organisatie. De beheerder kan het aantal downloads per taakhulp bijhouden.

Raadpleeg voor meer informatie over deze functie  [Help bij taakhulpen](../learners/feature-summary/job-aids.md).

### Aankondigingen

Een aankondiging is een multimediabericht (tekst, beeld of video) dat een beheerder kan maken en uitzenden naar een specifieke groep gebruikers. Gebruik aankondigingen om studenten te motiveren om trainingen te volgen en zo een leercultuur op te bouwen.

Raadpleeg voor meer informatie over deze functie  [Help voor aankondigingen](../learners/feature-summary/announcements.md).

### Tin Can API-ondersteuning

Adobe Learning Manager ondersteunt de Tin Can API-specificatie (ook bekend als Experience API of xAPI). U kunt Tin Can API-compatibele content uploaden en volgen op dezelfde manier als u SCORM- en AICC-inhoud volgt.

Neem voor meer informatie contact op met het ondersteuningsteam van Adobe.

### Cursusreeksen

U kunt een leerpad creëren door automatisch een vervolgcursus of leeractiviteit toe te wijzen.

Gebeurtenissen voor leerplannen zijn bijgewerkt. Er zijn enkele nieuwe gebeurtenissen toegevoegd. Raadpleeg  [Leerplannen](../learners/feature-summary/learning-programs.md) voor meer informatie.

### Herinnering voor notities

Als u notities maakt terwijl u een cursus volgt, herinnert Learning Manager u hier na 15 dagen aan door u een bericht te sturen om de notities te bekijken.

### Gamification op groepsniveau

Beheerders kunnen de omvang van gamification definiëren door de omvangsinstellingen te wijzigen. U kunt gamification selectief inschakelen onder vergelijkbare profielgebruikers, groepen of locatie. Raadpleeg  [Gamification](../learners/feature-summary/gamification.md) voor meer informatie.

### Ondersteuning voor Frans en Duits

De Learning Manager-toepassing is beschikbaar in het Frans en Duits. U kunt de taal aanpassen voor feedback, cursusinstanties en communicatie.

### Verbeteringen {#Enhancements-13}

De bestaande kenmerken van Learning Manager zijn aanzienlijk verbeterd. Enkele van de belangrijkste verbeteringen zijn:

### CSV importeren

Als u gebruikers verwijdert, kunt u dezelfde gebruikers niet opnieuw aan de toepassing toevoegen door één gebruiker toe te voegen. U kunt de verwijderde gebruiker echter wel weer toevoegen met behulp van het CSV-uploadproces. Er zijn belangrijke wijzigingen in de beperking voor verplichte velden in de CSV-uploadfunctie. Raadpleeg  [Veelgestelde vragen over CSV](../administrators/add-users-in-bulk.md) voor meer informatie.

### Cursuslijstweergave

U kunt cursussen standaard als kaarten bekijken. In deze release is een lijstweergave geïntroduceerd. U kunt op het pictogram met de drie balkjes naast het zoekveld klikken om de weergave te wijzigen.

### Cursussen verwijderen

U kunt nu cursussen in de fasen Concept en Gearchiveerd verwijderen. Raadpleeg  [Cursussen](../administrators/feature-summary/courses.md) voor meer informatie. Als een leerobject wordt verwijderd, worden ook alle bijbehorende rapportagegegevens verwijderd. Als een cursus wordt verwijderd en als deze deel uitmaakte van een ander leerobject, verschijnt een geschikt bericht voor de gebruiker.

**Leerprogramma&#39;s en -plannen**

U kunt de volgorde waarin studenten cursussen volgen binnen leerprogramma&#39;s afdwingen. U kunt leerprogramma&#39;s in concepten en gearchiveerde fasen verwijderen. Als een leerobject wordt verwijderd, worden ook alle bijbehorende rapportagegegevens verwijderd.

**Certificeringen**

U kunt certificeringen in concepten en gearchiveerde fasen verwijderen. Als een leerobject wordt verwijderd, worden ook alle bijbehorende rapportagegegevens verwijderd.

**Effectiviteitsscore van cursus**

U kunt L1- en L3-feedbackgegevens exporteren voor elke cursus in Beheerdersaanmelding.

**Cursussen met modules maken**

U kunt studenten verplichten om aan vereisten te voldoen voordat ze aan een cursus beginnen.

**Gebruikersmeldingen**

Studenten krijgen een melding telkens wanneer zij zichzelf inschrijven voor een leerprogramma.

**Klaslokaalmodules (ILT)**

U kunt klassikale cursussen maken voor een datum in het verleden. Met behulp van deze functie kunnen bedrijfsbeheerders informatie over oudere klassikale cursussen ook in Learning Manager invoeren en rapporten genereren.

**Rapporten exporteren**

Het studentenrapport is verbeterd. U kunt naam, e-mail, status van leerobject, inschrijvingscriteria, inschrijvingsdatum, voltooiingsdatum en startdatum in het rapport bekijken.

**Externe partners toevoegen**

Nadat u de externe studenten voor het Learning Manager-account hebt ingeschreven, kunt u ook het aantal studenten verlagen, indien nodig. Het aantal studenten mag echter niet lager zijn dan het aantal gebruikte plaatsen. Als tijdelijke oplossing kunt u de geregistreerde studenten eerst verwijderen en vervolgens opnieuw inschrijven met het vereiste aantal plaatsen.

### Opgeloste problemen {#Issuesfixed-14}

**Aanwezigheid van studenten**

Aanwezigheidsformulier in de weergave Beheerder geeft de volledige naam van de werknemer weer als deze beschikbaar is. Eerder verscheen alleen de voornaam van de student.

**Leerprogramma&#39;s en -plannen**

Alle cursussen in leerprogramma&#39;s worden in de verwachte volgorde weergegeven. Eerder waren er problemen met de volgorde van de cursussen in een leerprogramma. Dit probleem is opgelost.

**Studenten toevoegen**

Als een bestaande gebruiker die zichzelf heeft geregistreerd, zichzelf opnieuw probeert te registreren via een zelfregistratieproces, verschijnt er een passende melding. De indeling en de inhoud van het bericht staan vast.

**Rapporten**

Als u wilt dat in de inhoud wordt aangegeven hoeveel tijd de gebruiker heeft besteed aan het consumeren van inhoud, kunt u dit herkennen aan de hand van een variabele. `code cmi.core.session_time`. De variabele was eerder niet ingesteld. Dit probleem is opgelost.

**Cursussen met modules maken**

Telkens wanneer een bestaande cursusmodule wordt vervangen door een andere module, wordt er een nieuwe versie van gegenereerd. Als de quiz van deze nieuwe module werd geëxporteerd, trad er een uitzondering op en werd het quizrapport niet gegenereerd. Dit probleem is nu opgelost.

**E-mailsjablonen**

De typfouten in de e-mailsjablonen zijn verbeterd.

+++

+++Update 9

Releasedatum: 9 februari 2016.

## Afmeldgedrag bijgewerkt {#signoutbehaviorupdated}

Wanneer gebruikers op **[!UICONTROL Afmelden]** in Leermanager worden ze nu afgemeld bij de toepassing Leermanager en worden ze ook afgemeld bij hun Adobe-id&#39;s.

+++

+++Update 8

Releasedatum: 20 januari 2016.

### Verbeteringen {#Enhancements-14}

**Aanpasbare e-mails**

* Gebruikers kunnen de voettekst van de e-mailsjablonen aanpassen. U kunt de voettekst van een e-mailsjabloon aanpassen met tekst van uw keuze. De aangepaste voettekst wordt automatisch toegepast op alle soorten e-mailsjablonen.

**Cursus volgen**

* In de voorbeeldmodus van een cursus worden leermiddelen na elkaar weergegeven op een nieuwe regel. Eerder werden de gebruikte leermiddelen soms naast elkaar op één regel weergegeven.

**Directe link naar leerobjecten**

* U heeft toegang tot de leerobjecten (met uitzondering van Certificering) via een directe URL. De **[!UICONTROL URL kopiëren]** wordt weergegeven op de tegels van leerobjecten. Gebruikers kunnen klikken **[!UICONTROL URL kopiëren]** en plak de koppeling in een aparte browserpagina om het leerobject rechtstreeks te openen.

**Cursussen maken met behulp van modules**

* Tijdens het maken van een cursus kunnen auteurs de volgorde van vereiste cursussen bepalen. Deze optie was eerder niet beschikbaar in Learning Manager.

* Auteurs kunnen vereiste cursussen toevoegen of verwijderen in Gepubliceerde cursussen. Deze functie was eerder alleen beschikbaar voor conceptcursussen.

**Gebruikersregistratie**

* Gebruikers kunnen zich zonder extra URL-verificatie bij Learning Manager aanmelden als hun Adobe ID met de e-mail-ID van Learning Manager overeenkomt. Wanneer de beheerder van een organisatie gebruikers aan het account toevoegt, geeft deze de e-mail-ID van Learning Manager op.

**Catalogus maken**

* In de beheerdersrol tijdens het maken van catalogi met **Leerobjecten toevoegen** gearchiveerde cursussen niet in de lijst met cursussen worden weergegeven.

**Andere oplossingen**

* In de beheerdersrol wordt de volledige naam van de studenten weergegeven in **Studenten** tabblad. Eerder verscheen alleen de voornaam van de student.

+++

+++Update 7

Releasedatum: 13 januari 2016.

### Opgeloste problemen {#Issuesfixed-15}

**Cursus volgen**

* In cursusinhoud verschijnt de inhoudsbalk altijd op het scherm. Eerder was er een probleem met de inhoudsbalk, omdat deze af en toe van het scherm verdween.
* Als gebruikers in de cursusinhoud een pop-upvenster zien waarin wordt gevraagd of ze echt willen stoppen of op de pagina willen blijven, gaan ze terug naar de inhoud wanneer ze er in dit venster voor kiezen op de pagina te blijven. In sommige scenario&#39;s verliet de gebruiker de inhoud wanneer op de knop Blijven werd geklikt.

**Andere oplossingen**

* Er zijn maar weinig problemen met betrekking tot het afspelen van inhoud opgelost.

+++

+++Update 6

Releasedatum: 22 december 2015.

### Verbeteringen {#Enhancements-15}

**Persoonlijk dashboard**

* Bij het openen van cursussen, catalogi en leerprogramma&#39;s in de beheerders- en auteursrollen wordt de tabvolgorde gewijzigd in **Gepubliceerd - concept - alles - gearchiveerd**. De standaardselectie is **Gepubliceerd**

### Opgeloste problemen {#Issuesfixed-16}

**Cursus volgen**

* Als u in de rol van student een cursus volgt, wordt de bestede leertijd in rapporten vastgelegd als de speler met de knop Terug van de browser of de Backspace-toets op het toetsenbord wordt gesloten. In sommige scenario&#39;s werd deze duur niet in rapporten vastgelegd.

**Gebruikersregistratie**

* Als een gebruiker een Learning Manager-account registreert met behulp van zelfregistratie via eenmalige aanmelding, verschijnt de gebruikersnaam correct in de gebruikerslijst, zoals in de records. In sommige gevallen werd de gebruikersnaam verkeerd weergegeven.

**Cursussen maken met behulp van modules**

* Wanneer een auteur een cursus dupliceert, kunnen de bronbestanden van de gedupliceerde cursus worden verwijderd of bijgewerkt. Gebruikers ondervonden soms problemen bij het updaten of verwijderen van de leermiddelen uit gedupliceerde cursussen.

**Aangepaste catalogus maken voor de gebruikersgroep**

* Tijdens het gebruik **Leerobjecten toevoegen** in de beheerdersrol, kunt u cursussen filteren, een cursus kiezen en toevoegen met **Toevoegen** onder aan het dialoogvenster. In sommige gevallen: **Toevoegen** niet voor sommige gebruikers werd weergegeven.

+++

+++Update 5

Releasedatum: 11 december 2015.

### Opgeloste problemen {#Issuesfixed-17}

**Gebruikersaanmelding**

* Wanneer een gebruiker zich bij de Learning Manager-toepassing probeerde aan te melden zonder de activeringslink te gebruiken, verscheen de foutmelding in de verkeerde indeling. Dit probleem is opgelost.

**App voor tablets**

* Na installatie van Learning Manager op een Android- of iOS-tablet, verschijnen er geen berichten over browsercompatibiliteit. Eerder zagen gebruikers een bericht over browsercompatibiliteit. Dit probleem is opgelost.

+++

+++Update 4

Releasedatum: 9 december 2015.

### Verbeteringen {#Enhancements-16}

**Gebruikers toevoegen**

* Wanneer de beheerder in de beheerdersrol gebruikers registreert of één gebruiker toevoegt, verschijnt er een bericht dat de workflow is voltooid met volgende stappen.
* Wanneer een gebruiker zich rechtstreeks probeert aan te melden bij de Leerbeheertoepassing zonder de activeringskoppeling van de gebruiker te gebruiken, verschijnt een foutbericht waarin gebruikers wordt gevraagd om de activeringskoppeling te gebruiken.

**Ondersteunde browsers**

* Als gebruikers de Learning Manager-toepassing in een niet-ondersteunde browsers openen, ontvangen zij een waarschuwing met de lijst van goedgekeurde browsers.

### Opgeloste problemen {#Issuesfixed-18}

**Rapporten**

* Wanneer u in de beheerders- of managersrol een rapport maakte met de leertijd als secundaire as, een managerfilter toepaste en het rapport opsloeg, kon de gebruiker dergelijke rapporten niet downloaden. U kunt elk type rapport downloaden.

**Gebruikers toevoegen**

* Er stonden enkele typfouten in de waarschuwingen die werden weergegeven tijdens het inschakelen van externe studenten in de beheerdersrol. Dit probleem is opgelost.
* In de beheerdersrol verschijnt een passende foutmelding wanneer het veld Manager niet goed wordt geselecteerd tijdens het toevoegen van één gebruiker.

**Gebruikersregistratie**

* De welkomstmail die nieuwe gebruikers ontvangen, benadrukt hoe belangrijk het is Adobe ID aan de Learning Manager-ID te koppelen voor geslaagde aanmelding.

**Aanpasbare e-mails**

* Wanneer u meerdere studenten toevoegde aan de klassikale cursussen die sessies als bijlage hebben, ontvingen sommige studenten geen e-mailmeldingen. Dit probleem is opgelost.
* E-mails aan studenten over inschrijvingen voor leerobjecten en andere gebeurtenissen bevatten de naam van het specifieke leerobject in het onderwerp van de e-mail.

**Andere oplossingen**

* De problemen met betrekking tot URL-links in e-mailsjablonen zijn opgelost.
* Ondersteuning voor

   * Publiceren naar Leermanager
   * Ondersteuning voor sneller uploaden van inhoud voor CP 8-versie (CP803-patch is vereist)

+++

+++Update 3

Releasedatum: 26 oktober 2015.

### Verbeteringen {#Enhancements-17}

**Gebruikers toevoegen**

* Link naar online Help in dialoogvenster Gebruikers toevoegen > Een CSV uploaden voor gebruikers wanneer zij een CSV-bestand uploaden.

**Fluidic Player**

* Wanneer u Captivate-cursusinhoud met een omvang van meer dan 500 MB uploadde, werd de inhoud niet afgespeeld in Fluidic Player. Deze beperking is opgeheven. De limiet voor de omvang is op dit moment 2 GB.

**Facturering**

* Wanneer een gebruiker in de beheerdersrol het aantal studenten invoert en op **Bestelling plaatsen,** er verschijnt een dialoogvenster met informatie over maandelijkse en jaarlijkse abonnementskosten per gebruiker.

### Opgeloste problemen {#Issuesfixed-19}

**Cursussen maken met behulp van modules**

* Wanneer auteurs cursussen met activiteitenmodules maken, kunnen zij geldige externe URL&#39;s kiezen, zelfs als deze mappaden in de URL bevatten. De URL&#39;s met mappaden werden eerder niet ondersteund. Dit probleem is opgelost.
* Als de cursusinhoud een project was dat met een ZIP-bestand in Learning Manager werd geüpload en als dat ZIP-bestand mappaden bevatte, zoals Zip>map>inhoud, werd dit type inhoud niet ondersteund. Dit probleem is opgelost.

**App voor tablets**

* Wanneer een gebruiker de bronbestanden van een cursus in de Learning Manager Android-app probeerde te downloaden, waren de bronbestanden niet downloadbaar. Dit probleem is opgelost.
* Wanneer de gebruiker een cursus volgt met behulp van een Fluidic Player, een notitie neemt en deze later probeert te downloaden, is deze niet downloadbaar. Dit probleem is opgelost.

+++

+++Update 2

Releasedatum: 28 september 2015.

### Verbeteringen {#Enhancements-18}

**Cursussen maken met behulp van modules**

* De Learning Manager-toepassing ondersteunt het uploaden van SCORM-inhoud, zelfs als de versie niet in het bestand manifest.xml wordt vermeld. Standaard wordt de versie beschouwd als 1.2.
* Wanneer u Captivate-cursusinhoud met een omvang van meer dan 500 MB uploadde, werd de inhoud niet afgespeeld in Fluidic Player. Als onderdeel van Update 2 is de maximale grootte gewijzigd in 800 MB.

**Facturering**

* Wanneer de gebruiker in de beheerdersrol een abonnement koopt met een creditcard, kan de gebruiker de eerste bestelling kiezen vanaf 10 studenten. Het minimumaantal studenten dat vereist is voor de eerste bestelling is teruggebracht van 100 naar 10.

**Gebruikersregistratie**

* In de welkomstmail die studenten na registratie ontvangen, is een URL-link opgenomen om een Adobe ID te maken.

**Gebruikers toevoegen**

* Het was soms niet mogelijk in de beheerdersrol gebruikers rechtstreeks vanuit Exavault-account toe te voegen via CSV-upload. Dit probleem is opgelost.

### Opgeloste problemen {#Issuesfixed-20}

**Leerprogramma&#39;s en -plannen**

* Studenten kunnen automatisch worden ingeschreven voor hetzelfde leerprogramma als onderdeel van meerdere leerplannen. Eerder waren er enkele uitzonderingen op deze workflow. Dit probleem is opgelost.

**Leaderboard en badges weergeven**

* Nadat in de studentrol een cursus was gevolgd die een badge bevatte, werd de badgeafbeelding niet weergegeven op de badgekaart op het dashboard van de student en in het gedownloade bestand. Dit probleem is opgelost.

**App voor tablets**

* Er verschijnt een pop-up om de beschikbaarheid van de student-app aan te geven wanneer de url van de student-app in een browser op een Android-apparaat wordt geopend.

**Andere oplossingen**

* Een probleem met het maken van gebruikersaccounts als gevolg van Akamai-ondersteuning voor netto-opslag is opgelost.
* Een probleem met betrekking tot het uploaden van SCORM 1.2-inhoud die een ZIP-bestand met meerdere mappen bevat, is opgelost.

+++
