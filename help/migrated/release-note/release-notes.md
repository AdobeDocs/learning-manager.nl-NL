---
description: Meer informatie over de nieuwe functies en verbeteringen in Adobe Learning Manager
jcr-language: en_us
title: Overzicht van nieuwe functies
contentowner: jayakarr
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '26196'
ht-degree: 0%

---



# Overzicht van nieuwe functies

<!--<table>
 <tbody>
  <tr>
   <td><img src="assets/cp-prime-appicon-88x84.png"></td>
   <td>
    <p><a href="https://business.adobe.com/products/learning-manager/adobe-learning-manager.html">Adobe Learning Manager</a> was launched in August 2015. As part of our continuous improvement efforts to enhance the product, we have been rolling out regular updates. Read on to know the features enhanced/issues fixed in update releases.<br></p></td>
  </tr>
 </tbody>
</table>-->

+++Update 95: de november 2023-versie van Adobe Learning Manager

**Releasedatum:** 18 november 2023

## Nieuwe functies in deze release

Weergave [Nieuwe functies in Adobe Learning Manager](/help/migrated/whats-new.md) voor meer informatie.
+++

+++Update 94

**Releasedatum:** 23 augustus 2023

## Nieuwe functies in deze update

* Selecteer het tandwielpictogram van de speler om de kwaliteit van de video te wijzigen.
* Wijzig de kwaliteit en snelheid van een video op social media.
+++

+++Update 93: de juli 2023-versie van Adobe Learning Manager

**Releasedatum:** 10 jul. 2023

Nieuwe functies in deze release

### Verbeterde Recommendations

Adobe Learning Manager heeft een nieuw en vernieuwd aanbevelingssysteem voor cursussen geïntroduceerd. Deze aanbevelingsfunctie gebruikt AI-algoritmen en gebruikersinteresses zoals Producten, Rollen en Niveaus om gepersonaliseerde contentaanbevelingen te bieden.

### Meerdere inschrijvingen

In deze versie van Adobe Learning Manager introduceren we meervoudige inschrijvingen voor studenten waarmee studenten zich in meer dan één instantie van een cursus op een of verschillende tijdsperioden kunnen inschrijven.

### Verplaatsing van de Exavault-connector

Deze release van Adobe Learning Manager bevat een nieuwe connector, die gebruikmaakt van het SFTP-protocol van de AWS Transfer-familie.

Zie voor meer informatie [Nieuwe functies in de juli 2023-versie van Adobe Learning Manager](/help/migrated/whats-new-2023-july.md).
+++

+++Update: 92

**Releasedatum:** 23 juni 2023

**bugs gecorrigeerd in deze update**

* Nadat u een module hebt voltooid, wordt de graad-API niet automatisch geactiveerd, wat resulteert in een groen vinkje dat niet wordt weergegeven zoals verwacht in de gebruikersinterface.
* Na het voltooien van een paar modules in een leerpad of een certificering wordt het groene vinkje, dat aangeeft dat de certificering is voltooid, niet weergegeven zoals verwacht.
* Adobe Learning Manager wordt niet zoals verwacht gestart nadat een gebruiker CSV met onjuiste velden is geüpload.
* In het pop-upvenster met waarschuwingen over hoe u contact opneemt met de beheerder worden ook andere e-mailadressen weergegeven.
* Alle badges die een student heeft verdiend, worden niet weergegeven in het antwoord.
* Tijdens gebruikersregistratie moet een gebruikersnaam met &quot; &quot; worden geaccepteerd.

#### Speler

* Voeg een menu toe om de schermresolutie te selecteren bij het afspelen van een video.
+++

+++Update 91

**Releasedatum:** 10 juni 2023

### Connectoren

* De Adobe Connect-connector vereist API&#39;s om CSRF-tokens te verzenden. Zie De beveiliging van Adobe Connect-accounts verbeteren voor meer informatie.

### Tekenreekswijziging

* We hebben de naam van de tekenreeks Rate this training gewijzigd om deze cursus te beoordelen, dit leerpad te beoordelen of deze certificering te beoordelen op basis van de training die een student volgt. Afhankelijk van het type training ziet een student de tekenreeks dienovereenkomstig.

### bugs gecorrigeerd in deze update

* In de beschrijving van de mobiele app Adobe Leermanager van de Play Store wordt ten onrechte gezegd dat een student een cursus offline kan volgen.
* Er zijn problemen opgetreden bij het migreren van inhoud (module_version.csv en course_module.csv) van LinkedIn naar Adobe Learning Manager.
* Als een account inactief is en meer dan drie jaar geleden is aangemaakt, worden alle gebruikers van het account verwijderd uit de AVG, ongeacht de status van de gebruikers.
* Wanneer u in de app voor docenten de wachtlijstlimiet instelt op nul in een sessie en de sessie opslaat, wordt in de gebruikersinterface onjuist &quot;Niet van toepassing&quot; weergegeven in plaats van nul.
* Bij het genereren van Studenttranscripten voor de Power BI-connector geeft de kolom Training of Moduleduur (min) null-waarden weer voor bepaalde klassikale of VC-modules.
* Nadat u een cursus als voltooid voor studenten in een instantie of meerdere instanties hebt gemarkeerd, worden alle studenten in de cursus als voltooid gemarkeerd, niet alleen de studenten in de huidige instantie of instanties.
+++

+++Update 90

**Releasedatum:** 4 april 2023

### In deze update opgeloste bugs

SAML-aanmelding mislukt als de SSO-aanmeldings-URL de entity_id bevat.
+++

+++Update 89: De Adobe Learning Manager van maart 2023

**Releasedatum:** 10 april 2023

### Nieuwe functies in deze update

**Verbeteringen aan de ILT-ervaring (Instructor Led Training)**

Er zijn verschillende verbeteringen aangebracht in de ILT-ervaring (Instructor-Led Training). Belangrijke verbeteringen zijn: de mogelijkheid om klassikale sessies te filteren op basis van locatie, de mogelijkheid om van instantie te wisselen (VILT) zonder dat de voortgang verloren gaat, een nieuwe &quot;Planningsassistent&quot; voor het beheren van conflicten in het boeken van docenten en klaslokalen, de mogelijkheid om &quot;Vaardigheden&quot; aan docenten te koppelen en op vaardigheden gebaseerde docenten te kiezen.

**Verbeteringen van de controlelijst voor waarneming**:

Auteurs kunnen nu &quot;Manager&quot; en &quot;Winkelmanager&quot; selecteren als waarnemer voor checklists. Managers kunnen de checklists binnen de managerinterface weergeven en voltooien zonder dat ze van rol naar docent moeten veranderen. Er wordt een melding naar een manager verzonden wanneer er een controlelijst aan hem/haar is toegewezen.

**Gebruik elke app-/smartphone-camera om QR-codes voor Learning Manager te scannen**

Studenten kunnen nu elke QR Code scanning-app of hun smartphone gebruiken om de door de Learning Manager gegenereerde QR-codes te scannen voor cursusinschrijving, voltooiing en meer.

**Rapportageverbeteringen**

Een nieuw gebruiksrapport voor docenten, Revisit-rapport voor trainingen, taakhulpenrapport en andere rapportverbeteringen.

**Ondersteuning voor &#39;hybride&#39; sessies**

Adobe Learning Manager ondersteunt nu de mogelijkheid om &quot;hybride&quot; ILT-sessies (Instructor Led Training) te maken. Virtuele ILT-sessies kunnen worden gemaakt met optionele locatie-informatie, zodat studenten de sessie persoonlijk kunnen bijwonen als ze beschikbaar zijn op de locatie.

**Betere voortgang bijhouden voor klaslokaal en virtuele ILT**

De klassikale en virtuele ILT-modules bieden nu de mogelijkheid om de quizstatus van een student (geslaagd of gezakt) samen met de aanwezigheidsstatus te melden. Daarom kan zowel aanwezigheid als quizsucces worden overwogen om de voortgang van de student te bepalen.

**Adobe Learning Manager-app voor Microsoft Teams**

De nieuwe Adobe Learning Manager-app op Microsoft Teams is ontworpen om het leren in de workflow te bevorderen en sociaal leren te stimuleren. Studenten hebben toegang tot leerinhoud binnen het platform Microsoft Teams zonder dat ze hoeven over te schakelen naar een browser. Neem contact op met uw CSAM voor de bètaversie van de Adobe Learning Manager-app op MS Teams.

### bugs gecorrigeerd in deze update

**Cursus**

* Een aangepaste auteur kan geen voorbeeld van een module bekijken als de cursus de status &quot;UNDER_CONSTRUCTION&quot; heeft. In het antwoord wordt Fout 404 weergegeven.
* De titel van de cursus op de pagina Cursus/Toevoegen van een auteur-app loopt over wanneer de titel van de cursus bepaalde tekenlimiet overschrijdt.

**Auteur**

* In de auteur-app overschrijdt de titel van de cursus (indien deze lang is) de paginagrenzen tijdens het maken van een cursus.
* Soms wordt een cursus toegevoegd, ook al is er geen auteur geselecteerd.

**Dashboard-rapporten**

* Knopinfo wordt mooi weergegeven wanneer de interfacetaal Engels is, maar genereert een consolefout wanneer de interfacetaal anders is.
* Wijzig de naam &quot;Verplicht&quot; in &quot;Vereist&quot; in het Studentendashboard.

**Docent-app**

* De tijdnotatie in de docent-app is niet consistent met de andere apps.

**Sociaal**

* Voor bepaalde soorten posten wordt de sociale raad na het posten niet zoals verwacht geopend.

**Beheerder**

* Een gebruiker met een aangepaste rol kan geen bronnen downloaden wanneer een voorbeeld van een cursus wordt weergegeven.

**E-mailsjablonen**

* Wanneer een student zich uitschrijft voor een leerprogramma dat een klassikale/VC-cursus bevat, ontvangt hij/zij geen e-mail over annulering.

**Taakhulpen**

* U kunt de naam van de cursus niet zien op de taakhulpenwidget.

**Publiceren**

* De modulebeschrijving die in Adobe Captivate is toegevoegd, is niet zichtbaar in Leermanager wanneer de module in ALM wordt gepubliceerd.

**Actieve velden**

* Wanneer een CSV met een groot aantal verslagen in proces is, vergt het een significante hoeveelheid tijd, waarin, als een gebruiker het programma opent en een waarde voor één van de attributen ingaat, het tot een nieuwe gebruikersgroep kan leiden die in fouten CSV zou kunnen resulteren. Om dat te verhelpen, wordt het pop-upbericht voor het kenmerk Actieve velden uitgeschakeld en wordt het opnieuw ingeschakeld zodra het CSV-uploaden is voltooid. Dit bericht wordt weergegeven wanneer de CSV-bestanden worden geïmporteerd.
* Als de kolom in het CSV-bestand van Gebruikers dezelfde naam heeft als het actieve veld voor externe gebruikers, mislukt het uploaden van de CSV.

**API-gerelateerde oplossingen**

* In de reactie learningObjects ontbreekt het bladwijzerkenmerk.
* Er wordt een toegangsitem gemaakt tijdens het genereren van een beide vernieuwingstokens voor verwijderde gebruikers.
* De LO-API retourneert een onjuiste loFormat, omdat er voor de berekening van het cursustype samen met de kerninhoud rekening is gehouden met voorbewerkingsmodules.

**Bekende problemen in deze update**

* De knop Delen in de studentencatalogus werkt niet zoals verwacht in de Safari-browser, de mobiele en iPad MS Teams-app.
* Meldingen worden niet weergegeven op het tabblad Activiteit nadat de app is verwijderd op andere computers.
Er gebeurt niets als u op de meldingen klikt op het tabblad Activiteit van de app op iPhone 14.
* In de app MS Teams worden de status en de naam van de cursus niet weergegeven op het tabblad Activiteit in de meldingen van de Learning Manager (voltooid, ingeschreven, deadline en verstreken).
* Er wordt een pop-up met XML-inhoud weergegeven wanneer de integratiebeheerder de MS Teams-app niet goedkeurt.
* De gebruikersinterfacetaal in de Adobe Learning Manager-app op MS Teams verandert niet zoals verwacht wanneer de taal wordt gewijzigd.
* U kunt niet communiceren met de eerste melding als de focus zich binnen het iFrame bevindt (tabbladen Home en Catalogus).

**Beperkingen van de mobiele app van Adobe Learning Manager**

* Het weergeven van offline inhoud.
* De raster-/lijstweergave op de pagina Catalogus/Mijn leerervaring.
* Meerdere pogingen om een cursus te volgen.
* Inschrijvingsdeadline op een cursuskaart.
* Op iOS-apparaten worden pushmeldingen niet weergegeven wanneer de app op de voorgrond staat.
* Diepe koppelingen in pushmeldingen worden niet omgeleid naar de bedoelde openingspagina.
* Als u op de knop Interesse registreren klikt, wordt het web weer geopend.
* Tijdens het reageren op of het plaatsen van opmerkingen in Sociaal leren kunt u geen bestand bijvoegen.
* U kunt zich niet aanmelden bij LinkedIn Learning.
+++

+++Update 88

**Releasedatum:** 7 maart 2023

### Prestatieverbeteringen in deze release

Wanneer een bulkinschrijving van studenten wordt uitgevoerd, wordt er geen logbestand gegenereerd voor elke student.
We hebben de verwerking van leerplannen voor grote accounts geoptimaliseerd. Zo voorkomt u zoekproblemen of vertragingen.
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

In de Learner-app mislukt het zoeken naar gebruikers en gebruikersgroepen vanwege een aantal problemen met de landinstellingen.
+++

+++Update 85

**Releasedatum:** 13 februari 2023

### Wat is gewijzigd in deze update

Er is ondersteuning toegevoegd voor vierletterige taalcode tijdens het filteren van talen in GET learningmanagerapi/v2/learningObjects.

### In deze update opgeloste bugs

Voor sommige landinstellingen retourneert de zoekopdracht onjuiste resultaten.
De metagegevens van de cursus worden overschreven wanneer de cursus meer dan één variant van dezelfde landinstelling heeft.
+++

+++Update 84

**Releasedatum:** 2 februari 2023

### Wat is gewijzigd in deze update

**Taakhulpenrapport**

Deze update bevat een nieuw taakhulprapport met alle taakhulpen in het account.

**Versiebeheer**

We hebben versiebeheer voor bronnen toegevoegd bij het toevoegen van de leermiddelen tijdens het maken van een cursus.

**Rapport voor pogingen**

Een student kan voor elke training een rapport bekijken van alle pogingen en revisies.

**Module reset API**

Een beheerder kan een module nu opnieuw instellen met behulp van de Module reset API. Zie voor meer informatie [Adobe Leermanager-API-referentie](https://captivateprime.adobe.com/docs/primeapi/v2/).

**E-mailsjabloon**

Voor een paar e-mailsjablonen kunt u nu een vereiste aan de sjabloon toevoegen.

**Overige wijzigingen**

* U kunt een door de manager goedgekeurde cursus als vereiste toevoegen.
* Prestatieverbetering bij het vernieuwen van het leeroverzichtdashboard.
* E-mail-ID&#39;s en account-ID&#39;s worden geverifieerd voordat een stuiterrapport wordt verzonden.

### BUGS DIE ZIJN OPGELOST IN DEZE UPDATE

* Dubbele auteursnamen worden weergegeven op de pagina Cursusoverzicht.
* Een hyperlink op de pagina voor het maken van een account leidde tot Fout 404.
* De Tsjechische landinstelling komt niet overeen met de verwachte instellingen voor de speler.
* In sommige gevallen worden vaardigheden als ongedefinieerd weergegeven voor nog lopende en niet begonnen studenten.
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

Voor Linked in learning connector is er een nieuw selectievakje waarmee Student zich kan uitschrijven op de pagina Filters. Zie voor meer informatie [LinkedIn Learning-connector](/help/migrated/integration-admin/feature-summary/connectors.md).

### In deze update opgeloste bugs

* Als u de muisaanwijzer op staafdiagrammen plaatst, wordt de knopinfo van het dashboardrapport weergegeven zoals verwacht.
* In Rapporten onder Gebruikersactiviteit geeft het rapport Bestede leertijd onjuiste gegevens voor dagelijkse/maandelijkse gegevens weer.
* In sommige gevallen geeft de quizscoregrafiek onjuiste waarden weer.
* In een cursus met SCORM-inhoud waarvoor meerdere pogingen zijn ingesteld, wordt de knop Opnieuw bekijken uitgeschakeld wanneer een student de cursus probeert.
* In sommige gevallen wordt de e-mail na het inschrijven van een student voor een cursus en het downloaden van een e-mailcontrolelogboek bezorgd, maar niet in het logbestand weergegeven.
* De agenda-uitnodiging voor een docent moet de tekstdocent in het onderwerp opnemen.
* Het pictogram van de trainingskaart weerspiegelt niet de gerelateerde aanbevelingen voor cursussen en de kaarten voor leerpaden die op de overzichtspagina van de cursus staan.
* Voeg een sectie Opgeslagen door mij toe aan de instellingen van de startpagina voor studenten.
* Voor bepaalde accounts wordt een gebruiker gevraagd zich aan te melden voor een SSO-account waarin Adobe-id vereist is.
* In tijdzones met Daylight Savings, wordt het &quot;start_time&quot;gebied berekend gebaseerd op het tijdverschil momenteel, niet gebaseerd op het tijdverschil in de daadwerkelijke begindatum en de tijd. Dit veroorzaakte uitnodigingen met onjuiste tijden.
* Wanneer een certificering terugkeert, wordt een kopie van de onderliggende cursussen intern in de database gemaakt. Deze cursussen worden dan in zoekacties weergegeven, in tegenstelling tot het verwachte gedrag.
* Wanneer het uploaden van een CSV mislukt, ontvangt u geen e-mailmelding.
* Als de namen van de actieve velden lang zijn, verdwijnen de namen wanneer ze worden gesleept en neergezet. Hierna werkt de knop Opslaan ook niet zoals verwacht.
* Een sessierapport wordt niet geëxporteerd via de aanwezigheids- en scorepagina van een cursus als de eerste gebruiker in het rapport een record heeft in de tabel met de activiteitsgraad en de opmerking als null heeft.
* Wanneer u de badges ophaalt met het beheerdersaccount, kunt u de lijst op de verwachte manier sorteren. Maar als u hetzelfde voor een student uitvoert, worden de resultaten niet gesorteerd.
* Als u een cursus kiest uit uw zoekresultaten en vervolgens probeert terug te gaan naar de zoekresultaten met de knop Vorige, verdwijnen de zoekresultaten.
* Niet alle gebruikers worden als docenten aan een gebruikersgroep toegevoegd in een sessie.
* Sjablonen die meerdere gebruikerssjablonen bevatten, hebben een aantal waarden op het onderwerp.
+++

+++Update 82

**Releasedatum:** 15 december 2022

* De GET LO-API bevat nu prijsinformatie, indien beschikbaar.
* Aan LT-rapporten wordt een nieuwe kolom, Voltooid door, toegevoegd. Zo kan de beheerder de voltooiingsbron van een LO beter identificeren.
* We hebben een nieuwe ILT-module toegevoegd waarin de status geslaagd/gezakt voor studenten en aanwezigheid kunnen worden vastgelegd. Docenten kunnen een student nu markeren als bezocht met geslaagd of aanwezig met de optie voor mislukken.
* Een beheerder kan nu van studenten verlangen dat ze de volgende module/cursus voltooien en ervoor slagen. Dit is van toepassing op vereisten, geordende cursussen en LP&#39;s.

**Opgeloste problemen**

* Problemen met Bahasa-talen van meeslepende mobiele ervaringen op de zijbalk en voettekst.
* Boeiende weergaveoplossingen voor module-voorvertoningen.
* Als u een zoekopdracht uitvoert in de beheerder en auteur, wordt de zoekopdracht uitgevoerd in een andere landinstelling dan de landinstelling die u hebt getypt.
* Wijzigingen in welkomstsjablonen voor e-mail werden niet opgeslagen na bewerking.
* Gebruikers met verschillende e-mail-id&#39;s en Adobe-id&#39;s konden zich niet aanmelden bij de mobiele app.
* Gebruikers werden onjuist geïdentificeerd tijdens het deelnemen aan Zoom-/BJ VC-sessies.
+++

+++Update 81 - november 2022-versie van Adobe Learning Manager

**Releasedatum:** 5 november 2022

**Opmerking:** Met deze versie van Adobe Learning Manager hebben gebruikers met inactieve accounts geen toegang meer tot hun accounts met behulp van subdomeinen. De accounts kunnen worden geopend met de account-id of door de pagina acapindex.html te gebruiken en de e-mail-ID in te voeren.

### Nieuwe functies in deze release

De november 2022-versie van Adobe Learning Manager bestaat uit:

* Meerdere SSO-configuraties
* Ondersteuning voor niet-aangemelde functies
* Paginaverbeteringen van trainingsoverzicht
* Player-aanpassing
* Imitatie van student en manager

Zie voor meer informatie [Nieuwe functies in de Adobe Learning Manager-versie van november 2022](/help/migrated/whats-new-2022-november.md).

**Opmerking:** Met de november 2022-versie van Adobe Learning Manager wordt Zoomen afgekeurd [JWT-verificatie in juni 2023](https://marketplace.zoom.us/docs/guides/auth/jwt/). Daarom blijft de Zoom-connector met JWT werken tot de vermelde datum, maar we raden gebruikers aan een Server-to-Server OAuth-app te maken om de functionaliteit in hun account te vervangen. Voor elke nieuwe verbinding wordt standaard Zoom OAuth-verificatie gebruikt.

### bugs gecorrigeerd in deze update

* Als student verschijnt een foutbericht wanneer u probeert toegang te krijgen tot een leerprogramma met meer dan 10 cursussen op mobiele apparaten.
* Als een cursus een herinnering heeft ingesteld die binnen dagen na het ontbreken van de deadline moet worden verzonden, wordt het e-mailbericht verzonden na een aantal dagen zoals verwacht, maar wordt het aantal dagen dat de deadline wordt gemist, n-1 in plaats van n.
* Een video wordt niet in de speler geladen als L1-feedback voor de cursus is ingeschakeld in de Learner-app en de gebruiker alleen een studentrol heeft.
* Een e-mail met een voltooiingsherinnering geeft niet de tijd weer in de tijdzone van de gebruiker zoals verwacht.
* Studenttranscripten die via dashboardrapporten worden gegenereerd, respecteren de filters niet en geven meer informatie weer dan vereist.
* U kunt geen inhoud selecteren waarin de interfacetaal niet als inhoudstaal is toegevoegd.
* Wanneer u zichzelf voor de tweede keer registreerde voor een cursus, was de URL die werd weergegeven onjuist.
* Wanneer een docent uit een VC-sessie wordt verwijderd, ontvangen zij geen e-mail om hen op de hoogte te stellen van de annulering van de sessie.
* De tekst &#39;minute&#39; op een tegel op de trainingspagina van de student wordt niet zoals verwacht vertaald naar Bahasa Indonesisch.
* Het dashboard Naleving geeft onjuiste gegevens voor niet-conforme studenten weer.
* Tijdens het toevoegen van een rapport kunt u geen cursussen of catalogi selecteren waaraan de interfacetaal niet is toegevoegd.
* In deze release zijn de volgende inhoudstalen toegevoegd:
   * Bulgaars
   * Vlaams
   * Portugees (Brazilië)

### Bekende problemen in deze update

* In sommige gevallen wordt de quizscoregrafiek niet zoals verwacht weergegeven. Als u de grootte van de grafiek wijzigt, wordt aan het begin een lege ruimte weergegeven. Bovendien worden niet alle vragen weergegeven en worden onregelmatig onjuiste gegevens weergegeven.
+++

+++Update 80

**Releasedatum:** 20 september 2022

* Aanmeldingsproblemen met de mobiele app op iOS zijn nu opgelost.
* Probleem met teruggestuurde e-mails opgelost.
* Docenten werden verkeerd op de hoogte gesteld, zelfs voordat ze door studenten werden ingediend.
* Een docent krijgt een e-mailmelding, ook al heeft een student geen activiteit verzonden.
* Nadat u een VC-sessie hebt gemaakt voor MS Teams of Adobe Connect, ontvangen docenten geen uitnodigingen voor de sessie.
* Onjuiste status in een leerpad.
* Verbeterde prestaties van de app.
+++

+++Update 79

**Releasedatum:** 18 augustus 2022

* Kalender-uitnodigingsbevestiging voor ILT-/VILT-sessies werkt nu met Google-agenda.
* Een manager van de winkel kan nu meldingen voor gebruikers onder hen zien, zelfs als ze als manager zijn verwijderd.
* In sommige gevallen mislukt de cursusinschrijving en wordt Fout 500 weergegeven.
* In sommige gevallen kunt u geen virtuele cursusinstantie voor teams wijzigen.
* Beheerders en docenten kunnen opmerkingen toevoegen voor gebruikers die geen ILT-/VILT-sessies hebben bijgewoond.
* Verbeterde prestaties bij het downloaden van grote rapporten.
* Wanneer de e-mail van een gebruiker wordt teruggestuurd, ontvangt de beheerder een e-mailmelding. Het e-mailbericht bevat een koppeling waarmee een CSV wordt gedownload met de lijst met gebruikers van wie het e-mailbericht is teruggestuurd als erop wordt geklikt. De beheerder kan vervolgens de benodigde actie ondernemen.
   * Het e-mailbericht wordt geactiveerd wanneer een e-mail stuitert of daalt.
   * De e-mail wordt eenmaal per dag getriggerd voor alle beheerders die aan de lijst zijn toegevoegd.
   * De koppeling verloopt over zeven dagen.
* Er wordt een foutbericht weergegeven wanneer wordt geprobeerd een reeds geïntegreerd Adobe Connect-account te integreren met een ander Learning Manager-account.
+++

+++Update 78

**Releasedatum:** 4 augustus 2022

### bugs gecorrigeerd in deze update

* Als u een cursus hebt die een module met een voorvertoning bevat en vervolgens een API gebruikt om de leermiddelen van de cursus op te halen, bevat de reactie geen gegevens van locatie, contentZipUrl en contentStructureInfoUrl.
* Onjuiste reactie na het verzenden van een XAPI-aanvraag van het Swagger-document, waarin de domeinnaam LearningManager is.
* In de map /boards/{id}/posts-API-reactie, wordt de eigenschap &quot;post.attributes.myPoll&quot; weergegeven als een leeg object.
* In sommige gevallen is voor een niet-aangemelde gebruiker de knop Toevoegen aan winkelwagen uitgeschakeld voor sommige cursussen of leerpaden.
* Onjuiste subdomein-URL op de brandingpagina.
+++

+++Update 77

**Releasedatum:** 24 mei 2022

**Opgeloste problemen in deze update:**

* Nieuwe cursussen respecteren de volgorde in de Salesforce-app niet. Als u de volgorde wijzigt, wordt de cursus niet in de gewenste volgorde weergegeven.
* Nadat u de instellingen in de klassieke startpagina hebt gewijzigd en deze hebt opgeslagen, worden de wijzigingen niet meer zoals verwacht opgeslagen. Dit gebeurt af en toe.
* HTML-code wordt weergegeven wanneer studenten hun meldingen controleren, wat een negatieve invloed heeft op de ervaring.
* Op het dashboard wordt de bestede tijd onjuist weergegeven als nul uur.

## UPDATE: Adobe Learning Manager wordt hernoemd naar Adobe Learning Manager

Dit is een update over een aanstaande wijziging en helpt u zich hierop voor te bereiden.

**Adobe Learning Manager als product wordt in juli 2022 omgedoopt tot Adobe Learning Manager**. Dit is een strategische inspanning die wordt gedaan om nauwkeuriger de aanpassing van het product aan bepaalde bedrijfsprioriteiten te weerspiegelen.

Het productteam onderneemt alle stappen om ervoor te zorgen dat er geen invloed is op uw gebruik van het platform. U kunt het product op de gebruikelijke wijze blijven gebruiken. De beheerders van het platform kunnen de nieuwe merknaam in bepaalde schermen in juli opmerken.

Als onderdeel van deze wijziging worden de toegangs-URL&#39;s voor Leerbeheer beïnvloed.

Als de toegangs-URL voor uw account bijvoorbeeld `https://learningmanager.adobe.com/XYZ`, wordt de nieuwe URL `https://learningmanager.adobe.com/XYZ`.

Alle bestaande URL&#39;s blijven werken.

Om deze actie te voltooien, werk met uw afdeling van IT van uw organisatie. Neem voor meer informatie contact met ons op via `learningmanagersupport@adobe.com`.
+++

+++Update 76

**Releasedatum:** 20 april 2022

* Oplossingen voor productterminologie in een paar dashboardrapporten.
* Een dubbele slash (&quot;//&quot;) in de URL van een eindpunt resulteerde in validatiefouten.
* Nadat u een pagina hebt vernieuwd, werden onjuiste gegevens weergegeven in de velden voor het voltooiingspercentage en het laatste bezochte veld.
* We hebben een aantal wijzigingen aangebracht in de manier waarop het waardecertificaat of een leerplan wordt berekend.
* Een aangepaste beheerder kon alle gebruikers als docenten toevoegen, ook al mocht hij/zij slechts één gebruiker toevoegen.
* Op een badge-PDF werd een onjuiste voltooiingsdatum weergegeven.
+++

+++Update 75

**Releasedatum:** 29 maart 2022

* In sommige accounts vindt de gebruikersimport, nadat de RAW CSV op de FTP-locatie is gekopieerd, niet zoals verwacht plaats en zijn er meerdere foutmeldingen.
* In eerdere versies van Learning Manager moest u Exavault FTP eerst configureren om het CSV-bestand te kopiëren om een Zoom-connector te configureren. In deze release wordt de FTP-connector niet meer gebruikt voor het CSV-bestand. U hoeft daarom niet eerst de FTP-verbinding te configureren.
+++

+++Update 74: Learning Manager AWS India-instantie

**Releasedatum:** 15 februari 2022

### Overzicht

An [instantie](https://learningmanagerapac.adobe.com/acapindex.html) van Learning Manager wordt nu gehost op AWS in Mumbai (ap-south-1). Voor klanten die dit Indiase exemplaar gebruiken, worden de persoonlijk geïdentificeerde informatie (PII) en de leerrecords van gebruikers alleen in India opgeslagen.

### Wat wordt ondersteund

Adobe Learning Manager India is qua functiecapaciteit vergelijkbaar met andere instanties zoals EU- en VS-regio&#39;s. Er zijn een paar functies die niet worden ondersteund in India. Dit zijn:

* Creditcard betaling voor aankoop van licenties
* Creative Cloud-inhoudscatalogus
* Slack-app
* **&#42;** Wachten op certificering voor SOC2-compatibiliteit

### Veelgestelde vragen

**Hoe verschilt deze instantie in Mumbai van andere omgevingen met alleen AWS?**

Er is geen verschil. De instantie in Mumbai is hetzelfde als [AWS US](http://learningmanager.adobe.com/) of [AWS EU](http://learningmanagereu.adobe.com/) instanties. Dit exemplaar wordt gehost in India, en alle leerrecords en gebruikersdata blijven in India. De volgende functies worden niet ondersteund in de instantie India:

* Creditcard betaling voor aankoop van licenties
* Creative Cloud-inhoudscatalogus
* Slack-app
* **&#42;** Wachten op certificering voor SOC2-compatibiliteit

**Zal dit milieu gemeenschappelijk Kader van Controles (CCF)-Volgzaam zijn?**

Ja. De nieuwe instantie is compatibel met Common Control Framework (CCF).
+++

+++Update 73

Releasedatum: 5 februari 2022

* Ondersteuning voor e-mailsjablonen is nu beschikbaar voor inhoudstalen, waaronder Hongaars en Fins.
+++

+++Update 72 - januari 2022-versie van Learning Manager

Releasedatum: 15 januari 2022

### Nieuwe en gewijzigde functies

* Locaties voor lesruimten toevoegen
* Gamificationwijzigingen
* Microsoft Teams connector
* API-wijzigingen
* Mobiele immersive webwijzigingen

<!--
For more information, see What's new in the [**January 2022 release of Adobe Learning Manager**](../whats-new.md).
-->

### In deze versie gecorrigeerde bugs

**Inhoudsbibliotheek**

* Het zoeken naar inhoudsbestanden in mappen met persoonlijke inhoud werkte niet voor gebruikers met aangepaste rolbevoegdheden. Dit is nu opgelost.

**Cursussen**

* Verwijderen van een cursus of leerpad was niet mogelijk als ze een historische associatie hadden met een leerplan. Dit is nu opgelost. Gebruikers kunnen nu een cursus of leerpad verwijderen als deze niet aan een leerplan zijn gekoppeld.
* Als u een voorbeeld van een cursus of leerpad bekijkt en het bronbestand een lange naam zonder spaties heeft, loopt de bestandsnaam niet terug zoals verwacht en loopt deze over op de volgende regel. Dit probleem is opgelost.
* In het geval van een virtuele lesruimte kon u eerder een module maken zonder daar een VC-conferentiesysteem te selecteren omdat in een nieuwe instantie VC URL niet de vereiste informatie had. Dit wordt nu vermeden door een foutbericht in het ontwerpstadium van de module waarin u wordt gevraagd het VC-conferentiesysteem op te geven voordat u de module kunt opslaan.
* Op de wachtlijstpagina werd een misleidend bannerbericht voor geregistreerde gebruikers weergegeven, dat nu wordt verwijderd.
* Bij bulkuitschrijving voor cursussen werd het pop-upvenster voor het invoeren van e-mailadressen niet weergegeven. Dit probleem is nu opgelost.
* De optie om e-mail naar studenten te verzenden vanuit het tabblad Aanwezigheid en scores in de app voor beheerders en docenten sluit niet uit dat niet-geselecteerde studenten na het uitvoeren van de geselecteerde bewerking worden verzonden. Daarom stuurde Leermanager e-mail naar alle studenten. Dit probleem is nu opgelost.
* Het inschrijvingsrapport wordt weergegeven als &quot;Niet gestart&quot;, ook al heeft een student de cursus al voltooid.

**SSO**

* In opstelling SSO, als entiteitsidentiteitskaart om het even welke belangrijke of trainingsruimten had toen login configuratie niet werkte, wordt dit nu behandeld als deel van de moeilijke situatie.

**Aankondigingen**

* Als beheerder werden de begin- en einddatums voor een aankondiging niet opgeslagen als de interface- en inhoudstaal was ingesteld op Deutsch/Espanol. Dit probleem is nu opgelost.

**E-mailsjabloon**

* Sessieuitnodigingen die meerdere dagen beslaan, waarbij de uitnodigingen niet de juiste informatie weerspiegelen op dagen, worden geblokkeerd door sommige e-mailclients. Dit is nu opgelost.
* De variabele &#39;Venue Name&#39; ontbrak in de e-mailsjabloon &#39;Herinnering voor aanstaande sessie&#39; voor studenten met een Duitse landinstelling. Dit is nu toegevoegd.
* De koppeling om een account te maken als onderdeel van de welkomstmail naar de gebruiker hield geen rekening met de gebruikerslandinstelling die nu is hersteld.

**E-mailherinneringen**

* Als studenten via een leerplan voor training waren ingeschreven, werden de e-mails met de voltooiingsherinnering meerdere keren verzonden op basis van het aantal bewerkingen dat is uitgevoerd op de voltooiingsdata van hetzelfde leerplan. Dit probleem is nu opgelost.

**Gebruiker**

* Het bericht dat aan gebruikers wordt getoond wanneer zijn/haar account inactief/geschorst is verbeterd om hun beheerder te bereiken dat hun accounts opnieuw worden ingeschakeld.

**Activiteit**

* Een docent kan de inzendingen van de student niet bekijken als de bestandsnaam voor inzending een speciaal teken bevat. Dit is nu opgelost.

**Rapport**

* Een beheerder kan het inschrijvingsrapport voor de cursus niet downloaden als het een student bevat die indirect via een flexibel leerpad voor deze cursus is ingeschreven, maar nog geen instantie voor deze cursus in het leerpad moet kiezen. Dit probleem is nu opgelost.
* Het herschikken van rapporten in het dashboard Rapporten voor beheerder- en managerrollen bleef de status van de rapportvolgorde niet behouden. Dit probleem is nu opgelost.

**Inhoud**

* Audio in trainingsinhoud werd niet automatisch afgespeeld in de voorvertoning als studentenmodus vanwege het automatisch afspeelbeleid van de browser. Dit probleem is nu opgelost voor ondersteunde browsers, behalve Safari.

**Gamification**

* Als een externe student in hetzelfde account is omgezet als interne student, heeft hij/zij geen toegang tot het leaderboard voor gamification in de Learner-app. Dit probleem is nu opgelost.

**Speler**

* De speler gaf geen waarschuwingsbericht weer wanneer de gebruiker probeerde over te stappen op modules in een geordende cursus met AICC-modules. Dit is nu opgelost.
* Voor bepaalde verworven cursussen met videomodules in headless LMS-case werkte het afspelen niet voor bepaalde gebruikers. Dit probleem is nu opgelost.

**Managerdashboard**

* Een manager kan het rapport voor zijn directe team niet exporteren van de pagina met teamvaardigheden van het Managerdashboard. Dit probleem is nu opgelost.

**Publiceren**

* In de European instance of Learning Manager content die rechtstreeks werd gepubliceerd naar de Adobe Learning Manager van Adobe Captivate, werd standaard gepubliceerd in de landinstelling Deutsch. Dit is nu opgelost.

**API**

* Het veld Duur wordt nu toegevoegd aan het taakhulpmodel.
* Voor de aanbeveling-API&#39;s retourneert een verzoek van een GET soms Error 500.
* Wanneer je trainingen migreert via Exavault en de tekst niet-Engelse tekens bevat, werd de tekst bijgewerkt met ongewenste tekens in de tekst. Dit probleem is nu opgelost.

**Lokalisatie**

* `NormalTextRun  BCX0 SCXW38820519 For the`Admin-, auteur- en Learner-apps, sommige inhoud in het Duits wordt niet weergegeven zoals verwacht.

## Bekende problemen in deze release

* Wanneer u een bericht maakt op de pagina Sociaal leren, kunt u geen audio opnemen of de audio uploaden nadat u op de microfoon hebt getikt. Dit is een beperking van de browser.
* In iOS worden H264- en WMA-audiobestanden niet ondersteund in de mobiele browser.
* Studenten met een + in hun e-mailadres hebben hun voortgang niet gemarkeerd. Dit is nadat ze een VC-cursus volgen in Microsoft Teams.
* In de Safari Mobile-browser kunnen studenten niet meer dan 200 Mb-bestanden uploaden in Sociaal leren. Dit is browserbeperking.
+++

+++Update 71

Releasedatum: 17 november 2021.

### Training delen met managers

Learning Manager biedt het dashboard Naleving aan alle beheerders en managers. Managers vinden het zeer nuttig om naleving van hun teamleden voor een bepaalde opleiding te volgen. Tegelijkertijd willen beheerders dat alle managers compatibiliteitstrainingen toevoegen aan hun dashboard en deze bijhouden.

In Learning Manager wordt de **Delen met managers** Met deze workflow kunnen beheerders training delen met managers, zodat ze kunnen worden toegevoegd aan het dashboard Naleving van een manager. Managers hoeven dus geen actie te ondernemen en kunnen meteen beginnen met het volgen van de naleving.

Zie voor meer informatie  [**Training delen met managers**](../administrators/feature-summary/reports.md#share_training_managers).

### bugs gecorrigeerd in deze update

* Als er twee accounts zijn en de verbeterde functie Leerpad is uitgeschakeld en er een gedeelde catalogus is van het eerste account naar het andere, heeft het Leerpad in het tweede account dubbele secties op de cursuspagina.
* Naast http:// en https:// ondersteunt een aangepaste FTP nu sftp://
* Exavault-connector gebruikt nu V2 API&#39;s.
* In sommige gevallen was de kwaliteit van video&#39;s suboptimaal. Het probleem is nu opgelost.
* Zelfs nadat een student een verplichte cursus heeft voltooid en door de manager is goedgekeurd, blijft de certificering in afwachting van goedkeuring.
* Als de namen van auteurs tekens met accent bevatten, mislukt de migratie van de cursus.
* Als het actieve veld in hoofdletters waarden heeft, wordt het actieve veld niet opgeslagen zoals verwacht.
* Kan leerpaden niet filteren op basis van vaardigheden.
* Wanneer een beheerder een instantie maakt en een nieuwe sessie toevoegt, ontvangt een docent geen e-mail met de uitnodiging voor de sessie. Dit probleem doet zich voor in Zoom VC-cursussen.
+++

+++Update 70

Releasedatum: 28 oktober 2021

### bugs gecorrigeerd in deze update

* In sommige gevallen wordt informatie over een leerpad niet weergegeven in een Studenttranscript.
* De tekst in het **Voltooiing markeren** wordt bijgewerkt om aan te geven dat de bewerking onomkeerbaar is.
* De API voor leerobjecten heeft in sommige gevallen een metagegevensfout geretourneerd.
+++

+++Update 69 - oktober 2021-versie van Learning Manager

**Releasedatum:** 9 oktober 2021

### Leerpad

De **Oktober 2021-versie van Adobe Learning Manager** introduceert het concept leerpaden.

>[!NOTE]
>
>De **Instellingen > Algemeen** Deze pagina heeft een nieuwe optie om de uitgebreide mogelijkheden van leerpaden in te schakelen. Als deze optie is ingeschakeld, kunt u leerpaden toevoegen aan een ander leerpad. U kunt de optie niet meer wijzigen nadat deze is ingeschakeld.

Leerpaden vervangen onze bestaande functie van Leerprogramma&#39;s. Stel je leerprogramma&#39;s voor die krachtige verbeteringen krijgen zonder dat je bestaande mogelijkheden kwijtraakt. Bovendien wordt de functie gemarkeerd als een leerpad.

Zie voor meer informatie [***Leerpaden***](../administrators/feature-summary/learning-paths.md).

### Overige wijzigingen

* Nieuwe Salesforce-app
* Inhoudshub
* Rapportagewijzigingen
* Samenvattingsrapport van sessie
* Wijzigingen in inhoudsopgave van speler
* API-wijzigingen
* Wijzigingen met betrekking tot verbindingen

Zie voor meer informatie [***Nieuwe functies in de oktober 2021-versie van Learning Manager***](../whats-new.md).

### bugs gecorrigeerd in deze update

* E-mailsjablonen, zoals Cursusuitschrijving, Uitschrijving van leerprogramma of Uitschrijving van certificering, weerspiegelen niet de nieuwste productterminologieën zoals gedefinieerd in de CSV. De standaardtekst in e-mailsjablonen ondersteunt nu aangepaste terminologieën.
* De gebruikerstaal in Leermanager wordt niet ondersteund in de workflow Publiceren op Leermanager. Als de gebruikerstaal anders is, wordt Publiceren naar Leermanager in het Engels uitgevoerd.
* Als u veel catalogi toevoegt aan een aangepaste rol, treedt er een fout op wanneer u de rol bijwerkt. Nu wordt de limiet van het aantal catalogi verhoogd tot 50 catalogi.
* In sommige gevallen zijn trainingen die worden verwijderd, nog steeds zichtbaar in een catalogus. Dit probleem is alleen opgetreden in de Admin-app en is nu opgelost.
* Wanneer de managerrol van de ene gebruiker naar een andere wordt gewijzigd, werd de managerrol van de vorige gebruiker nog weerspiegeld in de UI. Dit is nu opgelost. Dit probleem is alleen aanwezig voor externe gebruikers en niet voor interne gebruikers.
* In sommige specifieke scenario&#39;s voor een grote groep gebruikers die worden geïmporteerd via gebruikers-CSV, is het importeren mislukt. Dit probleem is nu opgelost.
* In een leertranscript wordt de voltooiingsdatum voor een extern certificaat niet weergegeven als een verplichte cursus wordt toegevoegd nadat een extern certificaat is gemaakt en een gebruiker aan het certificaat is ingeschreven. Dit is nu opgelost.
* In een certificaat wordt de gelokaliseerde naam van de student niet weergegeven zoals verwacht. Dit is nu opgelost.
* In het geval van Zoom VC-sessies ontvangt een docent niet altijd de uitnodiging voor de sessie. Dit is nu opgelost. De docent ontvangt nu de vereiste communicatie.
* Een student ontvangt geen uitnodigingen voor een sessie als sjablonen op cursusniveau zijn ingeschakeld, maar sjablonen op accountniveau zijn uitgeschakeld. Dit is nu opgelost.
* Voor specifieke tijdzones werden e-mailherinneringen een dag later dan verwacht bezorgd. Dit is nu opgelost.
* Studenten ontvangen geen sessiemeldingse-mails als bepaalde e-mailsjablonen zijn uitgeschakeld.
* Als een BlueJeans-vergadering door auteurs, beheerders wordt bijgewerkt, werd de URL van de BJ-vergadering onbruikbaar. Dit is nu opgelost.
* Wanneer de GET/LO-API in sommige gevallen wordt uitgevoerd, worden de cursussen die deel uitmaken van een leerprogramma niet geretourneerd.
* Als de student inhoud probeert te uploaden waarvan de naam lege ruimte heeft, komt de student een interne serverfout tegen.
* De voor studenten gegenereerde badge-PDF hadden opmaakproblemen toen ze werden gegenereerd in niet-Engelse landinstellingen. Dergelijke problemen zijn nu opgelost.
+++

+++Update 68

Releasedatum: 28 september 2021

### bugs gecorrigeerd in deze update

* In de mobiele browser zijn diepe koppelingen ingeschakeld voor het volgende:

   * Alle boards
   * Openbare raad en post
   * Privéboard en Plaatsen met toegang
   * Privéboard en zonder toegang
   * Beperkte raad en functie
   * Opmerking op bericht
   * Reageren op opmerking
   * Profiel van sociale gebruiker

* Voor accounts die gebruikmaken van een aangepast domein, wordt het favicon niet weergegeven in de Learner-app.
* Bij AEM verwijdert de component Learning Manager de configuratie van andere componenten.
* De Help-pagina voor AEM component wordt omgeleid naar een onjuiste locatie.
* Extern ophalen en opslaan van e-mails/tokens van gebruikers zodat gebruikers hun eigen back-end voor opslag kunnen implementeren in plaats van AEM gebruikersknooppunten te gebruiken.
* Bij het bewerken van normale tekstbeschrijvingen in cursussen, leerprogramma&#39;s, certificaten en taakhulpen verschijnt een waarschuwingsbericht.
* De rapporten van het dashboard van de Manager worden niet gedownload wanneer een gebruiker zowel douane als managerrollen heeft.
* Een e-mailoverzicht geeft een onjuiste waarde van de trainingsactiviteit weer.
* In sommige gevallen gedraagt de leermanager zich onverwacht wanneer u van de Content Marketplace naar de studentenpagina gaat.
* In de sociale app werken de filters niet zoals verwacht in de lijstweergave.
* De welkomstmail die interne gebruikers ontvangen, wordt ook ontvangen door externe gebruikers.
* Voeg de widget Leerbeheer toe aan de paginasjabloon in AEM.
* Als u een certificaat opnieuw wilt publiceren nadat u een cursus hebt verwijderd, kunt u dit niet doen.
* Studenten ontvangen geen mails met de details van een sessie.
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

De **Augustus 2021** **release van Adobe Learning Manager** is gericht op het verbeteren van de leerervaring, rapportage en administratieve workflows. Enkele hooglichten zijn:

* **Contentmarktplaats:** Learning Manager biedt nu meer dan 70000 cursussen op verschillende domeinen, zoals Technologie, Beheer, Leiderschap, enzovoort.
* **Verbeterde toegankelijkheidsondersteuning:** Toegankelijkheidsondersteuning voor de studentrol versterkt via verbeterde toetsenbordnavigatie, mogelijkheden voor schermlezers en compliance met contrastverhouding.
* **RTF-opmaak:** Learning Manager biedt nu uitgebreide tekstbewerking voor beschrijvingen in cursussen, programma&#39;s, certificaten en taakhulpen. Op deze manier kunnen auteurs beschrijvingen in tekst met opmaak opgeven, zoals hyperlinks, afbeeldingen en andere tekstopmaakopties, in plaats van tekst zonder opmaak.
* **Sterrenclassificatie:** Een student kan nu een cursus beoordelen op een schaal van 5 punten. Een beheerder kan kiezen uit een bestaande effectiviteitsscore of een classificatie van 5 sterren.
* **Badgr-integratie:** Studenten kunnen Leermanager nu toestaan om badges die ze in Leermanager hebben verdiend, automatisch naar hun Badgr-account te pushen, vanwaar ze hun badges in hun sociale netwerken kunnen delen.
* **Leergebeurtenissen exporteren naar Salesforce:** Learning Manager biedt nu de mogelijkheid om bepaalde specifieke gebeurtenissen in Learning Manager te exporteren, zoals toevoeging, inschrijving en voltooiing van nieuwe gebruikers, naar een Salesforce-tenant, en biedt de mogelijkheid om deze te koppelen aan het juiste gebruikersobject of Contact-object in Salesforce.

Zie voor meer informatie [***Nieuwe en gewijzigde functies in de augustus 2021-versie van Learning Manager***](../whats-new.md).


**Releasedatum:** 7 augustus 2021

### bugs gecorrigeerd in deze update

**Leerervaring**

* Nadat een student aan twee gebruikersgroepen is toegevoegd en er een leerplan is toegevoegd, wordt de student ingeschreven voor een andere instantie van dezelfde cursus.
* In sommige gevallen wordt de cursus niet zoals verwacht afgespeeld nadat u zich hebt ingeschreven en de cursus hebt gestart.
* In de cursusbeschrijving worden HTML-tags weergegeven, die nu zijn gecorrigeerd.
* Als u een opmerking plaatst op een bericht op een sociaal board dat meerdere regels beslaat, wordt de opmerking op één regel weergegeven. Dit is nu opgelost.

**Ontwerpen**

* In sommige gevallen met automatische inschrijvingen ontvangen studenten meerdere e-mails over inschrijvingen.

**Rapportage**

* Wanneer de interface is ingesteld op een aantal niet-Engelse landinstellingen, genereren Studenttranscripten niet zoals verwacht.
* Mogelijkheid om de voortgang van een cursus opnieuw in te stellen binnen een leerprogramma en certificering.
* Als een CSV actieve velden met dezelfde naam maar met verschillende hoofdlettergevoeligheid bevat, produceert de CSV een uitzondering.

**Overige**

* De optie voor het bewerken van scores en opmerkingen moet worden uitgeschakeld als er geen student is geselecteerd of als de aanwezigheid van de geselecteerde student niet is gemarkeerd.
* Waarden in actieve velden worden in kleine letters weergegeven in het dialoogvenster Gebruiker bewerken, ook al heeft een gebruiker eerder de waarden in hoofdletters toegevoegd.
* Beheerders en beheerders kunnen goedkeuringen die in behandeling zijn voor cursussen bekijken. Hierdoor kan het management ervoor zorgen dat managers het leren en trainen van werknemers volgen en kunnen beheerders van leerprogramma&#39;s cursusinschrijving goedkeuren als dat nodig is.
* Een gebruiker met een auteur- of aangepaste beheerder-/auteursmachtiging kan een taakhulp die door een andere gebruiker is gemaakt, niet bewerken.
* Wanneer de gebruiker vanuit de beheerdersrol naar Cursus > Instantie navigeert en voor een instantie de optie &#39;Ingeschreven studenten&#39; selecteert, toont deze eerder de studenten uit &#39;Standaardinstantie&#39;. De beheerder moest de instantie handmatig uit het vervolgkeuzemenu wijzigen. Nu navigeert Leermanager correct de gebruiker naar de studentenpagina met de juiste instantie geselecteerd.

**Apparaatapp**

* Op Android- en iPhone-apparaten kan een student niet willekeurig cursusmodules starten. Dit leidt tot Fout 401 onbevoegd.
* Een student kan twee QR-codes scannen, maar bij het scannen van de derde QR-code wordt een foutbericht weergegeven.
* Op sommige Android- en iOS-apparaten wordt een bestand niet geopend zoals verwacht voor sommige gedownloade cursussen.
* Als u een taakhulp probeert te openen, wordt een foutbericht weergegeven.
* De apparaatapp gedraagt zich onverwacht wanneer een leerprogramma offline wordt gebruikt.
* Wanneer een student weer online gaat en de app opent, blijft de app vastzitten op het welkomstscherm.
* Wanneer een gebruiker weer online is, schakelt de app soms over naar de klassieke weergave.
* Wanneer een cursus offline wordt gebruikt, wordt de voortgang niet opgeslagen.
* Soms wordt een cursusnaam niet zoals verwacht vanaf het begin weergegeven wanneer de naam lang is.
* Op de cataloguspagina worden de cursussen niet zoals verwacht gesorteerd.
+++

+++Update 65

Releasedatum: juli 2021

### bugs gecorrigeerd in deze update

* Problemen met aanmeldingen voor gebruikers.
* De e-mailsjabloon voor cursusinschrijving voor manager geeft niet de deadline voor cursusvoltooiing weer als de variabele aan de sjabloon wordt toegevoegd.
* TLS 1.0 en TLS 1.1 zijn vervangen.
* Problemen met het verwijderen van AVG-gegevens voor een gebruiker.
+++

+++Update 64

Releasedatum: juli 2021

### bugs gecorrigeerd in deze update

* Studenten die zich al voor een cursus hebben ingeschreven, ontvangen een melding voor inschrijving.
* Wanneer een aangepast certificaat als badge wordt gegenereerd, wordt de datumnotatie niet ondersteund in de Duitse taal.
+++

+++Update 63

Releasedatum: juni 2021

### bugs gecorrigeerd in deze update

* U kunt een gebruiker met een lege naam in een CSV-bestand maken.
* Als er een &#39;/&#39;-teken in het actieve veld staat na het maken van een taak voor het downloaden van user.csv, verandert de status van de taak niet van &quot;Verzonden&quot; in &quot;Voltooid&quot;.
* Geordende modules respecteren de sequentie niet.
* Wanneer een externe auteur wordt verwijderd, is de cursus die de auteur heeft gemaakt niet meer beschikbaar.
* Het zoeken naar een leerobject met meer dan één vaardigheid levert onverwachte resultaten op.
+++

+++Update 62

Releasedatum: juni 2021

### bugs gecorrigeerd in deze update

* Aanmelden bij de app is niet mogelijk wanneer de account is gestart met aanmelding met SP.
* Video&#39;s worden niet gerenderd vanuit Helderheid zoals verwacht.
* De userGroupInfo-API is niet zichtbaar tijdens een bezoek aan het leerprogramma in een van de apps.
* Kan niet zoeken in een gearchiveerd leerprogramma en certificering tijdens het maken van een dashboardrapport.
* Een auteur kan een taakhulp die door een andere auteur is gemaakt, niet bewerken of bijwerken.
* De API voor het indienen van bestanden werkt niet zoals verwacht in de EU-cluster.
+++

+++Update 61

Releasedatum: mei 2021

### bugs gecorrigeerd in deze update

* Prestatieverbetering bij userGroupInfo-aanroepen.
* Na het inschakelen van nieuwe Helderheidsprofielen ondersteunt Learning Manager inhoud met video- en audiomodules.
* Leertranscripten kunnen de gegevens niet vastleggen als een smal datumbereik is geselecteerd.
* Er wordt een sessie-uitnodiging voor alle sessies naar de ingeschreven studenten verzonden, zelfs als er maar één nieuwe sessie is toegevoegd.
* Audiomodules worden niet naar verwachting geüpload.
+++

+++Update 60

Releasedatum: april 2021

### bugs gecorrigeerd in deze update

**Rapport**

* Als u na het maken van een rapport naar een gearchiveerde cursus zoekt, kunt u dit niet doen.
* Fouten in één rapport worden doorgegeven aan anderen. Als gevolg daarvan leidden deze verslagen tot fouten.

**Taakhulpen**

* Nadat u een taakhulp hebt gedownload, kunt u deze niet meer verwijderen.

**Speler**

* WebVTT-bijschriften verschijnen niet zoals verwacht.

**Learner-app**

* Op de pagina Certificatie-overzicht geeft Externe certificering niet de duur weer die door een auteur is toegevoegd.
* De optie toevoegen **Alles** in het filter Vaardigheid.
* Studenten ontvingen meerdere digest-e-mails.
* Het aantal geselecteerde rijen komt niet overeen met het aantal rijen dat op een pagina wordt verwacht.

**AEM**

* Widgets worden niet zoals verwacht bijgewerkt nadat een pagina is vernieuwd.

**Lokalisatie**

* Een paar Duitse tekenreeksen zijn niet gelokaliseerd zoals verwacht.
* De vertaling van tekenreeksen is standaard in het Engels als een student de interface- en inhoudstaal niet heeft geselecteerd.

**Certificering**

* Het ordenen van de module kan worden omzeild als de voorwaarden niet worden nageleefd.

**Browser**

* Auteur-, manager- of student-apps worden niet zoals verwacht weergegeven in IE 11.

**Gamification**

* Gamificationpunten worden niet ingewisseld zoals verwacht.

**Inhoudsbibliotheek**

* Cursussen voor proefversie van inhoud werken niet zoals verwacht.

**Speler**

* De speler wordt alleen geladen in de ruimte waarin de widget aanwezig is.
* Video&#39;s in een Captivate-module worden niet naar behoren afgespeeld.

**Connector**

* In sommige gevallen worden bestanden verwijderd uit een FTP/Box-connector.
* Bestanden worden verwijderd uit ftp als de bestanden met dezelfde naam worden bijgewerkt.
* Een gebeurtenis BlueJeans ondersteunt paginering wanneer het aantal gebeurtenissen groter is dan 100.

**Update voor mobiele apps 3.3 - maart 2021**

Releasedatum: 26 maart 2021.

### Nieuwe en gewijzigde functies {#whatsnewandchanged}

Captivate Learning Manager Mobile App-update 3.3 introduceert een gloednieuwe startpagina die mastheads en op AI gebaseerde trainingsaanbevelingen ondersteunt. Deze startpagina is beschikbaar voor alle accounts die zijn geconfigureerd voor de nieuwe optie Immersive Layout. Voor de accounts die zijn geconfigureerd met de klassieke lay-out, wordt de klassieke/verouderde startpagina nog steeds weergegeven. Zij zouden geen veranderingen in de homepage moeten waarnemen.

Bovendien kunnen studenten met deze update ook hun badge als PDF en een afbeelding downloaden. De update introduceert ook een pop-up met feedback, waarmee studenten anoniem feedback over de app kunnen geven.

Zie voor meer informatie  [Apparaatapp van Learning Manager](../learners/feature-summary/ipad-android-tablet-users.md).

Lees verder voor meer informatie.

#### Nieuwe startpagina

Voor alle accounts waarvoor de optie Immersive Layout ingeschakeld is, is er een gloednieuwe startpagina die de configuratie van Immersive Layout ondersteunt.

#### Feedbackscore

In deze release vraagt Leermanager de gebruiker om feedback te geven over de ervaring die de mobiele app heeft opgedaan.

#### Badge downloaden

Met deze update kunnen studenten hun badges in PDF- en afbeeldingsindeling downloaden.

<!--## Previous update releases {#previousupdatereleases}-->
+++

+++Update 60 - Februari 2021-versie van Learning Manager

Releasedatum: 20 februari 2021

### Nieuwe en gewijzigde functies {#Whatsnewandchanged-1}

* Boardweergave in het sociale leven.
* De sociale banner aanpassen.
* Catalogusfilters in Learner-app.
* Uitschrijving uit training.
* Importeer gebruikers uit Salesforce-contactpersonen.
* ...en nog veel meer.

Zie Nieuwe functies in de [Update van leermanager van februari 2021](../whats-new.md).

### bugs gecorrigeerd in deze update {#bug-fixes}

**Certificering**

* In sommige gevallen kon een student een cursus niet opnieuw proberen, die deel uitmaakt van een certificering, ook al zijn de maximale pogingen voor de cursus ingesteld op oneindig. Dit probleem is nu opgelost.
* In sommige gevallen kan een student zich niet inschrijven voor een certificering vanwege de **Inschrijven** niet zichtbaar zijn zoals verwacht.

**Inhoudsbibliotheek**

* Onjuiste Help-URL op de **Nieuwe inhoud toevoegen** pagina. De juiste URL is bijgewerkt.

**Cursus**

* Een L2 Quizscore-rapport dat voor een AICC-inhoudsmodule is gedownload, geeft een onjuiste score weer onder de kolom Totale gebruikersscore/Quizscore. Dit probleem is opgelost.
* Bronnen van een cursus downloaden werkte niet als deze vanuit een andere cursus worden gedupliceerd als de student geen toegang had tot de oorspronkelijke cursus die werd gebruikt om een dubbele cursus te maken.
* Bannerafbeeldingen waar deze niet worden verwijderd wanneer de auteur deze verwijdert terwijl de cursus in de conceptstatus staat. Dit probleem is opgelost.

**AEM**

* Na het invoegen van de component Leermanager in AEM duurde het lang voordat de pagina werd geladen, zodat toegang tot de andere componenten niet meer mogelijk was. Dit probleem is opgelost.

**Beheerder**

* Gearchiveerde cursussen worden niet zoals verwacht weergegeven in de zoekresultaten. Dit probleem is opgelost.
* Beheerder kan niet zoeken naar gearchiveerde cursussen in **Admin-app** -> **Aangepaste rapporten** -> **Excel-rapporten** -> **Cursusrapporten**, die nu is opgelost.

* Het downloaden van een quizrapport als Excel werkt niet als het bestand studenten bevat die de trainingen voor en na het bijwerken van de inhoud hebben gevolgd. Dit probleem is opgelost.
* Een CSV-upload mislukt als de actieve velden speciale tekens bevatten. Dit is opgelost.
* In een paar gevallen, wanneer een student een quiz aflegt die in Captivate is gemaakt, worden de antwoorden niet vastgelegd zoals verwacht.
* Nadat u een abonnement hebt gemaakt en hebt geprobeerd het abonnement te bewerken, kunt u het **Opslaan** en **Annuleren** knoppen worden niet zoals verwacht weergegeven. Dit is opgelost.

**Speler**

* Voor een specifiek type inhoud van het SCORM-2004-cv-scenario werkte niet. Studenten moesten dus naar het punt navigeren waar ze waren opgehouden. Dit is nu opgelost. De inhoud moet nu worden hervat vanaf het punt waar deze eerder werd gebruikt.
* Na het inschrijven voor een cursus wordt de inhoud in sommige gevallen niet zoals verwacht afgespeeld. Dit probleem is opgelost.

**Uitschrijving**

* In een inschrijvingsrapport worden alleen 20 uitgeschreven studenten weergegeven, zelfs als er meer studenten zijn uitgeschreven voor de cursus/certificering. Dit probleem is opgelost.
* In sommige gevallen was er een probleem bij het exporteren van de lijst met uitgeschreven studenten in inschrijvingsrapport. Dit is nu opgelost.

**Leerprogramma**

* Als een student voor een flexibel leerplan slechts voor een van de cursusinstanties is ingeschreven en vervolgens op de cursuskoppeling van de andere cursussen waarvan de instanties niet zijn geselecteerd, klikt, wordt er een lege pagina geopend.

**Student**

* Enkele studenten, wier gebruikersnamen speciale tekens hebben, ontvangen geen e-mailmeldingen zoals verwacht.
* In de meeslepende weergave worden in sommige gevallen de volgende VC-sessies niet zoals verwacht weergegeven in de kalenderwidget.
* In de Learner-app **Vaardigheid** werkt niet zoals verwacht. Dit probleem is opgelost.

**Zoeken**

* In een bepaald scenario kon de manager niet eerder naar de gebruikersgroep van een manager zoeken. Dit probleem is nu opgelost voor de managerrol.

**Gebruikersgroep**

* Bij het exporteren van een gebruikersgroeprapport met meer dan 500 gebruikers kwamen de gegevenswaarden en de kolomkoppen in het rapport niet overeen wat nu is gecorrigeerd.
* Wanneer de beheerder de e-mailhandtekening in e-mailsjablonen bewerkt en meerdere regels toevoegde, werd de HTML-tags alleen weergegeven in de beheerinterface. Dit probleem is nu opgelost.
* In **Admin App > Catalog > Zoeken naar catalogus**, kunt u niet zoeken.

**Gebruikers**

* Enkele actieve externe gebruikers werden verwijderd. We hebben wijzigingen aangebracht en het probleem is nu opgelost.

**Importeren**

* Het importeren van een CSV-bestand mislukt als de CSV-header volgspaties bevat of als het e-mailadres van een gebruiker accenten of diakritische tekens bevat.

**Verzending activiteit**

* In de app Docent-activiteit, verzendpagina voor activiteiten, overlapte de verzonden datumwaarde met de bestandsnaam als het een lang probleem was dat nu wordt opgelost.

**Docent**

* Een docent ontvangt sessieuitnodigingen voor al zijn/haar sessies, ook al wordt alleen een nieuwe sessie toegevoegd. Dit probleem is opgelost.

**SCORM**

* Voor bepaalde SCORM-inhoud zijn er weinig browsergerelateerde problemen, problemen met de navigatie van de speler en inconsistenties in de opname van quizscore. Deze problemen zijn opgelost.

**SAML en SSO**

* We hebben het foutbericht bijgewerkt dat u ziet wanneer de SSO-referenties zijn verlopen.

**Learning Manager-API**

* De API getlearningObject heeft onjuiste inschrijvingsgegevens geretourneerd vanwege problemen in cache. Dit probleem is opgelost.
* Een VC-sessie geeft nu de URL van de vergadering weer in het veld Locatie in een vergaderuitnodiging.
* Als u meerdere VC-providerintegraties hebt ingesteld en een van deze integraties niet naar behoren functioneert, wordt het vervolgkeuzemenu VC-selectie gebruikt om een lege lijst weer te geven. Dit is nu opgelost. Resterende VC-integratie wordt nu correct weergegeven.
* Connect VC-sjablonen worden niet zoals verwacht geladen wanneer een docent zich bij de sessie aansluit.
* In de gebruikersinterface wordt een onjuiste duur weergegeven na het migreren van modules met tijdsduur in het csv-bestand module_version.
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

### BlueJeans Event-connector {#bluejeanseventconnector}

BlueJeans Events-connector verbindt Learning Manager- en BlueJeans-systemen om de synchronisatie van data te automatiseren. Met deze connector kunt u:

* **Virtuele sessies instellen met BlueJeans Events:** Configureer een nieuwe gebeurtenis in BlueJeans en stel een VC-sessie in Learning Manager in door de juiste BlueJeans-gebeurtenis te selecteren. Datum- en tijdgegevens worden automatisch gekozen uit de gebeurtenissen BlueJeans.
* **Synchronisatie van geautomatiseerde gebruikersvoltooiing:** Via een geautomatiseerd proces voor het synchroniseren van gebruikersvoltooi kan de beheerder van de leermanager automatisch voltooiingsrecords voor BlueJeans-gebeurtenissen ophalen.

Deze nieuwe connector vereist een afzonderlijke set referenties om de connector te configureren.

Zie voor meer informatie [***BlueJeans Event-connector***](../integration-admin/feature-summary/connectors.md#bj-events).

+++

+++Update 58- December 2020-versie van Learning Manager

## Update 58 - december 2020 van de Learning Manager-versie

Releasedatum: 5 december 2020.

### Nieuwe en gewijzigde functies {#Whatsnewandchanged-2}

Deze release is gericht op het volgende:

* Nieuwe startpagina-ervaring van student
* Responsieve lay-out voor mobiel web voor studentrol
* Op AI gebaseerde aanbeveling voor studenten
* E-mails met wekelijkse samenvatting
* Checklist
* Integratie met Marketo
* Aangepast domein
* Importeren van quizscores uit Adobe Connect
* Diepe koppeling naar catalogus voor studenten
* Verbeteringen in linkedIn Learning
* ...en nog veel meer

Zie voor meer informatie  [***Nieuwe functies in de december 2020-versie van Adobe Learning Manager***](../whats-new.md).

### Niet-ondersteunde functies in mobiele boeiende ervaring {#unsupportedfeaturesinmobileimmersiveexperience}

De volgende functies worden niet ondersteund:

* Sociale app: een student wordt omgeleid naar een klassieke ervaring als hij/zij op de sociale widget op de startpagina klikt
* Profielinstellingen/Profiel bewerken
* Badge/Vaardigheden weergeven
* Leaderboard: Een student wordt omgeleid naar de klassieke ervaring als hij op de Leaderboard-widget op de startpagina klikt
* Taakhulpen downloaden.
* Filteropties in Zoeken.

### bugs gecorrigeerd in deze update {#bug-fixes-1}

* U kunt een inhoudsmap niet verwijderen als de inhoudsmap verwijderde inhoud bevat.
* Met een leerplan kunnen beheerders een cursus instellen met een automatische instantie. Voor een cursus met de module Activiteit indienen werden de gegevens van de docent niet correct eerder ingesteld. Leermanager wijst de docent nu automatisch van de standaardinstantie toe aan deze automatische instantie.
* Een aangepaste badge met een cataloguslabel met een spatie staat het downloaden van de PDF niet toe zoals verwacht.
* Een rapport dat u van het dashboard hebt gedownload, verschilt van de abonnements-e-mail die u voor het dashboardrapport hebt ontvangen.
* Een Studenttranscript heeft geen bijgewerkte gegevens voor een herhaalde certificering.
* Als u de cursus hebt verlaten en de cursus hebt gestart, wordt het aantal pogingen niet zoals verwacht weergegeven. Er verschijnt soms ook een leeg scherm wanneer u meerdere keren een cursus probeert te volgen.
* Er is fout 5xx nadat u een module uploadt.
* Niet alle studenten zien een persoonlijk sociaal board.

### Bekende problemen in deze update {#known-issues-1}

Nadat u een cursus of certificering hebt voltooid, ziet u de pop-up met feedback niet meteen. Dit probleem doet zich alleen voor wanneer u de cursus volgt in de meeslepende gebruikersinterface. Als u de cursus volgt in de klassieke gebruikersinterface, ziet u het pop-upvenster met feedback zoals verwacht.

+++

+++Update 57

## Update 57

Releasedatum: 23 september 2020

**Inhoudsbibliotheek**

* Als u een inhoud uit de inhoudsbibliotheek archiveert, wordt de inhoud in de **Gepubliceerd** tabblad. Wanneer u de pagina vernieuwt, wordt de gearchiveerde inhoud niet meer weergegeven.
* Wanneer u een inhoudsmap maakt, **Naam** het veld is niet als verplicht gemarkeerd , hetgeen in feite een verplicht veld is .

**Klantenverzoek**

* Neem de volgende velden op het dashboard, Abonnementsrapport, op om te zien voor welke cursussen elke student is ingeschreven en of hij of zij de cursussen heeft voltooid:

   * UUID
   * E-mailadres

**Studenttranscript**

* Het genereren van een Studenttranscript in de Indonesische landinstelling veroorzaakte fouten.

**Zoeken**

* U kunt niet zoeken naar een specifieke cursus. Dit is opgelost.

+++

+++Update 56 - Mobiele app

Releasedatum: 25 augustus 2020

### Cursussen volgen vanuit LinkedIn Learning {#takecoursesfromlinkedinlearning}

Learning Manager ondersteunt al LinkedIn Learning-cursussen binnen het leerplatform. Studenten kunnen nu dergelijke LinkedIn Learning-cursussen volgen in de mobiele app van Learning Manager. Zoek in de apparaatapp naar een cursus en start de cursus.

Zie Cursussen volgen op [***LinkedIn Learning***](../learners/feature-summary/ipad-android-tablet-users.md#linkedin).

### Pushmelding voor beheerdersinschrijvingen {#pushnotificationforadminenrollments}

Wanneer de beheerder studenten inschrijft voor trainingen, krijgen de studenten meldingen over de inschrijvingen.

Pushmelding wordt nu ook ondersteund voor aankondigingen.

### Verplicht L1-feedback {#mandatoryl1feedback}

In de nieuwste release van augustus 2020 stelt Learning Manager beheerders in staat L1-feedback zodanig te configureren dat alle vragen verplicht worden gesteld. Hetzelfde wordt nu ondersteund vanuit het perspectief van de student in de mobiele app.

### Verbeteringen in gebruikersinterface {#userinterfaceenhancements}

**Voettekstkoppelingen**

De beheerder kan meerdere voettekstkoppelingen instellen in de beheerderweergave op het web. Studenten hebben nu toegang tot deze koppelingen door op het hamburgerpictogram en het Help-pictogram te tikken.

Standaard zijn er twee koppelingen en de beheerder kan nog drie koppelingen toevoegen (via de beheerdersweergave op het web) die in de app worden weergegeven.

**Kaartweergave voor leerobjecten**

Standaard worden de trainingen in de secties Mijn leerervaring en Catalogus van de app weergegeven als kaarten in plaats van als lijsten. Dit is een wijziging voor studenten zoals eerder was de standaardweergave &quot;Lijstweergave&quot;.

Studenten kunnen echter wel schakelen tussen de lijstweergave en de kaartweergave.

+++

+++Update 55- augustus 2020-versie van Learning Manager

Releasedatum: 23 augustus 2020

### Nieuwe en gewijzigde functies {#Whatsnewandchanged-3}

Deze release is gericht op het volgende:

* Verbeteringen voor rapportage
* Persoonlijke inhoudsmappen
* Aangepaste FTP
* Ondersteuning voor bijschriften voor video&#39;s
* Verbeteringen voor Power BI
* Verbeterde feedback
* Nieuwe en gewijzigde API&#39;s
* Wijzigingen in het beleid voor gegevensbehoud
* ...en nog veel meer

Zie voor meer informatie  [***Nieuwe functies in de augustus 2020-versie van Adobe Learning Manager***](../whats-new.md).

### Opmerkingen over deze release {#notes}

* Het genereren van een studenttranscript (~1 GB) duurt minder dan 15 minuten.
* In eerdere versies van Learning Manager gaven de quizscore en de hoogste quizscore in het studenttranscript de score en de maximale score op in de 25/100-indeling. Voor een betere leesbaarheid en analyse wordt de quizscore nu ook geëxporteerd als aparte kolommen - **Quiz_score, Quiz_score_max, Highest_Quiz_score en Highest_Quiz_score_max**. Hiermee kunnen beheerders snelle berekeningen en analyses maken.

### bugs gecorrigeerd in deze update {#bug-fixes-2}

**Connector**

* Een student kan niet gelijktijdig aan twee verschillende vergaderingen deelnemen, die door twee verschillende auteurs worden gemaakt.
* Als u op de optie Verbindingen beheren klikt vanaf de Adobe Connect-kaart, gaat u naar de FTP-verbindingspagina.
* Een geplande FTP-synchronisatie wordt afgesloten met een uitzondering.
* Er zijn wachtwoordgerelateerde problemen wanneer u verbinding maakt met Exavault.

**Cursus**

* U kunt een VC-module maken zonder een conferentiesysteem te selecteren. Als neveneffect genereert het maken van een cursus een fout 500.
* Een student kan geen bronnen downloaden, ook al is de student voor een gedupliceerde cursus ingeschreven.
* Wanneer een beheerder of auteur een voorbeeld van een cursus als student bekijkt, kan deze geen bronnen downloaden, tenzij hij/zij voor de cursus is ingeschreven.

**Apparaatapp**

* In specifieke inschrijvingsgevallen worden in het Donut-diagram onder Mijn In afwachting van leerervaring verschillende waarden van de Learner-app weergegeven, van de browser tot de Mobile-app.

**Certificering**

* De status van het rapportfilter werkt niet zoals verwacht bij het downloaden van een dashboardrapport voor certificering.

**Zoeken**

* Als u op de pagina Studentencatalogus probeert een cursus te doorzoeken op basis van de bijbehorende notitie, verschijnen er geen zoekresultaten.

**SCORM**

* Voor bepaalde inhoud wordt in de SCORM-speler een leeg scherm weergegeven.
* Een inhoud Storyline wordt geïdentificeerd als inhoud van de Captivate, als het gepubliceerde project Storyline een Webvoorwerp bevat dat aan de gepubliceerde output van de Captivate richt.
* SCORM-inhoud kan niet worden gestart vanwege een onjuiste URL.

**Aangepaste rol**

* Voor bepaalde scenario&#39;s kan een aangepaste beheerder de volledige lijst met leerobjecten niet zien.
* Een aangepaste beheerder kan niet zoeken naar een leerprogramma of certificering in de dashboardrapporten.
* Een aangepaste beheerder kan niet zoeken naar een manager op een dashboard.
* Studenttranscripten die zijn gegenereerd door een aangepaste beheerder, bevatten geen gegevens van verwijderde gebruikers.
* Een aangepaste auteur of aangepaste beheerder kan een leerprogramma, een cursus of een certificering niet dupliceren.

**Rapporten**

* In de kolom Type in een Studenttranscript wordt de waarde als cursus weergegeven voor de cursussen die deel uitmaken van een certificering als de student niet is ingeschreven voor de certificering.

**Vaardigheden**

* Wanneer u een vaardigheid voor een cursus toevoegt, zijn er enkele problemen bij het zoeken naar een vaardigheid.

**Gamification**

* Als veel gebruikers vertrouwelijk worden gemaakt, gedraagt de browser zich onverwacht als ze op het vertrouwelijke tabblad Studenten in Edge and Internet Example klikken.
* Wanneer de frequentie van een criterium wordt gewijzigd, worden de punten die met een oudere frequentie zijn berekend, aan de huidige berekening toegevoegd.

**Beheerder**

* Studenten kunnen niet als aanwezig worden gemarkeerd als de cursusinstantie die aan een leerprogramma is toegewezen, wordt gewijzigd.

**E-mailsjablonen**

* Voor Leerprogramma&#39;s en Certificeringen ontbreekt de schakelknop in de e-mailsjabloon.

**Inhoudsbibliotheek**

* SCORM-inhoud wordt niet zoals verwacht gestart vanwege een onjuiste URL.

**Studenttranscripten**

* .Als u bij het genereren van Studenttranscripten een verwijderde student toevoegt in het invoervak Studenten selecteren en vervolgens de optie Gegevens van verwijderde studenten opnemen in het venster Geavanceerd inschakelt, gedraagt de pagina zich onverwacht.

**Zoeken**

* U kunt niet zoeken naar een cursus aan de hand van de bijbehorende notities.

**Excel-rapporten**

* Als een controlerapport van een gebruiker meer dan een uur duurt om te downloaden vanwege grote gegevens of trage verwerking, worden de verbindingstijden niet langer weergegeven en wordt het rapport nooit gedownload.
* In een Studenttranscript wordt de kolom Type weergegeven als &#39;Cursus&#39; in plaats van als &#39;Certificering&#39; voor de cursussen die deel uitmaken van de certificering, als de student niet is ingeschreven voor de certificering.

**Learner-app**

* Een student kan op ongeordende wijze een geordende cursus volgen door via een uitschrijvingsbericht of een uitschrijvingsbericht cursussen te openen.
* Een student ontvangt geen herinneringsmails voor de sessie zoals verwacht.
* Een cursus wordt niet zoals verwacht gestart als een bepaalde module ontbreekt.

**Aankondigingen**

* Als een aankondiging de tag bevat <a>, wordt de aankondiging niet zoals verwacht tot stand gebracht.

**Account**

* In sommige gevallen worden accounts gedeactiveerd, ook al heeft een account een geldige inkooporder.

**API**

* Als u op Verbindingen beheren klikt vanaf de Adobe Connect-kaart, wordt u omgeleid naar de pagina FTP-verbinding.
* In sommige gevallen ontvangt de Connect-beheerder onjuiste waarschuwingen.
* LinkedIn Learning-migratie veroorzaakt een aantal fouten.

### Bekende problemen in deze update {#known-issues-2}

**Dashboard-rapporten**

* Wanneer een leerprogramma voor certificering wordt verwijderd, worden in het rapport Actieve trainingen de cursussen weergegeven die zich in het leerprogramma of de certificering bevinden, ook al waren er geen inschrijvingen voor het leerprogramma of de certificering.

+++

+++Update 54 - Mobiele app

## Update 54 - Mobiele app

Releasedatum: 16 april 2020.

Voor de nieuwste functies, updates en een betere ervaring raden we u aan de apparaatapp bij te werken naar de nieuwste versie. De update is **verplicht**.

### Nieuwe en verbeterde functies {#newandenhancedfeatures}

Een beheerder kan belangrijke informatie doorgeven aan alle gebruikers van de app. Aankondigingen kunnen van het type video of afbeelding of een eenvoudig tekstbericht zijn. Met deze apparaatapp-release ondersteunen we nu aankondigingen in de apparaat-app. Zodra de app wordt gestart, verschijnt er een nieuwe aankondiging, zodat studenten geen belangrijke communicatie van de beheerders missen. Studenten kunnen het document direct lezen of later lezen door op de pagina **Aankondigingen** tabblad.

Als er een aankondiging of meerdere aankondigingen zijn, kunt u de aankondigingen in het deelvenster **Aankondigingen** sectie.

Tik op **Aankondigingen**. De meest recente aankondiging wordt op het scherm weergegeven.

Tik op **Naar links vegen voor volgende**.

### Aankondigingen {#announcements}

![](assets/read-later.png)

Als u de aankondiging op dat moment niet wilt lezen, kunt u er altijd voor kiezen om de aankondiging later te lezen. Tikken **Later lezen** de aankondiging en de aankondiging gaan terug naar de ongelezen staat .

### bugs gecorrigeerd in deze update {#bugsfixedinthisupdate}

* In iOS wordt het afspelen van een podcast gestopt wanneer het scherm is vergrendeld. Het probleem is opgelost en de audio wordt afgespeeld, zelfs als het scherm is vergrendeld.
* Als u een cursus volgt in de apparaatapp, kan de resulterende dia soms leeg worden weergegeven. Dit probleem is opgelost in deze update.

+++

+++Update 53 - April 2020-versie van Learning Manager

Releasedatum: 4 april 2020.

De april 2020-versie van Learning Manager was gericht op het volgende:

* [Prestatieverbeteringen](../whats-new.md#performance)
* [Lesruimtetraining](../whats-new.md#classroom)
* [Workflows beheren](../whats-new.md#manager)
* [Sociaal leren](../whats-new.md#social)
* [Rapportage](../whats-new.md#reporting)
* [Leerervaring](../whats-new.md#learner)
* [Wijzigingen op API-niveau](../whats-new.md#api)

Zie voor meer informatie [***Nieuwe functies in de april 2020-versie van Learning Manager***](../whats-new.md).

+++

+++Update 52 - Mobiele app

## Update 52 - Mobiele app

Releasedatum: 20 december 2019

### Nieuwe en verbeterde functies {#Newandenhancedfeatures-1}

#### Bedrijfsmerklogo {#companybrandinglogo}

De app heeft nu de mogelijkheid om de merknaam, het merklogo of beide in de apparaatapp weer te geven, afhankelijk van de instellingen die door de beheerder zijn ingesteld.

#### Diepe koppelingen {#deeplinks}

Leermanager start nu de apparaatapp zodra u op een link/URL klikt die door een leermanager wordt ondersteund. Als de app niet op het apparaat is geïnstalleerd, wordt de URL in de browser geopend.

Hier volgen enkele gebruiksscenario&#39;s die in deze update worden ondersteund.

* Klik op een trainings-URL die in een e-mail is ontvangen.
* Standaard training-URL&#39;s die worden weergegeven in de e-mailsjablonen.
* Account-URL die wordt weergegeven in de e-mailsjablonen.
* Mijn leerervaring en Catalogus go-URL&#39;s.

Bovendien elke URL met een domein *learningmanager.adobe.com* wordt geopend in de apparaatapp.

#### Elementen uploaden in extern certificaat als bewijs van voltooiing {#uploadassetsinexternalcertificateasproofofcompletion}

In deze update kan een student elementen uploaden als bewijs van voltooiing voor een extern certificaat.

Een student kan een extern certificaat openen en elementen uploaden, zoals PDF-, tekst- of afbeeldingsbestanden.

Zie voor meer informatie  [***Elementen uploaden in extern certificaat***](../learners/feature-summary/ipad-android-tablet-users.md#externalcert).****

### Opgeloste problemen in deze release {#issuesfixedinthisrelease}

* Een gebruiker kan zich niet aanmelden bij de apparaatapp als de e-mail speciale tekens bevat.
* Tijdens het schuiven flikkert het pictogram Leerobject wanneer u zich in een lijstweergave bevindt.
* U kunt nu alle pushmeldingen bekijken zonder op de pijl-omlaag te tikken en de berichten een voor een te bekijken.
* Nadat u op een melding hebt geklikt voor een bericht dat in beheer is geaccepteerd of afgewezen, wordt er een lege pagina in de app geopend. In deze update wordt de boardpagina geopend.

+++

+++Update 51

In deze update kunt u ook de bannerafbeelding voor een leerobject wijzigen.

U kunt de banner ook aanpassen op een pagina voor Sociaal leren.

## Update 51

Releasedatum: 17 december 2019

### Nieuwe en verbeterde functies {#Newandenhancedfeatures-2}

### Leerplannen met configureerbare rollen {#learningplansscopedbyconfigurableroles}

U kunt aangepaste rollen voor leerplannen maken waarmee gebruikers en leerobjecten bereikbaar zijn. Met andere woorden, leerplannen kunnen worden gemaakt met een beperkt bereik dat is afgeleid van het rolbereik van een aangepaste beheerder.

Een beheerder kan nu het bereik definiëren of beperken terwijl toegang tot leerplanmanagement wordt verleend.

Zie voor meer informatie [***Leerplannen met configureerbare rollen***](../administrators/feature-summary/custom-role.md#scopeconfigure).

### Actieve velden in rapporten beperken {#restrictactivefieldsinreports}

Voor actieve velden hebben we twee nieuwe opties toegevoegd: **Te rapporteren** en **Exportable**.

Voor CSV-velden en handmatig toegevoegde velden als een actief veld is gemarkeerd als **Te rapporteren** wordt het actieve veld doorzoekbaar in een filter in een dashboardrapport.

Zie voor meer informatie  [***Actieve velden in rapporten beperken***](../administrators/feature-summary/add-users-user-groups.md#restrictactivefields)***.**

### Beschrijving van inhoudsmodule weergeven {#viewdescriptionofcontentmodule}

Als auteur kunt u de beschrijving van de modules zien terwijl u de module aan een cursus toevoegt.

Voeg tijdens het maken van een module de beschrijving toe. Ga voor meer informatie over het maken van een cursus naar [***Een cursus maken***](../authors/feature-summary/courses.md).

### Cursus- en sessienamen weergeven {#displaycourseandsessionnames}

Als docent kunt u sessie- en cursusnamen zien in de weergave Aanwezigheid. U kunt bijhouden welke sessies worden gewijzigd.

### Aankondiging voor studenten {#announcementforlearners}

Studenten kunnen nu een aankondiging in volledige weergave bekijken in plaats van een lijstweergave. Dit gebeurt wanneer de student één ongelezen aankondiging heeft. Dit verbetert de ervaring van studenten bij het bekijken van de aankondiging.

Met Adobe Learning Manager kunt u uw account nu aanpassen om uw gebruikers een rijkere ervaring te bieden. Hier volgt een lijst met elementen die kunnen worden aangepast. Contact [Ondersteuning voor Learning Manager](mailto:learningmanagersupport@adobe.com)om deze wijzigingen aan te brengen.

* Trainingskaartkleuren.
* Voortgangspictogram
* Afbeelding muisaanwijzer
* Lettertype

Zie voor meer informatie [***Uw account aanpassen***](../administrators/feature-summary/themes.md#customize).

### Bannerafbeeldingen uploaden {#uploadbannerimages}

In deze update kunt u ook de bannerafbeelding voor een leerobject wijzigen.

U kunt de banner ook aanpassen op een pagina voor Sociaal leren.

### API-ondersteuning {#apisupport}

Deze update van Learning Manager bevat een API voor de volgende bewerkingen:

**Badge PDF downloaden**

Deze update bevat de API voor studenten zodat PDF van een badge kan worden gedownload.

**Studenttranscript downloaden**

Deze update bevat de API van de student om het downloaden van studenttranscripten toe te staan.

**Quizrapport downloaden**

Deze update bevat de Admin API om het downloaden van quizrapporten toe te staan.

**Gegroepeerde gamification**

De API voor studenten maakt het nu mogelijk alle studenten en gamificationpunten op te halen in het bereik van de student. Dit helpt bij het bouwen van een gamificationleaderboard.

**API:** `GET /users`

**Verzoek:** `GET\\ users?page[offset]=0&page[limit]=10&sort=id&filter=gamification`

**Reactie:** *Het antwoord bevat de gesorteerde gebruikers in volgorde van gamificationpunten.*

**Niet storen**

Momenteel kunnen alleen beheerders gebruikers toevoegen aan de lijst Niet storen via de gebruikersinterface. Na deze release kan een student deze machtigingen voor zichzelf instellen via de API, mits deze API door de beheerder is ingeschakeld. Voor het inschakelen van deze API voor een account is een back-endinstelling vereist. Met deze API kan de student de machtigingen hieronder bewerken die betrekking hebben op e-mails.

* Directe e-mails aan student
* Escalatiemails naar studenten Managers
* Informatie over directe rapporten
* Informatie over rapporten op het niveau overslaan

Raadpleeg de volgende bronnen voor meer informatie over API&#39;s van Learning Manager:

* [***API-referentie***](<https://learningmanager.adobe.com/docs/Learning> Managerapi/v2/)
* [***Handleiding voor API-ontwikkelaars***](<https://helpx.adobe.com/captivate-Learning> Manager/integration-admin/feature-summary/developer-manual.html)

### Opgeloste problemen in deze release {#Issuesfixedinthisrelease-1}

* Alleen gebruikers die tot een specifieke gebruikersgroep behoren, moeten aankondigingen ontvangen die voor hen zijn bedoeld. Andere gebruikers mogen de aankondigingen niet ontvangen.
* De speler geeft een spinner weer voordat de inhoud wordt weergegeven.
* Metagegevens van gebruikers in rapporten veroorzaken een Null-aanwijzeruitzondering.
* Na het toevoegen van een docent voor een standaardinstantie voor Connect VC-cursus, verschijnt het bericht: *&quot;Geen sessie voor deze module&quot;*, wordt weergegeven op de pagina Cursusinstantie in de Admin-app.

* Het exporteren van een studenttranscript leidt tot onverwacht gedrag tijdens een FTP-overdracht.
* De naam van een auteur wordt onjuist weergegeven op cursussen in een leerprogramma.
* De wijzigingen in de productterminologie van taakhulpen komen niet overeen met de verwachting.
* De naam van een module wordt afgekapt als de naam lang is en wordt weergegeven in de staande mobiele modus.
* Kan geen instantie maken voor een oudere Connect-cursus nadat de standaardinstantie is bijgewerkt met een oudere Connect-implementatie.
* Een docent ontvangt een uitnodiging voor een kandidaat, zelfs voordat de cursus wordt gepubliceerd.

+++

+++Update 50

## Update 50

Releasedatum: 24 okt. 2019

### Nieuwe en verbeterde functies {#Newandenhancedfeatures-3}

#### Een aangepaste rol maken met meerdere catalogusbereiken {#createcustomrolewithmultiplecatalogscopes}

Als beheerder kunt u een aangepaste rol beperken op basis van catalogi en gebruikersgroepen. Alle gebruikers die tot dergelijke rollen behoren, kunnen alleen leerobjecten van de catalogus in hun bereik zien. Deze gebruikers kunnen alleen handelingen uitvoeren die zijn gedefinieerd in het bereik van hun gebruikersgroepen.

Tot nu toe kon in Learning Manager voor één gebruikersgroep met volledige machtigingen een aangepaste rol worden ingesteld voor meerdere catalogi.

In deze update van Leermanager kunt u een aangepaste rol voor meerdere catalogi maken, waarbij aan elke catalogus verschillende machtigingen worden toegekend. Zie voor meer informatie [***Het bereik van aangepaste rollen voor meerdere catalogi***](../administrators/feature-summary/custom-role.md#multi-scope).

### Verbeteringen voor zoeken {#enhancementstosearch}

**Leerplan**

Op de pagina Leerplannen voor beheerders en auteurs is er nu een zoekbalk die u kunt gebruiken om in elk leerplan te zoeken.

![](assets/search-for-as-learningplan.png)

**Beheerders- en auteur-apps**

In deze update van Learning Manager kunt u als beheerder of auteur, naast het uitvoeren van een automatisch aangevulde zoekopdracht, een gratis zoekopdracht uitvoeren om een leerobject te zoeken.

### Zoekfilter blijft behouden {#searchfilterispreserved}

Dit geldt alleen voor een studentenprofiel.

Op de **Catalogus** en **Mijn leerervaring** pagina&#39;s kan een student een filter toepassen op het linkerdeelvenster, bijvoorbeeld **Cursussen** of **Leerprogramma&#39;s** en klikt u op een cursus- of catalogusitem.

![](assets/choose-learning-objects.png)

Wanneer de student terugkeert naar de **Catalogus** of **Mijn leerervaring** pagina&#39;s met de knop Vorige van de browser, blijft het filter behouden. Het filter dat een student eerder heeft toegepast, wordt niet meer opnieuw ingesteld.

### Zichtbaarheid van zoekfilters bepalen {#controlvisibilityofsearchfilters}

In eerdere versies van Learning Manager hebben beheerders geen controle over de zichtbaarheidsopties van een catalogusfilter, zodat studenten de vaardigheden en tags niet zien. In deze versie van Leermanager kunnen beheerders filteren op typen, vaardigheden en tags van een catalogus.

In het dialoogvenster **Instellingen** pagina, voor de categorie Filterdeelvensters weergeven wanneer u klikt op **[!UICONTROL Bewerken]** kunt u de volgende opties zien. De opties bepalen de filterdeelvensters die zichtbaar zijn voor studenten, zodat de studenten de zoekresultaten kunnen verfijnen.

Zie voor meer informatie [***Filterdeelvensters weergeven***](../administrators/feature-summary/settings.md#filter-panels).

### QR-code downloaden uit beheerdersapp {#downloadqrcodefromadministratorapp}

In eerdere updates van Leermanager ondervond een aangepaste beheerder problemen tijdens het downloaden van een QR-code. In deze update heeft een aangepaste beheerder toegang tot **Alle studenten** en machtiging voor **Cursusinschrijving** kan de QR-code downloaden.

QR-code is nog steeds niet beschikbaar voor gebruikers met een aangepaste rol voor het geval ze machtigingen hebben voor een beperkt gebruikersbereik.

### Opmerkingen toevoegen tijdens het inschrijven van studenten {#addcommentswhileenrollinglearners}

Als beheerder of manager kunt u opmerkingen toevoegen terwijl u studenten voor een cursus inschrijft. U kunt aanvullende informatie opgeven over de cohort van gebruikers die zich inschrijven. Deze gegevens worden geëxporteerd in cursusrapporten.

Zie voor meer informatie [***Opmerkingen toevoegen tijdens het inschrijven van studenten***](../administrators/feature-summary/courses.md#enroll-comments).

### Ondersteuning voor Adobe Connect permanente vergaderruimte {#supportforadobeconnectpersistentmeetingroom}

In Adobe Connect gebruiken klanten bestaande vergaderruimten die ze al in Connect hebben gemaakt. Alle vergaderruimten in Connect zijn blijvend en de sjablonen voor de vergaderruimte worden zorgvuldig ingesteld om een uniforme ervaring te bieden voor elke permanente ruimte.

In deze versie van Learning Manager is de integratie met Adobe Connect nu verbeterd en biedt deze nu ook ondersteuning voor permanente ruimtes. Dit betekent dat u nu een virtuele-lesruimtesessie kunt maken met een van de ruimten die al in Adobe Connect zijn gemaakt.

Met Learning Manager kunnen studenten nu ook de verbindingsruimte voor hun virtuele sessie betreden met behulp van SSO-verificatie.

Zie voor meer informatie [***Ondersteuning voor permanente ruimte in Adobe Connect***](../integration-admin/feature-summary/connectors.md#persistent).

### Waarschuwing voordat aanwezigheid wordt gemarkeerd als de sessieduur nul is {#warningbeforemarkingattendanceifthesessiondurationiszero}

Een auteur of een beheerder kan een sessie maken met een duur van 0. Het is mogelijk wanneer:

* begindatum en/of einddatum leeg zijn.
* begintijd en/of eindtijd leeg zijn.

In deze update wordt **waarschuwingsbericht waarin staat dat de duur van een sessie nul is**, wordt weergegeven aan de beheerder, manager of docent.

### Waarschuwing als een klassikale module is gemaakt zonder sessiegegevens toe te voegen {#warningifaclassroommoduleiscreatedwithoutaddingsessiondata}

Als een auteur een cursus maakt door een klassikale of VC-module toe te voegen, kan de auteur ervoor kiezen:

* Geen begin-/einddatum en begin-/eindtijd toevoegen.
* Voeg een datum toe, maar geen begin-/eindtijd.
* Voeg een datum en begintijd toe.

In al het bovenstaande worden, wanneer een beheerder, manager of docent aanwezigheid of voltooiing markeert, de waarden van de begindatum en einddatum van de sessie gelijk, wat betekent dat in een Studenttranscript de waarde Bestede leertijd als nul wordt weergegeven.

In deze update wordt **waarschuwingsbericht waarin staat dat de sessiegegevens onvolledig zijn**, wordt getoond aan de auteur.

### Opgeloste problemen in deze release {#Issuesfixedinthisrelease-2}

**Learner-app**

* Een student kan een cursus niet in een leerprogramma bekijken als de cursus door een externe auteur is gemaakt.
* Als een beheerder een bericht aan een externe board toevoegt, gaat het verzoek tot beheer naar een interne SME, die aan die vaardigheid is toegewezen.
* Een student kan de knop Start of Doorgaan niet weergeven na het inschrijven voor LinkedIn-cursussen.

**E-mail**

* Als een DND-lijst een groot aantal gebruikers bevat, wordt **Instellingen** pagina wordt heel langzaam geladen. In deze update wordt paginering toegevoegd aan een lijst met DND&#39;s voor e-mail.
* Een docent ontvangt updates/mails voor sessies waar hij/zij geen deel van uitmaakt. In deze update is deze fout opgelost.

**Vaardigheden**

* In een Studenttranscript wordt het type waarde van een vaardigheid verkeerd weergegeven als tekst.

**Mobiele app**

* In de mobiele app kon een student een leerplan-instantie bekijken en inschrijven, wat niet het beoogde gedrag was. In deze update is deze fout opgelost.

**Aangepaste rollen**

* Als aangepaste beheerder kunt u geen manager zoeken in een dashboardrapport.

**Meerdere pogingen**

* In sommige scenario&#39;s worden een aantal cursusmodules niet aan studenten weergegeven.

**Externe inschrijving**

* U kunt het externe profiel van een gebruiker niet wijzigen als er plaatsen zijn ingevuld voor de bovenste profielen.

### Bekende problemen in deze release {#knownissuesinthisrelease}

* Als u in de onderstaande browsers met de muis over het linkerdeelvenster beweegt, wordt de tekst na een kleine vertraging weergegeven.

   * Edge 42.17134.1.0
   * Edge 44.1763.1.0
   * Internet Explorer 11.1006
   * Internet Explorer 11.615

* Een student mag een Connect-vergaderruimte voor en na de sessie betreden.

+++

+++Update 49

## Update 49

Releasedatum: 26 augustus 2019

### Nieuwe en verbeterde functies {#Newandenhancedfeatures-4}

**Prestatieverbeteringen**

* Gebruikers in het systeem importeren is sneller dan in eerdere versies. Er is een aanzienlijke verbetering bij het importeren van grote gebruikersgegevens.
* Voor managers en beheerders zijn de opties in de vervolgkeuzelijst Rapportconfiguratie gewijzigd om de gegevens op aanvraag te laden.
* API-prestaties zijn verbeterd. Veel API&#39;s zouden nu een verbeterde reactietijd moeten hebben.
* De tijd die nodig is om het studenttranscript te genereren is verbeterd.
* Er is geen vertraging op de pagina&#39;s waarop interne en externe studenten worden weergegeven, vooral niet als er een groot aantal gebruikers is.

**Speciale gebruikersrechten**

Een beheerder kan een gebruikersgroep speciale bevoegdheden geven op basis waarvan leden van de groep aan alle boards kunnen deelnemen. Eventuele beperkingen die zijn ingesteld in de sectie Omvanginstellingen worden omzeild door de speciale gebruikersgroep. Zie voor meer informatie [***Speciale gebruikersrechten***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#privilege).

**Wijzigingen in de gebruikersinterface**

* In het dialoogvenster **Rapport toevoegen** de **Tijdspanne** en **Filters** kiezers worden weergegeven als afzonderlijke secties, die standaard zijn samengevouwen. Zie voor meer informatie [***Rapporten maken***](../administrators/feature-summary/reports.md#report).

* In het dialoogvenster **Rapport toevoegen** voor een gebruikersgroep, kunt u automatisch automatisch zoeken om een of meer gebruikersgroepen te kiezen. Zie voor meer informatie [***Gebruikersgroeprapporten***](../administrators/feature-summary/reports.md#user-group-reporting).

**Wijzigingen in waarden in tijdkolommen**

In de Studenttranscripten worden in de tijdkolommen de minuten afgerond naar de dichtstbijzijnde minuut en is de waarde van de seconde 00. Zie voor meer informatie [***Tijdkolommen***](../administrators/feature-summary/learner-transcripts.md#datetime).

### Opgeloste problemen in deze release {#Issuesfixedinthisrelease-3}

**Studentendashboard**

* De status wordt weergegeven in een studentenagenda **Ingeschreven sessie** zelfs als een manager de inschrijving nog moest goedkeuren. Nu de juiste status **In behandeling** wordt weergegeven aan de student totdat de manager de inschrijving goedkeurt.

* In een bepaald geval werd voor een sessie de status weergegeven in de studentenagenda **Ingeschreven** ook al heeft de student een cursus voltooid.

**Managerdashboard**

* Managers konden nalevingstrainingen van hun team niet volgen als de teamleden via leerplannen waren ingeschreven.

**Zoeken**

* In de docentenweergave kon u niet naar een student zoeken.

**Gebruikersinterface**

* Voor een account waarop taxonomiewijzigingen zijn toegepast, werden de wijzigingen niet zoals verwacht weergegeven in meldingen.

### Bekende problemen in deze release {#Knownissuesinthisrelease-1}

* Met de zoekbalk kunt u niet zoeken naar verwijderde gebruikers in de lijst Externe gebruikers. Als tussenoplossing kunt u omlaag schuiven om de lijst met alle gebruikers weer te geven en de gewenste gebruiker handmatig te vinden.
* Als een speciale gebruiker op een externe board plaatst, wordt het verzoek om beheer ontvangen door SME&#39;s in zijn/haar bereik.

+++

+++Update 48

## Update 48

Releasedatum: 2 augustus 2019

### Nieuwe en verbeterde functies {#Newandenhancedfeatures-5}

**Scheiding van het bereik in Sociaal leren voor interne en externe gebruikers** Een beheerder kan afzonderlijke bereiken definiëren voor interne en externe studenten. Er zijn twee nieuwe secties voor interne en externe gebruikers. In beide secties kunt u het bereik voor de studentengroepen definiëren. Voor interne gebruikers kunt u de waarden van het gebruikerskenmerk definiëren. Voor externe gebruikers kunt u het externe profiel definiëren waarin studenten dezelfde sociale ruimte kunnen delen. Zie voor meer informatie [***Bereik-instellingen***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#scopesettings).  **Sociaal-Beperken van het maken van sociale boards** Om het maken van boards door alle studenten te beperken en de boards effectief te modereren, kan een beheerder een bepaalde groep gebruikers machtigingen verlenen om boards te maken. De beheerder kan het maken van een board beperken tot een geselecteerde groep en niet tot elke student die deelneemt aan Sociaal leren. Zie voor meer informatie [***Machtigingen voor het maken van boards***](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#permission).  **Alleen lege actieve velden voor studenten weergeven** Een beheerder kan ervoor kiezen om de actieve velden weer te geven of te verbergen nadat de waarden zijn ingevuld. Zie voor meer informatie [***Gebruikersweergave***](../administrators/feature-summary/add-users-user-groups.md#activefields).  **Interne gebruikers worden na een opgegeven inactiviteitsduur verwijderd** Een beheerder kan de duur (in dagen) instellen waarbinnen een interne student wordt verwijderd als de student tijdens de opgegeven periode inactief blijft. Zie *** voor meer informatie[Gebruikers automatisch verwijderen](../administrators/feature-summary/settings.md#autodelete)***.  **Koppelingen in de voettekst aanpassen** Een beheerder kan koppelingen toevoegen aan en aanpassen in de voettekst. De koppelingen kunnen ook worden aangepast voor verschillende landinstellingen. De bestaande methode voor het toevoegen van de koppeling Contact opnemen met beheerder aan de voettekst is ook beschikbaar in het dialoogvenster **Voettekstkoppelingen** sectie. Zie voor meer informatie [***Voettekstkoppelingen aanpassen***](../administrators/feature-summary/settings.md#footer).

### Bekende problemen in deze release {#Knownissuesinthisrelease-2}

* Aangepaste voettekstkoppelingen worden niet weergegeven voor integratiebeheerders.

+++

+++Update 47 - Mobiele app

## Update 47 - Mobiele app

Releasedatum: 24 juli 2019

Android-gebruikers:

Deze update ondersteunt ook de noodzakelijke wijzigingen om te voldoen aan de herziene aanbevelingen van Google voor het implementeren van pushmeldingen. U ontvangt daarom niet meer **meldingen** als u versie 2.7.4 of ouder gebruikt.

We raden u aan een upgrade naar versie 2.8 uit te voeren om meldingen te ontvangen.

### Nieuwe en verbeterde functies {#Newandenhancedfeatures-6}

**Sociaal leren**

Deel uw expertise met collega&#39;s in de vorm van door gebruikers gegenereerde inhoud die op thematische discussieboards wordt geplaatst. Andere studenten die geïnteresseerd zijn in vergelijkbare vaardigheden kunnen deze boards volgen om te leren en zelfs bij te dragen aan het onderwerp, vergelijkbaar met een platform voor sociale media.

Deel ideeën en zinvolle inzichten in een informele omgeving. Vind berichten niet leuk, upload inhoud en reageer op berichten. Zie voor meer informatie [***Sociaal leren in de mobiele app***](../learners/feature-summary/ipad-android-tablet-users.md#socialmobile).

**Media op een board delen**

Deel afbeeldingen, documenten, audio- of videobestanden op elk board, zodat andere leden van het board uw bericht kunnen bekijken en een interactie kunnen starten.  Zie voor meer informatie [***Bericht delen***](../learners/feature-summary/ipad-android-tablet-users.md#socialmobile).

**Bestand verzenden voor klassikale en activiteitsmodules**

Verzend bestanden als bewijs van voltooiing van de cursus naar uw docent. De docent kan vervolgens uw inzending goedkeuren of afwijzen op basis van de inhoud van het bestand. Zie voor meer informatie [***Bestand ter goedkeuring verzenden***](../learners/feature-summary/ipad-android-tablet-users.md#submitfile).

**Bijgewerkte platformondersteuning**

De mobiele app van Learning Manager wordt nu ondersteund op apparaten met Android 7 en hoger en iOS 10 en hoger. Zie voor meer informatie [***Systeemvereisten***](../system-requirements.md).

### Bekende problemen in deze release {#Knownissuesinthisrelease-3}

1. Op Android kunt u geen GIFFEN uploaden in een bericht, opmerking of tijdens het beantwoorden van een opmerking.
1. Als moderator van een board kunt u het bericht, de opmerking of het antwoord van een gebruiker niet verwijderen. U kunt echter hetzelfde uitvoeren vanuit de webapp.
1. In de app kunt u geen vraagtype markeren.
1. Nadat u Sociaal leren in de app hebt ingeschakeld, start u de app opnieuw om het tabblad weer te geven **Sociaal leren**. Als u Sociaal leren niet ziet, sluit u de app en start u de app opnieuw. Het tabblad Sociaal leren is zichtbaar.

+++

+++Update 46

### Nieuwe en verbeterde functies {#Newandenhancedfeatures-7}

## Update 46

Releasedatum: 20 juni 2019

**Automatisch beheer van inhoud**

Met Sociaal leren kunt u inhoud die door studenten is geplaatst op twee manieren beheren, namelijk: - **Geen beheer** en **Handmatig beheer**. In deze release verbetert Adobe Learning Manager de mogelijkheden voor sociaal leren door AI-functies voor automatisch beheer te bieden. Nadat inhoud is gepost, wordt de inhoud geanalyseerd om na te gaan of de inhoud behoort tot de vaardigheid waarvoor de inhoud is gepost. Op basis van de vertrouwensscore wordt de inhoud live geplaatst of verzonden voor handmatig beheer. Zie voor meer informatie *[** Auto-ondersteund beheer **](../administrators/feature-summary/social-learning-configurations-as-an-admin.md#autocuration)**.***

**Vaardigheid toewijzen aan vaardigheidsdomeinen**

Wijs vaardigheden in uw account toe aan de vaardigheidsdomeinen die aanwezig zijn in het LMS van de Learning Manager. Zo kunt u uw accountvaardigheden koppelen aan de vaardigheidsdomeinen die worden ondersteund door de Learning Manager voor automatisch beheer. Zie voor meer informatie [***Vaardigheid toewijzen aan domeinen***](../administrators/feature-summary/curation-skills.md).

**CSV-specificaties en voorbeeld-CSV&#39;s**

Bijgewerkte CSV-specificaties die u kunt gebruiken om uw bestaande LMS-migratiegegevens toe te wijzen. Gebruik de nieuwste downloadbare CSV-specifications en sample-csvs zip-bestanden om inzicht te krijgen in de voorgeschreven indeling van in te voeren gegevens. Zie voor meer informatie  [***Migratiehandleiding***.](../integration-admin/feature-summary/migration-manual.md)

### Opgeloste problemen in deze release {#Issuesfixedinthisrelease-4}

**Learning Manager-API**

* Wanneer een extern profiel wordt toegevoegd met de API-methode POST *externalProfile*, wordt de welkomstmail niet weergegeven.

**Managerdashboard**

* Wanneer een manager de optie heeft geselecteerd **Dit kwartaal**, werden de gegevens over inschrijving, voortgang en voltooiing van een leerobject niet weergegeven. In deze versie worden deze gegevens nu weergegeven zoals verwacht.

**Studenten op wachtlijst**

* In eerdere versies van Leermanager werd na inschrijving door een manager een foutbericht weergegeven wanneer een docent wilde controleren of er studenten op de wachtlijst stonden. In deze release kan een docent door de lijst met studenten op de wachtlijst bladeren zonder dat er een foutbericht verschijnt.

**Overzicht van certificering**

* Nadat een auteur een cursus en een certificering had gemaakt die een beschrijving en overzichtsinhoud bevatte, werd de overzichtsinhoud niet weergegeven zoals verwacht toen een student op de cursuspagina belandde. De inhoud was echter wel zichtbaar op de voorbeeldpagina&#39;s van de student in de Admin- en Auteur-apps. In deze release wordt de inhoud van het overzicht weergegeven zoals verwacht in de Learner-app.

**Catalogus**

* Voor elke catalogus kan een student alle leerobjecten bekijken. Als in eerdere versies een catalogus geen leerobject bevatte, werd de catalogus nog weergegeven aan het begin van andere catalogi. In deze release staan alle catalogi zonder leerobjecten onder aan de catalogi.

+++

+++Update 45

Releasedatum: 30 mei 2019

**Nieuwe en verbeterde functies**

* Geconsolideerd zoeken in alle instanties naar ingeschreven studenten in de studentsectie van het leerobject. Zoek naar ingeschreven gebruikers in de sectie Student van het leerobject met automatisch aangevulde zoeksuggesties. Zie voor meer informatie [***Zoeken naar ingeschreven gebruikers***](../administrators/feature-summary/courses.md#searchforusers).
* Volledige bewerkingsmogelijkheden van leerobjecten die via een gedeelde catalogus zijn verkregen. Zie voor meer informatie [***Besturing gedeelde catalogus***](../administrators/feature-summary/shared-catalog-full-control.md). Neem contact op met de ondersteuning van Leermanager om de functie in te schakelen.
* Docenten kunnen nu gemakkelijk de sessies en modules identificeren met openstaande beoordelingen. Zie voor meer informatie [***Beoordelingen in behandeling***](../instructors/feature-summary/learners.md#pending).

* Vaardigheden ondersteunen nu het toekennen van creditwaarden in decimale notatie. Op deze manier kunnen auteurs een decimaal niveau aan een bepaalde cursus toekennen. Zie voor meer informatie [***Decimale ondersteuning***](../administrators/feature-summary/skills-levels.md#decimal).
* Automatiseer het maken van aangepaste rollen. Zie voor meer informatie [***Rollen configureren via CSV-bestanden***](../integration-admin/feature-summary/configure-role-csv-files.md).
* Inzendingen vereist voor externe certificeringen en activiteitenmodules zijn nu optioneel. Hierdoor kunnen managers en docenten evalueren zonder indiening. Zie voor meer informatie [***Optionele indiening***](../managers/feature-summary/learning-objects.md#optional).
* Download Studenttranscripten voor verwijderde gebruikers. Zie voor meer informatie [***Studenttranscripten***](../administrators/feature-summary/learner-transcripts.md).
* Ondersteuning voor de volgende talen:

   * Koreaans
   * Turks
   * Nederlands
   * Pools

**Bekende problemen**

* Decimale ondersteuning in vaardigheidspunten wordt alleen ondersteund voor Engels.
* Voor Koreaans, Japans en Russisch wordt de waarde van de sessietijdmeridiaan niet weergegeven zoals verwacht.

**Opgeloste problemen in deze release**

* De quizscores worden niet opgeslagen voor een leerprogramma of certificering op het tabblad Aanwezigheid en scores.
* Een beheerder of manager kan een externe certificering niet als voltooid markeren.
* In het dialoogvenster Studenttranscripten kan een beheerder geen aangepast datumbereik selecteren als de taal is ingesteld op Portugees of Spaans.
* Een beheerder kan geen extern profiel maken wanneer de profieltaal Frans is.
* Actieve velden zijn niet zichtbaar in het dialoogvenster Gebruiker bewerken als de landinstelling een andere taal heeft dan Engels.

+++

+++Update 44 - Mobiele app

Releasedatum: 26 april 2019

* **Wijzigingen in gebruikersinterface:** In de app  ![](assets/hamburger.jpg) en de  ![](assets/search-magnifying-glass-icon.png) boven in het scherm worden nu opties weergegeven.

![](assets/1.png)

* **QR-code scannen voor inschrijving:** De mogelijkheden voor QR-codes zijn verbeterd. Naast ondersteuning voor het markeren van aanwezigheid met behulp van QR-code, ondersteunt deze nu ook het inschrijven voor een cursus en het voltooien van een cursus met behulp van QR-code.

  Als u zich voor een cursus wilt inschrijven en de cursus wilt voltooien, kunt u een QR-code scannen die uw beheerder heeft verstrekt. Ga voor meer informatie over het scannen van QR-codes in de webversie van Learning Manager naar  [***QR-code scannen***](<https://helpx.adobe.com/captivate-Learning> Manager/whats-new.html#QRcodetoenrollcompletenrollcompleteaccourse).

* **Meerdere pogingen op cursus:** Met de app Leermanager kan de student cursussen volgen waarvoor meerdere pogingen zijn ingeschakeld. Zie voor meer informatie over het instellen van meerdere pogingen  [***Meerdere pogingen***](<https://helpx.adobe.com/captivate-Learning> Manager/authors/feature-summary/courses.html#multiPogingen).

+++

+++Update 43

## Update 43

Releasedatum: 28 januari 2019

* De leertijd die een student aan een module heeft besteed, kan meerdere keren worden geteld bij het meer dan één keer markeren van aanwezigheid. Dit probleem is opgelost.
* Aanwezigheid voor een leerobject binnen een meerdaagse sessie markeren kan de verkeerde startdatum voor de sessie voor een student in een leertranscript weergeven. Dit probleem is opgelost.
* Gebruikers kunnen een cursus mogelijk niet bekijken wanneer deze aan een voltooid leerprogramma of een voltooide certificering wordt toegevoegd. Dit probleem is opgelost.
* Gebruikers kunnen zich ten onrechte inschrijven wanneer ze uit een gebruikersgroep worden verplaatst. Dit probleem is opgelost.
* Studenten en docenten ontvangen mogelijk geen e-mail wanneer de sessiedetails worden gewijzigd in de app voor docenten. Dit probleem is opgelost.
* URL van Adobe Connect werkt mogelijk niet correct wanneer &#39;/&#39; aan het einde van de URL wordt opgegeven. Dit probleem is opgelost.
* Er kan een foutbericht worden weergegeven wanneer u ten minste één verplichte module selecteert voor een reeds gepubliceerde cursus. Dit probleem is opgelost.
* Wanneer een student een cursus heeft voltooid en deze als verplicht is gemarkeerd door de auteur, wordt de voltooiing van de cursus mogelijk niet als voltooid gemarkeerd. Dit probleem is opgelost.
* Gecontroleerde waarde van een geselecteerde module voor een dubbele cursus wordt mogelijk niet onmiddellijk weergegeven. De cursus wordt alleen als een dubbele cursus weergegeven wanneer de pagina wordt vernieuwd. Dit probleem is opgelost.
* Na publicatie van een cursus worden alle modules als niet-ingeschakeld weergegeven in de bewerkingsmodus. De pagina moet worden vernieuwd om de wijzigingen te kunnen zien. Dit probleem is opgelost.
* Selectie van een verplichte module was mogelijk beschikbaar voor een geordende cursus wanneer deze niet had moeten zijn. Dit probleem is opgelost.
* Er verschijnt nog steeds een verplichte module in het vervolgkeuzemenu nadat deze is verwijderd tijdens het bewerken van de cursus. Dit probleem is opgelost.
* Voorwerk- en testmodules worden standaard als verplicht gemarkeerd. Dit probleem is opgelost.
* Als u op de L3-feedbackkoppeling in uw e-mail klikt, wordt het modaal met feedback mogelijk niet geopend. Dit probleem is opgelost.
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

* Beheerders kunnen bepalen welke machtigingen studenten krijgen om quizscores in Studenttranscripten weer te geven. U kunt deze functie in- of uitschakelen op de pagina Instellingen.
* Het invoegen van gebruikersmeldingen kan willekeurig mislukken, waardoor de bijbehorende e-mails niet worden bezorgd. Dit probleem is opgelost.
* Gegevens over de bestede leertijd verschijnen niet in het Studenttranscript en de Dashboard Rapporten. Dit probleem is opgelost.
* Informatie over activiteiten zoals inschrijving/voltooiing is mogelijk niet aanwezig in het Studenttranscript dat door een manager is gedownload. Dit is opgelost.
* Modules die deel uitmaken van een cursus die nog wordt uitgevoerd, kunnen in het Studenttranscript worden weergegeven als voltooid. Dit probleem is opgelost.
* Studenttranscript geeft de gedownloade gegevens mogelijk niet weer volgens het geselecteerde datumbereik. Dit probleem is opgelost.
* Voor gebruikers waaraan alleen de rol Auteur is toegewezen, worden catalogi mogelijk niet weergegeven. Dit probleem is opgelost.
* Wanneer een aangepaste rolbeheerder het Studenttranscript downloadt, bevat het gedownloade rapport geen informatie over de LO&#39;s die alleen deel uitmaakten van standaardcatalogi. Dit probleem is opgelost.
* Het totaalaantal gebruikers en de lijst met gebruikers op de pagina Gebruikersgroep komen mogelijk niet overeen. Dit is opgelost.
* De pop-up van het leerprogramma verschijnt mogelijk niet, zelfs niet wanneer deze is ingeschakeld en gebruikers worden omgeleid naar de LO-pagina. Dit probleem is opgelost.
* Wanneer de wachtlijst is gewist en studenten voor een cursus zijn ingeschreven, kan de beheerder een e-mailbericht ontvangen met de naam van de student in plaats van de naam van de student te vermelden. Dit probleem is opgelost.
* Achternaam wordt mogelijk niet weergegeven in de gebruikersinterface voor een gebruiker die via de POST-gebruikers-API is toegevoegd. Dit probleem is opgelost.

+++

+++Update 40

Update 40

Releasedatum: september 2018.

Prestatieverbetering

* Gebruikers ondervinden mogelijk time-out-problemen tijdens het downloaden van grote sets studenttranscript. Dit probleem is opgelost.
* Gebruikers kunnen vertraging ervaren tijdens het downloaden van een grote set inschrijvingsrapporten waarin de quizscore van de student is opgenomen. Dit probleem is opgelost.
* Het downloaden van een grote set quizscorerapporten kan langer duren dan normaal. Dit is opgelost.
* Wanneer de student een leerprogramma heeft voltooid, verschijnt het L1-feedbackformulier niet automatisch, zelfs wanneer de automatische pop-up door de beheerder is ingeschakeld. Dit probleem is opgelost.
* In de gedownloade rapporten van het audittrail van de gebruiker en het audittrail van de inhoud kunnen de kolommen die zijn gewijzigd op gebruikersnaam en gewijzigd op e-mailadres van de gebruiker niet worden vastgelegd. Het rapport toont Systeem in dergelijke gevallen. Deze is bijgewerkt en gemarkeerd als Onbekend.

+++

+++Update 39

Releasedatum: 19 mei 2018.

* Deze release van Adobe Learning Manager introduceert nieuwe functies en verbeteringen. Het biedt de mogelijkheid om aangepaste rollen te maken, cataloguslabels toe te voegen, gebruikers leegte, tags te beheren, leerobjecten een andere naam te geven, Slack-integratie, nieuwe connectorintegraties, ondersteuning voor xAPI en nog veel meer. Ga voor meer informatie over de nieuwe functies en verbeteringen naar  [Overzicht van de nieuwe functie](../whats-new.md#main-pars_text).

* Learning Manager voldoet aan de AVG. Zie voor meer informatie [Compatibiliteit van Learning Manager met AVG](/help/migrated/kb/prime-gdpr.md).

## Bekend probleem {#knownissue}

* De hyperlink naar het aantal cursussen en certificeringen binnen het modaal venster Tags bevat schaduwcursussen en terugkerende certificeringen. Wanneer u op de hyperlink klikt, worden deze cursussen en certificeringen mogelijk niet in de lijst weergegeven, wat leidt tot een verschil in aantal.

+++

+++Update 38

* Studenten met de status In behandeling of met de status In afwachting van acceptatie werden als voltooid gemarkeerd. Dit probleem is opgelost.
* Wanneer een docent alle studenten zoekt en selecteert, verschillen het aantal geselecteerde studenten en het getoonde aantal. Dit probleem is opgelost.
* Wanneer u een student zoekt en deze selecteert en aanwezigheid markeert, kan de leermanager aanwezigheid voor alle studenten markeren. Dit is opgelost.
* Leermanager geeft de tijd in e-mails weer in 24-uursnotatie. Dit is opgelost. De tijd wordt nu weergegeven in de 12-uursnotatie.
* Wanneer een manager een student voor een cursus aanwijst met de knop Aanwijzen op de meldingenpagina, wordt het modale venster Aanwijzen niet geladen. Dit is opgelost.
* In geëxporteerde Excel-rapporten zou de deadline (inschrijvingsdatum + dagen om de waarde in automatische instantie van de LO&#39;s te voltooien) onjuist worden weergegeven. Dit probleem is opgelost.

* Zoekresultaten van gebruikers worden leeg weergegeven wanneer er geen gebruikers aanwezig zijn in de groep die wordt doorzocht. Dit is nu opgelost.
* Managers kunnen niet worden verwijderd, zelfs niet als er geen directe rapporten zijn. Dit probleem is opgelost. Managers kunnen nu worden verwijderd.
* Functionaliteit voor voortgang van module opnieuw instellen werkt mogelijk niet meer. Dit is nu opgelost.
* Verwijderde certificering kan worden weergegeven in de widget voor studenten. Dit probleem is opgelost.
* Het probleem met de berekening van de cursuseffectiviteit is opgelost.

* Het probleem met de integratie van een nieuw Connect-account is opgelost.
* Automatische pop-up van L1-feedback wordt niet weergegeven als deze is ingeschakeld bij niet-standaardinstanties. Probleem is opgelost.
* Docenten kunnen aanwezigheid voor alle gebruikers niet tegelijk markeren voor sessies die deel uitmaken van het leerprogramma/certificering. Dit is opgelost.

+++

+++Update 37

Releasedatum: 25 maart 2018.

De versie van maart 2018 van Adobe Learning Manager introduceert spannende nieuwe functies en verbeteringen. Het biedt u de mogelijkheid om rapporten van de audittrail van gebruikers en aanmeldings-/toegangsrapporten te genereren, studenten de mogelijkheid te bieden cursusinstanties te kiezen, klaslokalen en virtuele lesruimten te verbeteren, en nog veel meer. Deze release biedt ook oplossingen voor problemen en prestatieverbeteringen.

Als u alle nieuwe functies in deze versie wilt lezen, raadpleegt u  [Nieuwe functies in Adobe Learning Manager](../whats-new.md).

### Bekend probleem {#KnownIssue-1}

**Probleem:** Het openen van een aantal specifieke leerobjecten met Internet Explorer v11.1478.10586.0 kan ertoe leiden dat de leermanager vastloopt.

**Oplossing:** Werk uw Internet Explorer 11-browser bij naar de nieuwste versie door contact op te nemen met het IT-team in uw organisatie.

+++

+++Update 36

Releasedatum: 22 januari 2018.

### Opgeloste problemen {#issuesfixed}

* Als u een wijziging aanbrengt in de instelling van de E-mailsjabloon, verdwijnt de E-mailbanner. Dit probleem is opgelost.
* Studenten kunnen geen persoonlijke taakhulpen toevoegen/starten. Dit is opgelost.
* Aangepaste gebruikersgroepen in een account worden mogelijk niet vermeld onder het veld gebruikersgroep in het modale venster Rapport toevoegen/bewerken. Dit probleem is opgelost.
* Als de naam van een badgeafbeelding ruimte bevat, wordt deze mogelijk niet weergegeven op de startpagina voor de student.
* Wanneer een ingeschreven gebruiker uit een cursus wordt verwijderd, worden het cursusrapport en het quizrapport niet gegenereerd voor die specifieke cursus. Dit probleem is opgelost.
* Als de beheerder het aantal aangewezen plaatsen voor een manager wijzigt, kan het aantal verkeerd worden weergegeven in het nominatieverzoek wanneer het vanuit verschillende plaatsen wordt geopend. Dit probleem is opgelost.
* Bij het converteren van een externe gebruiker naar een interne gebruiker, wordt de gebruiker mogelijk niet toegevoegd aan de groep Alle interne studenten. Dit probleem is opgelost.
* Als u naar een individuele student zoekt, deze selecteert en de uitschrijvingsactie uitvoert, kunnen alle studenten in die groep worden uitgeschreven in plaats van alleen de geselecteerde student. Dit probleem is opgelost.
* Als beheerder kunt u het selectievakje mogelijk niet gebruiken om een student binnen certificeringen te selecteren. Dit probleem is opgelost.
* Het maken en bijwerken van gebruikersgroepen met meer dan 600 individuele gebruikers mislukt. Dit probleem is opgelost. U kunt nu gebruikersgroepen met meer dan 600 individuele gebruikers maken.
* Als u een aangepaste gebruikersgroep verwijdert die deel uitmaakt van een andere aangepaste gebruikersgroep, kan de intersectieregel het gebruikersnummer naar de hogere groep doorschuiven. Dit probleem is opgelost.
* Wanneer de standaardcatalogus is uitgeschakeld en er een nieuwe catalogus wordt gemaakt en de manager toegang heeft tot deze nieuw gemaakte catalogus, kan hij mogelijk geen cursus onder die catalogus zoeken. Dit probleem is opgelost.
* Gebruikers van mobiele toepassingen ontvangen geen L1-feedback als pushberichten. Dit is opgelost.

+++

+++Update 35

Releasedatum: 7 januari 2018.

Deze release van Learning Manager biedt u prestatieoptimalisaties om de schaalbaarheid, prestaties en beveiliging te verbeteren.

### Verbeteringen {#enhancements}

* Ervaar elastisch zoeken tijdens het zoeken naar cursussen en gebruikers in alle toepassingen. Dit omvat zoeken in cursussen, gebruikers en gebruikersgroepen.
* Ondersteuning voor het gebruik van Box-connector om Learning Manager te integreren met externe systemen om de synchronisatie van gegevens te automatiseren. Zie voor meer informatie [Box-connector](../integration-admin/feature-summary/connectors.md#main-pars_header_302653946).
* Bijgewerkte CSV-specificaties die u kunt gebruiken om uw bestaande LMS-migratiegegevens toe te wijzen. Gebruik de nieuwste downloadbare CSV-specifications en sample-csvs zip-bestanden om inzicht te krijgen in de voorgeschreven indeling van in te voeren gegevens. Zie voor meer informatie [Migratiehandleiding.](../integration-admin/feature-summary/migration-manual.md)

+++

+++Update 34

### Opgeloste problemen {#IssuesFixed-1}

* Aankondigingen mislukken wanneer het aantal gebruikers groot is. Dit probleem is opgelost.
* Toegang tot het Leerbeheerdersaccount met behulp van de subdomein-URL in de EU kan gebruikers omleiden naar een andere pagina. Dit probleem is opgelost.
* Wanneer een LP wordt besteld, moet een student de LP alleen in de opgegeven volgorde kunnen gebruiken. Studenten konden cursussen die niet in de lijst stonden, eerst volgen met behulp van de cursushyperlinks. Dit probleem is opgelost. Studenten kunnen een cursus pas starten nadat hij de vorige heeft voltooid.

* Foutbericht voor niet-ondersteunde browserversie wordt niet weergegeven in niet-ondersteunde versies van Internet Explorer (IE 7, IE 8, IE 9 en IE 10) en Safari (versie 7, 8 en 9). Dit probleem is opgelost.



+++

+++Update 33

Releasedatum: 5 oktober 2017.

### Opgeloste problemen {#IssuesFixed-2}

* Wijzigingen in een gedeelde cursus worden niet doorgegeven aan het gedeelde account als de auteur de cursus automatisch opslaat in het oorspronkelijke account. Dit probleem is opgelost.
* Voor specifieke Leerbeheerprojecten werd content soms vastgezet in de Fluidic Player. Dit probleem is opgelost.

* De kalenderlijst onder de widget Leerkalender in het dashboard Student kan in willekeurige volgorde worden weergegeven. Dit probleem is opgelost. De lijst wordt nu op een ordelijke manier weergegeven.
* Wanneer aanwezigheid wordt gemarkeerd met de optie Alles selecteren, worden studenten in de leerobjecten voor dezelfde sessie gemarkeerd als aanwezig. Dit probleem is opgelost.
* In bepaalde schermen met hoge resolutie gaf de e-mail die werd ontvangen van Learning Manager problemen met de uitlijning en afbreking van de bannerafbeelding en -tekst. Dit is opgelost.
* Bepaalde e-mails van Learning Manager, zoals e-mails zonder berichtgegevens, werden niet geactiveerd voor de gebruikers. Voorbeeld: e-mail ontvangen bij het maken en inschakelen van een extern profiel en e-mail ontvangen bij het configureren van een Connect-account. Dit probleem is opgelost.
* Wanneer u een LP maakt, een herinnering instelt, gebruikers inschrijft en vervolgens de deadline van de instantie wijzigt, wordt de gewijzigde deadline mogelijk niet weergegeven voor de herinneringen. Dit is opgelost. De herinneringen hebben nu de gewijzigde deadline.
* In bepaalde gevallen waren voor inhoud die is gemaakt met Adobe Presenter het totaal en de verstreken tijd in de Fluidic Player niet gelijk aan de inhoud. Dit probleem is opgelost.
* In bepaalde gevallen is de optie om toe te voegen nog steeds ingeschakeld nadat u een leerprogramma aan een catalogus hebt toegevoegd. Dit probleem is opgelost.
* Als u Leerbeheer opent in een apparaatbrowser, wordt een optie weergegeven voor het ervaren van Leerbeheer op de apparaatapp. Klik op Ja om de Play Store (Android) te starten als de app niet is geïnstalleerd, of start de app als deze is geïnstalleerd (in Android en iOS). Er waren problemen met deze workflow en deze zijn opgelost.

+++

+++Update 32

Releasedatum: 17 augustus 2017.

### Opgeloste problemen {#IssuesFixed-3}

**Cursus met meerdere moduleversies die bij een verwijderingsactie wordt teruggedraaid naar de vorige versie.**

Wanneer een cursus meerdere moduleversie-items voor specifieke modules heeft, wordt deze bij het verwijderen van de module teruggedraaid naar de vorige versie en niet volledig verwijderd. Dit probleem is opgelost.

**Wijzigingen in een gedeelde cursus worden niet doorgegeven als deze automatisch worden opgeslagen door de muis tussen tabbladen te verplaatsen.**

Wijzigingen in een gedeelde cursus worden niet doorgegeven aan een tenantaccount als de auteur in het bovenliggende account de cursus automatisch opslaat door naar het volgende tabblad te gaan. Dit probleem is opgelost.

**Gebruikers konden de deadline van instanties niet wijzigen voor een cursus met alleen activiteiten.**

Gebruikers konden de deadline van een instantie niet wijzigen in activiteitscursussen omdat dit zou terugkeren naar de vorige deadline. Dit probleem is opgelost.

**Geen mogelijkheid om een unieke id te gebruiken nadat deze uit een leerobject is verwijderd.**

Wanneer u een unieke id aan een cursus toewijst en deze verwijdert, kunt u deze niet meer gebruiken. Dit probleem is opgelost.

**Een leerprogramma dat al is ingeschreven als onderdeel van een leerplangebeurtenis, verschijnt opnieuw als onderdeel van een andere gebeurtenis in de Learner-app.**

Als een leerprogramma al is ingeschreven als onderdeel van een leerplangebeurtenis, kan het weer verschijnen als onderdeel van een andere gebeurtenis in de Learner-app. Dit probleem is opgelost.

**Student ontvangt herinneringse-mails met onjuiste deadline/sessietijd.**

Studenten kregen vaak e-mails met onjuiste herinneringen voor de deadline of de sessietijd vanwege tijdzonecorrecties. Dit probleem is opgelost.

**De tijdlijn van het gamificationleaderboard toont externe studenten als hij wordt omgezet van een externe student in een interne student.**

De tijdlijn van het gamificationleaderboard van een interne student kan externe student tonen wanneer deze van een externe naar een interne student wordt geconverteerd. Dit probleem is opgelost.

**Het UUID-veld voor een student wordt in bewerkbare indeling weergegeven terwijl er één gebruiker en CSV-gebruikers in een UUID-account worden gemaakt.**

De student zag het UUID-veld tijdens het voltooien van zijn profiel, zelfs als de beheerder de UUID voor één gebruiker en CSV-gebruikers heeft verstrekt. Dit probleem is opgelost.

**De bestede leertijd wordt in bepaalde gevallen niet vastgelegd in rapporten.**

De bestede leertijd werd niet weergegeven in rapporten voor een student.

* Als zijn/haar aanwezigheid automatisch wordt gemarkeerd door het systeem voor het aansluiten van modules.
* Wanneer een QR-code wordt gescand voor CR- en VC-modules met behulp van de toepassing Learning Manager-apparaat.

**Deze release van Learning Manager introduceerde ook verbeteringen en foutoplossingen met betrekking tot de apparaatspeler.**

* Problemen met de voltooiing van activiteitenmodules. Dit is opgelost.
* Wanneer de student een video afspeelt in de staande modus, werken de knoppen +10 en -10 mogelijk niet. Dit is opgelost
* Verbeterde afspeelervaring van bepaalde voorbeeldprojecten bij afspelen op een Android-apparaat (mobiel en tabblad) dat eerder zou flikkeren.
* Wanneer u een nieuwe notitie toevoegt, moet het notitievenster worden gesloten en moet het afspelen worden hervat in de speler. In bepaalde gevallen is dit niet het geval. Dit is opgelost.
* Wanneer u de notities opent die aan een module zijn toegevoegd, wordt de knop Sluiten mogelijk niet weergegeven. Dit probleem is opgelost.
* Wanneer de student het notitievenster opent met behulp van Notititiemarkering, moet hij mogelijk tweemaal op het pictogram Notities klikken om het deelvenster te sluiten.
* Als u op de inhoudsopgave klikt, wordt deze mogelijk niet automatisch samengevouwen en moet u de inhoud handmatig sluiten. Dit probleem is opgelost.
* Een cursus die een module met meerdere talen heeft, geeft mogelijk niet alle beschikbare talen weer, omdat de schuifbalk mogelijk niet overeenkomstig wordt geschaald. Dit is opgelost.
* Wanneer u een activiteitencursusmodule van derden opent in de modus Liggend in een speler, wordt de tekstrichting mogelijk niet aangepast, waardoor het moeilijk is om te schuiven. Dit is opgelost.
* Het tikgebied voor de sluitknop van de speler is vergroot in zowel de online als de offline modus.
* De inhoudsopgave wordt niet automatisch gesloten wanneer de oriëntatie van het apparaat wordt gewijzigd. Dit is opgelost.
* Enkele kleine problemen met betrekking tot de gebruikersinterface, zoals de uitlijning van de afspeelknop, het keuzerondje en andere instellingen in de liggende en staande modus, zijn opgelost.

* Het probleem met de zoekbalk die wordt weergegeven, zelfs als de afspeeloptie voor de show uitgeschakeld is in inhoud, is opgelost.
* De sluitknop van de speler was niet zichtbaar voor bepaalde projecten wanneer de oriëntatie van het apparaat was gewijzigd. Dit is opgelost.
* Het probleem met betrekking tot de inhoudsopgave van de module die wordt afgekapt in de liggende modus op de apparaatspeler, is opgelost. In bepaalde gevallen was de inhoudsopgave niet zichtbaar voor de inhoud in de apparaatspeler. Dit is ook gecorrigeerd.

**Deze release van Learning Manager bevat ook verbeteringen en oplossingen voor de apparaattoepassing die hieronder worden vermeld**.

* Pushmelding met betrekking tot voltooiingsdeadlines wordt niet geleverd op bepaalde apparaten. Dit probleem is opgelost.
* We ondersteunen nu ook de levenscyclus van leerobjecten op apparaattoepassing. Studenten hebben nu toegang tot de nieuwste inhoud in leerobjecten als deze door de auteur zijn bewerkt.

* Problemen met de toepassingsoriëntatie (inclusief de standaardoriëntatie en staande modus) van de Leerbeheertoepassing zijn opgelost.
* Er is mogelijk geen optie om de inhoud bij te werken wanneer de gebruiker overschakelt van de offline naar de online modus.
* Modulebestelling wordt nu ondersteund voor cursussen in apparaattoepassing in online modus.

* Als een gebruiker geen taakhulpen heeft gedownload, kan het klikken op het tabblad Mijn taakhulpen in de offline modus ertoe leiden dat de app in IOS vastloopt en een bericht verschijnt met de melding dat er een fout is opgetreden bij het laden van gegevens in Android. Dit is opgelost.
* De toepassing Learning Manager sluit of genereert een fout als we de cursus direct openen nadat we het internet hebben uitgeschakeld, zelfs als het een gedownloade cursus is. Dit probleem is nu opgelost.
* Wanneer u de QR-code scant, wordt soms een vastgelegde afbeelding van de vorige QR-codescan weergegeven. Dit is gecorrigeerd.
* Als u probeert een taakhulp te verwijderen die al op het tabblad Taakhulpen is toegevoegd, wordt er een foutbericht weergegeven. Dit probleem is opgelost.

+++

+++Update 31

Releasedatum: 16 juli 2017.

### Verbeteringen {#Enhancements-1}

**Gamification**

Deze release vergroot het bereik van gamification. Externe gebruikers kunnen nu deelnemen aan Gamification. Als beheerder kunt u het bereik van gamification definiëren door de bereikinstellingen te wijzigen. U kunt gamification selectief inschakelen onder vergelijkbare profielgebruikers, groepen of locatie.

**Verbeteringen voor externe gebruikers**

Dankzij deze verbetering kunt u een tijdbereik instellen waarna gebruikers automatisch worden verwijderd na de periode van inactiviteit. Dankzij deze verbetering kan de beheerder ook de gebruiker opnieuw als externe student toevoegen voor zowel automatisch als handmatig verwijderde studenten.

**Taakhulp, aankondigingen en uitschrijvingsrapport**

Taakhulpen zijn trainingsinhoud waartoe een student toegang heeft zonder dat hij of zij zich hoeft in te schrijven voor een specifiek leerobject zoals een cursus of leerprogramma. Dankzij deze verbetering kunnen beheerders het Taakhulpenrapport extraheren en downloaden. Als beheerder kunt u ook een rapport genereren van alle aankondigingen die door u zijn verzonden. Beheerders en managers kunnen ook een rapport extraheren van de studenten die zijn uitgeschreven.

**Leermanagerconnectoren**

U kunt nu gebruikersvaardigheden exporteren naar een FTP-locatie om deze te integreren met een willekeurig extern systeem met behulp van de optie Gegevens exporteren. U kunt de verbindingsnaam voor uw integratie opgeven en kiezen of u interne gebruikers wilt importeren of gebruikersvaardigheden wilt exporteren door deze te configureren of op verzoek op te halen.

**Cursusinstanties kopiëren**

U kunt nu de instantie-URL kopiëren door op de vervolgkeuzepijl in de rechterbovenhoek van een instantie te klikken.

### Opgeloste problemen {#IssuesFixed-4}

**Gebruikers krijgen geen agenda-uitnodiging wanneer ze zijn ingeschreven voor het leerprogramma**

Gebruikers kregen soms geen agenda-uitnodiging (.ics) wanneer ze zich inschrijven voor leerprogramma&#39;s, certificaten met lesruimte en Connect-sessies. Dit probleem is opgelost. Gebruikers krijgen nu .ics-bestanden als bijlagen waarin de sessiedetails en de inschrijvingsmail worden vermeld.

**Beschrijving van activiteit, ook als deze in meerdere talen wordt verstrekt, wordt nog steeds in het Engels weergegeven**

Een gebruiker waarvan de taalvoorkeur voor de inhoud is ingesteld op niet-Engels, kan de beschrijving van de activiteitenmodule nog steeds in het Engels zien. Dit probleem is opgelost.

+++

+++Update 30

Releasedatum: 30 juni 2017.

### Verbeteringen {#Enhancements-2}

**Ondersteuning voor meerdere leerobjecten in leerplan**

Als beheerder of auteur kunt u nu meerdere leerobjecten aan een leerplan toewijzen. Als een van de leerobjectinstanties wordt gearchiveerd of verloopt, wordt het hele leerplan automatisch uitgeschakeld. Dankzij deze verbetering kunt u ook zoeken in **[!UICONTROL Voltooid leermateriaal]** en **[!UICONTROL Leermateriaal toewijzen]** velden met unieke ID&#39;s voor leerobjecten.

**Toegankelijkheid**

Met deze update ondersteunt Learning Manager Learner Experience nu sectie 508-toegankelijkheidsstandaard. Learning Manager is ook compatibel met de nieuwste versie van **[!UICONTROL JAWS]**. Deze functie wordt alleen ondersteund voor de Learner-toepassing. Gebruik Internet Explorer 11, Windows Chrome of macOS Safari om toegang te krijgen tot deze functie.

### Opgeloste problemen {#IssuesFixed-5}

**Onjuiste informatie in bepaalde tijdzones**

In herinneringen voor deadlines werd het aantal resterende dagen voor studenten in bepaalde tijdzones onjuist vermeld. Dit probleem is opgelost.

**Problemen met het leerprogramma in het geval van een verlopen programma-instantie**

Bij het starten van modules van het leerprogramma traden er problemen op als de programmainstantie was verlopen. Hierdoor werkte de uitbreiding van de module niet en konden studenten de speler niet starten en de inhoud niet bezoeken. Dit probleem is opgelost.

**Vertaalproblemen in Learner-toepassing**

Gebruikers van de leermanager ondervonden bepaalde vertaalproblemen in de Learner-app. Deze problemen zijn opgelost.

**Problemen met een abonnement op een vaardigheid**

In bepaalde gevallen konden studenten zich niet abonneren op een nieuwe vaardigheid. Dit probleem is opgelost.

+++

+++Update 29

Releasedatum: 9 april 2017.

### Nieuwe functies {#newfeatures}

Voor een lijst met nieuwe functies en verbeteringen in de Learning Manager-release van april raadpleegt u [Nieuwe functies.](../whats-new.md)

**Widget-app voor studenten**

Gebruik widgets op de startpagina om uw cursussen, vaardigheden en resultaten te beheren. Gebruik de zoekbalk om een zoekopdracht uit te voeren in uw gehele LMS dat alle leerobjecten, catalogi, vaardigheden, notities en discussies omvat

Ga voor meer informatie over de nieuwe startpagina naar  [Startpagina voor studenten in Leermanager](../learners/feature-summary/getting-started-learner.md).

**Beheerdersinstellingen voor het Studentendashboard**

Als beheerder kunt u de startpagina van de student bepalen door verschillende widgets in en uit te schakelen.

**Mobiele app van Learning Manager voor studenten**

Met de nieuwe mobiele app van Learning Manager kunnen studenten de app gebruiken om zich in te schrijven voor cursussen en deze uit te voeren. De app kan ook worden gebruikt om dashboards te beheren.

Ga voor meer informatie over het gebruik van Learning Manager in mobiele telefoons naar  [Leerprogramma van Learning Manager voor mobiele telefoons](../learners/feature-summary/ipad-android-tablet-users.md#main-pars_header_1451175907).

**Aanwezigheid markeren met behulp van QR-code**

Gebruik QR Scan Code om uw aanwezigheid voor klassikale sessies te markeren met uw mobiele apparaten.

**Docentrol**

Learning Manager introduceert nu docenten voor modules. Docenten kunnen modulesessies beheren, inclusief de tijd, locatie en plaatslimiet voor de modules die aan hen zijn toegewezen.

Zie voor gedetailleerde informatie over docenten  [Docenten in Leermanager](../instructors/feature-summary/getting-started.md#main-pars_header).

**Collega-account**

Als beheerder kunt u collega-accounts maken waarmee u uw gekochte plaatsen kunt delen.

Zie voor meer informatie over het maken en beheren van collega-accounts  [Collega-accounts](../administrators/feature-summary/peer-account.md#main-pars_text).

**Cursusequivalentie-aanbod**

Gebruik **[!UICONTROL Nieuwe taal toevoegen]** wanneer u een module of cursus toevoegt om deze beschikbaar te maken in meerdere talen en in verschillende indelingen.

**Studenttranscript**

Learning Manager biedt managers en beheerders de mogelijkheid om transcriptgegevens te downloaden om de leergeschiedenis van zowel individuen als teams bij te houden.

**Integratie met andere contentproviders**

Learning Manager heeft drie nieuwe connectoren in deze release geïntroduceerd, zodat studenten cursussen van de volgende contentproviders kunnen openen en volgen: Lynda.com, getAbstract en Harvard ManageMentor.

Om te weten te komen hoe te om elk van deze schakelaars te vormen en te gebruiken, zie  [Connectoren](../integration-admin/feature-summary/connectors.md#main-pars_header).

**Unieke id voor leerobjecten**

Tijdens het maken van leerobjecten kunnen auteurs en beheerders nu unieke id&#39;s opgeven voor de cursussen, leerprogramma&#39;s of certificeringen. Als u een unieke id wilt inschakelen bij het maken van een leerobject, klikt u op Instellingen > Algemeen. Schakel het selectievakje Inschakelen in naast de optie Unieke ID&#39;s voor leerobjecten.

**Discussieboard voor studenten**

Gebruik het Discussieboard in cursussen om met uw collega&#39;s en docenten te communiceren. Als student kunt u alle berichten voor cursussen bekijken. U kunt echter ook alleen de berichten verwijderen die u hebt ingevoerd. Zie voor meer informatie over het Discussieboard  [Weergeven van en deelnemen aan discussies](../learners/feature-summary/courses.md#main-pars_header_1772461149).

### Verbeteringen {#Enhancements-3}

**X van Y cursussen**

De voltooiingscriteria voor leerobjecten zoals cursussen, certificeringen en leerplannen kunnen zo worden ingesteld dat studenten slechts X van Y modules of cursussen hoeven te voltooien. Auteurs kunnen ook de voltooiingscriteria voor certificeringen en leerplannen instellen.

Zie voor meer informatie over deze functie  [Voltooiingscriteria voor cursussen](../learners/feature-summary/courses.md#main-pars_image_1164377098).

**Cursusmoderatie**

Beheerders ontvangen nu meldingen wanneer een auteur modules bewerkt of bijwerkt en een cursus opnieuw publiceert.

**Beheerdersinstellingen voor het herstellen van modules**

Beheerders kunnen nu de optie Module herstellen configureren zodat studenten een niet-succesvolle of een niet-voltooide cursus opnieuw kunnen instellen.

**Rapportcatalogus**

Wanneer u rapporten maakt in Leerbeheer, kunt u nu rapporten en grafieken voor catalogi genereren.

**Verbeteringen van leerplannen**

Beheerders kunnen nu leerplannen maken van het type Op datum. Met het leerplan Op datum kan een beheerder de naam van de gebeurtenis opgeven, de datum voor de gebeurtenis kiezen en de gebruikersgroep selecteren waartoe de gebeurtenis behoort.

**Cursusspecifieke inschrijvingsberichten**

Beheerders kunnen nu cursusspecifieke inschrijvingsberichten configureren en verzenden via e-mail naar studenten.

**Vaste aankondigingen**

Als beheerder kunt u nu de functie Sticky inschakelen voor aankondigingen.

**Ondersteuning voor URL in aankondigingen**

U kunt URL&#39;s toevoegen als aankondigingen door de URL in HTML toe te voegen.

**Nieuwe leveringstypen toevoegen (cursussen)**

Met Adobe Learning Manager kunt u nu leveringstypen voor uw cursussen toevoegen.

**Verbeteringen in auteursrol**

Eerdere auteurs konden alleen modules en cursussen maken. Auteurs kunnen nu ook certificeringen en leerprogramma&#39;s voor studenten maken.

**Auteursrol voor externe gebruikers**

Als beheerder kunt u nu auteursrollen toewijzen aan externe gebruikers.

**Meerdere auteurs**

Met Learning Manager kunnen meerdere auteurs nu tegelijkertijd dezelfde inhoudsgroep bewerken.

**Verbeteringen voor Adobe Connect**

U kunt nu één Adobe Connect-URL configureren met meerdere Learning Manager-accounts.

**Ondersteuning voor nieuwe talen**

Ondersteuning voor Japans, Braziliaans Portugees en Italiaans is beschikbaar vanaf deze release.



+++

+++Update 28

Releasedatum: 30 januari 2017.

### Opgeloste problemen {#IssuesFixed-6}

#### Accountinstellingen {#accountsettings}

Wanneer u als beheerder op Extern profiel klikt en Acties > Profiel wijzigen kiest, worden niet alle profielen weergegeven. Dit probleem is nu opgelost.

#### Levenscyclus van cursus {#courselifecycle}

* Wanneer u een cursus start die is gemaakt met het e-learningprogramma van de Biz-bibliotheek, werkte de actie &quot;Hervatten&quot; niet. Dit probleem is opgelost.
* Sommige gebruikers konden een cursus niet starten in iPad via de cursuskoppeling in Aankondigingen. Dit is nu opgelost.
* Wanneer u op de knop Doorgaan in het programma van de student klikt, hebt u de cursussen niet op volgorde kunnen openen. Dit is nu opgelost.
* Het label Cursusoverzicht voor cursussen in het programma van de student was eerder misplaatst. Dit probleem is nu opgelost.

#### Learner-app {#learnerapp}

* Als u op uw apparaat een aankondigingsafbeelding opent in de modus Volledig scherm, kunt u niet teruggaan naar de toepassing. Dit is nu opgelost.
* Tincan-inhoud die vanuit de Captivate is geüpload, kon niet worden afgespeeld in de online modus van Android- en iOS-besturingssystemen. Dit probleem is opgelost.

#### Cursusrapporten {#coursereports}

Er worden onjuiste studenttranscriptrapporten gegenereerd in Learning Manager wanneer de cursus meerdere versies van modules heeft. Dit is nu opgelost.

#### API-laag {#apilayer}

Er treedt een fout op wanneer u de informatie over de moduleversie probeerde op te halen met behulp van AP/cursussen/{coursesid}. Dit is nu opgelost.

+++

+++Update 27

Releasedatum: 23 december 2016.

### Nieuwe functies {#Newfeatures-1}

Adobe stelt ondernemingen in staat om de trainingsgegevens en trainingsinhoud van hun organisatie van hun bestaande LMS-systemen (Learning Management Systems) naar de LMS-toepassing van Learning Manager te migreren.

Learning Manager biedt de tools en sjablonen waarmee de integratiebeheerder van uw organisatie de migratietaken kan instellen en uitvoeren.

Raadpleeg voor meer informatie over de functie Migratie  [Help bij Migratiehandleiding](../integration-admin/feature-summary/migration-manual.md)

### Verbeteringen {#Enhancements-4}

**Gebruikersregistratie**

Als beheerder kunt u nu specifieke domeinnamen toevoegen terwijl u externe gebruikers toevoegt. Wanneer studenten zich bij het account registreren, kunnen ze alleen e-mailadressen uit die domeinnamen invoeren.

U kunt ook e-mailverificatiekoppelingen naar het e-mailadres van gebruikers sturen wanneer gebruikers zich bij het account registreren. Zie voor meer informatie over deze verbetering  [Gebruikers/gebruikersgroepen toevoegen](../administrators/feature-summary/add-users-user-groups.md#main-pars_header_1217981931).

**Fluidic Player**

Met Fluidic Player kunt u nu de afspeelsnelheid wijzigen. U kunt kiezen uit vijf beschikbare snelheidsvarianten. Met Fluidic Player kunt u ook de volume-instellingen bepalen wanneer u een cursus volgt.

Als student kunt u ook 10 seconden vooruit of achteruit springen met de nieuwe pictogrammen aan weerszijden van de afspeelknop in de Fluidic Player. Zie voor meer informatie over deze verbeteringen  [Fluidic Player](../learners/feature-summary/fluidic-player.md).

De verbeteringen in Fluidic Player zijn alleen van toepassing op video.

+++

+++Update 26

Releasedatum: 6 december 2016.

### Verbetering {#enhancement}

Als onderdeel van deze update biedt Learning Manager een eindpunt [PATCH/gebruikers/{id}](<https://learningmanager.adobe.com/docs/Learning> Managerapi/v1/#!/user/patch_users_id) om gebruikers in een toepassing bij te werken. U hebt toegang tot dit API-eindpunt in de beheerdersrol. Met****dit eindpunt kunt u de volgende informatie over gebruikers van Learning Manager bijwerken:

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

Met de functie Gedeelde catalogus kunnen beheerders van verschillende accounts catalogi met leerobjecten delen of aanschaffen. Als uitbreiding op deze functie voor gedeelde catalogi ondersteunen we het doorgeven van de updates naar leerobjecten zoals badges, vaardigheden, modules, cursussen, leerprogramma&#39;s, certificeringen en taakhulpen.

Raadpleeg voor meer informatie over deze functie  [Help voor gedeelde catalogi](../administrators/feature-summary/catalogs.md#propagation)

**L1- en L3-feedback**

* Het dialoogvenster L1-feedback verschijnt zodra een student het cursusgebruik heeft voltooid. De student ontvangt ook een melding over het voltooien van L1-feedback.
* In de L1- en L3-feedbackfunctie is een optie voor het toevoegen van beschrijvende vragen geboden. Beheerders kunnen deze beschrijvende vragen aan studenten toevoegen. Deze voorziening is een aanvulling op de standaardset vragen van de Learning Manager. U kunt twee beschrijvende vragen toevoegen voor L1-feedback en één beschrijvende vraag voor L3-feedback.\
  Raadpleeg voor meer informatie over deze functie [Help voor beschrijvende vragen over L1- en L3-feedback](../administrators/feature-summary/courses.md#descriptive)

**Gebruikers exporteren**

* Op verzoek van een aantal grote zakelijke gebruikers is een nieuwe optie beschikbaar om de lijst van alle gebruikers in het Leerbeheeraccount te downloaden. Klik in Beheerdersaanmelding op **[!UICONTROL Gebruikers]** in het linkerdeelvenster en klik op **[!UICONTROL Gebruikersgegevens exporteren]** om de lijst met gebruikers als Excel-blad te downloaden.

### Opgeloste problemen {#Issuesfixed-1}

**Cursusinschrijvingen**

* Wanneer een beheerder cursusinschrijvingen probeerde te bekijken via het tabblad Studenten, verschenen sommige namen van ingeschreven studenten niet. Dit probleem is opgelost.

**Cursussen toevoegen**

* Als een auteur tijdens het toevoegen van een vaardigheid aan de cursus een vaardigheid toevoegde die aan het einde van de naam een lege ruimte heeft, trad er een fout op en werd de cursus niet opgeslagen. Dit probleem is opgelost.

**Cursussen volgen**

* Sommige studenten konden tijdens het volgen van een cursus niet van de ene module naar de andere gaan omdat de modules niet als voltooid werden gemarkeerd. Dit probleem is opgelost.
* In een geordende cursus konden studenten niet navigeren tussen de modules in de inhoudsopgave tijdens de normale modi en de revisiemodi. Dit probleem is opgelost.

**Fluidic Player**

* Wanneer een gebruiker module-inhoud met verborgen frames/dia&#39;s uploadde, werden de verborgen frames/dia&#39;s soms weergegeven in de inhoudsopgave in het linkerdeelvenster. Dit probleem is opgelost.

**Rapporten**

* De tijd die nodig is om rapporten te laden, is hoger in de nieuwste update van Learning Manager. Dit probleem is opgelost.

+++

+++Update 24

Releasedatum: 12 oktober 2016.

### Verbeteringen {#Enhancements-6}

**Cursusrapporten**

* Voor UUID-accounts (Universal Unique Identifier) die zijn ingeschakeld voor Learning Manager, verschijnt de UUID in het inschrijvingsrapport van de cursus, studenttranscripten en quizscorerapporten.

### Opgeloste problemen {#Issuesfixed-2}

**Taakhulpen**

* Wanneer een student probeerde te navigeren van Leermateriaal>Taakhulpen naar Leermateriaal>Cursussen, werden cursussen soms niet geladen zoals verwacht op het tabblad Leermateriaal>Cursussen. Dit probleem is opgelost.

**Gebruikers toevoegen**

* Wanneer één gebruiker wordt toegevoegd aan de toepassing van de Learning Manager, ontvangt de gebruiker soms geen e-mailmelding. Dit probleem is opgelost.
* Beheerders kunnen het CSV-bestand niet downloaden als het uploadproces voor CSV mislukt. Dit probleem is opgelost. Beheerders kunnen de nieuwste CSV downloaden, zelfs als het uploadproces voor CSV mislukt.
* Als een CSV wordt geïmporteerd nadat gebruikersgegevens die zichzelf hebben geregistreerd, zijn gewijzigd in hoofdletters en kleine letters, worden de zelfgeregistreerde gebruikersgegevens niet weergegeven in de gebruikersinterface van de beheerder. Dit probleem is opgelost.

**Cursusrapporten**

* In sommige gevallen werden quizscores niet weergegeven voor cursussen, ook al worden de scores weergegeven in studenttranscripten. Dit probleem is opgelost.

**Inschrijvingsrapporten**

* In sommige gevallen werden de Excel-inschrijvingsrapporten van de student niet gedownload voor de leerobjecten. Dit probleem deed zich voor wanneer niet-ASCII- of speciale tekens werden gebruikt in de naam van leerobjecten. Dit probleem is opgelost.

**Gebruikersaanmelding**

* Tijdens het instellen van een wachtwoord tijdens de registratie of tijdens het opnieuw instellen, werd het foutbericht niet weergegeven, ook al wordt het ingevoerde wachtwoord niet in overeenstemming gebracht met het wachtwoordbeleid. Dit probleem is opgelost.

**Cursuseffectiviteit**

* In de studentrol werd de effectiviteit van de cursus weergegeven als een van de **Sorteren op** filteropties, zelfs als een beheerder de cursuseffectiviteit voor studenten heeft uitgeschakeld. Dit probleem is opgelost.

**Certificeringen**

* Wanneer een beheerder studenten uit een terugkerende certificering verwijderde, trad er een fout op en hing de toepassing Learning Manager op. Dit probleem is opgelost.

**Rapporten**

* Wanneer een beheerder een certificeringsrapport probeert te genereren met **Einddatum** als optie, werden de inactieve gebruikers niet getoond in het rapport. Dit probleem is opgelost.
* Wanneer een beheerder op de koppeling Cursusrapporten klikte op het tabblad Rapporten>Mijn rapporten, verscheen een pop-upvenster zonder de knop Sluiten. Dit probleem is opgelost.

**Fluidic Player**

* Wanneer een gebruiker de modus Volledig scherm kiest in Fluidic Player terwijl hij een voorvertoning weergeeft van cursussen als beheerder of auteur, wordt het scherm leeg weergegeven. Dit probleem is opgelost.

**Ondersteuning voor meerdere talen**

* In reactie op API-aanroepen van gebruikers verschenen vraagtekens in plaats van Chinese tekens. Dit probleem is opgelost.

**API-laag**

* Er trad een fout op wanneer een gebruiker de standaard catalogus-id probeerde op te halen met behulp van get/catalog/catalog ID API. Een standaardcatalogus-id kan vergelijkbaar zijn met &#39;970_default&#39;. Dit probleem is opgelost.

**Gebruikersinterface**

* Enkele kleine typfouten zijn gecorrigeerd in de gebruikersinterface van de Learning Manager-toepassing voor de studentrol.

+++

+++Update 23

Releasedatum: 19 september 2016.

### Opgeloste problemen {#Issuesfixed-3}

**Studenttranscripten**

* Als er meer dan twintig inactieve/verwijderde studenten in een account zaten, werden de inactieve studenten boven twintig niet weergegeven in de vervolgkeuzelijst met zoekopdrachten van het dialoogvenster Studenttranscript. Dit probleem is opgelost.
* Als een extern gebruikersaccount is verlopen, zijn de studenten niet vermeld in het gegenereerde studenttranscript. Dit probleem is opgelost.

**Catalogi**

* Sommige klanten ondervonden een probleem met de weergave van gebruikersgroepen in een catalogus. Zelfs als een catalogus meer dan twintig gebruikersgroepen bevat, werden er slechts twintig gebruikersgroepen weergegeven. We hebben dit probleem opgelost door 200 gebruikersgroepen op een pagina weer te geven.

+++

+++Update 22

Releasedatum: 13 september 2016.

In deze update-release hebben we enkele back-endproblemen met productengineering opgelost om de klantervaring te verbeteren.

### Opgeloste problemen {#Issuesfixed-4}

* Er is een probleem opgetreden met het exporteren van modulegegevens in studenttranscripten, met als gevolg onjuiste exportgegevens. Dit probleem is opgelost.
* Als een gebruiker een e-mail-ID-extensie met meer dan vier tekens gebruikt, wordt deze niet ondersteund. Als een e-mail-ID bijvoorbeeld <abcd@company.world> het werd niet ondersteund omdat de extensiewereld uit meer dan vier tekens bestaat. We hebben dit opgelost om de extensie te ondersteunen met meer dan vier tekens.

+++

+++Update 21

Releasedatum: 1 september 2016.

### Verbeteringen {#Enhancements-7}

**Cursuseffectiviteit**

Beheerders kunnen nu de effectiviteitsfunctie van de cursus of het leerprogramma aanpassen om de effectiviteitsscore voor studenten te verbergen.

**Externe gebruikers toevoegen**

Learning Manager heeft de maximumlimiet voor externe zelfregistraties verhoogd tot 5 cijfers.

**Rapporten**

Alle gedownloade rapporten en studentenlijsten voor alle leerobjecten geven nu verwijderde gebruikers weer met een duidelijke afbakening voor verwijderde gebruikers.

### Opgeloste problemen {#Issuesfixed-5}

**Levenscyclus van cursus**

Wanneer een auteur een gedeelde cursus bewerkte om gewijzigde module-informatie bij te werken, verscheen soms een waarschuwingsbericht dat de gebruiker deze niet kon bewerken omdat eerdere wijzigingen werden verwerkt. Dit probleem is opgelost.

**Ondersteuning voor meerdere talen**

In sommige functies van de gebruikersinterface van Learning Manager werden de berichten niet vertaald en weergegeven in de juiste landinstellingen. Dit probleem is opgelost.

**Gebruikers toevoegen**

* Wanneer een verwijderde gebruiker weer als één gebruiker wordt toegevoegd, is de gebruiker niet standaard toegevoegd aan de gebruikersgroep &#39;alle gebruikers&#39;. Dit probleem is opgelost.
* Een beperkt aantal profielen verscheen in de dialoogvensters voor het wijzigen van het externe aanmeldings- en zelfinschrijvingsprofiel. Paginering is nu geïmplementeerd.

**Taakhulpen**

Wanneer een student het tabblad Taakhulpen in het studentaccount opende, verscheen een foutbericht als &#39;Deze taakhulp staat niet meer in uw lijst&#39; voordat de inhoud werd geladen. Dit probleem is opgelost.

**Catalogi**

Tijdens het maken van de catalogus werkte het filter Sorteren op niet zoals verwacht terwijl cursussen als inhoud aan de catalogus werden toegevoegd. Dit probleem is opgelost.

**Instellingen**

Wanneer een beheerder een subdomein gebruikte dat al door een ander account werd gebruikt, verscheen in accountinstellingen geen foutbericht aan de beheerder. Dit probleem is opgelost.

**API-laag**

* Wanneer include manager wordt gebruikt terwijl het halen van gebruikers, werd volledige hiërarchie van managers opgehaald in plaats van de directe manager van de gebruiker. Dit probleem is opgelost.
* Wanneer een gebruiker met autorisatiemachtigingen voor het bereik van de student gebruikers probeerde toe te voegen, verscheen er een algemeen foutbericht. Dit probleem is opgelost en de student ziet nu een onbevoegd toegangsbericht.
* Wanneer een gebruiker een laatste bestaande gebruiker in een gebruikersgroep probeerde te verwijderen, werd een foutbericht van 204 weergegeven aan de gebruiker. Dit probleem is nu opgelost door een relevante foutmelding weer te geven waarin staat dat de groep ten minste één gebruiker moet hebben.
* De ruimte, indien aanwezig aan het begin van de naam, is bijgesneden tijdens het weergeven van de gebruikersnaam in de GET/gebruikers-API. Dit is nu opgelost.
* De conceptcursussen werden ook geretourneerd als beheerder alle cursussen probeerde op te halen. Deze conceptcursussen moeten privé zijn voor de auteur. Dit probleem is opgelost, conceptcursussen worden nu niet meer geretourneerd.

**Adobe Connect-integratie**

* In sommige op Adobe Connect gebaseerde virtuele klassikale sessies werd de aanwezigheid niet automatisch gemarkeerd na de sessie. Dit probleem deed zich alleen voor wanneer een aanmeldings-ID door de docent werd gebruikt om zich aan te melden in plaats van een e-mail-ID. Het is nu opgelost.
* In sommige gevallen verscheen de naam van de docent meerdere keren in de vervolgkeuzelijst Docent tijdens het maken van de op Adobe Connect gebaseerde virtuele klassikale module. Dit probleem is opgelost.

+++

+++Update 20

Releasedatum: 22 augustus 2016.

### Verbeteringen {#Enhancements-8}

**API-laag**

Als onderdeel van deze update hebben we de volgende nieuwe API&#39;s toegevoegd om te voldoen aan een aantal van onze klantvereisten:

1. POST Users
1. DELETE Users
1. GET userGroups
1. GET-gebruikersgroepen /{id}
1. DELETE-gebruikersgroepen /{id}/Users
1. POST userGroups /{id}/Users
1. GET /users/userId/userGroups

We hebben ook het bestaande gebruikersmodel uitgebreid met de volgende toevoegingen:

1. Managermodel is toegevoegd als relatie met gebruikersmodel
1. userGroupId wordt toegevoegd als een nieuwe parameter aan GetUsers

**Studenttranscript**

Wanneer een gebruiker een studenttranscript voor een student genereerde, verscheen het pop-upvenster voor een zeer korte tijd en verdween het zonder dat de gebruiker om actie werd gevraagd. We hebben de gebruikerservaring verbeterd door een pop-up op te geven die pauzeert en de gebruiker vraagt op OK te klikken.

**Adobe Connect-integratie**

De aanmeldings-id wordt opgegeven als een nieuw optioneel veld in de Adobe Connect-integratie-instellingen voor gebruikers die zich niet met hun e-mail-ID aanmelden.

### Opgeloste problemen {#Issuesfixed-6}

**Cursusrapporten**

* Wanneer een cursusmodule uit open vragen of alleen enquêtevragen bestond, verscheen een leeg quizscorerapport toen het werd geëxporteerd. Dit probleem is opgelost.
* In sommige gevallen werd het quizscorerapport niet gedownload wanneer een gebruiker de koppeling Quizscore exporteren gebruikte. Dit probleem is opgelost.

**Cursussen maken**

De pagina Cursusinstellingen in de auteursrol werd niet weergegeven wanneer een vaardigheid die aan die cursus is gekoppeld, door de beheerder is gearchiveerd. Dit probleem is opgelost.

**Slimme inschrijving**

Het zoekveld ondersteunt geen speciale tekens als invoer, zodat de zoekresultaten niet worden weergegeven. Dit probleem is opgelost.

+++

+++Update 19

Releasedatum: 11 augustus 2016.

### Verbeteringen {#Enhancements-9}

**Slimme inschrijving**

De prestaties van de zoekmachine zijn verbeterd, zodat gebruikers nauwkeuriger zoekresultaten krijgen.

**Adobe Connect-integratie**

Het verificatie-/authenticatieproces van de integratieaanvraag is verbeterd in de toepassing Learning Manager.

### Opgeloste problemen {#Issuesfixed-7}

**Gebruikers toevoegen**

* Wanneer er een groot aantal gebruikers van de leermanager zijn, was er een vertraging in het laden van gebruikers en gebruikersgroeppagina. Dit probleem is opgelost.
* Nadat de beheerder het CSV-bestand met nieuwe gebruikers heeft geüpload, werd de lijst met gebruikers op de pagina pas bijgewerkt met nieuwe gebruikers nadat de pagina was vernieuwd. Dit probleem is opgelost.
* Soms werd na het importeren van gebruikers met behulp van CSV de waarde van de gebruikers-id op de pagina vervangen door e-mail-ID. Dit probleem is opgelost.

**Gebruikersgroepen maken**

In sommige gevallen werd het aantal gebruikers niet weergegeven op de standaardpagina voor gebruikersgroepen in Leerbeheer. Dit probleem is opgelost.

**Studenttranscript**

Kenmerkwaarden van actieve velden werden onjuist weergegeven in studenttranscripten voor Certificeringen. Dit probleem is opgelost.

**Delen van meerdere accounts**

In een scenario waarin een accountbeheerder een cursuscatalogus met de ontvanger deelde en later een test- of voorwerkmodule bijwerkte, werd de inhoud van de voorwerk- of testmodule gebruikt om af te spelen in de inhoudsmodule voor de ontvanger. Dit probleem is opgelost.

**Thema&#39;s en branding**

Wanneer een beheerder een thema in de toepassing wijzigt met de widget Live voorvertoning en van rol verandert, functioneert de widget Live voorvertoning niet zoals verwacht in een nieuwe rol. Dit probleem is opgelost.

**Ondersteuning voor meerdere talen**

Wanneer een beheerder de landinstelling van de toepassing wijzigt in Vereenvoudigd Chinees of Spaans, werden sommige menu-inhoud in het linkerdeelvenster, online instructies en pop-upberichten niet weergegeven in betekenisvolle woorden of zinnen. Dit probleem is opgelost.

**Fluidic Player**

* Wanneer een auteur een cursus maakt met AICC- of Tin Can-inhoud en een voorvertoning van de inhoud probeert te bekijken, wordt de inhoud niet afgespeeld. Dit probleem is opgelost.
* Modulevoorbeeld functioneert niet tijdens het maken van een cursus of tijdens het bewerken van de cursus door een auteur. Dit probleem is opgelost.

**Catalogi**

Wanneer een student rechtstreeks in de browser toegang probeerde te krijgen tot de URL van catalogi/leerprogramma&#39;s, werd deze omgeleid naar cursussen. Dit probleem is opgelost.

**Salesforce-integratie**

* Nadat een Salesforce- of FTP-verbinding tot stand was gebracht, werden op de pagina Kenmerken toewijzen de vervolgkeuzepijlen voor de velden niet weergegeven in de browsers IE, Edge en Safari. Bovendien werden sommige pop-upberichten niet weergegeven in de workflows. Dit probleem is opgelost.
* In sommige gevallen, wanneer een beheerder probeerde om de .csv ingevoerde gegevens in de schakelaar van FTP te synchroniseren, mislukte de synchronisatie met herhaalde ingangen. Dit probleem is opgelost.

**API-laag**

* Wanneer een beheerder de externe student autoriseert met OAuth-verificatie, konden de externe studenten zich soms niet aanmelden bij de toepassing. Dit probleem is opgelost.
* Wanneer er een API-aanroep is voor taakhulpen van studenten, werd soms een onbevoegde toegangsfout weergegeven. Dit probleem is opgelost.

**Instellingen**

Wanneer op de pagina Gegevensbronnen een automatische planningstijd wordt ingesteld en opgeslagen, wordt deze soms teruggezet naar de oude status. Dit probleem is opgelost.

**Rapportage van gebruikersgroepen**

Waarden van gebruikersgroepen in filter werden niet ingevuld wanneer het rapporttype als Aangepast werd gekozen. Dit probleem is opgelost.

**Adobe Connect-integratie**

Onjuiste titel verscheen voor Adobe Connect-integratie nadat de verbinding was voltooid. De tekst van de paginakoptekst wordt gecorrigeerd.

**Rapporten**

Zelfs als de optie Gegevens voor huidige waarden weergeven is geselecteerd, worden de meest recente gegevens niet weergegeven in de rapporten. Dit probleem is opgelost.

+++

+++Update 18

Releasedatum: 31 juli 2016.

## Nieuwe functies en verbeteringen {#newfeaturesandenhancements}

Raadpleeg voor een lijst met nieuwe functies en verbeteringen in de release van Leermanager van juli de [Nieuwe functies](../whats-new.md).

Hieronder vindt u een aantal van de verbeteringen ter referentie.

**Studenttranscript**

Leerbeheer biedt u een functie om transcripten te genereren voor de studenten van de Learning Manager van uw organisatie. Raadpleeg voor meer informatie  [Help-inhoud van de functie Studenttranscripten](../administrators/feature-summary/learner-transcripts.md).

**Badge exporteren als PDF**

Met Learning Manager kunt u uw badges exporteren als PDF-bestanden. Raadpleeg voor meer informatie  [Inhoud van badges](../administrators/feature-summary/badges.md).

**Quizscore voor modules**

U kunt quizscore toevoegen voor de modules Lesruimte, Virtuele lesruimte en Activiteiten.

**Gebruikers toevoegen**

* U kunt studenten van de ene zelfregistratiegroep naar de andere verplaatsen.
* U kunt gebruikers van de ene externe groep naar de andere externe groep verplaatsen.
* U kunt een gebruiker van een externe groep maken als manager van dezelfde externe groep.
* Nadat u een externe gebruikersgroep aan Leermanager hebt toegevoegd, kunt u het registratieproces voor externe gebruikers ook pauzeren. U kunt de blokkering (pauzeren) op elk gewenst moment opheffen door de optie Hervatten te kiezen.
* U kunt nu de naam en de e-mail-ID van de studenten bewerken.

**Zelfinschrijving**

Studenten kunnen zich ook uitschrijven voor leerobjecten zoals een cursus, leerprogramma of certificering. Studenten kunnen zich echter niet van een leerobject uitschrijven nadat ze een leerobject hebben voltooid.

**Leerobjecten gebruiken**

Beheerders kunnen een leeractiviteit van studenten nu als voltooid markeren.

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

Wanneer er een groot aantal gebruikers van de leermanager zijn, was er een vertraging in het laden van gebruikers en gebruikersgroeppagina. Dit probleem is opgelost.

**Gebruikersgroepen maken**

In sommige gevallen werd het aantal gebruikers niet weergegeven op de standaardpagina voor gebruikersgroepen in Leerbeheer. Dit probleem is opgelost.

+++

+++Update 16

Releasedatum: 10 juni 2016.

## Probleem opgelost {#Issuefixed-1}

Sommige klanten ondervonden problemen bij het gebruik van de functie Single Sign-On in Learning Manager. Dit probleem is opgelost door de entityId van de leermanager naar een URL te verwijzen (<https://learningmanager.adobe.com>) in plaats van een trefwoord. Learning Manager voldoet aan de SAML 2.0-specificatie.

+++

+++Update 15

Releasedatum: 25 mei 2016.

### Verbeteringen {#Enhancements-10}

**Certificeringen/leerprogramma&#39;s**

* In de inschrijvingslijst voor certificeringen en leerprogramma&#39;s voor studenten wordt de volledige naam (voor- en achternaam) van de studenten weergegeven. Eerder verscheen alleen de voornaam van de studenten.
* Vaardigheden met het hoogste niveau worden beschouwd uit de lijst met cursussen in certificeringen/leerprogramma&#39;s en worden op kaarten weergegeven als certificatie/leerprogrammavaardigheid. Als er meerdere cursussen met dezelfde aftitelingswaarde zijn, worden deze in alfabetische volgorde opgehaald. Eerder werden de vaardigheidsnamen voor certificatie-/leerprogramma&#39;s willekeurig gekozen uit een lijst van de respectieve cursussen.

**CSV importeren**

Voor de functie voor automatisch uploaden van CSV via FTP ontvangen beheerders e-mailmeldingen als er een fout is opgetreden in het uploaden van CSV.

**Externe partners toevoegen**

Wanneer externe studenten de registratiepagina bezoeken met een URL van een extern profiel, wordt de naam van het externe profiel weergegeven op de registratiepagina voor een betere identificatie.

### Opgeloste problemen {#Issuesfixed-9}

**Cursussen voorvertonen en publiceren**

* Als u in de auteursrol een voorvertoning weergeeft van een cursus die vanuit de Captivate is geüpload als SCORM+SWF-inhoud met `code $$cpQuizInfoStudentName$$` variabele, null-waarde weergegeven voor variabele. Dit probleem is opgelost.
* Wanneer een apostrof (&#39;) van een Presenter-cursus met een titel in Leermanager werd gepubliceerd en weergegeven, werden vraagtekens (???) in de inhoudsopgave weergegeven. Dit probleem is opgelost.

**Certificeringen**

* Als een certificering aan een catalogus is gekoppeld en de certificering terugkeert, wordt deze in alle bijbehorende catalogi weergegeven. Eerder konden gebruikers de terugkerende certificeringen soms niet in hun catalogi bekijken.
* Als een beheerder tijdens het maken van certificeringen de **dagen om te voltooien** een waarde die groter is dan of gelijk is aan de geldigheidsperiode van de certificering, wordt een waarschuwingsbericht weergegeven. Eerder werd het waarschuwingsbericht niet weergegeven aan de beheerders.
* De certificering **geldigheid** wordt weergegeven aan gebruikers in maanden. Eerder verscheen de basiswaarde in jaren.

**Leerprogramma&#39;s definiëren**

De deadline verschijnt niet voor standaardleerprogramma-instanties. Eerder verscheen een vooraf gedefinieerde deadline die mogelijk niet relevant was voor gebruikers.

**Cursussen maken met modules**

* Wanneer een auteur een module van een gemengde cursus bijwerkte, verscheen de aanwezigheidspagina niet in beheerdersrol. Dit probleem is opgelost.
* Wanneer de naam van een cursusinstantie een dubbele punt (:) bevat, is de exporthandeling voor de studentenlijst mislukt. Dit probleem is opgelost.

+++

+++Update 14

Releasedatum: 4 mei 2016.

### Verbeteringen {#Enhancements-11}

**Catalogi**

Wanneer een student toegang krijgt tot de catalogus, verschuift de standaardfocus tussen tabbladen op basis van de beschikbaarheid van leerobjecten, in de volgende volgorde: 1. Cursussen 2. Programma&#39;s 3. Certificeringen en 4. Taakhulpen. Als de cursussen bijvoorbeeld niet beschikbaar zijn op het tabblad Cursussen voor die student, verschuift de focus naar het volgende leerobject, namelijk Programma&#39;s, als er leerprogramma&#39;s zijn.

**Accountinstellingen**

In het bevestigingsvenster van de deactivering van het account wordt een feedbackoptie weergegeven wanneer een beheerder ervoor kiest om een account te deactiveren.

### Opgeloste problemen {#Issuesfixed-10}

**Rapporten exporteren**

* Exporteren van studentenlijst mislukte wanneer een grote groep gebruikers was ingeschreven voor een leerprogramma. Dit probleem is opgelost.
* Wanneer een cursus twee instanties met dezelfde naam heeft en de naam van de instantie lang is, zijn er geen werkbladen gemaakt in het geëxporteerde Excel-bestand. Dit probleem is opgelost.

**Bulkinschrijving**

Wanneer een groot aantal studenten voor leerobjecten zoals leerprogramma&#39;s, cursussen, certificeringen, taakhulpen en leerplannen werd ingeschreven, mislukte de inschrijving. Dit probleem is opgelost.

+++

+++Update 13

Releasedatum: 20 april 2016.

### Opgeloste problemen {#Issuesfixed-11}

**Cursussen maken met modules**

Wanneer module-inhoud met een lange bestandsnaam werd geüpload, waren er problemen met de weergave van knoppen. De opties voor het uploaden en verwijderen van de module functioneerden niet zoals verwacht. Dit probleem is opgelost.

**CSV importeren**

Op verzoek van Amerikaanse klanten is de tijd voor automatisch uploaden via FTP veranderd van middernacht GMT in middernacht PST.

**Rapporten exporteren**

Exporteren van inschrijvingsgegevens mislukte als een van de ingeschreven studenten na het volgen van de cursus wordt verwijderd. Dit probleem is opgelost.

**E-mailsjablonen**

* Het woord **partners,** die werd gebruikt om externe groepen te vertegenwoordigen,**** is **** verwijderd uit de hoofdtekst en titel van e-mailsjablonen. Externe groepen worden niet noodzakelijkerwijs partners genoemd.\
  **Opmerking:** Deze bijgewerkte sjabloon wordt niet weergegeven als de standaardsjabloon al is gewijzigd. Klik op **Origineel herstellen** in **Sjabloonvoorbeeld** in.

* Er kan niet op de URL worden geklikt in het e-mailbericht dat Beheerders altijd ontvangen **Profiel gemaakt (zelfregistratie)** en **Profiel gemaakt (extern/partners)** e-mailsjablonen worden bewerkt. Dit probleem is opgelost.

+++

+++Update 12

Releasedatum: 7 april 2016.

### Verbeteringen {#Enhancements-12}

**Taakhulpen**

Maak taakhulpen met een URL. U kunt alleen een URL-naam vermelden in de workflow voor het maken van taakhulp en taakhulp maken als u bestaande online inhoud wilt gebruiken als taakhulp.

**Studenten toevoegen**

U mag gegevens van één gebruiker bewerken, zoals naam, e-mail, profiel en naam van manager. Alle overeenkomstige gebruikersgroepen worden bijgewerkt met de meest recente gebruikersgegevens.

**Rapporten exporteren**

Naam van manager, naam van leerobject en door de gebruiker gedefinieerde kolommen met niet-unieke waarden uit CSV worden toegevoegd aan de geëxporteerde studentenlijst voor leerobjecten. Eerder verschenen alleen de basisgegevens van studenten zoals naam, datum, e-mail en status.

**Externe partners toevoegen**

Externe studenten kunnen zich niet aanmelden bij de toepassing nadat hun account is verlopen. Externe partners kunnen hun accountstatus in de toepassing bekijken.

**Certificeringen**

U kunt certificeringen in maanden verlengen door de waarde in **Geldigheid** veld. Eerder was verlenging van de certificering alleen toegestaan in termen van jaren.

### Opgeloste problemen {#Issuesfixed-12}

**Aankondigingen**

Paginering werkte niet op de pagina Aankondigingen in Beheerdersaanmelding. Dit probleem is opgelost.

**Leerprogramma&#39;s en -plannen**

* Wanneer een student een geordende cursusmodule in een leerprogramma probeerde over te slaan, werd geen foutbericht weergegeven. Dit probleem is nu opgelost. Een foutbericht **Kan modules niet overslaan** wordt weergegeven.
* Cursussen werden niet aan leerprogramma&#39;s toegevoegd wanneer paginering werd gebruikt in de cursuslijst. Dit probleem is opgelost.
* **Gearchiveerd** werd twee keer weergegeven in Leerprogramma&#39;s > Instanties. Dit probleem is opgelost.

**Taakhulpen**

* Wanneer een student taakhulpen uit de **Leren** tab, **Naam** sorteren werkte pas als verwacht nadat de pagina is vernieuwd. Dit probleem is opgelost.

* Als een taakhulp deel uitmaakt van meerdere cursussen, werden de cursussen niet weergegeven in de lijst Taakhulpen. Dit probleem is opgelost.
* Als een student in- of uitzoomde in de browser, werkte de paginering voor de lijst Taakhulpen niet zoals verwacht. Dit probleem is opgelost.

**Cursus volgen**

* Als een student in- of uitzoomde in de browser, werkte de paginering voor cursussen niet zoals verwacht. Dit probleem is opgelost.

**Vaardigheden maken**

In de aanmelding van studenten verschijnt de knopinfo voor vaardigheidsnaam in **Vaardighedenkaart **was** **geeft de***volledige naam niet weer. Dit probleem is opgelost.

**Externe partners toevoegen**

* Er is een tekstbericht opgenomen op de registratiepagina voor externe gebruikers als **Gebruikers moeten zich eerst registreren en een gebruikersnaam-wachtwoord maken voor volgende aanmeldingen**.

**Gebruikersmeldingen**

* Wanneer een externe student op de knop **Notities openen** in E-mailmelding Cursus opnieuw bekijken wordt de speler geopend, maar het deelvenster Notities werkte niet. Dit probleem is opgelost.
* Wanneer een externe student de voorbereidings- of evaluatiemodules probeert te openen met **Notities openen** koppeling in e-mailmelding Cursus opnieuw bekijken. Notitie-inhoud is niet zichtbaar. Dit probleem is opgelost.

**Cursussen maken met modules**

Wanneer een beheerder probeerde studenten in te schrijven voor een blended-cursus die verlopen klaslokaalmodule bevat, werd het inschrijvingsdialoogvenster niet geopend. Dit probleem is opgelost.

**Rapporten exporteren**

Als een vraagtekst meer dan 255 tekens bevat en is ingeschakeld voor de SCORM 1.2-indeling, werkte quizrapportage voor dergelijke vragen niet. Dit probleem is opgelost.

+++

+++Update 11

Releasedatum: 15 maart 2016.

### Opgeloste problemen {#Issuesfixed-13}

**Cursussen met modules maken**

* Wanneer u in Beheerdersaanmelding probeert een nieuwe instantie voor cursussen te maken van **Gearchiveerd** is opgetreden, is een fout opgetreden. Dit probleem is opgelost.
* Bij Beheerdersaanmelding voor gelokaliseerde inhoud werden tijdens het inschrijven van studenten voor de cursusinstantie de acties en de lay-outs voor het inschrijvingsscherm vervormd. Dit probleem is opgelost.
* Wanneer een auteur klassikale of virtuele klassikale modules maakte, verscheen de standaardmaand van de datumkalender als januari 2015. Dit probleem is opgelost en geeft standaard de huidige datum weer.
* Wanneer de naam van een cursusinstantie uit een schuine streep vooruit of achteruit bestond, mislukte de exporthandeling van de studentenlijst. Dit probleem is opgelost.

**Aankondigingen**

Wanneer een student de muis op een videomelding hapte, veranderde de cursor niet in een puntige vinger zoals verwacht. Dit probleem is opgelost.

**Gebruikersmeldingen**

Wanneer een externe student op de knop **Notities openen** koppeling in e-mailmelding Cursus opnieuw bezoeken, werkt niet. Dit probleem is nu opgelost. Deze koppeling opent de speler met notities, zelfs als de gebruiker niet is aangemeld bij Leermanager.

**Ondersteuning voor Frans en Duits**

De Help-URL&#39;s in de CSV-uploadfunctie doorlopen naar de Engelse Help-inhoud. Dit probleem is opgelost.

**Cursussen voorvertonen en publiceren**

Wanneer u een voorvertoning weergeeft van Presenter 10- en 11 TinCan API (SWF/HTML)-inhoud, werkte de inhoud niet in de authoringaanmelding. Dit probleem is opgelost.

**Aanpasbare e-mails**

De titelnamen in e-mailsjablonen waren niet geschikt. De inhoud wordt in deze sjabloontitels bijgewerkt om ze leesbaar te maken.

**Taakhulpen**

In Internet Explorer 11 verscheen de naam en het pictogram van de taakhulp vervormd in de voorvertoning van Auteur en Beheerder. Dit probleem is opgelost.

+++

+++Update 10

Releasedatum: 28 februari 2016.

## Nieuwe functies {#Newfeatures-2}

### Taakhulpen

Taakhulpen is een opslagplaats van trainingsinhoud die zonder enige inschrijvings- of voltooiingscriteria toegankelijk is voor studenten. Studenten kunnen naar deze taakhulpen verwijzen om hulp te krijgen bij het uitvoeren van activiteiten of taken in een organisatie. De beheerder kan het aantal downloads per taakhulp bijhouden.

Raadpleeg voor meer informatie over deze functie  [Help bij taakhulpen](../learners/feature-summary/job-aids.md).

### Aankondigingen

Een aankondiging is een multimediabericht (tekst, afbeelding of video) dat een beheerder kan maken en uitzenden naar een gedefinieerde groep gebruikers. Gebruik aankondigingen om studenten te motiveren om trainingen te volgen en zo een leercultuur op te bouwen.

Raadpleeg voor meer informatie over deze functie  [Help voor aankondigingen](../learners/feature-summary/announcements.md).

### Tin Can API-ondersteuning

Adobe Learning Manager ondersteunt de Tin Can API-specificatie (ook wel Experience API of xAPI genoemd). U kunt Tin Can API-compatibele inhoud uploaden en volgen, net als bij het bijhouden van SCORM- en AICC-inhoud.

Neem voor meer informatie contact op met het ondersteuningsteam van de Adobe.

### Cursusvolgorde

U kunt een leerpad maken door automatisch een vervolgcursus of leeractiviteit toe te wijzen.

Gebeurtenissen voor leerplannen zijn bijgewerkt. Er zijn enkele nieuwe gebeurtenissen toegevoegd. Raadpleeg  [Leerplannen](../learners/feature-summary/learning-programs.md) voor meer informatie.

### Herinnering voor notities

Als u notities maakt terwijl u een cursus volgt, herinnert Leermanager u na 15 dagen door een melding te verzenden om de notities te bekijken.

### gamification op groepsniveau

Beheerders kunnen het bereik van gamification definiëren door de bereikinstellingen te wijzigen. U kunt gamification selectief inschakelen onder vergelijkbare profielgebruikers, groepen of locatie. Raadpleeg  [Gamification](../learners/feature-summary/gamification.md) voor meer informatie.

### Ondersteuning voor Frans en Duits

De toepassing Learning Manager is beschikbaar in het Frans en Duits. U kunt de taal aanpassen voor feedback, cursusinstanties en communicatie.

### Verbeteringen {#Enhancements-13}

Er zijn aanzienlijke verbeteringen aangebracht in de bestaande functies van Learning Manager. De belangrijkste verbeteringen zijn:

### CSV importeren

Als u gebruikers verwijdert, kunt u dezelfde gebruikers niet opnieuw aan de toepassing toevoegen door één gebruiker toe te voegen. U kunt de verwijderde gebruiker echter wel weer toevoegen met behulp van het CSV-uploadproces. De beperking voor verplichte velden in de CSV-uploadfunctie is aanzienlijk gewijzigd. Raadpleeg  [Veelgestelde vragen over CSV](../administrators/add-users-in-bulk.md) voor meer informatie.

### Cursuslijstweergave

Standaard kunt u cursussen als kaarten bekijken. Deze release bevat een lijstweergave. U kunt op het pictogram met de drie balken naast het zoekveld klikken om de weergave te wijzigen.

### Cursussen verwijderen

U kunt nu cursussen in de fasen Concept en Gearchiveerd verwijderen. Raadpleeg  [Cursussen](../administrators/feature-summary/courses.md) voor meer informatie. Als een leerobject wordt verwijderd, worden ook alle bijbehorende rapportagegegevens verwijderd. Als een cursus wordt verwijderd en als deze deel uitmaakte van een ander leerobject, verschijnt een geschikt bericht voor de gebruiker.

**Leerprogramma&#39;s en -plannen**

U kunt de volgorde afdwingen waarin studenten cursussen binnen leerprogramma&#39;s kunnen volgen. U kunt leerprogramma&#39;s in concepten en gearchiveerde fasen verwijderen. Als een leerobject wordt verwijderd, worden ook alle bijbehorende rapportagegegevens verwijderd.

**Certificeringen**

U kunt certificeringen in concepten en gearchiveerde fasen verwijderen. Als een leerobject wordt verwijderd, worden ook alle bijbehorende rapportagegegevens verwijderd.

**Effectiviteitsscore van cursus**

In Beheerdersaanmelding kunt u L1- en L3-feedbackgegevens voor elke cursus exporteren.

**Cursussen met modules maken**

U kunt studenten verplichten om de voorwaarden te voltooien voordat ze de cursussen volgen.

**Gebruikersmeldingen**

Studenten krijgen meldingen wanneer ze zichzelf inschrijven voor een leerprogramma.

**Klaslokaalmodules (ILT)**

U kunt klassikale cursussen maken voor een datum in het verleden. Met deze functie kunnen bedrijfsbeheerders informatie over oudere klassikale cursussen ook in de Leermanager invoeren en rapporten genereren.

**Rapporten exporteren**

Het studentenrapport is verbeterd. U kunt naam, e-mail, status van leerobject, inschrijvingscriteria, inschrijvingsdatum, voltooiingsdatum en startdatum in het rapport bekijken.

**Externe partners toevoegen**

Na het inschrijven van de externe studenten voor de Learning Manager-account kunt u het aantal studenten indien nodig ook verkleinen. U kunt de studenten echter niet verkleinen tot meer dan het gebruikte aantal plaatsen. Als tussenoplossing kunt u eerst de geregistreerde studenten verwijderen en vervolgens opnieuw inschrijven met het vereiste aantal plaatsen.

### Opgeloste problemen {#Issuesfixed-14}

**Aanwezigheid van studenten**

Op het blad Aanwezigheid in de weergave Beheerder wordt de volledige naam van de medewerker weergegeven als deze beschikbaar is. Eerder verscheen alleen de voornaam van de student.

**Leerprogramma&#39;s en -plannen**

Alle cursussen in leerprogramma&#39;s worden in de verwachte volgorde weergegeven. Eerder waren er problemen met de volgorde van de cursussen in een leerprogramma. Dit probleem is opgelost.

**Studenten toevoegen**

Als een bestaande gebruiker die zichzelf heeft geregistreerd, opnieuw probeert te registreren met behulp van een zelfregistratieproces, verschijnt een geschikt bericht. De indeling en inhoud van het bericht zijn vast.

**Rapporten**

Als u wilt dat in de inhoud wordt aangegeven hoeveel tijd de gebruiker heeft besteed aan het consumeren van inhoud, kunt u dit herkennen aan de hand van een variabele. `code cmi.core.session_time`. De variabele is niet eerder ingesteld. Dit probleem is opgelost.

**Cursussen met modules maken**

Wanneer een bestaande cursusmodule wordt vervangen door een andere module, wordt er een nieuwe versie van gegenereerd. Als de quiz van deze nieuwe module wordt geëxporteerd, trad er een uitzondering op en werd het quizrapport niet gegenereerd. Dit probleem is nu opgelost.

**E-mailsjablonen**

De typos in de e-mailsjablonen is opgelost.

+++

+++Update 9

Releasedatum: 9 februari 2016.

## Afmeldingsgedrag bijgewerkt {#signoutbehaviorupdated}

Wanneer gebruikers op **[!UICONTROL Afmelden]** in Leermanager worden ze nu afgemeld bij de toepassing Leermanager en worden ze ook afgemeld bij hun Adobe-id&#39;s.

+++

+++Update 8

Releasedatum: 20 januari 2016.

### Verbeteringen {#Enhancements-14}

**Aanpasbare e-mails**

* Gebruikers kunnen de voettekstsectie van de e-mailsjablonen aanpassen. U kunt de voettekst in een e-mailsjabloon aanpassen met de tekst van uw keuze. De aangepaste voettekst wordt automatisch toegepast op alle typen e-mailsjablonen.

**Cursus volgen**

* De bronobjecten in de voorbeeldmodus van een cursus worden op een nieuwe regel achter elkaar weergegeven. Eerder waren er gevallen waarin de leermiddelen in een cursus in één regel naast elkaar verschenen.

**Directe koppeling naar leerobjecten**

* U hebt toegang tot de leerobjecten (behalve Certificering) via een directe URL. De **[!UICONTROL URL kopiëren]** wordt weergegeven op de tegels van leerobjecten. Gebruikers kunnen klikken **[!UICONTROL URL kopiëren]** en plak de koppeling in een aparte browserpagina om het leerobject rechtstreeks te openen.

**Cursussen maken met modules**

* Tijdens het maken van een cursus kunnen auteurs de vereiste cursussen in willekeurige volgorde rangschikken. Deze optie was eerder niet beschikbaar in Leerbeheer.

* Auteurs kunnen vereiste cursussen toevoegen aan of verwijderen uit Gepubliceerde cursussen. Deze functie was eerder alleen beschikbaar voor conceptcursussen.

**Gebruikersregistratie**

* Gebruikers kunnen zich zonder extra URL-verificatie aanmelden bij Leermanager als hun Adobe ID overeenkomt met de e-mail-ID van Leermanager. Tijdens het toevoegen van gebruikers aan het account verstrekt de beheerder van een organisatie de e-mail-ID van de leermanager.

**Catalogus maken**

* In de beheerdersrol tijdens het maken van catalogi met **Leerobjecten toevoegen** gearchiveerde cursussen niet in de lijst met cursussen worden weergegeven.

**Andere oplossingen**

* In de beheerdersrol wordt de volledige naam van de studenten weergegeven in **Studenten** tabblad. Eerder verscheen alleen de voornaam van de student.

+++

+++Update 7

Releasedatum: 13 januari 2016.

### Opgeloste problemen {#Issuesfixed-15}

**Cursus volgen**

* Wanneer u cursusinhoud opent, wordt de afspeelbalk van de inhoud altijd op het scherm weergegeven. Eerder was er een probleem met de inhoudsbalk, omdat deze af en toe van het scherm verdween.
* Als gebruikers tijdens het openen van cursusinhoud een pop-upvenster zien waarin wordt gevraagd of ze echt willen afsluiten of op de pagina willen blijven, kunnen ze teruggaan naar de inhoud als ze op dit dialoogvenster blijven. In sommige gevallen werd de gebruiker uit de cursusinhoud gehaald door op de knop Blijven te klikken.

**Andere oplossingen**

* Enkele problemen met betrekking tot het afspelen van inhoud zijn opgelost.

+++

+++Update 6

Releasedatum: 22 december 2015.

### Verbeteringen {#Enhancements-15}

**Persoonlijk dashboard**

* Bij het openen van cursussen, catalogi en leerprogramma&#39;s in de beheerders- en auteursrollen wordt de tabvolgorde gewijzigd in **Gepubliceerd - concept - alles - gearchiveerd**. De standaardselectie is **Gepubliceerd**

### Opgeloste problemen {#Issuesfixed-16}

**Cursus volgen**

* Als de speler tijdens het volgen van een cursus wordt gesloten met behulp van de knop Terug van de browser of de Backspace-toets op het toetsenbord, wordt de leertijd die aan de cursus is besteed, vastgelegd in rapporten. In sommige scenario&#39;s was er een probleem dat deze duur niet werd vastgelegd in rapporten.

**Gebruikersregistratie**

* Als een gebruiker een Leerbeheerdersaccount registreert met behulp van zelfregistratie met SSO ingeschakeld, wordt de gebruikersnaam correct weergegeven in de gebruikerslijst volgens records. In sommige gevallen werd de gebruikersnaam niet correct weergegeven.

**Cursussen maken met modules**

* Wanneer een auteur een cursus dupliceert, kunnen de bronbestanden van de gedupliceerde cursus worden verwijderd of bijgewerkt. In sommige scenario&#39;s ondervonden gebruikers problemen bij het bijwerken of verwijderen van de leermiddelen uit gedupliceerde cursussen.

**Een aangepaste catalogus maken voor een gebruikersgroep**

* Tijdens het gebruik **Leerobjecten toevoegen** in de beheerdersrol, kunt u cursussen filteren, een cursus kiezen en toevoegen met **Toevoegen** onder aan het dialoogvenster. In sommige gevallen: **Toevoegen** niet voor sommige gebruikers werd weergegeven.

+++

+++Update 5

Releasedatum: 11 december 2015.

### Opgeloste problemen {#Issuesfixed-17}

**Gebruikersaanmelding**

* Wanneer een gebruiker zich probeerde aan te melden bij de Leerbeheertoepassing zonder activeringskoppeling, verscheen het foutbericht in een verkeerde indeling. Dit probleem is opgelost.

**App voor tablets**

* Na het installeren van Learning Manager op een Android- of iPhone-tablet, worden er geen berichten over browsercompatibiliteit weergegeven. Eerder verscheen voor gebruikers een bericht over browsercompatibiliteit. Dit probleem is opgelost.

+++

+++Update 4

Releasedatum: 9 december 2015.

### Verbeteringen {#Enhancements-16}

**Gebruikers toevoegen**

* Wanneer de beheerder in de beheerdersrol gebruikers registreert of één gebruiker toevoegt, verschijnt een bericht dat de workflow met de volgende stappen is voltooid.
* Wanneer een gebruiker zich rechtstreeks probeert aan te melden bij de Leerbeheertoepassing zonder de activeringskoppeling van de gebruiker te gebruiken, verschijnt een foutbericht waarin gebruikers wordt gevraagd om de activeringskoppeling te gebruiken.

**Ondersteunde browsers**

* Als een gebruiker toegang krijgt tot de toepassing Learning Manager in niet-ondersteunde browsers, ontvangt de gebruiker een waarschuwing met de lijst van browsers op de witte lijst.

### Opgeloste problemen {#Issuesfixed-18}

**Rapporten**

* Wanneer u in de beheerdersrol of de beheerdersrol een rapport maakt met de secundaire as als bestede leertijd, een managerfilter toepast en het rapport opslaat, kon de gebruiker dergelijke rapporten niet downloaden. U kunt alle typen rapporten downloaden.

**Gebruikers toevoegen**

* Er stonden enkele typfouten in het waarschuwingsbericht terwijl externe studenten in de beheerdersrol werden ingeschakeld. Het probleem is opgelost.
* In de beheerdersrol verschijnt een foutbericht als het veld Manager niet goed is geselecteerd tijdens het toevoegen van één gebruiker.

**Gebruikersregistratie**

* Welkomstmail die nieuwe gebruikers ontvangen, benadrukt het belang van het koppelen van Adobe ID aan de Leermanager-id voor geslaagde aanmelding.

**Aanpasbare e-mails**

* Wanneer u meerdere studenten toevoegde aan de klassikale cursussen die sessies als bijlage hebben, ontvingen sommige studenten geen e-mailmeldingen. Dit probleem is opgelost.
* E-mails aan studenten over inschrijvingen voor leerobjecten en andere gebeurtenissen bevatten de specifieke naam van het leerobject in het onderwerp van de e-mail.

**Andere oplossingen**

* De problemen met betrekking tot URL-koppelingen in e-mailsjablonen zijn opgelost.
* Ondersteuning voor

   * Publiceren naar Leermanager
   * Snellere ondersteuning voor het uploaden van inhoud voor CP 8-versie (CP803-patch is vereist)

+++

+++Update 3

Releasedatum: 26 oktober 2015.

### Verbeteringen {#Enhancements-17}

**Gebruikers toevoegen**

* De koppeling Online Help in het dialoogvenster Gebruikers toevoegen > CSV-upload verschijnt voor een beter begrip van de gebruikers tijdens het uploaden van het CSV-bestand.

**Fluidic Player**

* Wanneer u inhoud van een Captivate cursus met een grootte van meer dan 500 MB uploadde, werd de inhoud niet afgespeeld in Fluidic Player. Deze beperking is verwijderd. Momenteel is de maximale grootte gewijzigd in 2 GB.

**Facturering**

* Wanneer een gebruiker in de beheerdersrol het aantal studenten invoert en op **Bestelling plaatsen,** er verschijnt een dialoogvenster met informatie over maandelijkse en jaarlijkse abonnementskosten per gebruiker.

### Opgeloste problemen {#Issuesfixed-19}

**Cursussen maken met modules**

* Tijdens het maken van cursussen met activiteitenmodules kunnen auteurs geldige externe URL&#39;s kiezen, zelfs als deze mappaden in de URL bevatten. Eerder werden URL&#39;s met mappaden niet ondersteund. Dit probleem is opgelost.
* Als de cursusinhoud een project is dat met een ZIP-bestand wordt geüpload in Leerbeheer en als dat ZIP-bestand mappaden bevat, als Zip>map>inhoud, wordt dit type inhoud niet ondersteund. Dit probleem is opgelost.

**App voor tablets**

* Wanneer een gebruiker de bronbestanden van een cursus probeert te downloaden in de Android-app van Learning Manager, kunnen de bronbestanden niet worden gedownload. Dit probleem is opgelost.
* Wanneer een gebruiker een cursus volgt met behulp van Fluidic Player en deze vervolgens probeert te downloaden van de cursus, kan deze niet worden gedownload. Dit probleem is opgelost.

+++

+++Update 2

Releasedatum: 28 september 2015.

### Verbeteringen {#Enhancements-18}

**Cursussen maken met modules**

* De toepassing Learning Manager ondersteunt het uploaden van SCORM-inhoud, zelfs als de versie niet wordt vermeld in het bestand manifest.xml. Standaard wordt de versie beschouwd als 1.2.
* Wanneer u inhoud van een Captivate cursus met een grootte van meer dan 500 MB uploadde, werd de inhoud niet afgespeeld in Fluidic Player. Als onderdeel van Update 2 is de maximale grootte gewijzigd in 800 MB.

**Facturering**

* In de beheerdersrol kan de gebruiker bij het aanschaffen van een abonnement met behulp van een creditcard de eerste bestelling kiezen, te beginnen met 10 studenten. Het minimum aantal studenten dat vereist is voor de eerste bestelling is teruggebracht van 100 naar 10.

**Gebruikersregistratie**

* Een URL-koppeling om een Adobe ID te maken is opgenomen in de welkomstmail die studenten na hun registratie ontvangen.

**Gebruikers toevoegen**

* In de beheerdersrol werkte het toevoegen van gebruikers via CSV-upload rechtstreeks vanuit het Exavault-account niet voor sommige klanten. Dit probleem is opgelost.

### Opgeloste problemen {#Issuesfixed-20}

**Leerprogramma&#39;s en -plannen**

* Studenten kunnen automatisch worden ingeschreven voor hetzelfde leerprogramma als onderdeel van meerdere leerplannen. Eerder waren er enkele uitzonderingen op deze workflow. Dit probleem is opgelost.

**Leaderboard en badges weergeven**

* In de studentrol werd, na het volgen van een cursus met een badge, de badgeafbeelding niet weergegeven op de badgekaart van het dashboard van de student en in het gedownloade bestand. Dit probleem is opgelost.

**App voor tablets**

* Er verschijnt een pop-up om de beschikbaarheid van de student-app aan te geven wanneer de URL van de student-app wordt geopend in een browser op een Android-apparaat.

**Andere oplossingen**

* Er is een probleem opgelost met het maken van gebruikersaccounts vanwege ondersteuning voor netto-opslag in Akamai.
* Er is een probleem opgelost met betrekking tot het uploaden van SCORM 1.2-inhoud met een ZIP-bestand met meerdere mappen.

+++
