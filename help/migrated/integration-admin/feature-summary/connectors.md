---
description: Leer hoe u diverse connectoren integreert in Learning Manager
jcr-language: en_us
title: Learning Manager-connectoren
contentowner: jayakarr
exl-id: 1f44934b-6a2b-484d-bc7f-d0f23e3008ca
source-git-commit: 5afe808b0fe862385afa1691abbbc076016d21df
workflow-type: tm+mt
source-wordcount: '15865'
ht-degree: 59%

---

# Learning Manager-connectoren

Bedrijven hebben andere toepassingen en systemen die geïntegreerd moeten worden met Learning Manager. Connectoren zijn hulpprogramma&#39;s die helpen bij het uitvoeren van op data gebaseerde integraties, zoals het importeren van gegevens in Learning Manager van externe systemen.  Het voert ook het exporteren van gegevens naar externe systemen uit vanuit Learning Manager.

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
>Met de versie van November 2022 van Adobe Learning Manager, heeft het Gezoem [ authentificatie JWT tegen Juni 2023 ](https://marketplace.zoom.us/docs/guides/auth/jwt/) afgekeurd. Volgens deze aankondiging werkt de Zoom-connector met JWT tot de genoemde datum, maar wij raden gebruikers aan om een server-naar-server OAuth-app te maken om deze functionaliteit in de accounts te vervangen. Elke nieuwe verbinding beschikt standaard over Zoom OAuth-verificatie.

## Salesforce-connector {#sfconnector}

De Salesforce-connector verbindt Learning Manager met Salesforce-accounts om de synchronisatie van gegevens te automatiseren. De mogelijkheden van de Salesforce-connector zijn als volgt:

### Kenmerken toewijzen {#map-attributes}

De integratiebeheerder kan Salesforce-kolommen kiezen en aan de overeenkomstige groepeerbare kenmerken van Learning Manager toewijzen. Wanneer de toewijzing is voltooid, wordt dezelfde toewijzing voor verdere gebruikersimporten gebruikt. De beheerder kan de toewijzing opnieuw configureren als deze een andere toewijzing voor het importeren van gebruikers wil.

### Geautomatiseerde gebruikersimport {#automated-user-import}

Via het proces voor gebruikersimport kan de Learning Manager-beheerder werknemersgegevens uit Salesforce ophalen en automatisch in Learning Manager importeren. Door deze automatisering hoeft het creëren van CSV&#39;s en het uploaden naar Learning Manager niet handmatig te gebeuren.

### Automatisch plannen {#auto-schedule}

Het kan effectief zijn om de functie voor automatische planning samen met de functie voor geautomatiseerde gebruikersimport te gebruiken. De Learning Manager-beheerder kan het schema volgens de behoeften van de organisatie instellen. Gebruikers in de toepassing Leermanager kunnen volgens het schema up-to-date zijn. De synchronisatie kan dagelijks worden uitgevoerd in de Learning Manager-toepassing.

### Gebruikers filteren {#filtering-user}

De Learning Manager-beheerder kan gebruikers filteren voordat ze worden geïmporteerd. Zo kan de Learning Manager-beheerder er bijvoorbeeld voor kiezen om alle gebruikers in de hiërarchie onder één of meer specifieke managers te importeren.

### De Salesforce-connector configureren {#configuresalesforceconnector}

Als u Salesforce wilt integreren met Learning Manager, moet u het proces leren

#### vereisten van het proces leren kennen {#prerequisites}

Zorg ervoor dat u uw organisatie-URL voor Salesforce hebt. Bijvoorbeeld, als uw organisatienaam **myorg** is, zou Salesforce URL `https://myorg.salesforce.com` kunnen zijn. Dit is alles wat u moet invoeren om het Salesforce-account met Learning Manager te verbinden.

Zorg er ook voor dat u de juiste gegevens hebt om u bij het account aan te melden.

#### Een verbinding maken {#createaconnection}

1. Beweeg de muis over de Salesforce-kaart/miniatuur op de Learning Manager-startpagina. Er verschijnt een menu. Klik op **[!UICONTROL Verbinden]** in het menu.

   ![](assets/mouserover-salesforce.png)

   *verbind optie*

1. Er verschijnt een dialoogvenster waarin u wordt gevraagd om de org-url in te voeren. Klik **[!UICONTROL verbind]** na het verstrekken van URL.
1. Zodra de verbinding tot stand is gebracht, verschijnt de overzichtspagina.

### Kenmerken toewijzen {#mapattributes}

Zodra de verbinding tot stand is gebracht, kunt u Salesforce-kolommen toewijzen aan de corresponderende kenmerken van Learning Manager. Deze stap is verplicht.

1. Op de toewijzingspagina ziet u links de kolommen van de Leermanager en rechts de kolommen van Salesforce. Selecteer de juiste kolomnaam die is toegewezen aan de kolomnaam van de leermanager.

   ![](assets/sfdc-map-columns.png)
   *Kenmerken toewijzen*

   >[!NOTE]
   >
   >De kolomgegevens van de leermanager die aan de linkerkant worden weergegeven, worden opgehaald uit de actieve velden. Het **manager** gebied moet aan een gebied van type e-mailadres worden in kaart gebracht. U moet alle kolommen toewijzen voordat u de connector kunt gebruiken.

1. Klik **[!UICONTROL sparen]** na de voltooiing van de afbeelding.
1. De connector is nu klaar voor gebruik. Het account dat is geconfigureerd verschijnt als een gegevensbron binnen de beheerdersapp. De beheerder kan de import of synchronisatie op verzoek plannen.

## Gebruik van de Salesforce-connector {#usingsalesforceconnector}

De Salesforce-connector maakt verbinding met Salesforce.com om de geconfigureerde gebruikers op te halen en toe te voegen aan Learning Manager.

### Gebruikers importeren van Salesforce-contacten {#import-salesforce-contacts}

Learning Manager verbetert de Salesforce-connector nu zodat zowel contacten als Salesforce-gebruikers worden opgehaald en automatisch geïmporteerd in Learning Manager.

Voer op de Salesforce-connector-pagina de Salesforce-URL in en voltooi de verificatie. Nadat u zich hebt geverifieerd, kunt u doorgaan met het importeren van gebruikers of contactpersonen. Als u de optie Contactpersonen kiest, geeft u de subset op van de contactpersonen die u wilt importeren.

Kies de Salesforce-kolommen en wijs deze toe aan de overeenkomstige groepeerbare kenmerken van de Learning Manager. Wanneer de toewijzing is voltooid, wordt dezelfde toewijzing voor verdere gebruikersimporten gebruikt.

1. Aanmelden bij Salesforce.
1. Voor de verbindingspagina, klik **[!UICONTROL de Invoer Interne Gebruikers]**.

   ![](assets/image048.png)
   *de Invoer interne gebruikers*

1. Op de **pagina van de Gebruikers van de Invoer**, is er een nieuwe optie, Contacten. Klik de radioknoop **Contacten** en u zult de volgende opties zien.

   ![](assets/image050.png)
   *Kaart de contactattributen*

1. Als u **[!UICONTROL ja]** klikt, kunt u het volgende uitvoeren:

   * **kies de kolom van Contacten:** selecteer het gebied dat u in Leermanager wilt invoeren.
   * **specificeer waarden:** kies de waarden die het geselecteerde gebied vertegenwoordigen.

   ![](assets/image053.png)
   *specificeer de waarden*

   * Wijs de Salesforce-kolommen toe aan die van Learning Manager.
   * Om te beginnen invoerend, klik **[!UICONTROL sparen]**.

1. Als u **[!UICONTROL Nr klikt. Importeer alle Contacten]**, kunt u de gebieden direct in kaart brengen zonder de contacten te filtreren. Hier importeert u alle contactpersonen uit Salesforce.
1. Om te beginnen invoerend, klik **[!UICONTROL sparen]**.

## Leerrecords exporteren {#export-learning-records}

Learning Manager biedt de mogelijkheid om leerrecords zoals transcripten, gebruikersrapporten en vaardigheidsrapporten te exporteren naar Salesforce. U kunt bepalen of de geëxporteerde gegevens moeten worden gekoppeld aan de tabel &#39;Gebruiker&#39; of de tabel &#39;Contactpersonen&#39; in Salesforce.

![](assets/export-events-new.png)
*het Exporteren leerverslagen*

### Aangepaste objecten in Salesforce {#custom-objects-in-salesforce}

Voordat u leerrecords uit Leerbeheer exporteert, moet u aangepaste objecten in Salesforce maken. Aangepaste objecten zijn objecten die u maakt om informatie op te slaan die specifiek is voor uw bedrijf of sector. Zie [Aangepaste objecten van Salesforce](https://trailhead.salesforce.com/en/content/learn/modules/data_modeling/objects_intro) voor meer informatie.

Zo maakt u de objecten:

1. Download en installeer de pakketten om de aangepaste objecten te maken.

   * [Pakket 1](https://test.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WPJ)
   * [Pakket 2](https://test.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WPT)
   * [Pakket 3](https://test.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WPi)

1. Hernoem de namen van de aangepaste objecten in Salesforce.
1. Selecteer de gebeurtenis en klik op **[!UICONTROL Opslaan]**.

>[!NOTE]
>
>Zorg ervoor dat de systeembeheerder toegang heeft tot alle actieve velden die na de pakketinstallatie zijn toegevoegd.

**de gebeurtenissen van de Verbinding met:** kies welke sectie u wilt uitvoeren - Gebruiker of Contact. Als u Contactobject kiest, worden gebruikers die wel in Leerbeheer aanwezig zijn maar niet in Salesforce, in Salesforce gemaakt.

![](assets/link-events.png)
*de gebeurtenisoptie van de Verbinding*

>[!NOTE]
>
>U kunt meerdere verbindingen maken in één account. Een enkele verbinding kan tot drie aangepaste objecten in Salesforce dienen. Als u meerdere verbindingen voor hetzelfde Salesforce-account wilt maken, moet u de drie pakketten installeren. We bieden ondersteuning tot drie pakketten.
>
>U moet net zoveel pakketten installeren als het aantal verbindingen dat u wilt maken.

>[!NOTE]
>
>Op de pagina Uitvoeringsstatus voor Salesforce kan het aantal verwerkte records alleen worden gecontroleerd vanuit Salesforce. In Learning Manager wordt de status weergegeven als voltooid, zelfs als alle records die zijn verwerkt gedeeltelijk zijn geëxporteerd of niet zijn voltooid.

## Het Salesforce-pakket installeren {#install-salesforce-package}

Learning Manager biedt een Salesforce App-pakket. Na de installatie en configuratie in SFDC kunnen verkoopmedewerkers hun trainingsactiviteiten uitvoeren in de SFDC-portal. Met deze app kunnen SFDC-gebruikers nieuwe trainingen verkennen, aanbevelingen bekijken en deze rechtstreeks in de SFDC-portal gebruiken. Gebruikers ontvangen de aankondigingen die door beheerders worden verzonden in de vorm van mastheads rechtstreeks binnen de app in de SFDC-portal.

### Instellen in de Learning Manager-app. {#setup-in-learning-manager-app}

1. Meld u als integratiebeheerder bij uw Learning Manager-beheerdersaccount aan.
1. Klik **[!UICONTROL Toepassingen]** > **[!UICONTROL Aanbevolen Apps]**.
1. Klik **[!UICONTROL Salesforce]**.
1. Let op de toepassingspagina van Salesforce op de toepassings-id (ook wel client-id genoemd) en het clientgeheim dat in de beschrijving wordt vermeld.
1. Klik **[!UICONTROL goedkeuren]** en uw app moet met succes worden goedgekeurd.
1. Klik {de Middelen van de Ontwikkelaar 1} > **[!UICONTROL Tokens van de Toegang voor het Testen en Ontwikkeling]**.****
1. In de sectie OAuth Code ophalen moeten de client-id en het bereik worden ingesteld op - admin:read,admin:write. Klik **[!UICONTROL voorleggen]**.
1. Voer bij Vernieuwingstoken ophalen de client-ID en het clientgeheim in. Klik **[!UICONTROL voorleggen]** en neem nota van het vernieuwingstoken.

### Account aanmaken in de Salesforce-app {#create-account-in-salesforce-app}

1. Maak een account aan op de aanmeldingspagina van Salesforce. U moet een Salesforce-account maken in de editie voor ontwikkelaars of ondernemingen.  [ de inschrijver URL van de Ontwikkelaar ](https://developer.salesforce.com/signup). Zorg ervoor dat u de e-mail-ID gebruikt om u aan te melden voor Salesforce die u voor Leerbeheer hebt gebruikt.
1. Verifieer uw account via de verificatie-e-mail.
1. Maak een wachtwoord aan en meld u aan bij Salesforce.
1. Noteer de Salesforce-URL na aanmelding (bijvoorbeeld site.lightning.force.com)

### Installeer het Learning Manager-pakket {#install-learning-manager-package}

Als u het pakket wilt installeren, moet u eerst het bestaande pakket in Salesforce verwijderen. Voordat u de installatie ongedaan maakt, moet u de instellingen inschakelen, zoals hieronder weergegeven. U moet deze instellingen toepassen, anders kunt u het pakket niet installeren.

>[!NOTE]
>
>De Adobe Learning Manager-app wordt alleen ondersteund in de Salesforce Lightning-weergave.

1. Lanceer het [ pakket url van de Manager leerden ](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t1k0000008WOQ).
1. In de **Login** pagina, klik **[!UICONTROL het Domein van de Douane van het Gebruik]**.
1. Ga het pakket URL in en klik **[!UICONTROL verdergaan]**. Op de installatiepagina moet de optie Installeren voor alleen beheerders zijn geselecteerd. Wijzig deze optie niet.
1. Klik **[!UICONTROL installeer]**. Zodra het pakket wordt geïnstalleerd, klik **[!UICONTROL Gedaan]**. U wordt naar de pagina Geïnstalleerde pakketten geleid en u kunt het geïnstalleerde Adobe Learning Manager-pakket zien.
1. Ga naar het startprogramma voor apps (naast Configuratie) en zoek naar Adobe Learning Manager.
1. Om app te vormen, klik **[!UICONTROL vormen]**.
1. Klik **[!UICONTROL Nieuw]** en voeg de volgende details toe:

   * **Configuratie:** Voer een naam naar keuze in.
   * **ClientID**: Ga de waarde in die u van de eerste sectie had verkregen.
   * **ClientSecret:** ga de waarde in die u van de eerste sectie had verkregen.
   * **RefreshToken:** ga de waarde in die u van de eerste sectie had verkregen.
   * **LearningManagerBaseURL:** URL van de plaats waar het Leren Manager wordt ontvangen.

### Instellingen voor externe site toevoegen {#add-remote-site-settings}

1. In de hoger-juiste hoek van de pagina, klik **[!UICONTROL Opstelling]**.
1. In **[!UICONTROL Snelle Vondst]**, onderzoek naar de Montages van de Verre Plaats.
1. Klik **[!UICONTROL Nieuwe Verre Plaats]**.
1. Voer de gegevens in:

   * **Naam van externe site:** Voer een naam naar keuze in.
   * **Remote Site URL:** De URL van de site waar Learning Manager wordt gehost.

1. Start Learning Manager.

### Meldingen inschakelen voor de app Leermanager {#enable-notifications-for-learning-manager-app}

1. In de hoger-juiste hoek, klik **[!UICONTROL Opstelling]**.
1. Zoek naar aangepaste meldingen.
1. Klik **[!UICONTROL Nieuw]**.
1. Voer de volgende gegevens in:

   1. **Naam van het Bericht van de Douane:** LearningManagerNotification
   1. **API Naam:** LearningManagerNotification

1. Selecteer zowel **Desktop** als **Mobiel** als Gesteunde kanalen.

1. Klik op **[!UICONTROL Opslaan]**.
1. Volg de onderstaande stappen om pushmeldingen voor mobiele apparaten in te schakelen:

   1. Installeer de mobiele Salesforce-app op uw mobiele telefoon.
   1. Meld u aan bij de app met uw gegevens.
   1. Ga naar **Opstelling** > **Montages van de Levering van het Bericht**.
   1. Voeg Salesforce toe voor iOS en Android.

### Deïnstalleer Learning Manager bij Salesforce

1. Ga in de Salesforce-app naar Geïnstalleerde pakketten.
1. Klik **[!UICONTROL Uninstall]**.

## Learning Manager configureren voor Salesforce-gebruikers {#configure-learning-manager-for-salesforce-users}

De Learning Manager-app is ook beschikbaar voor gebruikers die in een Salesforce-account aanwezig zijn. De beheerder van Salesforce kan gebruikers toevoegen op basis van de profielen. De Salesforce-profielen komen overeen met die in Learning Manager. Bijvoorbeeld beheerder, integratiebeheerder, docent enzovoort. De Salesforce-beheerder kan ook een aangepast profiel maken.

Als Salesforce-beheerder kunt u de profielen aan gebruikers toewijzen of een aangepast profiel maken.

![](assets/create-profile.png)

U kunt het Salesforce-profiel aan de studenten toewijzen wanneer u het pakket installeert.

Nadat u het pakket hebt geïnstalleerd, moet u het profiel configureren.

Klik **[!UICONTROL vormen]** > **[!UICONTROL Nieuw]**, en voeg dan het volgende toe:

* Configuratienaam
* Client-id
* Clientgeheim
* LearningManagerBaseURL
* Omleiden uitschakelen

>[!NOTE]
>
>Studenten kunnen de app Leermanager alleen weergeven als u de app voor alle studenten inschakelt.

Vervolgens geeft u toegang tot de Learning Manager-app.

![](assets/permission-set.png)

*Vastgestelde toestemmingen om tot de Leermanager app* toegang te hebben

Selecteer de gebruikers en wijs de betreffende machtigingen toe. De studenten hebben nu toegang tot de Learning Manager-app.

Nu selecteert u een profiel, een standaard profiel van een gebruiker bijvoorbeeld, en klikt u op het profiel. Klik **[!UICONTROL uitgeven]** en in de **sectie van de Montages van de Toepassing van de Douane**, laat de controle-doos **Adobe Learning Manager** toe. Hierdoor heeft de student toegang tot de app.

In de vervolgkeuzelijst **Startpagina voor studenten** selecteert u in de sectie **Aangepaste tabbladinstellingen** de optie **Standaard ingeschakeld**.

U moet de app voor alle profielen zichtbaar maken.

Klik **[!UICONTROL sparen]** en de studenten die tot alle profielen behoren zullen tot de app van de Leermanager toegang hebben.

### Wijzigingen met betrekking tot leerpad {#learning-path-changes}

#### Bestaande verbindingen {#existing-connections}

Als de optie Leerpad is uitgeschakeld in het beheerdersaccount, worden er geen rijen en kolommen toegevoegd aan het rapport.

Als de optie Leerpad is ingeschakeld in het beheerdersaccount, wordt de kolom &quot;Type&quot; gevuld met Leerpad voor het geval studenten zich ervoor inschrijven.

>[!NOTE]
>
>Als de vlag wordt toegelaten en u een bestaande verbinding gebruikt, kunnen een paar verslagen worden gemist.

#### Nieuwe verbindingen {#new-connections}

Als de optie Leerpad is uitgeschakeld in het beheerdersaccount, bestaat het trainingsrapport uit de volgende kolommen, maar bevat het geen gegevens.

* **Ingesloten pad:** geeft de naam van het leerprogramma weer.
* **Ingesloten pad-ID:** geeft de ID&#39;s voor het leerprogramma weer.
* **Ingebedde identiteitskaart van de Cursus:** toont IDs van cursussen die binnen een Leerweg zijn.

Daarnaast worden de drie nieuwe kolommen weergegeven voor nieuwe verbindingen in accounts waarvoor leerpad is ingeschakeld en stromen alle gegevens door.

Bovendien bevat het rapport het kolomtype Leerpad (hoger niveau) voor alle studenten die zijn ingeschreven voor een leerpad.

In de kolom Type wordt de naam van het leerprogramma gewijzigd in Leerpad. Bestaande verbindingen wijzigen niet.

## Learning Manager FTP-connector {#ftpconnector}

Met behulp van de FTP-connector kunt u Learning Manager integreren met willekeurige externe systemen om de synchronisatie van gegevens te automatiseren. Van externe systemen wordt verwacht dat ze gegevens in een CSV-formaat kunnen exporteren en in de juiste map van het Learning Manager FTP-account kunnen plaatsen. De mogelijkheden voor FTP-connector zijn als volgt:

U kunt ook de Box-connector gebruiken voor gegevensmigratie, gebruikersimport en gegevensexport. Zie Box connector voor meer informatie.

### Gegevensimport {#data-import}

Met het gebruikersimportproces kan de beheerder van de leermanager werknemersgegevens ophalen van de FTP-service van de Learning Manager en deze automatisch importeren in Learning Manager. Met behulp van deze functie kunt u meerdere systemen integreren door de door deze systemen gegenereerde CSV in de juiste mappen van de FTP-accounts te plaatsen. De Learning Manager haalt de CSV-bestanden op, voegt deze samen en importeert de gegevens volgens de planning. Raadpleeg de planningsfunctie voor meer informatie.

**Kenmerken toewijzen**

De integratiebeheerder kan de kolommen van CSV kiezen en deze toewijzen aan de groepeerbare kenmerken van de Learning Manager. Deze toewijzing is een tijdsinspanning. Zodra de toewijzing is voltooid, wordt dezelfde toewijzing gebruikt voor de daaropvolgende gebruikersimporten. De toewijzing kan opnieuw worden geconfigureerd als de beheerder een andere toewijzing voor het importeren van gebruikers wil hebben.


#### Gegevens exporteren {#export-data}

Gevensexport stelt gebruikers in staat om de vaardigheden van de gebruiker en de transcripten van de student te exporteren naar een FTP-locatie om deze te integreren met een willekeurig systeem van derden.

#### Planning {#scheduling}

Beheerders kunnen planningstaken volgens de vereisten van de organisatie instellen en gebruikers in de toepassing Leermanager zijn up-to-date volgens de planning. Op dezelfde manier kan de integratiebeheerder de export van vaardigheden tijdig plannen om deze te integreren met een extern systeem. Synchronisatie kan dagelijks worden uitgevoerd in de toepassing Learning Manager.

### Learning Manager FTP-connector configureren {#configure-captivate-prime-ftp-connector}

Leer het proces om de FTP-connector te integreren met Learning Manager.

#### Een verbinding maken {#Create-a-connection-1}

1. Beweeg de muis over de FTP-kaart/miniatuur op de startpagina van Learning Manager. Er verschijnt een menu. Selecteer het Connect-item in het menu.

   ![](assets/mouseover-ftpconnector.png)

   *verbind optie*

Als u via FTP-client verbinding wilt maken met een FTP-server, hebt u de volgende informatie nodig:

* **Domein van FTP**: Dit is het adres van de server van FTP u wilt verbinden met. Bijvoorbeeld: ftp.example.com
* **Haven**: De standaardFTP haven is 21, maar sommige servers zouden verschillende havens om veiligheidsredenen kunnen gebruiken. Voor Adobe Learning Manager - poort 22
* **Gebruikersnaam van FTP**: De gebruikersbenaming u moet tot de server van FTP toegang hebben.
* **Wachtwoord van FTP**: Het wachtwoord verbonden aan de gebruikersbenaming.

**FileZilla (Vensters, macOS, en Linux)**

**Stap 1: Download en installeer FileZilla**

Als u FileZilla nog niet hebt geïnstalleerd, download het van de officiële website: [ Download ](https://filezilla-project.org/) en installeer het op uw computer.

**Stap 2: Open FileZilla**

Start FileZilla na de installatie op uw computer.

**Stap 3: Verzamel de Informatie van de Server van FTP**

**Stap 4: Ga de Informatie van de Server van FTP in FileZilla** in

In het hoogste menu, selecteer **[!UICONTROL Dossier]** en selecteer dan **[!UICONTROL Manager van de Plaats]** (of gebruik de kortere weg Ctrl+S).

**Stap 5: Voeg Nieuwe Plaats van FTP toe**

In de Manager van de Plaats, selecteer **Nieuwe Plaats** en typ een naam (b.v., Mijn Server van FTP).

**Stap 6: Ga de Details van FTP** binnen

Typ de volgende informatie:

* **Gastheer**: Type het adres van uw server van FTP.
* **Haven**: Als de server een haven meer dan 21 gebruikt, ga het correcte havenaantal in.
* **Protocol**: Kies **[!UICONTROL SFTP - het Protocol van de Overdracht van het Dossier SSH]**.
* **Type van Logon**: Selecteer **[!UICONTROL Normaal]**.
* **Gebruiker**: Type uw gebruikersbenaming van FTP.
* **Wachtwoord**: Type uw wachtwoord van FTP.

**Stap 7: Verbind met de Server van FTP**

Selecteer **[!UICONTROL verbind]** knoop in de Manager van de Plaats. FileZilla maakt verbinding met de FTP-server als alle gegevens correct zijn.

**Stap 8: Navigeer en breng Dossiers** over

Zodra de verbinding tot stand is gebracht, ziet u de externe bestanden aan de rechterkant en de lokale bestanden aan de linkerkant. U kunt door de mappen navigeren en bestanden overbrengen door deze tussen de deelvensters te slepen.

>[!CAUTION]
>
>Vermijd het wijzigen van belangrijke bestanden op de server wanneer u bestanden overbrengt.

<!--1. A dialog appears prompting you to enter the email id. Provide the email id of the person responsible for managing the Learning Manager FTP account for the organization. Click **[!UICONTROL Connect]** after providing the email id. 
1. Learning Manager sends you an email prompting the user to reset the password before accessing the FTP for the first time. The user must reset the password and use it for accessing the Learning Manager FTP account.

   >[!NOTE]
   >
   >Only one Learning Manager FTP account can be created for a given Learning Manager account.

   In the overview page, you can specify the Connection Name for your integration. Choose what action you want to take  from  the following options:

   * Import Internal Users  
   * Import xAPI
   * Export User Skills - Configure a Schedule  
   * Export User Skills - OnDemand  
   * Export Learner Transcripts - Configure a Schedule
   * Export Learner Transcripts - OnDemand

   ![](assets/ftp-connector-dashboard.png)
   *Export options*-->

### Importeren {#import}

+++ interne gebruiker

Met de optie voor het importeren van interne gebruikers kunt u de gebruikers van een CSV importeren in een Leermanager op verzoek of tijdens het plannen.

+++

+++Kenmerken toewijzen

Zodra de verbinding tot stand is gebracht, kunt u de kolommen van de CSV-bestanden toewijzen. Het bestand wordt in de FTP-map geplaatst bij de overeenkomstige attributen van Learning Manager. Deze stap is verplicht.

1. Op de pagina Kenmerken toewijzen ziet u links de verwachte kolommen van de leermanager en rechts de CSV-kolomnamen. In eerste instantie ziet u aan de rechterkant een leeg selectievakje. Importeer om het even welke malplaatje CSV door te klikken **verkies Dossier**.
1. Via de bovenstaande stap worden alle CSV-kolomnamen aan de rechterkant van de vervolgkeuzelijst ingevuld. Selecteer de juiste kolomnaam die is toegewezen aan de kolomnaam van de leermanager.

   >[!NOTE]
   >
   >Het veld Manager moet worden toegewezen aan een veld van het type e-mailadres. U moet alle kolommen toewijzen voordat u de connector kunt gebruiken.

1. Selecteer **[!UICONTROL sparen]** na de voltooiing van de afbeelding.

   De connector is nu klaar voor gebruik. Het geconfigureerde account verschijnt als gegevensbron in de beheerdersapp zodat de beheerder de import of de synchronisatie op verzoek kan plannen.

+++

+++De FTP-connector van Learning Manager gebruiken

1. De CSV-bestanden van externe systemen moeten op het volgende pad worden geplaatst:

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   >[!NOTE]
   >
   >In de release van juli 2016 is alleen import van gebruikers toegestaan. Om de FTP-connector te gebruiken, moet u ervoor zorgen dat de CSV-bestanden in de volgende map worden geplaatst:

   `code Home/import/user/internal/*.csv`

1. De FTP-connector haalt alle rijen uit CSV-bestanden. Het is belangrijk dat de rij die overeenkomt met een gebruiker in een CSV niet in andere CSV&#39;s verschijnt.
1. Alle CSV&#39;s moeten de kolommen bevatten die in de toewijzing zijn opgegeven.
1. Alle vereiste CSV&#39;s moeten aanwezig zijn in de map voordat het proces begint.

>[!NOTE]
>
>Tijdens het importeren van gebruikers in Learning Manager moet de beheerder ook weten hoe gebruikers worden beheerd in Learning Manager. Verwijs naar [ Hulp van het Beheer van de Gebruiker ](migration-manual.md#usermanagement) om meer informatie te kennen.

+++

+++xAPI importeren

Met de opties voor xAPI-import kunt u het importeren van xAPI-statements van externe diensten in Learning Manager op verzoek plannen.

+++

+++Vereiste configuraties voor het importeren van xAPI

1. Selecteer op de configuratiepagina een bestaande configuratie die beschikbaar is in de configuratielijst om xAPI-statements uit de CSV te importeren. Klik geef uit of **voeg een nieuwe verbinding van de Configuratie** toe om aan de vorm invoer-Bronnen pagina te navigeren.

   **Configuratie**

   * Vul de velden Naam en Naam van bronbestand op de pagina configureren-importeren-bronnen in. De naam van het bronbestand moet overeenkomen met de bestandsnaam die is in de FTP-maplocatie opgegeven.
   * Klik op **[!UICONTROL Opslaan]** om uw wijzigingen op te slaan.

   ![](assets/configurations.png)
   *vorm*

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
   *de verklaringen van de Invoer xAPI - vorm Programma*

1. Van de linkerruit, klik **[!UICONTROL op Vereiste Uitvoering]**.

   ![](assets/on-demand.png)
   *de verklaringen van de Invoer xAPI - op bestelling*

1. Klik in het linkerdeelvenster op **[!UICONTROL Uitvoeringsstatus]** om het overzicht van alle runs voor deze connector in chronologische volgorde weer te geven. U kunt de begindatum en de duur van de xAPI-import, het type import (op verzoek of volgens een planning) en de status van de import (of de xAPI-import in voortgang is, of voltooid of mislukt is) bekijken.

   ![](assets/execution-status2x.png)
   *de verklaringen van de Invoer xAPI - de Status van de Uitvoering*

+++

<!--### Export

+++Skills

There are two options to export User skill reports.

**[!UICONTROL User Skills - On Demand]**: You can specify the  start date and export the report using the option. The report is extracted from the date entered until present.

![](assets/export-on-demand2x.png)
*On demand export option*

**[!UICONTROL User Skills - Configure]**: This option let's you schedule the extraction of the report. Select the Enable Schedule check box and specify the start date and time. You can also specify the interval at which you want the report to be generated and sent.

![](assets/user-skills-configure.png)
*Configure export of report*

+++

To open the Export folder where the exported files are placed, open the link to FTP Folder provided in the User Skills page as shown below.

![](assets/ftp-folder.png)
*FTP folder to view files*

The auto-exported files are present in the location **Home/export/&#42;FTP_location&#42;**

The auto-exported files are available with the title, **skill_achievements_&#42;date from&#42;_to_&#42;date to&#42;.csv**

![](assets/exported-csvs.png)
*Exported .csv file*

+++Learner Transcript

![](assets/on-demand-report.png)

**Configure**: This option  let's  you schedule the extraction of the report. Select the Enable Schedule check box and specify the start date and time. You can also specify the interval at which you want the report to be generated and sent.

![](assets/configure-report.png)

+++

To open the Export folder where the exported files are placed in your FTP location, open the link to FTP Folder provided on the Learner Transcript page as shown below

The auto-exported files are present in the location **Home/export/&#42;FTP_location&#42;**

The auto-exported files are available with the title, **learner_transcript_&#42;date from&#42;_to_&#42;date to&#42;.csv**-->

### Ondersteuning voor handmatige csv-velden {#support-for-manual-csv-fields}

Bij het importeren van gebruikersgegevens via FTP moet een beheerder alle actieve velden in het systeem toewijzen aan het juiste veld in de csv.

Dit is verplicht voor alle actieve csv-velden. Voor handmatig geactiveerde velden kan de integratiebeheerder de optie **DontImportFromSource** selecteren.

Door deze optie te selecteren worden de waarden van handmatig geactiveerde velden niet overschreven bij de csv-import. De door de student ingevulde waarden blijven intact.

>[!NOTE]
>
>Terwijl het in kaart brengen, als de optie **DontImportFromSource** voor csv actief gebied wordt geselecteerd, dan zal dit gebied van het systeem worden geschrapt.

![](assets/ftp-conector-foractivefields.png)
*de schakelaar van FTP voor Actieve gebieden*

## Lynda-connector {#lynda-connector}

De Lynda-connector wordt gebruikt door zakelijke klanten van Lynda.com die graag willen dat hun studenten Lynda-cursussen kunnen zoeken en volgen in Learning Manager. De connector kan worden geconfigureerd om periodiek cursussen van Lynda.com op te halen met uw API-sleutel. Zodra een cursus binnen Learning Manager is gemaakt, kunnen gebruikers deze opzoeken en volgen. De voortgang van de student kan vervolgens binnen Learning Manager worden bijgehouden.

### De Lynda-connector configureren {#configure-the-lynda-connector}

1. Klik op Lynda in het dashboard van de integratiebeheerder.

   U ziet de tegel met drie opties: Aan de slag, Verbinden en Verbindingen beheren.

1. Klik op Verbinden als u de Lynda-connector voor het eerst configureert.

   <!--Configure the Exavault FTP account before you configure this connector.-->

1. Geef op de verbindingspagina een naam op voor uw connector. Voer de appsleutel en de geheime sleutel voor uw verbinding in.

   >[!NOTE]
   >
   >Neem contact op met uw leverancier voor de appsleutel en de geheime sleutel.

1. Klik op Opslaan.

   De configuratie wordt opgeslagen en de Lynda-verbinding voor uw account wordt toegevoegd. U kunt nu vanaf de startpagina op Verbindingen beheren klikken en uw configuratie op elk gewenst moment bewerken.

1. Als u al een verbinding tot stand hebt gebracht, klikt u op Verbindingen beheren om al uw verbindingen te bekijken.

   >[!NOTE]
   >
   >De migratiefunctie moet zijn ingeschakeld voor uw account voordat u deze connector kunt configureren.

1. Klik op de verbinding die u wilt bewerken.
1. Van de linkerruit, klik **[!UICONTROL vormen]**. Voer een van de volgende handelingen uit:

   * Bekijk of bewerk de details van uw account en het synchronisatieschema vanuit dit venster. Schakel het selectievakje Verbinding inschakelen in als u dit account wilt inschakelen.
   * Klik op Bewerken en bewerk uw gegevens. Klik op Herstellen om uw updates voor dit veld ongedaan te maken
   * Klik op Schema inschakelen om uw synchronisatie te plannen. U kunt de starttijd en -datum invoeren en vervolgens de frequentie van uw synchronisatieplanning in dagen invoeren. Bijvoorbeeld, om de drie dagen synchroniseren.

   Klik op **[!UICONTROL Opslaan]** om uw wijzigingen op te slaan.

   ![](assets/lynda.png)

   *vorm de Lynda schakelaar voor het Leren Manager*

1. Klik in het linkerdeelvenster op Uitvoering op verzoek. Met deze optie kunt u gebruikersfeeds en andere relevante gegevens vanuit Lynda importeren. Voer de startdatum voor de uitvoering op verzoek in en klik op Uitvoeren om de synchronisatie uit te voeren. Alle gegevens vanaf de startdatum tot heden worden geïmporteerd.

   * Wanneer de toepassing tijdens de synchronisatie uitvalt, kunt u tijdens de uitvoering klikken op Toegang tot Learning Manager uitschakelen.
   * Als u tijdens de uitvoering op Toegang tot Learning Manager inschakelen klikt, is er geen onderbreking van de service tijdens de synchronisatie.

   ![](assets/lynda-ondemand.png)

   *voer op bestelling uitvoering voor Lynda schakelaar* uit

1. U kunt ook op elk moment op Uitvoeringsstatus in het linkerdeelvenster klikken om het overzicht van alle runs voor deze connector in chronologische volgorde te bekijken. U kunt de startdatum en duur van de synchronisatie, het type synchronisatie (of het al dan niet gaat om synchronisatie op verzoek) en de status van de synchronisatie (of de synchronisatie wordt uitgevoerd of is voltooid) bekijken.

   >[!NOTE]
   >
   >Wanneer u een verbinding wist en opnieuw aanmaakt, worden de vorige runs voor de connector weergegeven. U kunt alle runs bekijken voordat u de verbinding wist.

   U kunt alleen de laatste synchronisatie opnieuw uitvoeren.

   ![](assets/lynda-ondemand.png)

   *Mening de samenvatting van alle looppas klikt de Status van de Uitvoering*

## getAbstract-connector {#getabstractconnector}

De getAbstract-connector kan gebruikt worden door zakelijke klanten van getAbstract.com die graag willen dat hun studenten getAbstract-samenvattingen kunnen zoeken en volgen in Captivate Prime. De connector kan worden geconfigureerd om periodiek gebruiksgegevens op te halen, op basis waarvan de voltooiingsrecords van studenten in Learning Manager worden gemaakt. Lees verder om te weten te komen hoe u deze connector in Learning Manager moet configureren.

### De getAbstract-connector configureren {#configure-the-get-abstract-connector}

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

   *vorm de getAbstract schakelaar voor het Leren Manager*

1. Klik in het linkerdeelvenster op Configureren. Voer een van de volgende handelingen uit:

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
   [ getAbstract het blad van het de steekproefonderzoek van de gebruikersvoer ](assets/report-export-20170401175342.xlsx)

## Harvard ManageMentor-connector {#hmmconnector}

De Harvard ManageMentor-connector wordt gebruikt door zakelijke klanten van Harvard ManageMentor die graag willen dat hun studenten Harvard ManageMentor-cursussen kunnen zoeken en volgen. De connector helpt bij het maken van cursussen binnen Learning Manager en kan worden geconfigureerd om periodiek de voortgangsgegevens van studenten op te halen. Voer de volgende procedure uit om deze connector te configureren:

### De Harvard ManagerMentor-connector configureren {#configure-the-harvard-managermentor-connector}

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

   *vorm de schakelaar van de Mentor HarvardManage voor het Leren Manager*

1. Klik in het linkerdeelvenster op Configureren. Voer een van de volgende handelingen uit:

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

   hmm12_metadata.csv: Dit bestand bevat de cursusmetagegevens voor de Harvard ManageMentor-connector. Zorg ervoor dat u de naamconventie volgt wanneer u het bestand uploadt.

   client_hmm12_20150125.csv: Het is de gebruikersfeed voor de Harvard ManageMentor-connector. Het dossier het noemen overeenkomst die volgt is **client_hmm12_yyyyMMdd.csv.**

   Zie de volgende twee voorbeelden van gebruikersfeed- en cursusfeed-bestanden voor deze connector:

   * [ dossier van de meta-gegevens van de cursus voor de schakelaar van Harvard ManageMentor ](assets/hmm12-metadata.csv)
   * [Gebruikersfeed voor de Harvard ManageMentor-connector](assets/client-hmm12-20170304.csv)

## Workday-connector {#workdayconnector}

Met behulp van de Workday-connector kunt u Learning Manager integreren met Workday tenant om de synchronisatie van gegevens te automatiseren.

### Importeren {#import-1}

#### Kenmerken toewijzen {#map-attributes-1}

De integratiebeheerder kan Workday-kolommen kiezen en aan de overeenkomstige groepeerbare kenmerken van Learning Manager toewijzen. Wanneer de toewijzing is voltooid, wordt dezelfde toewijzing voor verdere gebruikersimporten gebruikt. De beheerder kan de toewijzing opnieuw configureren als deze een andere toewijzing voor het importeren van gebruikers wil.

#### Geautomatiseerde gebruikersimport {#automated-user-import-1}

Met het gebruikersimportproces kan de Learning Manager Administrator werknemersgegevens uit Workforce halen en ze automatisch in Learning Manager importeren.

#### Gebruikers filteren {#filtering-users}

Learning Manager Administrator kan gebruikers filteren voordat ze worden geïmporteerd. Zo kan de Learning Manager-beheerder er bijvoorbeeld voor kiezen om alle gebruikers in de hiërarchie onder één of meer specifieke managers te importeren.

### Exporteren {#export}

Via Gebruikersvaardigheden exporteren kunnen gebruikers automatisch gebruikersvaardigheden naar Workday exporteren.

>[!NOTE]
>
>Het is niet mogelijk vaardigheden van meerdere Learning Manager-accounts tegelijkertijd met hetzelfde Workday-account te exporteren.

#### Opmerkingen {#points-to-note}

* Zorg ervoor dat UUID, E-mailadres en naam van de medewerker uniek zijn in meerdere Workday-integraties. Onjuiste waarden leiden tot een verbindingsfout.
* Het UUID-veld dat eenmaal via Workday is ingevuld, kan niet worden verwijderd door een client-side LMS-beheerder. Als je de waarde wilt wijzigen, neem dan contact op met het Adobe Learning Manager-team voor onboarding of ondersteuning.
* De optie Gebruikers leegmaken werkt mogelijk ook niet omdat gebruikers leegmaken alleen ondersteuning biedt voor 50 gebruikers die per run moeten worden leeggemaakt. Wees uiterst voorzichtig bij het uploaden van de gebruikers via de UUID&#39;s.

### Planning {#Scheduling-1}

De beheerder kan planningstaken volgens de vereisten van de organisatie instellen en gebruikers in de Learning Manager-toepassing zijn up-to-date volgens de planning. Op dezelfde manier kan de integratiebeheerder de export van vaardigheden op een tijdige basis plannen om deze te integreren met een extern systeem. De synchronisatie kan dagelijks worden uitgevoerd in de Learning Manager-toepassing.

### De Workday-connector configureren {#configure-workday-connector}

>[!PREREQUISITES]
>
>Vraag de beheerder van Workday van uw organisatie om een Gebruiker van het Systeem van de Integratie (ISU) met de toestemmingen te creëren zoals die in het document ISU_Permissions worden bepaald. Download een exemplaar via onderstaande link.

[ Download een exemplaar van de veiligheid van het integratiesysteem gebruiker (ISU).](assets/isu-permissions-v1.pdf) Leer het proces om de Workday-connector te integreren met Learning Manager.

1. Beweeg de muis over de tegel van Workday op de startpagina van Learning Manager. Er verschijnt een menu. Klik op **[!UICONTROL Verbinden]** in het menu.

   ![](assets/workday-tile.png)

   *de tegel van Workday*

1. Er verschijnt een dialoogvenster waarin u wordt gevraagd de gegevens voor de nieuwe verbinding in te voeren. Voer de volgende velden in voordat u de verbinding tot stand brengt.

   * Verbindingsnaam: voer een verbindingsnaam naar keuze in.
   * Host-URL: de integratiebeheerder kan de host-URL-details bij de desbetreffende Workday-beheerder opvragen.
   * Tenant: de tenant is intern in uw bedrijf. U ontvangt de gegevens van de tenant van de Workday-beheerder.
   * Gebruikersnaam en wachtwoord: De Workday-beheerder maakt een geïntegreerde systeemgebruiker (ISU) met de vereiste beveiligingsrechten en deelt deze met de integratiebeheerder.

>[!NOTE]
>
>   Learning Manager gebruikt versie 40.1 van de Workday API.


![](assets/configure-connector.png)
*vorm de schakelaar van Workday*

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

### Importeren {#import-5}

#### Kenmerken toewijzen {#map-attributes-4}

U kunt de Workday-connector gebruiken om Learning Manager en Workday te integreren om de synchronisatie van gegevens te automatiseren. U kunt alle actieve gebruikers van Workday naar Learning Manager importeren. Gebruikers kunnen worden geïmporteerd vanuit verschillende gegevensbronnen, waaronder FTP en Salesforce.

Voordat gebruikers kunnen worden geïmporteerd, moeten de gebruikersattributen van Learning Manager en Workday worden toegewezen. Kies op de overzichtspagina onder Importeren voor de optie Interne gebruikers om de toewijzingsattributen op te geven.

Voer de Adobe Learning Manager-gegevens in de kolom onder Adobe Learning Manager. Gebruik de vervolgkeuzelijsten om de juiste gegevens te selecteren voor de kolommen onder Workday.

>[!NOTE]
>
>Momenteel ondersteunt Learning Manager het importeren van 69 gebruikersattributen uit Workday. Voeg via de actieve velden in Learning Manager meer attributen toe.

![](assets/workday.png)
*attributen van de Kaart*

Selecteer **Uitsluiten de Voorwaardelijke Arbeiders** checkbox om de tijdelijke arbeiders beschikbaar onder een manager te verhinderen ingevoerd te worden.

Workday heeft vier hiërarchieniveaus, terwijl Learning Manager twee niveaus heeft. De vier niveaus in Workday zijn vaardigheidsprofielcategorie, vaardigheidsprofiel, vaardigheidsitemcategorie en vaardigheidsitem. Uw vaardigheidsnaam en niveau van Leermanager worden samen toegewezen in Workday onder het vaardigheidsitem.

>[!NOTE]
>
>U kunt extra Workday-attributen toevoegen. Neem contact op met uw CSAM om de attributen toe te voegen.

+++Lijst met ondersteunde Workday-kenmerken

wd:User_ID
wd:Worker_ID
manager
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.@wd:Opgemaakte_naam
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.@wd:Opgemaakte_naam
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
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.@wd:Opgemaakte_telefoon
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
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Name
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
wd:Employment_Data.wd:Worker_Status_Data.wd:Gearchiveerd
wd:Employment_Data.wd:Worker_Status_Data.wd:Retirement_Date
wd:Employment_Data.wd:Worker_Status_Data.wd:Terminated
wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Date
wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Last_Day_of_Work
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Code
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Name
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Type_Reference.wd:ID.1.$
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Subtype_Reference.wd:ID.1.$
wd:Qualification_Data.wd:Education.0.wd:School_Name
wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Job_Title
wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Company
wd:Management_Chain_Data.wd:Worker_Surveillance_Management_Chain_Data.wd:Management_Chain_Data.0.wd:Manager.Employee_ID
Primaire werke-mail
wd:Organization_Type_Reference_cost_Center_ID
wd:Organization_Type_Reference_cost_center_name
wd:Organization_Type_Reference_Company
wd:Organization_Subtype_Reference_Department
wd:Organization_Subtype_Reference_Division
wd:Universal_ID
wd:Integration_Field_Override_Data.3.wd:Value
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.0.wd:Country_Region_Descriptor
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.0.wd:Country_Region_Reference.wd:ID.2.$
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Gemeente

+++

### Exporteren {#export-1}

U kunt alle vaardigheden van een gebruiker van Learning Manager naar Workday exporteren. Alleen actieve gebruikersvaardigheden worden geëxporteerd en Learning Manager exporteert geen gearchiveerde vaardigheden. U kunt ook meerdere Leerbeheer verbinden\
accounts aan dezelfde Workday-connector. Als de vaardigheidsnamen in twee Learning Manager-accounts hetzelfde zijn, worden ze toegewezen aan dezelfde vaardigheid in Workday. Als twee Learning Manager-accounts hetzelfde Workday-account gebruiken, is het raadzaam om de vaardigheidsnamen in alle Learning Manager-accounts bij te werken voordat u de vaardigheid in Workday bijwerkt.

+++Gebruikersvaardigheden - Configureren

Met deze optie kunt u de extractie van het rapport plannen. Zorg ervoor dat het selectievakje Exporteren van gebruikersvaardigheden via deze verbinding inschakelen is ingeschakeld. Selecteer het selectievakje Planning inschakelen en geef de begindatum en -tijd op. U kunt ook aangeven met welke intervallen u het rapport wilt laten genereren en verzenden. Schakel het selectievakje Planning inschakelen in en voer de startdatum, tijd en herhaling na een bepaald aantal dagen in. Klik op Opslaan als u klaar bent.

![](assets/configure-schedule.png)
*vorm het rapport van gebruikersvaardigheden*

+++

++ + Gebruikersvaardigheden - Op verzoek

U kunt de begindatum opgeven en het rapport exporteren met deze optie. Het rapport wordt geëxtraheerd van de ingevoerde datum tot heden. Voer de datum in vanaf wanneer u wilt beginnen met het genereren van het rapport en klik op Uitvoeren.

![](assets/on-demand-report.png)
*Op het rapport van de gebruikersvaardigheden van de vraag*

+++

++ + Gebruikersvaardigheden - Uitvoeringsstatus

Hier kunt u de samenvatting van alle taken bekijken en een statusrapport daarvan ontvangen. U kunt foutrapporten downloaden door op de foutrapportagelink te klikken.

![](assets/execution-status.png)
*het uitvoeringsrapport van de vaardigheidsuitvoering van de Gebruiker*

+++

## miniOrange-connector {#mini-orange-connector}

Met behulp van de miniOrange-connector kunt u Learning Manager integreren met miniOrange-tenant om de synchronisatie van gegevens te automatiseren.

### Importeren {#import-6}

#### Kenmerken toewijzen {#map-attributes-5}

De integratiebeheerder kan miniOrange-kenmerken kiezen en deze toewijzen aan de overeenkomstige groepeerbare kenmerken van de Learning Manager. Wanneer de toewijzing is voltooid, wordt dezelfde toewijzing voor verdere gebruikersimporten gebruikt. De beheerder kan de toewijzing opnieuw configureren als deze een andere toewijzing voor het importeren van gebruikers wil.

#### Geautomatiseerde gebruikersimport {#automated-user-import-3}

Via het gebruikersimportproces kan de beheerder van de leermanager werknemersgegevens ophalen uit miniOrange en deze automatisch importeren in Learning Manager.

#### Gebruikers filteren {#filtering-users-3}

Learning Manager Administrator kan gebruikers filteren voordat ze worden geïmporteerd. Zo kan de Learning Manager-beheerder er bijvoorbeeld voor kiezen om alle gebruikers in de hiërarchie onder één of meer specifieke managers te importeren.

Instellen   miniOrange   contact op met het CSM-team van Learning Manager.

### De miniOrange-connector configureren {#configure-mini-orange-connector}

1. Beweeg de muis over de miniOrange-kaart/miniatuur op de startpagina van Learning Manager. Er verschijnt een menu. Klik **[!UICONTROL verbind]** optie in het menu.

   ![](assets/miniorange-tile.png)

   *miniOrange schakelaartegel*

1. Klik **[!UICONTROL verbind]** om een nieuwe verbinding te vestigen. De miniOrange-connector-pagina wordt weergegeven. Vul de gegevens in van het account dat u wenst toe te wijzen.

   ![](assets/establish-connection.png)

   *creeer een verbinding*

1. Als u miniOrange gebruiker direct als Lerende interne gebruiker van de Manager wilt invoeren, gebruik de **[!UICONTROL optie van de Invoer Interne Gebruikers]**.

   ![](assets/import-users.png)

   *de Invoer interne gebruikers*

1. In de toewijzingspagina, links   ziet u de kolommen van de leermanager en rechts   zie de miniOrnage kolommen. Selecteer de juiste kolomnaam die is toegewezen aan de kolomnaam van de leermanager.

   ![](assets/map-attributes.png)

   *Kenmerken toewijzen*

1. Klik, als u de gegevensbron als beheerder wilt bekijken bewerken, op **[!UICONTROL Instellingen > Gegevensbron]**.

   De vastgestelde miniOrange-bron wordt vermeld. Als u vereist om de filter uit te geven, geeft de klik **** uit.

   ![](assets/data-source.png)

   *Mening en geef een gegevensbron* uit

1. U ontvangt een melding na voltooiing van de import. Klik op **[!UICONTROL Gebruikers > Importlogboek]** om het importlogboek te bekijken of te bewerken.

<!-- #### Delete a connection {#deleteaconnection}

To delete an established  miniOrange  connection, follow these steps. -->

## Zoomconnector {#zoom-connector}

U kunt Learning Manager integreren met Zoom-connectoren en deze gebruiken om lessen te hosten.  Met de connector kunt u vergaderingen/klassen voor videoconferenties met de studenten instellen.

Volg deze stappen om de connector in te stellen en te gebruiken.

1. Beweeg de muis over de zoomminiatuur op de startpagina van Learning Manager. Er verschijnt een menu. Klik **[!UICONTROL verbind]** optie van het menu.

   <!-- ![](assets/connectors.png)

   *Zoom connector tile* -->

1. De pagina Zoom connector wordt geopend. Voer de gegevens van uw account in de respectievelijke velden in om de gebruikersfeed te integreren en te synchroniseren. U kunt de gegevens van de beheerder van uw connectoraccount opvragen.

   <!-- ![](assets/bluejeans-connecotrpage.png)
   *Connect to BlueJeans/ Zoom* -->

   >[!NOTE]
   >
   >Als student gebruikt u bij het inschakelen van de connector dezelfde e-mail-ID die gebruikt wordt voor uw Learning Manager-account om gebruikersfeeds terug te laten keren naar Learning Manager.

1. Zodra de verbinding tot stand is gebracht, maakt u als auteur een VC-cursus met Zoomen als conferentiesysteem.

   <!-- ![](assets/vc.jpg)
   
   *Create a VC course* -->

1. Beheerders, managers en studenten kunnen studenten voor de gemaakte cursus inschrijven. Bij inschrijving ontvangt de student een e-mail. De student kan zich aanmelden op zijn Learning Manager-account om de details van het programma te bekijken en de cursus te volgen.
1. Na afloop van de cursus wordt het eindrapport naar Learning Manager gestuurd. De beheerder kan het voltooiingsrapport bekijken om de aanwezigheid en de score van de studenten te controleren.

   ![](assets/attendence-and-scoringreport.png)
   *Aanwezigheid en het schrapen rapport*

### Een zoomserver-naar-server-OAuth-app maken {#create-a-zoom-server-to-server-oauth-app}

Wanneer u een Zoom Server-to-Server OAuth-app maakt voor gebruik in Adobe Learning Manager, moet u het bereik toevoegen dat door Adobe Learning Manager is vereist tijdens het maken van de verbinding.

Voor Adobe Learning Manager zijn de onderstaande bereiken vereist. De bereiken moeten worden geselecteerd in de OAuth-app.

* Alle gebruikersvergaderingen weergeven `/meeting:read:admin`
* Alle gebruikersvergaderingen weergeven en beheren `/meeting:write:admin`
* Rapportgegevens weergeven `/report:read:admin`
* Alle gebruikersinformatie weergeven `/user:read:admin`
* Gebruikersgegevens weergeven en gebruikers beheren `/user:write:admin`
* Een registrant voor een vergadering toevoegen `/meeting:write:registrant:admin`
* Alle registranten van vergaderingen weergeven `/meeting:read:list_registrants:admin`
* Gebruikersvergaderingen van subaccounts weergeven en beheren `/meeting:write:meeting:master`
* Rapportgegevens weergeven `/report:read:list_meeting_participants:admin`

## Box-connector {#box_connector}

Met de Box-connector kunt u Learning Manager integreren met willekeurige externe systemen om de synchronisatie van gegevens te automatiseren. Verwacht wordt dat externe systemen gegevens kunnen exporteren in een CSV-indeling en deze in de juiste map van het Learning Manager Box-account kunnen plaatsen. De mogelijkheden van de Box-connector zijn als volgt:

U kunt de FTP-connector ook gebruiken voor gegevensmigratie, gebruikersimport en gegevensexport. Ga voor meer informatie naar [Learning Manager FTP-connector.](connectors.md#main-pars_header_1427405935)

### Gegevensimport {#data-import-1}

Met het gebruikersimportproces kan de Learning Manager Administrator werknemersgegevens uit de Learning Manager Box-service halen en ze automatisch in Learning Manager importeren. Met behulp van deze functie kunt u meerdere systemen integreren door de door deze systemen gegenereerde CSV in de juiste mappen van de Box-accounts te plaatsen. Learning Manager haalt de CSV-bestanden op, voegt ze samen en importeert de gegevens volgens de planning. Raadpleeg de planningsfunctie voor meer informatie.

**Kenmerken toewijzen**

Kenmerken toewijzen Deze toewijzing is een eenmalige inspanning. Zodra de toewijzing is voltooid, wordt dezelfde toewijzing gebruikt voor de daaropvolgende gebruikersimporten. De toewijzing kan opnieuw worden geconfigureerd als de beheerder een andere toewijzing voor het importeren van gebruikers wil hebben.

## Gegevensexport {#data-export}

De gegevensexport stelt gebruikers in staat om de vaardigheden van de gebruiker en de studenttranscripten te exporteren naar een Box-locatie om deze te integreren met een willekeurig extern systeem.

## Rapporten plannen {#schedule-reports}

De beheerder kan planningstaken volgens de vereisten van de organisatie instellen en gebruikers in de Learning Manager-toepassing zijn up-to-date volgens de planning. Op dezelfde manier kan de integratiebeheerder de export van vaardigheden op een tijdige basis plannen om deze te integreren met een extern systeem. De synchronisatie kan dagelijks worden uitgevoerd in de Learning Manager-toepassing.

## Box-connector configureren {#boxconnector}

U kunt de Box-connector integreren met Learning Manager door het proces te leren kennen.

1. Beweeg de muis over de Box-kaart/miniatuur op de startpagina van Learning Manager. Er verschijnt een menu. Klik op Verbinden in het menu.

   ![](assets/screen-shot-2017-10-25at54426pm.png)

   *verbind met Doos*

1. Er verschijnt een dialoogvenster waarin u wordt gevraagd de e-mail-ID in te voeren. Geef de e-mail-ID op van de persoon die verantwoordelijk is voor het beheer van het Box-account voor de organisatie. Klik op Verbinden nadat u de e-mail-ID hebt opgegeven.
1. Learning Manager stuurt u een e-mail waarin de gebruiker wordt gevraagd het wachtwoord opnieuw in te stellen voordat hij/zij voor het eerst toegang krijgt tot de Box. De gebruiker moet het wachtwoord opnieuw instellen en dit gebruiken voor toegang tot het Box-account van de Learning Manager.

   >[!NOTE]
   >
   >Er kan slechts één Learning Manager Box-account worden gemaakt voor een bepaald Learning Manager-account.

   Op de overzichtspagina kunt u de verbindingsnaam voor uw integratie opgeven. Kies uit de volgende opties welke actie u wilt uitvoeren:

   * Interne gebruikers importeren
   * xAPI-activiteitsrapporten importeren
   * Vaardigheden van gebruikers exporteren - Een planning configureren
   * Vaardigheden van gebruikers exporteren - Op verzoek
   * Studenttranscript exporteren - Een planning configureren
   * Studenttranscript exporteren - Op verzoek

## Importeren {#import-7}

+++Interne gebruiker

Met de optie voor het importeren van interne gebruikers kunt u het genereren van een gebruikersimportverslag automatisch plannen. De gegenereerde rapporten worden als .CSV-bestanden naar u verzonden.

+++

+++Kenmerken Kaart

Zodra een verbinding tot stand is gebracht, kunt u de kolommen van CSV-bestanden die in de Box-map zijn geplaatst, toewijzen aan de overeenkomstige kenmerken van Leerbeheer. Deze stap is verplicht.

1. Op de pagina Kenmerken toewijzen, links   aan de zijkant ziet u de verwachte kolommen van de leermanager en aan de rechterkant   u kunt de CSV-kolomnamen zien. In eerste instantie ziet u aan de rechterkant een leeg selectievakje. Importeer een CSV-sjabloon door op Bestand kiezen te klikken.
1. Via de bovenstaande stap worden alle CSV-kolomnamen aan de rechterkant van de vervolgkeuzelijst ingevuld. Selecteer de juiste kolomnaam die is toegewezen aan de kolomnaam van de leermanager.

   *het gebied van de Manager moet aan een gebied van het type e-mailadres worden in kaart gebracht. U moet alle kolommen toewijzen voor u de connector kunt gebruiken.*

1. Klik op Opslaan nadat u de toewijzing hebt voltooid.

   De connector is nu klaar voor gebruik. Het geconfigureerde account verschijnt als gegevensbron in de beheerdersapp zodat de beheerder de import of de synchronisatie op verzoek kan plannen.

+++

+++xAPI-activiteitsrapport

Met de optie xAPI-activiteitsrapport kunt u de import van xAPI-statements uit externe diensten genereren. De bestanden worden als CSV-bestanden opgeslagen en vervolgens geconverteerd naar xAPI-statements tijdens het importeren in Learning Manager.

+++

+++Vereiste configuraties voor het importeren van xAPI

1. Selecteer op de configuratiepagina een bestaande configuratie die beschikbaar is in de configuratielijst om xAPI-statements uit de CSV te importeren. Klik geef uit of A **voeg een nieuwe verbinding van de Configuratie** toe om aan de de verklaring-Configuratie-Bron van het Dossier van de Invoer xAPI te navigeren.

   ![](assets/artboard-11-2x.png)

   *geef of voeg een nieuwe configuratie* uit toe

   **Configuratie**

   * Vul de velden Naam en Naam van bronbestand op de pagina configureren-importeren-bronnen in. De naam van het bronbestand moet overeenkomen met de bestandsnaam die is in de FTP-maplocatie opgegeven.
   * Klik op **[!UICONTROL Opslaan]** om uw wijzigingen op te slaan.

   ![](assets/configurations-main2x.png)

   *vorm*

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
   *de verklaringen van de Invoer xAPI - vorm Programma*

1. Van de linkerruit, klik **[!UICONTROL op Vereiste Uitvoering]**.

   ![](assets/box-on-demand-2x.png)
   *de verklaringen van de Invoer xAPI - op bestelling*

1. Klik in het linkerdeelvenster op **[!UICONTROL Uitvoeringsstatus]** om het overzicht van alle runs voor deze connector in chronologische volgorde weer te geven. U kunt de begindatum en de duur van de xAPI-import, het type import (op verzoek of volgens een planning) en de status van de import (of de xAPI-import in voortgang is, of voltooid of mislukt is) bekijken.

   ![](assets/box-execution-status2x.png)
   *de verklaringen van de Invoer xAPI - de Status van de Uitvoering*

+++

+++Interface van de Learning Manager Box-connector

1. De CSV-bestanden van externe systemen moeten op het volgende pad worden geplaatst:

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   >[!NOTE]
   >
   >In de release van juli 2016 is alleen import van gebruikers toegestaan. Zorg er daarom voor dat de CSV-bestanden in de volgende map worden geplaatst om de Box-connector te gebruiken:

   `code Home/import/user/internal/*.csv`

1. De Box-connector haalt alle rijen uit CSV-bestanden. Het is belangrijk dat de rij die overeenkomt met een gebruiker in een CSV niet in andere CSV&#39;s verschijnt.
1. Alle CSV&#39;s moeten de kolommen bevatten die in de toewijzing zijn opgegeven.
1. Alle vereiste CSV&#39;s moeten aanwezig zijn in de map voordat het proces begint.

Bij het importeren van gebruikers in Learning Manager, moet de beheerder ook weten hoe gebruikers in Learning Manager beheerd worden. Verwijs naar [ Hulp van het Beheer van de Gebruiker ](migration-manual.md#usermanagement) om meer informatie te kennen.

+++

## Badge als {#export-2}

+++Vaardigheden

Er zijn twee opties om vaardigheidsrapporten van de gebruiker te exporteren.

Gebruikersvaardigheden - Op verzoek: u kunt via deze optie de startdatum specificeren en het rapport exporteren. Het rapport wordt geëxtraheerd vanaf de ingevoerde datum tot heden

**[!UICONTROL Gebruikersvaardigheden - Configureren]**: via deze optie kunt u de extractie van het rapport plannen. Selecteer het selectievakje Planning inschakelen en geef de begindatum en -tijd op. U kunt ook aangeven met welke intervallen u het rapport wilt laten genereren en verzenden.

+++

Als u de Exportmap wilt openen waar de geëxporteerde bestanden op uw Box-locatie worden geplaatst, opent u de koppeling naar Box-map op de pagina Gebruikersvaardigheden, zoals hieronder weergegeven.

De auto-uitgevoerde dossiers zijn aanwezig in de plaats **Home/export/&#42; Box_location&#42;**

De auto-uitgevoerde dossiers zijn beschikbaar met de titel, **skill_results_ &#42; datum van &#42;_aan_&#42; datum aan &#42; .csv**

>[!NOTE]
>
>De klant beheert de toegangsrechten en de inhoud in de Box-map die door het team van Leermanager wordt gedeeld.  Ook de inhoud in de map wordt fysiek opgeslagen in de regio Frankfurt.

### Ondersteuning voor handmatige csv-velden {#support-for-manual-csv-fields-1}

Bij het importeren van gebruikersgegevens via Box moet een beheerder alle actieve velden in het systeem toewijzen aan het juiste veld in de csv.

Dit is verplicht voor alle actieve csv-velden. Voor handmatig geactiveerde velden kan de integratiebeheerder de optie **DontImportFromSource** selecteren.

Door deze optie te selecteren worden de waarden van handmatig geactiveerde velden niet overschreven bij de csv-import. De door de student ingevulde waarden blijven intact.

>[!NOTE]
>
>Terwijl het in kaart brengen, als de optie **DontImportFromSource** voor csv actief gebied wordt geselecteerd, dan zal dit gebied van het systeem worden geschrapt.

![](assets/box-connector-foractivefields.png)
*de schakelaar van de Doos voor Actieve gebieden*

>[!NOTE]
>
>Elke connector of migratie, die gebruik maakt van FTP/Box als gegevensbron, zal alle csv-bestanden die worden verwerkt, verwijderen.
>
>Het csv-bestand voor de inhoudconnectoren, bijvoorbeeld LinkedIn, zal na zeven dagen worden verwijderd, terwijl het csv-bestand voor het importeren van gebruikers onmiddellijk zal worden verwijderd.

## LinkedIn Learning-connector {#linkedinlearningconnector}

De LinkedIn Learning-connector wordt gebruikt door zakelijke klanten van LinkedIn.com die graag willen dat hun studenten cursussen kunnen zoeken en volgen in Learning Manager. De connector kan worden geconfigureerd om periodiek cursussen op te halen met uw API-sleutel. Zodra een cursus binnen Learning Manager is gemaakt, kunnen gebruikers deze opzoeken en volgen. De voortgang van de student kan vervolgens binnen Learning Manager worden bijgehouden.

>[!NOTE]
>
>U krijgt de unieke LO-id&#39;s voor alle cursussen die zijn geïmporteerd van de LinkedIn Learning-connector naar Adobe Learning Manager.

>[!NOTE]
>
>De tijd die wordt besteed aan cursussen van LinkedIn Learning wordt via het LinkedIn Content/LinkedIn-platform doorgegeven aan het Learning Manager-studieplatform. Als LinkedIn Learning de studietijd niet doorstuurt, kan deze tijd niet door ons studieplatform worden geregistreerd. In dat geval is de leertijd die door de leermanager wordt weergegeven nul.

### Instellingen configureren in Linkedln Learning-portaal {#configure-settings-in-linkedln-learning-portal}

1. Meld u als beheerder aan bij Linkedln Learning LMS.
1. Klik **[!UICONTROL admin]** van het hoogste navigatievenster.
1. Klik op het tabblad **[!UICONTROL Instellingen]** in het volgende venster.
1. Selecteer **[!UICONTROL Integratie van de Playback]** van het linkernavigatiepaneel en klik dan de **Integratie** tabel.
1. Klik **[!UICONTROL Montages van de Lancering van de Inhoud LMS]** om zijn montages uit te breiden.
1. Voeg de volgende drie hostnamen toe: **learningmanager.adobe.com**, **learningmanagerlrs.adobe.com**, **cpcontents.adobe.com**
1. Selecteer **[!UICONTROL AICC-integratie inschakelen]**.

   ![](assets/linkedin-learning.png)

   *LinkedIn het Leren configuratie*

### LinkedIn Learning-connector configureren {#configure-linkedin-learning-connector}

1. Van het dashboard van de Admin van de Integratie, klik [!UICONTROL  het Leren van LinkedIn ]. De opties Aan de slag, Verbinden en Verbindingen beheren worden weergegeven.
1. Als u de het Leren van LinkedIn schakelaar voor het eerst vormt, klik [!UICONTROL  verbind ].

   <!--Configure the Exavault FTP account before you configure this connector.

   ![](assets/configure.jpg)
   *Configure connection*-->

1. Geef op de verbindingspagina een naam op voor uw connector. Voer de appsleutel en de geheime sleutel voor uw verbinding in.

   >[!NOTE]
   >
   >De bedrijfsbeheerder kan een nieuwe toepassing genereren via de LinkedIn Learning Admin-portal om de appkey en de geheime sleutel op te halen.

1. Klik op **[!UICONTROL Opslaan]**.

   De configuratie wordt opgeslagen en de LinkedIn Learning-verbinding voor uw account wordt toegevoegd. U kunt **[!UICONTROL nu klikken beheert Verbindingen]** van de homepage, en uw configuratie op om het even welk ogenblik uitgeven.

1. Als u reeds een vastgestelde verbinding hebt, klik **[!UICONTROL leidt Verbindingen]** mening al uw verbindingen.

   >[!NOTE]
   >
   >De migratiefunctie moet zijn ingeschakeld voor uw account voordat u deze connector kunt configureren.

1. Klik op de verbinding die u wilt bewerken.
1. Klik in het linkerdeelvenster op Configureren. Voer een van de volgende handelingen uit:

   * Bekijk of bewerk de details van uw account en het synchronisatieschema vanuit dit venster. Selecteer **[!UICONTROL toelaten de controledoos van de Verbinding]** als u deze rekening wilt toelaten.
   * Klik **[!UICONTROL geef]** uit en geef uw geloofsbrieven uit. Klik op Herstellen om uw updates voor dit veld ongedaan te maken.
   * Klik **[!UICONTROL laat Programma]** toe om uw synchronisatie te plannen. U kunt de starttijd en -datum invoeren en vervolgens de frequentie van uw synchronisatieplanning in dagen invoeren. Bijvoorbeeld, om de drie dagen synchroniseren.

   Klik op **[!UICONTROL Opslaan]** om uw wijzigingen op te slaan.

1. Van de linkerruit, klik **[!UICONTROL Uitvoering op bestelling]**. Met deze optie kunt u gebruikersfeeds en andere relevante gegevens vanuit LinkedIn importeren. Voer de startdatum in voor de uitvoering op verzoek en klik op Uitvoeren om de synchronisatie uit te voeren. Alle gegevens vanaf de startdatum tot heden worden geïmporteerd.

   * U kunt **[!UICONTROL klikken onbruikbaar maakt toegang]** aan het Leren Manager tijdens uitvoering waar de toepassing onderbreking tijdens de synchronisatie heeft.
   * Als u **[!UICONTROL klikt laat toegang]** aan het Leren Manager tijdens uitvoering toe, is er geen verstoring in de dienst tijdens synchronisatie.

   ![](assets/ondemandexecution.jpg)

   *Op vraaguitvoering van rapport*

1. U kunt ook op elk moment op Uitvoeringsstatus in het linkerdeelvenster klikken om het overzicht van alle runs voor deze connector in chronologische volgorde te bekijken. U kunt de startdatum en duur van de synchronisatie, het type synchronisatie (of het al dan niet gaat om synchronisatie op verzoek) en de status van de synchronisatie (of de synchronisatie wordt uitgevoerd of is voltooid) bekijken.

   ![](assets/executionstatus.jpg)

   *de uitvoeringsstatus van het Rapport*

   >[!NOTE]
   >
   >Wanneer u een verbinding wist en opnieuw aanmaakt, worden de vorige runs voor de connector weergegeven. U kunt alle runs bekijken voordat u de verbinding wist.

   U kunt alleen de laatste synchronisatie opnieuw uitvoeren.

### LinkedIn Learning-content filteren {#filter-linkedin}

Er zijn filters in LinkedIn-connectoren om inhoud te scheiden op basis van LinkedIn Learning-bibliotheken. Daarnaast kunt u ook inhoud filteren op basis van taal en bibliotheek en alleen de cursussen in de gewenste talen importeren. Wanneer de inhoud is geïmporteerd, wordt deze op basis van de importconfiguratie gescheiden in meerdere catalogi.

Dit zijn de filters:

**Gebruik van filtertraining:** filtert een subgroep van cursussen uit LinkedIn naar Learning Manager.

* **Gebaseerd op taal**

![](assets/filter-language.png)

*Filter door taal*

* **Gebaseerd op Bibliotheek van het Leren van LinkedIn**

![](assets/filter-catalog.png)

*Filter door catalogus*

**Trainingen importeren naar**

![](assets/iport-training.png)
*de opleiding van de Invoer aan catalogi*

**Importtags**

Er is een type tag, **aangepaste tag**, die u kunt gebruiken om aangepaste tags toe te voegen aan uw LinkedIn Learning-cursussen. U kunt zoveel tags toevoegen als u wilt, van elkaar gescheiden door komma&#39;s.

![](assets/add-custom-tags.png)

*voeg douanetags toe*

De inhoud wordt pas na de migratie opgeslagen. De inhoud wordt in respectieve catalogi opgeslagen.

## Power BI-connector {#powerbiconnector}

>[!NOTE]
>
>Learning Manager ondersteunt alleen integratie met commerciële licenties van Microsoft Power BI. Het integreert niet met Microsoft Power BI in Government Cloud.

U kunt integratie met deze connector gebruiken om uw bestaande Power BI-accounts te benutten voor het analyseren en visualiseren van leergegevens uit Learning Manager binnen Power BI. Tijdens de configuratie kan de integratiebeheerder zijn Power BI-werkruimte zo instellen dat deze stapsgewijs wordt gevuld met twee live-datasets - studenttranscript en rapporten over gebruikersvaardigheden. U kunt vervolgens alle functies en mogelijkheden van Power BI gebruiken om aangepaste dashboards te ontwikkelen, implementeren en distribueren naar wens van de organisatie.

### De connector configureren {#configuring-the-connector}

Om de schakelaar, in de **[!UICONTROL pagina van Connectoren]** te vormen, beweeg over de **[!UICONTROL Power BI]** tegel en klik **[!UICONTROL verbind]**. De Power BI-pagina wordt geopend. Verstrek de client-ID en het clientgeheim van de app, de naam van de tenant en de werkruimte-ID (optioneel) om een verbinding tot stand te brengen. Volg deze stappen om deze gegevens te verkrijgen.

![](assets/power-bi-configurepage.png)

*vorm de Power BI schakelaar*

1. Start <https://app.powerbi.com/embedsetup> .
1. Klik **[!UICONTROL bed voor uw organisatie]** in en teken binnen aan uw rekening van Microsoft.
1. Voer de naam van de app in.
1. Selecteer in de sectie App-type de optie Server-side web-app.
1. In de **[!UICONTROL Redirect URL]** sectie, selecteer de optie **Gebruik een douane URL** (kies dit als u URL van de doeltoepassing kent). Voer de volgende URL in:

   `https://learningmanager.adobe.com/ctr/app/azure/_callback` (werk het domein bij op basis van de omgeving)

1. Voer in het veld Home-URL de volgende URL in: `https://learningmanager.adobe.com/`
1. In de toestemmingssectie, lees **Alle gegevensreeks** en **leest en schrijf alle gegevensreeks**.

   De tenant verkrijgen: neem contact op met uw Power BI-beheerder om de naam van de tenant op te geven.

   Werkplek-ID verkrijgen: een werkplek maken is alleen mogelijk voor Power BI Pro-gebruikers. U kunt een werkplek maken in Power BI en de ID uit de URL halen.

1. Klik **[!UICONTROL app van het Register]** en bewaar identiteitskaart van de Cliënt en Geheime tijd van de Cliënt.

>[!NOTE]
>
>Als u de verbinding opnieuw wilt autoriseren, moet u nog een Power App maken en de omleidings-URL voor herbranding opgeven.

U kunt Studenttranscripten, Gebruikersvaardigheden en xAPI-activiteitsrapport op dezelfde manier exporteren. Kies in het linkerpaneel voor Studenttranscripten/Gebruikersvaardigheden. De pagina Exporteren wordt geopend.

Schakel het selectievakje **[!UICONTROL Gebruikersvaardigheid/Studenttranscript-export inschakelen in via deze verbinding]** in. Wijzigingen opslaan.

**Export configureren**: als u de extractie van het rapport wilt plannen. Selecteer **[!UICONTROL laat de controledoos van het Programma]** toe en specificeer de begindatum en tijd. U kunt ook aangeven met welke intervallen u het rapport wilt laten genereren en verzenden.

![](assets/power-bi-configureuserskillpage.png)

*de Uitvoer vormt om het rapport te plannen*

**Uitvoer op bestelling:** u kunt de begindatum specificeren en het rapport uitvoeren gebruikend de optie. Het rapport wordt geëxtraheerd vanaf de ingevoerde datum tot heden.

![](assets/power-bi-userskillondemandpage.png)

*Uitvoer op bestelling*

De geëxporteerde gegevens kunnen worden bekeken door u aan te melden bij uw Power BI-account. De geëxporteerde gegevens staan vermeld onder de optie gegevenssets.

### xAPI Activiteitsrapporten exporteren in Learning Manager {#export-xapi-activity-reports-in-captivate-prime}

Van de PowerBI-xAPI capaciteitspagina, klik **[!UICONTROL het Rapport van de xAPI van de Uitvoer]**.

![](assets/powerbi-dashboard.png)
*PowerBI - het Rapport van de Activiteit van de Uitvoer xAPI*

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
*xAPI de Uitvoer vormt Plan*

**Op verzoek**

Klik in het linkerdeelvenster op **[!UICONTROL Op verzoek]** en geef de begindatum op de pagina xAPi-statements exporteren-Op verzoek.

![](assets/on-demand-2.png)
*xAPI de Uitvoer op bestelling*

Alle geëxporteerde gegevens gaan naar een dataset die door Adobe in uw Power BI-account wordt gemaakt.

xAPI-export naar Power BI mislukt als enkele van de xAPI-statements in LRS geen JSON-pad hebben dat voor export is geconfigureerd. Voor de xAPI-statements waar het JSON-pad niet beschikbaar is, moet de constante waarde N/A worden toegevoegd en weergegeven in Power BI.

**Uitvoeringsstatus**

Selecteer **Uitvoeringsstatus** om een overzicht van alle taken in chronologische volgorde weer te geven. Het waarschuwingsteken geeft aan wat er tijdens de run fout is gegaan. U kunt foutenrapporten als **CSV** downloaden door op de verbinding van het foutenrapport te klikken.

![](assets/execution-status.png)
*xAPI de Status van de Uitvoering*

### Gecombineerde rapporten {#unified-reports}

Leermanager biedt een manier om export te maken met een combinatie van rapporten zoals gebruikersgegevens, studenttranscript, gamification, feedbackrapporten en meer, als één dataset naar Power BI.

Hierdoor kunnen Power BI-gebruikers de gegevens uit meerdere rapporten samenvoegen om veel krachtige analyses en visualisaties in Power BI te presenteren.

![](assets/unified-power-bireports.png)
*Verenigde rapporten van de Power BI*

**Export op verzoek**

Geef de begindatum en einddatum op en exporteer het rapport met de optie. Het rapport wordt voor het opgegeven datumbereik geëxtraheerd.

![](assets/on-demand-export.png)
*Op bestelling de uitvoer*

**Geplande export**

Als u de extractie van het rapport wilt plannen. Selecteer het selectievakje **Planning inschakelen** en geef de begindatum en -tijd op. U kunt ook aangeven met welke intervallen u het rapport wilt laten genereren en verzenden.

![](assets/configure-schedule.png)
*vorm programma*

U kunt trainingsrapporten ook exporteren naar Power BI.

Trainingsrapporten kunnen worden geëxporteerd naar Power BI als onderdeel van de functie Gecombineerde rapporten.

Het trainingsrapport heeft twee extra velden:

* Aantal gebruikers dat feedback op een cursus heeft gedeeld
* Gemiddelde waardering met sterren voor een cursus

### Filterstatus van studenttranscripten {#lt-status}

In het gedeelte Gecombineerde rapporten van een Power BI-connectie is er een optie om studenttranscripten te exporteren op basis van de status van de leerobjecten.

* **Alles selecteren:** exporteer alle bestanden of activiteiten op moduleniveau in het opgegeven datumbereik.
* **Voltooid:** exporteer alle bestanden die voltooid zijn in het datumbereik.
* **Bezig:** voer alle verslagen uit die status - in bewerking hebben.
* **niet begonnen:** sluit de verslagen uit die in de bepaalde datumwaaier worden ingeschreven, maar niet begonnen wanneer het produceren van het rapport.

* **Niet ingeschreven:** voeg alle bestanden bij die niet zijn ingeschreven in het datumbereik.

![](assets/lt-filters.png)
*status van de Filter van het Leren Transcripten*

U kunt de gewenste lijst exporteren en Power BI gebruiken om het rapport later te analyseren.

### Power BI-sjablonen downloaden {#template}

Learning Manager biedt ook kant-en-klare sjablonen voor Power BI. Deze sjablonen bieden betere analysemogelijkheden voor Adobe Learning Manager-accountbeheerders.

U kunt de sjablonen eenvoudig downloaden, relevante rapporten exporteren en rapporten met een plotbestand samenstellen met behulp van deze beschikbare sjablonen.

![](assets/download-power-bi-template.png)
*Power BI van de Download malplaatjes*

Zo kunnen gebruikers deze sjablonen downloaden en gebruiken in een Power BI-toepassing, deze verder aanpassen en een boeiend verhaal vertellen in uw rapporten.

[**Download de malplaatjes** ](https://documentcloud.adobe.com/link/track?uri=urn:aaid:scds:US:842bb6a2-cd7d-4c3d-b968-da38bc1cc18a)

<!--<table> 
 <tbody>
  <tr> 
   <td><img src="assets/download.png"></td> 
   <td><p> </p> <p><a disablelinktracking="false" href="https://documentcloud.adobe.com/link/track?uri=urn:aaid:scds:US:842bb6a2-cd7d-4c3d-b968-da38bc1cc18a"><strong><em>Download the templates</em></strong></a></p></td> 
  </tr> 
 </tbody>
</table>-->

U kunt de sjablonen ook handmatig downloaden via de bovenstaande link. Gebruik de sjablonen en pas uw rapporten aan de hand daarvan aan.

### Trainingsrapport exporteren {#export-training-report}

De trainingsrapporten kunnen worden geëxporteerd naar Power BI als onderdeel van de functie Gecombineerde rapporten.

Het trainingsrapport heeft deze extra velden:

* Aantal gebruikers dat feedback op een cursus heeft gedeeld
* Gemiddelde waardering met sterren voor een cursus

![](assets/export-training-report.png)
*het trainingsrapport van de Uitvoer*

### Wijzigingen met betrekking tot leerpad {#learning-path-related-changes}

#### Beheerder: transcripten leren en geïntegreerd rapport {#learning-transcripts-and-unified-reports}

**Bestaande verbindingen**

Als de optie Leerpad is uitgeschakeld in het beheerdersaccount, worden er geen rijen en kolommen toegevoegd aan de rapporten.

Als de optie Leerpad is ingeschakeld in het beheerdersaccount, bevat het rapport het kolomtype Leerpad (hoger niveau) voor alle studenten die zijn ingeschreven voor een leerpad.

**Nieuwe verbindingen**

Als de optie Leerpad is uitgeschakeld in het beheerdersaccount, bestaat het trainingsrapport uit de volgende kolommen:

* Ingesloten pad: geeft de naam van het leerprogramma weer.
* Ingesloten pad-ID: geeft de ID&#39;s voor het leerprogramma weer.
* Ingesloten cursus-ID: geeft de ID&#39;s van de cursussen in een leerpad weer.

Bovendien bevat het rapport het kolomtype Leerpad (hoger niveau) voor alle studenten die in een leerpad zijn ingeschreven.

In de kolom Type wordt de naam leerprogramma gewijzigd naar leerpad. Bestaande verbindingen wijzigen niet. Voor nieuwe verbindingen worden de wijzigingen echter na 30 dagen doorgevoerd.

#### Trainingsrapport: Uniform rapport {#training-report}

**Bestaande verbindingen**

Als de optie Leerpad is uitgeschakeld in het beheerdersaccount, worden er geen rijen en kolommen toegevoegd aan de rapporten.

Als de optie Leerpad is ingeschakeld in het beheerdersaccount, bevat het rapport de kolom &quot;Type&quot;. De kolom bevat de nieuwe waarde &quot;Leerpad (hoger niveau), indien van toepassing&quot;.

**Nieuwe verbindingen**

Als de optie Leerpad is uitgeschakeld in het beheerdersaccount, bestaat het trainingsrapport uit de volgende kolommen:

* **Ingesloten pad:** geeft de naam van het leerprogramma weer.
* **Ingesloten pad-ID:** geeft de ID&#39;s voor het leerprogramma weer.
* **Ingebedde identiteitskaart van de Cursus:** toont IDs van cursussen die binnen een Leerweg zijn.

Bovendien bevat het rapport het kolomtype Leerpad (hoger niveau) voor alle studenten die in een leerpad zijn ingeschreven.

In de kolom Type wordt de naam leerprogramma gewijzigd naar leerpad. Bestaande verbindingen wijzigen niet. Voor nieuwe verbindingen worden de wijzigingen echter na 30 dagen doorgevoerd.

## Aangepaste FTP {#custom-ftp}

**Voorwaarden**

>[!NOTE]
>
>Als u uw aangepaste FTP wilt installeren, neemt u contact op met uw CSM. De CSM zal de vereiste details van het opzetten van de FTP verstrekken.
>
>Bij het instellen van de FTP is een doorlooptijd vereist. IT-ondersteuning is vereist voor de lijst met IP&#39;s en poorten en voor het maken van bepaalde mappen met specifieke machtigingen op uw FTP-server.

Learning Manager biedt de mogelijkheid om verbinding te maken met uw aangepaste FTP-locatie.

Uw FTP zal deze ondersteunen:

### Gegevensimport {#data-import-2}

Met het gebruikersimportproces kan de Learning Manager Administrator werknemersgegevens ophalen van de FTP-service van Learning Manager en ze automatisch in Learning Manager importeren. Met behulp van deze functie kunt u meerdere systemen integreren door de door deze systemen gegenereerde CSV in de juiste mappen van de FTP-accounts te plaatsen. Learning Manager haalt de CSV-bestanden op, voegt ze samen en importeert de gegevens volgens de planning. Raadpleeg de planningsfunctie voor meer informatie.

**Kenmerken toewijzen**

Kenmerken toewijzen Deze toewijzing is een eenmalige inspanning. Zodra de toewijzing is voltooid, wordt dezelfde toewijzing gebruikt voor de daaropvolgende gebruikersimporten. De toewijzing kan opnieuw worden geconfigureerd als de beheerder een andere toewijzing voor het importeren van gebruikers wil hebben.

### Gegevensexport {#data-export-3}

Met de gegevensexport kunnen gebruikers gebruikersvaardigheden en studenttranscripten exporteren naar de FTP-locatie om deze te integreren met elk systeem van een derde partij.

### Rapporten plannen {#schedule-reports-2}

De beheerder kan planningstaken volgens de vereisten van de organisatie instellen en gebruikers in de Learning Manager-toepassing zijn up-to-date volgens de planning. Op dezelfde manier kan de integratiebeheerder de export van vaardigheden op een tijdige basis plannen om deze te integreren met een extern systeem. De synchronisatie kan dagelijks worden uitgevoerd in de Learning Manager-toepassing.

Om uw eigen FTP te vormen, teken binnen als Admin van de Integratie, en klik **[!UICONTROL Douane FTP]** > **[!UICONTROL verbind]**.

Er zijn twee soorten verificaties:

![](assets/custom-ftp-authenticationoptions.png)
*de authentificatieopties van FTP van de Douane*

* **Basis:** in basisauthentificatie, zult u slechts de het domeinURL van FTP, gebruikersbenaming, en wachtwoord moeten verstrekken. Klik op Verbinden nadat u de details hebt opgegeven.
* **Certificatie:** als de klant FTP certificaatauthentificatie steunt dan kunnen zij deze optie kiezen. Nadat u op SSH-sleutel genereren hebt geklikt, wordt de SSH-toets gedownload naar uw lokale computer. Als u het bestand opent, ziet de toets er als volgt uit:

![](assets/ssh-public-key.png)
*SSH openbare sleutel*

U moet deze openbare sleutel in uw FTP-server plaatsen voordat u de onderstaande details toevoegt. Zodra u de bepaalde sleutel als openbare sleutel van uw FTP plaatst, verstrek het het domeinurl van FTP en de gebruikersbenaming en klik op **verbind** knoop om de verbinding te opstelling.

Als de verbinding eenmaal is ingesteld, worden automatisch mappen voor importeren en exporteren gemaakt op de FTP-locatie. Nadat de import-/exportfunctionaliteit is geleverd door Aangepaste FTP.

>[!NOTE]
>
>Een aangepaste FTP-connector kan alleen met SFTP-servers worden geconfigureerd.

## ADFS-aansluiting {#adfsconnector}

Voorwaarden om een ADFS-verbinding tot stand te brengen:

* Login aan uw Azure Portal gebruikend dit URL: [ https://portal.azure.com/ ](https://portal.azure.com/) alvorens uw app te registreren.
* Azure Active Directory openen.

## Stappen om uw toepassing te registreren {#steps-to-register-your-application}

* Klik op Azure Active Directory. Klik **[!UICONTROL toevoegen]** > **[!UICONTROL registratie van de App]**.

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

  *voeg toestemmingen* toe

* Selecteer **Microsoft Graph**.

  <!--![](assets/ms-graph.png)-->

  <!--*Select Microsoft Graph*-->

* Selecteer **Toepassingstoestemmingen**.

  ![](assets/request-api-permission.png)

  *Uitgezochte toestemmingen van de Toepassing*

* Zoek naar de *directory* en selecteer **Directorygegevens lezen**.

  ![](assets/read-directory-data.png)

  *Uitgezochte Lezen foldergegevens*

* Voer *gebruiker* in als de zoekterm.

  ![](assets/search-user.png)

  *ga de onderzoekstermijn* in

* Selecteer **De volledige profielen van alle gebruikers lezen**.

  ![](assets/select-read-all.png)

  *Uitgezocht lees de volledige profielen van alle gebruikers*

* Selecteer **Machtigingen toevoegen**.

  <!--![](assets/select-add-permission.png)-->

  <!-- *Select Add Permissions*-->

### ADFS-configuratiepagina {#adfs-configuration-page}

1. Voer op de ADFS-configuratiepagina in Adobe Learning Manager de client-id en het eerder verkregen client-geheim in.

   Klik op **[!UICONTROL Verbinden]**.

1. Login aan **portal.azure.com**. De waarden worden ingevuld in de velden Tenant-id en Primair domein.

### Importeren {#import-8}

#### Kenmerken toewijzen {#map-attributes-6}

De integratiebeheerder kan ADFS-kenmerken kiezen en deze toewijzen aan de groepeerbare kenmerken van de overeenkomstige Learning Manager. Wanneer de toewijzing is voltooid, wordt dezelfde toewijzing voor verdere gebruikersimporten gebruikt. Het kan opnieuw worden geconfigureerd als de beheerder een andere toewijzing voor het importeren van gebruikers wil hebben.

#### Geautomatiseerde gebruikersimport {#automated-user-import-4}

Via het proces voor gebruikersimport kan de beheerder van de leermanager werknemersgegevens ophalen uit ADFS en deze automatisch importeren in Learning Manager.

#### Gebruikers filteren {#filtering-users-4}

De beheerder van de leermanager kan filteren op de gebruikers toepassen voordat deze worden geïmporteerd. Zo kan de Learning Manager-beheerder er bijvoorbeeld voor kiezen om alle gebruikers in de hiërarchie onder één of meer specifieke managers te importeren.

Neem contact op met het CSM-team van Learning Manager om de ADFS-connector in te stellen.

## De ADFS-connector configureren {#configure-adfs-connector}

1. Beweeg de muis over de ADFS-kaart/miniatuur op de startpagina van Learning Manager. Er verschijnt een menu. Klik op de optie Verbinden in het menu.

   ![](assets/adfs1.jpg)

   *ADFS duimnagel*

1. Klik op Verbinden om een nieuwe verbinding tot stand te brengen. De ADFS-connector-pagina wordt weergegeven. Vul de gegevens in van het account dat u wenst toe te wijzen.

   ![](assets/adfs2.jpg)

   *Vestig verbinding*

1. Als u de ADFS-gebruiker rechtstreeks als interne gebruiker van de Learning Manager wilt importeren, gebruikt u de optie Interne gebruikers importeren.

   ![](assets/adfs3.jpg)

   *de Gebruiker van de Invoer aan Leermanager*

1. In de toewijzingspagina, links   ziet u de kolommen van de leermanager en rechts   zie de ADFS-kolommen. Selecteer de juiste kolomnaam die is toegewezen aan de kolomnaam van de leermanager.

   ![](assets/adfs4.jpg)

   *Kenmerken toewijzen*

1. Om gegevensbron, als Beheerder te bekijken en uit te geven, klik **[!UICONTROL Montages]** > **[!UICONTROL Gegevensbron]**.

   De bestaande ADFS-bron wordt vermeld. Als u vereist om de filter uit te geven, geeft de klik **** uit.

   ![](assets/datasource.jpg)
   *Bron van Gegevens het plaatsen*

1. U ontvangt een melding na voltooiing van de import. Om het de invoerlogboek te bekijken of uit te geven, klik **[!UICONTROL Gebruikers]** > **[!UICONTROL logboek van de Invoer]**.

### Een verbinding verwijderen {#delete-a-connection-1}

Voer de volgende stappen uit om een gevestigde miniOrange-verbinding te verwijderen.

## Adobe Connect {#connect}

1. Klik in Adobe Connect op de drie puntjes op de kaart en kies **Verbinden**.
1. Klik **vormen nu** verbinding in de sectie van de Configuratie van Adobe Connect.
1. Geef de Adobe Connect-domeinnaam van uw bedrijf en meld u aan met uw bedrijfsgegevens.

   Een voorbeeld van een Adobe Connect-URL: ***mycompany.adobeconnect.com***

   U moet de e-mail-ID van de Adobe Connect-accountbeheerder opgeven.

   >[!NOTE]
   >
   >Alleen door Adobe gehoste accounts worden ondersteund in Learning Manager. Voorbeeld; &#39;.adobeconnect.com&#39;.

1. Klik **[!UICONTROL integreren]**.

   Nadat de e-mail-ID is geverifieerd, geeft Learning Manager het bericht weer als Connect is geïntegreerd. U kunt uw virtuele klassikale cursussen automatisch bekijken met behulp van Adobe Connect.

   **Nadat het Connect-accountbeheer zijn/haar email-ID heeft geverifieerd, wordt het verzoek ter goedkeuring voorgelegd aan het Adobe Connect back-end team. Het duurt doorgaans een dag of twee voordat de integratie is goedgekeurd en ingesteld.**

   >[!NOTE]
   >
   >De Adobe Connect-accountbeheerder moet de algemene gebruiksvoorwaarden van Adobe Connect accepteren. Als deze niet worden geaccepteerd, mislukt uw aanmeldpoging mogelijk. Meld u na het aanmaken van het Adobe Connect-account eenmaal aan op het account. Bij de eerste aanmeldpoging verschijnt er een pagina met de Algemene voorwaarden.

### Sessie-informatie voor virtueel klaslokaal toevoegen {#add-virtual-classroom-session-information}

Als de auteur van een virtuele klassikale cursus de sessie-informatie niet heeft verstrekt, dan kan de beheerder de sessiedetails opnemen.

Klik op de naam van de VC-cursus in Beheerdersaanmelding. Klik op Instanties in het linkerdeelvenster en op Sessiedetails.  Klik op het pictogram Bewerken in de rechterhoek van de pagina Sessiedetails om de sessiegegevens toe te voegen.

Met de integratie van Adobe Learning Maanger en Adobe Connect voor het maken van virtuele klassikale modules of sessies, moet uw Connect-account ondersteuning bieden voor vergaderzalen met een voldoende aantal ruimten en gelijktijdige gebruikers voor uw use case. Deze vergaderzalen worden gebruikt om virtuele klassikale modules van Learning Manager te hosten. Er wordt door Learning Manager dynamisch een nieuwe Connect vergaderzaal aangemaakt voor elke virtuele klasmodule of sessie binnen Learning Manager.

>[!NOTE]
>
>U moet Adobe Connect apart aanschaffen, los van Adobe Learning Manager.

### Permanente vergaderruimte van Adobe Connect {#persistent}

In Adobe Connect gebruiken klanten bestaande vergaderruimtes die ze al hebben gemaakt in Connect. Alle vergaderruimtes in Connect zijn permanent en de sjablonen voor de vergaderruimtes zijn zorgvuldig ingesteld om een uniforme ervaring voor elke permanente ruimte te bieden.

U kunt een virtueel klaslokaal maken met behulp van een ruimte die al in Adobe Connect is gemaakt.

In Learning Manager kunnen studenten de verbonden ruimte voor hun virtuele sessie ook betreden met behulp van een verificatiemethode.

![](assets/adobe-connect-authentication.png)
*de authentificatie van Adobe Connect*

Wanneer u met behulp van Adobe Connect een VC-module maakt, kunt u een permanente ruimte selecteren. Als u **Nee** selecteert, wordt zoals voorheen een dynamische vergaderruimte gemaakt.

![](assets/persistent-room-selection.png)
*Blijvende ruimteselectie*

Als een student via Adobe Connect een cursus heeft gevolgd en afgerond, wordt na enige tijd een opname van de sessie en een wachtwoord weergegeven in de Learner-app.

![](assets/connect-recording.png)
*verbind opname*

### Quizscores importeren uit Adobe Connect {#quiz-adobe-connect}

Importeer Connect-quizgegevens in Learning Manager en integreer deze met de bestaande rapportworkflow, zodat gebruikers van Leermanager quizgegevens, gebruikersreacties en scores kunnen ophalen uit Adobe Connect-sessies binnen het rapport, zoals deze beschikbaar zijn voor modules met quizzen op eigen tempo.

Als een student een quizcursus volgt of interacties heeft in het Connect-gedeelte die quizrapportages ondersteunen, worden alle interacties van studenten gevolgd totdat ze zijn voltooid. De cursus moet een Connect VC-cursus zijn.

Hieronder volgt een korte workflow van het proces.

**Adobe Connect - Host**

* De host in Connect maakt een cursus en uploadt interactieve inhoud met een quiz.
* De host maakt een training in een **virtuele lesruimte** en slaat de VC-training op. De host heeft de optie om de hierboven gemaakte cursus te koppelen aan de VC of kan tijdens de sessie de optie **Cursus delen** in de Connect-app gebruiken om de cursus te delen.

**het Leren Manager - Auteur**

* De auteur leidt tot een cursus in het Leren Manager met het moduletype als **Virtuele Classroom.**
* Kies uit de **Conferentiesysteem**-vervolgkeuzelijst de optie Koppelen als de VC-provider.
* Kies de Persistent Meeting-cursus en selecteer het VC-klaslokaal dat door de host in Connect is gemaakt. Kies de docent. Sla de cursus op en publiceer deze.

**Leermanager - Student**

* Nadat de cursus is gepubliceerd, schrijft de student zich in voor de cursus.
* De student wordt naar de Connect VC-sessie geleid waar de Connect-host hem/haar toegang toe geeft.

**Adobe Connect - Host**

* Binnen de VC-sessie deelt de Connect-host de quiz die eerder werd gedeeld.

**Adobe Connect - Student**

* De student neemt deel aan de quiz en sluit de sessie wanneer de quiz is voltooid.

**Leermanager - Student**

* De student sluit de sessie en de sessie wordt automatisch gesynchroniseerd.

**Leermanager - Admin**

* Wanneer de sessie is verlopen, wordt de importworkflow van de quiz na de geplande duur geactiveerd.
* Wacht totdat de planning is geactiveerd en de verwerking is voltooid. U kunt de verwerkingsstatus controleren aan de kant van de integratiebeheerder door de **Uitvoeringsstatus** te bekijken binnen de Adobe Connect-connector om de voortgang te zien. Zodra de uitvoering succesvol is, zal de status in **Voltooid** veranderen.

* De beheerder kiest vervolgens de cursus voor leermanagers die eerder is gemaakt. De beheerder ziet het volgende:

   * **Aanwezigheid en scores** - Toont de uiteindelijke quizscore en de aanwezigheidsstatus.
   * **L2-quizscore**

      * **door Gebruiker** - toont de definitieve quizscore die als **Punten** en **Percentage** wordt getoond.
      * **Op vraag** - Toont de quizinformatie als een rapportdiagram.

## Marketo Engage-connector {#marketo}

Learning Manager integreert met Marketo Engage, een marketingautomatiseringssoftware waarmee je marketingcampagnes kunt uitvoeren.

De aansluiting van het Marketo Engage is ontworpen om leads toe te voegen (of bij te werken) in de database van het Marketo Engage wanneer een nieuwe gebruiker wordt toegevoegd aan de Learning Manager-account. Het associeert ook het leergedrag van de gebruiker in Leermanager (cursusinschrijving, cursusvoltooiing, vaardigheidstoewijzing en vaardigheidsvoltooiing) als aangepaste objecten met de overeenkomstige leads in het Marketo Engage. Hierdoor kan een marketeer deze informatie gebruiken om doelgroepen te targeten op basis van hun leergedrag dat is vastgelegd in Learning Manager en functies van Marketo Engage zoals &quot;Slimme lijsten&quot; gebruiken.

Als integratiebeheerder kunt u Learning Manager met een Marketo Engage-exemplaar integreren om gegevenssynchronisatie te automatiseren. U kunt interne gebruikers en trainingsinschrijvingen exporteren, evenals voltooiingen van vaardigheden. De handelingen kunnen gepland worden uitgevoerd en op verzoek worden geconfigureerd.

Om Learning Manager te integreren met uw Marketo-account, moet uw Marketo-account de mogelijkheid hebben om schema&#39;s te maken op basis van API&#39;s.

U kunt de volgende drie rapporten van de Marketo-app downloaden:

* Gebruikersrapport
* Leertranscript
* Gebruikersvaardigheidsrapport

Wanneer u een verbinding met een Marketo Engage maakt, moet u de volgende gegevens opgeven:

* Verbindingsnaam
* Client-id
* Client-geheim
* Marketo Engage

![](assets/marketo-creds.png)

*ga geloofsbrieven voor Marketo* in

>[!NOTE]
>
>U kunt de client-id en het client-geheim uit de Marketo Engage-app halen. Op Marketo app, kunt u identiteitskaart van de Cliënt en geheim van de **** sectie LaunchPoint, en het Domein van Marketo van de **WebServices** sectie krijgen.

Op de **Verenigde sectie van Rapporten** van de verbinding van de Engage van de Markeo in de Leermanager app, kunt u campagnes tot stand brengen die op het volgende worden gebaseerd:

* Een nieuwe gebruiker wordt toegevoegd aan Leerbeheer
* Een nieuwe gebruiker is ingeschreven voor een cursus
* Een nieuwe gebruiker heeft een cursus voltooid
* Een student is ingeschreven voor een vaardigheid
* Een student heeft een vaardigheid gehaald

Net als bij elke andere connector kunt u op verzoek gegevens plannen en exporteren.

### Kolomtoewijzing in Marketo Engage {#column-mapping-in-marketo-engage}

Er zijn twee typen databases in Marketo:

* Lead-database
* Aangepast object-database

Kolomtoewijzing wordt gebruikt om de lead-database te maken. Leads zijn gebruikers die u uit het gebruikersrapport hebt geëxporteerd.

De velden van het gebruikersrapport staan vermeld in de kolom Adobe Learning Manager. De velden in de kolom Marketo bevatten wat Marketo biedt. Met beide kolommen kunt u elk veld in Learning Manager toewijzen aan dat van Marketo. Vanuit een kolom Leermanager sluit u zich aan bij een gerelateerde kolom uit Marketo. Na het samenvoegen van de kolommen wordt er een lead-database gemaakt.

U kunt vervolgens alle geëxporteerde gebruikers in Marketo bekijken.

In het gedeelte **Aangepaste objecten van Marketo** in de Marketo-app kunt u zien dat alle drie de rapporten aanwezig zijn: studenttranscript, gebruikersvaardigheid en gebruikersrapport. Deze rapporten hebben het koord **&quot;cp_&quot;** prepended aan elk. Elke nieuwe gebruiker die wordt geëxporteerd naar Marketo wordt als lead beschouwd.

### Gebeurtenissen

Exporteer gegevens van Learning Manager-gebeurtenissen naar een Marketo Engage-instantie. Selecteer de te exporteren gebeurtenissen naar de Marketo Engage-database ofwel op afroep ofwel op schema.

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

## Microsoft Teams-connector {#microsoft-teams-connector}

Microsoft® Teams® is een permanent op chat gebaseerd samenwerkingsplatform dat het delen van documenten, online vergaderingen en andere functies voor zakelijke communicatie ondersteunt.

Adobe Learning Manager gebruikt een virtual classroom connector die gebruikt kan worden om Microsoft Teams-vergaderingen in Learning Manager te integreren.

De Microsoft Teams-connector verbindt de Learning Manager- en Microsoft Teams-systemen om automatische synchronisatie van gegevens mogelijk te maken. Hier volgt een lijst met de mogelijkheden van de Microsoft Teams-connector:

**de virtuele zittingen van de opstelling gebruikend Microsoft Teams**

Deze connector helpt uw Adobe Learning Manager-account te integreren met uw Microsoft Teams-account. Na de integratie kan een auteur in Learning Manager met de connector Microsoft Teams gebruiken als technologieserviceprovider voor de virtuele klassikale modules die in Learning Manager zijn gemaakt.

**sta Microsoft Teams toe om studenten voor authentiek te verklaren wanneer het ingaan van virtuele klas**

Een organisator van de vergadering kan de lobby inschakelen om de toegang tot de vergadering te beperken en de andere vergaderopties beheren die door Microsoft Teams worden geboden.

**de geautomatiseerde synchronisatie van de gebruikersvoltooiing van het gebruik**

Met het geautomatiseerde synchronisatieproces voor de voltooiing van gebruikers kan een Learning Manager-beheerder automatisch de voltooiingsrecords en de opname-URL voor de Teams-vergadering ophalen.

Voor meer informatie, zie [**de schakelaar van Microsoft Teams in Adobe Learning Manager**](install-microsoft-teams-connector.md) installeren.

## Interface voor trainingsgegevens {#training-data-access}

>[!IMPORTANT]
>
>Deze specifieke functionaliteit is alleen beschikbaar als Adobe Learning Manager als een invoegtoepassing wordt verkocht aan Adobe Experience Manager. De cursusgegevens zouden over 24 uur stabiel zijn.

>[!NOTE]
>
>In de sectie wordt uitgelegd hoe de infrastructuur werkt. Neem contact met ons op als u een headless of AEM-gebaseerde, niet-aangemelde ervaring wilt opbouwen. We zullen de juiste benadering voorstellen voor uw gebruiksscenario. Deze functionaliteit is momenteel niet beschikbaar als selfservice.

De ]**schakelaar van de Toegang van de Gegevens van de Opleiding**[!UICONTROL  laat u een headless ervaring creëren. Deze ervaring kan op zichzelf staan of een aangepaste gebruikersinterface zijn op basis van AEM Sites. Het helpt studenten trainingsinformatie op te halen en weer te geven en maakt zoeken en filteren mogelijk. Zodra de gegevensconnector is ingeschakeld, is er een set openbare API&#39;s beschikbaar om de interface te bouwen, waarin de cursus-/leerpadinformatie voor de studenten wordt weergegeven.

### De connector configureren {#configure-training-data-connector}

Gebruik de ]**schakelaar van de Toegang van de Gegevens van de Opleiding**[!UICONTROL  om uw rekening van Adobe Learning Manager met gegevensopslag en onderzoekssystemen te integreren. Zo krijgt uw op AEM Sites gebaseerde interface trainingsgegevens, worden webpagina&#39;s weergegeven en krijgen studenten betere zoekopties.

Exporteer trainingsmetagegevens van Adobe Learning Manager naar de services voor het ophalen en inschakelen van gegevens met behulp van de API&#39;s. U kunt ook een schema maken om deze exportbewerkingen te automatiseren.

Ga als volgt te werk om de connector voor toegang tot trainingsgegevens te configureren:

1. In de app van Admin van de Integratie, selecteer **[!UICONTROL Toegang van de Gegevens van de Opleiding]** > **[!UICONTROL Aan de slag]**.
1. Selecteer **[!UICONTROL Volgende]** op de **[!UICONTROL Begonnen]** pagina.
1. Typ de verbindingsnaam en de domeinen die in de lijst staan.

   ![](assets/connection-name-and-domain-name.png)
Verbindingsnaam en domeinnaam typen

1. Selecteer het **[!UICONTROL Type van interface]** van de volgende opties:

   * **[!UICONTROL Inheemse Lerende Manager]**: Dit is het standaardaanbod, dat slechts voor inheemse interface beschikbaar is.
   * **[!UICONTROL Headless interfaces]**: Dit is de premium aanbieding die API&#39;s blootstelt aan het bouwen van een niet-aangemelde ervaring.

   ![](assets/types-of-interface.png)
Typen interface

1. Selecteer **[!UICONTROL verbind]**. De basis-URL en de CDN-URL worden automatisch gegenereerd.
U kunt deze URL&#39;s gebruiken om de gegevens op te halen via API&#39;s.

   >[!NOTE]
   >
   >Klanten die de premium aanbieding gebruiken, krijgen een andere URL dan de gebruikers die de standaard aanbieding gebruiken.


1. Selecteer **[!UICONTROL Metagegevens van de Opleiding van de Uitvoer]** op de schakelaarpagina.
1. Selecteer **[!UICONTROL toelaten de uitvoer van trainingsmeta-gegevens]** gebruikend deze verbinding om de opleidingsgegevens uit te voeren.
1. Nadat u de verbinding hebt ingeschakeld, worden de afbeeldingen van alle cursussen, leerpaden en certificaten gemigreerd naar de CDN.
1. Exporteer de metagegevens van de cursussen, leerpaden en certificaten naar de service voor zoeken en ophalen.
1. U kunt de export van metagegevens plannen door de planningsoptie Inschakelen te selecteren. Het schema zal automatisch om de 3 uur voor het Premium Plan voorkomen.
1. Voor een rapport op bestelling, ga naar **[!UICONTROL Op bestelling]**, selecteer de **[!UICONTROL datum van het Begin]**, en dan **[!UICONTROL klik]** uitvoert.
U kunt de status van de rapportuitvoering op de **[!UICONTROL pagina van de Status van de Uitvoering controleren]**.

### Website maken in AEM {#create-website-in-aem}

**Vereiste:** installeer het AEM pakket van de [**bewaarplaats GitHub** ](https://github.com/adobe/adobe-learning-manager-reference-site/releases/tag/1.0.0).

1. Gebruik basis- en opvraag-URL&#39;s, client-id, client-geheim en Admin Refresh Token, en maak een configuratie in AEM.
1. Maak de website met behulp van de AEM-componenten.
1. Publiceer de website.

Voor meer informatie, zie dit [**document**](../../adobe-learning-manager-integration-aem.md).

### Studenten {#learners}

De gepubliceerde website toont een lijst met alle gemigreerde cursussen, certificaten en leertrajecten die zijn opgehaald uit de zoekservice voor niet-aangemelde studenten.

Wanneer een student op cursus, certificaat of leerpad klikt, wordt de overzichtspagina geopend. Wanneer de student zich inschrijft, moet deze zich eerst op de pagina aanmelden en daarna de cursus volgen.

### Niet-aangemelde ervaring {#non-logged-in-experience}

Dankzij de niet-aangemelde ervaring kunt u een real-time ervaring creëren voor niet-aangemelde gebruikers. Een niet-aangemelde ervaring fungeert bijvoorbeeld als startpagina voor marketingcampagnes om aanmelding-ups te stimuleren.

De niet-het programma geopende ervaring in Adobe Learning Manager kan worden gevormd gebruikend de ]**schakelaar van de Toegang van de Gegevens van de Opleiding**[!UICONTROL . De connector biedt de volgende mogelijkheden:

* Standard-aanbieding
* Premium-aanbieding

**Standaard het aanbieden**

De standaardaanbieding is om de native versie van Adobe Learning Manager te bouwen. Gebruikers kunnen een headless ervaring bouwen die alleen voor demonstraties en niet-aangemelde headless is. De headless ervaring van de demonstratie is niet schaalbaar en mag niet worden gebruikt in een productieomgeving.

**het Aanbieden van de Premie**

Het premieaanbieden helpt gebruikers een headless interface bouwen, die door de **[!UICONTROL schakelaar van de Toegang van de Gegevens van de Opleiding]** wordt gevormd. Hiermee kunnen gebruikers real-time gegevens over cursussen en leerpaden ophalen, zoals naam, beschrijving, auteur, vaardigheden, duur, enz. Voor overvloeiingsscenario&#39;s krijgt u ook real-time beperkingen voor licenties, bezette plaatsen, wachtlijstlimieten en wachtlijstaantallen. Klanten kunnen deze API&#39;s gebruiken om zoek- en filtermogelijkheden en een volledig cursusoverzicht voor niet-aangemelde studenten te maken.

Klanten kunnen een Premium-lidmaatschap aanschaffen om deze uiterst schaalbare, niet-aangemelde ervaring te creëren.

>[!NOTE]
>
>Neem contact op met het ondersteuningsteam of de CSM om het Premium-lidmaatschap aan te schaffen.

Nadat een gebruiker een lidmaatschap heeft gekocht, activeert het CSM-team het Premium-lidmaatschap voor hen. Met behulp van de connector Trainingsgegevenstoegang kunnen gebruikers een niet-aangemelde ervaring instellen met de eerder vermelde functies.

## Adobe Commerce-connector {#adobe-commerce-connector}

>[!NOTE]
>
>Deze specifieke functionaliteit is alleen beschikbaar als Adobe Learning Manager als invoegtoepassing wordt verkocht aan Adobe Experience Manager.

>[!NOTE]
>
>Deze connector kan ook worden ingeschakeld voor proefaccounts.

Adobe Learning Manager biedt nu integratie met Adobe Commerce, een platform om eCommerce-ervaringen te bouwen voor B2B- en B2C-klanten.

Adobe Commerce is een uitbreidbare en schaalbare oplossing voor commerce enablement waarmee u op één platform commerce-ervaringen via meerdere kanalen kunt opbouwen voor B2B- en B2C-klanten. Gebruik de Adobe Commerce-connector om uw Adobe Learning Manager-account te verbinden met Adobe Commerce en e-commercemogelijkheden op het leerplatform te realiseren.

Schakel deze connector in en gebruik de Adobe Commerce-functies om het leeraanbod als betaalde trainingen aan te bieden. Merk op dat u Adobe Commerce apart moet kopen voordat u het met Adobe Learning Manager kunt integreren via deze connector.

De connector integreert met Adobe Commerce door de opleidingsgegevens naar het commerceplatform te sturen, waar studenten vervolgens een betaling kunnen doen en een opleiding kunnen aanschaffen.

Naast het initiëren van een aankoop, verzamelt de connector ook aankoopgegevens van Adobe Commerce, die door Adobe Learning Manager gebruikt worden om de aankoop te valideren en toegang tot de training te ontgrendelen.

**Voorwaarden**

1. Laat [ RabbitMq ](https://devdocs.magento.com/cloud/project/services-rabbit.html) of een andere overseinenmakelaar toe.
1. Laat [ CRON ](https://devdocs.magento.com/cloud/env/variables-deploy.html#cron_consumers_runner) toe.
1. Bewerk voor stappen 1 en 2 de volgende bestanden:

   1. .magento.app.yaml
   1. .magento/services.yaml
   1. .magento.env.yaml

1. Opties limiet opheffen via aangepaste module. Deze stap is optioneel, maar wordt sterk aanbevolen voor grote datasets.
1. Schakel alle async API&#39;s op de pagina in. Omdat er veel gegevens kunnen zijn, gebeurt de uitvoer asynchroon. De API&#39;s van Adobe Commerce worden de payload van de aanvraag genoemd. Het verzoek duwt de berichten aan een rij en er is een consument aan deze rij, die deze berichten verwerkt en producten aan de verkoopkant creeert. Adobe Commerce voorziet standaard niet in deze async verwerking. Daarom moet u deze optie inschakelen.
1. Voeg een link toe om terug te keren naar ALM op de succespagina van de betaling. Deze retour-URL moet geconfigureerd zijn in Adobe Commerce. De URL die voor de koppeling moet worden gebruikt. - `https://learningmanager.adobe.com/app/learner#/postPayment`
1. Wijzig de indexering van &quot;Bij opslaan&quot; in &quot;Gepland&quot;.  Voor meer informatie, zie dit [ KB ](https://support.magento.com/hc/en-us/articles/360040227191).
1. Pas de volgende patches toe. Voor meer informatie, zie [ flarden ](https://devdocs.magento.com/cloud/project/project-patch.html) toepassen.
1. Configureer snel.  Voor Adobe Commerce is een snelle implementatie van cloudinfrastructuur vereist. Deze wordt gebruikt in Staging- en Productomgevingen. Zie [Fastly instellen](https://devdocs.magento.com/cloud/cdn/configure-fastly.html) voor meer informatie.

### De connector configureren {#configure-connector}

Klik, als integratiebeheerder, in de Adobe Commerce-connector op **[!UICONTROL Connect]**.

Voer op de configuratiepagina de volgende gegevens in. Deze details, de verificatiecodes, zijn beschikbaar in Adobe Commerce. Zodra u een integratie in Adobe Commerce hebt gemaakt, zijn de referenties daar beschikbaar.

![](assets/adobe-commerce-configuration.png)
*vorm de Verbinding van Adobe Commerce*

Zodra de Adobe Commerce-connectorverbinding ingeschakeld is, kan een auteur de prijs voor een cursus, een leerpad of een certificaat bepalen.

Nadat de cursus, het leerpad of het certificaat gepubliceerd is, kan een cursist cursussen kopen de cursisten-app.

* **Native Learning Manager:** De student kan een cursus, Leerplan of een certificaat kopen vanuit Learning Manager. Dit is alleen van toepassing wanneer de auteur een prijs heeft toegevoegd.
* **Op maat gemaakt met behulp van AEM sites:** De leerling kan een cursus kopen op een AEM-site.

### Workflow {#workflow}

De Adobe Commerce Administrator configureert Learning Manager als een integratie.

De auteur markeert de cursussen, leerpaden of certificaten als premium en kent prijzen toe. Deze optie is er alleen als e-commerce voor het account is ingeschakeld. Ga voor meer informatie naar [Cursussen maken](../../authors/feature-summary/courses.md).

De cursus of het leerpad zal niet beschikbaar zijn voor aankoop totdat de gegevens gesynchroniseerd zijn in Adobe Commerce.

### Cursussen exporteren naar Adobe Commerce {#export-commerce}

Nadat een auteur de prijzen voor verschillende cursussen, leerpaden of certificeringen heeft ingesteld, exporteert u, als de integratiebeheerder, de cursussen, leerpaden of certificeringen naar Adobe Commerce.

>[!NOTE]
>
>In de versie van Maart 2024 van Adobe Learning Manager, hebben wij steun voor [ Adobe Commerce 2.4.6 ](https://experienceleague.adobe.com/docs/commerce-operations/release/notes/adobe-commerce/2-4-6.html?lang=en) geïntroduceerd.


1. Klik **[!UICONTROL Meta-gegevens van de Opleiding van de Uitvoer]** > **[!UICONTROL op bestelling]**.

1. Selecteer de datums.

1. Klik op **[!UICONTROL Uitvoeren]**. Bij een succesvolle uitvoering zullen alle cursussen of leerpaden die geprijsd zijn, verplaatst worden naar Adobe Commerce. De student kan de cursus vervolgens kopen via Leermanager.

### Native Learning Manager met Adobe Commerce {#learning-manager-with-commerce}

#### Student {#learner}

Als student moet u aangemeld zijn om een cursus, een certificaat of een leerpad te kopen.

Om een cursus aan te schaffen klikt u op Nu kopen. U wordt doorverwezen naar Adobe Commerce om de aankoop te voltooien. Zodra de betaling is gelukt, ziet u een bericht waarin u wordt gevraagd terug te gaan naar de Leermanager en de cursus te starten. U moet zich ook afzonderlijk aanmelden bij Adobe Commerce om de aankoop te voltooien.

Als u een cursus, certificaat of leerpad aanschaft via ALM Native of AEM, ontvangt u e-mails van zowel ALM als Adobe Commerce.

Bovendien kunt u e-mails van Adobe Commerce in- en uitschakelen.

### AEM sites met Adobe Commerce {#aem-sites-with-adobe-commerce}

Als de optie Op maat gemaakt met behulp van AEM-sites ingeschakeld is, kunt u als leerling cursussen kopen van een op maat gemaakte AEM-site.

De AEM-site zal alle metadata van Learning Manager hebben om zoeken via Adobe Commerce mogelijk te maken. De cursussen worden opgehaald van Adobe Commerce in niet-aangemelde gevallen.

Zowel ingelogd als niet ingelogd is mogelijk. Niet-aangemelde gebruikers kunnen de catalogus, leerplannen en certificaten doorzoeken en bekijken. Maar als u een cursus wilt aanschaffen, moet u inloggen op de AEM-site.

Net als bij de native Learning Manager kunt u, nadat u ingelogd bent, een cursus aan het winkelwagentje toevoegen en vervolgens de cursus bekijken of kopen.

### Adobe Commerce-connector instellen {#setup-commerce-connector}

#### Vereisten {#pre-requisites}

De beheerder laat checkbox toe, **laat tarifering voor trainingen**, in **Montages > Algemeen** in Admin app. Als de optie is ingeschakeld, kunnen auteurs prijzen voor trainingen opgeven.  Als u een Adobe Commerce-koppeling toevoegt, is dit vinkje automatisch van toepassing.

Adobe Learning Manager ondersteunt e-commerce om opleidingen te kopen en te verkopen. Hier kunnen gebruikers opleidingen verkopen om de up-selling en cross-selling van hun producten te bevorderen.

Met de integratie van Adobe Commerce ondersteunt Adobe Learning Manager het kopen en verkopen van opleidingen om een completere klantenervaring te bieden in Customer Partner Education-scenario&#39;s.

De belangrijkste doelen van deze integratie zijn:

* Gebruikers kunnen omzet genereren door cursussen te verkopen op Adobe Learning Manager of via een Headless Learning-interface.
* Schakel Adobe Commerce-integratie in het platform in om cursussen te verkopen met behulp van de native app en AEM van Learning Manager.
* Laat de klanten van de leermanager formeel leren aanbieden in de vorm van betaalde cursussen.
* Studenten in staat stellen een voorvertoning van cursussen te bekijken voordat ze besluiten de training aan te schaffen.

#### Adobe Learning Manager-playlist {#native-learning-manager}

**Beheerder van de Integratie**

1. Voeg op de pagina Integratiebeheerder de Adobe Commerce-connector toe. Haal de verificaties op uit de applicatie die in Adobe Commerce is gemaakt.
1. Zodra Adobe Commerce ingeschakeld is, is e-commerce ingeschakeld op Adobe Learning Manager. De gegevens van Learning Manager worden naar Adobe Commerce gesynchroniseerd volgens een schema. De gegevens bevatten alle (betaalde) opleidingen, samen met de metadata (gebruikers, vaardigheden, naam van de auteur, prijs enz.).

>[!NOTE]
>
>Adobe Learning Manager en Adobe Commerce hebben verschillende aanmeldingsgegevens.

### AEM {#aem}

In deze modus volgt een Student de cursus op een AEM-gebaseerde site, die gebouwd is met behulp van AEM-gebaseerde sjablonen en componenten.

Op de AEM site heeft de student ondersteuning voor winkelwagentje, winkelwagentje toevoegen aan winkelwagentje, cursussen uit het winkelwagentje verwijderen enzovoort.

Als de gebruiker niet ingelogd is, kan deze nog steeds zoeken naar cursuscatalogi en cursusdetails bekijken, maar geen cursus kopen. Als student moet u ingelogd zijn om een cursus te kopen.

Nadat de Student de cursus gekocht heeft, wordt hij doorverwezen naar de overzichtspagina van de cursus in de staat van inschrijving, waar hij de gekochte cursus kan volgen.

#### Headless: niet-ingelogd {#headless-non-logged-in}

Een student kan:

* Opleidingen zoeken via de zoekfunctie.
* Opleidingen filteren naar prijsbereik.

Een student kan niet:

* Een cursus aanschaffen via de Overzichtspagina.
* Betaalde inhoud bekijken.

#### Headless: ingelogd {#headless-logged-in}

Een student kan:

* Gratis of betaalde opleidingen ontdekken, bekijken, zoeken en filteren.

* Een cursus toevoegen aan zijn winkelwagen en dan afrekenen om hem te kopen.
* Trainingscursussen in de winkelwagen toevoegen, updaten of verwijderen.
* Gelijktijdig betalen voor meerdere trainingscursussen.
* Een betaalde cursus bekijken in de speler.
* Berichten zien als er een betalingsfout is.

* De factuur zien als bijlage bij de e-mail na het kopen van de cursus.

#### On-demand synchronisatie {#on-demand-sync}

De synchronisatie tussen Learning Manager en Adobe Commerce vindt tweemaal per dag plaats. Nadat de Beheerder een rekening voor e-commerce toelaat, **laat de uitvoer van opleidingsmeta-gegevens toe gebruikend deze verbinding** optie, wanneer toegelaten, slaat de beelden van de Cursus, het Leren Weg, en Certificaten in een openbare CDN op.

Als de gegevens niet worden gesynchroniseerd, worden de prijzen niet voor studenten weergegeven.

Als e-commerce voor de native Learning Manager is ingeschakeld en de synchronisatie tussen Learning Manager en Adobe Commerce is voltooid, kunnen studenten gratis of betaalde training bekijken of doorzoeken.

Voor AEM, is er geen Nu kopen, slechts **voeg aan Kaart** knoop toe. Deze knop blijft ook uitgeschakeld als de synchronisatie niet wordt uitgevoerd.

#### Veelgestelde vragen {#faqs}

+++Welke cursussen kunnen niet worden aangeschaft?

Cursussen zoals herhaalde certificeringen, opleidingen van de inhoudsmarkt, verworven opleidingen, opleidingen van connectoren, Taakhulpen en door de manager goedgekeurde/genomineerde cursussen, kunnen niet door een student gekocht worden.
+++

+++Is er een wijziging in het Studenttranscript en het trainingsrapport?

Deze rapporten tonen de prijs en de datum van aankoop van alle gekochte trainingen in de rekening.
+++

+++Kan een student zich inschrijven voor een gratis training?

Ja, een student kan zich inschrijven voor een gratis opleiding. Een gratis opleiding toont de knoppen voor voorvertoning en inschrijving op de overzichtspagina.
+++
