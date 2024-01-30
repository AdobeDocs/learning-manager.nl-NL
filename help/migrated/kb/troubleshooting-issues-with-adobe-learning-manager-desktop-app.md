---
description: Dit document bevat basistips voor probleemoplossing om enkele van de veelvoorkomende problemen op te lossen die zich voordoen tijdens de installatie en het gebruik van de Learning Manager desktop-app.
jcr-language: en_us
title: Problemen oplossen met de Adobe Learning Manager desktop-app
contentowner: kuppan
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '1447'
ht-degree: 53%

---



# Problemen oplossen met de Adobe Learning Manager desktop-app

Dit document bevat basistips voor probleemoplossing om enkele van de veelvoorkomende problemen op te lossen die zich voordoen tijdens de installatie en het gebruik van de Learning Manager desktop-app.

## Ik kan het volgende niet doen {#iamunabletodothefollowing}

+++Ik kan de Adobe Learning Manager-bureaubladtoepassing niet downloaden

1. Controleer uw internetverbinding en firewallinstellingen.
1. Klik in Sociaal leren op **[!UICONTROL Nieuw bericht]** om een bericht te maken. Als u geen board hebt, maakt u eerst een board.
1. Klik op een van de volgende berichtknopopties die verschijnen om inhoud te maken zoals Schermopname, Audio opnemen, Video opnemen, Learning Manager-galerij. U wordt doorgestuurd naar de pagina van de Adobe Learning Manager desktop-app vanwaar u de Learning Manager desktop-app voor uw desktop kunt downloaden.
1. U heeft een geldig Adobe Learning Manager-account nodig waarop Sociaal leren is ingeschakeld door uw beheerder. Uw beheerder heeft mogelijk ook downloads uitgeschakeld via de webbrowser. Neem contact op met uw Adobe Learning Manager-beheerder voor meer informatie over het downloaden van de Adobe Learning Manager desktop-app.

+++

+++Ik kan de Adobe Learning Manager-bureaubladtoepassing niet installeren

1. Zorg ervoor dat uw systeem aan de minimale systeemvereisten voldoet. Zie [Systeemvereisten voor Adobe Learning Manager-app voor desktop](../learners/adobe-learning-manager-app-for-desktop/adobe-learning-manager-desktop-app-system-requirements.md).
1. Verwijder elke eerdere installatie van de Adobe Learning Manager desktop-app. Zie voor meer informatie  [Eerdere installaties opschonen](#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp) voor meer informatie.
1. Zie voor fouten tijdens het installatieproces [Toepassingslogboeken zoeken](#howtofindapplicationlogs). Neem contact op met uw Adobe Learning Manager-beheerder voor verdere ondersteuning.

+++

+++Ik kan de Adobe Learning Manager-bureaubladtoepassing niet starten

1. Zorg ervoor dat de Adobe Learning Manager desktop-app gedownload en geïnstalleerd is.
1. Klik in Sociaal leren op **[!UICONTROL Nieuw bericht]** (als u geen geregistreerd bord heeft, maakt u eerst een bord) Klik op een van de volgende opties voor de postknop die worden weergegeven: Screenshot maken, Audio-opname, Video-opname, Adobe Leerbeheergalerie. U wordt doorgestuurd naar een pagina vanwaar u de Adobe Learning Manager desktop-app kunt downloaden.
1. Als de app niet wordt gestart, kunt u deze ook starten via het menu Start in Windows of vanuit Launchpad op Mac OS X.

+++

+++Ik kan me niet aanmelden bij mijn account in de bureaubladtoepassing van Adobe Learning Manager

1. Zorg ervoor dat u verbonden bent met internet en dat uw firewall-instellingen de Adobe Learning Manager desktop-app niet blokkeren.
1. Zorg ervoor dat u een geldig Adobe Learning Manager-leeraccount hebt waarop Sociaal leren is ingeschakeld.
1. Als u zich nog steeds niet kunt aanmelden, moet u de Adobe Learning Manager desktop-app afsluiten en opnieuw starten en vervolgens opnieuw proberen.
1. Neem voor meer hulp contact op met uw Adobe Learning Manager-beheerder.

+++

+++Ik kan mijn webcam/microfoon niet zien in de bureaubladtoepassing van Adobe Learning Manager

1. Zorg ervoor dat uw webcam/microfoon correct is aangesloten op het systeem en naar behoren werkt.
1. Zorg ervoor dat u de nieuwste stuurprogramma&#39;s voor uw webcam/microfoon hebt geïnstalleerd. Sommige apparaten werken niet goed zonder de benodigde stuurprogramma&#39;s.
1. Herstel de voorkeuren van de toepassing en start vervolgens de Adobe Learning Manager desktop-app opnieuw en probeer het nogmaals. Zie [Toepassingsvoorkeuren opnieuw instellen](#howtoresetapplicationpreferences) voor meer informatie.
1. Als u Mac OS X Mojave 10.14 gebruikt, verleent u machtigingen voor de Adobe Learning Manager desktop-app voor toegang tot uw webcam/microfoon. Zie [Webcam-/microfoonmachtigingen instellen voor OSX Mojave](#howtosetwebcammicrophonepermissionsonMacOSXMojave) voor meer informatie.

+++

+++Ik kan mijn berichten niet publiceren vanuit de bureaubladtoepassing van Adobe Learning Manager

1. Zorg ervoor dat u een geldig Adobe Learning Manager-leeraccount hebt waarop Sociaal leren is ingeschakeld door uw Adobe Learning Manager-beheerder.
1. Herstel de voorkeuren van de toepassing en start vervolgens de Adobe Learning Manager desktop-app opnieuw en probeer het nogmaals. Zie voor meer informatie [Toepassingsvoorkeuren opnieuw instellen](#howtoresetapplicationpreferences).
1. Schakel geavanceerde logboekregistratie in voor fouten tijdens het publiceren. Zie [Geavanceerde logboekregistratie inschakelen](#howtoenableadvancedlogging) voor meer informatie, herstart vervolgens de Adobe Learning Manager desktop-app en herhaal de bovenstaande stappen die de fout veroorzaken. Stuur de nieuwste toepassingslogboeken naar uw Adobe Learning Manager-beheerder voor hulp. Zie [Toepassingslogboeken zoeken](#howtofindapplicationlogs) voor meer informatie.

+++

+++Ik kan mijn oudere projecten niet zien of openen

1. U kunt alleen projecten zien die zijn gemaakt met uw Adobe Learning Manager-account, op dezelfde computer waarop ze zijn gemaakt.
1. Herstel de voorkeuren van de toepassing en start vervolgens de Adobe Learning Manager desktop-app opnieuw en probeer het nogmaals. Zie voor Help [Toepassingsvoorkeuren opnieuw instellen](#howtoresetapplicationpreferences).
1. Voor fouten tijdens het openen van projecten schakelt u geavanceerde logboekregistratie in. Zie voor meer informatie [Geavanceerde logboekregistratie inschakelen](#howtoenableadvancedlogging). Start de Adobe Learning Manager desktop-app opnieuw en voer de stappen uit die de fout veroorzaken. Stuur de nieuwste toepassingslogboeken naar uw Adobe Learning Manager-beheerder voor hulp. Zie [Toepassingslogboeken zoeken](#howtofindapplicationlogs) voor meer informatie.

+++

## Toepassingsvoorkeuren opnieuw instellen? {#howtoresetapplicationpreferences}

### Windows {#windows}

1. Als u het dialoogvenster Uitvoeren wilt openen, drukt u op de knop **Windows + R** toetsen.
1. Type `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` en druk op Enter.
1. Verwijder de bestanden met de naam **preferences.json** en **preferences.xml**.

### MAC OS X {#macosx}

1. Open Finder.
1. Als u het dialoogvenster **Ga naar** map, druk op **Cmd + Shift + G** toetsen.
1. Type `**~/Library/Application Support/Adobe/Learning Manager 1.0**` en druk op Enter.
1. Verwijder de bestanden met de naam **preferences.json** en **preferences.xml**.

## Toepassingslogboeken zoeken? {#howtofindapplicationlogs}

### Windows {#application-logs}

1. Druk op **Windows + R** toetsen.
1. Type `**%TEMP%\\elthor**` en druk op Enter.
1. Mappen sorteren op de **Gewijzigd op** en opent u de meest recente map. Deze map bevat de meest recente toepassingslogbestanden.

### MAC OS X {#MacOSX-1}

1. Openen **Finder**.
1. Als u het dialoogvenster **Ga naar map** dialoogvenster, drukken op **Cmd + Shift + G** toetsen.
1. Typ &quot;**/var/folders**&quot; (zonder aanhalingstekens) en druk op Enter.
1. Zoeken naar &quot;**elthor**&quot; in de zoekbalk en open de map.
1. Sorteer de mappen op **Date Modified **en open de meest recente map. Deze map bevat de meest recente toepassingslogbestanden.

## Hoe kan ik geavanceerde logboekregistratie inschakelen? {#howtoenableadvancedlogging}

### Windows {#Windows-1}

1. Druk op **Windows-toets + R**.****
1. Typ &quot;**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**&quot; (zonder offertes) en druk op Enter.***
1. Maak een back-up van het bestand **preferences.json** en opent u deze in een teksteditor.***
1. Zoeken naar de toets **debugMode** en wijzig de waarde-eigenschap van deze sleutel in &quot;**true**&quot; (zonder aanhalingstekens).

### MAC OS X {#MacOSX-2}

1. Open Finder.
1. Als u het dialoogvenster **Ga naar map** dialoogvenster, drukken op **Cmd + Shift + G**.
1. Typ &quot;**~/Library/Application Support/Adobe/Learning Manager 1.0**&quot; (zonder aanhalingstekens) en druk op Enter.
1. Maak een back-up van bestand **preferences.json** en open het bestand vervolgens in een tekstverwerkingsprogramma.
1. Zoeken naar de toets **debugMode** en wijzig de waarde-eigenschap van deze sleutel in &quot;**true**&quot; (zonder aanhalingstekens)

## Hoe stelt u webcam- en microfoonmachtigingen in op Mac OS X Mojave? {#howtosetwebcammicrophonepermissionsonmacosxmojave}

1. Klikken **[!UICONTROL Systeemvoorkeuren]** in Dock.
1. Klikken **[!UICONTROL Beveiliging en privacy]** > **[!UICONTROL Privacy].**
1. Klik op **[!UICONTROL Webcam- en microfoonopties]** en zorg dat het selectievakje Adobe Learning Manager is ingeschakeld. Als Adobe Learning Manager niet wordt vermeld, installeert u eerst de Adobe Learning Manager desktop-app en start u deze.

## Adobe Learning Manager schoonmaken voor cache voor desktopupdates {#howtocleanupadobecaptivateprimefordesktopupdatescache}

### Windows {#clean-previous-installation}

1. Druk op **Windows-toets + R**.
1. Type `**%APPDATA%\\..\\Local\\Adobe\\Learning Manager 1.0**` en druk op Enter.
1. Verwijder de map **Updates**.

### MAC OS X {#MacOSX-3}

1. Open Finder.
1. Als u het dialoogvenster **Ga naar map** dialoogvenster, drukken op **Cmd + Shift + G**.
1. Type `**~/Library/Application Support/Adobe/Learning Manager 1.0**` en druk op Enter.
1. Verwijder de map **Updates**.

## Adobe Learning Manager schoonmaken voor map desktop temp? {#howtocleanupadobecaptivateprimefordesktoptempfolder}

### Windows {#clean-previous-installation-1}

1. Als u het dialoogvenster Run wilt openen, drukt u op **Windows-toets + R**.
1. Typ &quot;**%TEMP%**&quot; (zonder aanhalingstekens) en druk op Enter.
1. Verwijder de map met de naam &quot;**elthor**&quot;.

### MAC OS X {#MacOSX-4}

1. Open Finder.
1. Als u het dialoogvenster **Ga naar map** dialoogvenster, drukken op **Cmd + Shift + G** toetsen.
1. Typ &quot;**/var/folders**&quot; (zonder aanhalingstekens) en druk op Enter.
1. Zoeken naar &quot;**elthor** in de zoekbalk.
1. Verwijder de map met de naam &quot;**elthor**&quot;.

## Adobe Learning Manager zoeken voor desktopprojecten? {#howtolocateadobecaptivateprimefordesktopprojects}

### Windows {#Windows-2}

1. Druk op **Windows-toets + R**.
1. Typ &quot;**~/Documents/My Adobe Learning Manager Projects**&quot; (zonder aanhalingstekens) en druk op Enter.
1. U of uw Adobe Learning Manager-beheerder heeft mogelijk de standaardmaplocatie voor projecten gewijzigd. Neem contact op met uw beheerder voor meer hulp bij het zoeken naar en opschonen van projecten.

### MAC OS X {#MacOSX-5}

1. Open Finder.
1. Als u het dialoogvenster **Ga naar map** dialoogvenster, drukken op **Cmd + Shift + G** toetsen.
1. Typ &quot;**~/Documents/My Adobe Learning Manager Projects**&quot; (zonder aanhalingstekens) en druk op Enter.

   U of uw Adobe Learning Manager-beheerder heeft mogelijk de standaardmaplocatie voor projecten gewijzigd. Neem contact op met uw systeembeheerder voor meer hulp bij het lokaliseren en verwijderen van projecten.

## Eerdere installaties van de Adobe Learning Manager desktop-app verwijderen {#howtocleanuppreviousinstallationsofadobelearningmanagerdesktopapp}

### Windows {#Windows-3}

1. Als u het dialoogvenster **Dialoogvenster Uitvoeren,** drukken **Windows-toetsen + R**.
1. Typ regedit en zoek &quot;**HKEY_LOCAL_MACHINE \\SOFTWARE\\Classes\\Installer\\**&quot; (zonder aanhalingstekens) of &quot;**HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Installer\\UserData\\S-1-5-18\\Products\\**&quot; (zonder aanhalingstekens) en druk op Enter.
1. Zoek de map met de naam Adobe Learning Manager en zoek de vorige installatie. Verwijder het registeritem.  U kunt de sleutel vinden door op de F3-toets te drukken.

### MAC OS X {#MacOSX-6}

Verplaats de bestanden vanaf het volgende pad &quot;**/Applications/Adobe Learning Manager/Users/Shared/Adobe/Learning Manager Assets/1.0**&quot; om de prullenbak te verwijderen en vervolgens de prullenbak leeg te maken.
