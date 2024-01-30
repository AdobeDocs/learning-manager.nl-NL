---
description: Lees hoe u Salesforce met Learning Manager kunt integreren met behulp van connectoren, hoe u FTP met Learning Manager kunt integreren en hoe u CSV automatisch kunt uploaden met behulp van een FTP-connector.
jcr-language: en_us
title: Learning Manager-connectoren
preview: true
source-git-commit: 2317aa899a82abe24d38c4e40a06df3646fde310
workflow-type: tm+mt
source-wordcount: '6293'
ht-degree: 72%

---



# Learning Manager-connectoren

Lees hoe u Salesforce met Learning Manager kunt integreren met behulp van connectoren, hoe u FTP met Learning Manager kunt integreren en hoe u CSV automatisch kunt uploaden met behulp van een FTP-connector.

Bedrijven hebben andere toepassingen en systemen die mogelijk geïntegreerd moeten worden met Learning Manager. Connectoren zijn hulpprogramma&#39;s die helpen bij het uitvoeren van op data gebaseerde integraties, zoals het importeren van gegevens in Learning Manager van externe systemen of het exporteren van gegevens naar externe systemen vanuit Learning Manager. In de versie van juli 2016 hebben de connectoren alleen de mogelijkheid om gebruikers voor Learning Manager in bulk te importeren uit externe systemen.

Learning Manager levert Salesforce- en FTP-connectoren. Via de Salesforce-connector kunnen de integratiebeheerders van een organisatie hun Salesforce-toepassing met Learning Manager integreren. Als integrator kunt u ook een FTP-connector gebruiken om een aantal gebruikers automatisch in uw bedrijfstoepassing te importeren.

Learning Manager levert ook de Lynda-, getAbstract- en de Harvard Management System-connectoren. Hiermee kunnen studenten toegang krijgen tot en gebruik maken van cursussen van Lynda.com, getAbstract en Harvard ManageMentor.

Lees verder om te weten te komen hoe u elk van deze connectoren in Learning Manager kunt configureren en gebruiken.

![](assets/connectorslist.jpg)

## Salesforce-connector {#sfconnector}

De Salesforce-connector verbindt Learning Manager met Salesforce-accounts om de synchronisatie van gegevens te automatiseren. De mogelijkheden van de Salesforce-connector zijn als volgt:

### Kenmerken toewijzen

De integratiebeheerder kan Salesforce-kolommen kiezen en aan de overeenkomstige groepeerbare kenmerken van Learning Manager toewijzen. Dit is een eenmalige inspanning. Wanneer de toewijzing is voltooid, wordt dezelfde toewijzing voor verdere gebruikersimporten gebruikt. De beheerder kan de toewijzing opnieuw configureren als deze een andere toewijzing voor het importeren van gebruikers wil.

### Geautomatiseerde gebruikersimport

Via het proces voor gebruikersimport kan de Learning Manager-beheerder werknemersgegevens uit Salesforce ophalen en automatisch in Learning Manager importeren. Door deze automatisering hoeft het creëren van CSV&#39;s en het uploaden naar Learning Manager niet handmatig te gebeuren.

### Automatisch plannen

Het kan effectief zijn om de functie voor automatische planning samen met de functie voor geautomatiseerde gebruikersimport te gebruiken. De Learning Manager-beheerder kan het schema volgens de behoeften van de organisatie instellen. Gebruikers in de toepassing Leermanager kunnen volgens het schema up-to-date zijn. De synchronisatie kan dagelijks worden uitgevoerd in de Learning Manager-toepassing.

### Gebruikers filteren

De Learning Manager-beheerder kan gebruikers filteren voordat ze worden geïmporteerd. Zo kan de Learning Manager-beheerder er bijvoorbeeld voor kiezen om alle gebruikers in de hiërarchie onder één of meer specifieke managers te importeren.

## De Salesforce-connector configureren {#configuresalesforceconnector}

Leer het proces kennen om Learning Manager te integreren met Salesforce.

### vereisten van het proces leren kennen {#prerequisites}

Zorg ervoor dat u uw organisatie-URL voor Salesforce hebt. Als uw organisatie bijvoorbeeld **myorg** heet, kan de Salesforce-URL [https://myorg.salesforce.com](https://myorg.salesforce.com/) zijn. Dit is alles wat u moet invoeren om het Salesforce-account met Learning Manager te verbinden.

Zorg er ook voor dat u de juiste gegevens hebt om u bij het account aan te melden.

## Een verbinding maken {#createaconnection}

1. Beweeg de muis over de Salesforce-kaart/miniatuur op de Learning Manager-startpagina. Er verschijnt een menu. Klik op **[!UICONTROL Verbinden]** in het menu.

   ![](assets/mouserover-salesforce.png)

1. Er verschijnt een dialoogvenster waarin u wordt gevraagd om de org-url in te voeren. Klikken **[!UICONTROL Verbinden]** nadat u de URL hebt opgegeven.
1. Zodra de verbinding tot stand is gebracht, verschijnt de overzichtspagina.

## Kenmerken toewijzen {#mapattributes}

Zodra de verbinding tot stand is gebracht, kunt u de Salesforce-kolommen aan de overeenkomstige attributen van Learning Manager koppelen. Deze stap is verplicht.

1. Op de toewijzingspagina ziet u links de kolommen van de Leermanager en rechts de kolommen van Salesforce. Selecteer de juiste kolomnaam die is toegewezen aan de kolomnaam van de leermanager.

   ![](assets/sfdc-map-columns.png)

   De kolomgegevens van de leermanager die aan de linkerkant worden weergegeven, worden opgehaald uit de actieve velden. De **manager** veld moet noodzakelijkerwijs worden toegewezen aan een veld van het type e-mailadres. U moet alle kolommen toewijzen voordat u de connector kunt gebruiken.

1. Klikken **[!UICONTROL Opslaan]** na het voltooien van de toewijzing.
1. De connector is nu klaar voor gebruik. Het account dat nu is geconfigureerd, verschijnt als gegevensbron in de beheerdersapp zodat de beheerder de import of de synchronisatie op verzoek kan plannen.

## Gebruik van de Salesforce-connector {#usingsalesforceconnector}

De Salesforce-connector maakt verbinding met Salesforce.com om de geconfigureerde gebruikers op te halen en toe te voegen aan Learning Manager.

## Learning Manager FTP-connector {#ftpconnector}

Met behulp van de FTP-connector kunt u Learning Manager integreren met willekeurige externe systemen om de synchronisatie van gegevens te automatiseren. Van externe systemen wordt verwacht dat ze gegevens in een CSV-formaat kunnen exporteren en in de juiste map van het Learning Manager FTP-account kunnen plaatsen. De mogelijkheden voor FTP-connector zijn als volgt:

U kunt ook de Box-connector gebruiken voor gegevensmigratie, gebruikersimport en gegevensexport. Zie [Box connector](third-party-connectors.md#main-pars_header_302653946) voor meer informatie.

## Gegevensimport {#dataimport}

Met het gebruikersimportproces kan de Learning Manager Administrator werknemersgegevens ophalen van de FTP-service van Learning Manager en ze automatisch in Learning Manager importeren. Met behulp van deze functie kunt u meerdere systemen integreren door de door deze systemen gegenereerde CSV in de juiste mappen van de FTP-accounts te plaatsen. Learning Manager haalt de CSV-bestanden op, voegt ze samen en importeert de gegevens volgens de planning. Raadpleeg de planningsfunctie voor meer informatie.

**Kenmerken toewijzen**

Kenmerken toewijzen Deze toewijzing is een eenmalige inspanning. Zodra de toewijzing gereed is, wordt dezelfde toewijzing gebruikt in volgende gebruikersimports. De toewijzing kan opnieuw worden geconfigureerd als de beheerder een andere toewijzing voor het importeren van gebruikers wil hebben.

## Gegevens exporteren {#exportdata}

Gegevensexport stelt gebruikers in staat om de vaardigheden van de gebruiker te exporteren naar een FTP-locatie om deze te integreren met een willekeurig systeem van derden.

## Planning {#scheduling}

De beheerder kan planningstaken volgens de vereisten van de organisatie instellen en gebruikers in de Learning Manager-toepassing zijn up-to-date volgens de planning. Op dezelfde manier kan de integratiebeheerder de export van vaardigheden op een tijdige basis plannen om deze te integreren met een extern systeem. De synchronisatie kan dagelijks worden uitgevoerd in de Learning Manager-toepassing.

## Learning Manager FTP-connector configureren {#configurecaptivateprimeftpconnector}

Leer het proces kennen om Learning Manager te integreren met de FTP-connector.

### Een verbinding maken {#Createaconnection-1}

1. Beweeg de muis over de FTP-kaart/miniatuur op de Learning Manager-startpagina. Er verschijnt een menu. Klik op **[!UICONTROL Verbinden]** in het menu.

   ![](assets/mouseover-ftpconnector.png)

1. Er verschijnt een dialoogvenster waarin u wordt gevraagd de e-mail-ID in te voeren. Geef de e-mail-ID op van de persoon die verantwoordelijk is voor het beheer van het FTP-account van de Learning Manager voor de organisatie. Klikken **[!UICONTROL Verbinden]** nadat u de e-mail-ID hebt opgegeven.
1. Learning Manager stuurt u een e-mail waarin de gebruiker wordt gevraagd het wachtwoord opnieuw in te stellen voordat hij/zij voor het eerst toegang krijgt tot de FTP. De gebruiker moet het wachtwoord opnieuw instellen en het gebruiken om toegang te krijgen tot het Learning Manager-FTP-account.

   Er kan slechts één Learning Manager FTP-account worden aangemaakt voor een bepaald Learning Manager-account.

   Op de overzichtspagina kunt u de verbindingsnaam voor uw integratie opgeven. Kies uit de volgende opties welke actie u wilt ondernemen:

   * Interne gebruikers importeren
   * Vaardigheden van gebruikers exporteren - Een planning configureren
   * Vaardigheden van gebruikers exporteren - Op verzoek

   ![](assets/connectors-overview.png)

## Importeren

+++ interne gebruiker

Met de optie voor het importeren van interne gebruikers kunt u het genereren van een gebruikersimportverslag automatisch plannen. De gegenereerde rapporten worden als .CSV-bestanden naar u verzonden.

+++

+++Kenmerken toewijzen

Zodra de verbinding tot stand is gebracht, kunt u de kolommen van de CSV-bestanden die in de FTP-map zijn geplaatst toewijzen aan de overeenkomstige attributen van Learning Manager. Deze stap is verplicht.

1. Op de pagina Kenmerken toewijzen ziet u links de verwachte kolommen van de leermanager en rechts de CSV-kolomnamen. In eerste instantie ziet u aan de rechterkant een leeg selectievakje. Een CSV-sjabloon importeren door te klikken **Bestand kiezen**.
1. Via de bovenstaande stap worden alle CSV-kolomnamen aan de rechterkant van de vervolgkeuzelijst ingevuld. Selecteer de juiste kolomnaam die is toegewezen aan de kolomnaam van de leermanager.

   *Het veld Manager moet worden toegewezen aan een veld van het type e-mailadres. U moet alle kolommen toewijzen voor u de connector kunt gebruiken.*

1. Klikken **[!UICONTROL Opslaan]** na het voltooien van de toewijzing.

   De connector is nu klaar voor gebruik. Het geconfigureerde account verschijnt nu als gegevensbron in de beheerdersapp zodat de beheerder de import of de synchronisatie op verzoek kan plannen.



+++

+++De FTP-connector van Learning Manager gebruiken

1. De CSV-bestanden van externe systemen moeten op het volgende pad worden geplaatst:

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   **Opmerking:** In de release van juli 2016 is alleen import van gebruikers toegestaan. Om de FTP-connector te kunnen gebruiken, moet u ervoor zorgen dat de CSV-bestanden in de volgende map worden geplaatst:

   `code Home/import/user/internal/*.csv`

1. De FTP-connector haalt alle rijen uit CSV-bestanden, dus het is belangrijk dat de rij die overeenkomt met een gebruiker in een CSV niet in andere CSV&#39;s wordt weergegeven.
1. Alle CSV&#39;s moeten de kolommen bevatten die in de toewijzing zijn opgegeven.
1. Alle vereiste CSV&#39;s moeten aanwezig zijn in de map voordat het proces begint.

Bij het importeren van gebruikers in Learning Manager, moet de beheerder ook weten hoe gebruikers in Learning Manager beheerd worden. Raadpleeg [Help bij gebruikersbeheer](../integration-admin/feature-summary/migration-manual.md#usermanagement) voor meer informatie.

+++

## Badge als

+++Vaardigheden

Er zijn twee opties om vaardigheidsrapporten van de gebruiker te exporteren.

**[!UICONTROL Gebruikersvaardigheden - op verzoek]**: U kunt de startdatum opgeven en het rapport exporteren met de optie. Het rapport wordt geëxtraheerd vanaf de ingevoerde datum tot heden.

![](assets/user-skills-on-demand.png)

**[!UICONTROL Gebruikersvaardigheden - Configureren]**: via deze optie kunt u de extractie van het rapport plannen. Selecteer het selectievakje Planning inschakelen en geef de begindatum en -tijd op. U kunt ook aangeven met welke intervallen u het rapport wilt laten genereren en verzenden.

![](assets/user-skills-configure.png)

+++

Als u de Exportmap wilt openen waarin de geëxporteerde bestanden op uw FTP-locatie worden geplaatst, opent u de koppeling naar de FTP-map op de pagina Gebruikersvaardigheden, zoals hieronder weergegeven.

![](assets/ftp-folder.png)

De automatisch geëxporteerde bestanden zijn aanwezig op de locatie **Home/export/&#42;FTP_locatie&#42;**

De automatisch geëxporteerde bestanden zijn beschikbaar met de titel, **skill_results__&#42;datum vanaf &#42;_aan_&#42;datum tot&#42;.csv**

![](assets/exported-csvs.png)

## Lynda-connector {#lyndaconnector}

De Lynda-connector kan worden gebruikt door zakelijke klanten van Lynda.com die graag willen dat hun studenten Lynda-cursussen kunnen zoeken en volgen in Learning Manager. De connector kan worden geconfigureerd om periodiek cursussen van Lynda.com op te halen met uw API-sleutel. Zodra een cursus binnen Learning Manager is gemaakt, kunnen gebruikers deze opzoeken en volgen. De voortgang van de student kan vervolgens binnen Learning Manager worden bijgehouden.

### De Lynda-connector configureren {#configurethelyndaconnector}

1. Klik op Lynda in het dashboard van de integratiebeheerder.

   U ziet de tegel met drie opties: Aan de slag, Verbinden en Verbindingen beheren.

1. Klik op Verbinden als u de Lynda-connector voor het eerst configureert.

   U moet het Exavault FTP-account configureren voordat u deze connector configureert.

1. Geef op de verbindingspagina een naam op voor uw connector. Voer de appsleutel en de geheime sleutel voor uw verbinding in.

   U moet contact opnemen met uw leverancier voor de appsleutel en de geheime sleutel.

1. Klik op Opslaan.

   De configuratie wordt opgeslagen en de Lynda-verbinding voor uw account wordt toegevoegd. U kunt nu vanaf de startpagina op Verbindingen beheren klikken en uw configuratie op elk gewenst moment bewerken.

1. Als u al een verbinding tot stand hebt gebracht, klikt u op Verbindingen beheren om al uw verbindingen te bekijken.

   De migratiefunctie moet zijn ingeschakeld voor uw account voordat u deze connector kunt configureren.

1. Klik op de verbinding die u wilt bewerken.
1. Klik in het linkerdeelvenster op Configureren. Voer een van de volgende handelingen uit:

   * Bekijk of bewerk de details van uw account en het synchronisatieschema vanuit dit venster. Selecteer het selectievakje Verbinding inschakelen om dit account in te schakelen.
   * Klik op Bewerken en bewerk uw gegevens. Klik op Herstellen om uw updates voor dit veld ongedaan te maken.
   * Klik op Schema inschakelen om uw synchronisatie te plannen. U kunt de starttijd en -datum invoeren en vervolgens de frequentie van uw synchronisatieplanning in dagen invoeren. Bijvoorbeeld, om de drie dagen synchroniseren.

   Klik op Opslaan om uw wijzigingen op te slaan.

   ![](assets/lynda.png)

1. Klik in het linkerdeelvenster op Uitvoering op verzoek. Met deze optie kunt u gebruikersfeeds en andere relevante gegevens vanuit Lynda importeren. Voer de startdatum voor de uitvoering op verzoek in en klik op Uitvoeren om de synchronisatie uit te voeren. Alle gegevens vanaf de startdatum tot heden worden geïmporteerd.

   * Wanneer de toepassing tijdens de synchronisatie uitvalt, kunt u tijdens de uitvoering klikken op Toegang tot Learning Manager uitschakelen.
   * Als u tijdens de uitvoering op Toegang tot Learning Manager inschakelen klikt, is er geen onderbreking van de service tijdens de synchronisatie.

   ![](assets/lynda-ondemand.png)

1. U kunt ook op elk moment op Uitvoeringsstatus in het linkerdeelvenster klikken om het overzicht van alle runs voor deze connector in chronologische volgorde te bekijken. U kunt de startdatum en duur van de synchronisatie, het type synchronisatie (of het al dan niet gaat om synchronisatie op verzoek) en de status van de synchronisatie (of de synchronisatie wordt uitgevoerd of is voltooid) bekijken.

   Wanneer u een verbinding wist en opnieuw aanmaakt, worden de vorige runs voor de connector weergegeven. U kunt alle runs bekijken voordat u de verbinding wist.

   U kunt alleen de laatste synchronisatie opnieuw uitvoeren.

   ![](assets/lynda-executionstatus.png)

## getAbstract-connector {#getabstractconnector}

Deze getAbstract-connector kan gebruikt worden door zakelijke klanten van getAbstract.com die graag willen dat hun studenten getAbstract-samenvattingen kunnen zoeken en volgen in Learning Manager. De connector kan worden geconfigureerd om periodiek gebruiksgegevens op te halen, op basis waarvan de voltooiingsrecords van studenten in Learning Manager worden gemaakt. Lees verder om te weten te komen hoe u deze connector in Learning Manager moet configureren.

### De getAbstract-connector configureren {#configurethegetabstractconnector}

1. Klik in het dashboard van de integratiebeheerder op getAbstract.

   U ziet de tegel met drie verschillende opties: Aan de slag, Verbinden en Verbindingen beheren.

1. Klik op Verbinden als u de getAbstract-connector voor het eerst configureert.

   U moet het Exavault FTP-account configureren voordat u deze connector configureert.

   Zorg ervoor dat u deze FTP-gegevens deelt met uw inhoudaanbieder om toegang te krijgen tot de feeds.

1. Voer in het veld Verbindingsnaam een naam voor uw verbinding in.

   Voer de juiste sleutels in de velden Client-ID en Clientgeheim in. Mogelijk moet u contact opnemen met uw leverancier voor de juiste sleutels voor deze connector.

   De sleutels zijn nodig om de metagegevens van de door de client gevolgde cursussen te verkrijgen.

1. Klik als u al verbinding hebt op de startpagina op getAbstract > Verbindingen beheren om uw bestaande configuratie te bekijken en te bewerken.

   De migratiefunctie moet zijn ingeschakeld voor uw account voordat u deze connector kunt configureren.

1. Klik op de verbinding waarvan u de configuratie wilt bekijken of bewerken.

   ![](assets/getabstractschedulepage.png)

1. Klik in het linkerdeelvenster op Configureren. Voer een van de volgende handelingen uit:

   * Bekijk of bewerk de details van uw account en het synchronisatieschema vanuit dit venster. Selecteer het selectievakje Verbinding inschakelen om dit account in te schakelen.
   * Klik op Bewerken en bewerk uw gegevens. Klik op Herstellen om uw updates voor dit veld ongedaan te maken.
   * Klik op Schema inschakelen om uw synchronisatie te plannen. U kunt de starttijd en -datum invoeren en vervolgens de frequentie van uw synchronisatieplanning in dagen invoeren. Bijvoorbeeld, om de drie dagen synchroniseren.

1. Klik op Opslaan.

   De configuratie wordt opgeslagen en de getAbstract-verbinding voor uw account wordt toegevoegd.

1. Klik in het linkerdeelvenster op Uitvoering op verzoek. Met deze optie kunt u gebruikersfeeds en andere relevante gegevens uit getAbstract importeren. Voer de startdatum voor de uitvoering op verzoek in en klik op Uitvoeren om de synchronisatie uit te voeren. Alle gegevens vanaf de startdatum tot heden worden geïmporteerd.

   * Wanneer de toepassing tijdens de synchronisatie uitvalt, kunt u tijdens de uitvoering klikken op Toegang tot Learning Manager uitschakelen.
   * Als u tijdens de uitvoering op Toegang tot Learning Manager inschakelen klikt, is er geen onderbreking van de service tijdens de synchronisatie.

1. U kunt ook op elk moment op Uitvoeringsstatus in het linkerdeelvenster klikken om het overzicht van alle runs voor deze connector in chronologische volgorde te bekijken. U kunt de startdatum en duur van de synchronisatie, het type synchronisatie (of het al dan niet gaat om synchronisatie op verzoek) en de status van de synchronisatie (of de synchronisatie wordt uitgevoerd of is voltooid) bekijken.

   Wanneer u een verbinding wist en opnieuw aanmaakt, worden de vorige runs voor de connector weergegeven. U kunt alle runs bekijken voordat u de verbinding wist.

   U kunt alleen de laatste synchronisatie opnieuw uitvoeren.

   Zorg er voor elk type synchronisatie voor dat de gebruikersfeed aanwezig is in de getAbstract FTP-map voor de gegevens die in de synchronisatie zijn gespecificeerd.

   Raadpleeg het volgende Excelblad met een voorbeeld van een gebruikersfeed-bestand van getAbstract. De bestandsnaam moet de volgende indeling hebben:** report_export_yyyy_MM_dd_HHmmss.xlsx** of **report_export_jjjj_MM_dd.xlsx**.
   [Voorbeeld van Excel-blad voor getAbstract-gebruikersinvoer](assets/report-export-20170401175342.xlsx)

## Harvard ManageMentor-connector {#hmmconnector}

De Harvard ManageMentor-connector kan worden gebruikt door zakelijke klanten van Harvard ManageMentor die graag willen dat hun studenten Harvard ManageMentor-cursussen kunnen zoeken en volgen. De connector helpt bij het maken van cursussen binnen Learning Manager en kan worden geconfigureerd om periodiek de voortgangsgegevens van studenten op te halen. Voer de volgende procedure uit om deze connector te configureren:

### De Harvard ManagerMentor-connector configureren {#configuretheharvardmanagermentorconnector}

1. Klik in het dashboard van de integratiebeheerder op Harvard ManageMentor.

   U ziet de tegel met drie verschillende opties: Aan de slag, Verbinden en Verbindingen beheren.

1. Klik op Verbinden als u de Harvard ManageMentor-connector voor het eerst configureert.

   U moet ook het Exavault FTP-account configureren voordat u deze connector configureert.

   Zorg ervoor dat u deze FTP-gegevens deelt met uw inhoudaanbieder om toegang te krijgen tot de feeds.

1. Voer in het veld Verbindingsnaam een naam voor uw verbinding in. Klik op Verbinden om deze verbinding op te slaan.
1. Klik als u al verbinding hebt op de startpagina op Harvard ManageMentor > Verbindingen beheren. Klik op de verbinding die u wenst te bewerken.

   De migratiefunctie moet zijn ingeschakeld voor uw account voordat u deze connector kunt configureren.

   ![](assets/hmm.png)

1. Klik in het linkerdeelvenster op Configureren. Voer een van de volgende handelingen uit:

   * Bekijk of bewerk de details van uw account en het synchronisatieschema vanuit dit venster. Selecteer het selectievakje Verbinding inschakelen om dit account in te schakelen.
   * Klik op Schema inschakelen om uw synchronisatie te plannen. U kunt de starttijd en -datum invoeren en vervolgens de frequentie van uw synchronisatieplanning in dagen invoeren. Bijvoorbeeld, om de drie dagen synchroniseren.

1. Klik in het linkerdeelvenster op Uitvoering op verzoek. Met deze optie kunt u gebruikersfeeds en andere relevante gegevens uit Harvard ManageMentor importeren. Voer de startdatum voor de uitvoering op verzoek in en klik op Uitvoeren om de synchronisatie uit te voeren. Alle gegevens vanaf de startdatum tot heden worden voor deze verbinding geïmporteerd.

   * Wanneer de toepassing tijdens de synchronisatie uitvalt, kunt u tijdens de uitvoering klikken op Toegang tot Learning Manager uitschakelen.
   * Als u tijdens de uitvoering op Toegang tot Learning Manager inschakelen klikt, is er geen onderbreking van de service tijdens de synchronisatie.

   Als u de synchronisatie om de paar dagen wilt automatiseren, geef dan het aantal dagen op in het veld Herhaal aantal dagen. Synchronisatie zorgt ervoor dat uw account wordt bijgewerkt met de laatste versie van de abstracts en samenvattingen van Harvard ManageMentor.

1. U kunt ook op elk moment op Uitvoeringsstatus in het linkerdeelvenster klikken om het overzicht van alle runs voor deze connector in chronologische volgorde te bekijken. U kunt de startdatum en duur van de synchronisatie, het type synchronisatie (of het al dan niet gaat om synchronisatie op verzoek) en de status van de synchronisatie (of de synchronisatie wordt uitgevoerd of is voltooid) bekijken.

   Wanneer u een verbinding wist en opnieuw aanmaakt, worden de vorige runs voor de connector weergegeven. U kunt alle runs bekijken voordat u de verbinding wist.

   U kunt alleen de laatste synchronisatie opnieuw uitvoeren.

   Om de synchronisatie te laten slagen, moet u ervoor zorgen dat ten minste één van de volgende bestanden aanwezig is in de FTP-map van Harvard ManageMentor:

   hmm12_metadata.xlsx: Dit bestand geeft de cursusmetagegevens voor de Harvard ManageMentor-connector. Zorg ervoor dat u de naamconventie volgt wanneer u het bestand uploadt.

   client_hmm12_20150125.xlsx: dit is de gebruikersfeed voor de Harvard ManageMentor-connector. De bestandsnaamconventie die u moet volgen, is **client_hmm12_yyyyMMMdd.xlsx.**

   Zie de volgende twee voorbeelden van gebruikersfeed- en cursusfeed-bestanden voor deze connector:
   [Cursusmetagegevensbestand voor de Harvard ManageMentor-connector](assets/hmm12-metadata.xlsx) [Gebruikersfeed voor de Harvard ManageMentor-connector](assets/client-hmm12-20170304.xlsx)

## Workday-connector {#workdayconnector}

Met behulp van de Workday-connector kunt u Learning Manager integreren met Workday tenant om de synchronisatie van gegevens te automatiseren.

### Importeren

#### Kenmerken toewijzen

De integratiebeheerder kan Workday-kolommen kiezen en aan de overeenkomstige groepeerbare kenmerken van Learning Manager toewijzen. Dit is een eenmalige handeling. Wanneer de toewijzing is voltooid, wordt dezelfde toewijzing voor verdere gebruikersimporten gebruikt. De beheerder kan de toewijzing opnieuw configureren als deze een andere toewijzing voor het importeren van gebruikers wil.

#### Geautomatiseerde gebruikersimport

Met het gebruikersimportproces kan de Learning Manager Administrator werknemersgegevens uit Workforce halen en ze automatisch in Learning Manager importeren.

#### Gebruikers filteren

Learning Manager Administrator kan gebruikers filteren voordat ze worden geïmporteerd. Zo kan de Learning Manager-beheerder er bijvoorbeeld voor kiezen om alle gebruikers in de hiërarchie onder één of meer specifieke managers te importeren.

## Exporteren

Via Gebruikersvaardigheden exporteren kunnen gebruikers automatisch gebruikersvaardigheden naar Workday exporteren.

Het is niet mogelijk vaardigheden van meerdere Learning Manager-accounts tegelijkertijd met hetzelfde Workday-account te exporteren.

## Planning {#Scheduling-1}

De beheerder kan planningstaken volgens de vereisten van de organisatie instellen en gebruikers in de Learning Manager-toepassing zijn up-to-date volgens de planning. Op dezelfde manier kan de integratiebeheerder de export van vaardigheden op een tijdige basis plannen om deze te integreren met een extern systeem. De synchronisatie kan dagelijks worden uitgevoerd in de Learning Manager-toepassing.

## De Workday-connector configureren {#configureworkdayconnector}

**Voorwaarde**: vraag de Workday-beheerder van uw organisatie om een integratiesysteemgebruiker (ISU) aan te maken met de toestemmingen zoals gedefinieerd in het document ISU_Permissions. Download een kopie via de onderstaande koppeling.
[Download een kopie van de beveiliging van het integratiesysteem voor gebruikers (ISU).](assets/isu-permissions-v1.pdf) Leer het proces om Learning Manager te integreren met de Workday-connector.

1. Beweeg de muis over de tegel van Workday op de startpagina van Learning Manager. Er verschijnt een menu. Klik op **[!UICONTROL Verbinden]** in het menu.

   ![](assets/workday-tile.png)

1. Er verschijnt een dialoogvenster waarin u wordt gevraagd de gegevens voor de nieuwe verbinding in te voeren. De volgende velden zijn de velden die u moet invoeren voordat u de verbinding tot stand brengt.

   * Verbindingsnaam: voer een verbindingsnaam naar keuze in.
   * Host-URL: de integratiebeheerder kan de host-URL-details bij de desbetreffende Workday-beheerder opvragen.
   * Tenant: de tenant is intern in uw bedrijf. U ontvangt de gegevens van de tenant van de Workday-beheerder.
   * Gebruikersnaam en wachtwoord: De Workday-beheerder maakt een geïntegreerde systeemgebruiker (ISU) met de vereiste beveiligingsrechten en deelt deze met de integratiebeheerder.

   Opmerking: Learning Manager gebruikt versie 28.1 van de Workday-API.

   ![](assets/configure-connector.png)

1. Klik op Verbinden na het invoeren van informatie in alle relevante velden.

   U kunt ook meerdere Workday-verbindingen laten synchroniseren met uw Learning Manager-account.

Op de overzichtspagina kunt u de verbindingsnaam voor uw integratie opgeven. Kies uit de volgende opties welke actie u wilt ondernemen:

* Interne gebruikers importeren
* Vaardigheden van gebruikers exporteren - Een planning configureren
* Vaardigheden van gebruikers exporteren - Op verzoek

![](assets/overview.png)

## Importeren

### Kenmerken toewijzen {#MapAttributes-1}

U kunt de Workday-connector gebruiken om Learning Manager en Workday te integreren om de synchronisatie van gegevens te automatiseren. U kunt alle actieve gebruikers van Workday naar Learning Manager importeren. Gebruikers kunnen worden geïmporteerd vanuit verschillende gegevensbronnen, waaronder FTP en Salesforce.

Voordat gebruikers kunnen worden geïmporteerd, moeten de gebruikersattributen van Learning Manager en Workday worden toegewezen. Kies op de overzichtspagina onder Importeren voor de optie Interne gebruikers om de toewijzingsattributen op te geven.

Voer de Adobe Learning Manager-gegevens in de kolom onder Adobe Learning Manager. Gebruik de vervolgkeuzelijsten om de juiste gegevens te selecteren voor de kolommen onder Workday.

Momenteel ondersteunt Learning Manager het importeren van 44 gebruikersattributen uit Workday. Voeg via de actieve velden in Learning Manager meer attributen toe.

![](assets/map-attributes.png)

Workday heeft vier hiërarchische niveaus terwijl Learning Manager twee niveaus heeft. De vier niveaus in Workday zijn vaardigheidsprofielcategorie, vaardigheidsprofiel, vaardigheidsitemcategorie en vaardigheidsitem. Uw vaardigheidsnaam en niveau van Leermanager worden samen toegewezen in Workday onder het vaardigheidsitem.

+++Lijst met ondersteunde Workday-kenmerken

wd:User_ID\
wd:Worker_ID\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.@wd:Opgemaakte_naam\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.@wd:Opgemaakte_naam\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:Prefix_Data.wd:Title_Descriptor\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:Prefix_Data.wd:Title_Descriptor\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:First_Name\
wd:Personal_Data.wd:Name_Data.wd:Preferred_Name_Data.wd:Name_Detail_Data.wd:Last_Name\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:First_Name\
wd:Personal_Data.wd:Name_Data.wd:Legal_Name_Data.wd:Name_Detail_Data.wd:Last_Name\
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.@wd:Formatted_Address\
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Postal_Code\
wd:Personal_Data.wd:Contact_Data.wd:Address_Data.0.wd:Country_Region_Descriptor\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.@wd:Opgemaakte_telefoon\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:Country_ISO_Code\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:International_Phone_Code\
wd:Personal_Data.wd:Contact_Data.wd:Phone_Data.0.wd:Phone_Number\
wd:Personal_Data.wd:Primary_Nationality_Reference.wd:ID.1.$\
wd:Personal_Data.wd:Gender_Reference.wd:ID.1.$\
wd:Personal_Data.wd:Identification_Data.wd:National_ID.0.wd:National_ID_Data.wd:ID\
wd:Personal_Data.wd:Identification_Data.wd:Custom_ID.0.wd:Custom_ID_Data.wd:ID\
wd:User_Account_Data.wd:Default_Display_Language_Reference.wd:ID.1.$\
wd:Role_Data.wd:Organization_Role_Data.wd:Organization_Role.0.wd:Organization_Role_Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Position_Title\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Title\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Name\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Business_Site_Summary_Data.wd:Address_Data.@wd:Formatted_Address\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Classification_Summary_Data.0.wd:Job_Classification_Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Job_Classification_Summary_Data.0.wd:Job_Group_Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Job_Data.0.wd:Position_Data.wd:Work_Space__Reference.wd:ID.1.$\
wd:Employment_Data.wd:Worker_Status_Data.wd:Active\
wd:Employment_Data.wd:Worker_Status_Data.wd:Active_Status_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Hire_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Original_Hire_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Gearchiveerd\
wd:Employment_Data.wd:Worker_Status_Data.wd:Retirement_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Terminated\
wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Date\
wd:Employment_Data.wd:Worker_Status_Data.wd:Termination_Last_Day_of_Work\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Code\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Name\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Type_Reference.wd:ID.1.$\
wd:Organization_Data.wd:Worker_Organization_Data.0.wd:Organization_Data.wd:Organization_Subtype_Reference.wd:ID.1.$\
wd:Qualification_Data.wd:Education.0.wd:School_Name\
wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Job_Title\
wd:Qualification_Data.wd:External_Job_History.0.wd:Job_History_Data.wd:Company\
wd:Management_Chain_Data.wd:Worker_Surveillance_Management_Chain_Data.wd:Management_Chain_Data.0.wd:Manager.Employee_ID

+++

## Exporteren

U kunt alle vaardigheden van een gebruiker van Learning Manager naar Workday exporteren. Let op: alleen actieve gebruikersvaardigheden worden geëxporteerd en Learning Manager exporteert geen gearchiveerde vaardigheden. U kunt ook meerdere Learning Manager-accounts aansluiten op dezelfde Workday-connector. Als de vaardigheidsnamen in twee Learning Manager-accounts hetzelfde zijn, worden ze toegewezen aan dezelfde vaardigheid in Workday. Het is raadzaam vaardigheidsnamen in alle Leermanaccounts bij te werken voordat u de vaardigheid in Workday bijwerkt voor het geval twee Learning Manager-accounts hetzelfde Workday-account gebruiken.

+++Gebruikersvaardigheden - Configureren

Met deze optie kunt u de extractie van het rapport plannen. Zorg ervoor dat het selectievakje Exporteren van gebruikersvaardigheden via deze verbinding inschakelen is ingeschakeld. Selecteer het selectievakje Planning inschakelen en geef de begindatum en -tijd op. U kunt ook aangeven met welke intervallen u het rapport wilt laten genereren en verzenden. Schakel het selectievakje Planning inschakelen in en voer de startdatum, tijd en herhaling na een bepaald aantal dagen in. Klik op Opslaan als u klaar bent.

![](assets/configure-schedule.png)

+++

++ + Gebruikersvaardigheden - Op verzoek

U kunt de begindatum opgeven en het rapport exporteren met deze optie. Het rapport wordt geëxtraheerd van de ingevoerde datum tot heden. Voer de datum in vanaf wanneer u wilt beginnen met het genereren van het rapport en klik op Uitvoeren.

![](assets/on-demand-report.png)

+++

++ + Gebruikersvaardigheden - Uitvoeringsstatus

Hier kunt u de samenvatting van alle taken bekijken en een statusrapport daarvan ontvangen. U kunt foutrapporten downloaden door op de foutrapportagelink te klikken.

![](assets/execution-status.png)

+++

## miniOrange-connector {#miniorangeconnector}

Met behulp van de miniOrange-connector kunt u Learning Manager integreren met miniOrange-tenant om de synchronisatie van gegevens te automatiseren.

### Importeren

#### Kenmerken toewijzen

De integratiebeheerder kan miniOrange-kenmerken kiezen en deze toewijzen aan de overeenkomstige groepeerbare kenmerken van de Learning Manager. Dit is een eenmalige handeling. Wanneer de toewijzing is voltooid, wordt dezelfde toewijzing voor verdere gebruikersimporten gebruikt. De beheerder kan de toewijzing opnieuw configureren als deze een andere toewijzing voor het importeren van gebruikers wil.

#### Geautomatiseerde gebruikersimport

Via het gebruikersimportproces kan de beheerder van de leermanager werknemersgegevens ophalen uit miniOrange en deze automatisch importeren in Learning Manager.

#### Gebruikers filteren

Learning Manager Administrator kan gebruikers filteren voordat ze worden geïmporteerd. Zo kan de Learning Manager-beheerder er bijvoorbeeld voor kiezen om alle gebruikers in de hiërarchie onder één of meer specifieke managers te importeren.

Neem contact op met het CSM-team van Learning Manager om een miniOrange-connector in te stellen.

## De miniOrange-connector configureren {#configureminiorangeconnector}

1. Beweeg de muis over de miniOrange-kaart/miniatuur op de startpagina van Learning Manager. Er verschijnt een menu. Klikken  **[!UICONTROL Verbinden]** in het menu.

   ![](assets/miniorange-tile.png)

1. Klik op Verbinden om een nieuwe verbinding tot stand te brengen. De miniOrange-connector-pagina wordt weergegeven. Vul de gegevens in van het account dat u wilt toewijzen.

   ![](assets/establish-connection.png)

1. Als u een miniOrnage-gebruiker rechtstreeks wilt importeren als interne gebruiker van de Learning Manager, gebruikt u de **[!UICONTROL Interne gebruikers importeren]** gebruiken.

   ![](assets/import-users.png)

1. Op de toewijzingspagina ziet u links de kolommen van de Leermanager en rechts de miniOrnage-kolommen. Selecteer de juiste kolomnaam die is toegewezen aan de kolomnaam van de leermanager.

   ![](assets/map-attributes.png)

1. Klik, als u de gegevensbron als beheerder wilt bekijken bewerken, op **[!UICONTROL Instellingen > Gegevensbron]**.

   De vastgestelde miniOrange-bron wordt vermeld. Als u het filter wilt bewerken, klikt u op **[!UICONTROL Bewerken]**.

   ![](assets/data-source.png)

1. U ontvangt een melding na voltooiing van de import. Klik op **[!UICONTROL Gebruikers > Importlogboek]** om het importlogboek te bekijken of te bewerken.

### Een verbinding verwijderen {#deleteaconnection}

Ga als volgt te werk om een bestaande miniOrange-verbinding te verwijderen.

## BlueJeans-connector {#bluejeansconnector}

U kunt de Learning Manager nu integreren met de BlueJeans-connector en BlueJeans gebruiken om lessen te hosten. In BlueJeans kunt u audio- en videovergaderingen, videochats en webinars starten.

Volg deze stappen om de connector in te stellen en te gebruiken.

1. Beweeg de muis over de BlueJeans-kaart/miniatuur op de startpagina van Learning Manager. Er verschijnt een menu. Klikken  **[!UICONTROL Verbinden]** in het menu.

   ![](assets/miniorange.png)

1. De BlueJeans-connectorpagina wordt geopend. Voer de gegevens van uw account in de respectievelijke velden in om Learning Manager en BlueJeans te integreren voor synchronisatie van de gebruikersfeed. U kunt de gegevens van de beheerder van uw BlueJeans-account opvragen.

   ![](assets/bluejeans-connecotrpage.png)

   Als student gebruikt u bij het inschakelen van de connector dezelfde e-mail-ID die gebruikt wordt voor uw Learning Manager-account om gebruikersfeeds terug te laten keren naar Learning Manager.

1. Zodra de verbinding tot stand is gebracht, kunnen auteurs een VC-cursus maken met BlueJeans/ als conferentiesysteem.

   ![](assets/conferencing-systems.png)

1. Beheerders, managers en studenten kunnen studenten voor de gemaakte cursus inschrijven. Bij inschrijving ontvangt de student een e-mail. De student kan zich aanmelden op zijn Learning Manager-account om de details van het programma te bekijken en de cursus te volgen.
1. Na afloop van de cursus wordt het eindrapport naar Learning Manager gestuurd. De beheerder kan het voltooiingsrapport bekijken om de aanwezigheid en de score van de studenten te controleren.

   ![](assets/-attendence-and-scoringreport.png)

## Box-connector {#boxconnector}

Met de BOX-connector kunt u Learning Manager integreren met willekeurige externe systemen om de synchronisatie van gegevens te automatiseren. Verwacht wordt dat externe systemen gegevens kunnen exporteren in een CSV-indeling en deze in de juiste map van het Learning Manager Box-account kunnen plaatsen. De mogelijkheden van de Box-connector zijn als volgt:

U kunt de FTP-connector ook gebruiken voor gegevensmigratie, gebruikersimport en gegevensexport. Ga voor meer informatie naar [Learning Manager FTP-connector.](third-party-connectors.md#main-pars_header_1427405935)

## Gegevensimport {#DataImport-1}

Met het gebruikersimportproces kan de Learning Manager Administrator werknemersgegevens uit de Learning Manager Box-service halen en ze automatisch in Learning Manager importeren. Met behulp van deze functie kunt u meerdere systemen integreren door de door deze systemen gegenereerde CSV in de juiste mappen van de Box-accounts te plaatsen. Learning Manager haalt de CSV-bestanden op, voegt ze samen en importeert de gegevens volgens de planning. Raadpleeg de planningsfunctie voor meer informatie.

**Kenmerken toewijzen**

Kenmerken toewijzen Deze toewijzing is een eenmalige inspanning. Zodra de toewijzing gereed is, wordt dezelfde toewijzing gebruikt in volgende gebruikersimports. De toewijzing kan opnieuw worden geconfigureerd als de beheerder een andere toewijzing voor het importeren van gebruikers wil hebben.

## Gegevensexport {#dataexport}

Gegevensexport stelt gebruikers in staat om de vaardigheden van de gebruiker te exporteren naar een Box-locatie om deze te integreren met een willekeurig systeem van derden.

## Rapporten plannen {#schedulereports}

De beheerder kan planningstaken volgens de vereisten van de organisatie instellen en gebruikers in de Learning Manager-toepassing zijn up-to-date volgens de planning. Op dezelfde manier kan de integratiebeheerder de export van vaardigheden op een tijdige basis plannen om deze te integreren met een extern systeem. De synchronisatie kan dagelijks worden uitgevoerd in de Learning Manager-toepassing.

## Box-connector configureren {#configureboxconnector}

Leer het proces kennen om Learning Manager te integreren met de Box-connector.

1. Beweeg de muis over de Box-kaart/miniatuur op de startpagina van Learning Manager. Er verschijnt een menu. Klik op Verbinden in het menu.

   ![](assets/screen-shot-2017-10-25at54426pm.png)

1. Er verschijnt een dialoogvenster waarin u wordt gevraagd de e-mail-ID in te voeren. Geef de e-mail-ID op van de persoon die verantwoordelijk is voor het beheer van het Box-account voor de organisatie. Klik op Verbinden nadat u de e-mail-ID hebt opgegeven.

1. Learning Manager stuurt u een e-mail waarin de gebruiker wordt gevraagd het wachtwoord opnieuw in te stellen voordat hij/zij voor het eerst toegang krijgt tot de Box. De gebruiker moet het wachtwoord opnieuw instellen en dit gebruiken om toegang te krijgen tot het Box-account van de Learning Manager.

   Er kan slechts één Learning Manager Box-account worden gemaakt voor een bepaald Learning Manager-account.

   Op de overzichtspagina kunt u de verbindingsnaam voor uw integratie opgeven. Kies uit de volgende opties welke actie u wilt ondernemen:

   * Interne gebruikers importeren
   * Vaardigheden van gebruikers exporteren - Een planning configureren
   * Vaardigheden van gebruikers exporteren - Op verzoek

## Importeren

+++Interne gebruiker

Met de optie voor het importeren van interne gebruikers kunt u het genereren van een gebruikersimportverslag automatisch plannen. De gegenereerde rapporten worden als .CSV-bestanden naar u verzonden.

+++

+++Kenmerken Kaart

Zodra een verbinding tot stand is gebracht, kunt u de kolommen van CSV-bestanden die in de Box-map worden geplaatst, toewijzen aan de overeenkomstige kenmerken van Leerbeheer. Deze stap is verplicht.

1. Op de pagina Kenmerken toewijzen ziet u links de verwachte kolommen van de leermanager en rechts de CSV-kolomnamen. In eerste instantie ziet u aan de rechterkant een leeg selectievakje. Importeer een CSV-sjabloon door op Bestand kiezen te klikken.

1. Via de bovenstaande stap worden alle CSV-kolomnamen aan de rechterkant van de vervolgkeuzelijst ingevuld. Selecteer de juiste kolomnaam die is toegewezen aan de kolomnaam van de leermanager.

   *Het veld Manager moet worden toegewezen aan een veld van het type e-mailadres. U moet alle kolommen toewijzen voor u de connector kunt gebruiken.*

1. Klik op Opslaan nadat u de toewijzing hebt voltooid.

   De connector is nu klaar voor gebruik. Het geconfigureerde account verschijnt nu als gegevensbron in de beheerdersapp zodat de beheerder de import of de synchronisatie op verzoek kan plannen.

+++

+++Interface van de Learning Manager Box-connector

1. De CSV-bestanden van externe systemen moeten op het volgende pad worden geplaatst:

   `code $OPERATION$/$OBJECT_TYPE$/$SUB_OBJECT_TYPE$/data.csv`

   **Opmerking:** In de release van juli 2016 is alleen import van gebruikers toegestaan. Als u de Box-connector wilt gebruiken, moet u ervoor zorgen dat de CSV-bestanden in de volgende map worden geplaatst:\
   `code Home/import/user/internal/*.csv`

1. De Box-connector haalt alle rijen uit CSV-bestanden, dus het is belangrijk dat de rij die overeenkomt met een gebruiker in een CSV niet wordt weergegeven in andere CSV&#39;s.
1. Alle CSV&#39;s moeten de kolommen bevatten die in de toewijzing zijn opgegeven.
1. Alle vereiste CSV&#39;s moeten aanwezig zijn in de map voordat het proces begint.

Bij het importeren van gebruikers in Learning Manager, moet de beheerder ook weten hoe gebruikers in Learning Manager beheerd worden. Raadpleeg [Help bij gebruikersbeheer](../integration-admin/feature-summary/migration-manual.md#usermanagement) voor meer informatie.

+++

## Badge als

+++Vaardigheden

Er zijn twee opties om vaardigheidsrapporten van de gebruiker te exporteren.

Gebruikersvaardigheden - Op verzoek: u kunt de startdatum opgeven en het rapport exporteren met de optie. Het rapport wordt geëxtraheerd vanaf de ingevoerde datum tot heden

**[!UICONTROL Gebruikersvaardigheden - Configureren]**: via deze optie kunt u de extractie van het rapport plannen. Selecteer het selectievakje Planning inschakelen en geef de begindatum en -tijd op. U kunt ook aangeven met welke intervallen u het rapport wilt laten genereren en verzenden.

+++

Als u de Exportmap wilt openen waar de geëxporteerde bestanden op uw Box-locatie worden geplaatst, opent u de koppeling naar Box-map op de pagina Gebruikersvaardigheden, zoals hieronder weergegeven.

De automatisch geëxporteerde bestanden zijn aanwezig op de locatie **Home/export/&#42;Box_location&#42;**

De automatisch geëxporteerde bestanden zijn beschikbaar met de titel, **skill_results__&#42;datum vanaf &#42;_aan_&#42;datum tot&#42;.csv**

De toegangsrechten en de inhoud in de Box-map die door het Leerbeheerteam wordt gedeeld, moeten door de klant worden beheerd.  Houd er ook rekening mee dat de inhoud in de map fysiek wordt opgeslagen in de regio Frankfurt.

## LinkedInLearning-connector {#linkedinlearningconnector}

De LinkedInLearning-connector kan worden gebruikt door zakelijke klanten van LinkedIn.com die graag willen dat hun studenten cursussen kunnen zoeken en volgen in Learning Manager. De connector kan worden geconfigureerd om periodiek cursussen op te halen met uw API-sleutel. Zodra een cursus binnen Learning Manager is gemaakt, kunnen gebruikers deze opzoeken en volgen. De voortgang van de student kan vervolgens binnen Learning Manager worden bijgehouden.

### LinkedIn-connector configureren {#configurelinkedinconnector}

1. Klik in het dashboard van de integratiebeheerder op LinkedInLearning.

   U ziet de tegel met drie opties: Aan de slag, Verbinden en Verbindingen beheren.

1. Klik op Verbinden als u de LinkedInLearning-connector voor het eerst configureert.

   U moet het Exavault FTP-account configureren voordat u deze connector configureert.

1. Geef op de verbindingspagina een naam op voor uw connector. Voer de appsleutel en de geheime sleutel voor uw verbinding in.

   Neem contact op met uw leverancier om de appkey en de geheime sleutel op te halen.

1. Klik op Opslaan.

   De configuratie wordt opgeslagen en de LinkedInLearning-verbinding voor uw account wordt toegevoegd. U kunt nu vanaf de startpagina op Verbindingen beheren klikken en uw configuratie op elk gewenst moment bewerken.

1. Als u al een verbinding tot stand hebt gebracht, klikt u op Verbindingen beheren om al uw verbindingen te bekijken.

   De migratiefunctie moet zijn ingeschakeld voor uw account voordat u deze connector kunt configureren.

1. Klik op de verbinding die u wilt bewerken.
1. Klik in het linkerdeelvenster op Configureren. Voer een van de volgende handelingen uit:

   * Bekijk of bewerk de details van uw account en het synchronisatieschema vanuit dit venster. Selecteer het selectievakje Verbinding inschakelen om dit account in te schakelen.
   * Klik op Bewerken en bewerk uw gegevens. Klik op Herstellen om uw updates voor dit veld ongedaan te maken.
   * Klik op Schema inschakelen om uw synchronisatie te plannen. U kunt de starttijd en -datum invoeren en vervolgens de frequentie van uw synchronisatieplanning in dagen invoeren. Bijvoorbeeld, om de drie dagen synchroniseren.

   Klik op Opslaan om uw wijzigingen op te slaan.

1. Klik in het linkerdeelvenster op Uitvoering op verzoek. Met deze optie kunt u gebruikersfeeds en andere relevante gegevens vanuit LinkedIn importeren. Voer de startdatum in voor de uitvoering op verzoek en klik op Uitvoeren om de synchronisatie uit te voeren. Alle gegevens vanaf de startdatum tot heden worden geïmporteerd.

   * Wanneer de toepassing tijdens de synchronisatie uitvalt, kunt u tijdens de uitvoering klikken op Toegang tot Learning Manager uitschakelen.
   * Als u tijdens de uitvoering op Toegang tot Learning Manager inschakelen klikt, is er geen onderbreking van de service tijdens de synchronisatie.

1. U kunt ook op elk moment op Uitvoeringsstatus in het linkerdeelvenster klikken om het overzicht van alle runs voor deze connector in chronologische volgorde te bekijken. U kunt de startdatum en duur van de synchronisatie, het type synchronisatie (of het al dan niet gaat om synchronisatie op verzoek) en de status van de synchronisatie (of de synchronisatie wordt uitgevoerd of is voltooid) bekijken.

   Wanneer u een verbinding wist en opnieuw aanmaakt, worden de vorige runs voor de connector weergegeven. U kunt alle runs bekijken voordat u de verbinding wist.

   U kunt alleen de laatste synchronisatie opnieuw uitvoeren.

