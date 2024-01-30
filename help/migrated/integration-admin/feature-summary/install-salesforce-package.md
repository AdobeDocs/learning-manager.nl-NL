---
jcr-language: en_us
title: Het Salesforce-pakket installeren
description: Learning Manager biedt een Salesforce App-pakket. Na de installatie en configuratie in SFDC kunnen verkoopmedewerkers hun trainingsactiviteiten uitvoeren in de SFDC-portal. Met deze app kunnen SFDC-gebruikers nieuwe trainingen verkennen, aanbevelingen bekijken en deze rechtstreeks in de SFDC-portal gebruiken. Gebruikers ontvangen de aankondigingen die door beheerders worden verzonden in de vorm van mastheads rechtstreeks binnen de app in de SFDC-portal.
contentowner: saghosh
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 51%

---



# Het Salesforce-pakket installeren

## Overzicht

Learning Manager biedt een Salesforce App-pakket. Na de installatie en configuratie in SFDC kunnen verkoopmedewerkers hun trainingsactiviteiten uitvoeren in de SFDC-portal. Met deze app kunnen SFDC-gebruikers nieuwe trainingen verkennen, aanbevelingen bekijken en deze rechtstreeks in de SFDC-portal gebruiken. Gebruikers ontvangen de aankondigingen die door beheerders worden verzonden in de vorm van mastheads rechtstreeks binnen de app in de SFDC-portal.

### Instellen in de Learning Manager-app.

1. Meld u als integratiebeheerder bij uw Learning Manager-beheerdersaccount aan.
1. Klikken **[!UICONTROL Toepassingen]** > **[!UICONTROL Aanbevolen apps]**.
1. Klikken **[!UICONTROL Salesforce]**.
1. Let op de toepassingspagina van Salesforce op de toepassings-id (ook wel client-id genoemd) en het clientgeheim dat in de beschrijving wordt vermeld.
1. Klikken **[!UICONTROL Goedkeuren]** en uw app moet zijn goedgekeurd.
1. Klikken **[!UICONTROL Bronnen voor ontwikkelaars]** > **[!UICONTROL Toegangstokens voor testen en ontwikkelen]**.
1. In de sectie OAuth Code ophalen moeten de client-id en het bereik worden ingesteld op - admin:read,admin:write. Klikken **[!UICONTROL Verzenden]**.
1. Voer bij Vernieuwingstoken ophalen de client-ID en het clientgeheim in. Klikken **[!UICONTROL Verzenden]** en noteer het vernieuwingstoken.

### Account aanmaken in de Salesforce-app

1. Maak een account aan op de aanmeldingspagina van Salesforce. U moet een Salesforce-account maken in de editie voor ontwikkelaars of ondernemingen.  [URL voor ontwikkelaarsaanmelding](https://developer.salesforce.com/signup). Zorg ervoor dat u de e-mail-ID gebruikt om u aan te melden voor Salesforce die u voor Leerbeheer hebt gebruikt.
1. Verifieer uw account via de verificatie-e-mail.
1. Maak een wachtwoord aan en meld u aan bij Salesforce.
1. Noteer de Salesforce-URL na aanmelding (bijvoorbeeld site.lightning.force.com)

### Installeer het Learning Manager-pakket

Als u het pakket wilt installeren, moet u eerst het bestaande pakket in Salesforce verwijderen. Voordat u de installatie ongedaan maakt, moet u de instellingen inschakelen, zoals hieronder weergegeven. U moet deze instellingen toepassen, anders kunt u het pakket niet installeren.

![](assets/uninstall-package.png)

*Het pakket Leerbeheer installeren*

>[!NOTE]
>
>De app Adobe Learning Manager wordt alleen ondersteund in de Salesforce Lightning-weergave.

1. Start de  [Learning Manager-pakket-URL](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Ftest.salesforce.com%2Fpackaging%2FinstallPackage.apexp%3Fp0%3D04t1k0000008YWn&amp;data=04%7C01%7Ckillamse%40adobe.com%7Cf588f553fc694d2edee108d9a5c74711%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C637723097572585825%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=mhYKVdwvS4F7WPruy0Kvw%2FsqgWxzTQpaZJyEACu8CNw%3D&amp;reserved=0).
1. In het dialoogvenster **Aanmelden** pagina, klikken **[!UICONTROL Aangepast domein gebruiken]**.

1. Voer de URL van het pakket in en klik op **[!UICONTROL Doorgaan]**. Op de installatiepagina moet de optie Installeren voor alleen beheerders zijn geselecteerd. Wijzig deze optie niet.
1. Klikken **Inshoog**. Nadat het pakket is geïnstalleerd, klikt u op **[!UICONTROL Gereed]**. U wordt naar de pagina Geïnstalleerde pakketten geleid en u kunt het geïnstalleerde Adobe Learning Manager-pakket zien.

1. Ga naar het startprogramma voor apps (naast Configuratie) en zoek naar Adobe Learning Manager.
1. Klik op **[!UICONTROL Configureren]**.
1. Klikken **[!UICONTROL Nieuw]** en voeg de volgende details toe:

   * **Configuratie:** Voer een naam naar keuze in.
   * **ClientID**: Voer de waarde in die u in de eerste sectie hebt gekregen.
   * **ClientSecret:** Voer de waarde in die u in de eerste sectie hebt gekregen.
   * **Vernieuwingstoken:** Voer de waarde in die u in de eerste sectie hebt gekregen.
   * **LearningManagerBaseURL:** De URL van de site waarop Leerbeheer wordt gehost.
   * **Disable Redirect:** Omleiden naar de studentenstartpagina in Learning Manager uitschakelen.

>[!NOTE]
>
>U kunt slechts één configuratie maken. Als u nog een configuratie probeert toe te voegen, verschijnt er een foutmelding. In de configuratie kunt u het Salesforce-account met het studentenaccount verbinden.

### Instellingen voor externe site toevoegen

1. Klik rechtsboven op de pagina op **[!UICONTROL Instellen]**.
1. In **Snel zoeken**, zoek naar instellingen voor externe site.
1. Klikken **[!UICONTROL Nieuwe externe site]**.
1. Voer de gegevens in:

   1. **Naam van externe site:** Voer een naam naar keuze in.
   1. **Remote Site URL:** De URL van de site waar Learning Manager wordt gehost.

1. Start Learning Manager.

### Schakel meldingen in voor de Learning Manager-app

1. Klik rechtsboven op **Instellen**.
1. Zoek naar aangepaste meldingen.
1. Klikken **[!UICONTROL Nieuw]**.
1. Voer de volgende gegevens in:

   1. **Naam aangepaste melding:** LearningManagerNotification
   1. **API-naam:** LearningManagerNotification

1. Beide selecteren **Desktop** en **Mobiel** als ondersteunde kanalen.

1. Klik op **[!UICONTROL Opslaan]**.
1. Volg de onderstaande stappen om pushmeldingen voor mobiele apparaten in te schakelen:

   1. Installeer de mobiele Salesforce-app op uw mobiele telefoon.
   1. Meld u aan bij de app met uw gegevens.
   1. Ga naar **Instellen** > **Leveringsinstellingen voor meldingen**.
   1. Voeg Salesforce toe voor iOS en Android.

### Deïnstalleer Learning Manager bij Salesforce

1. Ga in de Salesforce-app naar Geïnstalleerde pakketten.
1. Klikken **[!UICONTROL Verwijderen]**.

## Learning Manager configureren voor Salesforce-gebruikers

De Learning Manager-app is ook beschikbaar voor gebruikers die in een Salesforce-account aanwezig zijn. De beheerder van Salesforce kan gebruikers toevoegen op basis van de profielen. De Salesforce-profielen komen overeen met die in Learning Manager. Bijvoorbeeld beheerder, integratiebeheerder, docent enzovoort. De Salesforce-beheerder kan ook een aangepast profiel maken.

### Profiel

Als Salesforce-beheerder kunt u de profielen aan gebruikers toewijzen of een aangepast profiel maken.

>[!NOTE]
>
>De gebruikers moeten zowel in Salesforce als in Leermanager aanwezig zijn.

![](assets/create-profile.png)

*Een profiel toewijzen aan een student*

Wanneer u een student toevoegt, moet u een specifiek profiel aan de student toewijzen. Ga dan naar dat profiel en verleen de vereiste toegang.

Studenten kunnen de app Leermanager alleen weergeven als u de app voor alle studenten inschakelt.

Vervolgens geeft u toegang tot de Learning Manager-app.

![](assets/permission-set.png)

*Machtigingen toevoegen om toegang te krijgen tot de app Learning Manager*

Wanneer u het pakket installeert, wordt een nieuwe machtigingenset gemaakt, **Adobe Leermanager-gebruiker**. Ga naar de machtigingenset en voeg de gebruikers toe.

Selecteer de gebruikers en wijs de betreffende machtigingen toe. De studenten hebben nu toegang tot de Learning Manager-app.

Nu selecteert u een profiel, een standaard profiel van een gebruiker bijvoorbeeld, en klikt u op het profiel. Klikken **[!UICONTROL Bewerken]** en in de **Aangepaste app-instellingen** schakelt u het selectievakje **Adobe Learning Manager**. Hierdoor heeft de student toegang tot de app.

In de vervolgkeuzelijst **Startpagina voor studenten** selecteert u in de sectie **Aangepaste tabbladinstellingen** de optie **[!UICONTROL Standaard ingeschakeld]**.

U moet de app voor alle profielen zichtbaar maken.

Klikken **[!UICONTROL Opslaan]** en de studenten die tot alle profielen behoren, krijgen toegang tot de app Leermanager.
