---
description: Leer hoe u diverse connectoren integreert in Learning Manager
jcr-language: en_us
title: Learning Manager-connectoren
contentowner: jayakarr
exl-id: 1f44934b-6a2b-484d-bc7f-d0f23e3008ca
source-git-commit: 7be69e68f3b8970e090c8eccd25771cd2e5e99f1
workflow-type: tm+mt
source-wordcount: '15924'
ht-degree: 60%

---

# Learning Manager-connectoren

Bedrijven hebben andere toepassingen en systemen die geïntegreerd moeten worden met Learning Manager. Connectors zijn hulpprogramma&#39;s die u helpen bij het uitvoeren van op gegevens gebaseerde integraties, zoals het importeren van gegevens naar Learning Manager van externe systemen.  U kunt ook gegevens vanuit Learning Manager exporteren naar externe systemen.

Learning Manager levert Salesforce- en FTP-connectoren. Via de Salesforce-connector kunnen de integratiebeheerders van een organisatie hun Salesforce-toepassing met Learning Manager integreren. Als integrator kunt u ook een FTP-connector gebruiken om een aantal gebruikers automatisch in uw bedrijfstoepassing te importeren.

Learning Manager levert ook de Lynda-, getAbstract- en de Harvard Management System-connectoren. Deze connectoren stellen studenten in staat om toegang te krijgen tot en gebruik te maken van cursussen van Lynda.com, getAbstract en Harvard ManageMentor.

Lees verder om te weten te komen hoe u elk van deze connectoren in Learning Manager kunt configureren en gebruiken.

<!--
>[!NOTE]
>
>**Update:** December 2020 update of Learning Manager
>
>For **FTP**, **Box**, and **Custom FTP** connectors, while exporting Learner Transcript or xAPI, you can also export the data as a **zip** file, for:
>
>* Learner Transcripts
>* xAPI
-->

>[!NOTE]
>
>Met ingang van de Adobe Learning Manager-release van november 2022 heeft Zoom de JWT-verificatie beëindigd [in juni 2023](https://marketplace.zoom.us/docs/guides/auth/jwt/). Volgens deze aankondiging werkt de Zoom-connector met JWT tot de genoemde datum, maar wij raden gebruikers aan om een server-naar-server OAuth-app te maken om deze functionaliteit in de accounts te vervangen. Elke nieuwe verbinding beschikt standaard over Zoom OAuth-verificatie.

## Salesforce-connector {#sfconnector}

De Salesforce-connector verbindt Learning Manager met Salesforce-accounts om de synchronisatie van gegevens te automatiseren. De mogelijkheden van de Salesforce-connector zijn als volgt:

### Kenmerken toewijzen

De integratiebeheerder kan Salesforce-kolommen kiezen en aan de overeenkomstige groepeerbare kenmerken van Learning Manager toewijzen. Wanneer de toewijzing is voltooid, wordt dezelfde toewijzing voor verdere gebruikersimporten gebruikt. De beheerder kan de toewijzing opnieuw configureren als deze een andere toewijzing voor het importeren van gebruikers wil.

### Geautomatiseerde gebruikersimport

Via het proces voor gebruikersimport kan de Learning Manager-beheerder werknemersgegevens uit Salesforce ophalen en automatisch in Learning Manager importeren. Door deze automatisering hoeft het creëren van CSV&#39;s en het uploaden naar Learning Manager niet handmatig te gebeuren.

### Automatisch plannen

Het kan effectief zijn om de functie voor automatische planning samen met de functie voor geautomatiseerde gebruikersimport te gebruiken. De Learning Manager-beheerder kan het schema volgens de behoeften van de organisatie instellen. Gebruikers in de Learning Manager-applicatie kunnen volgens het schema up-to-date zijn. De synchronisatie kan dagelijks worden uitgevoerd in de Learning Manager-toepassing.

### Gebruikers filteren

De Learning Manager-beheerder kan gebruikers filteren voordat ze worden geïmporteerd. Zo kan de Learning Manager-beheerder er bijvoorbeeld voor kiezen om alle gebruikers in de hiërarchie onder één of meer specifieke managers te importeren.

### De Salesforce-connector configureren {#configuresalesforceconnector}

Leer meer over het proces om Salesforce te integreren met Learning Manager

#### vereisten van het proces leren kennen {#prerequisites}

Zorg ervoor dat u uw organisatie-URL voor Salesforce hebt. Als de naam van uw organisatie bijvoorbeeld myorg **is**, kan `https://myorg.salesforce.com`de Salesforce-URL . Dit is alles wat u moet invoeren om het Salesforce-account met Learning Manager te verbinden.

Zorg er ook voor dat u de juiste gegevens hebt om u bij het account aan te melden.

#### Een verbinding maken {#createaconnection}

1. Beweeg de muis over de Salesforce-kaart/miniatuur op de Learning Manager-startpagina. Er verschijnt een menu. Klik op **[!UICONTROL Verbinden]** in het menu.

   ![](assets/mouserover-salesforce.png)

   *Verbindingsoptie*

1. Er verschijnt een dialoogvenster waarin u wordt gevraagd om de org-url in te voeren. Klik op **[!UICONTROL Verbinden]** nadat u de URL hebt opgegeven.
1. Zodra de verbinding tot stand is gebracht, verschijnt de overzichtspagina.

### Kenmerken toewijzen {#mapattributes}

Zodra de verbinding tot stand is gebracht, kunt u Salesforce-kolommen toewijzen aan de bijbehorende kenmerken van Learning Manager. Deze stap is verplicht.

1. Op de toewijzingspagina ziet u links de kolommen van Learning Manager en aan de rechterkant de Salesforce-kolommen. Selecteer de juiste kolomnaam die wordt toegewezen aan de kolomnaam van de leermanager.

   ![](assets/sfdc-map-columns.png)
   *Kenmerken toewijzen*

   >[!NOTE]
   >
   >De Learning Manager-kolomgegevens aan de linkerkant worden opgehaald uit de actieve velden. Het **managerveld** moet worden toegewezen aan een veld met het type e-mailadres. U moet alle kolommen toewijzen voordat u de connector kunt gebruiken.

1. Klik op **[!UICONTROL Opslaan]** nadat de toewijzing is voltooid.
1. De connector is nu klaar voor gebruik. Het account dat is geconfigureerd verschijnt als een gegevensbron binnen de beheerdersapp. De beheerder kan de import of synchronisatie op verzoek plannen.

## Gebruik van de Salesforce-connector {#usingsalesforceconnector}

De Salesforce-connector maakt verbinding met Salesforce.com om de geconfigureerde gebruikers op te halen en toe te voegen aan Learning Manager.

### Gebruikers importeren van Salesforce-contacten {#import-salesforce-contacts}

Learning Manager verbetert de Salesforce-connector nu zodat zowel contacten als Salesforce-gebruikers worden opgehaald en automatisch geïmporteerd in Learning Manager.

Voer op de pagina van de Salesforce-connector de Salesforce-URL in en voltooi de verificatie. Nadat u zich hebt geverifieerd, kunt u gebruikers of contactpersonen importeren. Als u de optie Contactpersonen kiest, geeft u de subset van de contactpersonen op die moeten worden geïmporteerd.

Kies de Salesforce-kolommen en wijs deze toe aan de bijbehorende groepskenmerken van Learning Manager. Wanneer de toewijzing is voltooid, wordt dezelfde toewijzing voor verdere gebruikersimporten gebruikt.

1. Meld u aan bij Salesforce.
1. Klik op de verbindingspagina op **[!UICONTROL Interne gebruikers]** importeren.

   ![](assets/image048.png)
   *Interne gebruikers importeren*

1. Op de **pagina Gebruikers** importeren ziet u een nieuwe optie Contactpersonen. Klik op het keuzerondje **Contacten** om de volgende opties te zien.

   ![](assets/image050.png)
   *De contactkenmerken toewijzen*

1. Als u op Ja ]**klikt**[!UICONTROL , kunt u het volgende doen:

   * **Kolom Contactpersonen kiezen:** Selecteer het veld dat u wilt importeren in Learning Manager.
   * **Waarden opgeven:** kies de waarden die het geselecteerde veld vertegenwoordigen.

   ![](assets/image053.png)
   *Geef de waarden op*

   * Wijs de Salesforce-kolommen toe aan die van Learning Manager.
   * Klik op **[!UICONTROL Opslaan]** om te beginnen met importeren.

1. Als u op Nee.**[!UICONTROL Importeer alle contactpersonen]**, u kunt de velden direct toewijzen zonder de contactpersonen te filteren. Hier importeert u alle contactpersonen uit Salesforce.
1. Klik op **[!UICONTROL Opslaan]** om te beginnen met importeren.

## Leerrecords exporteren

Learning Manager biedt de mogelijkheid om leerrecords, zoals een transcript, gebruikersrapport of vaardigheidsrapport, te exporteren naar Salesforce. U kunt bepalen of de geëxporteerde gegevens moeten worden gekoppeld aan de tabel &#39;Gebruiker&#39; of &#39;Contactpersonen&#39; in Salesforce.

![](assets/export-events-new.png)
*Leerrecords exporteren*

### Aangepaste objecten in Salesforce

Voordat u leerrecords van Learning Manager exporteert, moet u aangepaste objecten maken in Salesforce. Aangepaste objecten zijn objecten die u maakt om informatie op te slaan die specifiek is voor uw bedrijf of branche. Zie [Aangepaste objecten van Salesforce](https://trailhead.salesforce.com/en/content/learn/modules/data_modeling/objects_intro) voor meer informatie.

Zo maakt u de objecten:

1. Download en installeer de pakketten om de aangepaste objecten te maken.

   * [Pakket 1](https://test.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WPJ)
   * [Pakket 2](https://test.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WPT)
   * [Pakket 3](https://test.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WPi)

1. Hernoem de namen van de aangepaste objecten in Salesforce.
1. Selecteer de gebeurtenis en klik op **[!UICONTROL Opslaan]**.

>[!NOTE]
>
>Zorg ervoor dat de systeembeheerder toegang heeft gekregen tot alle actieve velden die zijn toegevoegd na de installatie van het pakket.

**Koppel gebeurtenissen aan:** Kies de sectie die u wilt exporteren- Gebruiker of Contactpersoon. Als u het contactobject kiest, worden er gebruikers gemaakt die wel aanwezig zijn in Learning Manager, maar niet in Salesforce.

![](assets/link-events.png)
*Optie Voor koppelingsevenementen*

>[!NOTE]
>
>U kunt meerdere verbindingen maken in één account. Een enkele verbinding kan tot drie aangepaste objecten in Salesforce dienen. Als u meerdere verbindingen voor hetzelfde Salesforce-account wilt maken, moet u de drie pakketten installeren. We bieden ondersteuning tot drie pakketten.
>
>U moet net zoveel pakketten installeren als het aantal verbindingen dat u wilt maken.

>[!NOTE]
>
>Op de pagina Uitvoeringsstatus voor Salesforce kan het aantal verwerkte records alleen worden gecontroleerd vanuit Salesforce. Leerbeheer geeft de status voltooid weer, zelfs als er een deel van de export of een fout opgetreden is in alle records die zijn verwerkt.

## Het Salesforce-pakket installeren

Learning Manager biedt een Salesforce-apppakket aan. Na de installatie en configuratie in SFDC kunnen verkoopmedewerkers hun trainingsactiviteiten uitvoeren in de SFDC-portal. Met deze app kunnen SFDC-gebruikers nieuwe trainingen verkennen, aanbevelingen bekijken en deze rechtstreeks in de SFDC-portal gebruiken. Gebruikers ontvangen de aankondigingen ook door beheerders in de vorm van mastheads rechtstreeks in de app binnen de SFDC-portal.

### Instellen in de Learning Manager-app.

1. Meld u als integratiebeheerder bij uw Learning Manager-beheerdersaccount aan.
1. Klik op **[!UICONTROL Applicaties]** > **[!UICONTROL Aanbevolen apps]**.
1. Klik op **[!UICONTROL Salesforce]**.
1. Noteer op de pagina van de Salesforce-app de toepassings-id (ook wel client-id genoemd) en het clientgeheim dat in de beschrijving wordt vermeld.
1. Klik op **[!UICONTROL Goedkeuren]** en de app moet zijn goedgekeurd.
1. Klik op **[!UICONTROL Bronnen]** voor ontwikkelaars > **[!UICONTROL Toegangstokens voor testen en ontwikkelen]**.
1. In de sectie OAuth-code ophalen moeten de Client-id en het bereik zijn ingesteld op - admin:read,admin:write. Klik op **[!UICONTROL Verzenden]**.
1. Voer bij Vernieuwingstoken ophalen de client-ID en het clientgeheim in. Klik op Verzenden ]**en let op**[!UICONTROL  de vernieuwingstoken.

### Account aanmaken in de Salesforce-app

1. Maak een account aan op de aanmeldingspagina van Salesforce. U moet een Salesforce-account maken in de Developer of Enterprise Edition.  [Aanmeldings-URL voor ontwikkelaars](https://developer.salesforce.com/signup). Zorg ervoor dat u de e-mail-id moet gebruiken om u te registreren voor Salesforce die u voor Learning Manager hebt gebruikt.
1. Verifieer uw account via de verificatie-e-mail.
1. Maak een wachtwoord aan en meld u aan bij Salesforce.
1. Noteer de Salesforce-URL na aanmelding (bijvoorbeeld site.lightning.force.com)

### Installeer het Learning Manager-pakket

Als u het pakket wilt installeren, moet u eerst het bestaande pakket in Salesforce verwijderen. Voordat u de installatie ongedaan maakt, moet u de instellingen inschakelen, zoals hieronder weergegeven. U moet deze instellingen toepassen, anders kunt u het pakket niet installeren.

>[!NOTE]
>
>De Adobe Learning Manager-app wordt alleen ondersteund in de Salesforce Lightning-weergave.

1. Start de [Pakket-URL](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WOQ) van Learning Manager.
1. Klik op de **pagina Aanmelden** op **[!UICONTROL Aangepast domein gebruiken]**.
1. Voer de pakket-URL in en klik op **[!UICONTROL Doorgaan]**. Op de installatiepagina moet de optie Installeren voor alleen beheerders zijn geselecteerd. Wijzig deze optie niet.
1. Klik op **[!UICONTROL Installeren]**. Nadat het pakket is geïnstalleerd, klikt u op **[!UICONTROL Gereed]**. U wordt naar de pagina Geïnstalleerde pakketten geleid en u kunt het geïnstalleerde Adobe Learning Manager-pakket zien.
1. Ga naar het startprogramma voor apps (naast Configuratie) en zoek naar Adobe Learning Manager.
1. Klik op **[!UICONTROL Configureren]** om de app te configureren.
1. Klik op **[!UICONTROL Nieuw]** en voeg de volgende gegevens toe:

   * **Configuratie:** Voer een naam naar keuze in.
   * **ClientID**: voer de waarde in die u uit de eerste sectie hebt verkregen.
   * **Clientsecret:** voer de waarde in die u hebt verkregen uit de eerste sectie.
   * **RefreshToken:** voer de waarde in die u hebt opgehaald uit de eerste sectie.
   * **LearningManagerBaseURL:** de URL van de site waar Learning Manager wordt gehost.

### Instellingen voor externe site toevoegen

1. Klik in de rechterbovenhoek van de pagina op **[!UICONTROL Instellingen]**.
1. **[!UICONTROL Ga in Snel zoeken]** naar instellingen voor externe site.
1. Klik op **[!UICONTROL Nieuwe externe site]**.
1. Voer de gegevens in:

   * **Naam van externe site:** Voer een naam naar keuze in.
   * **Remote Site URL:** De URL van de site waar Learning Manager wordt gehost.

1. Start Learning Manager.

### Meldingen inschakelen voor de app Learning Manager

1. Klik in de rechterbovenhoek op **[!UICONTROL Instellen]**.
1. Zoek naar aangepaste meldingen.
1. Klik op **[!UICONTROL Nieuw]**.
1. Voer de volgende gegevens in:

   1. **Aangepaste naam melding:** LearningManagerNotification
   1. **API-naam:** LearningManagerNotification

1. Selecteer kanalen voor bureaublad **** en **mobiel** als ondersteunde kanalen.

1. Klik op **[!UICONTROL Opslaan]**.
1. Volg de onderstaande stappen om pushmeldingen voor mobiele apparaten in te schakelen:

   1. Installeer de mobiele Salesforce-app op uw mobiele telefoon.
   1. Meld u aan bij de app met uw gegevens.
   1. Ga naar **Instellingen** > Voor levering **van** meldingen.
   1. Voeg Salesforce toe voor iOS en Android.

### Deïnstalleer Learning Manager bij Salesforce

1. Ga in de Salesforce-app naar Geïnstalleerde pakketten.
1. Klik op **[!UICONTROL Verwijderen]**.

## Learning Manager configureren voor Salesforce-gebruikers

De Learning Manager-app is ook beschikbaar voor gebruikers die in een Salesforce-account aanwezig zijn. De beheerder van Salesforce kan gebruikers toevoegen op basis van de profielen. De Salesforce-profielen komen overeen met die in Learning Manager. Bijvoorbeeld beheerder, integratiebeheerder, docent enzovoort. De Salesforce-beheerder kan ook een aangepast profiel maken.

Als Salesforce-beheerder kunt u de profielen aan gebruikers toewijzen of een aangepast profiel maken.

![](assets/create-profile.png)

U kunt het Salesforce-profiel aan de studenten toewijzen wanneer u het pakket installeert.

Nadat u het pakket hebt geïnstalleerd, moet u het profiel configureren.

Klik op **[!UICONTROL >**[!UICONTROL  Nieuw ]**configureren]** en voeg de volgende opties toe:

* Configuratienaam
* Client-id
* Clientgeheim
* LearningManagerBaseURL
* Omleiden uitschakelen

>[!NOTE]
>
>Als u wilt dat studenten de app Learning Manager kunnen weergeven, moet u de app voor alle studenten inschakelen.

Vervolgens geeft u toegang tot de Learning Manager-app.

![](assets/permission-set.png)

*Machtigingen instellen voor toegang tot de app Learning Manager*

Selecteer de gebruikers en wijs de betreffende machtigingen toe. De studenten hebben nu toegang tot de Learning Manager-app.

Nu selecteert u een profiel, een standaard profiel van een gebruiker bijvoorbeeld, en klikt u op het profiel. Klik op **[!UICONTROL Bewerken]** en schakel in het **gedeelte Aangepaste app-instellingen** het selectievakje **Adobe Learning Manager** in. Hierdoor heeft de student toegang tot de app.

In de vervolgkeuzelijst **Startpagina voor studenten** selecteert u in de sectie **Aangepaste tabbladinstellingen** de optie **Standaard ingeschakeld**.

U moet de app voor alle profielen zichtbaar maken.

Klik op **[!UICONTROL Opslaan]** , waarna de leerlingen die tot alle profielen behoren, toegang krijgen tot de app Leerbeheer.

### Wijzigingen met betrekking tot leerpad

#### Bestaande verbindingen

Als de optie Leerpad is uitgeschakeld in het beheerdersaccount, worden er geen rijen en kolommen in het rapport toegevoegd.

Als de optie Leerpad is ingeschakeld in het beheerdersaccount, wordt het leerpad ingevuld in de kolom &#39;Type&#39; voor het geval dat studenten zijn ingeschreven.

>[!NOTE]
>
>Als de markering is ingeschakeld en u een bestaande verbinding gebruikt, kunnen enkele records worden gemist.

#### Nieuwe verbindingen

Als de optie Leerpad is uitgeschakeld in het beheerdersaccount, bestaat het trainingsrapport uit de volgende kolommen, maar bevat het geen gegevens.

* **Ingesloten pad:** geeft de naam van het leerprogramma weer.
* **Ingesloten pad-ID:** geeft de ID&#39;s voor het leerprogramma weer.
* **Ingesloten cursus-id:** hier worden de id&#39;s weergegeven van cursussen die zich binnen een leerpad bevinden.

Daarnaast worden de drie nieuwe kolommen weergegeven voor nieuwe verbindingen in accounts waarvoor leerpad is ingeschakeld en stromen alle gegevens door.

Daarnaast bevat het rapport het type Leerpad (hoger niveau) voor alle leerlingen die zijn ingeschreven voor een leerpad.

In de kolom Tekst wordt het leerprogramma hernoemd als Leerpad. Bestaande verbindingen wijzigen niet.

## Learning Manager FTP-connector {#ftpconnector}

Met behulp van de FTP-connector kunt u Learning Manager integreren met willekeurige externe systemen om de synchronisatie van gegevens te automatiseren. Van externe systemen wordt verwacht dat ze gegevens in een CSV-formaat kunnen exporteren en in de juiste map van het Learning Manager FTP-account kunnen plaatsen. De mogelijkheden van de FTP-connector zijn als volgt:

U kunt de Box-connector ook gebruiken voor gegevensmigratie, gebruikers importeren en gegevens exporteren. Zie Box Connector voor meer informatie.

### Gegevensimport {#dataimport}

Met het gebruikersimportproces kan de Learning Manager Administrator werknemersgegevens ophalen van de FTP-service van Learning Manager en ze automatisch in Learning Manager importeren. Met behulp van deze functie kunt u meerdere systemen integreren door de door deze systemen gegenereerde CSV in de juiste mappen van de FTP-accounts te plaatsen. Learning Manager haalt de CSV-bestanden op, voegt ze samen en importeert de gegevens volgens de planning. Raadpleeg de planningsfunctie voor meer informatie.

**Kenmerken toewijzen**

Kenmerken toewijzen Deze toewijzing is een eenmalige inspanning. Zodra de toewijzing is voltooid, wordt dezelfde toewijzing gebruikt voor de daaropvolgende gebruikersimporten. De toewijzing kan opnieuw worden geconfigureerd als de beheerder een andere toewijzing voor het importeren van gebruikers wil hebben.

#### Gegevens exporteren {#exportdata}

Gevensexport stelt gebruikers in staat om de vaardigheden van de gebruiker en de transcripten van de student te exporteren naar een FTP-locatie om deze te integreren met een willekeurig systeem van derden.

#### Planning {#scheduling}

De beheerder kan planningstaken volgens de vereisten van de organisatie instellen en gebruikers in de Learning Manager-toepassing zijn up-to-date volgens de planning. Op dezelfde manier kan de integratiebeheerder de export van vaardigheden op een tijdige basis plannen om deze te integreren met een extern systeem. De synchronisatie kan dagelijks worden uitgevoerd in de Learning Manager-toepassing.

### Learning Manager FTP-connector configureren {#configurecaptivateprimeftpconnector}

Leer het proces om de FTP-connector te integreren met Learning Manager.

#### Een verbinding maken {#Createaconnection-1}

1. Beweeg de muis over de FTP-kaart/miniatuur op de Learning Manager-startpagina. Er verschijnt een menu. Klik op **[!UICONTROL Verbinden]** in het menu.

   ![](assets/mouseover-ftpconnector.png)

   *Verbindingsoptie*

1. Er verschijnt een dialoogvenster waarin u wordt gevraagd de e-mail-ID in te voeren. Geef het e-mailadres op van de persoon die verantwoordelijk is voor het beheer van het FTP-account van Learning Manager voor de organisatie. Klik op **[!UICONTROL Verbinding maken]** nadat u de e-mail-id hebt verschaffend.
1. Learning Manager stuurt u een e-mail waarin de gebruiker wordt gevraagd het wachtwoord opnieuw in te stellen voordat hij/zij voor het eerst toegang krijgt tot de FTP. De gebruiker moet het wachtwoord opnieuw instellen en het gebruiken om toegang te krijgen tot het Learning Manager-FTP-account.

   >[!NOTE]
   >
   >Er kan slechts één Learning Manager FTP-account worden aangemaakt voor een bepaald Learning Manager-account.

   Op de overzichtspagina kunt u de verbindingsnaam voor uw integratie opgeven. Kies welke actie u wilt uitvoeren uit de volgende opties:

   * Interne gebruikers importeren
   * xAPI importeren
   * Vaardigheden van gebruikers exporteren - Een planning configureren
   * Vaardigheden van gebruikers exporteren - Op verzoek
   * Transcripties van lerende exporteren - Een schema configureren
   * De transcriptie van een leerling exporteren - OnDemand

   ![](assets/ftp-connector-dashboard.png)
   *Exportopties*

### Importeren

+++Interne gebruiker

Met de optie voor het importeren van interne gebruikers kunt u de gebruikers op aanvraag of in een planning importeren uit een CSV-bestand in een Learning Manager.

+++

+++Kenmerken toewijzen

Zodra de verbinding tot stand is gebracht, kunt u de kolommen van de CSV-bestanden toewijzen. Het bestand wordt in de FTP-map geplaatst bij de overeenkomstige attributen van Learning Manager. Deze stap is verplicht.

1. Op de pagina Kenmerken toewijzen zie je aan de linkerkant de verwachte kolommen van Learning Manager en aan de rechterkant de namen van de CSV-kolomnamen. In eerste instantie ziet u aan de rechterkant een leeg selectievakje. Importeer een CSV-sjabloon door op Bestand **kiezen te klikken**.
1. Via de bovenstaande stap worden alle CSV-kolomnamen aan de rechterkant van de vervolgkeuzelijst ingevuld. Selecteer de juiste kolomnaam die wordt toegewezen aan de kolomnaam van de leermanager.

   >[!NOTE]
   >
   >Het veld Manager moet worden toegewezen aan een veld van het type e-mailadres. U moet alle kolommen toewijzen voordat u de connector kunt gebruiken.

1. Klik op **[!UICONTROL Opslaan]** nadat de toewijzing is voltooid.

   De connector is nu klaar voor gebruik. Het geconfigureerde account verschijnt als gegevensbron in de beheerdersapp zodat de beheerder de import of de synchronisatie op verzoek kan plannen.



+++

+++De FTP-connector voor Learning Manager gebruiken

1. De CSV-bestanden van externe systemen moeten op het volgende pad worden geplaatst:

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   >[!NOTE]
   >
   >In de release van juli 2016 is alleen het importeren van gebruikers toegestaan. Als u de FTP-connector wilt gebruiken, moet u ervoor zorgen dat de CSV-bestanden in de volgende map zijn geplaatst:

   `code Home/import/user/internal/*.csv`

1. De FTP-connector neemt alle rijen uit CSV-bestanden. Het is belangrijk dat de rij die overeenkomt met een gebruiker in een CSV niet in andere CSV&#39;s verschijnt.
1. Alle CSV&#39;s moeten de kolommen bevatten die in de toewijzing zijn opgegeven.
1. Alle vereiste CSV&#39;s moeten aanwezig zijn in de map voordat het proces begint.

>[!NOTE]
>
>Tijdens het importeren van gebruikers in Learning Manager moet de beheerder ook weten hoe gebruikers worden beheerd in Learning Manager. Raadpleeg de Help](migration-manual.md#usermanagement) bij [Gebruikersbeheer voor meer informatie.

+++

+++XAPI importeren

Met de opties voor xAPI-import kunt u het importeren van xAPI-statements van externe diensten in Learning Manager op verzoek plannen.

+++

+++Configuraties vereist om xAPI te importeren

1. Selecteer op de configuratiepagina een bestaande configuratie die beschikbaar is in de configuratielijst om xAPI-instructies te importeren uit het CSV-bestand. Klik op Bewerken of **voeg een nieuwe configuratiekoppeling** toe om naar de pagina Importbronnen configureren te gaan.

   **Configuratie**

   * Vul de velden Naam en Naam van bronbestand op de pagina configureren-importeren-bronnen in. De naam van het bronbestand moet overeenkomen met de bestandsnaam die is in de FTP-maplocatie opgegeven.
   * Klik op **[!UICONTROL Opslaan]** om uw wijzigingen op te slaan.

   ![](assets/configurations.png)
   *Configureren*

   **Filteren**

   * Klik in het linkerdeelvenster op **[!UICONTROL Filteren]**.
   * Vul de velden Naam en Voorwaarden op de pagina configureren-importeren-filteren in om de records uit te filteren. Klik op **[!UICONTROL Nieuw filter toevoegen]** om een ander filter toe te voegen. U kunt een filter opslaan of verwijderen door in de kolom Acties op de optie **Opslaan** of **Verwijderen** te klikken.

   ![](assets/filter.png)
   *Filteren*

   **Toewijzing**

   * Klik in het linkerdeelvenster op **[!UICONTROL Toewijzing]**.
   * Op de pagina xAPI-statements importeren-Configuratie-Toewijzing ziet u aan de linkerkant de xAPI JSON-padveldnamen die aan de CSV-kolomnamen moeten worden toegewezen.
   * Standaard zijn de drie JSON-padveldnamen die aan de CSV-kolomnamen moeten worden toegewezen **actor.mbox**, **verb.id** en **object.id**. U kunt andere toe te wijzen velden toevoegen door op **Nieuwe toewijzing toevoegen** te klikken.

   * Selecteer het type kolomnaam dat u aan de Json-padveldnaam wilt toewijzen (of dit nu gaat een tekenreeks, nummer, Booleaan, of datumtype is).
   * Klik na het voltooien van de toewijzing op Opslaan. De xAPI-import kan nu volgens een planning of op verzoek worden geïmporteerd.

   ![](assets/mapping.png)
   *Toewijzing*

1. Klik in het linkerdeelvenster op **[!UICONTROL Planning configureren]**. Klik op **[!UICONTROL Planning inschakelen]** om het importeren van xAPI-statements te plannen.

   U kunt de starttijd en -datum invoeren en vervolgens de frequentie van uw xAPI-importplanning in dagen invoeren. Bijvoorbeeld, xAPI-import voor elke 3 dagen inschakelen.

   ![](assets/configure-schedule2x.png)
   *xAPI-instructies importeren - Schema configureren*

1. Klik in het linkerdeelvenster op **[!UICONTROL Uitvoeren van aanvraag]**.

   ![](assets/on-demand.png)
   *xAPI-instructies importeren - On Demand*

1. Klik in het linkerdeelvenster op **[!UICONTROL Uitvoeringsstatus]** om het overzicht van alle runs voor deze connector in chronologische volgorde weer te geven. U kunt de begindatum en de duur van de xAPI-import, het type import (op verzoek of volgens een planning) en de status van de import (of de xAPI-import in voortgang is, of voltooid of mislukt is) bekijken.

   ![](assets/execution-status2x.png)
   *xAPI-instructies importeren - Uitvoeringsstatus*

+++

### Badge als

+++Vaardigheden

Er zijn twee opties om rapporten over gebruikersvaardigheden te exporteren.

**[!UICONTROL Gebruikersvaardigheden - Op aanvraag]**: met de optie kunt u de begindatum opgeven en het rapport exporteren. Het rapport wordt geëxtraheerd van de ingevoerde datum tot heden.

![](assets/export-on-demand2x.png)
*Exportoptie op aanvraag*

**[!UICONTROL Gebruikersvaardigheden - Configureren]**: via deze optie kunt u de extractie van het rapport plannen. Selecteer het selectievakje Planning inschakelen en geef de begindatum en -tijd op. U kunt ook aangeven met welke intervallen u het rapport wilt laten genereren en verzenden.

![](assets/user-skills-configure.png)
*Export van rapport configureren*

+++

Als u de map Exporteren wilt openen waarin de geëxporteerde bestanden worden geplaatst, opent u de koppeling naar de FTP-map op de pagina Gebruikersvaardigheden, zoals hieronder wordt weergegeven.

![](assets/ftp-folder.png)
*FTP-map om bestanden weer te geven*

De automatisch geëxporteerde bestanden staan op de locatie **Start/Exporteren/&#42;FTP_location&#42;**

De automatisch geëxporteerde bestanden zijn beschikbaar met de titel, **skill_achievements_&#42;datum tot &#42;__&#42;en met.csv&#42;**

![](assets/exported-csvs.png)
*Geëxporteerd .csv bestand*

+++Transcript van lerende

![](assets/on-demand-report.png)

**Configureren**: met deze optie kunt u de extractie van het rapport plannen. Selecteer het selectievakje Planning inschakelen en geef de begindatum en -tijd op. U kunt ook aangeven met welke intervallen u het rapport wilt laten genereren en verzenden.

![](assets/configure-report.png)

+++

Als u de map Exporteren wilt openen waarin de geëxporteerde bestanden op uw FTP-locatie worden geplaatst, opent u de koppeling naar de FTP-map die op de transcriptiepagina van de gebruiker wordt weergegeven, zoals hieronder wordt getoond

De automatisch geëxporteerde bestanden staan op de locatie **Start/Exporteren/&#42;FTP_location&#42;**

De automatisch geëxporteerde bestanden zijn beschikbaar met de titel, **learner_transcript_datum tot &#42;__&#42;op heden en&#42; .csv&#42;**

![](assets/exported-file.png)

### Ondersteuning voor handmatige csv-velden {#supportformanualcsvfields}

Bij het importeren van gebruikersgegevens via FTP moet een beheerder alle actieve velden in het systeem toewijzen aan het juiste veld in de csv.

Dit is verplicht voor alle actieve csv-velden. Voor handmatig geactiveerde velden kan de integratiebeheerder de optie **DontImportFromSource** selecteren.

Door deze optie te selecteren worden de waarden van handmatig geactiveerde velden niet overschreven bij de csv-import. De door de student ingevulde waarden blijven intact.

>[!NOTE]
>
>Als tijdens de toewijzing de optie **DontImportFromSource** is geselecteerd voor een actief CSV-veld, wordt dit veld uit het systeem verwijderd.

![](assets/ftp-conector-foractivefields.png)
*FTP-connector voor actieve velden*

## Lynda-connector {#lyndaconnector}

De Lynda-connector wordt gebruikt door zakelijke klanten van Lynda.com die graag willen dat hun studenten Lynda-cursussen kunnen zoeken en volgen in Learning Manager. De connector kan worden geconfigureerd om periodiek cursussen van Lynda.com op te halen met uw API-sleutel. Zodra een cursus binnen Learning Manager is gemaakt, kunnen gebruikers deze opzoeken en volgen. De voortgang van de student kan vervolgens binnen Learning Manager worden bijgehouden.

### De Lynda-connector configureren {#configurethelyndaconnector}

1. Klik op Lynda in het dashboard van de integratiebeheerder.

   U ziet de tegel met drie opties: Aan de slag, Verbinden en Verbindingen beheren.

1. Klik op Verbinden als u de Lynda-connector voor het eerst configureert.

   <!--Configure the Exavault FTP account before you configure this connector.-->

1. Geef op de verbindingspagina een naam op voor uw connector. Voer de appsleutel en de geheime sleutel voor uw verbinding in.

   >[!NOTE]
   >
   >Neem contact op met uw leverancier voor de appsleutel en de geheime sleutel.

1. Klik op Opslaan.

   De configuratie wordt opgeslagen en de Lynda-verbinding voor uw account wordt toegevoegd. U kunt nu op Verbindingen beheren klikken op de startpagina en uw configuratie op elk gewenst moment bewerken.

1. Als u al een verbinding tot stand hebt gebracht, klikt u op Verbindingen beheren om al uw verbindingen te bekijken.

   >[!NOTE]
   >
   >De migratiefunctie moet zijn ingeschakeld voor uw account voordat u deze connector kunt configureren.

1. Klik op de verbinding die u wilt bewerken.
1. Klik **[!UICONTROL op Configureren]** in het linkerdeelvenster. Voer een van de volgende handelingen uit:

   * Bekijk of bewerk de details van uw account en het synchronisatieschema vanuit dit venster. Schakel het selectievakje Verbinding inschakelen in als u dit account wilt inschakelen.
   * Klik op Bewerken en bewerk uw gegevens. Klik op Herstellen om uw updates voor dit veld ongedaan te maken
   * Klik op Schema inschakelen om uw synchronisatie te plannen. U kunt de starttijd en -datum invoeren en vervolgens de frequentie van uw synchronisatieplanning in dagen invoeren. Bijvoorbeeld, om de drie dagen synchroniseren.

   Klik op **[!UICONTROL Opslaan]** om uw wijzigingen op te slaan.

   ![](assets/lynda.png)

   *De Lynda-connector configureren voor Learning Manager*

1. Klik in het linkerdeelvenster op Uitvoering op verzoek. Met deze optie kunt u gebruikersfeeds en andere relevante gegevens vanuit Lynda importeren. Voer de startdatum voor de uitvoering op verzoek in en klik op Uitvoeren om de synchronisatie uit te voeren. Alle gegevens vanaf de startdatum tot heden worden geïmporteerd.

   * Wanneer de toepassing tijdens de synchronisatie uitvalt, kunt u tijdens de uitvoering klikken op Toegang tot Learning Manager uitschakelen.
   * Als u tijdens de uitvoering op Toegang tot Learning Manager inschakelen klikt, is er geen onderbreking van de service tijdens de synchronisatie.

   ![](assets/lynda-ondemand.png)

   *Uitvoeren op aanvraag voor Lynda-connector*

1. U kunt ook op elk moment op Uitvoeringsstatus in het linkerdeelvenster klikken om het overzicht van alle runs voor deze connector in chronologische volgorde te bekijken. U kunt de startdatum en duur van de synchronisatie, het type synchronisatie (of het al dan niet gaat om synchronisatie op verzoek) en de status van de synchronisatie (of de synchronisatie wordt uitgevoerd of is voltooid) bekijken.

   >[!NOTE]
   >
   >Wanneer u een verbinding wist en opnieuw aanmaakt, worden de vorige runs voor de connector weergegeven. U kunt alle runs bekijken voordat u de verbinding wist.

   U kunt alleen de laatste synchronisatie opnieuw uitvoeren.

   ![](assets/lynda-ondemand.png)

   *Het overzicht van alle uitvoeringen weergeven door op Uitvoeringsstatus te klikken*

## getAbstract-connector {#getabstractconnector}

De getAbstract-connector kan gebruikt worden door zakelijke klanten van getAbstract.com die graag willen dat hun studenten getAbstract-samenvattingen kunnen zoeken en volgen in Captivate Prime. De connector kan worden geconfigureerd om periodiek gebruiksgegevens op te halen, op basis waarvan de voltooiingsrecords van studenten in Learning Manager worden gemaakt. Lees verder om te weten te komen hoe u deze connector in Learning Manager moet configureren.

### De getAbstract-connector configureren {#configurethegetabstractconnector}

1. Klik in het dashboard van de integratiebeheerder op getAbstract.

   U ziet de tegel met drie verschillende opties: Aan de slag, Verbinden en Verbindingen beheren.

1. Klik op Verbinden als u de getAbstract-connector voor het eerst configureert.

   <!--Configure the Exavault FTP account before you configure this connector.

   Ensure that you share this FTP credentials with your content provider to access the feeds.-->

1. Voer in het veld Verbindingsnaam een naam voor uw verbinding in.

   Voer de juiste sleutels in de velden Client-ID en Clientgeheim in. Neem contact op met uw leverancier voor de juiste sleutels voor deze connector.

   De sleutels zijn nodig om de metagegevens van de door de client gevolgde cursussen te verkrijgen.

1. Klik als u al verbinding hebt op de startpagina op getAbstract > Verbindingen beheren om uw bestaande configuratie te bekijken en te bewerken.

   >[!NOTE]
   >
   >De migratiefunctie moet zijn ingeschakeld voor uw account voordat u deze connector kunt configureren.

1. Klik op de verbinding waarvan u de configuratie wilt bekijken of bewerken.

   ![](assets/getabstractschedulepage.png)

   *De getAbstract-connector voor Learning Manager configureren*

1. Klik op Configureren in het linkerdeelvenster. Voer een van de volgende handelingen uit:

   * Bekijk of bewerk de details van uw account en het synchronisatieschema vanuit dit venster. Schakel het selectievakje Verbinding inschakelen in als u dit account wilt inschakelen.
   * Klik op Bewerken en bewerk uw gegevens. Klik op Herstellen om uw updates voor dit veld ongedaan te maken
   * Klik op Schema inschakelen om uw synchronisatie te plannen. U kunt de starttijd en -datum invoeren en vervolgens de frequentie van uw synchronisatieplanning in dagen invoeren. Bijvoorbeeld, om de drie dagen synchroniseren.

1. Klik op **[!UICONTROL Opslaan]**.

   De configuratie wordt opgeslagen en de getAbstract-verbinding voor uw account wordt toegevoegd.

1. Klik in het linkerdeelvenster op Uitvoering op verzoek. Met deze optie kunt u gebruikersfeeds en andere relevante gegevens uit getAbstract importeren. Voer de startdatum voor de uitvoering op verzoek in en klik op Uitvoeren om de synchronisatie uit te voeren. Alle gegevens vanaf de startdatum tot heden worden geïmporteerd.

   * Wanneer de toepassing tijdens de synchronisatie uitvalt, kunt u tijdens de uitvoering klikken op Toegang tot Learning Manager uitschakelen.
   * Als u tijdens de uitvoering op Toegang tot Learning Manager inschakelen klikt, is er geen onderbreking van de service tijdens de synchronisatie.

1. U kunt ook op elk moment op Uitvoeringsstatus in het linkerdeelvenster klikken om het overzicht van alle runs voor deze connector in chronologische volgorde te bekijken. U kunt de startdatum en duur van de synchronisatie, het type synchronisatie (of het al dan niet gaat om synchronisatie op verzoek) en de status van de synchronisatie (of de synchronisatie wordt uitgevoerd of is voltooid) bekijken.

   >[!NOTE]
   >
   >Wanneer u een verbinding wist en opnieuw aanmaakt, worden de vorige runs voor de connector weergegeven. U kunt alle runs bekijken voordat u de verbinding wist.

   U kunt alleen de laatste synchronisatie opnieuw uitvoeren.

   Zorg er voor elk type synchronisatie voor dat de gebruikersfeed aanwezig is in de getAbstract FTP-map voor de gegevens die in de synchronisatie zijn gespecificeerd.

   Raadpleeg het volgende Excelblad met een voorbeeld van een gebruikersfeed-bestand van getAbstract. De bestandsnaam moet het volgende formaat hebben: **rapport_export_jjjj_MM_dd_UUmmss.xlsx** of **report_export_jjjj_MMM_dd.xlsx**.
   [voorbeeld excelblad van getAbstract-gebruikersfeed](assets/report-export-20170401175342.xlsx)

## Harvard ManageMentor-connector {#hmmconnector}

De Harvard ManageMentor-connector wordt gebruikt door zakelijke klanten van Harvard ManageMentor die graag willen dat hun studenten Harvard ManageMentor-cursussen kunnen zoeken en volgen. De connector helpt bij het maken van cursussen binnen Learning Manager en kan worden geconfigureerd om periodiek de voortgangsgegevens van studenten op te halen. Voer de volgende procedure uit om deze connector te configureren:

### De Harvard ManagerMentor-connector configureren {#configuretheharvardmanagermentorconnector}

1. Klik in het dashboard van de integratiebeheerder op Harvard ManageMentor.

   U ziet de tegel met drie verschillende opties: Aan de slag, Verbinden en Verbindingen beheren.

1. Klik op Verbinden als u de Harvard ManageMentor-connector voor het eerst configureert.

   <!--Configure the Exavault FTP account before you configure this connector.

   Ensure that you share this FTP credentials with your content provider to access the feeds.-->

1. Voer in het veld Verbindingsnaam een naam voor uw verbinding in. Klik op Verbinden om deze verbinding op te slaan.
1. Klik als u al verbinding hebt op de startpagina op Harvard ManageMentor > Verbindingen beheren. Klik op de verbinding die u wenst te bewerken.

   >[!NOTE]
   >
   >De migratiefunctie moet zijn ingeschakeld voor uw account voordat u deze connector kunt configureren.

   ![](assets/hmm.png)

   *Configureer de HarvardManage Mentor connector voor Learning Manager*

1. Klik op Configureren in het linkerdeelvenster. Voer een van de volgende handelingen uit:

   * Bekijk of bewerk de details van uw account en het synchronisatieschema vanuit dit venster. Schakel het selectievakje Verbinding inschakelen in als u dit account wilt inschakelen.
   * Klik op Schema inschakelen om uw synchronisatie te plannen. U kunt de starttijd en -datum invoeren en vervolgens de frequentie van uw synchronisatieplanning in dagen invoeren. Bijvoorbeeld, om de drie dagen synchroniseren.

1. Klik in het linkerdeelvenster op Uitvoering op verzoek. Met deze optie kunt u gebruikersfeeds en andere relevante gegevens uit Harvard ManageMentor importeren. Voer de startdatum voor de uitvoering op verzoek in en klik op Uitvoeren om de synchronisatie uit te voeren. Alle gegevens vanaf de startdatum tot heden worden voor deze verbinding geïmporteerd.

   * Wanneer de toepassing tijdens de synchronisatie uitvalt, kunt u tijdens de uitvoering klikken op Toegang tot Learning Manager uitschakelen.
   * Als u tijdens de uitvoering op Toegang tot Learning Manager inschakelen klikt, is er geen onderbreking van de service tijdens de synchronisatie.

   Als u de synchronisatie om de paar dagen wilt automatiseren, geef dan het aantal dagen op in het veld Herhaal aantal dagen. Synchronisatie zorgt ervoor dat uw account wordt bijgewerkt met de laatste versie van de abstracts en samenvattingen van Harvard ManageMentor.

1. U kunt ook op elk moment op Uitvoeringsstatus in het linkerdeelvenster klikken om het overzicht van alle runs voor deze connector in chronologische volgorde te bekijken. U kunt de startdatum en duur van de synchronisatie, het type synchronisatie (of het al dan niet gaat om synchronisatie op verzoek) en de status van de synchronisatie (of de synchronisatie wordt uitgevoerd of is voltooid) bekijken.

   >[!NOTE]
   >
   >Wanneer u een verbinding wist en opnieuw aanmaakt, worden de vorige runs voor de connector weergegeven. U kunt alle runs bekijken voordat u de verbinding wist.

   U kunt alleen de laatste synchronisatie opnieuw uitvoeren.

   Om de synchronisatie te laten slagen, moet u ervoor zorgen dat ten minste één van de volgende bestanden aanwezig is in de FTP-map van Harvard ManageMentor:

   hmm12_metadata.xlsx: Dit bestand geeft de cursusmetagegevens voor de Harvard ManageMentor-connector. Zorg ervoor dat u de naamconventie volgt wanneer u het bestand uploadt.

   client_hmm12_20150125.xlsx: dit is de gebruikersfeed voor de Harvard ManageMentor-connector. De bestandsnaamconventie die gevolgd moet worden is **client_hmm12_yyyyMMMdd.xlsx.**

   Zie de volgende twee voorbeelden van gebruikersfeed- en cursusfeed-bestanden voor deze connector:

   * [Cursusmetagegevensbestand voor de Harvard ManageMentor connector](assets/hmm12-metadata.xlsx)
   * [Gebruikersfeed voor de Harvard ManageMentor-connector](assets/client-hmm12-20170304.xlsx)

## Workday-connector {#workdayconnector}

Met behulp van de Workday-connector kunt u Learning Manager integreren met Workday tenant om de synchronisatie van gegevens te automatiseren.

### Importeren

#### Kenmerken toewijzen

De integratiebeheerder kan Workday-kolommen kiezen en aan de overeenkomstige groepeerbare kenmerken van Learning Manager toewijzen. Wanneer de toewijzing is voltooid, wordt dezelfde toewijzing voor verdere gebruikersimporten gebruikt. De beheerder kan de toewijzing opnieuw configureren als deze een andere toewijzing voor het importeren van gebruikers wil.

#### Geautomatiseerde gebruikersimport

Met het gebruikersimportproces kan de Learning Manager Administrator werknemersgegevens uit Workforce halen en ze automatisch in Learning Manager importeren.

#### Gebruikers filteren

Learning Manager Administrator kan gebruikers filteren voordat ze worden geïmporteerd. Zo kan de Learning Manager-beheerder er bijvoorbeeld voor kiezen om alle gebruikers in de hiërarchie onder één of meer specifieke managers te importeren.

### Exporteren

Via Gebruikersvaardigheden exporteren kunnen gebruikers automatisch gebruikersvaardigheden naar Workday exporteren.

>[!NOTE]
>
>Het is niet mogelijk vaardigheden van meerdere Learning Manager-accounts tegelijkertijd met hetzelfde Workday-account te exporteren.

#### Punten om te notitie

* Zorg ervoor dat de UUID, het e-mailadres en de naam van de werknemer uniek zijn in meerdere Workday-integraties. Onjuiste waarden leiden tot een fout in de verbinding.
* Het UUID-veld dat is ingevuld via Workday on kan niet worden verwijderd door een LMS-beheerder met wie een client te maken heeft. Als je de waarde wilt wijzigen, neem je contact op met het introductie- of ondersteuningsteam van Adobe Learning Manager.
* De optie Gebruiker leegmaken werkt mogelijk ook niet, omdat Gebruikers leegmaken slechts 50 gebruikers per run ondersteunt. Wees uiterst voorzichtig bij het uploaden van de gebruikers via de UUID&#39;s.

### Planning {#Scheduling-1}

De beheerder kan planningstaken volgens de vereisten van de organisatie instellen en gebruikers in de Learning Manager-toepassing zijn up-to-date volgens de planning. Op dezelfde manier kan de integratiebeheerder de export van vaardigheden op een tijdige basis plannen om deze te integreren met een extern systeem. De synchronisatie kan dagelijks worden uitgevoerd in de Learning Manager-toepassing.

### De Workday-connector configureren {#configureworkdayconnector}

>[!PREREQUISITES]
>
>Vraag de Workday-beheerder van uw organisatie om een ISU (Integration System User) te maken met de machtigingen zoals gedefinieerd in het ISU_Permissions document. Download een exemplaar via onderstaande link.

[Download een kopie van isu-beveiliging (Integration System User).](assets/isu-permissions-v1.pdf) Leer dit proces om de Workday-connector te integreren met Learning Manager.

1. Plaats de muisaanwijzer op de Workday-tegel op de startpagina van Learning Manager. Er verschijnt een menu. Klik op **[!UICONTROL Verbinden]** in het menu.

   ![](assets/workday-tile.png)

   *Workday-tegel*

1. Er verschijnt een dialoogvenster waarin u wordt gevraagd de gegevens voor de nieuwe verbinding in te voeren. Voer de volgende velden in voordat u de verbinding tot stand brengt.

   * Verbindingsnaam: voer een verbindingsnaam naar keuze in.
   * Host-URL: de integratiebeheerder kan de host-URL-details bij de desbetreffende Workday-beheerder opvragen.
   * Tenant: De tenant is intern in uw bedrijf. U ontvangt de gegevens van de tenant van de Workday-beheerder.
   * Gebruikersnaam en wachtwoord: de Workday-beheerder maakt een geïntegreerde systeemgebruiker (ISU) met de vereiste beveiligingsrechten en deelt deze met de integratiebeheerder.

>[!NOTE]
>
>   Learning Manager gebruikt versie 40.1 van de Workday-API.


![](assets/configure-connector.png)
*Workday-connector configureren*

1. Klik op Verbinden na het invoeren van informatie in alle relevante velden.

   >[!NOTE]
   >
   >U kunt ook meerdere Workday-verbindingen laten synchroniseren met uw Learning Manager-account.

Op de overzichtspagina kunt u de verbindingsnaam voor uw integratie opgeven. Kies uit de volgende opties welke actie u wilt ondernemen:

* Interne gebruikers importeren
* Vaardigheden van gebruikers exporteren - Een planning configureren
* Vaardigheden van gebruikers exporteren - Op verzoek

![](assets/overview.png)
*Overzicht van Workday*

### Importeren

#### Kenmerken toewijzen {#MapAttributes-1}

U kunt de Workday-connector gebruiken om Learning Manager en Workday te integreren om de synchronisatie van gegevens te automatiseren. U kunt alle actieve gebruikers van Workday naar Learning Manager importeren. Gebruikers kunnen worden geïmporteerd vanuit verschillende gegevensbronnen, waaronder FTP en Salesforce.

Voordat gebruikers kunnen worden geïmporteerd, moeten de gebruikersattributen van Learning Manager en Workday worden toegewezen. Kies op de overzichtspagina onder Importeren voor de optie Interne gebruikers om de toewijzingsattributen op te geven.

Voer de Adobe Learning Manager-gegevens in de kolom onder Adobe Learning Manager. Gebruik de vervolgkeuzelijsten om de juiste gegevens te selecteren voor de kolommen onder Workday.

>[!NOTE]
>
>Momenteel ondersteunt Learning Manager het importeren van 69 gebruikersattributen uit Workday. Voeg via de actieve velden in Learning Manager meer attributen toe.

![](assets/workday.png)
*Kenmerken toewijzen*

Schakel het **selectievakje Tijdelijk personeel** uitsluiten in om te voorkomen dat tijdelijke werknemers die beschikbaar zijn onder een manager, worden geïmporteerd.

Workday heeft vier hiërarchieniveaus, terwijl Learning Manager twee niveaus heeft. De vier niveaus in Workday zijn de categorie met het vaardigheidsprofiel, het skillprofiel, de categorie met een skill-item en een skill-item. Uw vaardigheidsnaam en het niveau van Learning Manager worden samen in Workday toegewezen onder het item &#39;Skill&#39;.

>[!NOTE]
>
>U kunt extra Workday-attributen toevoegen. Neem contact op met uw CSAM om de attributen toe te voegen.

+++Lijst met ondersteunde Workday-kenmerken

wd:User_ID
wd:Worker_ID
directeur
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.@wd:Formatted_Name
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.@wd:Formatted_Name
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:Prefix_Data.wd:Title_Descriptor
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:Prefix_Data.wd:Title_Descriptor
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:First_Name
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:Last_Name
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:First_Name
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:Last_Name
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.@wd:Formatted_Address
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Postal_Code
wd:Personal_Data.wd:Contact_Data.wd:Email_Address_Data.0.wd:Email_Address
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Country_Region_Descriptor
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.@wd:Formatted_Phone
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:Country_ISO_Code
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:International_Phone_Code
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:Phone_Number
wd:Personal_Data.wd:Primary_Nationality_Reference.wd:ID.1.$
wd:Personal_Data.wd:Gender_Reference.wd:ID.1.$
wd:Personal_Data.wd:Identification_Data.wd:National_ID.0.wd:National_ID_Data.wd:ID
wd:Personal_Data.wd:Identification_Data.wd:Custom_ID.0.wd:Custom_ID_Data.wd:ID
wd:User_Account_Data.wd:Default_Display_Language_Reference.wd:ID.1.$
wd:Role_Data.wd:Organization_Role_Data.wd:Organization_Role.0.wd:Organization_Role_Reference.wd:ID.1.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Position_Title
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Title
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Naam
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.@wd:Formatted_Address
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Classification_Summary_Data.0.wd:Job_Classification_Reference.wd:ID.1.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Classification_Summary_Data.0.wd:Job_Group_Reference.wd:ID.1.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Work_Space__Reference.wd:ID.1.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Profile_Summary_Data.wd:Job_Family_Reference.0.wd:ID.1.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Profile_Summary_Data.wd:Job_Profile_Name
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Profile_Summary_Data.wd:Job_Profile_Reference.wd:ID.1.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.0.wd:Country_Reference.wd:ID.2.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Worker_Type_Reference.wd:ID.1.$
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.0.@wd:Formatted_Address
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Profile_Summary_Data.wd:Management_Level_Reference.wd:ID.1.$
wd:Employment_Data.wd:Worker_Status_Data.wd:Active
wd:Employment_Data.wd:Worker_Status_Data.wd:Active_Status_Date
wd:Employment_Data.wd:Worker_Status_Data.wd:Hire_Date
wd:Employment_Data.wd:Worker_Status_Data.wd:Original_Hire_Date
wd:Employment_Data.wd:Worker_Status_Data.wd:Gepensioneerd
wd:Employment_Data.wd:Worker_Status_Data.wd:Retirement_Date
wd:Employment_Data.wd:Worker_Status_Data.wd:Beëindigd
wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Date
wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Last_Day_of_Work
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Code
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Name
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Type_Reference.wd:ID.1.$
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Subtype_Reference.wd:ID.1.$
wd:Qualification_Data.wd:Education.0.wd:School_Name
wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Job_Title
wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Bedrijf
wd:Management_Chain_Data.wd:Worker_Supervisory_Management_Chain_Data.wd:Management_Chain_Data.0.wd:Manager.Employee_ID
Primaire e-mail voor je werk
wd:Organization_Type_Reference_Cost_Center_ID
wd:Organization_Type_Reference_Cost_Center_Name
wd:Organization_Type_Reference_Company
wd:Organization_Subtype_Reference_Department
wd:Organization_Subtype_Reference_Division
wd:Universal_ID
wd:Integration_Field_Override_Data.3.wd:Waarde
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.0.wd:Country_Region_Descriptor
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.0.wd:Country_Region_Reference.wd:ID.2.$
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Gemeente

+++

### Exporteren

U kunt alle vaardigheden van een gebruiker van Learning Manager naar Workday exporteren. Alleen actieve gebruikersvaardigheden worden geëxporteerd en Learning Manager exporteert geen gearchiveerde vaardigheden. Je kunt ook meerdere Learning Manager verbinden\
naar dezelfde Workday-connector. Als de vaardigheidsnamen gelijk zijn in twee Learning Manager-accounts, worden deze toegewezen aan dezelfde vaardigheid in Workday. Voordat u de vaardigheid in Workday bijwerkt, is het raadzaam om, voor het geval twee Learning Manager-accounts hetzelfde Workday-account gebruiken, de vaardigheidsnamen in alle Learning Manager-accounts bij te werken.

+++Gebruikersvaardigheden - Configureren

Met deze optie kunt u de extractie van het rapport plannen. Zorg ervoor dat het selectievakje Exporteren van gebruikersvaardigheden via deze verbinding inschakelen is ingeschakeld. Selecteer het selectievakje Planning inschakelen en geef de begindatum en -tijd op. U kunt ook aangeven met welke intervallen u het rapport wilt laten genereren en verzenden. Schakel het selectievakje Planning inschakelen in en voer de startdatum, tijd en herhaling na een bepaald aantal dagen in. Klik op Opslaan als u klaar bent.

![](assets/configure-schedule.png)
*Rapport met gebruikersvaardigheden configureren*

+++

+++Gebruikersvaardigheden - op aanvraag

U kunt de begindatum opgeven en het rapport exporteren met deze optie. Het rapport wordt geëxtraheerd van de ingevoerde datum tot heden. Voer de datum in vanaf wanneer u wilt beginnen met het genereren van het rapport en klik op Uitvoeren.

![](assets/on-demand-report.png)
*Rapport over on-demand gebruikersvaardigheden*

+++

+++Gebruikersvaardigheden - Uitvoeringsstatus

Hier kunt u de samenvatting van alle taken bekijken en een statusrapport daarvan ontvangen. U kunt foutrapporten downloaden door op de foutrapportagelink te klikken.

![](assets/execution-status.png)
*Rapport over het uitvoeren van gebruikersvaardigheden*

+++

## miniOrange-connector {#miniorangeconnector}

Met behulp van de miniOrange-connector kunt u Learning Manager integreren met miniOrange-tenant om de synchronisatie van gegevens te automatiseren.

### Importeren

#### Kenmerken toewijzen

De integratiebeheerder kan miniOrange-kenmerken kiezen en deze toewijzen aan de bijbehorende groepskenmerken van Learning Manager. Wanneer de toewijzing is voltooid, wordt dezelfde toewijzing voor verdere gebruikersimporten gebruikt. De beheerder kan de toewijzing opnieuw configureren als deze een andere toewijzing voor het importeren van gebruikers wil.

#### Geautomatiseerde gebruikersimport

Bij het importeren van gebruikers kan Learning Manager-beheerder de gegevens van werknemers ophalen uit miniOrange en deze automatisch importeren in Learning Manager.

#### Gebruikers filteren

Learning Manager Administrator kan gebruikers filteren voordat ze worden geïmporteerd. Zo kan de Learning Manager-beheerder er bijvoorbeeld voor kiezen om alle gebruikers in de hiërarchie onder één of meer specifieke managers te importeren.

Als u de miniOrange-connector wilt instellen, neemt u contact op met het CSM-team van Learning Manager.

### De miniOrange-connector configureren {#configureminiorangeconnector}

1. Houd op de startpagina van Learning Manager de muis boven de miniOrange-kaart/miniatuur. Er verschijnt een menu. Klik op  **[!UICONTROL de optie Verbinden]** in het menu.

   ![](assets/miniorange-tile.png)

   *tegel miniOrange-connector*

1. Klik op **[!UICONTROL Verbinden]** om een nieuwe verbinding tot stand te brengen. De pagina van connector miniOrange wordt weergegeven. Vul de gegevens in van het account dat u wenst toe te wijzen.

   ![](assets/establish-connection.png)

   *Een verbinding maken*

1. Als u de gebruiker miniOrangeer rechtstreeks wilt importeren als een interne gebruiker van Learning Manager, gebruikt u de **[!UICONTROL optie Interne gebruikers]** importeren.

   ![](assets/import-users.png)

   *Interne gebruikers importeren*

1. Op de toewijzingspagina zie je links de kolommen van Learning Manager en aan de rechterkant de miniOrnage-kolommen. Selecteer de juiste kolomnaam die wordt toegewezen aan de kolomnaam van de leermanager.

   ![](assets/map-attributes.png)

   *Kenmerken toewijzen*

1. Klik, als u de gegevensbron als beheerder wilt bekijken bewerken, op **[!UICONTROL Instellingen > Gegevensbron]**.

   De bestaande miniOrange-bron wordt vermeld. Als u het filter wilt bewerken, klikt u op **[!UICONTROL Bewerken]**.

   ![](assets/data-source.png)

   *Een gegevensbron weergeven en bewerken*

1. U ontvangt een melding na voltooiing van de import. Klik op **[!UICONTROL Gebruikers > Importlogboek]** om het importlogboek te bekijken of te bewerken.

<!-- #### Delete a connection {#deleteaconnection}

To delete an established  miniOrange  connection, follow these steps. -->

## Zoomconnector {#zoom-connector}

U kunt Learning Manager integreren met Zoom-connectoren en deze gebruiken om lessen te hosten.  Met de connector kunt u videoconferenties/lessen instellen met de studenten.

Volg deze stappen om de connector in te stellen en te gebruiken.

1. Plaats op de startpagina van Learning Manager de muis op de miniatuur Zoomen. Er verschijnt een menu. Klik op  **[!UICONTROL de optie Verbinden]** in het menu.

   <!-- ![](assets/connectors.png)

   *Zoom connector tile* -->

1. De pagina Connector zoomen wordt geopend. Voer de gegevens van uw account in de desbetreffende velden in om de gebruikersfeed te integreren en te synchroniseren. U kunt de gegevens van de beheerder van uw connectoraccount opvragen.

   <!-- ![](assets/bluejeans-connecotrpage.png)
   *Connect to BlueJeans/ Zoom* -->

   >[!NOTE]
   >
   >Als student gebruikt u bij het inschakelen van de connector dezelfde e-mail-ID die gebruikt wordt voor uw Learning Manager-account om gebruikersfeeds terug te laten keren naar Learning Manager.

1. Zodra de verbinding tot stand is gebracht, kunt u als auteur een VC-cursus maken met Zoom als het conferentiesysteem.

   <!-- ![](assets/vc.jpg)
   
   *Create a VC course* -->

1. Beheerders, beheerders en studenten kunnen studenten inschrijven voor de gemaakte cursus. Bij inschrijving ontvangt de student een e-mail. De student kan zich aanmelden op zijn Learning Manager-account om de details van het programma te bekijken en de cursus te volgen.
1. Na afloop van de cursus wordt het eindrapport naar Learning Manager gestuurd. De beheerder kan het voltooiingsrapport bekijken om de aanwezigheid en de score van de studenten te controleren.

   ![](assets/attendence-and-scoringreport.png)
   *Aanwezigheids- en scorerapport*

### Een zoom-server-naar-server OAuth-app maken

Wanneer u een Zoom Server-to-Server OAuth-app maakt voor gebruik in Adobe Learning Manager, moet u tijdens het maken van de verbinding bereiken toevoegen die Adobe Learning Manager vereist heeft.

Voor Adobe Learning Manager zijn de onderstaande bereiken vereist. De bereiken moeten worden geselecteerd in de OAuth-app.

* Alle vergaderingen van gebruikers weergeven `/meeting:read:admin`
* Alle vergaderingen van gebruikers weergeven en beheren `/meeting:write:admin`
* Rapportgegevens weergeven `/report:read:admin`
* Alle gebruikersinformatie weergeven `/user:read:admin`
* Gebruikersinformatie weergeven en beheren `/user:write:admin`

## Box-connector {#boxconnector}

Met de Box-connector kunt u Learning Manager integreren met willekeurige externe systemen om de synchronisatie van gegevens te automatiseren. Naar verwachting kunnen externe systemen gegevens exporteren in een CSV-indeling en deze in de juiste map van het Learning Manager Box-account plaatsen. De mogelijkheden van de Box-connector zijn als volgt:

U kunt de FTP-connector ook gebruiken voor gegevensmigratie, gebruikers importeren en gegevens exporteren. Ga voor meer informatie naar [Learning Manager FTP-connector.](connectors.md#main-pars_header_1427405935)

### Gegevensimport {#DataImport-1}

Met het gebruikersimportproces kan de Learning Manager Administrator werknemersgegevens uit de Learning Manager Box-service halen en ze automatisch in Learning Manager importeren. Met behulp van deze functie kunt u meerdere systemen integreren door de door deze systemen gegenereerde CSV in de juiste mappen van de Box-accounts te plaatsen. Learning Manager haalt de CSV-bestanden op, voegt ze samen en importeert de gegevens volgens de planning. Raadpleeg de planningsfunctie voor meer informatie.

**Kenmerken toewijzen**

Kenmerken toewijzen Deze toewijzing is één tijdsinspanning. Zodra de toewijzing is voltooid, wordt dezelfde toewijzing gebruikt voor de daaropvolgende gebruikersimporten. De toewijzing kan opnieuw worden geconfigureerd als de beheerder een andere toewijzing voor het importeren van gebruikers wil hebben.

## Gegevensexport {#dataexport}

De gegevensexport stelt gebruikers in staat om de vaardigheden van de gebruiker en de studenttranscripten te exporteren naar een Box-locatie om deze te integreren met een willekeurig extern systeem.

## Rapporten plannen {#schedulereports}

De beheerder kan planningstaken volgens de vereisten van de organisatie instellen en gebruikers in de Learning Manager-toepassing zijn up-to-date volgens de planning. Op dezelfde manier kan de integratiebeheerder de export van vaardigheden op een tijdige basis plannen om deze te integreren met een extern systeem. De synchronisatie kan dagelijks worden uitgevoerd in de Learning Manager-toepassing.

## Box-connector configureren {#configureboxconnector}

Leer het proces om Box Connector te integreren met Learning Manager.

1. Op de startpagina van Learning Manager houdt u de muis boven de boxkaart/miniatuur. Er verschijnt een menu. Klik op het item Verbinden in het menu.

   ![](assets/screen-shot-2017-10-25at54426pm.png)

   *Verbinding maken met Box*

1. Er verschijnt een dialoogvenster waarin u wordt gevraagd de e-mail-ID in te voeren. Geef het e-mailadres op van de persoon die verantwoordelijk is voor het beheer van het Learning Manager Box-account voor de organisatie. Klik op Verbinding maken nadat u de e-mail-id hebt verschaffend.
1. Learning Manager stuurt u een e-mail waarin de gebruiker wordt gevraagd het wachtwoord opnieuw in te stellen voordat hij/zij voor het eerst toegang krijgt tot de Box. De gebruiker moet het wachtwoord opnieuw instellen en gebruiken om toegang te krijgen tot het account van Learning Manager Box.

   >[!NOTE]
   >
   >Er kan slechts één Learning Manager Box-account worden gemaakt voor een bepaald Learning Manager-account.

   Op de overzichtspagina kunt u de verbindingsnaam voor uw integratie opgeven. Kies welke actie u wilt uitvoeren uit de volgende opties:

   * Interne gebruikers importeren
   * xAPI-activiteitsrapporten importeren
   * Vaardigheden van gebruikers exporteren - Een planning configureren
   * Vaardigheden van gebruikers exporteren - Op verzoek
   * Transcriptie voor lerende exporteren - Een schema configureren
   * Export Learner Transcript - OnDemand

## Importeren

+++Interne gebruiker

Met de optie voor het importeren van interne gebruikers kunt u het genereren van een gebruikersimportverslag automatisch plannen. De gegenereerde rapporten worden als .CSV-bestanden naar u verzonden.

+++

+++Toewijzingskenmerken

Nadat een verbinding tot stand is gebracht, kunt u de kolommen met CSV-bestanden die in de map Box zijn geplaatst, toewijzen aan de overeenkomstige kenmerken van Leerbeheer. Deze stap is verplicht.

1. Op de pagina Kenmerken toewijzen zie je aan de linkerkant de verwachte kolommen van Learning Manager en aan de rechterkant de namen van de CSV-kolomnamen. In eerste instantie ziet u aan de rechterkant een leeg selectievakje. Importeer een CSV-sjabloon door op Bestand kiezen te klikken.
1. Via de bovenstaande stap worden alle CSV-kolomnamen aan de rechterkant van de vervolgkeuzelijst ingevuld. Selecteer de juiste kolomnaam die wordt toegewezen aan de kolomnaam van de leermanager.

   *Het veld Manager moet worden toegewezen aan een veld met het type e-mailadres. U moet alle kolommen toewijzen voor u de connector kunt gebruiken.*

1. Klik op Opslaan nadat de toewijzing is voltooid.

   De connector is nu klaar voor gebruik. Het geconfigureerde account verschijnt als gegevensbron in de beheerdersapp zodat de beheerder de import of de synchronisatie op verzoek kan plannen.

+++

+++xAPI-activiteitsrapport

Met de optie xAPI-activiteitsrapport kunt u de import van xAPI-statements uit externe diensten genereren. De bestanden worden als CSV-bestanden opgeslagen en vervolgens geconverteerd naar xAPI-statements tijdens het importeren in Learning Manager.

+++

+++Configuraties vereist om xAPI te importeren

1. Selecteer op de configuratiepagina een bestaande configuratie die beschikbaar is in de configuratielijst om xAPI-instructies te importeren uit het CSV-bestand. Klik op Bewerken of Kies een **nieuwe configuratiekoppeling** om naar de pagina xAPI-instructies- Configuratiebestand importeren te gaan.

   ![](assets/artboard-11-2x.png)

   *Een nieuwe configuratie bewerken of toevoegen*

   **Configuratie**

   * Vul de velden Naam en Naam van bronbestand op de pagina configureren-importeren-bronnen in. De naam van het bronbestand moet overeenkomen met de bestandsnaam die is in de FTP-maplocatie opgegeven.
   * Klik op **[!UICONTROL Opslaan]** om uw wijzigingen op te slaan.

   ![](assets/configurations-main2x.png)

   *Configureren*

   **Filteren**

   * Klik in het linkerdeelvenster op Filteren
   * Vul de velden Naam en Voorwaarden op de pagina configureren-importeren-filteren in om de records uit te filteren. Klik op Nieuw filter toevoegen om een ander filter toe te voegen. U kunt een filter opslaan of verwijderen door in de kolom Acties op de optie Opslaan of Verwijderen te klikken.

   ![](assets/box-filter-2x.png)

   *Filteren*

   **Toewijzing**

   * Klik in het linkerdeelvenster op Toewijzing.
   * Op de pagina Configureren-Importeren-Toewijzing ziet u aan de linkerkant de xAPI JSON-padveldnamen die aan de CSV-kolomnamen moeten worden toegewezen.
   * Standaard zijn de drie JSON-padveldnamen die aan de CSV-kolomnamen moeten worden toegewezen **actor.mbox**, **verb.id** en **object.id**. U kunt andere toe te wijzen velden toevoegen door op Nieuwe toewijzing toevoegen te klikken.
   * Selecteer het type kolomnaam dat u aan de Json-padveldnaam wilt toewijzen (of dit nu gaat een tekenreeks, nummer, Booleaan, of datumtype is).
   * Klik na het voltooien van de toewijzing op Opslaan. De xAPI-import kan nu volgens een planning of op verzoek worden geïmporteerd.

   ![](assets/box-mapping-2x.png)
   *Toewijzing*

1. Klik in het linkerdeelvenster op **[!UICONTROL Planning configureren]**. Klik op Planning inschakelen om het importeren van xAPI-statements te plannen. U kunt de starttijd en -datum invoeren en vervolgens de frequentie van uw xAPI-importplanning in dagen invoeren. Bijvoorbeeld, xAPI-import voor elke 3 dagen inschakelen.

   ![](assets/configure-schedulebox2x.png)
   *xAPI-instructies importeren - Schema configureren*

1. Klik in het linkerdeelvenster op **[!UICONTROL Uitvoeren van aanvraag]**.

   ![](assets/box-on-demand-2x.png)
   *XAPI-instructies importeren - On Demand*

1. Klik in het linkerdeelvenster op **[!UICONTROL Uitvoeringsstatus]** om het overzicht van alle runs voor deze connector in chronologische volgorde weer te geven. U kunt de begindatum en de duur van de xAPI-import, het type import (op verzoek of volgens een planning) en de status van de import (of de xAPI-import in voortgang is, of voltooid of mislukt is) bekijken.

   ![](assets/box-execution-status2x.png)
   *xAPI-instructies importeren - Uitvoeringsstatus*

+++

+++De connector Van Het vak Leerbeheer gebruiken

1. De CSV-bestanden van externe systemen moeten op het volgende pad worden geplaatst:

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   >[!NOTE]
   >
   >In de release van juli 2016 is alleen het importeren van gebruikers toegestaan. Als u de Box-connector wilt gebruiken, moet u ervoor zorgen dat de CSV-bestanden in de volgende map zijn geplaatst:

   `code Home/import/user/internal/*.csv`

1. De Box-connector neemt alle rijen uit CSV-bestanden. Het is belangrijk dat de rij die overeenkomt met een gebruiker in een CSV niet in andere CSV&#39;s verschijnt.
1. Alle CSV&#39;s moeten de kolommen bevatten die in de toewijzing zijn opgegeven.
1. Alle vereiste CSV&#39;s moeten aanwezig zijn in de map voordat het proces begint.

Bij het importeren van gebruikers in Learning Manager, moet de beheerder ook weten hoe gebruikers in Learning Manager beheerd worden. Raadpleeg de Help](migration-manual.md#usermanagement) bij [Gebruikersbeheer voor meer informatie.

+++

## Badge als

+++Vaardigheden

Er zijn twee opties om rapporten over gebruikersvaardigheden te exporteren.

Gebruikersvaardigheden - Op verzoek: u kunt via deze optie de startdatum specificeren en het rapport exporteren. Het rapport wordt geëxtraheerd vanaf de ingevoerde datum tot heden

**[!UICONTROL Gebruikersvaardigheden - Configureren]**: via deze optie kunt u de extractie van het rapport plannen. Selecteer het selectievakje Planning inschakelen en geef de begindatum en -tijd op. U kunt ook aangeven met welke intervallen u het rapport wilt laten genereren en verzenden.

+++

Als u de map Export wilt openen waarin de geëxporteerde bestanden op uw Box-locatie worden geplaatst, opent u de koppeling naar de Box-map op de pagina Gebruikersvaardigheden, zoals hieronder wordt weergegeven.

De automatisch geëxporteerde bestanden staan op de locatie **Start/Exporteren/&#42;Box_location&#42;**

De automatisch geëxporteerde bestanden zijn beschikbaar met de titel, **skill_achievements_&#42;datum tot &#42;__&#42;en met.csv&#42;**

>[!NOTE]
>
>De klant beheert de toegangsmachtigingen en de inhoud in de Box-map die wordt gedeeld door het Learning Manager-team.  Ook wordt de inhoud in de map fysiek opgeslagen in de regio Frankfurt.

### Ondersteuning voor handmatige csv-velden {#Supportformanualcsvfields-1}

Bij het importeren van gebruikersgegevens via Box moet een beheerder alle actieve velden in het systeem toewijzen aan het juiste veld in de csv.

Dit is verplicht voor alle actieve csv-velden. Voor handmatig geactiveerde velden kan de integratiebeheerder de optie **DontImportFromSource** selecteren.

Door deze optie te selecteren worden de waarden van handmatig geactiveerde velden niet overschreven bij de csv-import. De door de student ingevulde waarden blijven intact.

>[!NOTE]
>
>Als tijdens de toewijzing de optie **DontImportFromSource** is geselecteerd voor een actief CSV-veld, wordt dit veld uit het systeem verwijderd.

![](assets/box-connector-foractivefields.png)
*Box-connector voor actieve velden*

>[!NOTE]
>
>Elke connector of migratie, die gebruik maakt van FTP/Box als gegevensbron, zal alle csv-bestanden die worden verwerkt, verwijderen.
>
>Het csv-bestand voor de inhoudconnectoren, bijvoorbeeld LinkedIn, zal na zeven dagen worden verwijderd, terwijl het csv-bestand voor het importeren van gebruikers onmiddellijk zal worden verwijderd.

## LinkedIn Learning-connector {#linkedinlearningconnector}

De LinkedIn Learning-connector wordt gebruikt door zakelijke klanten van LinkedIn.com die graag willen dat hun studenten cursussen kunnen zoeken en volgen in Learning Manager. De connector kan worden geconfigureerd om periodiek cursussen op te halen met uw API-sleutel. Zodra een cursus binnen Learning Manager is gemaakt, kunnen gebruikers deze opzoeken en volgen. De voortgang van de student kan vervolgens binnen Learning Manager worden bijgehouden.

>[!NOTE]
>
>U krijgt de unieke LO-id&#39;s voor alle cursussen die zijn geïmporteerd vanuit de LinkedIn-connector voor leren naar Adobe Learning Manager.

>[!NOTE]
>
>De tijd die wordt besteed aan cursussen van LinkedIn Learning wordt via het LinkedIn Content/LinkedIn-platform doorgegeven aan het Learning Manager-studieplatform. Als LinkedIn Learning de studietijd niet doorstuurt, kan deze tijd niet door ons studieplatform worden geregistreerd. In dat geval is de leertijd die door Learning Manager is besteed, nul.

### Instellingen configureren in Linkedln Learning-portaal {#configuresettingsinlinkedlnlearningportal}

1. Meld u als beheerder aan bij Linkedln Learning LMS.
1. Klik op **[!UICONTROL Beheer]** in het navigatievenster boven aan het scherm.
1. Klik op het tabblad **[!UICONTROL Instellingen]** in het volgende venster.
1. Selecteer **[!UICONTROL Afspeelintegratie]** in het linkernavigatievenster en klik vervolgens op het **tabblad Integratie** .
1. Klik op **[!UICONTROL Start-instellingen]** VOOR LMS-inhoud om de bijbehorende instellingen uit te vouwen.
1. Voeg de volgende drie hostnamen toe: **learningmanager.adobe.com**, **learningmanagerlrs.adobe.com**, **cpcontents.adobe.com**
1. Selecteer **[!UICONTROL AICC-integratie inschakelen]**.

   ![](assets/linkedin-learning.png)

   *LinkedIn Leren configureren*

### LinkedIn Learning-connector configureren {#configurelinkedinlearningconnector}

1. Klik in het dashboard van integratiebeheerder op [!UICONTROL LinkedIn Leren]. De opties Aan de slag, Verbinden en Verbindingen beheren worden weergegeven.
1. Als u de LinkedIn Learning Connector voor het eerst configureert, klikt u op [!UICONTROL Verbinden].

   <!--Configure the Exavault FTP account before you configure this connector.

   ![](assets/configure.jpg)
   *Configure connection*-->

1. Geef op de verbindingspagina een naam op voor uw connector. Voer de appsleutel en de geheime sleutel voor uw verbinding in.

   >[!NOTE]
   >
   >De ondernemingsbeheerder kan via de LinkedIn-leerbeheerportal een nieuwe applicatie genereren om de Appkey en de Geheime sleutel op te halen.

1. Klik op **[!UICONTROL Opslaan]**.

   De configuratie wordt opgeslagen en de LinkedIn Learning-verbinding voor uw account wordt toegevoegd. U kunt nu op Verbindingen ]**beheren klikken**[!UICONTROL  op de startpagina en uw configuratie op elk gewenst moment bewerken.

1. Als u al een verbinding tot stand hebt gebracht, klikt u op **[!UICONTROL Verbindingen]** beheren om al uw verbindingen weer te geven.

   >[!NOTE]
   >
   >De migratiefunctie moet zijn ingeschakeld voor uw account voordat u deze connector kunt configureren.

1. Klik op de verbinding die u wilt bewerken.
1. Klik op Configureren in het linkerdeelvenster. Voer een van de volgende handelingen uit:

   * Bekijk of bewerk de details van uw account en het synchronisatieschema vanuit dit venster. Schakel het **[!UICONTROL selectievakje Verbinding]** inschakelen in als u deze account wilt inschakelen.
   * Klik op **[!UICONTROL Bewerken]** en bewerk uw referenties. Klik op Herstellen om uw updates voor dit veld ongedaan te maken.
   * Klik op **[!UICONTROL Schedule]** inschakelen om uw synchronisatie te plannen. U kunt de starttijd en -datum invoeren en vervolgens de frequentie van uw synchronisatieplanning in dagen invoeren. Bijvoorbeeld, om de drie dagen synchroniseren.

   Klik op **[!UICONTROL Opslaan]** om uw wijzigingen op te slaan.

1. Klik in het linkerdeelvenster op **[!UICONTROL Uitvoeren]** op aanvraag. Met deze optie kunt u gebruikersfeeds en andere relevante gegevens vanuit LinkedIn importeren. Voer de begindatum in voor de uitvoering op aanvraag en klik op Uitvoeren om de synchronisatie uit te voeren. Alle gegevens vanaf de startdatum tot heden worden geïmporteerd.

   * U kunt klikken op **[!UICONTROL Toegang tot]** Learning Manager uitschakelen tijdens uitvoering, waarbij de toepassing een uitvaltijd heeft tijdens de synchronisatie.
   * Als u tijdens het uitvoeren klikt op **[!UICONTROL Toegang tot]** Learning Manager inschakelen, is er geen onderbreking in de service tijdens het synchroniseren.

   ![](assets/ondemandexecution.jpg)

   *Op aanvraag uitvoeren van rapport*

1. U kunt ook op elk moment op Uitvoeringsstatus in het linkerdeelvenster klikken om het overzicht van alle runs voor deze connector in chronologische volgorde te bekijken. U kunt de startdatum en duur van de synchronisatie, het type synchronisatie (of het al dan niet gaat om synchronisatie op verzoek) en de status van de synchronisatie (of de synchronisatie wordt uitgevoerd of is voltooid) bekijken.

   ![](assets/executionstatus.jpg)

   *Uitvoeringsstatus van rapport*

   >[!NOTE]
   >
   >Wanneer u een verbinding wist en opnieuw aanmaakt, worden de vorige runs voor de connector weergegeven. U kunt alle runs bekijken voordat u de verbinding wist.

   U kunt alleen de laatste synchronisatie opnieuw uitvoeren.

### LinkedIn Learning-content filteren {#filter-linkedin}

Er zijn filters in LinkedIn-connectoren om inhoud te scheiden op basis van LinkedIn Learning-bibliotheken. Daarnaast kunt u ook inhoud filteren op basis van taal en bibliotheek en alleen de cursussen in de gewenste talen importeren. Wanneer de inhoud is geïmporteerd, wordt deze op basis van de importconfiguratie gescheiden in meerdere catalogi.

Dit zijn de filters:

**Gebruik van filtertraining:** filtert een subgroep van cursussen uit LinkedIn naar Learning Manager.

* **Op basis van taal**

![](assets/filter-language.png)

*Filteren op taal*

* **Op basis van bibliotheek van LinkedIn Learning**

![](assets/filter-catalog.png)

*Filteren op catalogus*

**Trainingen importeren naar**

![](assets/iport-training.png)
*Training importeren in catalogi*

**Importtags**

Er is een type tag, **aangepaste tag**, die u kunt gebruiken om aangepaste tags toe te voegen aan uw LinkedIn Learning-cursussen. U kunt zoveel tags toevoegen als u wilt, van elkaar gescheiden door komma&#39;s.

![](assets/add-custom-tags.png)

*Aangepaste tags toevoegen*

De inhoud wordt pas opgeslagen na de migratie. De inhoud wordt in respectieve catalogi opgeslagen.

## Power BI-connector {#powerbiconnector}

>[!NOTE]
>
>Learning Manager ondersteunt alleen integratie met commerciële licenties van Microsoft Power BI. Het integreert niet met Microsoft Power BI in Government Cloud.

U kunt integratie met deze connector gebruiken om te profiteren van uw bestaande Power BI-accounts om leergegevens van Learning Manager in Power BI te analyseren en visualiseren. Tijdens de configuratie kan de integratiebeheerder zijn Power BI-werkruimte zo instellen dat deze stapsgewijs wordt gevuld met twee live-datasets - studenttranscript en rapporten over gebruikersvaardigheden. U kunt vervolgens alle functies en mogelijkheden van Power BI gebruiken om aangepaste dashboards te ontwikkelen, implementeren en distribueren naar wens van de organisatie.

### De connector configureren {#configuringtheconnector}

Als u de connector wilt configureren, gaat u naar de **[!UICONTROL pagina Connectors]** , houdt u de muisaanwijzer boven de **[!UICONTROL Power BI-tegel]** en klikt u op **[!UICONTROL Verbinden]**. De Power BI-pagina wordt geopend. Verstrek de client-ID en het clientgeheim van de app, de naam van de tenant en de werkruimte-ID (optioneel) om een verbinding tot stand te brengen. Volg deze stappen om deze gegevens te verkrijgen.

![](assets/power-bi-configurepage.png)

*De Power BI-connector configureren*

1. Launch <https://app.powerbi.com/embedsetup>.
1. Klik op **[!UICONTROL Insluiten voor uw organisatie]** en meld u aan bij uw Microsoft-account.
1. Voer de naam van de app in.
1. Selecteer in het gedeelte App-type de optie Webtoepassing aan de serverzijde.
1. Selecteer in de **[!UICONTROL sectie URL]** omleiden de optie **Een aangepaste URL** gebruiken (kies deze url als u de URL van de doeltoepassing weet). Voer de volgende URL in:

   `https://learningmanager.adobe.com/ctr/app/azure/_callback` (werk het domein bij op basis van de omgeving)

1. Voer in het veld Start-URL de volgende URL in: `https://learningmanager.adobe.com/`
1. Selecteer in het gedeelte met machtigingen de optie **Alle gegevensset** lezen en **Alle gegevensset** lezen en schrijven.

   De tenant verkrijgen: neem contact op met uw Power BI-beheerder om de naam van de tenant op te geven.

   Werkplek-ID verkrijgen: een werkplek maken is alleen mogelijk voor Power BI Pro-gebruikers. U kunt een werkplek maken in Power BI en de ID uit de URL halen.

1. Klik op **[!UICONTROL De app]** Registreren en de Client-id en Het Clientgeheim opslaan.

>[!NOTE]
>
>Als u de verbinding opnieuw wilt autoriseren, moet u een andere Power App maken en de omleidings-URL met een nieuwe naam opgeven.

U kunt Studenttranscripten, Gebruikersvaardigheden en xAPI-activiteitsrapport op dezelfde manier exporteren. Kies in het linkerpaneel voor Studenttranscripten/Gebruikersvaardigheden. De pagina Exporteren wordt geopend.

Schakel het selectievakje **[!UICONTROL Gebruikersvaardigheid/Studenttranscript-export inschakelen in via deze verbinding]** in. Wijzigingen opslaan.

**Export configureren**: als u de extractie van het rapport wilt plannen. Schakel het **[!UICONTROL selectievakje Schema]** inschakelen in en geef de begindatum en -tijd op. U kunt ook aangeven met welke intervallen u het rapport wilt laten genereren en verzenden.

![](assets/power-bi-configureuserskillpage.png)

*Exporteren configureren om het rapport te plannen*

**Exporteren op aanvraag:** u kunt de begindatum opgeven en het rapport exporteren met behulp van de optie. Het rapport wordt geëxtraheerd vanaf de ingevoerde datum tot heden.

![](assets/power-bi-userskillondemandpage.png)

*Exporteren op aanvraag*

De geëxporteerde gegevens kunnen worden bekeken door u aan te melden bij uw Power BI-account. De geëxporteerde gegevens staan vermeld onder de optie gegevenssets.

### xAPI Activiteitsrapporten exporteren in Learning Manager {#exportxapiactivityreportsincaptivateprime}

Klik op de pagina met Mogelijkheden van PowerBI-xAPI op **[!UICONTROL XAPI-activiteitenrapport]** exporteren.

![](assets/powerbi-dashboard.png)
*PowerBI - XAPI-activiteitsrapport exporteren*

Selecteer **Configuratie** in het linkerdeelvenster en volg de onderstaande stappen:

* Vul het JSON-padveld in dat met de kolomnaam en het tekenreekstype overeenkomt.
* Klik op **[!UICONTROL Toevoegen]** om meer JSON-paden toe te voegen.
* U kunt de invoer in de JSON-padvelden bewerken door op **[!UICONTROL Bewerken]** te klikken.
* Klik op **[!UICONTROL Opslaan]** om uw wijzigingen op te slaan.

**Planning configureren**

Klik in het linkerdeelvenster op **[!UICONTROL Planning configureren]** en doe het volgende:

* Klik op Exporteren van xAPI-statements via deze verbinding inschakelen.
* Selecteer het selectievakje **[!UICONTROL Planning inschakelen]** en geef de begindatum en -tijd op. U kunt ook opgeven om de hoeveel dagen de export moet worden herhaald en verzonden.
* Klik op de knop **[!UICONTROL Opslaan]** om de instellingen van de geconfigureerde planning op te slaan.

![](assets/configure-schedule.png)
*Configuratieschema voor xAPI-export*

**Op verzoek**

Klik in het linkerdeelvenster op **[!UICONTROL Op verzoek]** en geef de begindatum op de pagina xAPi-statements exporteren-Op verzoek.

![](assets/on-demand-2.png)
*xAPI-export op aanvraag*

Alle geëxporteerde gegevens gaan naar een dataset die door Adobe in uw Power BI-account wordt gemaakt.

xAPI-export naar Power BI mislukt als enkele van de xAPI-statements in LRS geen JSON-pad hebben dat voor export is geconfigureerd. Voor de xAPI-statements waar het JSON-pad niet beschikbaar is, moet de constante waarde N/A worden toegevoegd en weergegeven in Power BI.

**Uitvoeringsstatus**

Selecteer **Uitvoeringsstatus** om een overzicht van alle taken in chronologische volgorde weer te geven. Het waarschuwingsteken geeft aan wat er tijdens de run fout is gegaan. U kunt foutrapporten downloaden als **CSV-bestand** door op de koppeling foutrapport te klikken.

![](assets/execution-status.png)
*Uitvoeringsstatus van xAPI-export*

### Gecombineerde rapporten {#unified-reports}

Learning Manager biedt een manier om exportbestanden te maken met een combinatie van rapporten zoals Gebruikersgegevens, Transcript, Gamification, Feedbackrapporten en meer, als één gegevensset naar Power BI.

Hierdoor kunnen Power BI-gebruikers de gegevens uit meerdere rapporten samenvoegen om veel krachtige analyses en visualisaties in Power BI te presenteren.

![](assets/unified-power-bireports.png)
*Uniforme Power BI-rapporten*

**Export op verzoek**

Geef de begin- en einddatum op en exporteer het rapport met behulp van de optie. Het rapport wordt voor het opgegeven datumbereik geëxtraheerd.

![](assets/on-demand-export.png)
*Op aanvraag exporteren*

**Geplande export**

Als u de extractie van het rapport wilt plannen. Selecteer het selectievakje **Planning inschakelen** en geef de begindatum en -tijd op. U kunt ook aangeven met welke intervallen u het rapport wilt laten genereren en verzenden.

![](assets/configure-schedule.png)
*Schema configureren*

U kunt trainingsrapporten ook exporteren naar Power BI.

Trainingsrapporten kunnen worden geëxporteerd naar Power BI als onderdeel van de functie Gecombineerde rapporten.

Het trainingsrapport heeft twee extra velden:

* Het aantal gebruikers dat feedback over een cursus heeft gedeeld
* Gemiddelde waardering met sterren voor een cursus

### Filterstatus van studenttranscripten {#lt-status}

In het gedeelte Gecombineerde rapporten van een Power BI-connectie is er een optie om studenttranscripten te exporteren op basis van de status van de leerobjecten.

* **Alles selecteren:** exporteer alle bestanden of activiteiten op moduleniveau in het opgegeven datumbereik.
* **Voltooid:** exporteer alle bestanden die voltooid zijn in het datumbereik.
* **In uitvoering:** exporteer alle records met de status In uitvoering.
* **Niet gestart:** sluit de records uit die zijn ingeschreven voor het opgegeven datumbereik, maar die niet zijn gestart bij het genereren van het rapport.

* **Niet ingeschreven:** voeg alle bestanden bij die niet zijn ingeschreven in het datumbereik.

![](assets/lt-filters.png)
*Filterstatus van leertranscripties*

U kunt de gewenste lijst exporteren en Power BI gebruiken om het rapport later te analyseren.

### Power BI-sjablonen downloaden {#template}

Learning Manager biedt ook kant-en-klare Power BI-sjablonen. Deze sjablonen bieden accountbeheerders van Adobe Learning Manager betere analysemogelijkheden.

Met deze beschikbare sjablonen kunt u eenvoudig de sjablonen downloaden, relevante rapporten exporteren en plotrapporten.

![](assets/download-power-bi-template.png)
*Power BI-sjablonen downloaden*

Zo kunnen gebruikers deze sjablonen downloaden en gebruiken in Power BI-toepassingen en deze verder aanpassen, zodat uw rapporten een interessant verhaal vertellen.

[**De sjablonen downloaden**](https://documentcloud.adobe.com/link/track?uri=urn:aaid:scds:US:842bb6a2-cd7d-4c3d-b968-da38bc1cc18a)

<!--<table> 
 <tbody>
  <tr> 
   <td><img src="assets/download.png"></td> 
   <td><p> </p> <p><a disablelinktracking="false" href="https://documentcloud.adobe.com/link/track?uri=urn:aaid:scds:US:842bb6a2-cd7d-4c3d-b968-da38bc1cc18a"><strong><em>Download the templates</em></strong></a></p></td> 
  </tr> 
 </tbody>
</table>-->

U kunt de sjablonen ook handmatig downloaden via de bovenstaande link. Gebruik de sjablonen en pas uw rapporten aan de hand daarvan aan.

### Trainingsrapport exporteren

De trainingsrapporten kunnen worden geëxporteerd naar Power BI als onderdeel van de functie Gecombineerde rapporten.

Het trainingsrapport heeft deze extra velden:

* Het aantal gebruikers dat feedback over een cursus heeft gedeeld
* Gemiddelde waardering met sterren voor een cursus

![](assets/export-training-report.png)
*Trainingsrapport exporteren*

### Wijzigingen met betrekking tot leerpad

#### Beheer: transcripties en eenduidige rapporten leren

**Bestaande verbindingen**

Als de optie Leerpad is uitgeschakeld in het beheerdersaccount, worden er geen rijen en kolommen in de rapporten toegevoegd.

Als de optie Leerpad is ingeschakeld in het beheerdersaccount, bevat het rapport het kolomtype Leerpad (hoger niveau) voor alle studenten die zijn ingeschreven voor een leerpad.

**Nieuwe verbindingen**

Als de optie Leerpad is uitgeschakeld in het beheerdersaccount, bestaat het trainingsrapport uit de volgende kolommen:

* Ingesloten pad: geeft de naam van het leerprogramma weer.
* Ingesloten pad-ID: geeft de ID&#39;s voor het leerprogramma weer.
* Ingesloten cursus-ID: geeft de ID&#39;s van de cursussen in een leerpad weer.

Bovendien bevat het rapport het kolomtype Leerpad (hoger niveau) voor alle studenten die in een leerpad zijn ingeschreven.

In de kolom Type wordt de naam leerprogramma gewijzigd naar leerpad. Bestaande verbindingen wijzigen niet. Voor nieuwe verbindingen worden de wijzigingen na 30 dagen doorgevoerd.

#### Trainingsrapport: verenigd rapport

**Bestaande verbindingen**

Als de optie Leerpad is uitgeschakeld in het beheerdersaccount, worden er geen rijen en kolommen in de rapporten toegevoegd.

Als de optie Leerpad is ingeschakeld in het beheerdersaccount, bevat het rapport de kolom &#39;Type&#39;. De kolom bevat de nieuwe waarde &#39;Leerpad (hoger niveau), indien van toepassing&#39;.

**Nieuwe verbindingen**

Als de optie Leerpad is uitgeschakeld in het beheerdersaccount, bestaat het trainingsrapport uit de volgende kolommen:

* **Ingesloten pad:** geeft de naam van het leerprogramma weer.
* **Ingesloten pad-ID:** geeft de ID&#39;s voor het leerprogramma weer.
* **Ingesloten cursus-id:** hier worden de id&#39;s weergegeven van cursussen die zich binnen een leerpad bevinden.

Bovendien bevat het rapport het kolomtype Leerpad (hoger niveau) voor alle studenten die in een leerpad zijn ingeschreven.

In de kolom Type wordt de naam leerprogramma gewijzigd naar leerpad. Bestaande verbindingen wijzigen niet. Voor nieuwe verbindingen worden de wijzigingen na 30 dagen doorgevoerd.

## Aangepaste FTP {#custom-ftp}

**Vereiste**

>[!NOTE]
>
>Als u uw aangepaste FTP wilt installeren, neemt u contact op met uw CSM. De CSM zal de vereiste details van het opzetten van de FTP verstrekken.
>
>Voor het instellen van de FTP is een tijd nodig en it-ondersteuning vereist om de lijst met IP&#39;s en poorten toe te staan en om bepaalde mappen met specifieke machtigingen op uw FTP-server te maken.

Learning Manager biedt de mogelijkheid om verbinding te maken met uw aangepaste FTP-locatie.

Uw FTP zal deze ondersteunen:

### Gegevensimport

Met het gebruikersimportproces kan de Learning Manager Administrator werknemersgegevens ophalen van de FTP-service van Learning Manager en ze automatisch in Learning Manager importeren. Met behulp van deze functie kunt u meerdere systemen integreren door de door deze systemen gegenereerde CSV in de juiste mappen van de FTP-accounts te plaatsen. Learning Manager haalt de CSV-bestanden op, voegt ze samen en importeert de gegevens volgens de planning. Raadpleeg de planningsfunctie voor meer informatie.

**Kenmerken toewijzen**

Kenmerken toewijzen Deze toewijzing is een eenmalige inspanning. Zodra de toewijzing is voltooid, wordt dezelfde toewijzing gebruikt voor de daaropvolgende gebruikersimporten. De toewijzing kan opnieuw worden geconfigureerd als de beheerder een andere toewijzing voor het importeren van gebruikers wil hebben.

### Gegevensexport

Met de gegevensexport kunnen gebruikers gebruikersvaardigheden en studenttranscripten exporteren naar de FTP-locatie om deze te integreren met elk systeem van een derde partij.

### Rapporten plannen

De beheerder kan planningstaken volgens de vereisten van de organisatie instellen en gebruikers in de Learning Manager-toepassing zijn up-to-date volgens de planning. Op dezelfde manier kan de integratiebeheerder de export van vaardigheden op een tijdige basis plannen om deze te integreren met een extern systeem. De synchronisatie kan dagelijks worden uitgevoerd in de Learning Manager-toepassing.

Als u uw eigen FTP wilt configureren, meldt u zich aan als integratiebeheerder en klikt u op **[!UICONTROL Aangepaste FTP]** -> **[!UICONTROL Verbinden]**.

Er zijn twee soorten verificaties:

![](assets/custom-ftp-authenticationoptions.png)
*Aangepaste OPTIES voor FTP-verificatie*

* **Standaard:** in basisverificatie hoeft u alleen de FTP-domein-URL, gebruikersnaam en wachtwoord op te geven. Klik na het verstrekken van de gegevens op Verbinden.
* **Certificering:** als FTP-ondersteuning biedt voor certificaatverificatie van klanten, kunnen ze deze optie kiezen. Nadat u op SSH-sleutel genereren hebt geklikt, wordt de SSH-sleutel gedownload naar uw lokale computer. Wanneer u het bestand opent, ziet de toets eruit als volgt:

![](assets/ssh-public-key.png)
*Openbare SSH-sleutel*

U moet deze openbare sleutel op uw FTP-server plaatsen voordat u de onderstaande gegevens toevoegt. Zodra u de opgegeven sleutel als openbare sleutel van uw FTP hebt ingesteld, geeft u de FTP-domein-URL en de gebruikersnaam op en klikt u op **de knop Verbinden** om de verbinding tot stand te brengen.

Zodra de verbinding is ingesteld, worden er automatisch mappen voor importeren en exporteren gemaakt in de FTP-locatie. Daarna wordt de functie voor importeren/exporteren verschaft door aangepaste FTP.

>[!NOTE]
>
>Een aangepaste FTP-connector kan alleen met SFTP-servers worden geconfigureerd.

## ADFS-aansluiting {#adfsconnector}

Voorwaarden om een ADFS-verbinding tot stand te brengen:

* Meld u aan bij uw Azure Portal met de volgende URL:  [https://portal.azure.com/](https://portal.azure.com/) voordat u uw app registreert.
* Open Azure Active Directory.

## Stappen om uw toepassing te registreren {#stepstoregisteryourapplication}

* Klik op Azure Active Directory. Klik op **[!UICONTROL App-registratie]** toevoegen ]**>**[!UICONTROL .

  <!--![](assets/add-app-registration.png)-->
  <!-- *Add app registration*-->

* Voer de naam in van de toepassing.

  <!--![](assets/register-app.png)-->
  <!--*Enter the name of the application*-->

  Klik op **[!UICONTROL Registreren]**.

* Selecteer in het rechterdeelvenster **[!UICONTROL Certificaten en geheimen]**.

  <!--![](assets/add-client-secret.png)-->

  <!--*Select Certificates and Secrets*-->

* Voeg een client-geheim toe.

  <!--![](assets/add-description.png)-->

  <!--*Add a client secret*-->

* Voeg een beschrijving toe aan het geheim en stel de vervaldatum in op 24 maanden.

  <!-- ![](assets/copy-values.png)-->

  <!--*Add description*-->

* Kopieer de waarde en het geheim naar bijvoorbeeld het kladblok.

  <!-- ![](assets/copy-secret.png)-->

  <!--*Copy value and secret key*-->

* Klik op **API-machtigingen**.

  <!--![](assets/click-api-permission.png)-->

  <!-- *Left pane containing API Permissions*-->

* Selecteer **Machtigingen toevoegen**. Schakel ook de optie **Admin toestemming verlenen** in.

  ![](assets/add-permission.png)

  *Machtigingen toevoegen*

* Selecteer **Microsoft Graph**.

  <!--![](assets/ms-graph.png)-->

  <!--*Select Microsoft Graph*-->

* Selecteer **Toepassingstoestemmingen**.

  ![](assets/request-api-permission.png)

  *Toepassingsmachtigingen selecteren*

* Zoek naar de *directory* en selecteer **Directorygegevens lezen**.

  ![](assets/read-directory-data.png)

  *Selecteer Directorygegevens lezen*

* Voer *gebruiker* in als de zoekterm.

  ![](assets/search-user.png)

  *Voer de zoekterm in*

* Selecteer **De volledige profielen van alle gebruikers lezen**.

  ![](assets/select-read-all.png)

  *Alle profielen van gebruikers lezen selecteren*

* Selecteer **Machtigingen toevoegen**.

  <!--![](assets/select-add-permission.png)-->

  <!-- *Select Add Permissions*-->

### ADFS-configuratiepagina

1. Voer op de ADFS-configuratiepagina in Adobe Learning Manager de client-id en het eerder verkregen client-geheim in.

   Klik op **[!UICONTROL Verbinden]**.

1. Meld u aan **bij portal.azure.com**. De waarden worden ingevuld in de velden Tenant-id en Primair domein.

### Importeren

#### Kenmerken toewijzen

De integratiebeheerder kan ADFS-kenmerken kiezen en deze toewijzen aan overeenkomstige groepskenmerken van Learning Manager. Wanneer de toewijzing is voltooid, wordt dezelfde toewijzing voor verdere gebruikersimporten gebruikt. De configuratie kan opnieuw worden geconfigureerd als de beheerder een andere toewijzing wil hebben voor het importeren van gebruikers.

#### Geautomatiseerde gebruikersimport

Bij het importeren van gebruikers kan Learning Manager-beheerder gegevens van werknemers ophalen uit ADFS en deze automatisch importeren in Learning Manager.

#### Gebruikers filteren

Leerbeheerbeheerder kan filters toepassen op gebruikers voordat ze worden geïmporteerd. Zo kan de Learning Manager-beheerder er bijvoorbeeld voor kiezen om alle gebruikers in de hiërarchie onder één of meer specifieke managers te importeren.

Neem contact op met het Learning Manager CSM-team om de ADFS-connector in te stellen.

## De ADFS-connector configureren {#configureadfsconnector}

1. Op de startpagina van Learning Manager houdt u de muis boven de ADFS-kaart/miniatuur. Er verschijnt een menu. Klik op de optie Verbinden in het menu.

   ![](assets/adfs1.jpg)

   *ADFS-miniatuur*

1. Klik op Verbinden om een nieuwe verbinding tot stand te brengen. De pagina ADFS-connector wordt weergegeven. Vul de gegevens in van het account dat u wenst toe te wijzen.

   ![](assets/adfs2.jpg)

   *Verbinding tot stand brengen*

1. Als u ADFS-gebruiker rechtstreeks wilt importeren als een interne gebruiker van Learning Manager, gebruikt u de optie Interne gebruikers importeren.

   ![](assets/adfs3.jpg)

   *Gebruikers importeren in Learning Manager*

1. Op de toewijzingspagina zie je links de kolommen van Learning Manager en aan de rechterkant de ADFS-kolommen. Selecteer de juiste kolomnaam die wordt toegewezen aan de kolomnaam van de leermanager.

   ![](assets/adfs4.jpg)

   *Kenmerken toewijzen*

1. Als u de gegevensbron wilt weergeven en bewerken, klikt u als beheerder op **[!UICONTROL Instellingen]** > **[!UICONTROL Gegevensbron]**.

   De gevestigde ADFS-bron wordt vermeld. Als u het filter wilt bewerken, klikt u op **[!UICONTROL Bewerken]**.

   ![](assets/datasource.jpg)
   *Gegevensbroninstelling*

1. U ontvangt een melding na voltooiing van de import. Klik op **[!UICONTROL Gebruikers]** > **[!UICONTROL logboek importeren om het importlogbestand]** weer te geven of te bewerken.

### Een verbinding verwijderen {#Deleteaconnection-1}

Ga als volgt te werk om een tot stand gebrachte miniOrange-verbinding te verwijderen.

## Adobe Connect {#connect}

1. Klik in Adobe Connect op de drie puntjes op de kaart en kies **Verbinden**.
1. Klik op de **koppeling Nu** configureren in de sectie Adobe Connect-configuratie.
1. Geef de Adobe Connect-domeinnaam van uw bedrijf en meld u aan met uw bedrijfsgegevens.

   Een voorbeeld van een Adobe Connect-URL: ***mycompany.adobeconnect.com***

   U moet de e-mail-ID van de Adobe Connect-accountbeheerder opgeven.

   >[!NOTE]
   >
   >Alleen door Adobe gehoste accounts worden ondersteund in Learning Manager. Voorbeeld; &#39;.adobeconnect.com&#39;.

1. Klik op **[!UICONTROL Integreren]**.

   Nadat de e-mail is geverifieerd, geeft Learning Manager het bericht weer omdat Connect is geïntegreerd. U kunt uw virtuele klassikale cursussen automatisch bekijken met behulp van Adobe Connect.

   **Nadat het Connect-accountbeheer zijn/haar email-ID heeft geverifieerd, wordt het verzoek ter goedkeuring voorgelegd aan het Adobe Connect back-end team. Het duurt doorgaans een dag of twee voordat de integratie is goedgekeurd en ingesteld.**

   >[!NOTE]
   >
   >De Adobe Connect-accountbeheerder moet de algemene gebruiksvoorwaarden van Adobe Connect accepteren. Als deze niet worden geaccepteerd, mislukt uw aanmeldpoging mogelijk. Meld u na het aanmaken van het Adobe Connect-account eenmaal aan op het account. Bij de eerste aanmeldpoging verschijnt er een pagina met de Algemene voorwaarden.

### Sessie-informatie voor virtueel klaslokaal toevoegen {#addvirtualclassroomsessioninformation}

Als de auteur van een virtuele klassikale cursus de sessie-informatie niet heeft verstrekt, dan kan de beheerder de sessiedetails opnemen.

Klik op de naam van de VC-cursus in Beheerdersaanmelding. Klik op Instanties in het linkerdeelvenster en Sessiedetails.  Klik op het pictogram Bewerken in de rechterhoek van de pagina Sessiedetails om sessiegegevens toe te voegen.

Met de integratie van Adobe Learning Maanger en Adobe Connect voor het maken van virtuele klassikale modules of sessies, moet uw Connect-account ondersteuning bieden voor vergaderzalen met een voldoende aantal ruimten en gelijktijdige gebruikers voor uw use case. Deze vergaderzalen worden gebruikt om virtuele klassikale modules van Learning Manager te hosten. Er wordt door Learning Manager dynamisch een nieuwe Connect vergaderzaal aangemaakt voor elke virtuele klasmodule of sessie binnen Learning Manager.

>[!NOTE]
>
>U moet Adobe Connect apart aanschaffen, los van Adobe Learning Manager.

### Permanente vergaderruimte van Adobe Connect {#persistent}

In Adobe Connect gebruiken klanten bestaande vergaderruimtes die ze al hebben gemaakt in Connect. Alle vergaderruimtes in Connect zijn permanent en de sjablonen voor de vergaderruimtes zijn zorgvuldig ingesteld om een uniforme ervaring voor elke permanente ruimte te bieden.

U kunt een virtueel klaslokaal maken met behulp van een ruimte die al in Adobe Connect is gemaakt.

In Learning Manager kunnen studenten de verbonden ruimte voor hun virtuele sessie ook betreden met behulp van een verificatiemethode.

![](assets/adobe-connect-authentication.png)
*Adobe Connect-verificatie*

Wanneer u met behulp van Adobe Connect een VC-module maakt, kunt u een permanente ruimte selecteren. Als u **Nee** selecteert, wordt zoals voorheen een dynamische vergaderruimte gemaakt.

![](assets/persistent-room-selection.png)
*Permanente ruimteselectie*

Als een student via Adobe Connect een cursus heeft gevolgd en afgerond, wordt na enige tijd een opname van de sessie en een wachtwoord weergegeven in de Learner-app.

![](assets/connect-recording.png)
*Verbinding maken met opnemen*

### Quizscores importeren uit Adobe Connect {#quiz-adobe-connect}

Importeer de Connect-quizgegevens in Learning Manager en integreer deze gegevens met de bestaande rapportageworkflow, zodat Learning Manager-gebruikers quizgegevens, gebruikersreacties en scores van Adobe Connect-sessies in rapporten kunnen ontvangen, bijvoorbeeld voor zelfstudiemodules met quizzen.

Als een student een quizcursus volgt of interacties heeft in het Connect-gedeelte die quizrapportages ondersteunen, worden alle interacties van studenten gevolgd totdat ze zijn voltooid. De cursus moet een Connect VC-cursus zijn.

Hieronder volgt een korte workflow van het proces.

**Adobe Connect - Host**

* De host in Connect maakt een cursus en uploadt interactieve inhoud met een quiz.
* De host maakt een training in een **virtuele lesruimte** en slaat de VC-training op. De host heeft de optie om de hierboven gemaakte cursus te koppelen aan de VC of kan tijdens de sessie de optie **Cursus delen** in de Connect-app gebruiken om de cursus te delen.

**Learning Manager - Auteur**

* De auteur maakt een cursus in Learning Manager met het moduletype **Virtual Classroom.**
* Kies uit de **Conferentiesysteem**-vervolgkeuzelijst de optie Koppelen als de VC-provider.
* Kies de Persistent Meeting-cursus en selecteer het VC-klaslokaal dat door de host in Connect is gemaakt. Kies de docent. Sla de cursus op en publiceer deze.

**Learning Manager - Lerende**

* Nadat de cursus is gepubliceerd, schrijft de student zich in voor de cursus.
* De student wordt naar de Connect VC-sessie geleid waar de Connect-host hem/haar toegang toe geeft.

**Adobe Connect - Host**

* Binnen de VC-sessie deelt de Connect-host de quiz die eerder werd gedeeld.

**Adobe Connect - Student**

* De student neemt deel aan de quiz en sluit de sessie wanneer de quiz is voltooid.

**Learning Manager - Lerende**

* De student sluit de sessie en de sessie wordt automatisch gesynchroniseerd.

**Learning Manager - Beheer**

* Wanneer de sessie is verlopen, wordt de importworkflow van de quiz na de geplande duur geactiveerd.
* Wacht totdat de planning is geactiveerd en de verwerking is voltooid. U kunt de verwerkingsstatus controleren aan de kant van de integratiebeheerder door de **Uitvoeringsstatus** te bekijken binnen de Adobe Connect-connector om de voortgang te zien. Als de uitvoering is gelukt, verandert de status in **Voltooid**.

* De beheerder kiest vervolgens de eerder gemaakte cursus Leerbeheer. De beheerder ziet het volgende:

   * **Aanwezigheid en scores** - Toont de uiteindelijke quizscore en de aanwezigheidsstatus.
   * **L2-quizscore**

      * **Op gebruiker** : hiermee wordt de eindquizscore weergegeven als **Punten** en **Percentage**.
      * **Op vraag** - Toont de quizinformatie als een rapportdiagram.

## Marketo Engage-connector {#marketo}

Learning Manager kan worden geïntegreerd met Marketo Engage, een marketingautomatiseringssoftware die helpt bij het uitvoeren van marketingcampagnes.

De Marketo Engage Connector is ontworpen om leads in de Marketo Engage-database toe te voegen (of bij te werken) wanneer er een nieuwe gebruiker aan het Learning Manager-account wordt toegevoegd. Ook worden leergedrag van de gebruiker in Learning Manager (cursusinschrijving, voltooiing van de cursus, vaardigheidstoewijzing en voltooiing van vaardigheden) geassocieerd met de overeenkomstige leads in Marketo Engage. Zo kan een marketeer deze informatie gebruiken om doelgroepen te targeten op basis van hun leergedrag dat is vastgelegd met Learning Manager en functies van Marketo Engage te gebruiken, zoals &#39;Slimme lijsten&#39;.

Als integratiebeheerder kunt u Learning Manager met een Marketo Engage-exemplaar integreren om gegevenssynchronisatie te automatiseren. U kunt interne gebruikers en trainingsinschrijvingen exporteren, evenals voltooiingen van vaardigheden. De handelingen kunnen gepland worden uitgevoerd en op verzoek worden geconfigureerd.

Learning Manager kan alleen integreren met uw Marketo-account als uw Marketo-account de mogelijkheid moet hebben om schema&#39;s te maken via API&#39;s.

U kunt de volgende drie rapporten van de Marketo-app downloaden:

* Gebruikersrapport
* Leertranscript
* Gebruikersvaardigheidsrapport

Wanneer u een Marketo Engage-verbinding maakt, moet u de volgende gegevens opgeven:

* Verbindingsnaam
* Client-id
* Client-geheim
* Marketo Engage Domain

![](assets/marketo-creds.png)

*Referenties voor Marketo invoeren*

>[!NOTE]
>
>U kunt de client-id en het client-geheim uit de Marketo Engage-app halen. In de Marketo-app kunt u de Client-id en het geheim ophalen uit de **sectie LaunchPoint** en het Marketo-domein uit de **sectie WebServices** .

In de **sectie Uniforme rapporten** van de verbinding Markeo Engage in de App Learning Manager kunt u campagnes maken op basis van het volgende:

* Er wordt een nieuwe gebruiker toegevoegd aan Learning Manager
* Een nieuwe gebruiker is ingeschreven voor een cursus
* Een nieuwe gebruiker heeft een cursus voltooid
* Een student is ingeschreven voor een vaardigheid
* Een student heeft een vaardigheid gehaald

Net als bij elke andere connector kunt u op verzoek gegevens plannen en exporteren.

### Kolomtoewijzing in Marketo Engage {#columnmappinginmarketoengage}

Er zijn twee typen databases in Marketo:

* Lead-database
* Aangepast object-database

Kolomtoewijzing wordt gebruikt om de lead-database te maken. Leads zijn gebruikers die u hebt geëxporteerd vanuit het gebruikersrapport.

De velden van het gebruikersrapport staan vermeld in de kolom Adobe Learning Manager. De velden in de kolom Marketo bevatten wat Marketo biedt. Met beide kolommen kunt u elk veld in Leerbeheer toewijzen aan het veld uit Marketo. Vanuit een Learning Manager-kolom word je lid van een gerelateerde kolom van Marketo. Na het samenvoegen van de kolommen wordt er een lead-database gemaakt.

U kunt vervolgens alle geëxporteerde gebruikers in Marketo bekijken.

In het gedeelte **Aangepaste objecten van Marketo** in de Marketo-app kunt u zien dat alle drie de rapporten aanwezig zijn: studenttranscript, gebruikersvaardigheid en gebruikersrapport. Voor deze rapporten wordt de tekenreeks **&#39;cp_&#39;** voorafgegaan. Elke nieuwe gebruiker die wordt geëxporteerd naar Marketo wordt als lead beschouwd.

### Gebeurtenissen

Exporteer gegevens vanuit Learning Manager-gebeurtenissen naar een Marketo Engage-instantie. Selecteer de te exporteren gebeurtenissen naar de Marketo Engage-database ofwel op afroep ofwel op schema.

* Nieuwe gebruiker toevoegen
* Gebruikersmetadata updaten
* Gebruikersactiviteit updaten
* Training-inschrijving
* Zelfinschrijving
* Voltooiing markeren

<!--## BlueJeans Events {#bj-events}

BlueJeans Events connector connects Learning Manager and BlueJeans systems to automate data synchronization. Using this connector, you can:

* **Set up virtual sessions using BlueJeans Events:** Configure a new event in BlueJeans and setup a VC session in Learning Manager by selecting the appropriate BlueJeans event. Date and time details are picked automatically from the BlueJeans events.
* **Automated User Completion Syncing:** An Automated user completion syncing process allows the Learning Manager Administrator to fetch completion records for BlueJeans events automatically.

This new connector requires a separate set of credentials to configure the connector. The credentials of the existing BlueJeans Meetings connector will not work for BlueJeans Events connector.

![](assets/bj-event-connector.png) 
*Credentials for BlueJeans Event Connector*

### Workflow {#workflow}

1. The BlueJeans Event moderator creates an event from within BlueJeans.
1. The author creates BlueJeans event course using the BlueJeans event url, which is created in future dates.
1. Since BlueJeans events have a similar title for multiple events, the author must append the event attendee url to the room name, so that he/she can choose the appropriate event.

   The format to enter event url: ***event name--event attendee url***

   For Dynamic rooms, the behavior is similar to that of Adobe Connect.

   ![](assets/bj-eventname.png)
   *BlueJeans Events configuration*

1. Once the author enters the BlueJeans event url, the date and time will be auto populated.
1. Add an instructor to the event. The instructor will now have elevated privileges as a Presenter in a BlueJeans event.

Administrators, managers, and learners can enroll learners to the created course. Upon enrollment, the learner receives an email. The learner can sign in to their Learning Manager account to view the program details and take the course.

When the course is complete, the completion report gets triggered after a scheduled duration. The administrator can see the completion report to check the attendance and score of the learners.

If the BlueJeans Event moderator enables the recording during the session, after session ends, the recording is available in the learner app.

![](assets/bluejeans-event-configure.png)
*BlueJeans Events configuration*

When you enable the check-box **Fetch Events created by the other users**, you can then add the list of BlueJeans event creators in the **Additional Event Creators** field. In the Author app, only events created by these users are searchable via the type-ahead field.

If the **Additional Event Creators** field is left blank, all events created in BlueJeans will be available for searching in the Author App.

The Author, in the Author app, then selects an event from the list of available events. In addition, the Author can add instructors to the event. These instructors in Learning Manager would become the presenters within BlueJeans events.

>[!NOTE]
>
>All users must belong to the same enterprise in BlueJeans Events App.

>[!NOTE]
>
>We've added a caching mechanism that improves the overall user experience. It is applicable when you select additional event creators. In this mode, the events are fetched the first time when an author searches for an event. The cache persists for 30 mins so that authors know how long they must wait to fetch the new events.-->

## Microsoft Teams-connector

Microsoft® Teams® is een permanent op chat gebaseerd samenwerkingsplatform dat het delen van documenten, online vergaderingen en andere functies voor zakelijke communicatie ondersteunt.

Adobe Learning Manager gebruikt een virtual classroom connector die gebruikt kan worden om Microsoft Teams-vergaderingen in Learning Manager te integreren.

De Microsoft Teams-connector verbindt de Learning Manager- en Microsoft Teams-systemen om automatische synchronisatie van gegevens mogelijk te maken. Hier volgt een lijst met de mogelijkheden van de Microsoft Teams-connector:

**Virtuele sessies instellen met Microsoft Teams**

Deze connector helpt uw Adobe Learning Manager-account te integreren met uw Microsoft Teams-account. Na de integratie kan een auteur in Learning Manager met de connector Microsoft Teams gebruiken als technologieserviceprovider voor de virtuele klassikale modules die in Learning Manager zijn gemaakt.

**Toestaan dat Microsoft Teams studenten verifiëren wanneer ze een virtueel klaslokaal binnenkomen**

Een organisator van de vergadering kan de lobby inschakelen om de toegang tot de vergadering te beperken en de andere vergaderopties beheren die door Microsoft Teams worden geboden.

**Automatische synchronisatie van gebruikersvoltooiing gebruiken**

Met het geautomatiseerde synchronisatieproces voor de voltooiing van gebruikers kan een Learning Manager-beheerder automatisch de voltooiingsrecords en de opname-URL voor de Teams-vergadering ophalen.

Zie Microsoft Teams Connector installeren in Adobe Learning Manager **](install-microsoft-teams-connector.md)voor meer informatie[**.

## Ervaring voor niet-aangemeld

Zonder aanmelding kunt u een realtime-ervaring creëren voor niet-aangemelde gebruikers. Een ervaring die niet is aangemeld, dient bijvoorbeeld als openingspagina voor marketingcampagnes om zich te registreren.

De ervaring die niet is aangemeld in Adobe Learning Manager kan worden geconfigureerd met behulp van de **[!UICONTROL connector Training Data Access]** . De connector biedt het volgende aanbod:

* Standaardaanbod
* Premiumaanbod

**Standaardaanbod**

De standaardversie is om de systeemeigen versie van Adobe Learning Manager te maken. Gebruikers kunnen een headless-ervaring maken zonder demonstratie en niet zijn aangemeld. De headless-ervaring van de demonstratie kan niet worden schalen en dient niet in een productieomgeving te worden gebruikt.

**Premiumaanbod**

Het premiumaanbod helpt gebruikers een headless interface te ontwikkelen, die wordt geconfigureerd door de **[!UICONTROL Training Data Access-connector]** . Dit stelt gebruikers in staat om real-time gegevens over de cursus en het leerpad te krijgen zoals naam, beschrijving, auteur, vaardigheden, duur, enz. Voor scenario&#39;s voor blended leren krijg je ook realtime limieten voor licenties, bezet stoelen, limieten voor wachtlijsten en aantal wachtlijsten. Klanten kunnen deze API&#39;s gebruiken om zoek- en filterfuncties en een volledig cursusoverzicht te maken voor studenten die niet zijn aangemeld.

Klanten kunnen een premiumlidmaatschap aanschaffen om deze zeer schaalbare, niet-aangemelde ervaring te ontwikkelen.

>[!NOTE]
>
>Neem contact op met het ondersteuningsteam of CSM om het premiumlidmaatschap aan te schaffen.

Nadat een gebruiker een lidmaatschap heeft gekocht, activeert het CSM-team het premiumlidmaatschap voor hem of haar. Met behulp van de Connector voor Training Data Access kunnen gebruikers een ervaring instellen die niet is aangemeld met de eerder vermelde functies.

### Connector voor trainingstoegang tot gegevens

>[!IMPORTANT]
>
>Deze specifieke functionaliteit is alleen beschikbaar als Adobe Learning Manager wordt verkocht als add-on voor Adobe Experience Manager. De cursusgegevens zouden over 24 uur verouderd zijn.

>[!NOTE]
>
>Het gedeelte belicht hoe de infrastructuur werkt, maar neem contact met ons op voor het bouwen van een headless of AEM-gebaseerde ervaring zonder aanmelding. We zullen de juiste aanpak voorstellen op basis van uw situatie. Deze functie is momenteel niet beschikbaar als zelfbedieningsfunctie.

Met de **[!UICONTROL connector toegang tot]** trainingsgegevens biedt u een headless-ervaring. Deze ervaring kan zelfstandig zijn of een aangepaste gebruikersinterface die is gebaseerd op AEM-sites. Met deze functie kunt u trainingsinformatie ophalen en weergeven, en kunt u zoeken en filteren. Zodra de gegevensconnector is ingeschakeld, is een set openbare API&#39;s beschikbaar om de interface te maken, waar cursus-/leerpadinformatie wordt weergegeven aan studenten.

#### De connector configureren

Gebruik de **[!UICONTROL connector voor Training Data Access]** om uw Adobe Learning Manager-account te integreren met systemen voor gegevensopslag en zoekfunctie. Zo krijgt de interface die is gebaseerd op AEM Sites, trainingsgegevens, webpagina&#39;s en betere zoekopties voor studenten.

U kunt trainingsmetagegevens van Adobe Learning Manager exporteren naar de services voor het ophalen en zoeken van gegevens met behulp van de API&#39;s. U kunt ook een schema maken om deze exportbewerkingen te automatiseren.

Ga als volgt te werk om de connector voor trainingsgegevens te configureren:

1. Selecteer in de app Integratiebeheer de optie **[!UICONTROL Toegang tot]** trainingsgegevens > **[!UICONTROL Aan de slag]**.
1. Selecteer **[!UICONTROL Volgende]** op de pagina Aan de **[!UICONTROL slag]** .
1. Typ de verbindingsnaam en de toegestane domeinen die zijn vermeld.

   ![](assets/connection-name-and-domain-name.png)Type verbindingsnaam en domeinnaam

1. Selecteer het **[!UICONTROL type interface]** uit de volgende opties:

   * **[!UICONTROL Native Learning Manager]**: dit is de standaardinstelling die alleen beschikbaar is voor native interface.
***[!UICONTROL Headless interfaces]**: dit is de premium-aanbieding die API&#39;s beschikbaar maakt voor een ervaring die niet is aangemeld.

   ![](assets/types-of-interface.png)Typen interface

1. Selecteer **[!UICONTROL Verbinden]**. De basis-URL en de CDN-URL worden automatisch gegenereerd.
U kunt deze URL&#39;s gebruiken om de gegevens op te halen met behulp van API&#39;s.

   >[!NOTE]
   >
   >Klanten die gebruikmaken van de premium-aanbieding, krijgen een andere URL dan klanten die de standaardversie gebruiken.


1. Selecteer **[!UICONTROL Trainingsmetagegevens]** exporteren op de pagina connector.
1. Selecteer **[!UICONTROL Export van]** trainingsmetagegevens via deze verbinding inschakelen om de trainingsgegevens te exporteren.
1. Nadat u de verbinding hebt ingeschakeld, worden de afbeeldingen van alle cursussen, leerpaden en certificaten gemigreerd naar de CDN.
1. Exporteer de metagegevens van de cursussen, leerpaden en certificaten naar de service voor zoeken en ophalen.
1. U kunt de export van metagegevens plannen door de optie Schema inschakelen te selecteren. Dit schema wordt automatisch om de 3 uur voor het premiumlidmaatschap uitgevoerd.
1. Voor een on-demand rapport gaat u naar **[!UICONTROL On Demand]**, selecteert u de **[!UICONTROL begindatum]** en **[!UICONTROL klikt u op]** Uitvoeren.
U kunt de status van de uitvoering van het rapport controleren op de pagina Status]**van uitvoering**[!UICONTROL .

### Website maken in AEM

**Vereist:** installeer het AEM-pakket vanuit de  [**opslagplaats**](https://github.com/adobe/adobe-learning-manager-reference-site/releases/tag/1.0.0) Voor GitHub.

1. Gebruik basis- en opvraag-URL&#39;s, client-id, client-geheim en Admin Refresh Token, en maak een configuratie in AEM.
1. Maak de website met behulp van de AEM-componenten.
1. Publiceer de website.

Raadpleeg dit  [**document**](../../adobe-learning-manager-integration-aem.md) voor meer informatie.

### Studenten

De gepubliceerde website toont een lijst met alle gemigreerde cursussen, certificaten en leertrajecten die zijn opgehaald uit de zoekservice voor niet-aangemelde studenten.

Wanneer een student op cursus, certificaat of leerpad klikt, wordt de overzichtspagina geopend. Wanneer de student zich inschrijft, moet deze zich eerst op de pagina aanmelden en daarna de cursus volgen.

## Adobe Commerce-connector

>[!NOTE]
>
>Deze specifieke functionaliteit is alleen beschikbaar als Adobe Learning Manager wordt verkocht als add-on voor Adobe Experience Manager.

>[!NOTE]
>
>Deze connector kan ook worden ingeschakeld voor proefaccounts.

Adobe Learning Manager biedt nu integratie met Adobe Commerce, een platform om eCommerce-ervaringen te bouwen voor B2B- en B2C-klanten.

Adobe Commerce is een uitbreidbare en schaalbare oplossing voor commerce enablement waarmee u op één platform commerce-ervaringen via meerdere kanalen kunt opbouwen voor B2B- en B2C-klanten. Gebruik de Adobe Commerce-connector om uw Adobe Learning Manager-account te verbinden met Adobe Commerce en e-commercemogelijkheden op het leerplatform te realiseren.

Schakel deze connector in en gebruik de Adobe Commerce-functies om het leeraanbod als betaalde trainingen aan te bieden. Merk op dat u Adobe Commerce apart moet kopen voordat u het met Adobe Learning Manager kunt integreren via deze connector.

De connector integreert met Adobe Commerce door de opleidingsgegevens naar het commerceplatform te sturen, waar studenten vervolgens een betaling kunnen doen en een opleiding kunnen aanschaffen.

Naast het initiëren van een aankoop, verzamelt de connector ook aankoopgegevens van Adobe Commerce, die door Adobe Learning Manager gebruikt worden om de aankoop te valideren en toegang tot de training te ontgrendelen.

**Vereiste**

1. Schakel  [RabbitMq](https://devdocs.magento.com/cloud/project/services-rabbit.html) of een andere berichtenmakelaar in.
1. Schakel CRON in[](https://devdocs.magento.com/cloud/env/variables-deploy.html#cron_consumers_runner).
1. Bewerk voor stappen 1 en 2 de volgende bestanden:

   1. .magento.app.yaml
   1. .magento/services.yaml
   1. .magento.env.jaml

1. Opties limiet opheffen via aangepaste module. Deze stap is optioneel, maar wordt sterk aanbevolen voor grote datasets.
1. Schakel alle async API&#39;s op de pagina in. Omdat er veel gegevens kunnen zijn, gebeurt de uitvoer asynchroon. De API&#39;s van Adobe Commerce worden de aanvraagpayload genoemd. De aanvraag pusht de berichten naar een wachtrij en er komt een consument in deze wachtrij, die deze berichten verwerkt en producten aanmaakt voor de commerce. Adobe Commerce voorziet standaard niet in deze async verwerking. Daarom moet u deze optie inschakelen.
1. Voeg een link toe om terug te keren naar ALM op de succespagina van de betaling. Deze retour-URL moet geconfigureerd zijn in Adobe Commerce. De URL die voor de koppeling moet worden gebruikt. -  `https://learningmanager.adobe.com/app/learner#/postPayment`
1. Wijzig de indexering van &#39;Bij opslaan&#39; in &#39;Gepland&#39;.  Zie dit  [kB](https://support.magento.com/hc/en-us/articles/360040227191) voor meer informatie.
1. Pas de volgende patches toe. Zie  [Patches](https://devdocs.magento.com/cloud/project/project-patch.html) toepassen voor meer informatie.
1. Snel configureren.  Snel is vereist voor Adobe Commerce via de cloudinfrastructuur en wordt gebruikt in staging- en productieomgevingen. Zie [Fastly instellen](https://devdocs.magento.com/cloud/cdn/configure-fastly.html) voor meer informatie.

### De connector configureren

Klik, als integratiebeheerder, in de Adobe Commerce-connector op **[!UICONTROL Connect]**.

Voer op de configuratiepagina de volgende gegevens in. Deze details, de verificatiecodes, zijn beschikbaar in Adobe Commerce. Nadat u een integratie in Adobe Commerce hebt gemaakt, zijn de referenties daar beschikbaar.

![](assets/adobe-commerce-configuration.png)
*Adobe Commerce Connector configureren*

Zodra de Adobe Commerce-connectorverbinding ingeschakeld is, kan een auteur de prijs voor een cursus, een leerpad of een certificaat bepalen.

Nadat de cursus, het leerpad of het certificaat gepubliceerd is, kan een cursist cursussen kopen de cursisten-app.

* **Native Learning Manager:** De student kan een cursus, Leerplan of een certificaat kopen vanuit Learning Manager. Dit is alleen van toepassing wanneer de auteur een prijs heeft toegevoegd.
* **Op maat gemaakt met behulp van AEM sites:** De leerling kan een cursus kopen op een AEM-site.

### Workflow

De Adobe Commerce Administrator configureert Learning Manager als een integratie.

De auteur markeert de cursussen, leerpaden of certificaten als premium en kent prijzen toe. Deze optie is er alleen als e-commerce voor het account is ingeschakeld. Ga voor meer informatie naar [Cursussen maken](../../authors/feature-summary/courses.md).

De cursus of het leerpad zal niet beschikbaar zijn voor aankoop totdat de gegevens gesynchroniseerd zijn in Adobe Commerce.

### Cursussen exporteren naar Adobe Commerce

Nadat een auteur de prijzen voor verschillende cursussen, leerpaden of certificeringen heeft ingesteld, exporteert u, als de integratiebeheerder, de cursussen, leerpaden of certificeringen naar Adobe Commerce.

>[!NOTE]
>
>In de Adobe Learning Manager-versie van maart 2024 hebben we ondersteuning voor [Adobe Commerce 2.4.6](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-6.html?lang=en) geïntroduceerd.


1. Klik op **[!UICONTROL Trainingsmetagegevens]** exporteren > **[!UICONTROL op aanvraag]**.

1. Selecteer de datums.

1. Klik op **[!UICONTROL Uitvoeren]**. Bij een succesvolle uitvoering zullen alle cursussen of leerpaden die geprijsd zijn, verplaatst worden naar Adobe Commerce. De leerling kan de cursus vervolgens kopen bij Learning Manager.

### Native Learning Manager met Adobe Commerce

#### Student

Als student moet u aangemeld zijn om een cursus, een certificaat of een leerpad te kopen.

Om een cursus aan te schaffen klikt u op Nu kopen. U wordt doorverwezen naar Adobe Commerce om de aankoop te voltooien. Zodra de betaling is uitgevoerd, zie je een bericht waarin je wordt gevraagd om terug te gaan naar Learning Manager en de cursus te starten. Je moet je ook afzonderlijk aanmelden bij Adobe Commerce om de aankoop te voltooien.

Als u een cursus, certificaat of leerpad aanschaft via ALM Native of AEM, ontvangt u e-mails van zowel ALM als Adobe Commerce.

Daarnaast kunt u ook e-mails van Adobe Commerce in- of uitschakelen.

### AEM-sites met Adobe Commerce

Als de optie Op maat gemaakt met behulp van AEM-sites ingeschakeld is, kunt u als leerling cursussen kopen van een op maat gemaakte AEM-site.

De AEM-site zal alle metadata van Learning Manager hebben om zoeken via Adobe Commerce mogelijk te maken. De cursussen worden opgehaald van Adobe Commerce in niet-aangemelde gevallen.

Zowel ingelogd als niet ingelogd is mogelijk. Niet-aangemelde gebruikers kunnen de catalogus, leerplannen en certificaten doorzoeken en bekijken. Maar als u een cursus wilt aanschaffen, moet u inloggen op de AEM-site.

Net als bij de native Learning Manager kunt u, nadat u ingelogd bent, een cursus aan het winkelwagentje toevoegen en vervolgens de cursus bekijken of kopen.

### Adobe Commerce-connector instellen

#### Vereisten

De beheerder schakelt het selectievakje **Prijzen voor trainings** inschakelen in Bij **Instellingen > Algemeen** in de admin-app. Als deze optie is ingeschakeld, kunnen auteurs prijzen voor trainingen opgeven.  Als u een Adobe Commerce-koppeling toevoegt, is dit vinkje automatisch van toepassing.

Adobe Learning Manager ondersteunt e-commerce om opleidingen te kopen en te verkopen. Hier kunnen gebruikers opleidingen verkopen om de up-selling en cross-selling van hun producten te bevorderen.

Met de integratie van Adobe Commerce ondersteunt Adobe Learning Manager het kopen en verkopen van opleidingen om een completere klantenervaring te bieden in Customer Partner Education-scenario&#39;s.

De belangrijkste doelen van deze integratie zijn:

* Gebruikers kunnen inkomsten genereren door cursussen te verkopen op Adobe Learning Manager of een Headless-leerinterface.
* Schakel Integratie van Adobe Commerce in op het platform om cursussen te verkopen met behulp van de native app van Learning Manager en AEM.
* Laat klanten van learningmanagers formele lessen aanbieden in de vorm van betaalde cursussen.
* Laat studenten een voorvertoning van de cursussen bekijken voordat ze besluiten de training aan te schaffen.

#### Adobe Learning Manager-playlist

**Integratiebeheerder**

1. Voeg op de pagina Integratiebeheerder de Adobe Commerce-connector toe. Haal de verificaties op uit de applicatie die in Adobe Commerce is gemaakt.
1. Zodra Adobe Commerce ingeschakeld is, is e-commerce ingeschakeld op Adobe Learning Manager. De gegevens van Learning Manager worden naar Adobe Commerce gesynchroniseerd volgens een schema. De gegevens bevatten alle (betaalde) opleidingen, samen met de metadata (gebruikers, vaardigheden, naam van de auteur, prijs enz.).

>[!NOTE]
>
>Adobe Learning Manager en Adobe Commerce hebben verschillende aanmeldingen.

### AEM

In deze modus volgt een Student de cursus op een AEM-gebaseerde site, die gebouwd is met behulp van AEM-gebaseerde sjablonen en componenten.

Op de AEM-site heeft de leerling ondersteuning voor het winkelwagentje, de knop Toevoegen aan winkelwagentje, het verwijderen van cursussen uit het winkelwagentje, enzovoort.

Als de gebruiker niet ingelogd is, kan deze nog steeds zoeken naar cursuscatalogi en cursusdetails bekijken, maar geen cursus kopen. Als student moet u ingelogd zijn om een cursus te kopen.

Nadat de Student de cursus gekocht heeft, wordt hij doorverwezen naar de overzichtspagina van de cursus in de staat van inschrijving, waar hij de gekochte cursus kan volgen.

#### Headless: niet-ingelogd

Een student kan:

* Opleidingen zoeken via de zoekfunctie.
* Opleidingen filteren naar prijsbereik.

Een student kan niet:

* Een cursus aanschaffen via de Overzichtspagina.
* Betaalde inhoud bekijken.

#### Headless: ingelogd

Een student kan:

* Gratis of betaalde opleidingen ontdekken, bekijken, zoeken en filteren.

* Een cursus toevoegen aan zijn winkelwagen en dan afrekenen om hem te kopen.
* Trainingscursussen in de winkelwagen toevoegen, updaten of verwijderen.
* Gelijktijdig betalen voor meerdere trainingscursussen.
* Een betaalde cursus bekijken in de speler.
* Berichten zien als er een betalingsfout is.

* De factuur zien als bijlage bij de e-mail na het kopen van de cursus.

#### Synchronisatie op aanvraag

De synchronisatie tussen Learning Manager en Adobe Commerce vindt tweemaal per dag plaats. Nadat de beheerder een account voor e-commerce heeft ingeschakeld, worden met de **optie Voor het exporteren van trainingsmetagegevens inschakelen via deze verbinding** de afbeeldingen van de cursus, het leerpad en de certificaten opgeslagen in een openbare CDN.

Als de gegevens niet worden gesynchroniseerd, worden de prijzen niet voor studenten weergegeven.

Voor native Learning Manager geldt dat als e-commerce is ingeschakeld en de synchronisatie tussen Learning Manager en Adobe Commerce is voltooid, studenten gratis of betaalde trainingen kunnen weergeven of zoeken.

Voor AEM is er geen knop Nu kopen, maar alleen een **knop Toevoegen aan winkelwagentje** . Deze knop blijft ook uitgeschakeld als de synchronisatie niet wordt uitgevoerd.

#### Veelgestelde vragen

+++Welke cursussen kunnen niet worden gekocht?

Cursussen zoals herhaalde certificeringen, opleidingen van de inhoudsmarkt, verworven opleidingen, opleidingen van connectoren, Taakhulpen en door de manager goedgekeurde/genomineerde cursussen, kunnen niet door een student gekocht worden.
+++

+++Zijn er wijzigingen in het transcript en trainingsrapport voor de leerling?

Deze rapporten tonen de prijs en de datum van aankoop van alle gekochte trainingen in de rekening.
+++

+++Kan een leerling zich inschrijven voor een gratis training?

Ja, een student kan zich inschrijven voor een gratis opleiding. Een gratis opleiding toont de knoppen voor voorvertoning en inschrijving op de overzichtspagina.
+++
